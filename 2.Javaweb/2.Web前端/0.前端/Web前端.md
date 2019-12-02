

## Web前端概述

HTML是网页的结构，CSS是网页的外观，而JavaScript是页面的行为。

## 1.HTML

 超文本标记语言

学习HTML就是学习各种标签，然后针对你想要的内容来使用相应的标签 

### 1.1 HTML基本骨架



```html
<!DOCTYPE html>   <!-- HTML5文档声明  -->
<html >
    <head>  <!-- 页头  -->
        <meta charset="UTF-8">    <!-- 声明字符集 -->
        <title>Document</title>		<!--导航栏标题 -->
    </head>
    <body>    <!--页身  -->
          <!-- 文档主体 -->
    </body>
</html>
```

html 里面所有的东西 都叫做标签

单标签：<标签名>

双标签：<标签名></标签名>

#### head标签

一般来说，只有6个标签能放在<head>标签内：

① &lt;title>；

	 <title>标签唯一的作用就是定义网页的标题 

②&lt;[meta>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/meta)；

```
<meta>标签又叫“元信息标签”  meta标签有两个重要的属性name和http-equiv。
```

****

```html
<head>    
    <!--网页关键字-->
    <meta  name="keywords" content=""/>
    <!--网页描述-->
    <meta  name="description" content=""/>
    <!--本页作者-->
    <meta  name="author" content="">
    <!--版权声明-->
    <meta  name="copyright" content=""/>
</head>
```

```html
<head>
    <meta  http-equiv="refresh" content="6;url=http:/www.baidu.com"/>
    <!--页面自动跳转-->
    <!--
如果content 只包含一个正整数,则是重新载入页面的时间间隔(秒);
如果content 包含一个正整数并且跟着一个字符串,则是重定向到指定链接的时间间隔(秒)-->
</head>
```

```html
<meta charset="UTF-8">    <!-- 声明字符集 -->
```

③&lt;link>；

 &lt;link>标签用于外部文件的链接，一般用于链接外部CSS样式表文件和JS文件 

```html
<link rel="stylesheet" href="*.css">
```

也可以用来引用网站图标

```html
<link rel="shortcut icon" href="*.ico">
```

④&lt;style>；

 用于定义元素的CSS样式 

```html
<head>
    <style type="text/css">
        <!--这里写CSS样式-->
    </style>
</head>
```

⑤&lt;script>

 用于定义页面的脚本

```html
<head>
    <script type="text/javascript">
    
    </script>
</head>
```

⑥&lt;base>；

定义页面所有链接的基础定位

| &lt;head>内部标签 | 说明                             |
| ----------------- | -------------------------------- |
| &lt;title>        | 定义网页的标题                   |
| &lt;meta>         | 定义网页的基本信息（供搜索引擎） |
| &lt;style>        | 定义CSS样式                      |
| &lt;link>         | 链接外部CSS文件或JS脚本文件      |
| &lt;script>       | 定义脚本语言                     |
| &lt;base>         | 定义页面所有链接的基础定位       |

#### body标签

网页的主体内容都在此标签中书写

#### 注释

```html
<!--说明性文字，用于注释-->
```



### 1.2 常用标签

> &lt;div>  &lt;img> &lt;a> &lt;ul>  &lt;ol> &lt;li>   &lt;p>

```html
<div>70% div</div>
<div>
	写内容就可以了
    大部分的网站都是通过div标签构成
	div + css
	特性就是一行一行的,想到下一行 就再来一个 div 标签就可以了
</div>
```

```html
<img src="">

注：

网页上 除了文字 最多的是啥？
网页就是由 文字 + 图片 + 媒体（音频 + 视频）
<img> 标签 在网页可以让图片显示出来

<img> 不需要闭合
需要让 img标签 和 图片有关联
放入一个 属性src 地址属性可以是网络地址或者本地地址（相对路径、绝对路径）
```

```html
<a href="里面放入要跳转的地址"></a>
跳转标签
<a target='_blank'>原页面不跳转 打开一个新页面</a> 
如果想点击图片进行跳转
就是a标签里面放入img标签即可
target	_blank 新窗口打开 _self 当前窗口打开
title	链接提示文本
href	跳转地址
```

```html
无序列表

<ul>
	<li> li可以有无限个 所有其余的内容放在li里面就可以了<li>
</ul>

正规的写法 ul下面的第一层只能放li 
嵌套实例
<li>
	<a href="http://www.baidu.com"><img src="1.jpg"></a>
</li>
```

```html
有序列表
<ol>
	<li>1111</li>
	<li>3333</li>
</ol>
 注：ol
ol和ul的用法基本一致
ol下面的 第一层 最好是 li
只不过ol的下面 是默认使用数字标注 1 ～ n
```

```html
p 标签

	<p>我是段落。</p>

	<div>我是div</div>
注：一般是段落 或者 新闻 或者特别多的文字 去使用的标签

默认是一行的，而且默认每行的上下的留白会有 比起其他的元素。
```

