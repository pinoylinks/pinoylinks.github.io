---
title: The grid-row
linkTitle: Chapter 5
date: 2023-09-07T08:14:13+08:00
type: book
weight: 5
math: true
highlight: true
tags:
  - chapter
---

<!--more-->

## Create the contents

### Add HTML element

```html
<div class="content-large">Content #1</div>
<div class="content-large">Content #2</div>
```

![Medium contents.](notebooks/on-intro-to-css-grid-create-by-dcode/medium-contents.webp "Medium contents.")

### Span the row

Initially, this will flow to the second row and again it will take up a single column and a single row.

To make them span to multiple rows, use the `grid-row-start` and `grid-row-end` properties.

{{% callout note %}}
The values are the grid line numbers.

4 rows = 5 grid lines
{{% /callout %}}

Target the `content-large` class.

```css
.content-large {
  grid-row-start: 2;
  grid-row-end: 4;
}
```

![Grid row.](notebooks/on-intro-to-css-grid-create-by-dcode/grid-row.webp "Grid row.")

### Alternative end value

We can also use the value `span 2`.

`span 2` means `grid-row-start` + 2 = 4.

So `grid-row-end: span 2;` is the same as `grid-row-end: 4;`.

```css
.content-large {
  grid-row-start: 2;
  grid-row-end: span 2;
}
