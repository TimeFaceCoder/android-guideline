
# 尺寸


在时光流影Android客户端的dimen文件中存在如下内容


    <dimen name="view_space_small">4dp</dimen>
    <dimen name="view_space_normal">8dp</dimen>
    <dimen name="view_space_medium">16dp</dimen>
    <dimen name="view_space_large">32dp</dimen>
    <dimen name="view_space_xlarge">64dp</dimen>

    <dimen name="size_80">80dp</dimen>
    <dimen name="size_72">72dp</dimen>
    <dimen name="size_56">56dp</dimen>
    <dimen name="size_48">48dp</dimen>
    <dimen name="size_36">36dp</dimen>
    <dimen name="size_24">24dp</dimen>
    <dimen name="size_12">12dp</dimen>

    <dimen name="text_large">22sp</dimen>
    <dimen name="text_medium">18sp</dimen>
    <dimen name="text_normal">16sp</dimen>
    <dimen name="text_small">14sp</dimen>
    


### view_space_XXXX

表示组件padding或者margin的间距。
如果存在UI设计出特殊间距，则直接在xml文件中设置。



### size_XX

客户端不建议使用组件的padding或者margin值来撑起来View的宽度或者高度，而是使用直接设置```size_XX```的形式写死View的高度或者宽度。

注意，如果写死了宽度或者高度，则组件中的文字大小应该设置成为```dp```


### text_XXXX

该属性已经通过自定义的theme直接设置到```textAppearanceSmall```，```textAppearanceMedium```，```textAppearanceLarge```，```textAppearance```，在使用过程中，只要从Widgets中拖出```Large Text```，```Medium Text```，```Small Text```，就可以直接使用这些字号。