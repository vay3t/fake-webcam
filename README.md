# Fake Webcam

### Install
```bash
sudo apt-get build-essential libelf-dev linux-headers-$(uname -r) ffmpeg
wget https://github.com/umlaeute/v4l2loopback/archive/v0.12.3.tar.gz
tar xvzf v0.12.3.tar.gz
cd v0.12.3
make
sudo make install
sudo depmod -a
sudo modprobe v4l2loopback
ls /dev/video* # check video dev '/dev/video0'
git clone https://github.com/vay3t/fake-webcam
```

### Run
```bash
sudo ./fakeWebcam.sh input_video.mp4 /dev/video2
# if u need exit press 'q'
```

### Check Cam
```bash
ffplay /dev/video2
```
