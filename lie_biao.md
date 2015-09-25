
# 列表


使用RecyclerView，若要实现下拉刷新和上拉加载更多需要配合TFPTRRecyclerViewHelper，BaseRecyclerAdapter，SwipeRefreshLayout,IPTRRecyclerListener的使用


# 布局文件
```    
    <android.support.v4.widget.SwipeRefreshLayout
        android:id="@+id/ptr_layout"
        android:layout_width="match_parent"
        android:layout_height="match_parent">

        <android.support.v7.widget.RecyclerView
            android:id="@+id/pull_refresh_list"
            android:layout_width="match_parent"
            android:layout_height="match_parent"/>
    </android.support.v4.widget.SwipeRefreshLayout>```


# 初始化

    private void initPull2Refresh() {
        // 初始化回调事件
        ptrListener = new IPTRRecyclerListener() {
            @Override
            public void onTFPullDownToRefresh(View refreshView) {
                // do下拉刷新
            }

            @Override
            public void onTFPullUpToRefresh(View refreshView) {
                // do上拉加载更多
            }
            @Override
            public void onScrollUp(int firstVisibleItem) {
                // 列表正在向上滑
            }

            @Override
            public void onScrollDown(int firstVisibleItem) {
                // 列表正在向下滑
            }
        };
        // 初始化TFPTRRecyclerViewHelper，用来控制recyclerview的各个状态
        tfptrListViewHelper =
                new TFPTRRecyclerViewHelper(getActivity(), mPullRefreshList,
                        mPtrLayout).setTFPTRMode(TFPTRRecyclerViewHelper.Mode.BOTH)
                        .tfPtrListener(ptrListener);
    }
    
    
# 控制下拉刷新和上拉加载更多
  使用tfptrListViewHelper.setTFPTRMode(TFPTRRecyclerViewHelper.Mode.BOTH)来控制加载方式
  

- TFPTRRecyclerViewHelper.Mode.BOTH  下拉刷新和上拉加载更多
- TFPTRRecyclerViewHelper.Mode.START 只能下拉刷新
- TFPTRRecyclerViewHelper.Mode.END   只能上拉加载更多
- TFPTRRecyclerViewHelper.Mode.DISABLE 不能下拉刷新和上拉加载更多


# 添加heeader和footer
  由于recyclerview本身是没有addHeader和addFooter方法，所以在BaseRecyclerAdapter中封装了添加header和footer方法。使用时要注意是通过adapter调用addHeader和addFooter来添加。
  
  
# 添加recyclerview滑动时的加载动画
- 继承BaseRecyclerAdapter并实现getAnimators()方法返回Animator[]
- RvAnimatorUtil工具类中定义了一些简单的动画，也可以在该工具中自行添加所需要的动画效果





    