# Raspberry-Car-Cam

Deployed on my driveway. It detects vehicles that’s going over 50mph and captures their car plates. Sends the car plates, speeds, and their photos my email bi-weekly. Personal Info's been deleted. 

### Annotate a Video with FFMPEG
```
ffmpeg -i ./example.MOV -vf "drawtext=fontfile=/System/Library/Fonts/SFNSMono.ttf:text='Stack Overflow':fontcolor=white:fontsize=124:box=1:boxcolor=black@0.5:boxborderw=5:x=(w-text_w)/2:y=(h-text_h)/2:enable='between(t,1,3)'" -codec:a copy example-labeled.mp4
```

### Execute Script
```
GOOGLE_APPLICATION_CREDENTIALS="/var/www/html/app/gcp-key.json" node image-capture.js
```

### Convert a video from .MOV to .mp4
```
ffmpeg -i my-video.mov -vcodec h264 -acodec mp2 my-video.mp4
```

### Video to Frames
```
ffmpeg -i example.MP4 -r 1 ./frames/thumb%04d.png -hide_banner
```