```html
<div>
		用户名:
		<input type="text">
	</div>
	<div>
		密码:
		<input type="password">

	</div>
	<div>
		选项1
		<input type="checkbox">
		选项2
		<input type="checkbox">
		选项3
		<input type="checkbox">
	</div>

	<div>
		单选：
		<input type="radio">
	</div>
	<div>
		<input type="color">
	</div>

注:input插件的东西

type='input的类型'

text 默认
password 密码
radio 单选
checkbox 复选
color 颜色
```

```html
input 
type='button' 
value='内容'

<input type='button' value='按钮上的文字'>

<button>内容</button>
```

### 1.3 文本相关

> &lt;h1>~&lt;h6> &lt;p>
>
> 

#### 标题标签

```html
<!DOCTYPE html> 
<html>
<head>
    <title>标题标签h1~h6</title>
</head>
<body>
    <h1>这是一级标题</h1>
    <h2>这是二级标题</h2>
    <h3>这是三级标题</h3>
    <h4>这是四级标题</h4>
    <h5>这是五级标题</h5>
    <h6>这是六级标题</h6>
</body>
</html>
```

 用于网页搜索引擎优化，是极其重要的标签 

#### 段落标签

 使用p标签来标记一段文字 ， 段落标签会自动换行，并且段落与段落之间有一定的空隙 

```html
<!DOCTYPE html> 
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>爱莲说</title>
</head>
<body>
    <h3>爱莲说</h3>
    <p>水陆草木之花，可爱者甚蕃。晋陶渊明独爱菊。自李唐来，世人甚爱牡丹。予独爱莲之出淤泥而不染，濯清涟而不妖，中通外直，不蔓不枝，香远益清，亭亭净植，可远观而不可亵玩焉。</p>
    <p>予谓菊，花之隐逸者也；牡丹，花之富贵者也；莲，花之君子者也。噫！菊之爱，陶后鲜有闻；莲之爱，同予者何人? 牡丹之爱，宜乎众矣。</p>
</body>
</html>
```

#### 文本标签

粗体&lt;strong>

```html
<p>这是普通文本</p>
<strong>这是粗体文本</strong>
```

斜体&lt;em>

```html
<em>斜体文本</em>
```

上标&lt;sup>

```html
<p>(a+b)<sup>2</sup>=a<sup>2</sup>+b<sup>2</sup>+2ab</p>
```

下标&lt;sub>

```html
<p>H<sub>2</sub>O指的是水分子</p>
```

删除线，下划线等可以使用CSS实现

#### 换行标签

自定义换行 break缩写 &lt;br>

```html
<!DOCTYPE html> 
<html>
<head>
    <title>换行标签</title>
</head>
<body>
    <h3>静夜思</h3>                  
    <p>床前明月光，疑是地上霜。<br/>举头望明月，低头思故乡。</p>
</body>
</html>
```



#### 水平线标签

&lt;hr>插入一条水平线 horizon（水平线） 

```html
<hr>
```

#### DIV标签

 div，即division（分区），用来划分一个区域。  div标签内可以放入&lt;body>标签的任何内部标签：段落文字、表格、列表、图像等。  使用div标签划分区域的代码更加具有逻辑性 。

```html
<div>

</div>
```

#### 特殊字符

 &amp;   &lt;    &gt;  &nbsp;  &nbsp;  &copy; 

#### 单标签

```
1、<meta/>
定义页面的说明信息，供搜索引擎查看。

2、<link/>
用于连接外部的CSS文件或脚本文件。

3、<base/>
定义页面所有链接的基础定位。

4、<br/>
用于换行。

5、<hr/>
水平线。

6、<input/>
用于定义表单元素

7、<img/>
图像标签。
```



### 1.4 图片和链接

在网页中使用 `img` 标签展示图片，图片的大小、边框、倒角效果使用css处理。

```text
<img src="houdunren.png" alt="后盾人"/>
```

| 属性  | 说明                     |
| ----- | ------------------------ |
| src   | 图片地址                 |
| alt   | 图像打开异常时的替代文本 |
| title | 鼠标悬浮的提示文本       |

```html
<img src="图片地址" alt="图片描述(给搜索引擎看)" title="图片描述(给用户看)">
```

 掌握.jpg、.png和.gif三种图片格式的区别 :

1、JPG可以很好处理大面积色调的图像，如相片、网页一般的图片。

2、PNG格式图片体积小，而且无损压缩，能保证网页的打开速度。最重要的是PNG格式图片支持透明信息。PNG格式图片可以称为“网页设计专用格式”。

3、GIF格式图片图像效果很差，但是可以制作动画。



[链接&lt;a>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/a)不能能过一个页面展示网站的所有功能，需要在不同页面中跳转，这就是链接所起到的功能。

```text
<a href="" target="_blank" title=""></a>
```

