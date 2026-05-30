---
# Documentation: https://docs.hugoblox.com/managing-content/

title: "Ph Flag"
summary: ""
authors: []
tags: []
categories: []
date: 2025-06-09T16:44:11+08:00
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

1. Hi! In this video, I'll show you how to create the Philippine flag using this wiki page as a guide in free and open-source software Inkscape. Let's get started.

---

2. Grab the rectangle tool and create a rectangle. (Switch to wiki).

---

3. Let's see the wiki page for the dimensions. So it is 180 x 90.

---

4. Next, let's create this path (STW). It has a length of 90 and is rotated 60 degrees from the edge.

---

5. So let's grab the pen tool and create the path, but let's enable snapping first. Go to advanced mode, then disable bounding boxes, path, and alignment. And then let's enable...

---

6. We can now create the path. Make sure to snap it on the nodes. Let's give it a red stroke and change its width to 1.5 px.

---

7. Next, grab the selector tool and while the object is selected, click it again to toggle the rotation handles, and move the rotation center here.

---

8. Next, open the transform dialog. Go to rotate tab, change the angle to 60. Let's see if it's really 60 (STW). Okay, it really is (STI). Change to rotate CCW and apply.

---

9. Duplicate the object and flip it vertically and move it here. Like so.

---

10. Next, select this object. Grab the pen tool and let's continue this path. Make sure it snaps to the nodes. If you can't snap here, make sure you enabled line midpoints.

---

11. Let's give it a solid fill (Copy color from wiki) (Paste it to Inkscape). Let's remove its stroke.

---

12. Next, let's select and continue the other path. Give it a fill and remove the stroke.

---

13. We can now delete this object.

---

14. Next, grab the pen tool and create this triangle. Let's give it a white fill.

---

15. Next, let's create the stars. So as we can see, these outer vertices are located along this circle that has a diameter of 10. And these inner vertices are located along this circle that has a diameter of 4. So let's zoom in a bit here. Grab the ellipse tool and create a circle. Let's give it a different fill and lets resize it to 10 px.

---

16. Next, grab the star tool and create a star. Let's snap it here and while pressing Control + Shift, let's drag up to create a star and snap it here.

---

17. To get these inner vertices along this circle that has a diameter of 4, we can easily achieve this by changing the star's spoke ratio to .4000. 

---

18. Let's measure it if it's correct. Okay, it's correct.

---

19. We can now delete the circle.

---

20. Next, let's duplicate the star and rotate it 90 degrees clockwise. Snap the center here and move it... (STW) 14 px to the left.

---

21. Next, let's center this star to the edge. Let's zoom out a bit and move it here.

---

22. Let's move this star down by 14 px. Click again to toggle the rotation handles and move the rotation center here. And rotate it... (STW) 30 degrees CCW.

---

23. While the object is selected, let's move its rotation center here. Duplicate it and flip it vertically to place the third star.

---

24. We can now create the sun, which seems complicated but actually very easy to make.

---

25. So grab the ellipse tool and create a circle and resize it to... (STW) 18 px.

---

26. Snap the center here and move it... (STW) 28 px to the right.

---

27. We can now create the rays.

---

28. Grab the pen tool and create a path like so. Make sure to press Control to constrain the angle. Let's give it a height of... (STW) 38/2 = 19 and move it here. 

---

29. Let's click it again and move the rotation center here.

---

30. Duplicate it and rotate it... (STW) 3.75 degrees on both directions. This will serve as the bigger part of the ray.

---

31. Grab the pen tool again and create a path. Let's give it a different stroke color. Let's give it a height of... (STW) 34/2 and move it here. 

---

32. Move the rotation center here and rotate it 3.75 in CW direction twice. Duplicate it again and rotate it thrice.

---

33. Duplicate it again but this time rotate it CCW twice and thrice.

---

34. Press Escape to unselect object.

---

35. Select this path and this path. (Make sure to hold Shift when adding objects to selection). Grab the Node Tool, select these nodes and join them with a new segment by clicking this icon. Then select these nodes and join them by clicking this icon.

---

36. Let's repeat the process for the other small ray. So select both of them, grab the Node Tool, join them with a new segment, and join these nodes.

---

37. Select this object. Grab the Node Tool, select these nodes and join them with a new segment. 

---

38. And while these nodes are selected, let's insert a new node between them. Select the newly added node and move it up by pressing the Up Arrow key. And let's not forget to join these nodes.

---

39. Now grab the pen tool and create a path like this. Make sure to snap it here and here.

---

40. Grab the Node Tool, select this node, and extend the path while pressing Ctrl + Alt to maintain the angle. This is very important to get the exact length of the rays.

---

41. Duplicate the path and snap it here. Select both of them, grab the Node Tool and join these nodes.

---

42. Select these nodes, press Shift + D to duplicate them, and move them up. Then join them with a new segment.

---

43. We can now delete this path.

---

44. Select these 4 objects and grab the Shape Builder tool. Just click to add shapes, so let's click this one, this one, and this one. Press Enter to commit the shape.

---

45. While they are still selected, let's unite them by going to Path > Union.

---

46. To create the 7 rays we'll do it manually. Hehe, just kidding. Actually, it's very easy to create with the use of the Rotate Copies LPE.

---

47. So let's select the object. Go to Path > Path Effects, then add Rotate Copies LPE.

---

48. Let's make the number of copies 1 for now.

---

49. Grab the Node Tool and move the origin of rotation to the center of the sun.

---

50. We can now increase the number of copies to 8: 1, 2, 3, 4, 5, 6, 7, 8.

---

51. Then let's convert the objects to path so that we have the actual paths for further path operations.

---

52. And while the rays are selected, let's add the sun to the selection and go to Path > Union.

---

53. So that's it. Happy Independence Day! Please like and subscribe. Thank you for watching. Bye!
