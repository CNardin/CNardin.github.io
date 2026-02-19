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
            <option value="article">Journal article</option>
            <option value="conference">Conference</option>
            <option value="thesis">Thesis</option>
            <option value="news">News</option>
          </select>

          <button onclick="resetFilters()" style="padding:10px 14px;border-radius:8px;border:1px solid #bbb;background:white;cursor:pointer">
            Reset filters
          </button>

        </div>

        <div id="tagButtons" style="margin-bottom:1rem"></div>

        <script>
        document.addEventListener("DOMContentLoaded", function(){

          const pubs = [...document.querySelectorAll(".pub-list-item")];

          // -------- YEAR DROPDOWN --------
          const years = [...new Set(
            pubs.map(p => (p.innerText.match(/\b20\d{2}\b/) || [])[0])
          )].filter(Boolean).sort().reverse();

          years.forEach(y => {
            let o = new Option(y, y);
            yearFilter.add(o);
          });

          // -------- TAG BUTTONS --------
          const tagSet = new Set();
          pubs.forEach(p => {
            p.querySelectorAll("a[href*='/tag/']").forEach(t => {
              tagSet.add(t.innerText.trim());
            });
          });

          tagSet.forEach(tag => {
            let b = document.createElement("button");
            b.innerText = tag;
            b.className = "tagbtn";
            b.onclick = () => { b.classList.toggle("active"); applyFilters(); };
            tagButtons.appendChild(b);
          });

          // -------- FILTER ENGINE --------
          window.applyFilters = function() {
            const y = yearFilter.value;
            const t = typeFilter.value;

            const activeTags = [...document.querySelectorAll(".tagbtn.active")]
              .map(b => b.innerText.toLowerCase());

            pubs.forEach(p => {
              let txt = p.innerText.toLowerCase();
              let show = true;

              // YEAR FILTER
              if (y && !txt.includes(y)) show = false;

              // TYPE FILTER (Based on folder structure)
              if (t) {
                const pubType = p.getAttribute('data-type'); // Get data-type attribute
                if (pubType !== t) show = false;
              }

              // TAG FILTER
              if (activeTags.length) {
                let tagsTxt = [...p.querySelectorAll("a[href*='/tag/']")]
                  .map(x => x.innerText.toLowerCase());
                if (!activeTags.some(tag => tagsTxt.includes(tag))) show = false;
              }

              p.style.display = show ? "" : "none";
            });
          }

          window.resetFilters = function() {
            yearFilter.value = "";
            typeFilter.value = "";
            document.querySelectorAll(".tagbtn").forEach(b => b.classList.remove("active"));
            applyFilters();
          }

          yearFilter.onchange = applyFilters;
          typeFilter.onchange = applyFilters;

        });
        </script>

        <style>
        .tagbtn {
          margin: 4px;
          padding: 6px 10px;
          border-radius: 20px;
          border: 1px solid #bbb;
          background: white;
          cursor: pointer;
        }
        .tagbtn.active {
          background: #333;
          color: white;
        }
        </style>

  - block: collection
    content:
      title: "All Publications"
      filters:
        folders:
          - articles
          - conferences
          - thesis
          - news
    design:
      view: citation
      sort_by: date
      sort_ascending: false
      columns: 1
---
