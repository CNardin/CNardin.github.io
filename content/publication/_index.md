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
          // Increased delay slightly to ensure Hugo Blox finishes rendering
          setTimeout(() => {
            const pubs = [...document.querySelectorAll(".pub-list-item")];
            console.log("Total publications found:", pubs.length); // Debug check

            // -------- YEAR DROPDOWN --------
            const yearSelect = document.getElementById("yearFilter");
            const years = [...new Set(
              pubs.map(p => (p.innerText.match(/\b20\d{2}\b/) || [])[0])
            )].filter(Boolean).sort().reverse();

            years.forEach(y => yearSelect.add(new Option(y, y)));

            // -------- FILTER ENGINE --------
            window.applyFilters = function() {
              const y = document.getElementById("yearFilter").value;
              const t = document.getElementById("typeFilter").value;
              const activeTags = [...document.querySelectorAll(".tagbtn.active")].map(b => b.innerText.toLowerCase());

              pubs.forEach(p => {
                const txt = p.innerText.toLowerCase();
                const links = [...p.querySelectorAll("a")].map(a => a.getAttribute("href") || "");
                let show = true;

                // 1. Year Filter
                if (y && !txt.includes(y)) show = false;

                // 2. Type Filter
                if (show && t) {
                  // Check if any link contains the category name 
                  // (matches /articles/, /conferences/, or /preprint/)
                  const hasFolder = links.some(l => l.toLowerCase().includes('/' + t.toLowerCase() + '/'));
                  
                  // Fallback: check the text content of the citation for specific conference names
                  const hasTextMatch = txt.includes('anidis') || txt.includes('wcee') || txt.includes('eurodyn');
                  
                  if (!hasFolder && !(t === 'conferences' && hasTextMatch)) {
                    show = false;
                  }
                }

                // 3. Tag Filter
                if (show && activeTags.length) {
                  const tagsTxt = [...p.querySelectorAll("a[href*='/tag/']")].map(x => x.innerText.toLowerCase());
                  if (!activeTags.some(tag => tagsTxt.includes(tag))) show = false;
                }

                p.style.display = show ? "" : "none";
              });
            };

            // Initialize listeners
            document.getElementById("yearFilter").onchange = applyFilters;
            document.getElementById("typeFilter").onchange = applyFilters;

          }, 800); 
        });
        </script>

        <style>
        .tagbtn { margin: 4px; padding: 6px 10px; border-radius: 20px; border: 1px solid #bbb; background: white; cursor: pointer; }
        .tagbtn.active { background: #333; color: white; }
        </style>

  - block: collection
    content:
      title: ""
      filters:
        folders:
          - publication
#          - publication/articles
#          - publication/conferences
#          - publication/preprint
        # Remove include_subfolders if listing explicitly, 
        # but keeping it doesn't hurt.
        include_subfolders: true
    design:
      view: citation
      sort_by: date
      sort_ascending: false
---