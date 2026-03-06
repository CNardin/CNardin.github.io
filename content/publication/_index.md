---
title: Publications
type: landing

sections:
  - block: markdown
    content:
      text: |
        ## Publications
        <div style="display:flex;gap:12px;flex-wrap:wrap;margin-bottom:1rem">
          <select id="yearFilter" style="padding:10px;border-radius:8px">
            <option value="">All years</option>
          </select>

          <select id="typeFilter" style="padding:10px;border-radius:8px">
            <option value="">All types</option>
            <option value="articles">Journal article</option>
            <option value="conferences">Conference</option>
            <option value="preprints">Preprint</option>
          </select>

          <button onclick="resetFilters()" style="padding:10px 14px;border-radius:8px;border:1px solid #bbb;background:white;cursor:pointer">
            Reset filters
          </button>
        </div>

        <div id="tagButtons" style="margin-bottom:1rem"></div>

        <script>
        document.addEventListener("DOMContentLoaded", function(){
          // Increased delay to 1000ms to ensure the collection block is fully rendered
          setTimeout(() => {
            // TARGETING CORRECT CLASS: .pub-list-item is used for 'view: citation'
            const pubs = [...document.querySelectorAll(".pub-list-item")];
            
            if (pubs.length === 0) {
              console.warn("No publications found with .pub-list-item. Trying alternative selectors.");
            }

            // ---------- ADD DATA ATTRIBUTES ----------
            pubs.forEach(p => {
              const text = p.innerText;

              // 1. Extract year
              const yearMatch = text.match(/\b(20\d{2})\b/);
              if (yearMatch) p.dataset.year = yearMatch[1];

              // 2. Detect type from ANY link inside the item
              // We look for the folder names in the href of all links (Title, PDF, Cite, etc.)
              const links = [...p.querySelectorAll("a")].map(a => a.getAttribute("href") || "");
              
              if (links.some(l => l.includes("/articles/"))) {
                p.dataset.type = "articles";
              } else if (links.some(l => l.includes("/conferences/"))) {
                p.dataset.type = "conferences";
              } else if (links.some(l => l.includes("/preprint/"))) {
                p.dataset.type = "preprints";
              }
            });

            // ---------- BUILD YEAR DROPDOWN ----------
            const yearSelect = document.getElementById("yearFilter");
            const years = [...new Set(pubs.map(p => p.dataset.year))]
              .filter(Boolean)
              .sort()
              .reverse();

            years.forEach(y => yearSelect.add(new Option(y, y)));

            // ---------- FILTER FUNCTION ----------
            window.applyFilters = function() {
              const selectedYear = document.getElementById("yearFilter").value;
              const selectedType = document.getElementById("typeFilter").value;

              pubs.forEach(p => {
                let yearMatch = !selectedYear || p.dataset.year === selectedYear;
                let typeMatch = !selectedType || p.dataset.type === selectedType;

                p.style.display = (yearMatch && typeMatch) ? "" : "none";
              });
            };

            window.resetFilters = function() {
              document.getElementById("yearFilter").value = "";
              document.getElementById("typeFilter").value = "";
              applyFilters();
            };

            document.getElementById("yearFilter").onchange = applyFilters;
            document.getElementById("typeFilter").onchange = applyFilters;

          }, 1000);
        });
        </script>

        <style>
        .pub-list-item { margin-bottom: 1rem; }
        </style>

  - block: collection
    content:
      title: ""
      filters:
        folders:
          - publication
        include_subfolders: true
      count: 0
    design:
      view: citation
      sort_by: date
      sort_ascending: false
---