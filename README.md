# zhuanpan

> A Vue.js project

## Vue H5 转盘

> 因为在给公司做H5的嵌套页，现在忙完了一些，有一些时间可以学习新东西

> 一直觉得C3动画是我做前端最难搞的东西，空了下来学习了一下网上的做法，也是为以后做的时候能了解原理

> 图片和思路都是在看的一位大神的博客，学习而来。

``` bash
# HTML 思路
我对于自己布局方面还是没有问题的，正常的布局方式。
但是在写完后会出现转盘和转盘按钮一起旋转的问题，发现之后觉得自己比较蠢- -，正确的思路应该是一个BOX包着一个转盘，加按钮。
让转盘转，我之前的思路是把转盘包着按钮。

# CSS 思路
因为是转盘，奖品信息的布局V-FOR出来以后，必须要将它们旋转角度，呈现转盘效果。


# JS 思路
首先要设置初始旋转角度和将要旋转的角度和旋转的时间
其次设置最终旋转的角度，和要旋转在哪,那一个data的下标，和我想要让他多转几圈
点击转动：var 旋转的结果 = 初始旋转角度*我要让她多转几圈*360*最终旋转的角度[data的下标] - 初始旋转角度 * 360;
初始旋转角度 = 旋转的结果
将要旋转的角度 = "rotate(" + 旋转的结果 + "deg)"

```
> 有一个坑没明白：V-FOR 出来的数据，添加样式nth:child()想让每一个数据的样式不同，但是第一个竟然从nth:child(3)开始添加，我就搞不懂了。我的解决方法在v-for的上面在包一个DIV- -

