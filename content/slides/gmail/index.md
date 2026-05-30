---
# Documentation: https://docs.hugoblox.com/managing-content/

title: "Gmail"
summary: ""
authors: []
tags: []
categories: []
date: 2025-01-21T12:13:45+08:00
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

1. First let's create a new scene, make it 60 frames long and change its background to white.  

---

2. Next let's Grab the Rectangle Tool and create an object.  

---

3. Change its stroke size to **155 px** and adjust its dimensions to **530x360**.  

---

4. Let’s center the object on the scene.  

---

5. Convert it to a path, then delete the old shape.  

---

6. Select the object and grab the Node Tool. Let’s disconnect these nodes.  

---

7. Duplicate the object and give it a different color. Let’s delete these end nodes, then add a new node between the remaining nodes.  

---

8. Select the midpoint node and move it down by pressing **G** (for Grab), then **Y** to lock it on the Y axis, and enter **200**. Update its stroke join to **Miter**.  

---

9. Select the other object and move it to the top for better visibility. Delete this segment, then go to **Path > Break Apart** to separate them.  

---

10. Let’s change their colors: **#4285F4** (blue), **#34A853** (green), and **#EA4335** (red). Rename them accordingly.  

---

11. Next, let’s create the background, which will also serve as a clipping mask for the three objects later.  

---

12. Duplicate the objects, convert their strokes to paths (delete the old objects). Let's hide the colors for now.  

---

13. Select these new objects, set their stroke size to **30**, then unite them via **Path > Union** (delete the old objects).  

---

14. Select the united object with the Node Tool, delete these segments, and connect these end nodes with a new segment.  

---

15. Grab these end nodes and move them downward (lock to the Y axis). Go to **Path > Union** again (delete the old objects).  

---

16. Delete these nodes, merge these broken nodes to close the shape, remove the stroke, fill it with **#E6E6E6**, and rename it **Container**.  

---

17. Reveal the hidden objects, change their stroke cap to **Square**, to clip them to the container, we need to group them all, and promote the group to a layer.  

---

18. Then set the Container’s blending mode to **DstATop**. For the darker red, set the blue object’s blending to **ColorBurn**. For the yellow effect, set the green object’s blending to **ColorDodge**.  

---

19. We can now animate. Go to frame **20** and add keyframes.  

---

20. Record the **X translation** for the blue and green objects, and the **Y translation** for the red object.  

---

21. At frame **0**, move the blue object **155px left**, the green object **155px right**, and the red object **194.19px up**.  

---

22. Play the animation. To smooth the movement, open the Graph Editor and adjust the animation curves. To show the animation curves lets enable them here.

---

23. Convert keyframe nodes to smooth nodes, then drag their left handles until it reaches **0** (press **X** to lock the X axis).

---

24. Play the final animation. That’s it! Thank you for watching.  

---

25. Please like, share, and subscribe.  

---

26. See you next time. Bye!
