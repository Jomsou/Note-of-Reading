>学了有一小段时间前端了，今做个CSS的注意点总结！这些都是自己会犯的错误，谨记之。

1.HTML与CSS中字体的颜色属性是color，而不是font-color，没有后者。
2.ID、class属性不要以数字开头，数字开头的ID在 Mozilla/Firefox 浏览器中不起作用。
3.class 和 id 有什么区别
* class是设置标签的类， class属性用于指定元素属于何种样式的类； 2、id是设置标签的标识。id属性用于定义一个元素的独特的样式。
* class是一个样式，class名称可以相同。id是一个标签，用于区分不同的结构和内容，id是先找到结构/内容，再给它定义样式；id的优先级要高于class。
* 单一的元素，或需要程序、JS控制的东西，需要用id定义；重复使用的元素、类别，用class定义。 如果在页面中要对某个对象进行脚本操作（js），那么可以给他定义一个id，否则只能利用遍历页面元素加上指定特定属性来找到它，这是相对浪费时间资源，远远不如一个id来得简单.

4.(内联样式）Inline style > （内部样式）Internal style sheet >（外部样式）External style sheet > 浏览器默认样式
内联样式>ID 选择器>伪类>属性选择器>类选择器>元素(类型)选择器>通用选择器（*）

