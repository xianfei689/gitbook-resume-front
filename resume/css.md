---
description: CSS
---

# CSS

### 1、 Q: CSS 属性是否区分大小写？

```css
 ul {
     MaRGin: 10px;
 }
```

解析： 

`不区分。 HTML，CSS都对大小写不敏感，但为了更好的可读性和团队协作一般都小写，而在XHTML 中元素名称和属性是必须小写的。`

###  2、Q: 行内\(inline\)元素 设置`margin-top`和`margin-bottom` 是否起作用？

解析：

* 块级元素（ block）     如&lt;div&gt;&lt;p&gt;
* 内联元素（行内元素、inline ）     如&lt;span&gt;&lt;img&gt;

    what is ?

 ``**`将展现宏观的元素设置成块（相对宏大） 将修饰细节的东西设置成行内元素（相对细微）。`**`例如：<div>元素就是作为容器出道的，他肯定就是块级元素。而<strong>这些修饰个别文字的样式，就是内联元素。`

      区别：

![](../.gitbook/assets/image%20%281%29.png)

1. 块级元素会独占一行（无法与其他元素显示在同一行内），而内联元素会在一行内显示
2. 块级元素可以设置widht、height属性，而内联元素设置无效。
3. 块级元素的width默认为100%，而内联元素则是根据自身的内容或者是子元素决定宽度。

* 延伸拓展：

 Question: 行内元素是否默认以**空格进行分割？**

```markup
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>Document</title>
        <style>
            *{
                padding:0px;
                margin:0px;
            }
           .inline{
                border:1px solid #ccc;
            }
            .block{
                
                border:1px solid #ccc;
            }

        </style>
    </head>
    <body>
            <span class="inline">hello</span> <span class="inline">world</span>
            <div class="block">
                    hello world
                </div>
            <span class="inline">hello</span><span class="inline">world</span>
    </body>
</html>
```

效果：

![](../.gitbook/assets/image%20%284%29.png)

![](../.gitbook/assets/image%20%283%29.png)

由图可知：  内联元素之间**不会默认以空格进行分割**，当**代码中有空格**间隔开那么，内联元素会有一个空格间隔。

