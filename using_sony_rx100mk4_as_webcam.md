# Using Sony RX100 mk4 As Webcam

## Requirements
```
v4l2loopback
gphoto2
```

## Usage
```
sudo modprobe v4l2loopback && gphoto2 --auto-detect && gphoto2 --stdout --capture-movie | ffmpeg -i - -vcodec rawvideo -pix_fmt yuv420p -threads 0 -f v4l2 /dev/video2
```

## Preview Modes

## Setting Up The Camera

## Final Thoughts

