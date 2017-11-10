# css选择器摘要
>参考博客[css选择器](http://www.w3cplus.com/css/advanced-html-css-lesson3-complex-selectors.html)
>[MDN伪类和伪元素选择器](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Introduction_to_CSS/Pseudo-classes_and_pseudo-elements)

## 1. 选择器的优先权:
1.1 style属性中设置的:1000
1.2 通过id选择器选中的:100
1.3 通过类选择器,属性选择器,伪类选择器(带一个冒号):10
1.4 通过元素选择器选中的,伪元素选择器(带两个冒号):1
1.5 同优先级的后设置的会高于先设置的

## 2. 申明的覆盖先后顺序:
2.1 相互冲突的申明按以下顺序适用,后一种将会覆盖前一种:

		在用户代理样式表的声明 (例如：浏览器在没有其他声明的默认样式).
		用户样式表中的常规声明（由用户设置的自定义样式）。
		作者样式表中的正常声明（这是我们设置的样式，Web开发人员）。
		作者样式表中的重要声明
		用户样式表中的重要声明
2.3 !important可以让一条规则总是优先于其他规则

## 3.常用的伪类选择器:
3.1 :first-child :last-child	eg:  ul li:first-child  选中ul后代里的li元素,而且这个li必须是ul后代里排第一的.

3.2 :nth-child() :nth-last-child()	eg:  .third span:nth-of-type(2n+1)   选中third类后代里的span元素,而且这个span元素必须是third类里后代排第2n+1的n从0开始取
3.3 :nth-of-type() :nth-of-last-type()

