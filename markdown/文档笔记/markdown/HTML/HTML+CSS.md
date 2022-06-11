## 思维导图

![20200507153758833](D:\Pictures\20200507153758833.png)

##网页的基本描述：

```html
<!DOCTYPE html>
<!--DOCTYPE:告诉浏览器，我们要使用什么规范-->
<html lang="en">
<!--head标签代表网页头部-->
<head>
    <!--meta描述性标签，它用来描述我们网站的一些信息-->
    <meta charset="UTF-8">
    <title>网页bast</title>
</head>
<!--body标签代表网页主体-->
<body>
网页内容测试
</body>
</html>
```

####网页的基本标签：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>基本标签</title>
</head>
<body>
<!--标题标签-->
<h1>一级标签</h1>
<!--段落标签-->
<p>这是一个段落</p>
<!--换行标签-->
这是换行<br/>
    换行成功<br/>
<!--水平线标签-->
<hr/>
<!--粗体、斜体标签-->
<h1>字体样式标签</h1>
粗体：<strong>这是粗体</strong> 
斜体：<em>这是斜体</em>
</body>
</html>
```

####特殊符号：

```html
<!--特殊符号-->
空    格：
空&nbsp;格
空&nbsp;格&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;end
<br/>
&gt;大于
<br/>
&lt;小于
<br/>
&copy;版权符号
```

####图像格式（图片的插入）：

![image-20220404205949240](C:\Users\26411\AppData\Roaming\Typora\typora-user-images\image-20220404205949240.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>图像标签学习</title>
</head>
<body>
<!--img标签学习
src:图片地址
    相对地址，绝对地址
    ../ --上一级目录
-->
<img src="resources/image/1.jpg（图片链接路径）"alt="图像替代文字（在没有图片的时候显示）"title="悬停文字（鼠标放在图片上显示）"width="600"height="400">
</body>
</html>
```

#### 链接标签

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>链接标签学习</title>
</head>
<body>

<!--a标签
herf:必填，表示要跳转到哪个界面

-->
<a href="图像标签.html">点击跳转到指定界面</a>
<a href="http://www.baidu.com">点击跳转到百度</a>

</body>
</html>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>链接标签学习</title>
</head>
<body>
<!--使用name作为标记-->
<a name="top">顶部</a>
<!--a标签
herf:必填，表示要跳转到哪个界面
target:表示窗口在哪里打开
_blank:在新窗口打开
_self:在自己的网页中打开
-->
<a href="图像标签.html"target="_blank">点击跳转到指定界面</a>
<a href="http://www.baidu.com"target="_self">点击跳转到百度</a>

<br/>
<!--图片超链接-->
<a href="http://www.csdn.net">
    <img src="resources/image/1.jpg"alt="测试"title="悬停文字"width="600"height="400">
</a>

<p>
    <a href="http://www.csdn.net">
        <img src="resources/image/1.jpg"alt="测试"title="悬停文字"width="600"height="400">
    </a>
</p>

<p>
    <a href="http://www.csdn.net">
        <img src="resources/image/1.jpg"alt="测试"title="悬停文字"width="600"height="400">
    </a>
</p>

<p>
    <a href="http://www.csdn.net">
        <img src="resources/image/1.jpg"alt="测试"title="悬停文字"width="600"height="400">
    </a>
</p>

<p>
    <a href="http://www.csdn.net">
        <img src="resources/image/1.jpg"alt="测试"title="悬停文字"width="600"height="400">
    </a>
</p>
<!--锚链接
1. 需要一个锚标记
2. 跳转到标记
#：通过#跳转到标记

-->

<a href="#top">回到顶部</a>

<a name="down">down</a>

<!--功能性链接
邮件链接：maito;
QQ链接：来自于腾讯（在QQ推广官方可以生成网页推广链接（加QQ）
-->
<a href="mailto:2641123591@qq.com">点击联系我</a>


<a target="_blank" href="http://wpa.qq.com/msgrd?v=3&uin=&site=qq&menu=yes"><img border="0" src="http://wpa.qq.com/pa?p=2::53" alt="在这里通过QQ沟通" title="在这里通过QQ沟通"/></a>


</body>
</html>
```

#### 行内元素和块元素

块元素：

- 无论内容多少，该元素独占一行
- （p、h1-h6...)

行内元素：

- 内容撑开宽度，左右都是行内元素的可以排在一行
- （a,strong,em...)

#### 列表

列表就是信息资源的一种展示形式，它可以使信息结构化和条理化，并以列表的样式显示出来，以便浏览器者能更快捷地获得相应的信息

列表的分类：

- 无序列表
- 有序列表
- 定义列表

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>列表标签学习</title>
</head>
<body>
<!--有序列表-->
<ol>
    <li>java</li>
    <li>python</li>
    <li>运维</li>
    <li>前端</li>
    <li>C/C++</li>
</ol>
<hr/>

<!--无序列表-->
<ul>
    <li>java</li>
    <li>python</li>
    <li>运维</li>
    <li>前端</li>
    <li>C/C++</li>

</ul>
<hr>
<!--定义列表-->

<dl>
   <dt>学科</dt>
    <dd>java</dd>
    <dd>python</dd>
    <dd>linux</dd>
    <dd>C/C++</dd>
    <hr>
    <dt>位置</dt>
    <dd>四川</dd>
    <dd>重庆</dd>
    <dd>西安</dd>
</dl>

</body>
</html>
```



