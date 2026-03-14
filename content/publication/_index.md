---
title: Publications
type: landing

sections:
  - block: markdown
    content:
      text: |
        ## Publications
        <div style="display:flex;gap:12px;flex-wrap:wrap;margin-bottom:0.5rem">
          <select id="yearFilter" style="padding:10px;border-radius:8px">
            <option value="">All years</option>
          </select>

          <select id="typeFilter" style="padding:10px;border-radius:8px">
            <option value="">All types</option>
            <option value="paper-article">Journal article</option>
            <option value="paper-conference">Conference</option>
            <option value="preprint">Preprint</option>
            <option value="news">News</option>
          </select>

          <button onclick="resetFilters()" style="padding:10px 14px;border-radius:8px;border:1px solid #bbb;background:white;cursor:pointer">
            Reset filters
          </button>
        </div>

        <script>
        document.addEventListener("DOMContentLoaded", function(){
          setTimeout(() => {
            const pubs = [...document.querySelectorAll(".pub-list-item")];

            pubs.forEach(p => {
              const text = p.innerText;

              // Extract year
              const yearMatch = text.match(/\b(20\d{2})\b/);
              if (yearMatch) p.dataset.year = yearMatch[1];

              // Detect type from href - match publication folder structure
              const links = [...p.querySelectorAll("a")].map(a => a.getAttribute("href") || "");
              if (links.some(l => l.includes("/publication/articles/"))) {
                p.dataset.type = "paper-article";
              } else if (links.some(l => l.includes("/publication/conferences/"))) {
                p.dataset.type = "paper-conference";
              } else if (links.some(l => l.includes("/publication/preprints/"))) {
                p.dataset.type = "preprint";
              } else if (links.some(l => l.includes("/publication/news/"))) {
                p.dataset.type = "news";
              }
            });

            // Build year dropdown
            const yearSelect = document.getElementById("yearFilter");
            const years = [...new Set(pubs.map(p => p.dataset.year))]
              .filter(Boolean).sort().reverse();
            years.forEach(y => yearSelect.add(new Option(y, y)));

            window.applyFilters = function() {
              const selectedYear = document.getElementById("yearFilter").value;
              const selectedType = document.getElementById("typeFilter").value;
              pubs.forEach(p => {
                const yearMatch = !selectedYear || p.dataset.year === selectedYear;
                const typeMatch = !selectedType || p.dataset.type === selectedType;
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

    design:
      spacing:
        padding: ['1rem', '0', '0', '0']

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