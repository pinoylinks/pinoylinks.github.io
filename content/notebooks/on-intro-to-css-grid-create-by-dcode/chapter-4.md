---
title: The grid-column
linkTitle: Chapter 4
date: 2023-09-07T08:14:13+08:00
type: book
weight: 4
math: true
highlight: true
tags:
  - chapter
---

<!--more-->

## Create the header

### Add HTML element

```html
<div class="header">Header</div>
```

![Head.](notebooks/on-intro-to-css-grid-create-by-dcode/head.webp "Head.")

### Span the column

Initially it will take up a single column and a single row.

To make the header span to the remaining columns (2 and 3), use the `grid-column-start` and `grid-column-end` properties.

{{% callout note %}}
The values are the grid line numbers.

3 columns = 4 grid lines
{{% /callout %}}

```css
.header {
  grid-column-start: 1;
  grid-column-end: 4;
}
```

![Grid Column.](notebooks/on-intro-to-css-grid-create-by-dcode/grid-column.webp "Grid Column.")
