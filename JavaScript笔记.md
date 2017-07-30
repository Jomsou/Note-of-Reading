# JavaScript学习笔记

>今天开始了《廖雪峰老师JavaScript、Python、git教程》的学习。一些知识点需要做一些笔记，谨记之。

## JavaScript的简介

> * avaScript是世界上最流行的脚本语言，因为你在电脑、手机、平板上浏览的所有的网页，以及无数基<br>于HTML5的手机App，交互逻辑都是由JavaScript驱动的。简单地说，JavaScript是一种运行在浏览器<br>中的解释型的编程语言。
> * 那么问题来了，为什么我们要学JavaScript？简单粗暴的回答就是：因为你没有选择。在Web世界里，<br>只有JavaScript能跨平台、跨浏览器驱动网页，与用户交互。


<i>**随着HTML5在PC和移动端越来越流行，JavaScript变得更加重要了。并且，新兴的Node.js把JavaScript引入到了服务器端，JavaScript已经变成了全能型选手。**</i>
### 错误的看法
JavaScript一度被认为是一种玩具编程语言，它有很多缺陷，所以不被大多数后端开发人员所重视。很多人认为，写JavaScript代码很简单，并且JavaScript只是为了在网页上添加一点交互和动画效果。<br>
<i>**但这是完全错误的理解。JavaScript确实很容易上手，但其精髓却不为大多数开发人员所熟知。编写高质量的JavaScript代码更是难上加难。**</i>

### JavaScript历史
在上个世纪的1995年，当时的网景公司正凭借其Navigator浏览器成为Web时代开启时最著名的第一代互联网公司。<br/>
由于网景公司希望能在静态HTML页面上添加一些动态效果，于是叫Brendan Eich这哥们在两周之内设计出了JavaScript语言。

### ECMAScript
因为网景开发了JavaScript，一年后微软又模仿JavaScript开发了JScript，为了让JavaScript成为全球标准，几个公司联合ECMA（European Computer Manufacturers Association）组织定制了JavaScript语言的标准，被称为ECMAScript标准。<br>
<i>**不过大多数时候，我们还是用JavaScript这个词。如果你遇到ECMAScript这个词，简单把它替换为JavaScript就行了。**</i>
### JavaScript版本
**由于浏览器在发布时就确定了JavaScript的版本，加上很多用户还在使用IE6这种古老的浏览器，这就导致你在写JavaScript的时候，要照顾一下老用户，不能一上来就用最新的ES6标准写，否则，老用户的浏览器是无法运行新版本的JavaScript代码的。**

## JavaScript引入方式

第一，JavaScript代码可以直接嵌在网页的任何地方，不过通常我们都把JavaScript代码放到head、body、元素里面。<script type="text/javascript">...</script><br>
第二，把JavaScript代码放到一个单独的.js文件，然后在HTML中通过<script src="..."></script>引入这个文件。

```
<!DOCTYPE html>
<html>
<head>
  <script src="/static/js/abc.js"></script>
</head>
<body>
  ...
</body>
</html>
```

**注意**：这样，/static/js/abc.js就会被浏览器执行。<br>
把JavaScript代码放入一个单独的.js文件中更利于维护代码，并且多个页面可以各自引用同一份.js文件。<br>
可以在同一个页面中引入多个.js文件，还可以在页面中多次编写<script src="..."></script>，浏览器按照顺序依次执行。

## 调试

**按住F12，调出Chrome的Developer Tools**
>* 先点击“控制台(Console)“，在这个面板里可以直接输入JavaScript代码，按回车后执行。<br>
>* 要查看一个变量的内容，在Console中输入console.log(a);，回车后显示的值就是变量的内容。<br>
>* 关闭Console请点击右上角的“×”按钮。请熟练掌握Console的使用方法，在编写JavaScript代码时，<br>经常需要在Console运行测试代码。
>* 可以研究开发者工具的“源码(Sources)”，掌握断点、单步执行等高级调试技巧


# 基本语法

## 语法

<i>**JavaScript的语法和Java语言类似，每个语句以;结束，语句块用{...}。但是，JavaScript并不强制要求在每个语句的结尾加;，浏览器中负责执行JavaScript代码的引擎会自动在每个语句的结尾补上;。**</i>

>注意：让JavaScript引擎自动加分号在某些情况下会改变程序的语义，导致运行结果与期望不一致。

## 注释
>* // 这是一行注释
>* 另一种块注释是用/*...*/把多行字符包裹起来，把一大“块”视为一个注释。

## 大小写

> 请注意，JavaScript严格区分大小写，如果弄错了大小写，程序将报错或者运行不正常。

# 数据类型和变量

## 数据类型

