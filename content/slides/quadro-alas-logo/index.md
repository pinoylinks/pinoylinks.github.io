---
# Documentation: https://docs.hugoblox.com/managing-content/

title: "Quadro Alas Logo"
summary: ""
authors: []
tags: []
categories: []
date: 2025-07-09T23:36:09+08:00
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
    transition: fade  # none/fade/slide/convex/concave/zoom
    transitionSpeed: default  # default/fast/slow
    background_transition: slide  # none/fade/slide/convex/concave/zoom
    touch: true
    loop: false
    menu_enabled: true
---

Hi, in this video, I'll show you how I created this logo. This logo is for Johnriel Casimero, AKA Quadro Alas, a famous boxer here in the Philippines right now.

---

The main concept is very simple: Quadro Alas is 4 Aces. So a Q + 4 As = .The concept also resembles the old xmen logo which is great since he is often called Beast. I further discussed it on my blog; you can check it out if you are interested.

---

So let's get started.

1. Let's first import the refined sketch. Then we'll lock it so that it won't move.

---

2. Next, let's grab the circle tool and create an object. Make sure to hold Control to lock the proportion. Then let's resize it to 1000 px.

---

3. Next, let's give it a black stroke, remove its fill, change its opacity to 75%, and change its width to... let's go to the Fill and Stroke dialog and change its width to 150 px. 

---

4. Next, let's convert it to path so that we can manipulate its nodes further by going to Path > Object to Path.

---

5. Next, let's grab the pen tool and create a path... but let's enable snapping first, go to Advanced mode and disable... then enable...

---

6. We can now create the path. Make sure to snap on midpoint, then press and hold Control and lock it on 45 degrees, click again here to create another node, and then right-click to finish the path.

---

7. Next, let's move this node here. So let's grab the node tool, select this node, and while pressing CTRL + ALT to lock the angle, let's move this node until it reaches here.

---

8. Next, let's duplicate the path, then flip it horizontally, and snap its midpoint to the center of the circle.

---

9. Next, let's select them all and convert them to actual paths by going to Path > Stroke to Path.

---

10. Next, let's trim these unnecessary parts here. So let's grab the pen tool and create a path. Make sure to snap on this node and make sure to hold Control to lock the angle. Right-click to finish the path.

---

11. Next, let's grab the node tool and let's move this node here. Make sure to hold Control.

---

12. Next, let's move this path down to about 20 px to create an overshoot. So let's go to Object and open the Transform dialog, and move it down by 20 px. Let's go to Outline mode so that we can see if it's enough. So I think it's enough.

---

13. While the path is selected, let's grab the pen tool and let's continue it to create a shape like this. Make sure to snap on the nodes. So this shape will serve like a cookie cutter to remove these excess parts.

---

14. So let's duplicate this object. Then Shift-select this object to add it to the selection, then go to Path > Difference.

---

15. Select this object and this object, then go to Path > Difference.

---

16. Let's repeat the process in this part. So grab the pen tool, create a path, let's move this node here, continue it to create a closed shape, move it up to create an overshoot.

---

BTW, overshoot is the slight extension of curved or pointed shapes to counter the optical illusion where they appear smaller than flat shapes at the same height.

We can now go to normal view. 

---

17.Next, let's create the negative space here to emphasize the letter Q. We can achieve this with the Offset Path effect. So let's duplicate this object, then let's create a throwaway shape like this. Select both of them, then go to Path > Intersection.

---

18. We can now offset this object. So let's open the Path Effects dialog, then add Offset. Let's give it 150/2 since the original stroke we used is 150, then let's convert it to path. Add this object to selection, then go to Path > Difference.

---

19. Finally, let's select all objects and let's unite them by going to Path > Union.

---

20. That's it thank you for watching.
