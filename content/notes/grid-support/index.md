---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Grid Support"
subtitle: ""
summary: ""

categories:
  - 📝 Notes
tags: 
- css

date: 2024-01-31T15:46:36+08:00
lastmod: 2024-01-31T15:46:36+08:00

draft: false

# links:
#   - name: 
#     url: 
#     icon_pack: fas
#     icon: link
---

The best way to test the browser if it supports the CSS Grid is if it supports grid area.

```css
@supports (grid-area: auto) {
  .site {
    display: grid;
  }
}
```

Grid area is from the new current spec.

Some older browser have legacy support for an older spec of the CSS Grid.

Which means if you test it with the display grid, the browser will still say yes while using the old spec.

If the browser doesn't support the new current spec, it's better if it ignores the CSS Grid throughout and use the fallback layout (mobile) instead.
