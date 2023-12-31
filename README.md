﻿# unity-PointCloudStreaming
This repo contain some unity scripts for point cloud streaming.

# Tutorial

## PCS setup

### unity side
(1) Clone this repo under your unity project **Asset/**
```
$ git clone https://github.com/ARG-NCTU/unity-PointTrobleCloudStreaming
```

(2-1) Download **opencvsharp** on [NAS](http://gofile.me/773h8/QzkncjedT) and add into your unity project.

![](/Tutorials/Image/image9.png)

(2-2) Change settings in Edit/Project Settings/Player/Other Setting/Configuration
1. change **Scripting Backend** to **Mono**
2. change **Active Input Handling** to **Both**

then,unity will reopen the project

![](/Tutorials/Image/image5.png)

(3) There are two objects you need in your unity project 
> [!NOTE]
> you can try example_scene in unity-PointCloudStreaming folder

- Camera_view
  ![](/Tutorials/Image/image3.png)
- PCS_test
  ![](/Tutorials/Image/image6.png)

(4) Drag **Camera_view** into **Update_rosip/Desired_object** and change your rosIP

![](/Tutorials/Image/image11.png)

### ROS side

(1) You need a camera to send Depth image and RGB image
> [!NOTE]
> type:Sensor.CompressedImage

(2) Check your IP and you will need in unity side
```
$ ifconfig
```

(3) Launch rosbridge
```
$ launch rosbridge_server rosbridge_websocket.launch
```

(4) Get camera info and add to **PCS_test/RGBD Merger(Script)** in unity side
```
$ rostopic echo /camera_left/color/camera_info
```

## Problem solving
If you meet unity material gray out can't edit for object like the figure below.

![](/Tutorials/Image/image4.png)

You can create a new material in your project window and drag it on the object, then you should be able to edit it.
