---
title: Span Columns + Rows
linkTitle: Chapter 6
date: 2023-09-07T08:14:13+08:00
type: book
weight: 6
math: true
highlight: true
tags:
  - chapter
---

<!--more-->

## Update the contents

### Update HTML element

```html
<div class="content-large">Content #1</div>
```

![Large content.](notebooks/on-intro-to-css-grid-create-by-dcode/large-content.webp "Large content.")

### Span the columns + rows

```css
.content-large {
  grid-column-start: 1;
  grid-column-end: span 2;
  grid-row-start: 2;
  grid-row-end: span 2;
}
```

![Grid column + grid row.](notebooks/on-intro-to-css-grid-create-by-dcode/grid-column-plus-grid-row.webp "Grid column + grid row.")