#### 表格

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>表格标签学习</title>
</head>
<body>
<!--表格table
行：  tr
列：  td
border:为表格加上边框=宽度
-->
<table border="1px">
    <tr>
        <td>1-1</td>
        <td>1-2</td>
        <td>1-3</td>
        <td>1-4</td>
    </tr>
    <tr>
        <td>2-1</td>
        <td>2-2</td>
        <td>2-3</td>
        <td>2-4</td>
    </tr>
    <tr>
        <td>3-1</td>
        <td>3-2</td>
        <td>3-3</td>
        <td>3-4</td>
    </tr>
</table>

</body>
</html>
```

#### 视频和音频

视频元素：

- vidio

音频元素：

- audio

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>媒体元素学习</title>
</head>
<body>
<!--音频和视频
src:资源路径
controls:控制条
autoplay:自动播放
-->
<video src="resources/vidio/target_video.mp4" controls autoplay></video>
<!--controls可以为视频增加控制元素-->
<audio src="resources/audio/测试.mp3" controls="controls" autoplay="autoplay"></audio>
</body>
</html>
```

#### 页面结构分析

| 元素名  | 描述                                           |
| ------- | ---------------------------------------------- |
| header  | 标题头部区域的内容（用于页面或页面中的一块区域 |
| footer  | 标记脚步区域的内容（用于整个页面中的一块区域） |
| section | web页面中的一块独立区域                        |
| article | 独立的文章内容                                 |
| aside   | 相关内容或应用（常用于侧边栏）                 |
| nav     | 导航类型辅助内容                               |

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>页面结构学习</title>
</head>
<body>

<header>
    <h2>网页头部</h2>
</header>
<section>
    <h2>网页主体</h2>
</section>
<footer>
    <h2>网页脚部</h2>
</footer>

</body>
</html>
```

##### iframe内联框架

![image-20220405102412644](C:\Users\26411\AppData\Roaming\Typora\typora-user-images\image-20220405102412644.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>iframe内联框架</title>
</head>
<body>
<!--iframe内联框架
src:地址
width:宽度高度

-->
<!--<iframe src="https://www.baidu.com" frameborder="0" width="1000px" height="800"></iframe>-->

<!--<iframe src="//player.bilibili.com/player.html?aid=55631961&bvid=BV1x4411V75C&cid=97257967&page=11" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>-->

<!--内联框架-->
<iframe src=""  name="hello" frameborder="0" width="1000px" height="800"></iframe>

<a href="媒体元素.html" target="hello">点击跳转</a>

</body>
</html>
```

##### 表单语法

