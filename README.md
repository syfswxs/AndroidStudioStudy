# 安卓大白话笔记
使用最大白话的语言描述Android开发中实现的功能，本文略掉Androidstudio的安装教程，需要的可自行百度。
#### 工具
* AndroidStudio
#### ！必读说明！
本文使用了大量的实际操作图文进行讲解，所以对于github图片加载不出来用户可先解决github图片加载问题后再进行学习，不然本教程将无法阅读。以下提供了一个方法，本人亲测有效。如果链接失效，请自行百度解决，养成先自己解决问题的好习惯。
* [修复github图片加载问题的方法](https://www.jianshu.com/p/3eacebfc55ab "点击查看")

      使用此方法时请阅读下方相关留言会更有帮助。
    
---    
## （一） 使用AndroidStudio的一些小技巧
* ### 代码自动排版快捷键
    * Ctrl + Alt + L
* ### 自动导入包快捷键
    * Alt + Enter
* ### 展开收缩代码快捷键
    * 使用Ctrl Shift +或-，就可以展开或收起全部代码。
    * Ctrl + 或 - 对当前方法展开或者收起
* ### Toast提示框
    * 代码：
    ```java
    Toast.makeText(JgjlActivity.this,"显示的文本:",Toast.LENGTH_SHORT).show();
    ```
    ![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/Toast1.png)
    > JgjlActivity为当前Activity的名称，根据实际情况修改  
    > 文本也根据需要修改
* ### finish()的用法
    * 说明：  
    ![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/finish.jpg)
    > 补充：当设计不需要返回上一个Activity时则调用finish方法。 

---
## （二） 遇到的问题
* ### 使用equals的时候，可能回事null值的对比参数要放后面，如图
    * ![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/equals%E9%97%AE%E9%A2%98.jpg)
* ### 当程序编译没问题，运行的时候又闪退，可以试试clean project
    * ![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/clean%20project.jpg)

---
## （三） 创建工程
>想要做一个app第一步则需要打开AndroidStudio创建工程
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
>这个界面显示了我们进入app后的界面模拟，系统在屏幕中间自动生成了一个文本内容：Hello World!
## （四） 实现功能
* ### 实现布局管理器内的view功能（文本显示、按钮、图片等等）
  * #### 显示文本（TextView文本框组件）
    * 在需要修改的界面activity.xml文件下选中左下角Text栏  
    ![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%96%87%E6%9C%AC%E6%A1%86%E7%BB%84%E4%BB%B6.jpg)
    * 我们看到布局文件的代码内容，如果想修改为其他文本内容，如：想显示“你好！”则在TextView（文本框组件）内的android:text（文本内容）后把"Hello World!"修改为 "你好！"  
    ![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%96%87%E6%9C%AC%E6%A1%86%E7%BB%84%E4%BB%B61.jpg)
    * 修改后我们点击左下角Design栏查看界面，可以看出我们已经完成了最基本的修改文本框内容的基本操作  
    ![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%96%87%E6%9C%AC%E6%A1%86%E7%BB%84%E4%BB%B62.jpg)
    >当然，文本框组件还有更多属性可修改，如字体颜色、字体大小等等  
    [TextView详细用法](https://www.runoob.com/w3cnote/android-tutorial-textview.html)
  * #### 按钮（Button）
    * ##### 添加按钮
      * 按钮组件如同文本组件一样在布局管理器之中添加  
      ![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%8C%89%E9%92%AE%E7%BB%84%E4%BB%B6.png)
      [Button以及ImageButton的详细用法](https://www.runoob.com/w3cnote/android-tutorial-button-imagebutton.html)
    * ##### 按钮背景
    水电费
  * #### 输入框（EditText）
    * 输入框组件如同文本组件一样在布局管理器之中添加  
    ![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E8%BE%93%E5%85%A5%E6%A1%86%E7%BB%84%E4%BB%B6.png)
    [EditText(输入框)详解](https://www.runoob.com/w3cnote/android-tutorial-button-imagebutton.html)
  * #### 图片（ImageView）
    * 图片组件如同文本组件一样在布局管理器之中添加  
    [ImageView(图像视图)](https://www.runoob.com/w3cnote/android-tutorial-imageview.html)
    
---
* ### 内容的布局
  * 从下图我们可以看出编辑界面框住的文本框组件只对应的是模拟界面的一个文本而已，我们视模拟界面中的文本为其中一个元素，而我们需要添加新的文本内容的时候需要在布局管理器中再添加一个文本框组件 
  ![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E5%86%85%E5%AE%B9%E5%B8%83%E5%B1%80.jpg)
  ![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E5%86%85%E5%AE%B9%E5%B8%83%E5%B1%801.jpg)
  * 添加第二段文本  
  ![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E5%86%85%E5%AE%B9%E5%B8%83%E5%B1%802.jpg)
  * 我们可以看出，需要第二段文本时，只需要在布局管理器组件内添加新的文本组件即可，这里边需要给各组件设置id标记，在第二个文本组件里我们需要它排列在第一个文本组件的下方，所以我们需要获取1组件的id再调用android:layout_below代码进行排列。该例子是在**相对布局管理器RelativeLayout**下实现的。  
  [相对布局管理器RelativeLayout详细用法](https://www.runoob.com/w3cnote/android-tutorial-relativelayout.html)
  >当然，AndroidStudio的布局管理器有多种，可自行学习使用

---

