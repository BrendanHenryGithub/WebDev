# sass的使用
>[sass官网](http://sass-lang.com/documentation/file.SASS_REFERENCE.html)
>[sass高级语法](https://manlili.github.io/2016/03/30/SASS%E9%AB%98%E7%BA%A7%E8%AF%AD%E6%B3%95/)

## 0. sass安装
0.1 Ubuntu下先apt安装ruby,ruby-dev
0.2 sudo gem install sass
0.3 使用示例 sass --watch main.scss:main.css //自动编译并跟踪目标文件.

## 1. 嵌套格式

        #main p {
            color: #00ff00;
            width: 97%;

            .redbox {   //省略main前缀
                background-color: #ff0000;
                color: #000000;
            }
        }

        .funky {    
            font: {   //省略font属性名前缀
                family: fantasy;
                size: 30em;
                weight: bold;
            }
        }
## 2. 变量的使用

        $width: 5em;
        //You can then refer to them in properties:
        #main {
            width: $width;
        }
## 3. 函数式调用

## 4. 利用&指代父选择器

        a {
            font-weight: bold;
            text-decoration: none;
            &:hover { text-decoration: underline; }  //快速添加伪类效果
            body.firefox & { font-weight: normal; }  
        }