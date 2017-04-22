---
title: FFmpeg移植Android
date: 2017-04-22 00:00:00 +0800
layout: post
categories:
  - Lab
tags:
  - FFmpeg
  - ANdroid
---

### FFmpeg  Android
- Error: error: linker command failed with exit code 1 

解决方法
1.  build.gradle 中加入
```C
	  ndk {
             moduleName "mtptest"
             abiFilters "armeabi-v7a"//CPU平台设置
             cFlags '-std=c++11 -fexceptions -fpermissive'
             stl 'stlport_static'
             }
```
2. Android.mk Application.mk 编码设为UTF8