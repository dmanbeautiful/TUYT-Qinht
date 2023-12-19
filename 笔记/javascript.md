# javascript

alert消息对话框(包含一个确定按钮)

![image-20231202115911507](https://damn-meili.oss-cn-beijing.aliyuncs.com/image-20231202115911507.png)

```
var message = confirm("")
```

prompt 点击确定按钮，文本框中的内容将作为函数返回值；取消则返回 null

```html
prompt(str1,str2);
str1: 要显示在消息对话框中的文本，不可修改
str2：文本框中的内容，可以修改
```

window.open打开新窗口

**语法：**

```html
window.open([URL], [窗口名称], [参数字符串])
```

**参数说明:**

```
URL：可选参数，在窗口中要显示网页的网址或路径。如果省略这个参数，或者它的值是空字符串，那么窗口就不显示任何文档。
窗口名称：可选参数，被打开窗口的名称。
    1.该名称由字母、数字和下划线字符组成。
    2."_top"、"_blank"、"_self"具有特殊意义的名称。
       _blank：在新窗口显示目标网页
       _self：在当前窗口显示目标网页
       _top：框架网页中在上部窗口中显示目标网页
    3.相同 name 的窗口只能创建一个，要想创建多个窗口则 name 不能相同。
   4.name 不能包含有空格。
参数字符串：可选参数，设置窗口参数，各参数用逗号隔开。
```

![img](https://damn-meili.oss-cn-beijing.aliyuncs.com/52e3677900013d6a05020261.jpg)

window.close关闭窗口

**用法：**

```
window.close();   //关闭本窗口
```

或

```
<窗口对象>.close();   //关闭指定的窗口
```

例如:关闭新建的窗口。

```
<script type="text/javascript">
   var mywin=window.open('http://www.imooc.com'); //将新打的窗口对象，存储在变量mywin中
   mywin.close();
</script>
```

**注意:上面代码在打开新窗口的同时，关闭该窗口，看不到被打开的窗口。**

## DOW

**HTML文档可以说由节点构成的集合，三种常见的DOM节点:**

**1. 元素节点：**上图中<html>、<body>、<p>等都是元素节点，即标签。

**2. 文本节点:**向用户展示的内容，如<li>...</li>中的JavaScript、DOM、CSS等文本。

**3. 属性节点:**元素属性，如<a>标签的链接属性href="http://www.imooc.com"。**窗口的同时，关闭该窗口，看不到被打开的窗口。**

### innerHTML属性

innerHTML 属性用于获取或替换 HTML 元素的内容。

**语法:**

```
Object.innerHTML
```

**注意:**

1.Object是获取的元素对象，如通过document.getElementById("ID")获取的元素。

2.注意书写，innerHTML区分大小写。

### 修改HTMl样式

**语法:**

```
Object.style.property=new style;
```

**注意:**Object是获取的元素对象，如通过document.getElementById("id")获取的元素。

**基本属性表（property）:**

**[![img](https://damn-meili.oss-cn-beijing.aliyuncs.com/52e4d4240001dd6c04850229.jpg)](https://img1.sycdn.imooc.com//52e4d4240001dd6c04850229.jpg)**

**注意:**该表只是一小部分CSS样式属性，其它样式也可以通过该方法设置和修改。

display:显示与隐藏,要通过document.getElementById("id")去获取元素

**语法：**

```html
Object.style.display = value
```

value: none/block

控制类名className

className 属性设置或返回元素的class 属性。

**语法：**

```
object.className = classname
```

**作用:**

获取元素的class 属性；为网页内的某个元素指定一个css样式来更改该元素的外观

<!DOCTYPE HTML>
<html>
<head>
<meta http-equiv="Content-Type" Content="text/html; charset=utf-8" />
<title>javascript</title>
<style type="text/css">
body{font-size:12px;}
#txt{
    height:400px;
    width:600px;
	border:#333 solid 1px;
	padding:5px;}
p{
	line-height:18px;
	text-indent:2em;}
</style>
</head>
<body>
  <h2 id="con">JavaScript课程</H2>
  <div id="txt"> 
     <h5>JavaScript为网页添加动态效果并实现与用户交互的功能。</h5>
        <p>1. JavaScript入门篇，让不懂JS的你，快速了解JS。</p>
        <p>2. JavaScript进阶篇，让你掌握JS的基础语法、函数、数组、事件、内置对象、BOM浏览器、DOM操作。</p>
        <p>3. 学完以上两门基础课后，在深入学习JavaScript的变量作用域、事件、对象、运动、cookie、正则表达式、ajax等课程。</p>
  </div>
  <form>
  <!--当点击相应按钮，执行相应操作，为按钮添加相应事件-->
    <input type="button" value="改变颜色" onclick="set.changeColor()">  
    <input type="button" value="改变宽高" onclick="set.changeSize()">
    <input type="button" value="隐藏内容" onclick="set.objHide()">
    <input type="button" value="显示内容" onclick="set.objShow()">
    <input type="button" value="取消设置" onclick="set.offSet()">
  </form>
  <script type="text/javascript">
   var txt=document.getElementById("txt");
   var set={
    changeColor:function(){
        txt.style.color="red";
        txt.style.backgroundColor="#ccc";
    },
    changeSize:function(){
        txt.style.width="300px";
        txt.style.height="300px";
    },
    objHide:function(){
        txt.style.display="none";
    },
    objShow:function(){
        txt.style.display="block";
    },
    offSet:function(){
        var message=confirm("你确定要重置所有设置么？");
        if(message==true){
            txt.removeAttribute('style');
        }
    }
  }
  </script>
</body>
</html>

