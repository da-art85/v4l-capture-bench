# v4l-capture-bench

V4L capture example from LinuxTV.org: http://linuxtv.org/downloads/v4l-dvb-apis/capture-example.html

Compile and run with param -c frames_number

Example:
```
make
v4l2-ctl -p 30
./v4l-capture -c 1000
```
This will capture 1000 frames and calculate the time took. v4l2-ctl sets 30 fps frame rate, so you should expect same actual frame rate

To save single frame to a file use -o and pipe stdout to file:
```
./v4l-capture -c 1 -o 1> test.jpg
```
To change frame format:
```
v4l2-ctl -v width=1280,height=720,pixelformat=0
```
