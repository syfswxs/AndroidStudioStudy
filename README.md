# 安卓大白话笔记
使用最大白话的语言描述Android开发中实现的功能

---
## 使用AndroidStudio的一些小技巧
### 代码自动排版快捷键
  * Ctrl + Alt + L
### 自动导入包快捷键
  * Alt + Enter
### 展开收缩代码快捷键
  * 使用Ctrl Shift +或-，就可以展开或收起全部代码。
  * Ctrl + 或 - 对当前方法展开或者收起
### Toast提示框
  代码：
  ```java
  Toast.makeText(JgjlActivity.this,"显示的文本:",Toast.LENGTH_SHORT).show();
  ```
    JgjlActivity为当前Activity的名称，根据实际情况修改
    文本也根据需要修改
 ![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/Toast1.png)
### finish()的用法
说明：
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/finish.jpg)
    补充：当设计不需要返回上一个Activity时则调用finish方法。
## 遇到的问题
 ### 使用equals的时候，可能回事null值的对比参数要放后面，如图
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/equals%E9%97%AE%E9%A2%98.jpg)
 ### 当程序编译没问题，运行的时候又闪退，可以试试clean project
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/clean%20project.jpg)
