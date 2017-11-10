# html标签摘要

## meta标签
>[参考博客1](https://segmentfault.com/a/1190000004279791)
>[参考博客](http://www.w3cplus.com/css/meta-tags-html-basics-best-practices.html)

## 块级标签与行内标签分类:
>默认情况下行内元素不会新起一行而块级元素会新起一行
1. 块级标签:<h1-h6> <p> <ul> <hr> <table> <form>
2. 行内元素:<a> <button> <img> <input> <label> <b> <i>

## 布局标签
![html5新增的布局标签](https://dn-anything-about-doc.qbox.me/md04171522012052410554136.gif)

		<section>
>定义文档中的节。它用来表现普通的文档内容或应用区块，但section元素标签并非一个普通的容器元素，它表示一段专题性的内容，一般会带有标题。     

<br>

		<article>
>特殊的section标签，它比section具有更明确的语义，它代表一个独立的、完整的相关内容块。当我们描述一件具体的事物的时候，通常鼓励使用article来代替section。
article会有标题部分（通常包含在header内），也可以包含footer。
article可以嵌套，内层的article对外层的article标签有隶属关系。


<br>

		<nav>

>可以作为页面导航的链接组，其中的导航元素链接到其它页面或者当前页面的其它部分，使html代码在语义化方面更加精确，同时对于屏幕阅读器等设备的支持也更好。

<br>

		<aside>

>aside标签用来装载非正文的内容，被视为页面里面一个单独的部分。它包含的内容与页面的主要内容是分开的，可以被删除，而不会影响到网页的内容、章节或是页面所要传达的信息。例如广告，成组的链接，侧边栏等等。

<br>


		<header>

>header标签定义文档的页眉，通常是一些引导和导航信息。它不局限于写在网页头部，也可以写在网页内容里面。
通常header标签至少包含一个标题标记（h1-h6），还可以包括hgroup标签，还可以包括表格内容、标识、搜索表单、nav导航等。

<br>

		<footer>

>footer标签定义section或document的页脚，包含了与页面、文章或是部分内容有关的信息，比如说文章的作者或者日期。 它和header标签使用基本一样，可以在一个页面中多次使用，如果在一个区段的后面加入footer，那么它就相当于该区段的页脚了。

<br>

		<hgroup>

>hgroup标签是对网页或区段section的标题元素（h1-h6）进行组合。例如，在一区段中你有连续的h系列的标签元素，则可以用hgroup将他们括起来。

<br>

		<figure>

>用于对元素进行组合。多用于图片与图片描述组合。

