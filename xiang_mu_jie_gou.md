# 项目结构


项目使用Gradle框架进行管理
具体java包管理如下

![代码框架](https://git.gitbook.com/raw/timeface/android-guideline/master/图片%201.png?token=dGltZWZhY2UtYXBwOjBmOWQ4NDBiLTJhOGQtNDJhZC1hMzJmLWQxNjEzODc2NzQ2Zg%3D%3D)

按照目录名放置java代码

aar文件放置到根目录aars文件夹中

jar文件放置到根目录libs文件夹中

如有特殊需求不能使用gradle方式引入第三方类库，则第三方类库源码需放置到根目录下third_party目录中，如第三方类库很少修改，则打包称aar文件放置到aars文件夹中，如需经常修改，则已第三方依赖的形式引入

另注：具有独立功能模块的代码，允许自己开发独立lib，已第三方依赖的形式引入。如果独立模块不独立为lib，则可以在对应目录下创建指示明确的文件夹。



activities
-------
放置activity类

adapters
-------
放置RecyclerView 的 Adapter类


bases
-------
放置基础类
包括

 - BaseActivity
	 所有Activity的基础类，单独创建的Activity必须继承该类
 - BaseAppCompatActivity
	 所有AppCompatActivity的基础类，单独创建的AppCompatActivity必须集成该类，该类用于显示类似ActionBarActiity的页面，但是我们项目使用ToolBar实现ActionBar的功能
 - BaseFragment
	 所有Fragment的基础类，单独创建的Fragment必须集成该类
 - BaseListAdapter
	 所有ListAdapter的基础类
	 继承该类可以让你的Adapter专注编写getView方法
 - BaseRecyclerAdapter
	 所有RecyclerAdapter的基础类
	 该类封装了header，footer和Item动画的调用方法。也可配合TFPTRRecyclerViewHelper快速实现列表刷新功能
 - BaseRecyclerViewActivity
	 所有简单列表可以直接继承该类，该类已包含基础的RecyclerView，Toolbar功能

dialogs
-------
放置dialog类


events
-------
放置event类
用于在使用EventBus发送消息时定义的类


fragments
-------
放置fragment类

managers
-------
主要包括listener，receiver，service和task
对应目录放置对应类型

models
-------
放置数据对象
BaseModule--所有对象的基础类，主要实现序列化操作

BaseResponse--所有网络请求相关数据对象的基础类，主要包括网络请求的公共元素

    /**
     * 操作是否成功
     */
    public int status;
    
    /**
     * 操作结果描述
     */
    public String info;
    
    /**
     * 错误编号
     */
    String errorCode;


数据对象名称创建主要已三种形式做为后缀

 - XXXXResponse
		网络请求数据对象的根对象，例如`TimeBookResponse`
		
 - XXXXItem
		网络请求数据对象中，数组对象类型的后缀，例如`TimeBookItem`（`TimeBookResponse`中包含一个`List<TimeBookItem>`）

 - XXXXObj
		其他对象类型，例如`UserObj`


utils
-------
放置工具类

views
-------
自定义view