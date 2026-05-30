---
title: Add Small Contents and Footer
linkTitle: Chapter 7
date: 2023-09-07T08:14:13+08:00
type: book
weight: 7
math: true
highlight: true
tags:
  - chapter
---

<!--more-->

## Create the contents

### Add small contents element

```html
<div class="content-small">Content #2</div>
<div class="content-small">Content #3</div>
```

![Small contents.](notebooks/on-intro-to-css-grid-create-by-dcode/small-contents.webp "Small contents.")

These will flow naturally so they are in the correct spot.

### Add footer element

```html
<div class="footer">Footer</div>
```

![Footer.](notebooks/on-intro-to-css-grid-create-by-dcode/footer.webp "Footer.")

### Span the column

It is the same as the header but we'll use the shorthand.

```css
.footer {
  grid-column: 1 / span 3;
}
```

![Span footer.](notebooks/on-intro-to-css-grid-create-by-dcode/span-footer.webp "Span footer.")
