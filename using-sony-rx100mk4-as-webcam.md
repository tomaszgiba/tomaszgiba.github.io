# Using Sony RX100 mk4 As Webcam in Ubuntu Linux

First, install these:
```bash
sudo apt install v4l2loopback gphoto2 ffmpeg
```
Use your camera dial to select a mode. I usually use auto. You can get very crisp image by selecting video but rx100 overheats. After every mode change you should stop and start (the following) cmd again.

Usage:
```bash
sudo modprobe v4l2loopback && gphoto2 --auto-detect && gphoto2 --stdout --capture-movie | ffmpeg -i - -vcodec rawvideo -pix_fmt yuv420p -threads 0 -f v4l2 /dev/video2
```

Now the dummy webcam device will show in your zoom. 
