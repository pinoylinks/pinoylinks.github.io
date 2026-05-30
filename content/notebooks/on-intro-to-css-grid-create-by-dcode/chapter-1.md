---
title: Setup
linkTitle: Chapter 1
date: 2023-09-07T08:14:13+08:00
type: book
weight: 1
math: true
highlight: true
tags:
  - chapter
---

<!--more-->

## Steps

### 1. Add `div` with class of container

```html
<div class="container">
```

### 2. Remove the default margin of the `body`

```css
body {
  margin: 0;
}
```

### 3. Make the container take up the entire width and height of the page

```css
.container {
  width: 100vw;
  height: 100vh;
}
```

### 4. Add font styling

```css
.container {
  width: 100vw;
  height: 100vh;

  font-family: `Quicksand`, sans-serif;
  font-weight: bold;
  font-size: 20px;
}
```
