# CSS伪类和伪元素

>CSS伪类和伪元素是用来添加一些选择器的特殊效果。


## 伪类的语法：

selector:pseudo-class {property:value;}

#### CSS类也可以使用伪类：

selector.class:pseudo-class {property:value;}

## 伪元素的语法：

selector:pseudo-element {property:value;}

#### CSS类也可以使用伪元素：

selector.class:pseudo-element {property:value;}

--------------------------------------------------------------------------------

## 所有CSS伪类/元素
|选择器|示例|示例说明|
|:----|:----|:---|
|:checked|input:checked|选择所有选中的表单元素 
:disabled input:disabled 选择所有禁用的表单元素 
:empty p:empty 选择所有没有子元素的p元素 
:enabled input:enabled 选择所有启用的表单元素 
:first-of-type p:first-of-type 选择每个父元素是p元素的第一个p子元素 
:in-range input:in-range 选择元素指定范围内的值 
:invalid input:invalid 选择所有无效的元素 
:last-child p:last-child 选择所有p元素的最后一个子元素 
:last-of-type p:last-of-type 选择每个p元素是其母元素的最后一个p元素 
:not(selector) :not(p) 选择所有p以外的元素 
:nth-child(n) p:nth-child(2) 选择所有p元素的第二个子元素 
:nth-last-child(n) p:nth-last-child(2) 选择所有p元素倒数的第二个子元素 
:nth-last-of-type(n) p:nth-last-of-type(2) 选择所有p元素倒数的第二个为p的子元素 
:nth-of-type(n) p:nth-of-type(2) 选择所有p元素第二个为p的子元素 
:only-of-type p:only-of-type 选择所有仅有一个子元素为p的元素 
:only-child p:only-child 选择所有仅有一个子元素的p元素 
:optional input:optional 选择没有"required"的元素属性 
:out-of-range input:out-of-range 选择指定范围以外的值的元素属性 
:read-only input:read-only 选择只读属性的元素属性 
:read-write input:read-write 选择没有只读属性的元素属性 
:required input:required 选择有"required"属性指定的元素属性 
:root root 选择文档的根元素 
:target #news:target 选择当前活动#news元素(点击URL包含锚的名字) 
:valid input:valid 选择所有有效值的属性 
:link a:link 选择所有未访问链接 
:visited a:visited 选择所有访问过的链接 
:active a:active 选择正在活动链接 
:hover a:hover 把鼠标放在链接上的状态 
:focus input:focus 选择元素输入后具有焦点 
:first-letter p:first-letter 选择每个<p> 元素的第一个字母 
:first-line p:first-line 选择每个<p> 元素的第一行 
:first-child p:first-child 选择器匹配属于任意元素的第一个子元素的 <]p> 元素 
:before p:before 在每个<p>元素之前插入内容 
:after p:after 在每个<p>元素之后插入内容 
:lang(language) p:lang(it) 为<p>元素的lang属性选择一个开始值 
