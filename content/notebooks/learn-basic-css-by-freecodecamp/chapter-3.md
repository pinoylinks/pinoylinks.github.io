---
title: CSS
linkTitle: Chapter 3
date: 2023-09-20T22:38:32+08:00
type: book
weight: 3
math: true
highlight: true
tags:
  - chapter
---

<!--more-->
1. Add `div>main>h1+p+section>h2`. The contents of `h1`, `p`, and `h2` elements are `CAMPER CAFE`, `Est. 2020`, and `Coffee` respectively.
2. Center `h1`, `h2`, and `p` elements.
3. Inside the opening `div` tag, add the `class` attribute with a value of `menu`.
4. Use the `.menu` selector to give your element a `width` of `80%` and `background-color` of `burlywood`.
5. Center the `.menu` horizontally with `margin-left` and `margin-right` set to `auto`.
6. Add `background-image` to the `body` with this image: `url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg)`.
7. Add an `article` element under the `Coffee` heading.
8. Nest two `p` elements inside your `article` element. The contents are `French Vanilla` and `3.00` respectively.

```html
<article>
  <p>French Vanilla</p>
  <p>3.00</p>
</article>
```

9.  Inside these two `p` elements, add the `class` attribute with the values of `flavor` and `price` respectively.
10. Align `.flavor` left and `.price` right.
11. To get them on the same line, you need to apply some styling to the `p` elements so they behave more like _inline_ elements. To do that, start by adding a `class` attribute with the value `item` to the first `article` element under the `Coffee` heading.
12. Using `.item p { }`, add a `display` property with value `inline-block` so the `p` elements behave more like inline elements.
13. That's closer, but the price didn't stay over on the right. This is because `inline-block` elements only take up the width of their content. To spread them out, add a `width` property to the `flavor` and `price` class selectors that have a value of `75%` and `25%` respectively.
14. That worked, but there is still a little space on the right of the price. Use the back space key on your keyboard to move the `p` element with the class `price` next to the `p` element with the class `flavor` so that they are on the same line in the editor. Make sure there is no space between them.

```html
<article class="item">
  <p class="flavor">French Vanilla</p><p class="price">3.00</p>
</article>
```

15. Using the `article` code block just above, complete the `Coffee` menu with the coffee/price pair below.

| Coffee            | Price |
|-------------------|-------|
| Caramel Macchiato | 3.75  |
| Pumpkin Spice     | 3.50  |
| Hazelnut          | 4.00  |
| Mocha             | 4.50  |

16. Create another section for desserts (`.dessert`).

| Desserts      | Price |
|---------------|-------|
| Donut         | 1.50  |
| Cherry Pie    | 2.75  |
| Cheesecake    | 3.00  |
| Cinnamon Roll | 2.50  |

17.  Add `.dessert` to css

```css
.flavor, .dessert {
  text-align: left;
  width: 75%;
}
```

18. Give the `menu` class a `padding` of `20px`.
19. Add a `max-width` property to the `menu` class with a value of `500px` to prevent it from growing too wide.
20. Change all the text in your `body`, by adding a `font-family` property with the value `sans-serif`. This is a fairly common font that is very readable.
21. Style both the `h1` and the `h2` elements so that only these elements' text use `Impact` font.
22. Add the fallback font `serif` after the `Impact` font.
23. Make the `Est. 2020` text italicized by creating an `established` class selector and giving it the `font-style` property with the value `italic`.
24. Add two new type selectors (`h1` and `h2`). Use the `font-size` property for both, but use the value `40px` for the `h1` and `30px` for the `h2`.
25. Add a `footer` element below the `main` element, where you can add some additional information.
26. Inside the `footer`, add a `p` element. Then, nest an anchor (`a`) element in the `p` that links to `https://www.freecodecamp.org` and has the text `Visit our website`.
27. Add a second `p` element below the one with the link and give it the text `123 Free Code Camp Drive`.
28. Add an `hr` element between the `p` element with the class `established` and the first `section` element. Note that `hr` elements are self closing.
29. Change the height of the `hr` element to be `3px`.
30. Change the background color of the `hr` element to `brown` so it matches the color of the coffee beans.
31. Make all the edges of the `hr` element the same color as the background of it using the `border-color` property.
32. Change the `height` property of the `hr` to be `2px`, so the total height of it becomes `4px`. The default value of a property named `border-width` is `1px` for all edges of `hr` elements.
33. Go ahead and add another `hr` element between the `main` element and the `footer` element.
34. To create a little more room around the menu, add `20px` of space on the inside of the `body` element by using the `padding` property.
35. Target all the `p` elements nested in elements with the `class` named `item` and set their top and bottom margin to be `5px`.
36. Using the same style selector in the previous step, make the font size of the items and prices larger by using a value of `18px`.
37. Now add the `bottom-line` class to the second `hr` element, then add some more space by creating a class named `bottom-line` using `25px` for the `margin-top` property.
38. Moving down to the `footer` element, make all the text have a value of `14px` for the font size.
39. Make the `footer` links the same color regardless if a link has been visited, use a type selector for the anchor element (`a`) and use the value `black` for the `color` property.
40. Change the color of the footer `Visit our website` link to be `black` when a user has visited the link.
41. Change the color of the footer `Visit our website` link to be `brown` when a user hovers over it.
42. Change the color of the footer `Visit our website` link to be `brown` when clicked on.
43. Change the top margin of the `h1` element to `0` to remove all the top margin.
44. To remove some of the vertical space between the `h1` element and the text `Est. 2020`, change the bottom margin of the `h1` to `15px`.
45. To decrease the default margin space below the address `p` element, create a class selector named `address` and use the value `5px` for the `margin-bottom` property. Don't forget to apply the `address` class to the `p` element containing the street address `123 Free Code Camp Drive`.
46. Under the `Coffee` heading, add an image using the url `https://cdn.freecodecamp.org/curriculum/css-cafe/coffee.jpg`. Give the image an `alt` value of `coffee icon`.
47. To make the image behave like heading elements (which are block-level), create an `img` type selector and use the value `block` for the `display` property and use the applicable `margin-left` and `margin-right` values to center it horizontally.
48. Add one last image under the `Desserts` heading using the url `https://cdn.freecodecamp.org/curriculum/css-cafe/pie.jpg`. Give the image an `alt` value of `pie icon`.
49. Add a negative top margin to the `img` elements to pull them up from their current positions. Negative values are created using a `-` in front of the value. To complete this project, go ahead and use a negative top margin of `25px` in the `img` type selector.