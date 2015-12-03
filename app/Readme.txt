GeoQuiz

1.activity是Android SDK中Activity类的一个实例，负责管理用户与屏幕的交互；
APP的功能是通过编写一个个Acitivity子类来实现的，简单的应用可能只有一个子类，而复杂的APP则会有多个子类；

2.layout定义了一系列用户界面对象以及他们在屏幕上显示的位置。保存在XML文件中。每个定义用来创建屏幕上的一个组件。

在这里，MainActivity管理着content_main.xml文件定义的用户界面。

3.输入包名的时候需要遵循“DNS反转”约定，亦即将企业组织或公司的域名反转后，在尾部加上应用名称。遵循此约定可以保证包名的唯一性。
比如，我的公司域名是leotse90.com，开发的APP叫做geoquiz，那么这里的包名就是：
com.leotse90.geoquiz

4.这里的layout－content_main.xml文件中，有两个组件：RelativeLayout和TextView。
组件是组成用户界面的构造模块。组件可以显示文字或者图像，与用户进行交互，甚至是布置屏幕上的其他组件。
Android中的每一个组件都是View类或者其子类（TextView或者Button等）。

5.元素的名称就是组件的类型，各元素均有一组XML属性，属性可以看作是如何配置组件的指令。

6.在这个APP的布局文件中，作为根元素，LinearLayout组件必须指定Android XML资源文件的命名空间属性为http://schemas.android.com/apk/res/android
LinearLayout组件继承自View子类的ViewGroup组件，ViewGroup组件是一个包含并配置其他组件的特殊组件。

7.match_parent：视图与其父视图大小相同；（以前还有一个fill_parent属性值，等同于match_parent，目前已经废弃）
  wrap_content：视图将根据其内容自动调整大小。
  android:padding="24dp"，该属性告诉组件在决定大小时，除内容本身外，还需要额外增加指定量的空间。
  dp即density-independent pixel。
  android:orientation属性：决定了子组件的放置方式，有两种，垂直或者水平。
  android:text属性：指定组件显示的文字内容。

8.activity子类的实例创建以后，onCreate(Bundle)方法将会被调用。activity创建后，它需要获取并管理属于自己的用户界面。
获取activity的用户界面，可以调用以下Activity方法setContentView(int layoutResID)，通过传入布局的资源ID参数，该方法
声称指定的布局的视图并将其放置在屏幕上。

9.布局是一种资源，资源是应用非代码形式的内容，比如图像文件、音频文件或者XML文件等。
项目的所有资源文件都存在res的子目录下。

10.R.java文件在Android项目编译过程中自动生成，遵照该文件头部的警示，不要尝试修改文件内容。
我们在指定Button组件的id时，使用+id标志，说明我们将要创建资源ID，而字符串@string表示只是做了引用。

11.Android应用属于典型的事件驱动类型。事件驱动型应用启动后，即开始等待行为事件的发生。
为响应某个事件而创建的对象叫做监听器（Listener）。
建议：监听器最好使用匿名内部类来实现，优点如下：
    1）在大量的代码块中，监听器方法的实现一目了然；
    2）匿名内部类的使用只出现在一个地方，因此可以减少一些命名类的使用。

12.为了让.apk应用能在模拟器上运行，.apk文件必须以debug key签名，分发.apk应用给用户时，必须以release key签名。