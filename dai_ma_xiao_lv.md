# 代码效率


为提升代码执行效率，在开发或者测试阶段进行如下代码审核。

* 使用```SparesArray```替换使用```Map<Integer, Object>```
* 注意for循环执行层次以及优化嵌套层次
* 使用```/>```进行闭环操作
* 多用```tools```的属性例如```tools:text``` ```tools:listitem```
* 利用drawableXXX属性来做有图文的控件，特别是类似设置页面中文字在左右边有剪头的View
* 






## Lint

项目送测后，使用lint进行代码检测

![lint使用方法](https://git.gitbook.com/raw/timeface/android-guideline/master/lint.png?token=dGltZWZhY2UtYXBwOjBmOWQ4NDBiLTJhOGQtNDJhZC1hMzJmLWQxNjEzODc2NzQ2Zg%3D%3D)


## 页面重绘问题

![开启方法](https://git.gitbook.com/raw/timeface/android-guideline/master/open_overdraw.png?token=dGltZWZhY2UtYXBwOjBmOWQ4NDBiLTJhOGQtNDJhZC1hMzJmLWQxNjEzODc2NzQ2Zg%3D%3D)

[详见内训资料](https://git.gitbook.com/raw/timeface/android-guideline/master/android_overdraw.pptx?token=dGltZWZhY2UtYXBwOjBmOWQ4NDBiLTJhOGQtNDJhZC1hMzJmLWQxNjEzODc2NzQ2Zg%3D%3D)


## GPU使用频次
![开启方法](https://git.gitbook.com/raw/timeface/android-guideline/master/open_gpu_test.png?token=dGltZWZhY2UtYXBwOjBmOWQ4NDBiLTJhOGQtNDJhZC1hMzJmLWQxNjEzODc2NzQ2Zg%3D%3D)



## 内存泄露

* 使用LeakCanary进行内存泄露检测

* 对于handler泄露可以自行创建一个handler模板
，具体如下

![第一步](https://git.gitbook.com/raw/timeface/android-guideline/master/template1.png?token=dGltZWZhY2UtYXBwOjBmOWQ4NDBiLTJhOGQtNDJhZC1hMzJmLWQxNjEzODc2NzQ2Zg%3D%3D)

![第二步](https://git.gitbook.com/raw/timeface/android-guideline/master/template2.png?token=dGltZWZhY2UtYXBwOjBmOWQ4NDBiLTJhOGQtNDJhZC1hMzJmLWQxNjEzODc2NzQ2Zg%3D%3D)

然后在代码中直接输入myhandler可得到一个避免handler引起泄露的代码片段


