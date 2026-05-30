---
title: Flux
summary: Tips, tricks and all things Flux ai.
subtitle: Tips, tricks and all things Flux ai.
date: 2025-07-25T22:16:19+08:00
lastmod: 2025-07-25T22:16:19+08:00
_build:
  list: always
draft: true
categories:
  - 📝 Notes
tags:
  - ai
  - flux
---

## Prompt

Feed in chatgpt or deepseek

```
You are a creative prompt engineer.

Your mission is to analyze the provided image and generate a distinct image tranformation instruction.

Turn this image into the style of a professional product photo. Describe a scene that could show a different aspect of the item in highly professional catalog, including possible light settings, camera angles, zoom levels, or a scenario where the item is being used.

Output only the transformation instruction, without explanation, numbering, or extra text.

Image description: 

A pair of mustard-colored corduroy shorts with an elastic waistband and drawstring sits on a bed of small stones.
The composition of the image is a close-up of the shorts, with the focus solely on the garment. The shorts are positioned in the center of the image, filling most of the frame. The stones act as a background, providing a neutral backdrop and depth to the image. The lighting is natural, casting no significant shadows.
The key subject is a pair of mustard-colored corduroy shorts. They have a ribbed texture and an elastic waistband. The drawstring is a contrasting white color, which stands out against the mustard color. The shorts are simple in design, with basic features.
The artistic medium appears to be a photograph, taken in natural light with a simple setup, with no visible post-processing or editing. The image is clear and sharply focused on the shorts, highlighting the texture and color.
The setting is outdoors and the background is a variety of small stones. The image captures the characteristics of the garment, without any extra environment or context. The lighting is natural and bright, casting no notable shadows or highlights, resulting in a neutral and straightforward presentation of the shorts. The overall atmosphere is neutral.

Edit instruction:

wear it on a model captured using iphone

```

## Output sample

feed in flux

### chatgpt

```
Transform the image into a high-end fashion catalog shot: place the mustard-colored corduroy shorts on a tall supermodel with a minimalistic white silk blouse tucked in, standing in a bright studio with a seamless white backdrop. Use soft diffused lighting from a large octagonal softbox to eliminate harsh shadows, creating a clean and polished look. Capture the model in a three-quarter pose at eye level with a 50mm lens for natural proportions, slightly zoomed out to show the full outfit while keeping the shorts as the focal point. Add subtle styling details like a thin leather belt and minimalist sandals to emphasize versatility.

be mindful of the aspect ration preferably portrait 1080 x 1920 px.

```

### deepseek

```
A supermodel wearing the mustard-colored corduroy shorts with an elastic waistband and drawstring, posing confidently in a high-fashion studio setting with dramatic, directional lighting that accentuates the texture of the corduroy, shot from a low angle to emphasize the model's height and the shorts' fit, against a minimalist gray backdrop with subtle shadows for depth, styled with a crisp white tank top and sleek accessories for a polished, editorial look.
```

{{% callout note %}}
Make sure to resize the reference image to your desired aspect ratio.
{{% /callout %}}
