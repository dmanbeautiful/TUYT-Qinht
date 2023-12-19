#### 复习html

适用于计算机编程代码的标签: code,kbd,tt,samp,var,**pre(预格式文本)**

```html
<html>

<body>

<abbr title="etcetera">etc.</abbr>
<br />
<acronym title="World Wide Web">WWW</acronym>

<p>在某些浏览器中，当您把鼠标移至缩略词语上时，title 可用于展示表达的完整版本。</p>

<p>仅对于 IE 5 中的 acronym 元素有效。</p>

<p>对于 Netscape 6.2 中的 abbr 和 acronym 元素都有效。</p>

</body>
</html>

```

文字可以实现向左向右输出，标签 abo

```html
<a href="#c4">查看</a>
实现在文本内部的跳转
<a name="c4">mmmm</a>
```

```html
<a href="mailto:someone@microsoft.com?subject=Hello%20again">发送邮件</a> 发送邮件
```

```html
<button type="button"
onclick="document.getElementById('demo').innerHTML = Date()">
点击我来显示日期和时间
</button>

<p id="demo"></p>
```

Safari 需要 -webkit- 前缀（请参见下面的实例）。您还必须至少指定 `top`、`right`、`bottom` 或 `left` 之一，以便粘性定位起作用————粘性位置

```html
div.sticky {
  position: -webkit-sticky; /* Safari */
  position: sticky;
  top: 0;
  background-color: green;
  border: 2px solid #4CAF50;
}
```

在此例中，在到达其滚动位置时，sticky 元素将停留在页面顶部（`top: 0`）。

clip 对照片元素进行剪切

注意，在使用相对定位时，无论是否进行移动，元素仍然占据原来的空间。因此，移动元素会导致它覆盖其它框。

通过把两个类选择器链接在一起，仅可以选择*同时包含这些类名*的元素（类名的顺序不限）。

如果一个多类选择器包含类名列表中没有的一个类名，匹配就会失败。请看下面的规则：

```html
.important.urgent {background:silver;}
```

不出所料，这个选择器将只匹配 class 属性中包含词 important 和 urgent 的 p 元素。因此，如果一个 p 元素的 class 属性中只有词 important 和 warning，将不能匹配。不过，它能匹配以下元素：

```html
<p class="important urgent warning">
This paragraph is a very important and urgent warning.
</p>
```

```
* {
  box-sizing: border-box;
}
```

使用后使边框不会因为padding而扩大导致盒子被破坏[CSS Box Sizing (w3school.com.cn)](https://www.w3school.com.cn/css/css3_box-sizing.asp)

如需居中图像，请将左右外边距设置为 `auto`，并将其设置为块元素：

```html
margin-left: auto;
margin-right: auto;
```

**注意：**`a:hover` 必须在 CSS 定义中的 `a:link` 和 `a:visited` 之后，才能生效！`a:active` 必须在 CSS 定义中的 `a:hover` 之后才能生效！伪类名称对大小写不敏感。

实现鼠标悬浮显示内容

```html
p {
  display: none;
  background-color: yellow;
  padding: 20px;
}

div:hover p {
  display: block;
}
</style>
</head>
<body>

<div>鼠标移到我上面来显示 p 元素
  <p>哈哈！我在这里！</p>
</div>
```

#### 下拉菜单

`.dropdown` 类使用 `position:relative`，当我们希望将下拉内容放置在下拉按钮的正下方（使用 `position:absolute`）时，需要使用该类。

`.dropdown-content` 类保存实际的下拉菜单内容。默认情况下它是隐藏的，并将在悬停时显示（请看下文）。请注意，`min-width` 设置为 160px。可随时更改此设置。提示：如果您希望下拉内容的宽度与下拉按钮的宽度一样，请将宽度设置为 100％（设置 `overflow:auto` 可实现在小屏幕上滚动）。

我们用了 CSS `box-shadow` 属性，而不是边框，这样下拉菜单看起来像一张“卡片”。

当用户将鼠标移到下拉按钮上时，`:hover` 选择器用于显示下拉菜单。

主要通过display:none和block来实现显示与否

对于父盒子首先要设置为相对定位和行内块

实现下拉的盒子基本设置

```html
box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
z-index: 1;
```

target="_blank在新的窗口打开超链接

placeholder在input的输入框中显示你想提示的文字

```html
 <input type="text" name="search" placeholder="Search..">
```

resize: none可以禁用2输入框右下角的抓取器
