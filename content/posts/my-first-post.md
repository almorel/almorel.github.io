---
title: "Encodage h265 via ffmpeg"
description: "Utiliser ffmpeg pour transcoder une vidéo en h265"
date: 2024-01-27T13:45:16+01:00
tags: ["ffmpeg"]
draft: false
#tldr: "intro"
---

## Encoder des fichiers VOD en h265

```bash
ffmpeg -i concat:VTS_06_1.VOB\|VTS_06_2.VOB\|VTS_06_3.VOB\|VTS_06_4.VOB\|VTS_06_5.VOB\|VTS_06_6.VOB \      
    -vsync 1 \                                                                                             
    -threads 0 \                                                                                           
    -aspect 16:9 \                                                                                         
    -map 0:v \                                                                                             
    -map 0:3 \                                                                                             
    -metadata title="TEST" \                                                                               
    -c:v libx265 \                                                                                         
    -preset ultrafast \                                                                                    
    -x265-params \                                                                                         
    crf=22:qcomp=0.8:aq-mode=1:aq_strength=1.0:qg-size=16:psy-rd=0.7:psy-rdoq=5.0:rdoq-level=1:merange=44 \
    -c:a ac3 \                                                                                             
    -b:a:1 320k \                                                                                          
    TEST.mkv                                                                                               
```
