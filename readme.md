.container 类用于固定宽度并支持响应式布局的容器。
    所谓固定宽度并不是允许开发者自己设置容器的宽度，而是bootstrap内部根据屏幕宽度利用媒体查询，帮我们设置了固定宽度，并且是能够自适应的。
    所以，无论何种情况下，请不要手动为响应式布局中的外层布局容器设置固定宽度值。



.container-fluid 类用于 100% 宽度，占据全部视口（viewport）的容器。
    .container-fluid自动设置为外层视窗的100%，如果外层视窗为body，那么它将全屏显示，
    无论屏幕大小，并且自动实现响应式布局。

全称是 screen reader only，意为：（仅供）屏幕阅读器，这个 class 主要用于增强 accessbility（可访问性）。
有时候 UI 
上会出现一些仅供视觉识别的元素，比如说“汉堡包菜单按钮”，只有视力正常的人才能清楚辨识这些元素的作用。而残障人士，比如弱势或盲人是不可能知道这些
视觉识别元素是什么的。他们上网使用的是屏幕阅读器，也就是 screen 
reader（sr），屏幕阅读器需要找到能辨识的文本说明然后“读”出来给用户听。问题是图形元素怎么可能“读出来”呢？因此我们还要写上这些元素的文
本说明，但是又不需要展示给普通用户看到，于是加上 sr-only 的意义就在于能保证屏幕阅读器正确读取且不会影响 UI 的视觉呈现。


    在html5中，任何以data-开始的都是自定义属性，通常它用来实现一些HTML里没有明确定义的元素，把用户自定义的属性应用到代码中。

       早期的HTML是不允许这种定义，但由于浏览器都不识别这种定义，最终会无视它的存在；相反，jQuery文件就能识别和读取。
       如今，Html5的出现使得data-定义越来越常见，国内外主流媒体的网站代码都会看到它。




       响应式的导航栏
为了给导航栏添加响应式特性，您要折叠的内容必须包裹在带有 class .collapse、.navbar-collapse 的 <div> 中。
折叠起来的导航栏实际上是一个带有 class .navbar-toggle 及两个 data- 元素的按钮。
第一个是 data-toggle，用于告诉 JavaScript 需要对按钮做什么，
第二个是 data-target，指示要切换到哪一个元素。三个带有 class .icon-bar 的 <span> 创建所谓的汉堡按钮。
这些会切换为 .nav-collapse <div> 中的元素。
为了实现以上这些功能，您必须包含 Bootstrap 折叠（Collapse）插件。




默认的导航栏
创建一个默认的导航栏的步骤如下：
向 <nav> 标签添加 class .navbar、.navbar-default。
向上面的元素添加 role="navigation"，有助于增加可访问性。
向 <div> 元素添加一个标题 class .navbar-header，内部包含了带有 class navbar-brand 的 <a> 元素。这会让文本看起来更大一号。
为了向导航栏添加链接，只需要简单地添加带有 class .nav、.navbar-nav 的无序列表即可。


aria-expanded表示展开状态。默认为undefined, 表示当前展开状态未知。其它可选值：true表示元素是展开的；false表示元素不是展开的。
aria-hidden字符串。可选值为true和false,true表示元素隐藏(不可见)，false表示元素可见。

垂直或基本表单
基本的表单结构是 Bootstrap 自带的，个别的表单控件自动接收一些全局样式。下面列出了创建基本表单的步骤：
向父 <form> 元素添加 role="form"。
把标签和控件放在一个带有 class .form-group 的 <div> 中。这是获取最佳间距所必需的。
向所有的文本元素 <input>、<textarea> 和 <select> 添加 class ="form-control" 。