| 选项   | 说明                                                |
| ------ | --------------------------------------------------- |
| href   | 跳转地址/邮箱链接mailto:/拨打电话tel:/下载文件*.zip |
| target | _blank 新窗口打开 _self 当前窗口打开                |
| title  | 链接提示文本                                        |

锚点链接

锚点可以设置跳转到页面中的某个部分。

1. 为元素添加`id` 属性来设置锚点

2. 设置 `a` 标签的 `href` 属性

3. ```text
   <a href="#comment-1">跳转到评论区</a>
   <div style="height: 1000px;"></div>
   
   <div id="comment-1" style="background: green;">
   	这是后盾人评论内容区
   </div>
   ```

4. 也可以跳转到不同页面的锚点

   ```text
   <a href="article.html#comment-1">跳转到评论区</a>
   ```

### 1.5 列表

| 标签 | 语义            | 说明     |
| :--- | :-------------- | :------- |
| ol   | ordered list    | 有序列表 |
| ul   | unordered list  | 无序列表 |
| dl   | definition list | 定义列表 |


#### 有序列表

 在该语法中，<ol>和</ol>标志着有序列表的开始和结束，而<li>和</li>标签表示这是一个列表项。在有序列表中可以包含多个列表项 。 注意，<ol>标签和<li>标签是配合使用，没有单独使用，而且<ol>标签内部不能存在任何其他标签，一般情况下只能存在<li>标签

```html
<ol>
    <li>有序列表项</li>
    <li>有序列表项</li>
    <li>有序列表项</li>
</ol>
```

| type属性值 | 列表项的序号类型         |
| :--------- | :----------------------- |
| 1          | 数字1、2、3……            |
| a          | 小写英文字母a、b、c……    |
| A          | 大写英文字母A、B、C……    |
| i          | 小写罗马数字i、ii、iii…… |
| I          | 大写罗马数字I、II、III…… |

 type属性实现的效果可以用CSS的**list-style-type**实现 

#### 无序列表


```html
<ul type="列表项符号">
    <li>无序列表项</li>
    <li>无序列表项</li>
    <li>无序列表项</li>
</ul>
```

| type属性值 | 列表项的序号类型  |
| :--------- | :---------------- |
| disc       | 默认值，实心圆“●” |
| circle     | 空心圆“○”         |
| square     | 实心正方形“■”     |

 学习了CSS之后，无序列表列表项符号由**list-style-type**属性定义，到时候应该摒弃type属性 

#### 自定义列表

```html
<dl>
    <dt>定义名词</dt>
    <dd>定义描述</dd>
    ……
</dl>
```

 说明：<dl>即“definition list（定义列表）”，<dt>即“definition term（定义名词）”，而<dd>即“definition description（定义描述）”。

在该语法中，<dl>标记和</dl>标记分别定义了定义列表的开始和结束，<dt>后面添加要解释的名词，而在<dd>后面则添加该名词的具体解释。 

### 1.6 表单

```html
<form  name="表单名称" action="服务器地址" method="post"></form>
```

