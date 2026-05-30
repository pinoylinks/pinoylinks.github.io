---
title: The `grid-template` Shorthand Property
linkTitle: Chapter 8
date: 2023-09-07T08:14:13+08:00
type: book
weight: 8
math: true
highlight: true
tags:
  - chapter
---

<!--more-->

## Separate

```css
.container {
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 50px 1fr 1fr 100px;
}
```

## Shorthand

```css
.container {
  grid-template: 50px 1fr 1fr 100px / 1fr 1fr 1fr;
}
