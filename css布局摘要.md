#  css布局摘要
## css框模型
>[参考资料w3c](http://www.w3school.com.cn/css/css_boxmodel.asp)  
>[参考资料简书](http://www.jianshu.com/p/fa1dc9629eee)    
>[参考资料实验楼](https://www.shiyanlou.com/courses/53/labs/252/document)
>[参考资料MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/box-sizing)
1. 在响应式布局中一般建议将所有的盒模型都设置为border-box;即:box-sizing:border-box
2. 为方便布局弱化元素之间的影响一般还设置全局属性:  margin: 0;


![框模型](http://upload-images.jianshu.io/upload_images/838624-cdfc00cf77982a0a.gif?imageMogr2/auto-orient/strip)

### margin padding 边距设置：
- 如果提供全部四个参数值，将按上、右、下、左的顺序作用于四边。
- 如果只提供一个，将用于全部的四边。
- 如果提供两个，第一个用于上、下，第二个用于左、右。
- margin 垂直方向会出现重叠现象,但水平方向不会出现。
eg:  margin: 10px 5px 10px 5px;

### display属性:
>[MDN参考](https://developer.mozilla.org/zh-CN/docs/Web/CSS/display)
1. display CSS属性指定用于元素的呈现框的类型。
2. 除了多种不同的生成的元素的盒类型，值 none 可以关闭一个元素的显示；当你使用 none 所有的后代元素他们的显示也会被关闭。


## css元素的定位与重叠
>[参考资料带实例演示](http://zh.learnlayout.com/position.html)
1. css的position属性：static，absolute，fixed，relative。

## css文本垂直水平对齐居中
1. text-align: The text-align CSS property describes how inline content like text is aligned in its parent block element. text-align does not control the alignment of block elements, only their inline content.
2. text-align-last: 对齐最后一行
3. text-justify: The text-justify CSS property defines what type of justification should be applied to text when it is justified (i.e., when text-align: justify; is set on it).
4. vertical-align: The vertical-align CSS property specifies the vertical alignment of an inline or table-cell box.Note that vertical-align only applies to inline and table-cell elements: you can't use it to vertically align block level elements.
5. justify-content: The CSS justify-content property defines how the browser distributes space between and around content items along the main axis(横轴) of their container.
6. align-content: The CSS align-content property defines how the browser distributes space between and around content items along the cross-axis(竖轴) of their container, which is serving as a flexible box container.
7. align-item: CSS align-items 属性以与justify-content相同的方式在侧轴方向上将当前行上的弹性元素对齐。与align-content属性的区别在于它指定了当前Flex容器的行中的项目的对齐方式，而align-content则指定了行自身的对齐方式。
8. align-selfs: CSS 属性 align-self 会对齐当前 flex 行中的 flex 元素，并覆盖 align-items 的值. 如果任何 flex 元素的侧轴方向 margin 值设置为 auto，则会忽略 align-self。
9. 单行元素设置其整体居中时只需要margin: 0 auto;

## css网格布局
>[mdn参考资料](https://developer.mozilla.org/en-US/docs/Web/CSS/grid)
>[css Tickets](https://css-tricks.com/snippets/css/complete-guide-grid/)

grid: repeat(2,350px) / auto-flow 50%;  #repeat中的2代表重复2次,此处就相当于设置两行,后面的50%意味着每行分成两列,每列占宽50%


## Flex layout 
1. To use flex layout, you should use this in the parent div:

        display:flex
        # you can also use inline-flex;

2. Terminology:
    - main axis : The main axis is the axis running in the direction the flex items are being laid out in.
    - cross axis : The cross axis is the axis running perpendicular to the direction the flex items are being laid out in. 
    - flex container : The parent element that has display: flex set on it is called the flex container.
    - flex items : The items being laid out as flexible boxes inside the flex container are called flex items.

3. Change the main axis:

        flex-direction: column
        # by default this is set to row.

4. Wrapping:

        # when you have a fixed amount of width or height in your layout is that eventually your flexbox children will overflow their container, breaking the layout. You can use this:
        flex-wrap: wrap

        # You can use flex-wrap to change both direction and wrap
        flex-flow: row wrap

5. Flex shortcut:    
>flex is a shorthand property that can specify up to three different values:    
- flex-grow : The unitless proportion value that dictates how much of the available space along the main axis each flex item will take up. 
- flex-shrink : This specifies how much of the overflowing amount is taken away from each flex item's size, to stop them overflowing their container. 
- flex-basis :  The minimum size value inside the flex value.    
- Most time we just use flex-grow and flex-basis.

## flex alignment
1. Horizontal alignment (main axis alignment):   
>justify-content controls where the flex items sit on the main axis. It define in the flex container    
- flex-start : The default value is flex-start, which makes all the items sit at the start of the main axis.
- flex-end : sit at the end.
- space-around :  It distributes all the items evenly along the main axis, with a bit of space left at either end.
- space-between : It is very similar to space-around except that it doesn't have any space at either end.

2. Vertical alignment (cross axis alignment):
>align-items controls where the flex items sit on the cross axis. It define in the flex container. And you can overwrite it for individual flex items by applying the align-self property to them.    
- stretch : If the parent hasn't got a fixed width in the cross axis direction, then all flex items will become as long as the longest flex items. 
- center : The center value that we used in our above code causes the items to maintain their intrinsic dimensions, but be centered along the cross axis. 
- flex-start : align all items at the start.
- flex-end : align all items at the end.