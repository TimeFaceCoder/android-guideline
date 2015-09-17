
# 命名


基本原则为骆驼法则，即首字母大写，命名需要准确描述类或者方法的作用




## 类及方法


首字母大写
添加准确后/前缀
* XXXXXXXXActivity   用于表示为Activity页面
* XXXXXXXXAdapter	用于表示为Adapter
* BaseXXXXXXXXX		用于表示某相基础类
* XXXXXXXXXDialog	用于表示Dialog
* XXXXXXXXXEvent		用于表示某种事件
* XXXXXXXXXFragment	用于表示Fragment页面
* IXXXXXXXXX			表示为Interface类
* XXXXXXXXXListener	表示为事件监听类
* XXXXXXXXXReceiver	表示事件接收类
* XXXXXXXXXService	表示服务
* XXXXXXXXXTask		表示Android Task
* XXXXXXXXXRunnable	表示为线程
* XXXXXXXXXFactory	表示为工厂类
* XXXXXXXXXUtils		表示为工具类
* XXXXXXXXXView		表示为自定义视图
* XXXXXXXXX+Android基本组件名，例如TextView，FrameLayout	表示为自定义组件
* XXXXXXXXXResponse	用于Gson直接解析过来的网络请求数据形成的对象
* XXXXXXXXXItem		用于Gson解析过来XXXXXXResponse对象中包含List的item对象
* XXXXXXXXXObj		表示基础对象，和网络请求无关
* 其他				同一类型页面或者功能前缀需一样

方法名首字母必须小写，其他符合骆驼法则







## 资源命名


*	activity_XXXXXX		某Activity页面对应xml文件
*	fragment_XXXXXXXXX	Fragment页面对应xml文件
*	item_XXXXXXXXX	Adapter类中描述某行item的xml文件
*	header_XXXXXXXXX	listView中header的xml文件
*	footer_XXXXXXXXX	listView中footer的xml文件
*	menu_XXXXXXXXX	menu描述文件
*	view_XXXXXXXXX	自定义view的描述文件
*	anim_XXXXXXXXX	动画
*	ic_XXXXXXXXX		图标
*	bg_XXXXXXXXX		背景图
*	selector_XXXXXXXXX	selector文件
*	shape_XXXXXXXXX	shape文件
*	anim_XXXXXXXXX	anim文件







