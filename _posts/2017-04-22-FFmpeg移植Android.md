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

- Error:FAILURE: Build failed with an exception.
  + What went wrong:
Execution failed for task ':app:compileDebugNdk'.
> Error: Your project contains C++ files but it is not using a supported native build system.
Consider using CMake or ndk-build integration with the stable Android Gradle plugin:
 https://developer.android.com/studio/projects/add-native-code.html
or use the experimental plugin:
 http://tools.android.com/tech-docs/new-build-system/gradle-experimental.
  + Try:
Run with --stacktrace option to get the stack trace. Run with --debug option to get more log output.
