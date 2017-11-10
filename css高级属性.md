# css的实用高级属性

## 0. css属性说明专用语法
>[MDN参考](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Value_definition_syntax)

## 1. 设置过渡效果:transition
e.g.设置背景颜色渐变.    

        /* property name | duration */
        transition: background-color 4s;

## 2. 背景浮动效果:background-attachment
>[MDN参考](https://developer.mozilla.org/zh-CN/docs/Web/CSS/background-attachment)
e.g.设置背景图片的相对浮动效果:

        background-attachment: fixed;

## 3. 利用:before伪元素给图片覆盖透明模板
e.g. 

        ::before{
            content: "";  //必须添加这个属性不然浏览器不会渲染
            position: absolute;  //用于将透明滤镜定位于目标区域上
            top:0px;
            background-color: rgba($color: black, $alpha: 0.75);
            width: 100%;     //设置成完全覆盖
            height: 100%;
            z-index: 1;         //置于目标区域上方
        }