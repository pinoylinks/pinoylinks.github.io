---
# Documentation: https://docs.hugoblox.com/managing-content/

title: "Egg Logo"
summary: ""
authors: []
tags: []
categories: []
date: 2025-01-10T10:16:47+08:00
_build:
  render: always
  list: never
slides:
  # Choose a theme from https://github.com/hakimel/reveal.js#theming
  theme: black
  # Choose a code highlighting style (if highlighting enabled in `params.toml`)
  #   Light style: github. Dark style: dracula (default).
  #   Available highlight themes listed in: https://highlightjs.org/static/demo/
  #   Use lower case names and replace space with hyphen '-'
  highlight_style: dracula

  diagram: true
  diagram_options:
    # Mermaid diagram themes include: default,base,dark,neutral,forest
    theme: base

  # RevealJS slide options.
  # Options are named using the snake case equivalent of those in the RevealJS docs.
  reveal_options:
    controls: true
    progress: true
    slide_number: c/t  # true | false | h.v | h/v | c | c/t
    center: true
    rtl: false
    mouse_wheel: true
    transition: slide  # none/fade/slide/convex/concave/zoom
    transitionSpeed: default  # default/fast/slow
    background_transition: slide  # none/fade/slide/convex/concave/zoom
    touch: true
    loop: false
    menu_enabled: true
---

Hi. In this video, we will be creating this logo using Inkscape. Let's get started.

---

Grab the **Rectangle Tool** and create an object.

---

Change the height to 65 pixels and the width to 72 pixels.

---

Remove the fill and give it a stroke of 4 pixels. Let's zoom to selection by hitting 3.

---

Convert it to a path so that we can manipulate its nodes.

---

Now grab the **Node Tool**, select these nodes, make sure to hold shift when adding nodes or objects to the selection, then click this icon.

---

While the nodes are selected, we're going to join them with a line segment by clicking this icon.

---

What we have now is a right triangle. This will serve as our guide to find the common curve to 2 circles. You will see what I mean in a moment.

---

Now grab the **Ellipse Tool** and create a circle. Make sure to hold control, lock the proportion, then resize it to 40 + 4, since it has a 4-pixel stroke.

---

Ahhh wait, let me undo for a second. We need to disable this scaling option so that the stroke size will remain when scaling.

---

And while we're at it, let's enable snapping. Go to advanced mode, then disable bounding box, paths, and alignment, then enable object midpoints. Hit escape to close.

---

So resize it to 40 + 4 pixels, then snap its midpoint here. Like that. Let's zoom out a bit.

---

Duplicate the circle and resize it to 90 + 4 pixels, then snap its midpoint here. Like that. Let's zoom out 2 times (scroll down to adjust objects).

---

Let's duplicate this circle and resize it to 234 + 4 pixels, then snap its midpoint here. Like that.

---

We can now delete the right triangle. Let's go to outline mode to see if the curves are perfectly placed.

---

So as we can see, they perfectly placed. Okay. Let's go back to normal mode.

---

Let's duplicate this circle, then snap its quadrant point here. Like that. Let's zoom to all objects by hitting 4.

---

Then let's duplicate any circle and give it a size of 378 + 4 pixels, then put it here. Like that.

---

Now, select all objects and grab the **Shape Builder Tool**. Just drag across objects that you want to unite. Hit enter to commit the shape or just click this icon.

---

To get the negative shape, select all objects, change their stroke width to 16 pixels, then convert strokes to paths.

---

Unite them all, then break apart, then delete this object.

---

Finally, let's unite them, change the color, and rotate it 240 degrees to the right.

---

That's it. Thank you for watching. Don't forget to like, share, and subscribe. See you next time. Bye.
