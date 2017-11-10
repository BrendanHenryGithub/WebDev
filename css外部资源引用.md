# css中引用CDN资源(字体,图标,框架)

## font-awesome的引用
1. 下载font-awesome包,提取出fonts文件夹,和匹配的css文件.按如下结构接入项目文件夹:

        css/
            font-awesome.min.css
            ...
        fonts/
            ...
        ...

2. 查阅font-awesome使用具体图标即可:
>[font-awesome](http://fontawesome.io/icons/)


## google字体的引用
引用示例:
        
        直接在css文件中添加以下代码:
        @import url("https://fonts.googleapis.com/css?family=Poppins:300,400,500,600,700"); 
