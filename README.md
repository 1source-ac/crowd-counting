# crowd-counting

https://www.analyticsvidhya.com/blog/2019/02/building-crowd-counting-model-python/

```
ffmpeg -i shibuya.mp4 -i frames/heatmaps_bcc/out.avi -t 60 -filter_complex " \
        [0:v]setpts=PTS-STARTPTS, scale=1920x1080[top]; \
        [1:v]setpts=PTS-STARTPTS, scale=1920x1080, \
             format=yuva420p,colorchannelmixer=aa=0.6[bottom]; \
        [top][bottom]overlay=shortest=1" out.mp4
```
