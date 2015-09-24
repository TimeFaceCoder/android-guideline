
# 列表


使用RecyclerView，若要实现下拉刷新和上拉加载更多需要配合TFPTRRecyclerViewHelper，BaseRecyclerAdapter，SwipeRefreshLayout,IPTRRecyclerListener的使用


# 布局文件
    
    <android.support.v4.widget.SwipeRefreshLayout
        android:id="@+id/ptr_layout"
        android:layout_width="match_parent"
        android:layout_height="match_parent">

        <android.support.v7.widget.RecyclerView
            android:id="@+id/pull_refresh_list"
            android:layout_width="match_parent"
            android:layout_height="match_parent"/>
    </android.support.v4.widget.SwipeRefreshLayout>


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
  

FPTRRecyclerViewHelper.Mode.BOTH


    