---
title: X Background
linkTitle: Chapter 9
date: 2023-09-07T08:14:13+08:00
type: book
weight: 9
math: true
highlight: true
tags:
  - chapter
---

<!--more-->

![X background.](notebooks/on-intro-to-css-grid-create-by-dcode/x-bg.webp "X background.")

## Linear Gradient

```css
.crossed {
  background: 
    linear-gradient(to top left,
      rgba(0,0,0,0) 0%,
      rgba(0,0,0,0) calc(50% - 0.8px),
      rgba(0,0,0,1) 50%,
      rgba(0,0,0,0) calc(50% + 0.8px),
      rgba(0,0,0,0) 100%),
    linear-gradient(to top right,
      rgba(0,0,0,0) 0%,
      rgba(0,0,0,0) calc(50% - 0.8px),
      rgba(0,0,0,1) 50%,
      rgba(0,0,0,0) calc(50% + 0.8px),
      rgba(0,0,0,0) 100%);
}
```

```html
<textarea class="crossed"></textarea>
```

## SVG

```css
.crossed {
  background: url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' version='1.1' preserveAspectRatio='none' viewBox='0 0 100 100'><line x1='0' y1='0' x2='100' y2='100' stroke='black' vector-effect='non-scaling-stroke'/><line x1='0' y1='100' x2='100' y2='0' stroke='black' vector-effect='non-scaling-stroke'/></svg>");
  background-repeat: no-repeat;
  background-position: center center;
  background-size: 100% 100%, auto;
}
```

```html
<textarea class="crossed"></textarea>
```
