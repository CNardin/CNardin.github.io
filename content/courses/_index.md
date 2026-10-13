---
# NON PUBBLICATO e NON DA TRADURRE: contenuto demo del tema Hugo Blox.
# Escluso da build, liste, sitemap e ricerca (build.render/list: never).
build:
  render: never
  list: never
  publishResources: false
title: Courses
summary: My courses
type: landing

cascade:
  - build:
      render: never
      list: never
      publishResources: false
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
      columns: 1
---
