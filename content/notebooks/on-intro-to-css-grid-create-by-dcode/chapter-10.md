---
title: Final Code
linkTitle: Chapter 10
date: 2023-09-07T08:14:13+08:00
type: book
weight: 10
math: true
highlight: true
tags:
  - chapter
---

<!--more-->

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    body {
      margin: 0;
    }

    .container {
      width: 100vw;
      height: 100vh;

      font-family: Quicksand, sans-serif;
      font-weight: bold;
      font-size: 20px;

      display: grid;

      grid-template-columns: 1fr 1fr 1fr;
      grid-template-rows: 50px 1fr 1fr 100px;

      gap: 10px;

      padding: 10px;
      box-sizing: border-box;
    }

    .container div {
      padding: 10px;
      border: 1px solid black
    }

    .header {
      grid-column-start: 1;
      grid-column-end: 4;
    }

    .content-large {
      grid-column-start: 1;
      grid-column-end: span 2;
      grid-row-start: 2;
      grid-row-end: span 2;
    }

    .footer {
      grid-column: 1 / span 3;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="header">Header</div>
    <div class="content-large">Content #1</div>
    <div class="content-small">Content #2</div>
    <div class="content-small">Content #3</div>
    <div class="footer">Footer</div>
  </div>
</body>
</html>
```
