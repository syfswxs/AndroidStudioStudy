# <span id="ml">目录</span>
- [ 安卓大白话笔记](#head1)
	- [ 工具](#head2)
	- [ ！必读说明！](#head3)
	- [ （一）使用AndroidStudio的一些小技巧](#head4)
		- [1. 代码自动排版快捷键](#head5)
		- [2. 自动导入包快捷键](#head6)
		- [3. 展开收缩代码快捷键](#head7)
		- [4. Toast提示框](#head8)
		- [5. finish()的用法](#head9)
	- [ （二）遇到的问题](#head10)
		- [1. 使用equals的时候，可能会是null值的对比参数要放后面](#head11)
		- [2. 当程序编译没问题，运行的时候又闪退，可以试试clean project](#head12)
	- [（三） 创建工程](#head13)
	- [（四） 实现功能](#head14)
		- [1. 实现布局管理器内的view功能（文本显示、按钮、图片等等）](#head15)
			- [a. 显示文本（TextView文本框组件）](#head16)
			- [b. 按钮（Button）](#head17)
				- [1. 添加按钮](#head18)
				- [2. 按钮背景修改](#head19)
				- [3. 按钮点击变色](#head20)
			- [c. 输入框（EditText）](#head21)
			- [d. 图片（ImageView）](#head22)
			- [e. 列表选项框（Spinner）](#head23)
				- [1. 添加列表选项框](#head24)
				- [2. 获取下拉列表选中的内容](#head25)
		- [2. 内容的布局](#head26)
		- [3. 数据的传输](#head27)
		- [4. 界面的跳转](#head28)
		- [5. 信息提示框](#head29)
		- [6. 视频启动页](#head30)
		- [7. 自定义上方标题栏](#head31)
		- [8. 仿ios底部菜单](#head32)
		- [9. 动态添加组件](#head33)
		- [10. 布局界面内容超过界面添加滚动条](#head34)
	- [（五） 其他](#head35)
		- [1. 素材下载](#head36)

# <span id="head1"> 安卓大白话笔记</span>
使用最大白话的语言描述Android开发中实现的功能，本文略掉Androidstudio的安装教程，需要的可自行百度。
## <span id="head2"> 工具</span>
* AndroidStudio
## <span id="head3"> ！必读说明！</span>
本文使用了大量的实际操作图文进行讲解，所以对于github图片加载不出来用户可先解决github图片加载问题后再进行学习，不然本教程将无法阅读。以下提供了一个方法，本人亲测有效。如果链接失效，请自行百度解决，养成先自己解决问题的好习惯。
* [修复github图片加载问题的方法](https://www.jianshu.com/p/3eacebfc55ab "点击查看")
>使用此方法时请阅读下方相关留言会更有帮助。
## <span id="head4"> （一）使用AndroidStudio的一些小技巧</span>
### <span id="head5">1. 代码自动排版快捷键</span>
* Ctrl + Alt + L
### <span id="head6">2. 自动导入包快捷键</span>
* Alt + Enter
### <span id="head7">3. 展开收缩代码快捷键</span>
* 使用Ctrl Shift +或-，就可以展开或收起全部代码。
* Ctrl + 或 - 对当前方法展开或者收起
### <span id="head8">4. Toast提示框</span>
* 代码：
```java
Toast.makeText(JgjlActivity.this,"显示的文本:",Toast.LENGTH_SHORT).show();
```
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/Toast1.png)
> JgjlActivity为当前Activity的名称，根据实际情况修改  
> 文本也根据需要修改
### <span id="head9">5. finish()的用法</span>
说明：  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/finish.jpg)
> 补充：当设计不需要返回上一个Activity时则调用finish方法。  
>>>>>>[**【点我回到目录】**](#ml)
## <span id="head10"> （二）遇到的问题</span>
### <span id="head11">1. 使用equals的时候，可能会是null值的对比参数要放后面</span>
* ![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/equals%E9%97%AE%E9%A2%98.jpg)
>>>>>>[**【点我回到目录】**](#ml)
### <span id="head12">2. 当程序编译没问题，运行的时候又闪退，可以试试clean project</span>
* ![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/clean%20project.jpg)  
>>>>>>[**【点我回到目录】**](#ml)
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
>>>>>>[**【点我回到目录】**](#ml)
## <span id="head14">（四） 实现功能</span>
### <span id="head15">1. 实现布局管理器内的view功能（文本显示、按钮、图片等等）</span>
#### <span id="head16">a. 显示文本（TextView文本框组件）</span>
* 在需要修改的界面activity.xml文件下选中左下角Text栏  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%96%87%E6%9C%AC%E6%A1%86%E7%BB%84%E4%BB%B6.jpg)
* 我们看到布局文件的代码内容，如果想修改为其他文本内容，如：想显示“你好！”则在TextView（文本框组件）内的android:text（文本内容）后把"Hello World!"修改为 "你好！"  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%96%87%E6%9C%AC%E6%A1%86%E7%BB%84%E4%BB%B61.jpg)
* 修改后我们点击左下角Design栏查看界面，可以看出我们已经完成了最基本的修改文本框内容的基本操作  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%96%87%E6%9C%AC%E6%A1%86%E7%BB%84%E4%BB%B62.jpg)
>当然，文本框组件还有更多属性可修改，如字体颜色、字体大小等等  
* [TextView详细用法](https://www.runoob.com/w3cnote/android-tutorial-textview.html)  
>>>>>>[**【点我回到目录】**](#ml)
#### <span id="head17">b. 按钮（Button）</span>
##### <span id="head18">1. 添加按钮</span>
* 按钮组件如同文本组件一样在布局管理器之中添加  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%8C%89%E9%92%AE%E7%BB%84%E4%BB%B6.png)
* [Button以及ImageButton的详细用法](https://www.runoob.com/w3cnote/android-tutorial-button-imagebutton.html)  
>>>>>>[**【点我回到目录】**](#ml)
##### <span id="head19">2. 按钮背景修改</span>
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
>>>>>>[**【点我回到目录】**](#ml)
##### <span id="head20">3. 按钮点击变色</span>
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
>>>>>>[**【点我回到目录】**](#ml)
#### <span id="head21">c. 输入框（EditText）</span>
* 输入框组件如同文本组件一样在布局管理器之中添加  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E8%BE%93%E5%85%A5%E6%A1%86%E7%BB%84%E4%BB%B6.png)
* [EditText(输入框)详解](https://www.runoob.com/w3cnote/android-tutorial-edittext.html)  
>>>>>>[**【点我回到目录】**](#ml)
#### <span id="head22">d. 图片（ImageView）</span>
* 图片组件如同文本组件一样在布局管理器之中添加  
* [ImageView(图像视图)](https://www.runoob.com/w3cnote/android-tutorial-imageview.html)  
>>>>>>[**【点我回到目录】**](#ml)
#### <span id="head23">e. 列表选项框（Spinner）</span>
>下拉列表为用户提供了我们设置好的内容选择  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/gif/%E4%B8%8B%E6%8B%89%E5%88%97%E8%A1%A8%E5%B1%95%E7%A4%BA.gif)
* [Spinner(列表选项框)的基本使用](https://www.runoob.com/w3cnote/android-tutorial-spinner.html)  
##### <span id="head24">1. 添加列表选项框</span>
* 如同文本框组件一样在对应的布局文件的布局管理器里添加  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E4%B8%8B%E6%8B%89%E5%88%97%E8%A1%A8_1.png)
* 下拉列表的内容我们需要事先设置好调用就行了，res-values-右键-New-Values resource file
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E4%B8%8B%E6%8B%89%E5%88%97%E8%A1%A8_2.png)
* 设置好文件名称-ok，在<resources></resources>内添加字符串数组<string-array>设置好下拉内容
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E4%B8%8B%E6%8B%89%E5%88%97%E8%A1%A8_3.png)
* 在下拉列表组件里调用即可  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E4%B8%8B%E6%8B%89%E5%88%97%E8%A1%A8_4.png)
>>>>>>[**【点我回到目录】**](#ml)  

##### <span id="head25">2. 获取下拉列表选中的内容</span>
* 来到对应的java文件中修改代码
```java
final Spinner szs = findViewById(R.id.m_s_zs);
szs.setOnItemSelectedListener(new AdapterView.OnItemSelectedListener() {//下拉列表监听器
@Override
public void onItemSelected(AdapterView<?> parent, View view, int position, long id) {
String zs = parent.getItemAtPosition(position).toString();
bundle.putCharSequence("zs", zs);//占时
}

@Override
public void onNothingSelected(AdapterView<?> parent) {

}
});
```  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E4%B8%8B%E6%8B%89%E5%88%97%E8%A1%A8_5.png)
* 这样就完成了下拉列表选中的值的获取     
>>>>>>[**【点我回到目录】**](#ml)  
### <span id="head26">2. 内容的布局</span>
* 从下图我们可以看出编辑界面框住的文本框组件只对应的是模拟界面的一个文本而已，我们视模拟界面中的文本为其中一个元素，而我们需要添加新的文本内容的时候需要在布局管理器中再添加一个文本框组件 
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E5%86%85%E5%AE%B9%E5%B8%83%E5%B1%80.jpg)
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E5%86%85%E5%AE%B9%E5%B8%83%E5%B1%801.jpg)
* 添加第二段文本  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E5%86%85%E5%AE%B9%E5%B8%83%E5%B1%802.jpg)
* 我们可以看出，需要第二段文本时，只需要在布局管理器组件内添加新的文本组件即可，这里边需要给各组件设置id标记，在第二个文本组件里我们需要它排列在第一个文本组件的下方，所以我们需要获取1组件的id再调用android:layout_below代码进行排列。该例子是在**相对布局管理器RelativeLayout**下实现的。  
* [相对布局管理器RelativeLayout详细用法](https://www.runoob.com/w3cnote/android-tutorial-relativelayout.html)
>当然，AndroidStudio的布局管理器有多种，可自行学习使用  
>>>>>>[**【点我回到目录】**](#ml)
### <span id="head27">3. 数据的传输</span>
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
>>>>>>[**【点我回到目录】**](#ml)
### <span id="head28">4. 界面的跳转</span>
>点击按钮跳转至下一个界面  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/gif/%E7%95%8C%E9%9D%A2%E8%B7%B3%E8%BD%AC.gif)
* 首先我们先来到按钮所在界面的java文件中修改代码，给该按钮添加一个单击事件监听器，让系统知道我们按下按钮并做出相应的动作
```java
Button jc = findViewById(R.id.m_b_jc);
jc.setOnClickListener(new View.OnClickListener() {
@Override
public void onClick(View v) {
final Intent intent_j = new Intent(MainActivity.this, JczzActivity.class);//new一个intent_j司机让他送我们到目的地
startActivity(intent_j);//跳转至JczzActivity界面
}
});
```  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E7%95%8C%E9%9D%A2%E8%B7%B3%E8%BD%AC.png)
* 这样我们就实现了界面的跳转
>>>>>>[**【点我回到目录】**](#ml)
### <span id="head29">5. 信息提示框</span>
>点击查看详细信息  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/gif/%E4%BF%A1%E6%81%AF%E6%8F%90%E7%A4%BA%E6%A1%86.gif)
* 首先我们要先设置好信息提示框的内容。在res-values-strings.xml里，在<string name="wqnr">...</string>范围里添加内容
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E4%BF%A1%E6%81%AF%E6%8F%90%E7%A4%BA%E6%A1%86.png)
* 在对应的组件代码里添加单击事件监听器，点击就弹出提示框
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E4%BF%A1%E6%81%AF%E6%8F%90%E7%A4%BA%E6%A1%861.png)
* 这样我们就实现了点击出现信息提示框的功能
>>>>>>[**【点我回到目录】**](#ml)
### <span id="head30">6. 视频启动页</span>
>程序启动的时候视频启动页，点任意地方跳转  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/gif/%E5%90%AF%E5%8A%A8%E9%A1%B5%E8%A7%86%E9%A2%91.gif)
* 其实视频启动页就是个activity活动界面，我们只是把标题栏以及状态栏全部隐藏了，把准备好的视频铺满整个屏幕而已。第一步是先把视频放入到项目当中。右键res文件夹-new-Android Resource Directory
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E8%A7%86%E9%A2%91%E5%90%AF%E5%8A%A8%E9%A1%B5.png)
* 如图选好raw选项
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E8%A7%86%E9%A2%91%E5%90%AF%E5%8A%A8%E9%A1%B51.png)
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E8%A7%86%E9%A2%91%E5%90%AF%E5%8A%A8%E9%A1%B52.png)
* raw文件夹就创建好了，再把视频导入raw文件夹  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E8%A7%86%E9%A2%91%E5%90%AF%E5%8A%A8%E9%A1%B53.png)  

代码
```java
public class MainActivity extends AppCompatActivity {

@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);

getWindow().addFlags(WindowManager.LayoutParams.FLAG_FULLSCREEN);//隐藏状态栏
getSupportActionBar().hide();//隐藏标题栏

/**************点击视频跳转至主界面********************/
VideoView videoview = (CustomVideoView) findViewById(R.id.m_v);
videoview.setOnClickListener(new View.OnClickListener() {
@Override
public void onClick(View v) {
Intent mainintent = new Intent(MainActivity.this, ZjmActivity.class); //使用intent方法，在活动间跳转
startActivity(mainintent);
finish();
}
});

initView();

//*********************设置几秒后自动跳转***********************************/
//        new Handler().postDelayed(new Runnable() {
//            @Override
//            public void run() {
//                Intent mainintent = new Intent(SplashActivity.this, MainActivity.class); //使用intent方法，在活动间跳转
//                startActivity(mainintent);
//                finish();
//            }
//        }, 8000);//设置等待时间，与跳转。


}

private void initView() {
VideoView videoview = (CustomVideoView) findViewById(R.id.m_v);
//设置播放加载路径
videoview.setVideoURI(Uri.parse("android.resource://" + getPackageName() + "/" + R.raw.xiaoshi));
//播放
videoview.start();
/*********循环播放****************/
//监听视频播放完的代码
videoview.setOnCompletionListener(new MediaPlayer.OnCompletionListener() {
@Override
public void onCompletion(MediaPlayer mPlayer) {
// TODO Auto-generated method stub
mPlayer.start();
mPlayer.setLooping(true);
}
});

}
}
```
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E8%A7%86%E9%A2%91%E5%90%AF%E5%8A%A8%E9%A1%B54.png)
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E8%A7%86%E9%A2%91%E5%90%AF%E5%8A%A8%E9%A1%B55.png)
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E8%A7%86%E9%A2%91%E5%90%AF%E5%8A%A8%E9%A1%B56.png)

布局界面代码
```java
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
tools:context=".MainActivity">

<com.example.xiaoshi.CustomVideoView
android:id="@+id/m_v"
android:layout_width="match_parent"
android:layout_height="match_parent" />

<TextView
android:id="@+id/m_t_jr"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_alignParentRight="true"
android:textColor="#F8F7F7"
android:paddingTop="16dp"
android:paddingRight="16dp"
android:text="点击任意地方进入"
/>
</RelativeLayout>
```  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E8%A7%86%E9%A2%91%E5%90%AF%E5%8A%A8%E9%A1%B57.png)
* 最后我们把该视频界面设置为程序进入的第一个界面，在manifests文件夹下的AndroidManifest.xml文件中
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E8%A7%86%E9%A2%91%E5%90%AF%E5%8A%A8%E9%A1%B58.png)
* 在对应的activity里添加以下内容
```java
<intent-filter>
<action android:name="android.intent.action.MAIN" />

<category android:name="android.intent.category.LAUNCHER" />
</intent-filter>
```  
* 如此，我们实现了视频启动页的功能。
>>>>>>[**【点我回到目录】**](#ml)
### <span id="head31">7. 自定义上方标题栏</span>
>自动生成的标题栏通常不满足我们的要求，我们可以自定义标题栏  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E4%B8%8A%E6%96%B9%E6%A0%87%E9%A2%98%E6%A0%8F1.png)
* 右键layout文件夹-New-Layout resource file
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E4%B8%8A%E6%96%B9%E6%A0%87%E9%A2%98%E6%A0%8F2.png)
* 自定义名称
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E4%B8%8A%E6%96%B9%E6%A0%87%E9%A2%98%E6%A0%8F5.png)
* 根据需要布局好组件
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E4%B8%8A%E6%96%B9%E6%A0%87%E9%A2%98%E6%A0%8F3.png)
* 接下来来到需要用到上方标题栏的activity中，在布局管理器当中添加以下代码
```java
<include layout="@layout/title"/>
```  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E4%B8%8A%E6%96%B9%E6%A0%87%E9%A2%98%E6%A0%8F4.png)
* 这样我们就把自定义好的标题栏应用到了activity中
>>>>>>[**【点我回到目录】**](#ml)
### <span id="head32">8. 仿ios底部菜单</span>
* 效果展示  
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/gif/%E4%BB%BFios%E5%BA%95%E9%83%A8%E8%8F%9C%E5%8D%95.gif)
* 实现
* 我们需要在java-包文件夹下新建一个ActionSheetDialog类，在此类中，我们可以设置菜单选项的最大个数等
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E4%BB%BFios%E5%BA%95%E9%83%A8%E8%8F%9C%E5%8D%951.png)
* 点击下方看详细源代码
* [ActionSheetDialog类源码](https://github.com/syfswxs/AndroidStudioStudy/blob/master/code/ActionSheetDialog.java)
* 此类源码中我们为条目设置好了相应的背景图片，如第一个条目是上方两个角为圆弧状，处于中间的条目四方都是直角状，下方的条目则下面两个角为圆弧状。这里我们需要事先设置好背景图片调用即可。
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E4%BB%BFios%E5%BA%95%E9%83%A8%E8%8F%9C%E5%8D%95.jpg)
* 右键drawable文件夹-new-drawable resource file新建文件，设置好相应的名称。
* [条目背景代码](https://github.com/syfswxs/AndroidStudioStudy/blob/master/code/duihuakuang_bg.xml)
* [上方条目背景代码](https://github.com/syfswxs/AndroidStudioStudy/blob/master/code/dibucaidan_bg_top.xml)
* [中间条目背景代码](https://github.com/syfswxs/AndroidStudioStudy/blob/master/code/dibucaidan_bg_middle.xml)
* [下方条目背景代码](https://github.com/syfswxs/AndroidStudioStudy/blob/master/code/dibucaidan_bg_bttom.xml)
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E4%BB%BFios%E5%BA%95%E9%83%A8%E8%8F%9C%E5%8D%954.png)
* 接下来我们调用底部菜单，在按下某个按钮触发发底部菜单，即要使用单击事件监听器
* 代码
```java
//点击右上角添加按钮出现底部弹窗
Button tj = findViewById(R.id.zjm_b_tj);
tj.setOnClickListener(new View.OnClickListener() {
@Override
public void onClick(View v) {
//定义底部菜单
new ActionSheetDialog(ZjmActivity.this)
.builder()
.setCancelable(true)
.setCanceledOnTouchOutside(true)
//定义一个选项
.addSheetItem("记录结果", ActionSheetDialog.SheetItemColor.XiaoShi,
new ActionSheetDialog.OnSheetItemClickListener() {//点击该选项时
@Override
public void onClick(int which) {//跳转至记录结果界面
Intent intent = new Intent(ZjmActivity.this,JgjlActivity.class);
startActivity(intent);
}
})
.addSheetItem("记录过程", ActionSheetDialog.SheetItemColor.XiaoShi,
new ActionSheetDialog.OnSheetItemClickListener() {//点击该选项时
@Override
public void onClick(int which) {
}
})
.show();
}
});
```
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E4%BB%BFios%E5%BA%95%E9%83%A8%E8%8F%9C%E5%8D%952.png)
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E4%BB%BFios%E5%BA%95%E9%83%A8%E8%8F%9C%E5%8D%953.png)
* 如此我们便实现了仿ios底部菜单
>>>>>>[**【点我回到目录】**](#ml)
### <span id="head33">9. 动态添加组件</span>
>根据用户的操作动态添加组件，比如删除此条动态，添加新的动态，我们都不能事先把组件准备好，因为不知道用户会发多少条动态。  
* 创建一个新的activity，在布局文件中添加一个布局管理器并设置好id
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E5%8A%A8%E6%80%81%E6%B7%BB%E5%8A%A0%E7%BB%84%E4%BB%B6.png)
* 转到代码界面，我们以动态添加按钮组件为例
>代码
```java
LinearLayout layout = findViewById(R.id.g_l);//创建一个相对布局管理器与布局文件对接（此处用了线性布局管理器，根据对应的布局管理器创建）
Button ccdl = new Button(this);//创建一个按钮组件
//wyj.setTextSize(TypedValue.COMPLEX_UNIT_SP,24);//设置文本字体大小
ccdl.setTextColor(Color.rgb(43, 43, 43));//设置文本颜色
ccdl.setText("用神是怎么得来的？");//设置按钮显示文字
layout.addView(ccdl);//把该按钮组件添加到布局管理器中
```
* 这样就实现了动态添加组件，我们可以根据需要依葫芦画瓢灵活运用
>>>>>>[**【点我回到目录】**](#ml)
### <span id="head34">10. 布局界面内容超过界面添加滚动条</span>
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/gif/%E6%B7%BB%E5%8A%A0%E6%BB%9A%E5%8A%A8%E6%9D%A1.gif)
* 只需要在相应的布局界面的布局管理器外添加
>代码
```java
<ScrollView xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
android:overScrollMode="ifContentScrolls">
...
</ScrollView>
```
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%B7%BB%E5%8A%A0%E6%BB%9A%E5%8A%A8%E6%9D%A1.png)
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E6%B7%BB%E5%8A%A0%E6%BB%9A%E5%8A%A8%E6%9D%A11.png)
* 包裹住布局管理器的代码
>>>>>>[**【点我回到目录】**](#ml)
## <span id="head35">（五） 其他</span>
### <span id="head36">1. 素材下载</span>
>这里提供了个下载图标素材的网站，可自定义颜色等  

* [下载素材网址](https://icons8.cn/icon/123415/%E6%90%9C%E7%B4%A2%E6%9B%B4%E5%A4%9A)

* 下载好的素材图片我们需要放到res-drawable文件夹下才能调用
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E7%B4%A0%E6%9D%90%E4%B8%8B%E8%BD%BD.png)
* 只需要找到图片名称即可调用图片
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E7%B4%A0%E6%9D%90%E4%B8%8B%E8%BD%BD1.png)
![Image](https://github.com/syfswxs/AndroidStudioStudy/blob/master/image/%E7%B4%A0%E6%9D%90%E4%B8%8B%E8%BD%BD2.png)
>>>>>>[**【点我回到目录】**](#ml)
