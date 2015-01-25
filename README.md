# v4l-capture-bench

V4L capture example from LinuxTV.org: http://linuxtv.org/downloads/v4l-dvb-apis/capture-example.html

Compile and run with param -c frames_number

Example:
```
gcc v4l2-capture.c
v4l2-ctl -p 30
./a.out -c 1000
```
This will capture 1000 frames and calculate the time took. v4l2-ctl sets 30 fps frame rate, so you should expect same actual frame rate
