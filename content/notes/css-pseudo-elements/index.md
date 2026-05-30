---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "CSS Pseudo Elements"
subtitle: ""
summary: ""

categories:
  - 📝 Notes
tags: 
- css

date: 2024-01-31T08:43:13+08:00
lastmod: 2024-01-31T08:43:13+08:00

draft: false
external_link: 
---

{{< toc >}}

## ::before and ::after

```css
blackquote::before {
    content: "“";
    font-size: 2em;
    color: red;
}

blackquote::after {
    content: "”";
}
```

![before and after pseudo elements](before-and-after-psuedo-elements.png)

## ::first-letter

```css
.container::first-letter {
    color: red;
    font-size: 2.7em;
    float: left;
    line-height: .9em;
    padding-right: 3px;
}
```

![first-letter pseudo element](first-letter-psuedo-element.png)

## ::first-line

```css
.container::first-line {
    font-weight: 700;
}
```

![first-line pseudo class](first-line-psuedo-element.png)

### :first-of-type

{{% callout note %}}
And, in case you're wondering, if you want to target the first item of a series, let's say the first paragraph of an article, you can do so using the `pseudo selector, first of type`.
{{% /callout %}}

```css
p:first-of-type {
    font-family: Roboto;
}
```

![first-of-type pseudo class](first-of-type-psuedo-class.png)

## ::selection

```css
blackquote::selection{
    background-color: aqua;
    color: rebeccapurple;
}
```

![selection pseudo element](selection-psuedo-element.png)
