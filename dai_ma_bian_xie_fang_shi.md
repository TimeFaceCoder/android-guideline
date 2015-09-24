# 代码编写方式

1. 代码中所有关联view的操作全部由butterknife的InjectView来处理（AS中使用butterknife插件来一键导入）
2. 所有Activity必须继承相关的BaseActivity或者BaseAppCompatActivity

两个基础类已经实现EventBus的注册、NetWork取消事件的监听、页面级TAG参数输出和页面统计相关功能


3. 所有Fragment必须继承相关BaseFragment

该基础页面已经实现EventBus的注册、NetWork取消事件的监听、页面级TAG参数输出和ButterKnife的解绑操作

4. 通用Adapter集成BaseListAdapter
5. 事件处理集成eventbus组件，在代码中需要实现IEventBus接口
6. 网络请求集成sgr组件，在代码中需要实现INetWork接口
7. 每一个Activity都需要一个open或者open4Result的静态方法，用于统一打开activity的参数，例如

```
public static void openForResult(Context context, CircleLocationItem selectedItem, int requestCode) {
    Intent intent = new Intent(context, CircleLocationActivity.class);
    intent.putExtra("selectedItem", selectedItem);
    ((Activity) context).startActivityForResult(intent, requestCode);
}
```

8. View的onClick处理

    * 如果在Activity页面上的View，直接使用对应xml文件中的view的onclick属性。
    * 如果在fragment页面上的view，则在对应的fragment.java文件中使用butterknife的OnClick批注进行处理
    * 如果在adapter页面上的view，使用XML中onclick属性处理的同时，使用view.setTag(key, value)的方式把该view的扩展信息设置进去。
    例如
```
viewHolder.mDynamicContentContentTv.setTag(R.string.tag_index, index);
viewHolder.mDynamicContentImageIv.setTag(R.string.tag_obj, item);
viewHolder.mDynamicContentImageIv.setTag(R.string.tag_ex, "time");
```