#### input

 <input type="表单类型"/> 

  input标签是自闭合标签，因为它没有结束标签。 ![inputæ ç­¾](http://www.lvyestudy.com/App_images/lesson/hj/9-3-0.png) 

```html
<input type="text" value="默认文字" size="文本框长度" maxlength="最多输入字符数"/>
<input type="password" value="默认文字" size="文本框长度" maxlength="最多输入字符数"/>
<input type="radio" name="单选按钮所在的组名" value="单选按钮的取值"/>
<input type="button" value="普通按钮的取值" onclick="JavaScript脚本程序"/>
<input type="submit" value="提交按钮的取值"/>
<input type="reset" value="重置按钮的取值"/>
<input type="image" src="图像的路径"/>
<input type="hidden"/>
<input type="file"/>


<input type="checkbox" value="复选框取值" checked="checked"/>
    <form name="form1" method="post" action="index.html">
        你喜欢的水果：<br />
        <input id="checkbox1" type="checkbox" checked="checked"/><label for="checkbox1">苹果</label><br />
        <input id="checkbox2" type="checkbox" /><label for="checkbox2">香蕉</label><br />
        <input id="checkbox3" type="checkbox" /><label for="checkbox3">西瓜</label><br />
        <input id="checkbox4" type="checkbox" /><label for="checkbox4">凤梨</label>
    </form>
```

#### 多行文本

 多行文本框使用的是textarea标签，而不是input标签。 

```
<textarea rows="行数" cols="列数">多行文本框内容</textarea>
```

> 文本框有3种形式：单行文本框text、密码文本框password和多行文本框textarea。单行文本框和密码文本框使用的是input标签，而多行文本框使用的是textarea标签。 

#### 下拉列表

```html
<select multiple="mutiple" size="可见列表项的数目"> <!--当设置multiple=“multiple”时，下拉列表可以选择多项-->
    <option>选项显示的内容</option>
    ……
    <option>选项显示的内容</option>
</select>
```



### 1.7 表格

> 表格基本标签有：table标签（表格）、tr标签（行）、td标签（单元格）。<tr>标签和<td>标签都要在表格的开始标签<table>和结束标签</table>之间才有效 

| 标签      | 说明             |
| :-------- | :--------------- |
| **table** | 表格             |
| caption   | 标题             |
| thead     | 表头（语义划分） |
| tbody     | 表身（语义划分） |
| tfoot     | 表尾（语义划分） |
| **tr**    | 行               |
| th        | 表头单元格       |
| **td**    | 表格单元格       |

<table>        
        <tr>
            <td>单元格1</td>
            <td>单元格2</td>
        </tr>
        <tr>
            <td>单元格3</td>
            <td>单元格4</td>
        </tr>
    </table>

####  合并行rowspan 

```html
<td rowspan="跨度的行数">
```

####  合并列colspan 

```html
<td colspan="跨度的列数">
```

### 1.8 多媒体

在网页中常见的多媒体文件包括音频文件和视频文件，对于在线音频和视频，我们往往都是使用embed标签来插入。

embed是HTML5新增的标签。

```html
<embed src="多媒体文件地址" width="播放界面的宽度" height="播放界面的高度"/>
```

插入音频

```html
<embed src="media/西班牙舞曲.mp3" width="400px" height="80px"/>
```

插入视频

```html
 <embed src="media/小苹果.wmv" width="400px" height="80px"/>
```

插入Flash

```
<embed src="App_images/lesson/hj/helloworld.swf"/>
```

插入背景音乐

```
<bgsound src="背景音乐的地址"  loop="播放次数"/>
```

> loop="2"表示重复2次，loop="infinite"表示无限次循环播放，也可以使用loop="-1"表示无限次循环播放。 

## 2.CSS

css注释：

```css
/*注释的内容*/
```



### 2.1 CSS引入方式

CSS引入样式主要有三种方式：外部样式，内部样式，内联样式。最常用的是外部样式，根据CSS就近原则,如果属性有相同，则内联样式优先级最高。

#### 外部样式

在head标签中通过link标签引入外部CSS，为了将CSS样式与HTML结构相分离，故常采用外部样式

```html
<link type="text/css" href="" />
```

#### 内部样式

在head标签中通过style标签直接使用CSS

```html
<style>
			
</style>
```

#### 内联样式

在标签中添加style属性

```html
<div style="width: 100px;height: 10px;background: red;"></div>
```

### 2.2 CSS选择器

CSS选择器的格式如下

```css
选择器 {
	属性:属性值;
	属性:属性值;
}
```

选择器有很多种，常用的选择器有如下几种,优先级：id>class>标签选择器

#### 标签选择器

```
标签 {
	属性:属性值;
	属性:属性值;
}
```

这里的选择器指的是常用的标签，标签不需要<,>即可，例如

```css
p{
	width:100px;
	height:100px;
	background:red;
}
```

注：div{} <div></div> 都会触发这个样式，一般用于清除浏览器默认样式

#### 类选择器

可以重复很多个

```html
<div class='abc'></div> 
```

在样式中的选择器写法

```css
.abc{

}
```

#### ID选择器

id选择器唯一的标签,

```html
<div id='abc'></div> 
```

在样式中的选择器写法

```css
#abc{

}
```

#### 后代选择器

```css
ul li{

}
```

```css
.myDiv .myp p{

}
```

注：父标签 空格 子标签

后代选择器 更精准的选择需要的元素

在css中 更精准 权重就更高

#### 群组选择器

```css
div,#id,div a ,div p{}
```

群组选择器 有通用样式 就放在群组选择器中

#### 通配符选择器

```css
*{

}
```

`*`通配符,可以选取所有元素，优先级比较低

#### 伪类选择器

### 2.3 盒子模型

#### [外边距 margin](https://developer.mozilla.org/zh-CN/docs/Web/CSS/margin)

width 宽度
height 高度
background 背景

外边距:当前元素距离外面的边距
4种:right top bottom left

margin  

可以缩写

margin:4个值  上 右 下 左

margin:3个值 上 左右 下

margin:2个值 上下 左右

margin:1个值 上下左右 

margin-left/ margin-right/ margin-bottom/margin-top

```css
margin: style              /*单值语法  所有边缘 */  举例： margin: 1em; 
margin: vertical horizontal /*二值语法  纵向 横向 */  举例： margin: 5% auto; 
margin: top horizontal bottom /*三值语法 上 横向 下*/  举例： margin: 1em auto 2em; 
margin: top right bottom left  /*四值语法 上 右 下 左*/  举例： margin: 2px 1em 0 auto; 

margin: inherit
```

#### [内边距 padding](https://developer.mozilla.org/zh-CN/docs/Web/CSS/padding)

margin - 外边距
padding - 内边距

margin 缩写形式  原来元素的大小不变


padding 原来的元素大小发生了改变

width:200px; height:200px;padding-left:100px;

实际宽度是300像素

width:200px;height:200px;
margin-left:100px;

实际宽度是 200像素

padding:四个参数  上 右 下 左

padding:三个参数 上 左右 下	

padding:二个参数 上下  左右	

padding:一个参数 上下左右



#### [边框 border](https://developer.mozilla.org/zh-CN/docs/Web/CSS/border)

border - 边框 占元素的大小 是往外长的

border - 缩写样式

border : 大小（10px） 实线或者虚线
实线(solid)
虚线(dashed)

颜色(#)(rgb())(red)

非缩写
border-width;
border-color;
border-style;

border-top-width:30px; 
border-right-width:20px;
border-bottom-width:5px;
border-left-width:55px;
border-left-color:red;
border-right-color:green;
border-bottom-color:yellow;
border-top-color:black;
border-left-style:solid;
border-top-style:dashed;
border-right-style:solid;
border-bottom-style:dashed;

border-right
border-top
border-left
border-bottom

#### 浮动 float

最主要的作用可以让元素 横着码

float:left / right

### 2.3 元素分类

所有的html元素
一共可以分成三大类

常用的就两类

**块状元素** 
div 最基本的块状元素

display：block

1.支持宽高 margin、padding
2.width 默认是100% ,独占一行

常见块级元素div h1-h6 p hr ol ul

**行内元素**
span 最基本的行内元素

display：inline

行内元素em strong input img a

1.宽高会随着内容变化而变化
2.支持margin、padding
3.不独占一行

嵌套问题

**块状元素可以随意嵌套**
**行内元素 只可以嵌套行内元素**

行内 - 横着码
块   - 支持宽、高、独占一行
**行内块**（不常用）

行内块元素

display：inline-block 

横着码放 但是不独占一行
支持宽、高

### 2.4 背景 background

background 背景 颜色 重复 位置
缩写样式

background-color:
背景颜色

background-image:url();
背景图片

background-size:
背景图的大小

background-repeat:
背景图平铺

no-repeat 不平铺
repeat-x 横坐标平铺
repeat-y 纵坐标平铺

background-position
背景坐标
放两个参数 第二个参数默认是center
第一个参数是x轴
第二个参数是y轴
支持 right/bottom/left/top/center的写法

### 2.5 字体样式

文字属性

| 属性        | 说明     |
| :---------- | :------- |
| font-family | 字体类型 |
| font-size   | 字体大小 |
| font-weight | 字体粗细 |
| font-style  | 字体斜体 |
| color       | 颜色     |

#### 字体类型

 font-family：字体1,字体2,字体3; 

 font-family可指定多种字体，多个字体将按优先顺序排列，以逗号隔开，注意逗号一定要是英文逗号。 

 默认情况下，浏览器的字体是宋体。中文字体常用的有宋体、微软雅黑，英文字体比较常用的是Times New Roman、Arial。 

#### 字体大小

 font-size：关键字/像素值; 

| font-size属性值 | 说明         |
| :-------------- | :----------- |
| xx-small        | 最小         |
| x-small         | 较小         |
| small           | 小           |
| medium          | 默认值，正常 |
| large           | 大           |
| x-large         | 较大         |
| xx-large        | 最大         |

 这些都是相对浏览器默认情况下而言。对于这些属性值，我们完全不需要记忆，大家一定要记住喔。因为我们在实际开发中，比较少使用这种方式来表达字体大小，一般都是采用像素作为单位的数值 px；

#### 字体粗细

 font-weight:粗细值; 

 粗细值可以取关键字和100~900的数值 

| font-weight属性值 | 说明                         |
| :---------------- | :--------------------------- |
| normal            | 默认值，正常体               |
| lighter           | 较细                         |
| bold              | 较粗                         |
| bolder            | 很粗（其实效果跟bold差不多） |

字体粗细font-weight属性值可以取100、200、…、900这九个值。400相当于正常字体normal，700相当于bold。100~900分别表示字体的粗细，是对字体粗细的一种量化方式，值越大就表示越粗，值越小就表示越细。

对于中文网页来说，一般仅用到**bold**、**normal**这两个属性值完全就可以了，粗细值不建议使用数值（100~900）。

#### 字体斜体

 font-style:取值; 

| font-style属性值 | 说明                                                         |
| :--------------- | :----------------------------------------------------------- |
| normal           | 默认值，正常体                                               |
| italic           | 斜体，这是一个属性                                           |
| oblique          | 将字体倾斜，将没有斜体变量（italic）的特殊字体，要应用oblique |

#### 字体颜色

 color:颜色值; 

颜色表示方式

 1.关键字指的就是颜色的英文名称，如red、blue、green等。 

2. 十六进制#FBF9D0 
3. rgb()

#### 行高

 line-height:像素值; 

 在CSS中，使用line-height属性来控制文本的行高 

如果大小为元素的大小时，内容会在中心

可以控制行内元素，但是控制不了块状元素

#### 英文大小写

 text-transform:属性值; 

| 属性值     | 说明                                             |
| :--------- | :----------------------------------------------- |
| none       | 默认值，无转换发生                               |
| uppercase  | 转换成大写                                       |
| lowercase  | 转换成小写                                       |
| capitalize | 将每个英文单词的首字母转换成大写，其余无转换发生 |

[font](https://developer.mozilla.org/zh-CN/docs/Web/CSS/font)

```css
/* Set the font size to 12px and the line height to 14px.
   Set the font family to sans-serif */
p { font: 12px/14px sans-serif }
```

### 2.6 定位

#### 相对定位

相对自己进行定位

```css
position:relative;

top:像素值;
bottom:像素值;

left:像素值;
right:像素值;
z-index z轴：数字优先级 支持负数
```

left/right      二选一

 top/bottom二选一

相对定位不会影响原来的位置，显示的元素会改变位置



#### 绝对定位



```css
position:absolute;
top:像素值;
bottom:像素值;
left:像素值;
right:像素值;
```

1.脱离标准流
2.原来的位置不会留着
3.绝对定位是根据有定位的父元素进行定位
4.如果父元素没有定位 那么就会找到最外层的元素直到html标签



#### 固定定位

相对定位 - 根据自己进行定位
绝对定位 - 根据有定位的父级去进行定位
窗口定位 - 根据窗口进行定位

**position:fixed** 
只会根据窗口 不看父级定位

有滚动条的话 一直跟着窗口走 
绝对定位不会跟窗口走

应用：广告

#### 继承定位

继承定位 
inherit

继承父级的定位
父级是什么定位 他自己就是什么定位

#### 默认定位

默认值
没有定位
static

子级 inherit -》子级的父级 inherit -》 父级 absolute

### 2.7 显示

#### display

display:none;
让原来的元素进行消失,位置不会进行保留。
display:block;
可以让行内元素变成块状元素的样子

float 也可以把元素变成块状元素

display:inline-block

行内块元素

横着码放 但是不独占一行
支持宽、高

### 2.8 单位

单位 px  绝对单位
百分比 %  相对单位 无法判断是多少像素

百分比 如何计算呢？
看父级元素的 height 50% 就是父级高度的 一半

比如 父级 300px 那么 30% 

300 * 0.3 = 90px

如果是 200%

300 * 2 = 600px
最后会折合成像素进行显示

比如全屏 用px 做不出来
但是用 % 很轻易就可以做出来



































## 3.JavaScript

### 3.1.1 WEB历史

#### JS的发展

1994年	---->      前端历史的起点  HTML+CSS

1995年	---->      JS

1997年	---->     ECMA（欧洲计算机制造联合会）ECMAScript规范化

2009年	---->     

2011年	---->     CSS3

2014年	---->     HTML5，WEB基础趋于稳定

2015年	---->     ECMAScript2015  每年6月一个版本,ES3，ES2015->ES6

**ECMA:规范**	**JS：具体实现**

> 运行环境：浏览器/node.js
>
> HTML结构 	CSS外观· JavaScript行为



#### JS的引入

浏览器中的Js引入，主要有内嵌式以及外链式

内嵌式

> 要求HTML与JS相分离，所以不推荐使用

```html
<script>
 
    
</script>
```

外链式

> 推荐使用

```html
<script src="*.js"></script>
```

示例一

```javascript
    <script>
        //文档输出
        document.write("hello");
        //控制台输出
        console.log("hello");
    </script>
```



### 3.1.2 学习方法

**记笔记！！**   **复习笔记！！温故知新！**  **形成知识图谱**

**知其然知其所以然：深挖底层原理！！**

**实战很重要！！薪资和代码量成正比**

**学而不思则罔，思而不学则殆**

**多读书**

### 3.1.3 浏览器内核

- **webkit内核(V8引擎)**
	+ 谷歌Chrome     **现在采用Blink内核**
	+ Safari
	+ Opera >=V14     **现在采用Blink内核**
	+ 国产浏览器
	+ 手机浏览器
	+ ...
- **Gecko（ Firefox内核 ）**
	+ 火狐Firefox
- Presto
	+ Opera <V14
- **Trident（IE内核）**
	+ IE
	+ IE EDGE开始采用双内核（其中包含chrome迷你）

[更多信息](https://blog.csdn.net/yuyanjing123456789/article/details/78689595)



谷歌浏览器的控制台（F12/Fn+F12）
- Elements：查看结构样式，可以修改这些内容
- Console：查看输出结果和报错信息，是JS调试的利器
- Sources：查看项目源码
- Network：查看当前网站所有资源的请求信息（包括和服务器传输的HTTP报文信息）、加载时间等（根据加载时间进行项目优化）
- Application：查看当前网站的数据存储和资源文件（可以盗图）

### 3.1.4 JS做客户端语言
> 按照相关的JS语法，去操作页面中的元素，有时还要操作浏览器里面的一些功能
- **ECMAScript3/5/6...**：JS的语法规范（变量、数据类型、操作语句等等）
- **DOM（document object model）**：文档对象模型，提供一些JS的属性和方法，用来操作页面中的DOM元素
- **BOM（browser object model）**：浏览器对象模型，提供一些JS的属性和方法，用来操作浏览器的

### 3.1.5 JS中的变量 variable
> 变量：可变的量，在编程语言中，变量其实就是一个名字，用来存储和代表不同值的东西
>
> var	let	const 	function	class	导包	symbol



```javascript
//ES3
var a = 12;
a = 13;
console.log(a); //=>输出的是a代表的值13

//ES6
let b = 100;
b = 200;

const c = 1000;
c = 2000; //=>报错：CONST创建的变量，存储的值不能被修改（可以理解为叫做常量）

//创建函数也相当于在创建变量
function fn(){}
//创建类也相当于创建变量
class A{}
//ES6的模块导入也可以创建变量
import B from './B.js';

//Symbol创建唯一值
// n==m    false
let n=Symbol(100);
let m=Symbol(100);
```

### 3.1.6 JS中的命名规范
- 严格区分大小写
```javascript
let Test=100;
console.log(test);//=>无法输出，因为第一个字母小写了
```
- 使用数字、字母、下划线、$	//数字不能作为开头
```javascript
let $box; //=>一般用JQuery获取的以$开头
let _box; //=>一般公共变量都是_开头

let 1box; //=>不可以，但是可以写box1
```
- 使用驼峰命名法：首字母小写，其余每一个有意义单词的首字母都要大写（命名尽可能**语义化**明显，使用英文单词）
```javascript
let studentInformation;
let studentInfo;
//常用的缩写：add/insert/create/new（新增）、update（修改）、delete/del/remove/rm（删除）、sel/select/query/get（查询）、info（信息）...

//不正确的写法
let xueshengInfo;
let xueshengxinxi;
let xsxx;
```
- 不能使用关键字和保留字
```javascript
当下有特殊含义的是关键字，未来可能会成为关键字的叫做保留字(？)
var let const function ...

var var = 10; //=>肯定不行的
//=>代码强迫症（代码洁癖）：良好的编程习惯、极客精神


```


### 3.1.7 JS中常用的数据类型
- 基本数据类型
	+ 数字number
		常规数字和NaN
	+ 字符串string
		所有用单引号、双引号、反引号（撇）包起来的都是字符串
	+ 布尔boolean
		true/false
	+ 空对象指针null
	+ 未定义undefined
- 引用数据类型
	+ 对象数据类型object
		+ {} 普通对象
		+ [] 数组对象
		+ /^[+-]?(\d|([1-9]\d+))(\.\d+)?$/ 正则对象
		+ Math数学函数对象
		+ 日期对象
		+ ...
	+ 函数数据类型function

参考资料

1. [关键字和保留字](https://blog.csdn.net/qq_19865749/article/details/78128894)
2. 2018年录制的免费课[基础视频](https://pan.baidu.com/s/1GBykF3c_eg9dqmTcxAfDow#list/path=%2F )： 第一周：24/25/26/27

### 3.2.0 number数字类型
> 包含：常规数字、NaN

#### 3.2.0.1 NaN
> not a number：不是一个数，但它率属于数字类型

NaN和任何值（包括自己）都不相等：NaN!=NaN，所以我们不能用相等的方式判断是否为有效数字

#### 3.2.0.2 isNaN
> 检测一个值是否为非有效数字，如果不是有效数字返回TRUE，反之是有效数字返回FALSE

在使用isNaN进行检测的时候，首先会验证检测的值是否为数字类型，如果不是，先基于Number()这个方法，把值转换为数字类型，然后再检测

```javascript
console.log(isNaN(10))		//false
console.log(isNaN('10'))   //false
console.log(isNaN('aa'))	//true
```



#### 3.2.0.3 把其它类型值转换为数字类型
- Number([val])
- parseInt/parseFloat([val],[进制])：也是转换为数字的方法，对于字符串来说，它是从左到右依次查找有效数字字符，直到遇到非有效数字字符，停止查找（不管后面是否还有数字，都不在找了），把找到的当做数字返回
- ==进行比较的时候，可能要出现把其它类型值转换为数字

```javascript

Number("10")	//10

Number("10.5")	//10.5

Number("10.5.5")	//NaN

Number("aa")	//NaN


```

```javascript
// console.log([val])：在控制台输出内容
// console.log('hello world~~');

// ==：进行比较的
console.log('AA' == NaN);
console.log(10 == NaN);
console.log(NaN == NaN); 

// isNaN([val])
// console.log(isNaN(10)); //=>FALSE
// console.log(isNaN('AA')); //=>TRUE
/*
 * Number('AA') =>NaN 
 * isNaN(NaN) =>TRUE
 */

// console.log(isNaN('10')); //=>FALSE

Number('10')  =>10
isNaN(10) =>FALSE


// ==========Number===========
// 把字符串转换为数字，只要字符串中包含任意一个非有效数字字符（第一个点除外）结果都是NaN，空字符串会变为数字零
console.log(Number('12.5')); //=>12.5
console.log(Number('12.5px')); //=>NaN
console.log(Number('12.5.5')); //=>NaN
console.log(Number('')); //=>0 */

// 布尔转换为数字
console.log(Number(true)); //=>1
console.log(Number(false)); //=>0
console.log(isNaN(false)); //=>false */

// null->0  undefined->NaN
console.log(Number(null)); //=>0
console.log(Number(undefined)); //=>NaN 

// 把引用数据类型转换为数字，是先把他基于toString方法转换为字符串，然后在转换为数字
console.log(Number({name:'10'}));//=>NaN
console.log(Number({}));//=>NaN
// {}/{xxx:'xxx'} .toString() => "[object Object]" => NaN
console.log(Number([]));//=>0
// [].toString() -> ''
console.log(Number([12]));//=>12
// [12].toString() -> '12'
console.log(Number([12,23]));//=>NaN
// [12,23].toString() -> '12,23'

let str = '12.5px';
console.log(Number(str)); //=>NaN
console.log(parseInt(str)); //=>12
console.log(parseFloat(str)); //=>12.5
console.log(parseFloat('width:12.5px')); //=>NaN 
```



### 3.2.1 string字符串数据类型

> 所有用单引号、双引号、反引号（撇 ES6模板字符串）包起来的都是字符串

#### 3.2.1.0 把其它类型值转换为字符串
- [val].toString()
- 字符串拼接

```javascript
let a = 12;
console.log(a.toString()); //=>'12'
console.log((NaN).toString()); //=>'NaN' */

// null和undefined是禁止直接toString的
// (null).toString() //=>报错
// 但是和undefined一样转换为字符串的结果就是 'null'/'undefined'

// 普通对象.toString()的结果是 "[object Object]"  =>?  =>Object.prototype.toString方法不是转换为字符串的，而是用来检测数据类型的

//====================字符串拼接
// 四则运算法则中，除加法之外，其余都是数学计算，只有加法可能存在字符串拼接（一旦遇到字符串，则不是数学运算，而是字符串拼接）
console.log('10' + 10); //=>'1010'
console.log('10' - 10); //=>0
console.log('10px' - 10); //=>NaN */

let a = 10 + null + true + [] + undefined + '珠峰' + null + [] + 10 + false;
/*
10 + null -> 10 + 0 -> 10
10 + true -> 10 + 1 -> 11
11 + [] -> 11 + '' -> '11'  空数组变为数字，先要经历变为空字符串，遇到字符串，啥都别想了，直接变为字符串拼接 
'11' + undefined -> '11undefined'
...
'11undefined珠峰null10false'
*/
console.log(a);
```




### 3.2.2 boolean布尔数据类型
> 只有两个值 true/false

#### 3.2.2.0 把其它类型值转换为布尔类型
> 只有 0、NaN、' '、null、undefined 五个值转换为FALSE，其余都转换为TRUE（而且没有任何的特殊情况）

- Boolean([val])
- !/!!
- 条件判断

```javascript
/* console.log(Boolean(0));
console.log(Boolean(''));
console.log(Boolean(' '));
console.log(Boolean(null));
console.log(Boolean(undefined));
console.log(Boolean([]));
console.log(Boolean([12]));
console.log(Boolean(-1)); */

// !：取反（先转为布尔，然后取反）
// !!：取反再取反，只相当于转换为布尔 <=> Boolean
/* console.log(!1); //=>FALSE
console.log(!!1); //=>true */

// 如果条件只是一个值，不是==/===/!=/>= 等这些比较，是要把这个值先转换为布尔类型，然后验证真假
if (1) {
	console.log('哈哈');
}
if ('3px' + 3) {
	//=>'3px3'
	console.log('呵呵');
}
if ('3px' - 3) {
	//=>NaN-3=>NaN
	console.log('嘿嘿');
}

```



### 3.2.3 null / undefined
> null和undefined都代表的是没有

- null：意料之中（一般都是开始不知道值，我们手动先设置为null，后期再给予赋值操作）
```
let num = null; //=>let num = 0;  一般最好用null作为初始的空值，因为零不是空值，他在栈内存中有自己的存储空间（占了位置）
...
num = 12;
```

- undefined：意料之外（不是我能决定的）
```
let num; //=>创建一个变量没有赋值，默认值是undefined
...
num = 12;
```

### 3.2.4 object对象数据类型-普通对象
> {[key]:[value],...} 任何一个对象都是由零到多组键值对（属性名：属性值）组成的（并且属性名不能重复）

> 数组是特殊的对象数据类型