---
title: Publications
type: landing

sections:

  - block: markdown
    content:
      text: |
        <input id="pub-filter" type="text" placeholder="🔎 Filter publications (title, author, tag…)" style="width:100%;padding:12px;font-size:1rem;border:1px solid #ccc;border-radius:8px;">
        
        <script>
        document.addEventListener("DOMContentLoaded", function() {
          const input = document.getElementById("pub-filter");
          input.addEventListener("keyup", function() {
            const q = input.value.toLowerCase();
            document.querySelectorAll(".pub-list-item").forEach(el => {
              el.style.display = el.innerText.toLowerCase().includes(q) ? "" : "none";
            });
          });
        });
        </script>

  - block: collection
    content:
      title: Publications
      text: ""
      count: 0   # 0 = all
      filters:
        folders:
          - publication
#    design:
#      view: citation
#      sort_by: date
#      sort_ascending: false
#      columns: 1

---
