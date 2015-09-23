# 三方框架

项目中引入大量第三方框架，整理如下


com.android.support:design
--------------------------
略

com.android.support:support-v4
-------
略

com.android.support:appcompat-v7
-------
略

com.android.support:recyclerview-v7
-------
略

com.android.support:cardview-v7
-------
略

com.michaelpardo:activeandroid
-------
[Activeandroid](https://github.com/pardom/ActiveAndroid)
主要用于项目中数据库的ORM

de.greenrobot:eventbus
-------
[EventBus](https://github.com/greenrobot/EventBus)
主要用于实现各个页面间数据同步等等事件发送

com.squareup.okhttp:okhttp
-------
[OkHttp](https://github.com/square/okhttp)
替换系统HttpClient。某些组件也基于okhttp，例如alioss，volley，picasso，glide等


com.github.chrisbanes.photoview
-------
[PhotoView](https://github.com/chrisbanes/PhotoView)
用于实现图片缩放和拖放功能


com.facebook.rebound:rebound
-------
[Rebound](https://github.com/facebook/rebound)
用于实现某些View的弹簧动画

com.github.rayboot.svr:svr
-------
[SVR](https://github.com/rayboot/SimpleVolleyRequest)
使用该框架作为数据级网络请求的框架，该框架使用Volley作为底层网络请求，并且集成了请求撤销功能

com.jakewharton:butterknife
-------
[ButterKnife](https://github.com/JakeWharton/butterknife)
使用该框架注入某些代码，例如findId等等
该框架可以配合[android-butterknife-zelezny](https://github.com/avast/android-butterknife-zelezny) 插件使用，可以快速导入所有页面id

com.bluelinelabs:logansquare
-------
[LoganSquare](https://github.com/bluelinelabs/LoganSquare)
用于解析网络请求返回的json string 转为数据对象的框架
解析效率优于Gson，使用方法见框架简介


io.reactivex:rxjava
-------
[RxJava](https://github.com/ReactiveX/RxJava)
项目已集成Rxjava和lambda表达式的框架，编写某些代码可以直接使用RxJava的方式


com.github.bumptech.glide
--------------------------
[Glide](https://github.com/bumptech/glide)
图片显示框架

timeface-common
--------------------------
我们提出的一些公共工具，用于和开发的其他app共享使用


cn.timeface.tfoss:filemanager
--------------------------
[TFOSS](https://github.com/TimeFaceCoder/TFOSS)
时光流影配合阿里云OSS服务的文件管理框架
主要用于上传文件和下载文件

com.github.rayboot.widget:ratioview
--------------------------
[RatioView](https://github.com/rayboot/RatioView)
按比例缩放View的组件


ALiImageSDK
--------------------------
[ALiImageSDK](https://github.com/rayboot/ALiImageSDK)
用于对阿里云图片的url进行变换的框架



cn.timeface.widget:drawabletextview
--------------------------
[drawabletextview](https://github.com/TimeFaceCoder/TFWidget)
用于完善图片+文字位置的组件