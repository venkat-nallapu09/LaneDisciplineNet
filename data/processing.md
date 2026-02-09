The clear objective for preparing a custom dataset is - 'LaneDisciplineNet
' learns camera-specific geometry; custom datasets ensure correct lane structure, depth scale, and robustness under real deployment conditions.


---

## Frames extraction from raw video

 here I'm using CMD commands (Windows) to extract frames from a video

###  Extract frames at a fixed FPS (e.g., 10 FPS)

 ```
ffmpeg -i input_video.mp4 -vf fps=10 frames\frame_%06d.jpg
```

### Extract frames with resizing (e.g., 1280×720)

```
ffmpeg -i input_video.mp4 -vf "fps=10,scale=1280:720" frames\frame_%06d.jpg

```

### Extract frames between timestamps
```
ffmpeg -ss 00:01:00 -to 00:03:00 -i input_video.mp4 frames\frame_%06d.jpg

```

-----

This hugging face repo consists of un-annotated img frames extracted from raw video input

```  
https://huggingface.co/datasets/nallapuvenkat/traffic-lane-data
```
-----

Now, we have to annotate them so that, we can train a model on our data. for this, I'm using _labelimg_.
For installing labelimg, open CMD

```
pip install labelimg
```

& for opening just type label img
