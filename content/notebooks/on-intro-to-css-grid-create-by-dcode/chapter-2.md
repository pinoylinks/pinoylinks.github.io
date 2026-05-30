---
title: The grid
linkTitle: Chapter 2
date: 2023-09-07T08:14:13+08:00
type: book
weight: 2
math: true
highlight: true
tags:
  - chapter
---

<!--more-->

### 1. Add `grid`

```css
.container {
  display: grid;
}
```

### 2. Add `grid-template-columns`

```css
.container {
  /* Shortcut */
  /* grid-template-columns: repeat(3, 1fr); */
  grid-template-columns: 1fr 1fr 1fr;
}
```

### 3. Add `grid-template-rows`

```css
.container {
  grid-template-rows: 50px 1fr 1fr 100px;
}
```

![The grid.](notebooks/on-intro-to-css-grid-create-by-dcode/the-grid.webp "The grid.")

{{% callout note %}}
The header and footer here have fixed heights of 50px and 100px respectively.
{{% /callout %}}

{{% callout note %}}
The other two are fractional and they can shrink if they need to when the browser resizes.
{{% /callout %}}
