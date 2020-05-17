# 安卓大白话笔记
使用最大白话的语言描述Android开发中实现的功能，本文略掉Androidstudio的安装教程，需要的可自行百度。
#### 工具
* AndroidStudio
#### ！必读说明！
本文使用了大量的实际操作图文进行讲解，所以对于github图片加载不出来用户可先解决github图片加载问题后再进行学习，不然本教程将无法阅读。以下提供了一个方法，本人亲测有效。如果链接失效，请自行百度解决，养成先自己解决问题的好习惯。
* [修复github图片加载问题的方法](https://www.jianshu.com/p/3eacebfc55ab "点击查看")

      使用此方法时请阅读下方相关留言会更有帮助。
    
## (一)使用AndroidStudio的一些小技巧
### 代码自动排版快捷键
  * Ctrl + Alt + L
  
 ---
### 自动导入包快捷键
  * Alt + Enter
  
 ---
### 展开收缩代码快捷键
  * 使用Ctrl Shift +或-，就可以展开或收起全部代码。
  * Ctrl + 或 - 对当前方法展开或者收起
  
 ---
### Toast提示框
  * 代码：
  ```java
  Toast.makeText(JgjlActivity.this,"显示的文本:",Toast.LENGTH_SHORT).show();
  ```
    JgjlActivity为当前Activity的名称，根据实际情况修改
    文本也根据需要修改
 ![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/Toast1.png)
 
 ---
### finish()的用法
  * 说明：
 ![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/finish.jpg) 
 
     补充：当设计不需要返回上一个Activity时则调用finish方法。
     
 ---
## (二)遇到的问题
### 使用equals的时候，可能回事null值的对比参数要放后面，如图
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/equals%E9%97%AE%E9%A2%98.jpg)
### 当程序编译没问题，运行的时候又闪退，可以试试clean project
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/clean%20project.jpg)

## （三）创建工程
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
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%96%B0%E5%BB%BA%E5%B7%A5%E7%A8%8B4.jpg)

    这个界面显示了我们进入app后的界面模拟，系统在屏幕中间自动生成了一个文本内容：Hello World!
## （四）实现功能
### 显示文本
* 在需要修改的界面activity.xml文件下选中左下角Text栏
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%96%87%E6%9C%AC%E6%A1%86%E7%BB%84%E4%BB%B6.jpg)
* 我们看到布局文件的代码内容，如果想修改为其他文本内容，如：想显示“你好！”则在TextView（文本框组件）内的android:text（文本内容）后把"Hello World!"修改为 "你好！"
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%96%87%E6%9C%AC%E6%A1%86%E7%BB%84%E4%BB%B61.jpg)
* 修改后我们点击左下角Design栏查看界面，可以看出我们已经完成了最基本的修改文本框内容的基本操作
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%96%87%E6%9C%AC%E6%A1%86%E7%BB%84%E4%BB%B62.jpg)
