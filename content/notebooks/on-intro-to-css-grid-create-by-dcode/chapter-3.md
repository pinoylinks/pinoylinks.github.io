---
title: Add Gaps and Borders
linkTitle: Chapter 3
date: 2023-09-07T08:14:13+08:00
type: book
weight: 3
math: true
highlight: true
tags:
  - chapter
---

<!--more-->

## Specify gap between each of the areas

```css
.container {
  gap: 10px;
}
```

![Add gaps.](notebooks/on-intro-to-css-grid-create-by-dcode/add-gaps.webp "Add gaps.")

{{% callout warning %}}
This excludes the edges of the container.
{{% /callout %}}

Fix:

1. Add `padding` same as the `gap` size (10px).
2. Add `box-sizing: border-box` to contain the padding as being part of the total width of the container.

```css
.container {
  padding: 10px;
  box-sizing: border-box;
}
```

![Add gaps around border.](notebooks/on-intro-to-css-grid-create-by-dcode/add-gaps-around-border.webp "Add gaps around border.")

## Add borders

Create another declaration.

```css
.container div {
  padding: 10px;
  border: 1px solid black
}
```
