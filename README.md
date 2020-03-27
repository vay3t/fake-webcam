# Fake Webcam

### Install
```bash
sudo apt-get install v4l2loopback-dkms ffmpeg
sudo modprobe v4l2loopback
ls /dev/video* # check video dev '/dev/video0'
git clone https://github.com/vay3t/fake-webcam
```

### Run
```bash
sudo ./fakeWebcam.sh input_video.mp4 /dev/video0
# if u need exit press 'q'
```

### Check Cam
```bash
ffplay /dev/video0
```
