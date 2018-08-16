---
layout: post
title: "Linux 下超好用字典 GoldenDict"
tagline: ""
description: ""
category: 经验总结
tags: [dict, linux, goldendict, youdao, ]
last_updated:
---

最近在使用 Linux 版有道的时候发现非常卡，影响正常使用，所以就发现了这个 GoldenDict。以前在 Win 下用过 [lingoes](http://www.lingoes.cn/) 但是无奈只有 Win 版本。

GoldenDict 是一种开源词典，它像 Eudict、Mdict、Lingoes 以及 BlueDict 等词典一样可以加载外挂词典文件。

## 安装

    sudo apt install goldendict

- For linux: https://github.com/goldendict/goldendict/wiki/Early-Access-Builds-for-Linux-Portable
- For Mac OS X : https://github.com/goldendict/goldendict/wiki/Early-Access-Builds-for-Mac-OS-X
- For Windows: https://github.com/goldendict/goldendict/wiki/Early-Access-Builds-for-Windows

## 功能特色

支持的字典格式

- Babylon .BGL files, complete with images and resources
- StarDict .ifo/.dict./.idx/.syn dictionaries
- Dictd .index/.dict(.dz) dictionary files
- ABBYY Lingvo .dsl source files, together with abbreviations. The files can be optionally compressed with dictzip. Dictionary resources can be packed together into a .zip file.
- ABBYY Lingvo .lsa/.dat audio archives. Those can be indexed separately, or be referred to from .dsl files.
- Lingoes 灵格斯词霸 .ld2 这里需要指出来的是 ld2 格式只有移动版 Android 才支持

更多支持的格式可以参考[这里](https://github.com/goldendict/goldendict/wiki/Supported-Dictionary-Formats)

支持 Windows, Linux, Mac, Android，Android 版是[商业软件](https://play.google.com/store/apps/details?id=mobi.goldendict.android)，免费版最多能用 5 本词典，支持分享查词。

完美支持单词复数，ing 形式等变形（软件设置中 morphology）


## 字典安装

### 在线字典
有道的源

    http://dict.youdao.com/search?q=%GDWORD%&ue=utf8

Bing 中文的源

    https://cn.bing.com/dict/search?q=%GDWORD%

iciba

    http://www.iciba.com/%GDWORD%/

zdic

    http://www.zdic.net/sousuo/?q=%GDWORD%

### 离线字典

简明英汉字典增强版，收录 324 万词条

- <https://github.com/skywind3000/ECDICT/wiki/%E7%AE%80%E6%98%8E%E8%8B%B1%E6%B1%89%E5%AD%97%E5%85%B8%E5%A2%9E%E5%BC%BA%E7%89%88>

牛津高阶英汉双解 第四版 (En-zh_CN)- 英汉双解，bgl 格式，排版美观，无发音


解压后，在词典 - 文件添加路径即可

    http://download.huzheng.org/zh_CN/

## 词形匹配
GoldenDict 默认情况下，比如屏幕取词获取 “stores” 默认是没有结果的，但是其实并不是 GoldenDict 的问题，只需要导入构词法规则库就能够让 GoldenDict 自动判断复数从而进行查词。

下载英语构词法规则库：

然后在 编辑 ->词典 ->词典来源 ->构词法规则库 中设置规则目录，在我的电脑上是 `/usr/share/myspell/dicts` ，当然也可以将下载的文件拷贝到该目录中记载即可。

## reference

- <http://goldendict.org/>
- Source Code <https://github.com/goldendict/goldendict>
- <https://blog.yuanbin.me/posts/2013-01/2013-01-31_23-07-00/>
- <http://forum.ubuntu.org.cn/viewtopic.php?f=95&t=265588>
- lingoes 词典 <http://www.lingoes.cn/zh/dictionary/index.html>
- <https://xinyo.org/archives/61412/> 朗文 5、韦伯 11、牛津 8（均含发音）词典包
- <https://www.cnblogs.com/oucbl/p/6839493.html>