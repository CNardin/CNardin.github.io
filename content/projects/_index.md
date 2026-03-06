---
title: 'Projects'
date: 2024-05-19
type: landing


cascade:
  - target:
      path: '{/projects/*/**}'
    type: docs
    params:
      show_breadcrumb: true

# design:
#   # Section spacing
#   spacing: '5rem'

# Page sections
sections:
  - block: collection
    id: projects
    content:
      title: Selected Projects
      text:  Here are a selection of projects that I have worked on over the years or I am currently working on.
      filters:
        folders:
          - projects  # This forces it to look ONLY inside the projects folder
        exclude_featured: false
        kinds:
          - page      # This tells Hugo to look for individual project pages, not whole sections
    design:
      view: article-grid
      fill_image: false
      columns: 3
      show_date: false
      show_read_time: false
      show_read_more: false
---

<!-- 
title: Courses
summary: My courses
type: landing

cascade:
  - target:
      path: '{/courses/*/**}'
    type: docs
    params:
      show_breadcrumb: true

sections:
  - block: collection
    id: courses
    content:
      title: Courses
      filters:
        tag: Course
        kinds:
          - section
    design:
      view: article-grid
      show_read_time: false
      show_date: false
      show_read_more: false
      columns: 1 -->