| 数据类型 | 说明 | 注意 |
| :------- | :----: | :--- |
| Number |JavaScript不区分整数和浮点数，统一用Number表示|NaN; // NaN表示Not a Number，当无法计算结果时用NaN表示<br>Infinity; // Infinity表示无限大，当数值超过了JavaScript的Number所能表示的最大值时，就表示为Infinity    |
| 字符串 |字符串是以单引号'或双引号"括起来的任意文本|'或""本身只是一种表示方式，不是字符串的一部分，因此，字符串'abc'只有a，b，c这3个字符|
| 布尔值 | true和false | &&运算是与运算<br>运算是或运算<br>!运算是非运算,单目运算符|
|比较运算符|==和===|==比较，自动转换数据类型再比较，很多时候，会得到非常诡异的结果；<br>===比较，它不会自动转换数据类型，如果数据类型不一致，返回false，如果一致，再比较。<br>因此，不要使用==比较，始终坚持使用===比较。<br>*NaN === NaN; // false<br>唯一能判断NaN的方法是通过isNaN()函数：isNaN(NaN); // true*<br>最后要注意浮点数的相等比较：1 / 3 === (1 - 2 / 3); // false<br>这不是JavaScript的设计缺陷。浮点数在运算过程中会产生误差，因为计算机无法精确表示无限循环小数。要比较两个浮点数是否相等，只能计算它们之差的绝对值，看是否小于某个阈值：Math.abs(1 / 3 - (1 - 2 / 3)) < 0.0000001; // true
|null和undefined|null表示一个“空”的值，它和0以及空字符串''不同，0是一个数值，'  '表示长度为0的字符串，而null表示“空”。在其他语言中，也有类似JavaScript的null的表示。<br>例如Java也用null，Swift用nil，Python用None表示。但是，在JavaScript中，还有一个和null类似的undefined，它表示“未定义”。|JavaScript的设计者希望用null表示一个空的值，而undefined表示值未定义。事实证明，这并没有什么卵用，区分两者的意义不大。<br>大多数情况下，我们都应该用null。undefined仅仅在判断函数参数是否传递的情况下有用。

## 数组

>数组是一组按顺序排列的集合，集合的每个值称为元素。JavaScript的数组可以包括任意数据类型。

例如：

[1, 2, 3.14, 'Hello', null, true];
上述数组包含6个元素。数组用[]表示，元素之间用,分隔。

另一种创建数组的方法是通过Array()函数实现：
new Array(1, 2, 3); // 创建了数组[1, 2, 3]
*然而，出于代码的可读性考虑，强烈建议直接使用[]。*

数组的元素可以通过索引来访问。请注意，索引的起始值为0：

var arr = [1, 2, 3.14, 'Hello', null, true];
arr[0]; // 返回索引为0的元素，即1
arr[5]; // 返回索引为5的元素，即true
arr[6]; // 索引超出了范围，返回undefined

## 对象

>javaScript的对象是一组由键-值组成的无序集合.

例如：

var person = {
    name: 'Bob',
    age: 20,
    tags: ['js', 'web', 'mobile'],
    city: 'Beijing',
    hasCar: true,
    zipcode: null
};
JavaScript对象的键都是字符串类型，值可以是任意数据类型。上述person对象一共定义了6个键值对，其中每个键又称为对象的属性，例如，person的name属性为'Bob'，zipcode属性为null。

要获取一个对象的属性，我们用对象变量.属性名的方式：

person.name; // 'Bob'
person.zipcode; // null
变量
变量不仅可以是数字，还可以是任意数据类型。
变量在JavaScript中就是用一个变量名表示，变量名是大小写英文、数字、$和_的组合，且不能用数字开头。变量名也不能是JavaScript的关键字，如if、while等。申明一个变量用var语句，比如：

var a; // 申明了变量a，此时a的值为undefined
var $b = 1; // 申明了变量$b，同时给$b赋值，此时$b的值为1
var s_007 = '007'; // s_007是一个字符串
var Answer = true; // Answer是一个布尔值true
var t = null; // t的值是null
同一个变量可以反复赋值，而且可以是不同类型的变量，但是要注意只能用var申明一次，例如：

var a = 123; // a的值是整数123
a = 'ABC'; // a变为字符串
这种变量本身类型不固定的语言称之为动态语言，与之对应的是静态语言。静态语言在定义变量时必须指定变量类型，如果赋值的时候类型不匹配，就会报错。例如Java是静态语言，赋值语句如下：

int a = 123; // a是整数类型变量，类型用int申明
a = "ABC"; // 错误：不能把字符串赋给整型变量
和静态语言相比，动态语言更灵活，就是这个原因。

请不要把赋值语句的等号等同于数学的等号。
strict模式

JavaScript在设计之初，为了方便初学者学习，并不强制要求用var申明变量。这个设计错误带来了严重的后果：如果一个变量没有通过var申明就被使用，那么该变量就自动被申明为全局变量：

i = 10; // i现在是全局变量
在同一个页面的不同的JavaScript文件中，如果都不用var申明，恰好都使用了变量i，将造成变量i互相影响，产生难以调试的错误结果。

使用var申明的变量则不是全局变量，它的范围被限制在该变量被申明的函数体内（函数的概念将稍后讲解），同名变量在不同的函数体内互不冲突。

为了修补JavaScript这一严重设计缺陷，ECMA在后续规范中推出了strict模式，在strict模式下运行的JavaScript代码，强制通过var申明变量，未使用var申明变量就使用的，将导致运行错误。

启用strict模式的方法是在JavaScript代码的第一行写上：

'use strict';
这是一个字符串，不支持strict模式的浏览器会把它当做一个字符串语句执行，支持strict模式的浏览器将开启strict模式运行JavaScript。

来测试一下你的浏览器是否能支持strict模式：
'use strict';
// 如果浏览器支持strict模式，
// 下面的代码将报ReferenceError错误:

abc = 'Hello, world';
alert(abc);
运行代码，如果浏览器报错，请修复后再运行。如果浏览器不报错，说明你的浏览器太古老了，需要尽快升级。

不用var申明的变量会被视为全局变量，为了避免这一缺陷，所有的JavaScript代码都应该使用strict模式。我们在后面编写的JavaScript代码将全部采用strict模式。