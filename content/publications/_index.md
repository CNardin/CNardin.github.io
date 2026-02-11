---
title: Publications
cms_exclude: true

blocks:
  - block: resume-awards
    # View.
    #   1 = List
    #   2 = Compact
    #   3 = Card
    #   4 = Citation
    view: compact
    content:
      title: Publications
      page_type: publication
      sort_by: date
      sort_ascending: false
    design:
      filters:
        enable: true
        tags: true
        publication_type: true
        year: true
      sort: true

# Optional header image (relative to `static/media/` folder).
banner:
  caption: ''
  image: ''
---