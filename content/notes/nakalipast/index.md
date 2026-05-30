---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Nakalipast"
subtitle: ""
summary: ""

categories:
  - 
tags: 
  - 

date: 2025-05-22T15:35:50+08:00
lastmod: 2025-05-22T15:35:50+08:00

draft: false

_build:
  render: always
  list: never
---

## Kdenlive

BG sound: -25db  
BG 1 Duration: 0 0 3430 1  
BG 2 Duration: 3430 0 3430 1  

## Kokoro

```
!pip install -q kokoro>=0.9.4 soundfile
!apt-get -qq -y install espeak-ng > /dev/null 2>&1
```

```
from kokoro import KPipeline
from IPython.display import display, Audio
import soundfile as sf
import torch
```

```
pipeline = KPipeline(lang_code='a')
```

```
text = '''
Rare, Striking, and Powerful Old Photos of the Philippines You've Likely Never Seen. Part 2.
'''
```

```
generator = pipeline(
    text, voice='am_michael', # <= change voice here
    speed=1, split_pattern=r'\n+'
)
for i, (gs, ps, audio) in enumerate(generator):
    print(i)  # i => index
    print(gs) # gs => graphemes/text
    print(ps) # ps => phonemes
    display(Audio(data=audio, rate=24000, autoplay=i==0))
    sf.write(f'{i}.wav', audio, 24000) # save each audio file
```

```
Rare, Striking, and Powerful Old Photos of the Philippines You've Likely Never Seen. Part 2.
```

## Ep 1

Refined by: 
* Original Format: Photo, Print, Drawing 
* Available Online 
* Date: 1800 to 1899 
* Location: Philippines

Link: https://www.loc.gov/photos/?dates=1800/1899&fa=location:philippines&q=philippines

## Ep 2

Refined by: 
* Original Format: Photo, Print, Drawing 
* Available Online 
* Date: 1800 to 1899 
* Location: Philippines

Link: https://www.loc.gov/photos/?dates=1800/1899&fa=location:philippines&q=philippines
