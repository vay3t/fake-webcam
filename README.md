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
sudo insmod v4l2loopback.ko exclusive_caps=1 video_nr=3 card_label="Fake"
ls /dev/video* # check video dev '/dev/video3'
git clone https://github.com/vay3t/fake-webcam
```

### Run
```bash
sudo ./fakeWebcam.sh mefunaronxd.mp4 /dev/video3
# if u need exit press 'q'
# Now open Chrome
# Set Camera 'Fake'
```

### Check Cam
```bash
ffplay /dev/video2
```
