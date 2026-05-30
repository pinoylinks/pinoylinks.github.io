---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:
  - block: portfolio
    id: bookmarks
    content:
      title: 
      subtitle: 
      filters:
        folders:
          - bookmarks
          - zk
          - notes
          - notebooks
        tags: []
        exclude_tags:
          - section
          - chapter
        kinds:
          - page
          - section
      sort_by: 'Date'
      sort_ascending: false
      default_button_index: 0
      buttons:
        - name: All
          tag: '*'
        - name: "#tools"
          tag: tools
        - name: "#resources"
          tag: resources
        - name: "#courses"
          tag: courses
        - name: "#games"
          tag: games
        - name: "#comics"
          tag: comics
        - name: "#articles"
          tag: articles
        - name: "#blogs"
          tag: blogs
    design:
      columns: '1'
      view: masonry
      flip_alt_rows: false
      spacing: {padding: [20px, 0, 0, 0]}
---
