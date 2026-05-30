---
title: "2 - Configuration Commands"
linkTitle: Chapter 2
date: 2024-12-27T14:25:49+08:00
type: book
weight: 2
math: false
highlight: false
tags:
  - chapter
---

<!--more-->

{{< youtube IANcdas-yHs >}}

## Configs

{{< toc >}}

### volume

```bash
config volume [val]
```
8 quiet .. 256 loud

### theme

```bash
config theme [value]
```

auto, blue, classic

### gif_len

```bash
config gif_len [seconds]
```

### gif_reset_mode

```bash
config gif_reset_mode [mode]
```

0: don't reset after recording  
1: reset after each recording

### gif_scale

```bash
config gif_scale [size]
```

1 = 128x128 px  
2 = 256x256 px --> perfectlly fine  
3 = 384x384 px --> perfectlly fine  
4 = 512x512 px  
5 =   
6 =  
7 =  
8 =   

### screenshot_scale

```bash
config screenshot_scale [size]
```

1 = 128x128 px  
2 = 256x256 px --> perfectlly fine  
3 = 384x384 px --> perfectlly fine  
4 = 512x512 px  
5 =   
6 =  
7 =  
8 =   

### splore_filter

```bash
config splore_filter
```

wip.

### tab_width

```bash
config tab_width [width]
```

1  
2 --> perfect for beginners  
3  

### draw_tabs

```bash
config draw_tabs [on | off]
```

when on, tab characters are drawn in the code editor.

### Saving config

Education edition users can't save the config settings after closing the browser. Here are the common settings.

```
config volume 200
```

```
config gif_len 30
```

```
config tab_width 2
```

```
config draw_tabs on
```
