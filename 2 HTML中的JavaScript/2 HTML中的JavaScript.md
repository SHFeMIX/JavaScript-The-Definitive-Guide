### 本章内容：
* 使用\<script>元素
* 行内脚本与外部脚本比较
* 稳当模式对JavaScript有什么影响
* 确保JavaScript不可用时的用户体验

### 小结
JavaScript是通过\<script>元素插入页面中的。这个元素可用于把JavaScript代码嵌入HTML页面中，跟其他标签混合在一起，也可以用于引入保存在外部文件中的JavaScript，本章重点可以总结如下：
* 要包含外部JavaScript文案，必须将src属性设置为要包含的URL。文案可以跟网页在同一台服务器上，也可以位于完全不同的域。
* 所有script元素会依照他们在网页中出现的次序被解释。在不使用defer合async属性的情况下，包含在script元素中的代码必须严格按照次序解释。
* 对不推迟执行的脚本，浏览器必须解释完位于script元素中的代码，然后才能继续渲染页面的剩余部分。为此，通常应该把script元素放到页面末尾，介于主内容以及body元素的关闭标签之前。
* 可以使用defer属性把脚本推迟到文档渲染完毕之后再执行。推迟脚本原则上按照它们被列出的次序执行。
* 可以使用async属性表示脚本不需要等待其他脚本，同时也不阻塞文档渲染吧，即异步加载。异步脚本不能保证按照它们在页面中出现的次序执行。
* 通过使用noscript元素，可以指定在浏览器不支持脚本时显示的内容。如果浏览器支持并启用脚本，则noscript元素中的任何内容都不会被渲染。