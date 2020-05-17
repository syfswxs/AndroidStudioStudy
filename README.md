# 安卓大白话笔记
使用最大白话的语言描述Android开发中实现的功能，本文略掉Androidstudio的安装教程，需要的可自行百度。
## 工具
AndroidStudio
## 使用AndroidStudio的一些小技巧
### 代码自动排版快捷键
  * Ctrl + Alt + L
### 自动导入包快捷键
  * Alt + Enter
### 展开收缩代码快捷键
  * 使用Ctrl Shift +或-，就可以展开或收起全部代码。
  * Ctrl + 或 - 对当前方法展开或者收起
### Toast提示框
  * 代码：
  ```java
  Toast.makeText(JgjlActivity.this,"显示的文本:",Toast.LENGTH_SHORT).show();
  ```
    JgjlActivity为当前Activity的名称，根据实际情况修改
    文本也根据需要修改
 ![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/Toast1.png)
### finish()的用法
  * 说明：
 ![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/finish.jpg) 
 
     补充：当设计不需要返回上一个Activity时则调用finish方法。
## 遇到的问题
### 使用equals的时候，可能回事null值的对比参数要放后面，如图
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/equals%E9%97%AE%E9%A2%98.jpg)
### 当程序编译没问题，运行的时候又闪退，可以试试clean project
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/clean%20project.jpg)

## 创建工程
想要做一个app第一步则需要打开AndroidStudio创建工程
* 打开AndroidStudio
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%96%B0%E5%BB%BA%E5%B7%A5%E7%A8%8B.jpg)
* 选择EmptyActivity
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%96%B0%E5%BB%BA%E5%B7%A5%E7%A8%8B1.jpg)
* 设置相关信息
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%96%B0%E5%BB%BA%E5%B7%A5%E7%A8%8B2.jpg)
* 创建好后的界面
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%96%B0%E5%BB%BA%E5%B7%A5%E7%A8%8B3.jpg)
* 程序自动生成了我们创建的app程序入口，我们此时想编辑进入程序的第一个界面里的内容我们首先要点击切换至入口的布局文件activity_main.xml，如图
