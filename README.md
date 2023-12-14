﻿# unity-PointCloudStreaming
This repo contain some unity scripts for point cloud streaming.

# Tutorial

## PCS setup

### unity side
(1) Clone this repo under your unity project **Asset/**
```
git clone git@github.com:ARG-NCTU/unity-PointCloudStreaming.git
```

(2) Download **opencvsharp** on [NUS](http://gofile.me/773h8/QzkncjedT) and add into your unity project.

![](/Tutorials/Image/image9.png)

(3) There are two objects you need in your unity project 
> [!NOTE]
> you can try example_scene in unity-PointCloudStreaming folder

- Camera_view
  ![](/Tutorials/Image/image3.png)
- PCS_test
  ![](/Tutorials/Image/image6.png)

### ROS side

(1) You need a camera to send Depth image and RGB image.
> [!NOTE]
> type:Sensor.CompressedImage

(2) Launch rosbridge
```
launch rosbridge_server rosbridge_websocket.launch
```

## Problem solving
if you meet unity material gray out can't edit for object like the figure below.

![](/Tutorials/Image/image4.png)

for prefab
![](/Tutorials/Image/image7.png)

select material -> extract material

![](/Tutorials/Image/image1.png)
![](/Tutorials/Image/image2.png)
