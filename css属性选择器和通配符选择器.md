[css属性选择器和通配符选择器](https://blog.csdn.net/haha_hello/article/details/54971063)
https://blog.csdn.net/haha_hello/article/details/54971063

### 一，属性选择器1
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>20-css属性选择器上.html</title>
    <!--
        属性选择器,根据指定的属性名称找到对应的标签,设置属性
        1,格式:
        [attribute] 
        作用:根据指定的属性名称找到对应的标签,设置属性
        [attribute=value] 
        作用:找到指定属性,并且属性的取值是value的标签,设置属性
        最常见的场景就是,区分input标签的属性
        input[type=password]{}
        <input type="text" id="">
        <input type="password" id="">
        <input type="radio" id="">
        <input type="checkbox" id="">
    -->
    <style>
        /*p[id]{
            color: red;
        }*/
        p[class=pp]{
            color: aqua;
        }
    </style>
</head>
<body>
<p id="=id1">我是段落1</p>
<p id="=id2" class="cc">我是段落2</p>
<p class="cc">我是段落3</p>
<p id="=id3">我是段落4</p>
<p class="pp">我是段落4</p>
</body>
</html>
```

### 二，属性选择器2
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>21-css属性选择器下.html</title>
    <!--
        1,属性的取值是以什么开头的
        [attribute|=value] css2 了解
        [attribute^=value] css3
        2,属性的取值是以什么结尾的
        [attribute$=value] css3
        3,属性的取值是否包含某个特定的值的
        [attribute~=value] css2 了解
        [attribute*=value] css3
    -->
    <style>
        /*img[alt^=abc]{
            color: red;
        }*/
        img[alt|=abc]{
            color: red;
        }
        img[alt$=abc]{
            color: aqua;
        }
        img[alt*=abc]{
            color: green;
        }
    </style>
</head>
<body>

<!--<img src="" alt="abcdef">-->
<!--<img src="" alt="abc-www">-->
<!--<img src="" alt="abc qqq">-->
<!--<img src="" alt="defabc">-->
<!--<img src="" alt="ppp abc">-->
<!--<img src="" alt="www-abc">-->
<!--<img src="" alt="qq">-->
<!--<img src="" alt="yy">-->
<img src="" alt="wwwabcwww">
<img src="" alt="www-abc www">
<img src="" alt="www abc www">
<img src="" alt="qq">
</body>
</html>
```

### 三，通配符选择器
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>22-css通配符选择器.html</title>
    <!--
        通配符选择器,给当前所有的标签设置属性
        1,格式:
        *{
            属性:值;  
          }
         2,注意:界面标签不能过多,性能就会比较差
    -->
    <style>
        *{
            color: red;
        }
    </style>
</head>
<body>
<h1>我是标题</h1>
<p>我是段落</p>
<a href="#">我是超链接</a>
```