# CSS学习总结
>学了有一小段时间前端了，今做个CSS的总结！

## 目录：
* CSS 简介
* CSS 语法
* CSS 引入方式
* CSS 选择器
* CSS 背景
* CSS 文本样式
* CSS 字体样式
* CSS 链接
* CSS 需注意的问题

## CSS简介
>详情见[CSS入门基础总结](CSS入门基础总结.md)

    * CSS 指层叠样式表 (Cascading Style Sheets)
    * 样式定义如何显示 HTML 元素
    * 样式通常存储在样式表中
    * 把样式添加到 HTML 4.0 中，是为了解决内容与表现分离的问题
    * 外部样式表可以极大提高工作效率
    * 外部样式表通常存储在 CSS 文件中
    * 多个样式定义可层叠为一

## CSS语法

	* CSS 规则由两个主要的部分构成：选择器，以及一条或多条声明:
	
![](http://upload-images.jianshu.io/upload_images/1599190-a5a51e1c106ff549.gif?imageMogr2/auto-orient/strip)

##### CSS 注释
	 * 注释是用来解释你的代码，并且可以随意编辑它，浏览器会忽略它。
	 * CSS注释以 "/*" 开始, 以 "*/" 结束。
		
	
## CSS引入方式

>插入样式表的方法有三种:

* 外部样式表(External style sheet)
 ```
	<head>
	<link rel="stylesheet" type="text/css" href="mystyle.css">
	</head>
```
* 内部样式表(Internal style sheet)
```
	<head>
	<style>
	hr {color:sienna;}
	p {margin-left:20px;}
	body {background-image:url("images/back40.gif");}
	</style>
	</head>
```
* 内联样式(Inline style)	
```	
	<p style="color:sienna;margin-left:20px">这是一个段落。</p>
```
* 多重样式优先级
> * (内联样式）Inline style > （内部样式）Internal style sheet >（外部样式）External style sheet > 浏览器默认样式
 * 注意：如果外部样式放在内部样式的后面，则外部样式将覆盖内部样式。


## CSS选择器
> [传送门](CSS选择器.md)


## CSS 背景

CSS 背景属性用于定义HTML元素的背景。
* CSS 属性定义背景效果:

   *  background-color
```
    十六进制 - 如："#ff0000"
    RGB - 如："rgb(255,0,0)"
    颜色名称 - 如："red"
```
   * background-image
```
 body {background-image:url('paper.gif');}
```
   * background-repeat:设置背景图像是否及如何重复
```
    background-repeat:repeat-x;
    background-repeat:repeat-y;
    background-repeat:no-repeat;/如果你不想让图像平铺
```
   * background-attachment:背景图像是否固定或者随着页面的其余部分滚动。
```
 scroll   背景图片随页面的其余部分滚动。这是默认
 fixed    背景图像是固定的
 inherit  指定background-attachment的设置应该从父元素继承
```
   * background-position
```
  background-position:right top;
```  

## CSS文本样式
> [传送门](CSS文本样式总结.md)

## CSS字体样式
 >[传送门](CSS字体样式总结.md)

## CSS 链接
* 链接的样式，可以用任何CSS属性（如颜色，字体，背景等）。
特别的链接，可以有不同的样式，这取决于他们是什么状态。
这四个链接状态是：
```
    a:link - 正常，未访问过的链接
    a:visited - 用户已访问过的链接
    a:hover - 当用户鼠标放在链接上时
    a:active - 链接被点击的那一刻
```
```
a:link {color:#000000;}      /* 未访问链接*/
a:visited {color:#00FF00;}  /* 已访问链接 */
a:hover {color:#FF00FF;}  /* 鼠标移动到链接上 */
a:active {color:#0000FF;}  /* 鼠标点击时 */
当设置为若干链路状态的样式，也有一些顺序规则：
a:hover 必须跟在 a:link 和 a:visited后面
a:active 必须跟在 a:hover后面
```
* 文本修饰：text-decoration 属性主要用于删除链接中的下划线
* 背景颜色：背景颜色属性指定链接背景色
* 字体颜色：字体颜色属性color

## CSS盒子模型
> [传送门](CSS-盒子模型.md)



## CSS 需注意的问题
> [传送门](CSS需注意的问题.md)
