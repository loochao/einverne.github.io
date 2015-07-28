---
layout: post
title: "毕设相关"
description: ""
category: 
tags: [skills, ]
---

##Word目录自动生成
如果想要目录自动生成，就必须事先对文章标题进行格式化，我使用的方式是在`大纲视图`中对章节标题进行一级二级三级格式化。另外的方法是通过格式中标题去给每一个标题添加样式。网上的教程太多了，我就做一个备忘吧，以后说不定在其他论文中也要生成目录。在格式化标题之后，导航窗口基本上就能显示一个简单的目录了，此时再自动生成目录一般不会出现太大的问题。

##Word页眉页脚
有些页需要重新从1页开始编号，则要在该页之前插入分节符。如需生成`第1页 共XX页`这种格式的页码，最好不要手工输入总共的页码，因为可能需要修改论文内容，而如果手工修改可能最后不会自动更新，会造成很大的问题。最好是在文档部件->域->编号里面插入总页数。


##MP4转gif
项目因为在Android手机上，需要录制视频展示，Android(API level 19) 开发工具中提供了录制视频的方法:

    adb shell screenrecord /sdcard/demo.mp4

在PC下连接手机,运行以上命令即可录制手机屏幕，视频格式为MP4,存放在手机SD卡，默认录制时间180s.
该命令还有其他一些参数，运行:

    adb shell screenrecord --help

可以查看所有参数。几个可能会使用到的参数是:

- \-\-time\-limit 10 录制时长
- \-\-size 1280*720 录制分辨率大小
- \-\-bit-rate 6000000 比特率

官方文档: http://developer.android.com/tools/help/adb.html#screenrecord
中文参考: http://blog.csdn.net/wirelessqa/article/details/22725581

录制完视频之后面临的一个问题是，怎么转成gif供PPT或者演示使用。最初想到的方法是使用Photoshop，也找到了一些方法能够将MP4视频转成Web使用gif，但是因为Photoshop将视频每一帧都保存，消耗内存太大，之后适当的调整了几次效果都不是很好，生成的文件也比较大。所以后来就直接使用了迅雷看看的gif生成了，不过缺点很明显，分辨率被调到很小，图像变得不清晰了。