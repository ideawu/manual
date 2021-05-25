## List Devices

```
# Windows
ffmpeg -y -f vfwcap -i list
# OS X
ffmpeg -f avfoundation -list_devices true -i ""
```

### Record Camera

```
# Windows
ffmpeg -y -f vfwcap -r 25 -i 0 out.mp4
-i 0 is the index (zero based) in the list of present capture devices (Driver 0 in this instance).

# OS X
ffmpeg -f avfoundation -s 640x480 -r 30 -i "0" -pixel_format uyvy422 -target pal-vcd -s 640x480 out.mp4

第1个(-i 之前) -s, -r, 摄像头的参数
第2个(-i 之后) -s, -r, 输出视频的参数
```

### 视频按时间长度拆分文件

```
ffmpeg -f segment -segment_time 10 out%03d.mp4
```