![image-20220405113351831](C:\Users\26411\AppData\Roaming\Typora\typora-user-images\image-20220405113351831.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>登录注册</title>
</head>
<body>
<h1>注册</h1>
<!--表单注册
action :表单提交的位置，可以是网站，也可以是一个请求地址
method:post,    get 提交方式
get：提交方式：可以在url中看到提交的信息（不安全）
post：提交方式，比较安全，可以传输大文件
-->

<form action="媒体元素.html"method="get">
<!--文本输入框：input type="txt"-->
    <p>名字:<input type="text" name="username"></p>
    <!--密码输入框：input type="password"-->
    <p>密码:<input type="password" name="pwd"></p>
<p>
    <input type="submit">
<!--submit表示提交-->
    <input type="reset">
<!--reset表示重置-->
</p>
</form>
</body>
</html>
```

#### 表单元素格式

| **属性**  | 说明                                                         |
| --------- | ------------------------------------------------------------ |
| **type**  | 指定元素类型。text、password、checkbox、radio、submit、resrt、file、hidden、image和button，默认为text |
| **name**  | 指定表单元素的名称                                           |
| **value** | 元素的初始值。type为radio时必须指定一个值                    |
| size      | 指定表单元素的初始宽度。当type为text或password时，表单元素的大小以字符为单位。对于其他类型，宽度以像素为单位 |
| maxlength | type为text或password时，输入的最大字符数                     |
| checked   | type为radio或checkbox时,指定按钮是否是被选中                 |

####文本框和单选框

```html
<form action="媒体元素.html"method="get">
<!--文本输入框：input type="txt"-->
<!-- {value="输入内容" maxlength="8" size="30"}-->
<!--
value="输入内容"——默认初始值
maxlength="8"——最长能写几个字符
size="30"——文本框的长度
name——代表属性（每一个input表单中都要带有name属性）
-->
    <p>名字:<input type="text" name="username" value="输入内容" maxlength="8" size="30"></p>
    <!--密码输入框：input type="password"-->
    <p>密码:<input type="password" name="pwd"></p>
<p>
    <input type="submit">
<!--submit表示提交-->
    <input type="reset">
<!--reset表示重置-->
</p>
</form>
```

单选框：

```html
<!--单选框标签
input type="radio"
value : 单选框的值
name : 表示组（如果组不同，那么一组的内容就可以同时选中）
-->
    <p>性别
    <input type="radio" value="boy" name="sex"/>男
    <input type="radio" value="girl" name="sex"/>女

</p>
```

#### 按钮和多选框

多选框：

```html
</p>
<!--多选框
input type="checkbox"
name——代表属性（每一个input表单中都要带有name属性）
-->
<p>爱好：
    <input type="checkbox" value="sleep" name="hobby">睡觉
    <input type="checkbox" value="code" name="hobby">敲代码
    <input type="checkbox" value="chat" name="hobby">聊天
    <input type="checkbox" value="game" name="hobby">游戏
</p>
```

按钮：

```html
<!--按钮
input type="button"——普通按钮
input type="image"——图像按钮
input type="submit"——提交按钮
input type="reset"——重置按钮
-->
<p>按钮:
    <input type="button" name="btn1" value="点击变长">
    <input type="image" src="resources/image/头像3.gif">
</p>
<p>
    <input type="submit">
<!--submit表示提交-->
    <input type="reset">
<!--reset表示重置-->
</p>
```

#### 列表框文本域和文件域

下拉框：

```html
<!--下拉框 ， 列表框
selected默认选择
checked默认选中（勾选）
-->
<P>下拉框
    <select name="列表名称">
        <option value="china">中国</option>
        <option value="选项的值">美国</option>
        <option value="ger"selected>德国</option>
        <option value="ch">瑞士</option>
    </select>
</P>
```

文本域：

```html
<!--文本域
textarea name="textarea"
cols="30" rows="10"——行和列
-->
<p>反馈
    <textarea name="textarea" cols="30" rows="10">文本内容</textarea>

</p>
```

文件域：

```html
<!--文件域
input type="file" name="files"
-->
<p>
    <input type="file" name="files">
    <input type="button" value="上传" name="upload">
</p>
```

#### 搜索框滑块和简单验证

滑块：

```html
<!--滑块-->
<p>滑块：
    <input type="range" min="0" max="100" step="5">
</p>
```

搜索框：

```html
<!--搜索框-->
    <p>搜索
        <input type="search" name="search">
    </p>
```

验证：

```html
<!--邮件验证-->
<p>邮箱
    <input type="email" name="email">
</p>
<!--URL-->
    <p>URL
        <input type="url" name="url">
    </p>
<!--数字验证
step="10"——表示一次调整10个数字
max;min表示最大值和最小值
-->
    <p>数字
        <input type="number" name="num" max="100" min="0" step="10">

    </p>
```

#### 表单的应用

**隐藏域**hidden

**只读**readonly

**禁用**disabled

```html
readonly（可以将内容设定为只读，无法修改
disabled（可以将选择内容禁用，然后该选项无法选中）
hidden（可以把内容隐藏起来，但是属性还在）
```

```html
<!--增强鼠标可用性-->
    <p>
    <label for="mark">点击试试</label>
    <input type="text">
</p>
```

#### 表单初级验证

常用方式：

- placeholder——提示信息
- required——非空判断
- pattern——正则表达式（较复杂，网络搜索相关的正则表达式

placeholder:默认信息提示用户输入

```HTML
<p>名字:<input type="text" name="username" placeholder="请输入用户名"></p>
```

required:表示此处内容不能为空（必须输入有内容才能提交）

pattern：正则表达式的验证

```HTML
<!--正则表达式列子
正则表达式网站：https://www.jb51.net/tools/regex.htm
-->
    <p>自定义邮箱：
        <input type="text" name="dymail" pattern="/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/">
    </p>
```

# CSS

##一、什么是CSS

#### 

cascading style sheet层叠级联样式表

css：表现（美化网页）

字体、颜色、边距、高度、宽度、背景图片、网页定位、网页浮动

1.3快速入门

style

```html
<!--  规范<style>可以编写CSS代码，每一个语句最好以分号结尾  -->
<!--
语法：选择器{
            声明1；
            声明2；
            声明3；
}
```

```html
<!--建议使用这种文档-->
    <link rel="stylesheet" href="style.css">
<!--link链接 stylesheet 默认层叠样式表  href z-->
```

CSS优势：

1. 内容和表现分离
2. 网页结构表现统一，可以实现复用
3. 样式十分丰富
4. 建议使用独立于HTML的CSS文件
5. 利用SEO，容易被搜索引擎收录！

### 三种导入方式

#### 1.行内样式

*这是行内样式*，一般不建议这样写，但是可以针对一些元素进行编写

```html
<!--行内样式，在标签元素中，编写一个style属性，编写样式即可-->
<h3 style="color:red">这是行内样式</h3>
注意在CSS中的注释为
/*这是注释*/
```

style标签一般是在<head>中进行

```html
<head>
    <meta charset="UTF-8">
    <title>Title</title>
<!--内部样式-->
    <style>
    h1{
        color:green;
    }
</style>
</head>
```

```html
<!--外部样式-->
    <link rel="stylesheet" href="style.css">
</head>
<body>

<!--CSS样式的优先级：采用就近原则，距离代码近的先采用-->

<h1>这是标题</h1>
<h2>这是第二个测试</h2>
<!--行内样式，在标签元素中，编写一个style属性，编写样式即可-->
<h3 style="color:red">这是行内样式</h3>

</body>
</html>
```

扩展：外部样式两种写法

####2.链接样式

- 链接式：
- html

```html
<!--外部样式-->
    <link rel="stylesheet" href="style.css">
```

#### 3.导入样式

- 导入式：(不建议使用)
- CSS2.1

```html
<!--导入式-->
    <style>
        @import url("style.css")
    </style>

```

link属于html标签。@import在css中使用表示导入外部样式表；
页面被加载的时，link会同时被加载，而@import引用的CSS会等到页面被加载完再加载;
import只在IE5以上才能识别，而link是HTML标签，无兼容问题;
link方式的样式的权重 高于@import的权重；
link 支持使用javascript改变样式 （document.styleSheets），后者不可
本质上区别不大，但是为了软件中编辑布局网页html代码，一般使用link较多。

##二、选择器

#### 基本选择器

**作用：选择页面上的某一个或者某一类元素**

1. 标签选择器：选择一类标签

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>

    <style>
        /*标签选择器，会选择到页面上所有的这个标签元素 */
        h1{
            color: #f8be2c;
            background: #06eea4;
            border-radius:24px;
        }
        p{
            font-size:60px;
        }
    </style>

</head>
<body>

<h1>学习Java</h1>
<h1>学习Java</h1>
<p>听狂神说</p>
</body>
</html>
```



2. 类 选择器class：选择所有class属性一致的标签，跨标签，.类名{}

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>类选择器</title>

    <style>
        /*类选择器的格式 .class的名称{}
        好处：可以多个标签归类，同一个class，可以复用
        class可以全局复用

        */
        .qinjiang{
            color:#06eea4;
        }
        .kuangshen{
            color:#ec760c;
        }


    </style>

</head>
<body>

<h1 class="qinjiang">标题1</h1>
<h1 class="kuangshen">标题2</h1>
<h1>标题3</h1>
<p class="qinjiang">P标签</p>

</body>
</html>
```



3. id选择器：全局唯一！！ #id名{}

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>id选择器</title>

    <style>
/*
id选择器——id必须保证全局唯一！！！
#id名称{}
不遵循就近原则，固定的
id选择器》class选择器》标签选择器
*/
#qingjiang{
    color:#f8be2c;
}
    </style>

</head>
<body>
<h1 id="qingjiang">标题1</h1>
<h1>标题2</h1>
<h1>标题3</h1>
<h1>标题4</h1>
<h1>标题5</h1>
</body>
</html>
```

优先级：id > class >标签

#### 层次选择器

1. 后代选择器：在某个元素的后面 ——祖爷爷 爷爷 爸爸 你

```css
/*后代选择器*/
body p{
    background: red;
}
```



2. 子选择器，一代，儿子

```css
/*子选择器*/

body>p{
    background: #06eea4;
}
```



3. 相邻兄弟选择器-同辈

```css
/*相邻兄弟选择器，只有一个，相邻（向下衍生）*/
.active + p{
    background: #f8be2c;
}
```



4. 通用选择器

```css
/*通用兄弟选择器 ,当前选中元素的向下的所有兄弟元素*/
.active~p{
    background: #feec85;
}
```

层次选择器：

```css
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>

    <style>
/*background背景颜色*/
       /* p{
            background: #ec760c;
        }
*/
/*后代选择器*/
/*body p{
    background: red;
}*/

    /*子选择器*/
/*body>p{
    background: #06eea4;
}*/
/*相邻兄弟选择器，只有一个，相邻（向下衍生）*/
/*.active + p{
    background: #f8be2c;
}*/
/*通用兄弟选择器 ,当前选中元素的向下的所有兄弟元素*/
.active~p{
    background: #feec85;
}

    </style>
</head>
<body>

<p>p0</p>
<p class="active">p01</p>
<p>p1</p>
<p>p2</p>
<p>p3</p>
<ul>
    <li>
        <p>p4</p>
    </li>
    <li>
        <p>p5</p>
    </li>
    <li>
        <p>p6</p>
    </li>
</ul>

</body>
</html>
```

后代选择器：

例如，如果写作 ul em，这个语法就会选择从 ul 元素继承的所有 em 元素，而不论 em 的嵌套层次多深。

因此，ul em 将会选择以下标记中的所有 em 元素：

这个规则会把作为 h1 元素后代的 em 元素的文本变为 红色。其他 em 文本（如段落或块引用中的 em）则不会被这个规则选中：

```css
<ul>
  <li>List item 1
    <ol>
      <li>List item 1-1</li>
      <li>List item 1-2</li>
      <li>List item 1-3
        <ol>
          <li>List item 1-3-1</li>
          <li>List item <em>1-3-2</em></li>
          <li>List item 1-3-3</li>
        </ol>
      </li>
      <li>List item 1-4</li>
    </ol>
  </li>
  <li>List item 2</li>
  <li>List item 3</li>
</ul>
```

![image-20220417171302079](C:\Users\26411\AppData\Roaming\Typora\typora-user-images\image-20220417171302079.png)





#### 结构伪类选择器

伪类：

```css
/*ul的第一个子元素*/
ul li:first-child{
    background: #f8be2c;
}
    /*ul的最后一个子元素*/
ul li:last-child{
    background: #f35626;
}

    /*选中p1:定位到父元素，选择当前的第一个元素
    选中当前p元素的父级元素，选中父级元素的第一个
    */
p:nth-child(1){
    background: chocolate;
}
/*选中父元素，下的p元素的第二个，类型*/
p:nth-of-type(2){
    background: yellow;
}

```

![image-20220417132711457](C:\Users\26411\AppData\Roaming\Typora\typora-user-images\image-20220417132711457.png)

#### 属性选择器

属性选择器（常用）

```css
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
         .demo a{
            display: block;
            height: 50px;
            width: 50px;
            float:left;
            border-radius: 10px;
            background: blue;
            text-align: center;
            color: beige;
            text-decoration: none;
            margin-right: 5px;
            font: bold 20px/50px Arial;
        }
         /*属性名，属性名=属性值（正则）
         =表示绝对等于
         *=表示包含
         ^=表示以...开头
         $=表示以...结尾
         存在id属性的元素  a[]{}
         */
        /* a[id]{
             background: red;
         }*/

         /*id=first的元素*/
       /* a[id=first]{
            background: aqua;
        }*/

        /*class中有links元素*/
       /* a[class = "links item2 first2"]{
            background: orange;
        }*/
        /*a[class*="links"]{
            background: black ;
        }*/
        /*选中href中以http开头的元素*/
        a[href^="http"]{
            background: orange;
        }
    </style>

</head>
<body>
<p class="demo">
    <a href="http://www.baidu.com" class="links item first" id="first">1</a>
    <a href="/adad/faf" class="links item2 first2" >2</a>
    <a href="qwe123" class="links item3 first3" >3</a>
    <a href="eweqe" class="links item4 first4" >4</a>
    <a href="rrrrr" class="links item5 first5" >5</a>
    <a href="ttt" class="links item6 first6" >6</a>
    <a href="yyy" class="links item7 first7" >7</a>
</p>
</body>
</html>

```



简单属性选择

如果希望选择有某个属性的元素，而不论属性值是什么，可以使用简单属性选择器。

```css
/*把包含标题（title）的所有元素变为红色，可以写作：*/
*[title] {color:red;}
/*可以只对有 href 属性的锚（a 元素）应用样式：*/
a[href] {color:red;}
/*可以根据多个属性进行选择，只需将属性选择器链接在一起即可。
例如，为了将同时有 href 和 title 属性的 HTML 超链接的文本设置为红色，*/
a[href][title] {color:red;}
/*可以对所有带有 alt 属性的图像应用样式，从而突出显示这些有效的图像*/
img[alt] {border: 5px solid red;}
/*想选择有 moons 属性的所有 planet 元素，使之显示为红色，以便能更关注有 moons 的行星，就可以这样写：*/
planet[moons] {color:red;}
/*让以下标记片段中的第二个和第三个元素的文本显示为红色，但第一个元素的文本不是红色：*/
<planet>Venus</planet>
<planet moons="1">Earth</planet>
<planet moons="2">Mars</planet>
/*根据具体属性值选择
除了选择拥有某些属性的元素，还可以进一步缩小选择范围，只选择有特定属性值的元素。*/
/*例如，假设希望将指向 Web 服务器上某个指定文档的超链接变成红色，可以这样写：*/

a[href="http://www.w3school.com.cn/about_us.asp"] {color: red;}
/*与简单属性选择器类似，可以把多个属性-值选择器链接在一起来选择一个文档。*/
a[href="http://www.w3school.com.cn/"][title="W3School"] {color: red;}
/*这会把以下标记中的第一个超链接的文本变为红色，但是第二个或第三个链接不受影响：*/
<a href="http://www.w3school.com.cn/" title="W3School">W3School</a>
<a href="http://www.w3school.com.cn/css/" title="CSS">CSS</a>
<a href="http://www.w3school.com.cn/html/" title="HTML">HTML</a>
/**/
```

##三、美化网页元素

####字体样式

span标签：重点要突出的字，使用span套起来

```css
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>

    <style>
        #title{
            font-size:50px;
        }
    </style>

</head>
<body>
欢迎学习<span id="title">Java</span>
</body>
</html>
```

```css
    /*
    font-family:字体
    font-size:字体大小
    font-weight:字体粗细
    color:字体颜色
    */
    <style>
        body{
            font-family: 楷体;
            color:#f8be2c;
        }
        h1{
            font-size: 50;
        }
        p1{
            font-weight: bold;
        }
    </style>
```

字体风格：

```css
通过 font-family 属性设置更具体的字体
h1 {font-family: Georgia;}
如果用户没有安装 Georgia 字体，就只能使用用户代理的默认字体来显示 h1 元素。

我们可以通过结合特定字体名和通用字体系列来解决这个问题：

h1 {font-family: Georgia, serif;}
如果你希望文档使用一种 sans-serif 字体，但是你并不关心是哪一种字体，以下就是一个合适的声明：

body {font-family: sans-serif;}
font-style 属性最常用于规定斜体文本。

该属性有三个值：

normal - 文本正常显示
italic - 文本斜体显示
oblique - 文本倾斜显示
p.normal {font-style:normal;}
p.italic {font-style:italic;}
p.oblique {font-style:oblique;}
```

字体变形：

font-variant 属性可以设定小型大写字母。

小型大写字母不是一般的大写字母，也不是小写字母，这种字母采用不同大小的大写字母。

```css
p {font-variant:small-caps;}
```



![image-20220417192757483](C:\Users\26411\AppData\Roaming\Typora\typora-user-images\image-20220417192757483.png)

字体加粗：

[font-weight 属性](https://www.w3school.com.cn/cssref/pr_font_weight.asp)设置文本的粗细。

使用 bold 关键字可以将文本设置为粗体。

关键字 100 ~ 900 为字体指定了 9 级加粗度。如果一个字体内置了这些加粗级别，那么这些数字就直接映射到预定义的级别，100 对应最细的字体变形，900 对应最粗的字体变形。数字 400 等价于 normal，而 700 等价于 bold。

如果将元素的加粗设置为 bolder，浏览器会设置比所继承值更粗的一个字体加粗。与此相反，关键词 lighter 会导致浏览器将加粗度下移而不是上移。

```css
p.normal {font-weight:normal;}
p.thick {font-weight:bold;}
p.thicker {font-weight:900;}
```

```css
<html>
<head>
<style type="text/css">
p.normal {font-weight: normal}
p.thick {font-weight: bold}
p.thicker {font-weight: 900}
</style>
</head>

<body>
<p class="normal">This is a paragraph</p>

<p class="thick">This is a paragraph</p>

<p class="thicker">This is a paragraph</p>
</body>

</html>
```

![image-20220417193202439](C:\Users\26411\AppData\Roaming\Typora\typora-user-images\image-20220417193202439.png)

字体大小

[font-size 属性](https://www.w3school.com.cn/cssref/pr_font_font-size.asp)设置文本的大小。

通过像素设置文本大小，可以对文本大小进行完全控制：

```css
h1 {font-size:60px;}
h2 {font-size:40px;}
p {font-size:14px;}
```

![image-20220417193732081](C:\Users\26411\AppData\Roaming\Typora\typora-user-images\image-20220417193732081.png)

使用em来设置字体大小：

1em 等于当前的字体尺寸。如果一个元素的 font-size 为 16 像素，那么对于该元素，1em 就等于 16 像素。在设置字体大小时，em 的值会相对于父元素的字体大小改变。

浏览器中默认的文本大小是 16 像素。因此 1em 的默认尺寸是 16 像素。

可以使用下面这个公式将像素转换为 em：*pixels*/16=*em*

（注：16 等于父元素的默认字体大小，假设父元素的 font-size 为 20px，那么公式需改为：*pixels*/20=*em*）

```css
h1 {font-size:3.75em;} /* 60px/16=3.75em */
h2 {font-size:2.5em;}  /* 40px/16=2.5em */
p {font-size:0.875em;} /* 14px/16=0.875em */
```

![image-20220417194001231](C:\Users\26411\AppData\Roaming\Typora\typora-user-images\image-20220417194001231.png)

结合使用百分比和EM：

![image-20220417194115801](C:\Users\26411\AppData\Roaming\Typora\typora-user-images\image-20220417194115801.png)

####CSS 字体属性

| 属性                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [font](https://www.w3school.com.cn/cssref/pr_font_font.asp)  | 简写属性。作用是把所有针对字体的属性设置在一个声明中。       |
| [font-family](https://www.w3school.com.cn/cssref/pr_font_font-family.asp) | 设置字体系列。                                               |
| [font-size](https://www.w3school.com.cn/cssref/pr_font_font-size.asp) | 设置字体的尺寸。                                             |
| [font-size-adjust](https://www.w3school.com.cn/cssref/pr_font_font-size-adjust.asp) | 当首选字体不可用时，对替换字体进行智能缩放。（CSS2.1 已删除该属性。） |
| [font-stretch](https://www.w3school.com.cn/cssref/pr_font_font-stretch.asp) | 对字体进行水平拉伸。（CSS2.1 已删除该属性。）                |
| [font-style](https://www.w3school.com.cn/cssref/pr_font_font-style.asp) | 设置字体风格。                                               |
| [font-variant](https://www.w3school.com.cn/cssref/pr_font_font-variant.asp) | 以小型大写字体或者正常字体显示文本。                         |
| [font-weight](https://www.w3school.com.cn/cssref/pr_font_weight.asp) | 设置字体的粗细。                                             |

####文本样式

1. 颜色 color	rgb	 rgba
2. 文本对齐方式   text-align = center
3. 首行缩进 text-indent:2em
4. 行高:line-height: 单行文字上下居中！ line-height = height
5. 装饰 text-decoration;
5. 文本图片水平对齐：vertical-align:middle

 ```css
 <!DOCTYPE html>
 <html lang="en">
 <head>
     <meta charset="UTF-8">
     <title>文本的装饰</title>
 <!--
 颜色：
     单词
         RGB 0~f
         RGBA  a:0-1
 text-align：排版，居中
 text-indent:首行缩进；段落首行缩进
  height:300px;
  line-height:50px;
 行高 和 块的高度一致，就可以上下居中
 -->
     <style>
         h1{
             color:rgba(0,255,255,0.8);
             /*这是文本居中*/
             text-align:center;
         }
         /*这是首行缩进，段落缩进*/
         .p1{
             text-indent: 2em;
         }
         /*这里设置行高*/
         .p3{
             background: royalblue;
             height:300px;
             line-height:50px;
         }
     </style>
 
 </head>
 <body>
 <h1>这是一个测试文本</h1>
    <p class="p1"> 嘉峪关城，城墙高9米，还要在城墙之上修建数十座大小不同的楼阁和众多的垛墙，用砖数量之大是非常惊人的，当时，施工条件很差，没有吊运设备，全靠人工搬运。</p>
     <p class="p3">而当时修关城所用的砖，都是在40里以外的地方烧制而成。砖烧好后，用牛车拉到关城之下，再用人工往上背。</p>
     <p>由于城高，唯一能上下的马道坡度大，上下很困难，尽管派了许多人往城墙上背砖，个个累得要死，但背上去的砖却仍然供不应求，工程进展受到了严重影响。</p>
 <p>一天，一个放羊的孩子来到这里放羊玩耍，看到这个情景，灵机一动，解下腰带，两头各捆上一块砖，搭在山羊身上，然后，用手拍一下羊背，身子轻巧的山羊，驮着砖一溜小跑就爬上了城墙。</p>
 <p> 人们看了又惊又喜，纷纷仿效，大量的砖头很快就运上了城墙。</p>
 
 
 </body>
 </html>
 ```

```css
text-indent:2em;//段落首行缩进
background://颜色
line-height://行高
```

####文本阴影和超链接伪类

####阴影

```css
/*text-shadow:阴影颜色，水平偏移，垂直偏移，阴影半径    */
        #price{
            text-shadow: #3d98e9 10px 10px 2px;
        }
```

####伪类

正常情况下，a,a:hover

```css
 a{
            /*Default color*/	默认颜色
            text-decoration: none;
            color:#000000;
        }
    /*鼠标悬浮的状态（只需记住：hover)*/
        a:hover{
            color:orange;
            font-size;50px;
        }
```

####列表

```css
/*ul li*/
/*
list-style:
none 去掉圆点
circle 空心圆
decimal 数字
square 正方形
*/
ul{
    background: #929090;
}
ul li{
    height: 30px;
    list-style:none ;
    text-indent: 1em ;
}
```

#### 背景

```css
background-image:url("");/*默认是全部平铺的*/
background-repeat:repeat-x/*水平平铺*/
background-repeat:repeat-y/*垂直平铺*/
background-repeat:no-repeat/*不平铺*/

```



背景颜色

背景图片

```css
background:red url("图片相对路劲") 270px 10px no-repeat
background-position：/*定位：背景位置*/

```



```css
 <style>
        div{
            width:1000px;
            height:700px;
            border:1px solid red;
            background-image: url("images/mao1.jpg");
        /*    默认全部平铺*/
        }
        div1{
            background-repeat: repeat-x;
        }
        div2{
            background-repeat: repeat-y;
        }
        div3{
            background-repeat: no-repeat;
        }
    </style>
```

![image-20220425205438523](C:\Users\26411\AppData\Roaming\Typora\typora-user-images\image-20220425205438523.png)

#### 渐变

网址：https://www.grablent.com
径向渐变、圆形渐变

```css
渐变
background-color: #4158D0;
background-image: linear-gradient(225deg, #4158D0 0%, #C850C0 5%, #FFCC70 12%, #56d9cc 75%, #e38bb9 100%);
/*https://www.grabient.com/*/
```

#### 盒子模型

![image-20220426202509982](C:\Users\26411\AppData\Roaming\Typora\typora-user-images\image-20220426202509982.png)

1. margin：外边距
2. padding：内边距
3. border：边框

#### 边框

###### 用户登录框

```css
<div id="box">
    <h2>会员登录</h2>
    <from action="#">
        <div>
            <span>用户名：</span>
            <input type="text">
        </div>
        <div>
            <span>密码：</span>
            <input type="text">
        </div>
        <div>
            <span>邮箱：</span>
            <input type="text">
        </div>
    </from>

</div>
</from>
</body>
```

```css
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
            /*body:总有一个默认的外边距margin:0*/
            /*h1,ul,li,a,body{*/
            /*    margin:0;*/
            /*    padding:0;*/
            /*    text-decoration: none;*/
            /*}*/
        /*border:粗细，样式，颜色*/
        #box{
            width:300px;
            border:1px solid red;
        }
            h2{
                font-size:16px;
                background-color:#63a35c;
                line-height:30px ;
                margin:0;
            }
        form{
            background:#63a35c;
        }
        div:nth-of-type(1)>input{
            border:3px solid black;
            /*border”参数的含义是：边框线的宽度是：thin（细线）；边框线的类型：solid（实线）；边框线的颜色：red（红色）。
边框线的宽度有三个标准值：thin（细线）、medium（中粗线）和thick（粗线），*/
        }
        div:nth-of-type(2)>input{
            border:3px dashed #f9ef74;/*dashed，用来形成虚框*/
        }

    </style>
</head>
<body>
<div id="box">
    <h2>会员登录</h2>
    <form action="#">
        <div>
            <span>用户名：</span>
            <input type="text">
        </div>
        <div>
            <span>密码：</span>
            <input type="text">
        </div>
        <div>
            <span>邮箱：</span>
            <input type="text">
        </div>
    </form>

</div>
</from>
</body>
</html>
```



border：粗细 样式 颜色

1. 边框的粗细
2. 边框的样式
3. 边框的颜色

####外边距----妙用：居中

margin-left/right/top/bottom–>表示四边，可分别设置，也可以同时设置如下

```css
margin:0 0 0 0/*分别表示上、右、下、左；从上开始顺时针*/
/*例1：居中*/
margin:0 auto /*auto表示左右自动*/
/*例2：*/
margin:4px/*表示上、右、下、左都为4px*/
/*例3*/
margin:10px 20px 30px/*表示上为10px，左右为20px，下为30px*/

```

######盒子的计算方式：
margin+border+padding+内容的大小

总结：
body总有一个默认的外边距 margin:0
常见操作：初始化

```css
margin:0;
padding:0;
text-decoration:none;

```

#### 圆角边框----border-radius

border-radius有四个参数（顺时针），左上开始
圆圈：圆角=半径

```css
<style>
        div{
           width:100px;
            height:100px;
            border:10px solid red;/*边框,solid:实线*/
            border-radius:100px;
        /*    圆圈： 圆角 = 半径！*/
        /*    左上，右上，右下，z下，顺时针*/
        }
    </style>
```



盒子阴影

浮动

标准文档流

![20200507094752916](D:\Pictures\20200507094752916.png)

块级元素：独占一行 h1~h6 、p、div、 列表…
行内元素：不独占一行 span、a、img、strong

> 行内元素可以包含在块级元素中，反之则不可以

#### display

1. block：块元素
2. inline：行内元素
3. inline-block：是块元素，但是可以内联，在一行
4. none：消失

> 这也是一种行内元素排列的方式，但是我们很多情况用float

```css
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <!--block 块元素
        inline 行内元素
        inline-block 是块元素，但是可以内联 ，在一行
    -->
    <style>
        div{
            width: 100px;
            height: 100px;
            border: 1px solid red;
            display: inline-block;
        }
        span{
            width: 100px;
            height: 100px;
            border: 1px solid red;
            display: inline-block;
        }
    </style>
</head>
<body>
<div>div块元素</div>
<span>span行内元素</span>
</body>
</html>

```

