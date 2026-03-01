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
          // Give Hugo a tiny moment to render the collection
          setTimeout(() => {
            const pubs = [...document.querySelectorAll(".pub-list-item")];
            
            // -------- YEAR DROPDOWN --------
            const yearSelect = document.getElementById("yearFilter");
            const years = [...new Set(
              pubs.map(p => (p.innerText.match(/\b20\d{2}\b/) || [])[0])
            )].filter(Boolean).sort().reverse();

            years.forEach(y => {
              yearSelect.add(new Option(y, y));
            });

            // -------- TAG BUTTONS --------
            const tagContainer = document.getElementById("tagButtons");
            const tagSet = new Set();
            pubs.forEach(p => {
              p.querySelectorAll("a[href*='/tag/']").forEach(t => tagSet.add(t.innerText.trim()));
            });

            tagSet.forEach(tag => {
              let b = document.createElement("button");
              b.innerText = tag;
              b.className = "tagbtn";
              b.onclick = () => { b.classList.toggle("active"); applyFilters(); };
              tagContainer.appendChild(b);
            });

            // -------- FILTER ENGINE --------
            window.applyFilters = function() {
              const y = document.getElementById("yearFilter").value;
              const t = document.getElementById("typeFilter").value;
              const activeTags = [...document.querySelectorAll(".tagbtn.active")].map(b => b.innerText.toLowerCase());

              pubs.forEach(p => {
                let txt = p.innerText.toLowerCase();
                let links = [...p.querySelectorAll("a")].map(a => a.getAttribute("href") || "");
                let show = true;

                // 1. Year Filter
                if (y && !txt.includes(y)) show = false;

                // 2. Type Filter (Checking URLs for folder names)
                if (show && t) {
                  // We check if any link contains the folder name (e.g., /articles/ or /conferences/)
                  // This also covers your custom folder "2025-anidis-maers" if it's inside /conferences/
                  const folderPattern = "/" + t + "/";
                  const hasFolder = links.some(l => l.includes(folderPattern) || l.includes("2025-anidis-maers"));
                  if (!hasFolder) show = false;
                }

                // 3. Tag Filter
                if (show && activeTags.length) {
                  let tagsTxt = [...p.querySelectorAll("a[href*='/tag/']")].map(x => x.innerText.toLowerCase());
                  if (!activeTags.some(tag => tagsTxt.includes(tag))) show = false;
                }

                p.style.display = show ? "" : "none";
              });
            };

            window.resetFilters = function() {
              document.getElementById("yearFilter").value = "";
              document.getElementById("typeFilter").value = "";
              document.querySelectorAll(".tagbtn").forEach(b => b.classList.remove("active"));
              applyFilters();
            };

            document.getElementById("yearFilter").onchange = applyFilters;
            document.getElementById("typeFilter").onchange = applyFilters;
          }, 500); 
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
        include_subfolders: true
    design:
      view: citation
      sort_by: date
      sort_ascending: false
---