# <span id="ml"> 目录</span>
- [ 安卓大白话笔记](#head1)
	- [ 工具](#head2)
	- [ ！必读说明！](#head3)
- [（一） 使用AndroidStudio的一些小技巧](#head4)
- [ 代码自动排版快捷键](#head5)
- [ 自动导入包快捷键](#head6)
- [ 展开收缩代码快捷键](#head7)
- [ Toast提示框](#head8)
- [ finish()的用法](#head9)
- [（二） 遇到的问题](#head10)
- [使用equals的时候，可能回事null值的对比参数要放后面，如图  ](#head11)
- [当程序编译没问题，运行的时候又闪退，可以试试clean project](#head12)
- [（三） 创建工程](#head13)
- [（四） 实现功能](#head14)
- [ 实现布局管理器内的view功能（文本显示、按钮、图片等等）](#head15)
	- [ 显示文本（TextView文本框组件）](#head16)
	- [ 按钮（Button）](#head17)
	- [ 输入框（EditText）](#head18)
	- [ 图片（ImageView）](#head19)
- [内容的布局  ](#head20)
- [ 数据的传输](#head21)
# <span id="head1"> 安卓大白话笔记</span>
使用最大白话的语言描述Android开发中实现的功能，本文略掉Androidstudio的安装教程，需要的可自行百度。
#### <span id="head2"> 工具</span>
* AndroidStudio
#### <span id="head3"> ！必读说明！</span>
本文使用了大量的实际操作图文进行讲解，所以对于github图片加载不出来用户可先解决github图片加载问题后再进行学习，不然本教程将无法阅读。以下提供了一个方法，本人亲测有效。如果链接失效，请自行百度解决，养成先自己解决问题的好习惯。
* [修复github图片加载问题的方法](https://www.jianshu.com/p/3eacebfc55ab "点击查看")
>使用此方法时请阅读下方相关留言会更有帮助。

---    
## <span id="head4">（一） 使用AndroidStudio的一些小技巧</span>
### <span id="head5"> 代码自动排版快捷键</span>
* Ctrl + Alt + L
### <span id="head6"> 自动导入包快捷键</span>
* Alt + Enter
### <span id="head7"> 展开收缩代码快捷键</span>
* 使用Ctrl Shift +或-，就可以展开或收起全部代码。
* Ctrl + 或 - 对当前方法展开或者收起
### <span id="head8"> Toast提示框</span>
* 代码：
```java
Toast.makeText(JgjlActivity.this,"显示的文本:",Toast.LENGTH_SHORT).show();
```
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/Toast1.png)
> JgjlActivity为当前Activity的名称，根据实际情况修改  
> 文本也根据需要修改
### <span id="head9"> finish()的用法</span>
* 说明：  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/finish.jpg)
> 补充：当设计不需要返回上一个Activity时则调用finish方法。 

---
## <span id="head10">（二） 遇到的问题</span>
### <span id="head11">使用equals的时候，可能回事null值的对比参数要放后面，如图  </span>
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/equals%E9%97%AE%E9%A2%98.jpg)
### <span id="head12">当程序编译没问题，运行的时候又闪退，可以试试clean project</span>
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/clean%20project.jpg)  
[回到目录](#ml)

---
## <span id="head13">（三） 创建工程</span>
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
## <span id="head14">（四） 实现功能</span>
### <span id="head15"> 实现布局管理器内的view功能（文本显示、按钮、图片等等）</span>
#### <span id="head16"> 显示文本（TextView文本框组件）</span>
* 在需要修改的界面activity.xml文件下选中左下角Text栏  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%96%87%E6%9C%AC%E6%A1%86%E7%BB%84%E4%BB%B6.jpg)
* 我们看到布局文件的代码内容，如果想修改为其他文本内容，如：想显示“你好！”则在TextView（文本框组件）内的android:text（文本内容）后把"Hello World!"修改为 "你好！"  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%96%87%E6%9C%AC%E6%A1%86%E7%BB%84%E4%BB%B61.jpg)
* 修改后我们点击左下角Design栏查看界面，可以看出我们已经完成了最基本的修改文本框内容的基本操作  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%96%87%E6%9C%AC%E6%A1%86%E7%BB%84%E4%BB%B62.jpg)
>当然，文本框组件还有更多属性可修改，如字体颜色、字体大小等等  
[TextView详细用法](https://www.runoob.com/w3cnote/android-tutorial-textview.html)
#### <span id="head17"> 按钮（Button）</span>
* ##### 添加按钮
* 按钮组件如同文本组件一样在布局管理器之中添加  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%8C%89%E9%92%AE%E7%BB%84%E4%BB%B6.png)
[Button以及ImageButton的详细用法](https://www.runoob.com/w3cnote/android-tutorial-button-imagebutton.html)
* ##### 按钮背景修改
* 展示  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%8C%89%E9%92%AE%E7%BB%84%E4%BB%B6_%E6%8C%89%E9%92%AE%E8%83%8C%E6%99%AF.png)
* 实现
>把按钮的四角改成有弧度的偏椭圆形，视觉上更美观。
* 右键drawable文件夹->New->Drawable resource file
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%8C%89%E9%92%AE%E7%BB%84%E4%BB%B6_anbj_1.png)
* 自定义名字->ok
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%8C%89%E9%92%AE%E7%BB%84%E4%BB%B6_anbj_2.png)
* 如图修改创建好的xml文件内容，就事先设置好了背景图片
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%8C%89%E9%92%AE%E7%BB%84%E4%BB%B6_anbj_3.png)
* [文件代码源文件](https://github.com/syfswxs/AndroidStudioStudy/blob/master/code/baocun_bt_bg.xml)
>可点击源文件参考代码
* 再回到当前activity的xml布局文件中在需要修改的按钮组件里修改android:background="@drawable/bt_baocun"内容，获取设置好的背景图片id即可
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%8C%89%E9%92%AE%E7%BB%84%E4%BB%B6_anbj_4.png)
* ##### 按钮点击变色
* 展示  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/gif/%E6%8C%89%E9%92%AE%E5%8F%98%E8%89%B2.gif)
* 实现
>按钮点击颜色的变化会带来好的交互体验
* 思路是在按下的时候换另一个背景图片就行了，所以我们只需要再新建一个背景图片，其他属性都相同只是颜色不同从而达到变色效果
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%8C%89%E9%92%AE%E7%BB%84%E4%BB%B6_anbs.png)
* 我们现在准备好了两个背景图，继续右键drawable文件夹->New->Drawable resource file新建一个xml文件，代码如下
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%8C%89%E9%92%AE%E7%BB%84%E4%BB%B6_anbs_1.png)
* [文件代码源文件](https://github.com/syfswxs/AndroidStudioStudy/blob/master/code/bt_baocun.xml)
>可点击源文件参考代码
#### <span id="head18"> 输入框（EditText）</span>
* 输入框组件如同文本组件一样在布局管理器之中添加  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E8%BE%93%E5%85%A5%E6%A1%86%E7%BB%84%E4%BB%B6.png)
[EditText(输入框)详解](https://www.runoob.com/w3cnote/android-tutorial-edittext.html)
#### <span id="head19"> 图片（ImageView）</span>
* 图片组件如同文本组件一样在布局管理器之中添加  
[ImageView(图像视图)](https://www.runoob.com/w3cnote/android-tutorial-imageview.html)

---
### <span id="head20">内容的布局  </span>
* 从下图我们可以看出编辑界面框住的文本框组件只对应的是模拟界面的一个文本而已，我们视模拟界面中的文本为其中一个元素，而我们需要添加新的文本内容的时候需要在布局管理器中再添加一个文本框组件 
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E5%86%85%E5%AE%B9%E5%B8%83%E5%B1%80.jpg)
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E5%86%85%E5%AE%B9%E5%B8%83%E5%B1%801.jpg)
* 添加第二段文本  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E5%86%85%E5%AE%B9%E5%B8%83%E5%B1%802.jpg)
* 我们可以看出，需要第二段文本时，只需要在布局管理器组件内添加新的文本组件即可，这里边需要给各组件设置id标记，在第二个文本组件里我们需要它排列在第一个文本组件的下方，所以我们需要获取1组件的id再调用android:layout_below代码进行排列。该例子是在**相对布局管理器RelativeLayout**下实现的。  
[相对布局管理器RelativeLayout详细用法](https://www.runoob.com/w3cnote/android-tutorial-relativelayout.html)
>当然，AndroidStudio的布局管理器有多种，可自行学习使用

---
### <span id="head21"> 数据的传输</span>
>获取输入的信息并使用  
* 输入信息是通过输入框等view输入的，我们要获得输入的数据，则要到与之对应的java文件里编写代码。在此我们以下图id为m_e_r的EditText为例  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%95%B0%E6%8D%AE%E4%BC%A0%E8%BE%93_1.png)
* 获取输入的内容则要到与之对应的java文件里编辑代码，当我们创建新的activity的时候系统会自动生成与之对应的java文件如图所示，我们点开MainActivity.java文件  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%95%B0%E6%8D%AE%E4%BC%A0%E8%BE%93_2.png)
* 首先我们要new出一个bundle，在这里我们可以理解为我们先找来一个盒子用于打包我们要获取的数据
```java
Bundle bundle = new Bundle();
```  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%95%B0%E6%8D%AE%E4%BC%A0%E8%BE%93_4.png)
* 现在bundle盒子准备好了，我们要获取数据。new一个字符串格式的r通过寻找id的方式锁定内容。即把输入的内容赋值给r。
```java
String r = ((EditText) findViewById(R.id.m_e_r)).getText().toString();//获取日的值
```  
* 接下来要把r放入准备好的bundle盒子中,
```java
bundle_c.putCharSequence("r", r);//把r的值打包到bundle包裹中取件密码为r
```  
>因为盒子里不只放入的是一个数据，所以设置好取件密码，这样后续从里面获取数据的时候方便快捷  
* 我们把数据打包好之后，需要呼叫快递员帮我们上门取件
```java
Intent intent_c = new Intent(MainActivity.this, CksjActivity.class);//new一个intent_c快递员送数据至CksjActivity界面
```  
>intent_c为上门取件的快递员，MainActivity为寄货地址，CksjActivity为收获地址，根据自己的需求而修改  
* 上门取件的快递员已经联系好，接下来我们要把包装好的bundle包裹给快递员配送
```java
intent_c.putExtras(bundle);//把bundle包裹给intent_c快递员配送
```  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%95%B0%E6%8D%AE%E4%BC%A0%E8%BE%93_5.png)
* 以上我们完成了数据的打包以及传输接下来我们跳到目的地CksjActivity.java文件接收数据
```java
/**************接应快递员取包裹***************************/
Intent intent = getIntent();//与intent快递员取得联系
final Bundle bundle = intent.getExtras();//我们找来新的bundle盒子接过快递员递给的快递
/*****接收加工材料******/
final String r = bundle.getString("r");//我们通过取件密码r从包裹中得到r并存在自家仓库中的r位置上
```  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%95%B0%E6%8D%AE%E4%BC%A0%E8%BE%93_3.png)
* 我们就完成了界面之间数据的传输，需要使用的时候直接调用仓库里的r即可。


