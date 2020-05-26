# HTML

```
HTML ：指的是超文本标记语言 (Hyper Text Markup Language) www万维网的描述性语言
```



# 网站的建站流程

```
注册域名--租用空间--网站建设（1确定网站主题 2搜集资料 3规划网站 4制作页面）--网站推广--网站维护
```



# 文件的命名规范

​     

```
     1.小写英文字母、数字、下划线的组合，
     2.其中不得包含汉字、空格和特殊字符；
     3.必须以英文字母开头。
```

# 网页组成

```
    结构：网页的结构部分            采用的是html编程
	表现：网页的样式               采用的是css编程
	行为：网页要实现的交互功能       采用的是javasrcipt编程
      其中html和css遵循W3C标准，Javasrcipt遵循ECMA标准
```

# head和body

```
head(头部）：描述区
body(主体）：内容区（所有在网页中显示的内容【图片、文字...】）
```

# html语法

```
 html标签： 长在 < 后面的第一个单词  叫做标签。分为两类标签：但标记、双标记
 双标记（常规标记）   <标签 属性="属性值" 属性="属性值">  </标签>
 单标记（空标记）     <标签 属性="属性值">	
 html属性：长在标签后面 以 空格 隔开的 属性
 属性和属性值之间，用 = 连接， 属性值放在""
 如果一个标签存在多个属性的清空下  属性和属性之间 用 空格隔开
```

# 一个标准的html项目初始化

<!DOCTYPE html>
<!-- 声明文档类型 -->
<html lang="en">
<!-- html为根标签：html语言...     lang="en" 语言-->
    <head>
        <!-- 描述区 -->
        <meta charset="UTF-8">
        <!-- charset="UTF-8"  控制编码格式  UTF-8国际性编码格式 -->
        <!-- 
            UTF-8国际性编码格式
            gb2312  /  gbk   中文简体
         -->
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <!-- 视口：禁止用户缩放 -->
        <meta http-equiv="X-UA-Compatible" content="ie=edge">
        <!-- 按照IE浏览器 edge 最新渲染模式  去 渲染页面 -->
        <title>test</title>
        <!-- title标签  当前网页的标题！显示在状态栏 -->
    </head>
    <body>明天会更好 </body>
</html>	

# 文本标题标签h1-h6

```
    特点：有默认样式：文本会加粗、字号不一样
    h1标签是比较特殊的：唯一性，在单独页面里面只能出现一次，放网站logo
    h2-h6 : 板块的标题、一段叙述性文本的标题。。。。。。
    需要注意的问题：h1 ~ h6  不能嵌套 它们是同一等级的
```

# 文本的加粗 & 文本的倾斜

    加粗：<b></b>       <strong>语义化：表示强调</strong>
    倾斜：<i></i>       <em></em>
# 下划线、水平线、换行符

    <u></u>
    <hr/>
    <br/>
# 段落标记

    <p></p>
    p标签是不能进行相互嵌套的，p标签里面不能嵌套h1 ~ h6
# span标签

```
    表示一个字符，或者某一小段文本
```

# 转义字符

    &nbsp;       不换行的空格
    &lt; &gt;    左右尖角号
    &copy;       备案图标
# div

```
div称为块或容器标签 作用：划分网页结构
```

# 列表

    无序列表(ul)：默认情况下，每一个li前面都存在一个列表符号（实心圆点），它主要运用在新闻列表、页面的主导航中
    有序列表(ol)：列表符号默认为数字，可以更改列表符号如：
       	 type="a"
       	 type="A"
       	 type="i"
       	 type="I"
    	还可以利用start属性设置属性值开始标志   注意：属性值只能为数字
    自定义列表(dl): 在网页中常看到，它包含两个标签dt、dd
        <dt>名词！</dt>
        <dd>对名词的解释</dd>
# 超链接

    a标签的属性：
        href="url"  作用：跳转地址
            <a href="#">新闻</a>   //空连接，使其返回最顶端 
            <a href="###">新闻</a> == <a href="javascript:void(0)"></a> //空连接，不会跳转 （用来模拟一个按钮）
        target="" 属性值：
            _self   默认值：在当前窗口打开
            _blank  新建一个窗口打开目标地址
        title=""  属性（不仅仅使用在a上面。大部分标签都支持） 做提示信息
     实现新闻列表的结构：
        <ul>
            <li>
                <a href="#">新闻内容新闻内容新闻内容新闻内容</a>
            </li>
            <li>
                <a href="#">新闻内容新闻内容新闻内容新闻内容</a>
            </li>
            <li>
                <a href="#">新闻内容新闻内容新闻内容新闻内容</a>
            </li>
        </ul>
    超链接默认的样式：文字为蓝色、下划线
# img属性

    src="图片的url(地址)"   必须存在
    alt=""                 必须存在
        alt属性的作用：
            1.文本替换图片（当图片加载不出来的时候，显示alt里面的文本）
            2.搜索引擎检测不到图片里面的文本，会查找alt里面的文本（seo优化）
    title="" :
        title属性的作用：
            a:提示文本
            b:当作图片的一个小标题
     width=""   控制图片的宽度
     height=""  控制图片的高度
     border=""  给图片添加边框
# 相对路径

    1.明确操作的文件在哪
    2.明确目标人物在哪
    ./     当前路径（操作文件所在的路径）
    相对路径的写法：
        1：同级找同级文件   ./直接写目标文件名称
        2：父级找子级       ./文件夹的名称/目标文件
        3：子级找父级       ../     返回上一级
# 表格的实现

    表格的作用  显示数据
    表格标签：table 表格 tr 行 td 列 
    表格的属性：
        width=""  宽 （table上面添加  整个表格的宽，如果添加在td上 每列的一个宽）
        height=""  高
        border=""   添加边框
        bordercolor=""   边框颜色
        cellpadding=""    内容距离边框的一个间距 单元格和内容间距的
        cellspacing=""    边框与边框之间的间距 控制单元格和单元格间距的属性
        align=""    水平对齐方式  属性值：left  right  center
        valign=""   垂直对齐方式  属性值：top  bottom  middle
    单元格的合并：
        跨行合行 跨列合列
        行合并： rowspan="合并的单元格的数量"
        列合并： colspan="合并的单元格的数量"
        注：无论合并行 还是 合并列 都是给td添加属性，和谁合并就删除谁
## 表格css属性补充	

```
	1.相邻边框合并

​					border-collapse:;   添加在table上面

​							属性值：

​								separate   分开（默认值）

​								collapse 合并	
```

```
	2.相邻边框之间的间距

​								border-spacing:  (添加在table上)
```

```
3.当表格没有内容的时候，是否显示边框区域

​					empty-cells:

​						属性值：

​								hide(默认值)

​								show
```

```
	4.控制表格宽度的方法

​					table-layout:

​						 属性值：

​								auto(默认值)  

​									auto的显示状态：值为auto：趋于平均分配，如果添加内容，根据里面内容的多少，再来分配td的宽度，

​									优点：布局灵活

​									弊端：性能消耗，必须先确定内容量，再来分配宽度

​								fixed(固定)

 									fixed的显示状态，趋于平均分配，不会受到内容的影响，如果单独设置宽度，宽度是可以变化的。

​        							优点：性能消耗较少。

​        							弊端：布局不灵活。
```

```
注：table添加padding不需要减，把td挤小
```

## 表格补充

####  数据行分组

```html
/*重点*/
<thead></thead>
<tbody></tbody>
<tfoot></tfoot>
```

####  数据列分组

```html
<colgroup span="value"></colgroup>
<!--span属性为把几列分为一组-->
```

####  列标题

```html
<th></th>
```

#### 表格标题

```html
<caption></caption>
```

## 表格标签的补充

```
  1 ： p标签不能进行互相嵌套

  2 : p标签里面不能嵌套h1 - h6

  3 : h1 - h6 之间不能进行互相嵌套

  4 : 块状元素一般做为块状或者内联元素的父元素。
```

# 表单

```
1.表单 表单的作用：收集数据（收集用户信息）表单用 form 表示
    form属性：
        action=""           接口（表单提交的路径）
        method="get/post"   数据提交的方法。
        name=""             表单的名称
    form控件：
        大部分通过input标签来实现
            input的属性：
                type=""     控制input显示类型（输入框、按钮、提交按钮、单选按钮）
                value=""    根据type类型的不同，作用也是不一样的。
                    value属性在文本框的作用：提示信息、记录文本的框的值
                    value属性在按钮里面的作用：更改按钮的文本
                name=""      表单控件的名称
                maxlength=""  能输入的最大长度
                size=""      控件的大小( 以字符为单位 )
```

        文本框（输入框）
            <input type="text">
        密码框
            <input type="password">
        空按钮
            <input type="button">  
        重置按钮
            <input type="reset">
        提交按钮
            <input type="submit">
    1）单选按钮组
    <input type=“radio” name=“ral” />男
    <input type=“radio” name=“ral”
    checked=“checked”/>(默认选中)女
```
2）复选框组
    <input type="checkbox" name="" />
    <input type="checkbox" name="" disabled="disabled" />
     *  disabled="disabled" (禁用)
     *  checked="checked"   (默认选中)
3）下拉列表（菜单）：
	<select >
   		<option>下拉选项1</option>
   		<option>下拉选项2</option>
   		…………
	</select>
	表示下拉列表，name属性不是必须的
	默认选择项用selected属性；
4）表单域多行文本定义：
	语法:	<textarea name=""  cols=""  rows="" ></textarea>
	多行文本。rows属性和cols属性用来设置文本输入窗口的高度和宽度，单位是字符。
	阻止浏览器对窗口的拖动设置:{resize:none;}（css属性）
5)上传文件：
	语法：<input type="file">
```

## 表单标签

```
1）表单字段集
语法：<fieldset></fieldset>

说明：相当于一个方框，在字段集中可以包含文本和其他元素。该元素用于对表单中的元素进行分组并在文档中区别标出文本。fieldset元素可以嵌套，在其内部可以在设置多个fieldset对象。disabled定义空间禁制可用；

2）字段级标题：
语法：<legend align="left/center/right/justify"></legend>
说明：legend元素可以在fieldset对象绘制的方框内插入一个标题。legend元素必须是fieldset内的唯一个元素。
3)提示信息标签：
语法：<label for="绑定控件id名"></label>

说明：label元素用来定义标签，为页面上的其他元素指定提示信息。要将label元素绑定到其他的控件上，可以将label元素的for属性设置为与该控件的id属性值相同。
```



# CSS

        1:什么是css？css作用是什么？？
            全拼：cascading style sheet （ 层叠样式表 ）
            作用：css做页面渲染，让网页看起来漂亮一点。
            css最新的版本：css3.0
        2:html + css ???????
            有利于优化
        3：css语法：
            注：所有的css语句，都要放在css样式表里面！！！
            css语法的组成：
                选择符 （ 选择的是要做渲染的标签 ）
                声明（具体渲染成什么样式）
                    声明又分为：属性 和 属性值。
            css语句的实现：
                语法规则:
                    选择符 { 属性：属性值 ; }
                    选择符{ 属性 ： 属性值1 属性值2 属性值3 ;}
                语法说明：
                    css里面所有的声明必须放在 {} 里面。
                    属性和属性值之间用：连接
                    每个声明后面要添加 ;
                    如果一个属性有多个属性值，属性值与属性值之间用空格隔开
# css样式

```
3.css样式表分别是内部样式表、外部样式表、内联样式表（行内样式、内嵌样式）
    内部样式表:
        用style标签 创建内部样式表, 最好把内部样式表放在head标签里面!
```

        语法:
            <style type="text/css">
                css语句
            </style>
        为什么style放在head里面?
            a:加载顺序:先让浏览器下载样式.
            b:body为内容区,head描述区. 把样式表放在描述区.
    外部样式表:
        自己去创建一个css文件( 外部样式表 )
        怎么导入外部样式表??
            第一种方法:
            <link> 
                属性:
                    rel="stylesheet"   建立关联性
                    href="url"         导入css样式表的路径
                    type="text/css"    定义类型(可以省略)
            
            第二种方法:
            <style>
                @import url("css的路径");
            </style>
    内联样式表:
        语法:
            <标签 style="css内联样式表"></标签>          
    link  && @import   区别:
        1:本质上的差异: 
            link属于html标签
            @import 属于css提供的一个方法.
        2:加载顺序:
            link导入的css 和 html结构同时加载.
            @import 等待所有的结构加载完毕 再 加载css.
        3:兼容方面:
            link的兼容性比较好.
        4:js 控制dom的差别
            @import导入的css样式,js动态控制样式的时候,会失效
# 样式表的权重

    内联样式表权重最高.
    内部样式表和外部样式表的权重,后写的会覆盖前写的.
    覆盖的只是相同样式（不同样式会继续执行） 
# css的层叠性（ 样式表的权重 ）

```
当给同一元素多次设置样式时，会出现权重问题，优先使用权重较高的样式，层叠指的是样式的优先级，当产生冲突以优先级高的为准
```

# 样式表体现css的层叠性

    css层叠性：
        样式产生冲突，按照权重大的样式执行
        不冲突的样式，正常执行
    权重问题：
        内联样式表的权重大
        后写的覆盖前写的（相同样式）
    例：
        爸爸说：快点起床 -> 学习了
        妈妈说：快点起床 -> 出去玩耍
        爷爷说：多睡会
    css层叠性面试题：
        题干：
            html结构： <div style="width:1000px;border:1px solid pruple;"></div>
    
            head标签里面的css样式如下：
                <head>
                    <link rel="stylesheet" href="./style.css">
                    <style>
                        /*内部样式表*/
                        div{ width:300px;background:blue; }
                    </style>
                </head>
    
            style.css里面的代码如下：
                div{
                    height:500px;
                    background:orange;
                }
    
        问题：该div再浏览器上执行的样式：
                width:1000px;
                border:1px solid pruple;
                background:blue;
                height:500px;
            
        分析：
            比较三个样式表的权重: 内联样式表的权重最高           
# 页面外围结构

    写页面的顺序：
        先划分上、下的结构 然后再划分左右结构 从外往里写
    把html标签区分：
        能不能给标签起名字，给标签颁发一个名字
            起名字的方法：
                小写的英文字母开头
                字母数字下划线连字符的组合
                语义化：名字尽量反应内容板块的作用和用途
                下划线：
                    以新闻页面为例
                        news_left
                        news_right
                        news_center
                连字符：
                        news-left
                        news-right
                        news-center
                驼峰式命名法：
                        newLeft
                        newRight
                        newCenter
                注意：
                    每个项目命名风格保持一致
                    起名字不能使用关键字（所有的标签和属性都属于关键字）
# css选择器

    最基本的选择符：
        3.1 类型选择符（标签选择符）
            说明：所有html标签都能当作选择符来用
                例如：html\body\div\p\span\....
            特点：选择页面中所有当前元素（div 选中页面中所有的div）
            作用：
                a.想统一某个标签样式的时候
                b.想清除某个元素默认样式的时候
        3.2 id选择符
            语法：
                <标签 id="自己起的名字"></标签>
                css用id写样式
                    #名称{css样式}
            特点：id是唯一的，在同一页面内，只能出现一次
            作用：id名称用作网页外围结构的搭建
        3.3 类选择符（class选择符）
            语法：
                <标签 class="名称"></标签>
                css用class写样式
                    .名称{css样式}
            特点：
                a.一个标签可以拥有多个class名称
                b.class可以重复使用
            作用：更适合定义类样式
        3.4 包含选择符（后代选择器、父子选择器）
            说明：根据父元素找子元素
            语法：
                父元素选择器 子元素选择符{给子元素写样式}
        3.5 群组选择符
            语法：
                把多个选择符以逗号分割的的形式组成一组，并对当前整个组写样式
                选择符1，选择符2，选择符3，.....{css样式}
        3.6 通配符
            *
            说明：选择页面中所有的标签
            作用：清除内填充和外边距（暂时用法）
            *{ 
                padding:0;  /*盒子的内填充*/
                margin:0;   /*盒子的外边距*/
            }
        3.7 伪类选择器
            a:link{color:red}           /* 未访问的链接状态*/
            a:visited{color:green}      /* 以访问的链接状态*/
            a:hover{color:gray}         /* 鼠标滑过的链接状态*/
            a:active{color:yellow}      /* 鼠标按下去的链接状态*/
            常用的方法：
                a{color:black;}
                a:hover{color:yellow;}
                注：做hover的交互效果：能够实现自身样式的改变，以及子元素样式的改变
                    无法对父元素做样式的改变
# 选择符的权重

    id选择符（100）>class选择符（10）>标签（类型选择符）（1）
    包含选择符的权重：是多个选择符的权重之和
    通配符的权重 0：不参与权重比较
    伪类选择符：10
    群组选择符：权重不发生变化，后写的会把前写的覆盖   （群组选择符权重不会相加，保持自身）
    如果权重相同的时候，后写的样式会把前写的样式覆盖掉
    内联样式表：1000
    注：！important     权重是最高的（最重要的）
        语法：加在样式属性值后面
# css层叠性

    提到层叠 必然权重
    内联样式表权重大于内部和外部样式表
    id > class > 标签
    ！important     (权重最高 优先执行)
    开发者样式(程序员) > 读者样式(用户) > 浏览器样式
# css作用：渲染页面

    怎样让内容居中显示
        margin:让6个板块在网页内左右居中
        用法：margin:0 auto
    css语法：
        选择符：{属性：属性值：}
        属性值：常规属性值、法定属性值
            常规属性值：300px
            法定属性值：官方提出某一单词，单词代表某一个意思
# 文本属性

```css
2.1 文本大小的设置
    font-size:
        a.系统为了统一文本大小，规定文本默认大小
        b.文本大小在设置的时候,一定设置成偶数（别低于12px)
        c.文本大小在设计图里面的获取，量文本的高度即可
        d.em 相对大小，根据父元素font-size的值而定
            例如：父元素font-size的值而定
                默认值情况下：1em == 16px
            em其他应用：
                line-hegiht(行高)
                line-height:2em;    (根据自身font-size的值确定)
            在设计图里面行高怎么获取：从一行的顶端到下面一行的顶端
        e. pt 磅 一般用在印刷领域
                9pt == 12px
        f.使用法定字号
            xx-small =9px
            x-small =11px
            small =13px
            medium =16px
            large =19px
            x-large =23px
            xx-large =27px
2.2 设置文本颜色
    color:
        颜色值：red pink black green yellow red gray white orange blue
        十六进制颜色值：
            0123456789abcdef
            #六位或者三位16进制数字
            0代表最暗的颜色 f代表最亮的颜色
        实现：#ffdd00   简写  #fd0
            ff 代表红色
            dd 代表绿色
            00 代表蓝色
        rgb模式
            rgb(245,245,245)
2.3 设置字体： （宋体、楷体、黑体...）
    为了统一文字间的差异：默认字体（微软雅黑）
    font-family:多个属性值的时候使用逗号隔开
        例：font-family:"宋体"
    系统能支持的字体：web安全字体
    font-family属性值是中文需要放在引号里面，英文字多个单词，也需要放在引号里面，一个英文字体的单词，不需要放引号里面
    如果存在中英文字体：先写英文再写中文字体
2.4 设置文本的加粗 font-weight
    属性值：
        bold        加粗
        bolder      更粗（系统显示的不明显）
        normal      恢复常规文本
        分成9个等级：
            100
            200
            ...
            900
        100-500 常规状态
        600-900 加粗状态
2.5 控制文本的倾斜 font-style
    属性值
        normal      恢复常规文本
        italic          文本倾斜
        oblique     文本倾斜
2.6 line-height:  行高
    a.在设计图上量取行高（第一行开始到第二行的顶端）
    b.当单行文本的line-height值 和 容器高保持一致，可使在容器中上下居中
2.7 text-align  文本对齐方式
    属性值：
        left
        right
        center
        justly  两端对齐
2.8 文本修饰属性  text-decoration:
    属性值：
        none        去掉下划线
        underline   下划线
        overline    上划线
        line-through    删除线
        blink       闪烁线
2.9 首行缩进  text-indent:
    text-intent:2em;
    text-intent:  （悬挂式缩进）
2.10 letter-spacing 字符间距
2.11 word-spacing 单词间距
2.12 text-transform
    属性值：
        capitalize  首字母大写
        uppercase   全部大写
        lowercase   全部小写
```
# css列表属性

```css
a.控制表符号：
    list-style-type:
        属性值：circle、square...
            list-style-type:none; 清除标识
b.list-style-image:url(图片的路径);
c.list-style-position:  列表符号的位置
    属性值：
        inside
        outside
e.list-style:none   去掉列表符  （常用）
```
# css背景属性 

```css
background  简写（复合式写法）
background-color：  背景颜色
backfround-image:url(图片路径)   背景图
    背景图的显示：
        特点：背景图是不占据空间的，跟随容器大小变化
        a.当容器大小 大于 背景图大小 平铺状态
        b.当容器大小 等于 背景图大小 只显示一张
        c.当容器大小 等于 背景图大小 只能显示容器的区域
背景图的显示状态：
    background-repeat:
        属性值：
            no repeat  不平铺
            repeat     平铺
            repeat-x   行向平铺  
            repeat-y   纵向平铺
背景图片的位置：
    background-position:
        属性值： （正值往下往右  负值往左往上）
        第一个值左右距离    第二个值上下距离
            可指定方位值：
                left(背景图左侧贴着容器左侧)   bottom（背景图贴着容器底部）
                right   top
                center  center 
        常用的简写形式：
            background:背景颜色 url(背景图) no-repeat center;
            扩展：
                background-attachment:
                背景图的固定：
                属性值 ： fixed、scroll
background和background-color的区别
	a. background可以设置背景颜色、背景图片、定位等。而background-color只能设置背景颜色
	b. 底色(background-color)是纯的色区。背景(background)，可以是纯色也可以是图案
	c. background的属性值是图片资源，而background-color的是颜色
```
# 浮动

    float属性
        属性值：
            left  坐浮动
            right  右浮动
            none  不浮动
    特点：
        重点注意：添加浮动的盒子，是不占据空间的
        同级元素横向排列，需要给当前所有的同级元素都添加浮动   
    注意：只要子元素有浮动，父元素必须有高度，否则会出现“高度塌陷”
# 边框

```css
a.用法：border:10px solid blue; (复合式写法)
b.属性拆分：
border-width:   边框大小
border-color:   边框颜色
border-style:   边框类型 
    solid 实线 
    dashed 虚线
    dotted 点状线 
    double 双线
    none 没有线条
c.单独一个方向设置边框：
    border-left: 20px solid organe;
    border-right:
    border-top:
    border-bottom:
d.
    border-width/color/style :
        属性值：
            1个值： 四周都添加边框
            2个值：上下 左右
            3个值：上 左右 下
            4个值：上 右 下 左
e:
    设置用边框画三角形：
        transparent 透明

注意：默认情况下边框是长在元素宽高之外、别用边框画结构
```
# 盒模型

```css
网页布局的基石：从盒子的内部到盒子的外围，
    内容 (图片、文字、视频、小盒子...)
    内填充 (补白)  （相当于盒子里面的泡沫）
    盒子本身(border) 
    外边距
盒模型具体的css属性：
    内填充：padding属性
        padding的用法：
            a.padding是长在 内容 和 盒子之间的距离
            b.padding是长在盒子里面的
            c.padding的作用：主要是控制元素在盒子内部的位置关系
            d.padding是添加在父元素上面
            e.padding可以把盒子撑大
                如果想让盒子保持原有的大小，需要在宽高的基础上减掉padding
                注：如果一个盒子没有固定大小（被内容撑开），添加padding不用减
            f.单一方向设置padding值：
                padding-left：
                padding-right：
                padding-top:
                padding-bottom:
            g.padding的设置方法：
                padding: 一个值  四周都padding
                padding: 两个值  上下  左右
                padding: 三个值  上  左右  下
                padding: 四个值  上  右  下  左
            h.padding不会对背景图的位置造成影响
            i.padding不能为负值
    外边距：margin属性
        用法：
            a.margin 是长在盒子外围的
            b.margin 控制当前元素 与 其他同级元素的位置关系
            c.margin 不会改变盒子内部的大小
            d.给元素的单一个方向设置margin值
                margin-left:
                margin-right:
                margin-top:
                margin-bottom:
            e.margin的设置方法：
                margin: 一个值  四周都margin
                margin: 两个值  上下  左右
                margin: 三个值  上  左右  下
                margin: 四个值  上  右  下  左
            f.可以为负值
            g.margin常出现的bug
                1.同级元素上下之间的margin值不会叠加，会重合，按最大值设置
                2.当父元素和第一个子元素都没有浮动，给第一个元素添加margin-top：会错误的把margin-top：添加在元素上面 
```



# **IFC**

```
IFC(Inline Formatting Contexts)直译为"内联格式化上下文"，IFC的line box（线框）高度由其包含行内元素中最高的实际高度计算而来（不受到竖直方向的padding/margin影响)
IFC中的line box一般左右都贴紧整个IFC，但是会因为float元素而扰乱。float元素会位于IFC与与line box之间，使得line box宽度缩短。 同个ifc下的多个line box高度会不同。 IFC中时不可能有块级元素的，当插入块级元素时（如p中插入div）会产生两个匿名块与div分隔开，即产生两个IFC，每个IFC对外表现为块级元素，与div垂直排列。
那么IFC一般有什么用呢？
水平居中：当一个块要在环境中水平居中时，设置其为inline-block则会在外层产生IFC，通过text-align则可以使其水平居中。
垂直居中：创建一个IFC，用其中一个元素撑开父元素的高度，然后设置其vertical-align:middle，其他行内元素则可以在此父元素下垂直居中。

总结：
1.内部的盒子会在水平方向，一个个地放置；
2.IFC的高度，由里面最高盒子的高度决定；
3.当一行不够放置的时候会自动切换到下一行；
```



# BFC

```txt
BFC(Block formatting context)直译为“块级格式化上下文”。它是一个独立的渲染区域，只有Block-level box（块）参与， 它规定了内部的Block-level Box如何布局，并且与这个区域外部毫不相干。
```

# BFC的布局规则

```txt
一、内部的Box会在垂直方向，一个接一个地放置。
二、Box垂直方向的距离由margin决定。属于同一个BFC的两个相邻Box的margin会发生重叠（按照最大margin值设置）
三、每个元素的margin box的左边， 与包含块border box的左边相接触
四、BFC的区域不会与float box重叠。
五、BFC就是页面上的一个隔离的独立容器，容器里面的子元素不会影响到外面的元素。
六、计算BFC的高度时，浮动元素也参与计算
```

# 哪些元素或属性能触发BFC

```
根元素(html)
float属性不为none
position为absolute或fixed
display为inline-block, table-cell, table-caption, flex, inline-flex
overflow不为visible
```

# BFC的应用

```txt
1、自适应两栏布局
2、清除内部浮动
3、防止margin上下重叠
```



# 文本溢出

```
文本会换行

英文、数字不会换行

white-space:  空白空间的处理

​    normal：默认值，多余空白会被浏览器忽略只保留一个；

​    pre：空白会被浏览器保留；

​    pre-wrap：保留一部分空白符序列，但是正常的进行换行；

​    pre-line:合并空白符序列，但是保留换行符；

​    nowrap:文本不会换行，文本会在同一行上继续，直到遇到<br/>    标签为止;
```

```
overflow:  溢出属性

​    visible:默认值，内容不会被修剪，会呈现在元素框之外；

​    hidden：内容会被修剪，并且其余内容是不可见的；

​    scroll：内容会被修剪，但是浏览器会显示滚动条，以便查看其余的内容;

​    auto：如果内容被修剪，则浏览器会显示滚动条，以便查看其他的内容;

​    inherit：规定应该从父元素继承overflow属性的值。
```

```
拓展：

​        overflow-x : hidden; 当内容溢出的时候，显示垂直方向的滚动条
​        overflow-y : hidden;
 text-overflow  文本溢出是否显示省略号
        clip  不显示
        ellipsis   显示省略号
```

```
单行文本溢出省略号显示：

​    1：不让文本换行：
​      white-space:nowrap;
​    2: 让超出的文本隐藏
​      overflow:hidden;
​    3: 超出的文本省略号显示
​      text-overflow:ellipsis; 
​    4：宽度的设置！！！
​      width
```

# 元素类型

## 元素分类

```
HTML里面 标签分为几类：
        单标记   双标记
根据css显示分类，XHTML元素被分为

三种类型:
	块状元素，内联元素（行内块元素放在内联元素这一大类里面），可变元素 <button>按钮</button>

&&

三种类型：	
	块状元素，内联元素，内联块元素(争议点：内联块状元素自己属于一类 || 属于内联一类)（css 2）
```

## 各种元素类型的特点

```
 一：块状元素特点（默认情况）：

​      1：块状元素，在页面中以矩形区域显示！

​      2：块状元素，能直接添加宽高！

​      3：块状元素，在页面显示，自上而下排列，独占一行。

​      4：块状元素，一般座位内容或者其他元素的容器！

​    二：内联元素特点（默认情况下）：

​      1：内联元素，不能设置大小，由内容撑开，最小单位也是矩形

​      2：内联元素，在一行内逐个显示

​      3：内联元素也支持盒模型的规则，但是个别属性不能正确显示,

​        例如（padding-top/bottom  margin-top/bottom）

​    三：可变元素： button

​      根据布局流的规则，生成块或者是内联
  行内块元素：
        display:inline-block;
        特点：
            a:能直接设置宽高
            b：在一行内逐个显示。
            c: inline-block的元素 支持 vertical-align 属性
        vertical-align 
        	属性  垂直对齐方式 
        		 middle 居中对齐
        top
        middle
        bottom
    典型的行内块元素？？？？？
        input  （默认值：inline-block)
        img	（默认的是 inline 但是特点和inline-block 相匹配）
        select
        ...
```

## 常见的块状元素

```
    div -最常用的块级元素

​    dl - 和dt-dd 搭配使用的块级元素

​    form - 交互表单

​    h1 -h6- 大标题

​    hr - 水平分隔线

​    ol – 有序列表

​    p - 段落

​    ul - 无序列表

​    li

​    fieldset - 表单字段集

​    colgroup-col - 表单列分组元素

​    table-tr-td 表格及行-单元格
```

## 常见的内联元素

```
    a –超链接（锚点）                

​    b - 粗体(不推荐) 

​    br - 换行               

​    i - 斜体

​    em - 强调               

​    img - 图片             

​    input - 输入框        

​    label - 表单标签         

​    span - 常用内联容器，定义文本内区块

​    strong - 粗体强调

​    sub - 下标  

​    sup - 上标

​    textarea - 多行文本输入框

​    u - 下划线

##     select - 项目选择 
```

## 元素类型的转换

```
  display属性:

​    检索或者设置元素所生成的盒模型类型！

  display的属性值：

​    a: display:block

​      作用：让元素转成块状元素，拥有块状元素的特点

​      大部分块状元素的display的默认值：block

​    b: display:inline

​      作用：让元素转成内联元素。

​      大部分内联元素的display的默认值 inline
     c: display:none;
        作用：隐藏该元素，在页面中不占据空间

     d: display:list-item:
        li的默认值，带有列表符号。、
    
     e: display：inline-block;
        input的默认值
 a: 默认情况下：大部分块状元素的display的默认值 block;
            其中 li 的默认值 list-item ( 列表元素 )


b: 默认情况下：大部分内联元素的display的默认值 inline;
            其中 input的默认值 inline-block  ( 内联块元素 /行内块元素 )
```

## 元素上下、左右居中问题

一、方法

​	给父元素添加display:flex; 给子元素添加 margin:auto;

二、方法

让子元素在父元素中左右居中 (margin:0 auto) 注：上下居中实现不了  auto auto（错误写法）

图片元素很特殊  给父元素添加  text-algin:center 可以实现左右居中

​	1.如果子元素是  dispaly:inline-block  就可以实现给父元素 添加 text-algin:center 可以实现左右居中

​	2.因为vertical-align 属性 对齐按照 顶线 中线 基线 底线

​	3.添加一个“标尺”用来确定 顶线 中线 基线 底线

​	4.因为要做上下居中 中线对齐： 标尺得高 和 父元素的高 保持一致

实现流程:

​	1.左右居中：

​		a.	给父元素添加text-align:center;

​		b.	保证子元素为inline-block

​	2.上下居中：

​		a.	添加“标尺” -> 确定 顶线 中线 基线 底线

​			   添加标尺 在子元素的后面添加同级元素span 并且 不能有回车

​        b : 必须保证 标尺 inline-block -> 标尺和子元素在同一行。

​        c : 给标尺确定中线 添加属性 vertical-align:middle;

​        d : 给标尺设置width:0;height:100%;

## 为什么图片能直接加宽高（面试题）

图片默认的display为inline,

解：

​	因为图片是“置换元素”，

​	因为浏览器在渲染置换元素的时候生成一个框，这个框可以设置大小

置换元素和非置换元素

​	置换元素：标签根据标签或者属性。来确定在页面中的显示状态

​		img input select

​	

## 新闻的图片(图片会往下撑3px 将它设置元素类型为 block)  绝对是 img 导入的（它是占空间的）   不是背景（背景图片是做渲染的）

## 定位铺垫

```
教室里调换座位

  		1. 起立离开当前的座位
  		2. 找参照物（教室）
  		3. 二排四列
```

## 定位

​	

```
定位属性： position

​			作用：检索或者设置元素的定位方式（改变元素位置的属性）

​	 定位的步骤：

​			1.给元素添加padding属性，证明该元素要做位置的变化。

​			 2.确定参照物	（通过psition的属性值来确定：

​			 static\absolute\relative\fixed\sticky)

​			 3.确定坐标:  left  right  top   bottom

 	position的属性值 （来确定定位方式【参照物】）；

​		a. static  静态定位：

​				position的默认值，默认文本流的状态

​				不会识别left  right  top  bottom指定的指标

​		 b. absolute 绝对定位：

​				参照物：按照已经有定位的父元素进行位置的变化。

​				假如 当前没有父元素 或者 父元素没有定位的情况下，以整个文档为参考物

​			     绝对定位，脱离文档流(margin:auto无效）、不占据空间

​		 c. relative 相对定位

​				a. 参照物： 自身默认的位置

​				b.始终占据空间，不会脱离文档流，
```



```
 包含块的设置：

​    		1：如果父元素为参照物：添加 position:relative;

​    		2: 给要做定位的子元素 添加position:absolute;
```

# 锚点的实现

```
 锚点：

​    超链接的一种：实现在单一页面内，不同位置的跳转。



  语法：

​    <标签 id="锚点名称"></标签>

        <a href="#锚点名称"></a>
```



## 定位元素的层级关系

```
 定位元素：

​      	后定位的元素会把前面定位的 盖住。

​     z-index:

​      	控制定位元素的层次关系

​      	属性值为一个数字（可以为负数），数字越大，层次关系越高
```

## 宽高自适应

  

```
宽度自适应：

​    当块状元素的宽 不设置 或者 width:100%;

​    当前元素跟随父元素发生变化
```

```
  高度自适应：(两种自适应的情况)

​      当height不去设置，或者设置 height:auto;

​      当前容器的高是被内容撑开的。
```

```
 第二种情况

​	让子元素跟随父元素高度变化

​	父元素必须有高度，，然后给子元素设置height:100%;

需求：让一个元素在浏览器窗口铺满

​			html,body{

​						height:100%

}

​	
```



```
 注：怎么分析是否应用高度自适应：

​    后期板块内是否会发生一些数据增或者减。
```

 

```
 第一种高度自适应需求： 

​    BUG1 : 内容增多，内容的容器固定，内容超出。

​    BUG2 : 当内容过于减少或者是没有内容的时候，容器的高特别小。

​    目标1： 内容增多，内容把高度撑开

​    目标2： 当容器中的内容偏少或者没有内容的时候，设置一个最小高度。
```

  

```
需求总结：

​    1：当内容增多的时候，让内容把容器撑开。

​    2：当内容减少的时候，让容器保持最小高。
```

```
  最小高度的设置 :

​    min-height:; 最小高度!!!!!
```

 

```
  说明: 

​    现代高版本浏览器(不包括ie8以下)解析min-height的时候:

​    如果一个元素设置min-height: 让当前元素保持一个最小高度,

​    如果超出最小高度容器会被内容撑开,如果内容不超出,或者没有内容

​    容器会保持min-height设置的最小高度.
```

## 元素类型&定位规则

### 元素嵌套规则

​	1.p标签不能进行互相嵌套

​	2.p标签里面不能嵌套h1-h6

​	3.h1-h6 之间不能进行嵌套

​	4.块状元素一般为块状或者内联元素的父元素

### 绝对定位对css属性的影响

​	position:absolute:

​		1.margin:0 auto;   不起作用

​		2.flaot不起作用

​		3.如果一个元素没有设置宽度，并且添加了绝对定位，元素宽是内容撑开的宽。

## IE低版本最小高度的设置

```
  min-height:;  IE6是不支持的!!

  IE6不支持min-height:;但是 ie6 默认的就把height解析成最小高度了!

  如果min-height 和 height同时设置,高版本浏览器会解读height!

  问题解决:

​    不让高版本认height 只加载min-height;

​    让IE6认识height
```

```
过滤器:

​    1: ie6过滤器 下划线过滤器

​      语法:_属性:属性值;

​      只有IE认识带有下划线的属性.


​    2: !important 权重控制

​      IE6不认识!important;


​    3. *属性过滤器
```

当在一个属性前面增加了*后，该属性只能被IE7浏览器识别，其它浏览器混略该属性的作用。

     语法：选择符{*属性：属性值；}
    
    \4.  \9 ：IE版本识别；其它浏览器都不识别
    
    语法：选择符{属性：属性值\9;}
    
    \5.  \0 :  IE8 及以上版本识别；其它浏览器都不识别

  如果考虑低版本IE6兼容:

  第一种方法:

    min-height:300px;
    
    _height:300px;

  第二种方法:

    min-height:300px;
    
    height:auto!important;
    
    height:300px
## 高度塌陷

```
 高度塌陷出现的场景:

​    如果子元素设置了浮动,父元素没有设置高度,父元素会出现高度塌陷!

  解决高度塌陷的方法:

​    1:给出现高度塌陷的父元素 添加overflow:hidden;

​    原理:overflow:hidden 触发了BFC;

​      bfc规定:计算BFC高度的时候,里面浮动元素也参与计算!

​    弊端:overflow:hidden 溢出隐藏 会隐藏掉定位在当前元素以外的内容.
	 2.在浮动元素的下面添加一个空元素
	 	并且在给空元素设置{clear:both}   //清除浮动  闭合浮动
	 	弊端：会出现很多没有意义的空元素，形成代码的冗余
	 3.万能清除法
	 	高度塌陷的元素：：after{
            content:".",
            display:block;
            clear:both;
            height:0;
            overflow:hidden;
            visibility:hidden;
		 }	
```

##  伪对象选择器:

```
	 ::after{}
		 	在元素的最后添加内容
		 	配合属性content使用
		 ::before{}
		 	在元素的之前添加内容
		 	配合属性content使用
		 ：first-letter
		 	第一个字符
		 ：first-line
		 	第一行字符
```

## 隐藏元素

```
	隐藏单个元素的方法

​		display:none   彻底隐藏 不占据空间

​		visiability:hidden；隐藏元素，占据空间
```



## 清除浮动

```
	属性：clear:

​					both(左右浮动)

​					left

​					right
```

# css3

```
 很多css3属性：还是最初的预览版，没有形成一个最终的正式版。

​    造成了很多属性，浏览器不兼容。

​    浏览器为了能使这些属性兼容，每个浏览器商，提供属于自己的浏览器的语法规则。

​    浏览器前缀。
```



```
 主流浏览器：

​    谷歌、火狐、苹果、欧鹏、ie


  浏览器前缀:

​    -webkit-     谷歌浏览器

​    -moz-      火狐浏览器

​    -ms-       IE浏览器

​    -o-       欧鹏浏览器

  css3属性在设置的时候:
   css3属性：文本阴影 
                text-shadow : 属性值1 属性值2 属性值3 属性值4
                    属性值1 ： 阴影的水平方向的位置
                    属性值2 ： 阴影的垂直方向的位置
                    属性值3 ： 阴影的大小
                    属性值4 ： 阴影的颜色

​    兼容模式

​      -webkit-text-shadow:5px -1px 5px #5361a9;

​      -moz-text-shadow:5px -1px 5px #5361a9;

​      -ms-text-shadow:5px -1px 5px #5361a9;

​      -o-text-shadow:5px -1px 5px #5361a9;

​    标准模式:

​      text-shadow:5px -1px 5px #5361a9;
```

## 优雅降级和渐进增强

为了适用不同的版本，前端开发的时候，一般会有两个思路:

- 优雅降级，
- 渐进增强；

## **优雅降低**

就是按照支持度最高的浏览器标准来写代码，一般是以chrome为准，对于技术支持较旧的浏览器，只要不影响使用都可以不处理（比如圆角效果border-radius在低版本IE中是没有圆角效果的，但却并不影响正常阅读，那就不管了），如果有功能方面在低版本无法正常，就做低版本的兼容，比如兼容到IE8/IE6；我自己走的路线是优雅降级；

## **渐进增强**

是以技术支持最低的浏览器为准，假设以IE6为准(如果兼容到IE8，就以IE8为准)，写的代码在IE6/8中没问题后，在补充一些高级浏览器支持的效果；

广义来说，其实要定义一个基准线，在此之上的增强叫做渐进增强，在此之下的兼容叫优雅降级。这个基准线对于我，是允许使用javascript、cookie和css的IE8浏览器。

不过狭义而言，渐进增强一般说的是使用CSS3技术，在不影响老浏览器的正常显示与使用情形下来增强体验，而优雅降级则是体现html标签的语义，以便在js/css的加载失败/被禁用时，也不影响用户的相应功能

## 线性渐变

 

```
线性渐变：

​    语法：

​      background: linear-gradient(direction, color-stop1, color-stop2, ...);

​      说明：

​      direction：默认为to bottom，即从上向下的渐变；
```



 

```
   1：单一方向的渐变：

​      to left   到左侧

​      to right   到右侧

​      to top

​      to bottom

​    2: 对角渐变

​      to left top 

​      to right bottom

​    3: 角度的渐变

​      10deg   10度

	4：重复性渐变
	
	 repeating-radial-gradient：();
```

```
    注：颜色默认情况下趋于均分

​      如果颜色后面带有百分比，按照百分比进行色彩的渐变

​      例如 red  10%     到10% 都是红色

​    注：

​      linear-gradient（）颜色的分布方向，标准模式 和 兼容完全相反！！

​      带有浏览器前缀的兼容模式，方向是不加to  从哪个方向开始
```

## 径向渐变

```
径向渐变：（一定要添加浏览器前缀）

​    线性渐变从一个方向到另一个方向

​    径向渐变从一个点向四周的渐变
```

```
  语法：

   background: radial-gradient(center, shape, size, start-color, ..., last-color);

​    center参数：渐变点的位置

​        left bottom  在左下角

​        10px  20px  离左侧10px  离上边20px

​    径向渐变的大小：

​      最远角 farthest-corner （ 默认大小 ）

​      最远边 farthest-side

​      最近角 closest-corner

​      最近边 closest-side
```

```
    说明：

​    center：渐变起点的位置，可以为百分比，默认是图形的正中心。

​    shape：渐变的形状，ellipse表示椭圆形，circle表示圆形。默认为ellipse，如果元素形状为正方形的元素，则ellipse和circle显示一样。

​    size：渐变的大小，即渐变到哪里停止，它有四个值。 closest-side：最近边； farthest-side：最远边； closest-corner：最近角； farthest-corner：最远角。
```

## css过渡

 

```
css3过渡属性：

​    \1. transition-property：检索或设置对象中的参与过渡的属性

​    \2. transition-duration：检索或设置对象过渡的持续时间

​    \3. transition-delay：检索或设置对象延迟过渡的时间

​    \4. transition-timing-function：检索或设置对象中过渡的动画类型
```

​    

```
 简写方法：

​     transition: 属性值1 属性值2 属性值3 属性值4

​      属性值1： 需要参与过渡属性  all ( 能支持过渡属性的都会过渡变换 默认值)

​      属性值2： 过渡的时间  s秒  ms 毫秒

​      属性值3： 延迟的时间  s秒  ms 毫秒

​      属性值4： 

​        动画的类型（匀速、匀加速、匀减速........）

​        linear  匀速
```

 

```
 注：transition 必须通过鼠标事件触发（鼠标滑过  ）
```

# css3-2d

```
二维的平面空间2D变换，是在一个平面对元素进行的操作。可以对元素进行水平或者垂直位移、旋转或者拉伸.
```

​		变形属性：transform

​		2d的变换：

## 				在平面进行位置的移动		transform:translate()

```
将元素向指定的方向移动，类似于position中的relative。

​						水平移动：向右移动translate(tx,0)和向左移动translate(-tx,0)；

​						垂直移动：向上移动translate(0,-ty)和向下移动translate(0,ty);

​						对角移动：右下角移动translate(tx,ty)、右上角移动translate(tx,-ty)、左上角移动translate(-tx,-ty)和左下角移动translate(-tx,ty)。
```

## 				在平面进行缩放					transform:scale()	

```
让元素根据中心原点对对象进行缩放。默认的值1。因此0.01到0.99之间的任何值，使一个元素缩小；而任何大于或等于1.01的值，让元素显得更大。

​						缩放scale()函数和translate()函数的语法非常相似，他可以接受一个值，也可以同时接受两个值，如果只有一个值时，其第二个值默认与第一个值相等。例如，scale(1,1)元素不会有任何变化，而scale(2,2)让元素沿X轴和Y轴放大两倍。

​						scaleX()：相当于scale(sx,1)。表示元素只在X轴（水平方向）缩放元素，其默认值是1。

​						scaleY()：相当于scale(1,sy)。表示元素只在Y轴（纵横方向）缩放元素，其默认值是１
```

## 				在平面旋转							transform:rotate()

```
	旋转rotate()函数通过指定的角度参数对元素根据对象原点指定一个2D旋转。它主要在二维空间内进行操作，接受一个角度值，用来指定旋转的幅度。如果这个值为正值，元素相对原点中心顺时针旋转；如果这个值为负值，元素相对原点中心逆时针旋转。

​						 rotateX() 方法，元素围绕其 X 轴以给定的度数进行旋转
​						 rotateY() 方法，元素围绕其 Y 轴以给定的度数进行旋转
```

## 				在平面倾斜							transform:skew()	

```
倾斜skew()函数能够让元素倾斜显示。它可以将一个对象以其中心位置围绕着X轴和Y轴按照一定的角度倾斜。
						一个参数时：表示水平方向的倾斜角度；
						两个参数时：第一个参数表示水平方向的倾斜角度，第二个参数表示垂直方向的倾斜角度
```

#   css3-景深

​    

```
观察物体的第一视角距离.

​    近大远小

​    perspective: 1200px;（一般都是在父元素中使用）

​    transform:perspective(1200px) （在子元素中使用）

​    两个都设置会发生冲突，建议只设置父元素，通常的数值在900-1200之间

​    如果当你的视线距离物体足够远的时候，基本上就不会有近大远小的感觉

​    视觉角度：

​      persperctive-origin:

​        left top

​        center center

​        50% 50%

​        0px 0px

  让当前形成一个3D舞台，让其子元素在3D空间里面进行一个变换。

​    transform-style:preserve-3d / flat(默认值：平面空间); 
```

# css3D

```
 形成一个3D空间：( 让父元素形成3D，让其子元素在3D空间进行变化 )

​    transform-style:preserve-3d

  2d场景，在屏幕上水平和垂直的交叉线x轴和y轴

  3d场景，在垂直于屏幕的方法，相对于3d多出个z轴

  Z轴：靠近屏幕的方向是正向，远离屏幕的方向是反向

  变形属性：

​    transform:
```

  3D功能函数：

  

```
  3D的位移：

​      transform:translate(x,y,z);

​        translateX()

​        translateY()

​        translateZ(不能是百分比)
```



```
   3D的旋转：

​      transform:rotate();

​        rotateX()

​        rotateY()

​        rotateZ() //默认情况效果类似

​        rotate3D(x,y,z,a)   [ 0不旋转。1旋转 ]

            - x：是一个0到１之间的数值，主要用来描述元素围绕X轴旋转的矢量值；
            - y：是一个０到１之间的数值，主要用来描述元素围绕Y轴旋转的矢量值；
            - z：是一个０到１之间的数值，主要用来描述元素围绕Z轴旋转的矢量值；
            - a：是一个角度值，主要用来指定元素在3D空间旋转的角度，如果其值为正值，元素顺时针旋转，反之元素逆时针旋转。
```



```
    3D缩放：

​      transform:scale3d(x,y,z);

​        scaleX()

​        scaleY()

​        scaleZ()
```



## 使背面不可见

​		backface-visbility:hidden;

## 变形原点

```
transform-origin
	transform-origin是变形原点，也就是该元素围绕着那个点变形或旋转，该属性只有在设置了transform属性的时候起作用；
	因为我们元素默认基点就是其中心位置，换句话说我们没有使用transform-origin改变元素基点位置的情况下，transform进行的rotate,translate,scale,skew等操作都是以元素自己中心位置进行变化的。
```

# css3动画

```
 transition:

​    过渡：

​      特点：需要事件进行触发。

  animation

​    动画：

​      特点：不需要事件进行触发。调用关键帧即可
```



```
制定关键帧：

​    @keyframes 关键帧的名称{

​      /*制定关键帧*/

​      /*from{}

​      to{}*/

​      0%{

​        //开始状态

​      }

​      25%{

​      }

​      50%{

​      }

​      ......

​      100%{

​        //结束状态

​      }

​    }
```

##   animation: 复合属性

```


​    animation-name  关键帧的名称

​    animation-duration  动画的持续的时间

​    animation-timing-function  动画运用的类型（匀速linear、加速度、减速度、贝塞尔曲线）

​    animation-delay 动画的延迟

​    animation-iteration-count  动画运动的次数（默认情况下运动1次） infinite(无限循环)

​    animation-direction 运动的方向

​        属性值：

​          \- reverse：反方向运行 （ 让关键帧从后往前执行 ）

​          \- alternate：动画先正常运行再反方向运行，并持续交替运行

​          \- alternate-reverse：动画先反运行再正方向运行，并持续交替运行

​    animation-play-state 

​        属性值：

​          paused暂停

​          running运动


  常用的写法：

​    animation:关键帧的名称 动画运动的时间 linear(匀速) 动画延迟的时间
```

```
  animation-timing-function:

​    动画的类型：

​      linear

​      ease

​      ease-in

​      step-start //没有动画中间的过渡效果。每次直接跳到下一帧开始的地方
```

# html5

## 		语义化结构标签：

​			

```
	section 		类似于div,section 更偏向划分区域

​				article			更偏向于 内容的展示

​				aside			  (在一边的，在一旁的，侧边)

​				header			表示内容的头部，网页的头部、头部区域

​				footer			 表示内容的底部,内容的底部、底部区域

​				nav				  导航链接、导航区域

​				flgure			   表示 一块独立的内容

​				figcaption		figure标题 （一般放在fgure的第一位或者最后一位）

​				    main    主体内容(IE不兼容)

​    				hgroup

​    				mark    高亮显示 默认北京为黄色（可以更改背景 内联元素）

​    				time    放时间的

​    				dialog   类似于微信的对话框 ( 默认display:none 默认定位 默认边框 )	
```

## 多媒体标签

  

```
video 视频

​    \- src属性:资源路径

​    \- controls属性：如果出现该属性，则向用户显示控件，比如播放按钮。

​    \- autoplay属性：如果出现该属性，则视频在就绪后马上播放。

​    \- loop属性：重复播放属性。

​    \- muted属性：静音属性。

​    \- poster属性：规定视频正在下载时显示的图像，直到用户点击播放按钮
```

```
 audio 音频

​    \- src属性:资源路径

​    \- controls属性：如果出现该属性，则向用户显示控件，比如播放按钮。

​    \- autoplay属性：如果出现该属性，则视频在就绪后马上播放。

​    \- loop属性：重复播放属性。

​    \- muted属性：静音属性。


```

```
 source标签:定义媒介资源

​    type属性:

​      视频:

​        用于视频：video/ogg  video/mp4   video/webm

​      音频:

​        用于音频：audio/ogg  audio/mpeg

​            也支持 wav
```

## H5增加的表单内容

```
 新增type类型

​    Type=“email”  限制用户必须输入email类型

​    Type=“url”    限制用户必须输入url类型

​    Type=“range”  产生一个滑动条表单

​    Type=“number”

​    Type=“search”  产生一个搜索意义的表单

​    Type=“color”   生成一个颜色选择的表单

​    Type=“time”   限制用户必须输入时间类型

​    Type=“month”    限制用户必须输入月类型

​    Type=“week”    限制用户必须输入周类型

​    Type=“datetime-local”    选取本地时间

​    type=”date”


```

```
  新增表单属性

​    required   监测是否为空。

​    min   最小

​    max   最大

​    step   步幅 确定一个法定值。 -3 0 3 6 9

​    autocomplete  是否自动提示信息  属性值  on  off

​    placeholder  文本框的提示信息

​    autofocus   自动聚焦。一个页面只能由一个。


​    pattern  后面的属性值是一个正则表达式。 

​            //手机号验证pattern="^1[3|5|8|7]\d{9}$"


​    novalidate   取消验证

​    multiple   选择（上传）多个文件


​    list   必须结合datalist标签，绑定datalist id名称。
```

```
H5增加的表单标签

​    <datalist></datalist>

​      给绑定id的list属性的元素，做提示信息的。

​    <output></output>

​      计算结果的输出，脚本的输出
```



## 渐进增强和优美降级

### 渐进增强和优雅降级概念出现的原因

```
翻看进度条，会发现渐进增强和优雅降级这两个概念是在 CSS3 出现之后火起来的。由于低级浏览器不支持 CSS3，但是 CSS3 特效太优秀不忍放弃，所以产生了的一种解决方式在高级浏览器中使用CSS3，而在低级浏览器只保证最基本的功能
```

### 什么时渐进增强和优美降级？

```
渐进增强（Progressive Enhancement）：一开始就针对低版本浏览器进行构建页面，完成基本的功能，
然后再针对高级浏览器进行效果、交互、追加功能达到更好的体验。

优雅降级（Graceful Degradation）：一开始就构建站点的完整功能，然后针对浏览器测试和修复。
比如一开始使用 CSS3 的特性构建了一个应用，然后逐步针对各大浏览器进行 hack 使其可以在低版本浏览器上正常浏览。
```

### 区别是什么？

```
优雅降级是从复杂的现状开始，并试图减少用户体验的供给，而渐进增强则是从一个非常基础的、能够起作用的版本开始，并不断扩充，以适应未来环境的需要。
```

### CSS3例子而言

```
就CSS3这种例子而言，我更加推崇渐进增强的写法。因为前缀CSS3的某些属性在浏览器中的实现效果有可能与正常的CSS3实现效果不太一样，所以最终还是得以正常CSS3为准。

​			例如CSS3中的 border-radius、background-image渐变

但是无论怎样将正常CSS3的写法放在最后总是好的。
```

### 个人总结

```
渐进增强相当于向上兼容，而优雅降级相当于向下兼容。
向下兼容指的是高版本支持低版本的或者说后期开发的版本支持和兼容早期开发的版本，
向上兼容的很少。大多数软件都是向下兼容的，
比如说Office2010能打开Office2007，Office2006，Office2005，Office2003等建的word文件，
但是用Office2003就不能打开用Office2007，Office2010等建的word文件！
现在有很成熟的技术，能够让你分析使用你客户端程序的版本比例。
如果低版本用户居多，当然优先采用渐进增强的开发流程；如果高版本用户居多，
为了提高大多数用户的使用体验，那当然优先采用优雅降级的开发流程。
例如：新浪微博网站前端的更新，拥有这种亿级用户的网站，绝对不可能追求某个特效而不考虑低版本用户可不可用，一定是确保低版本到高版本的可访问性，再去渐进增强，采用新功能给高版本用户提供更好的用户体验。但也不是没有反例。如果你开发的是一款面向青少年的软件（或网站），你知道这个群体的人总是喜欢尝试新事物，总是喜欢酷炫的特效，总是喜欢把它们的软件更新到最新版本（而不像我们老一辈的用户）。面对这种情况，渐进增强的开发流程实为上选。
```

# css属性选择器

```
  1: 选择符[属性名]         只要带有当前属性名就会被选中。

  2: 选择符[属性名="属性值"]     不仅制定属性名，有指定属性值

  3: 选择符[属性名~="属性值"]     属性值为一个词列表，只要包含当前词就会被选中

  4: 选择符[属性名^="属性值"]     属性值必须是当前指定的属性值开头的

  5：选择符[属性名$="属性值"]     属性值必须是当前指定的属性值结尾的

  6: 选择符[属性名*="属性值"]     属性值中只要包含了指定的字符就会被选中

  7: 选择符[属性名|="属性值"]     属性值仅是当前指定的属性值，或者是以属性值- 开头 （ left-con ）
```

```
结构性伪类选择器

 结构性伪类选择器：( 选择谁 选择符就行写谁 )

  如果子集标签类型一致（类名一致）的情况下：采用的是 child

​    1 : 选择符:first-child{ }

​    2 : 选择符:last-child{ }

​    3 : 选择符:nth-child(val){}

​      val : 

​        可以是某个数值 表示第几个

​        2n 或者 even    偶数

​        2n + 1 或者 odd  奇数

​    4 : 选择符:nth-last-child(){}  倒数第几个

​    5 : 选择符:only-child{}  当前子集只有一个元素的时候才会被选择
```



```
如果子集合标签类型不一致（类名不一致）的情况下：采用的是 of-type 

  of-type  先确定类型，把不同类型的先剔除。剩下同类的进行第几个选择。



​    1 : 选择符:first-of-type{ }

​    2 : 选择符:last-of-type{ }

​    3 : 选择符:nth-of-type(val){}

​      val : 

​        可以是某个数值 表示第几个

​        2n 或者 even    偶数

​        2n + 1 或者 odd  奇数

​    4 : 选择符:nth-last-of-type(){}  倒数第几个

​    5 : 选择符:only-of-type{}  当前子集只有一个元素的时候才会被选择

  拓展：

​    ：root  选择的是根元素 html

​    选择符:empty 当当前元素 没有任何 内容 或者 没有任何子元素的时候会被选中
```

# 元素状态伪类

```
 E:enabled

​    匹配所有用户界面（form表单）中处于可用状态的E元素

  E:disabled

​    匹配所有用户界面（form表单）中处于不可用状态的E元素

  E:checked

​    匹配所有用户界面（form表单）中处于选中( 单选、多选 )状态的元素E

  E::selection

​    匹配E元素中被用户选中或处于高亮状态的部分
```

# 动态伪类

```
 E:link

​    链接伪类选择器 

​    选择匹配的E元素，而且匹配元素被定义了超链接并未被访问过。常用于链接描点上

  E:visited 

​    链接伪类选择器

​    选择匹配的E元素，而且匹配元素被定义了超链接并已被访问过。常用于链接描点上

  E:active

​    用户行为选择器

​    选择匹配的E元素，且匹配元素被激活。常用于链接描点和按钮上

  E:hover

​    用户行为选择器

​    选择匹配的E元素，且用户鼠标停留在元素E上。IE6及以下浏览器仅支持a:hover

  E:focus

​    用户行为选择器

​    选择匹配的E元素，而且匹配元素获取焦点
```

# 层级选择器

```
    父元素>子元素{}  

​      说明：只能选择父元素的最近的一层子元素。


​    兄弟元素 + 兄弟元素{}

​      说明：通过当前的元素 选择符 离她最近的 下面的兄弟元素


​    兄弟元素 ~ 兄弟元素{}

​      说明：通过当前的元素 选择符 下面的所有的兄弟元素
```

# 文本阴影属性

```
    text-shadow:

​      属性值：

​        属性值1 : 阴影横向的位置

​        属性值2 : 阴影纵向的位置

​        属性值3 : 阴影的大小

​        属性值4 : 阴影的颜色



​    多阴影的设置：

​      text-shadow:-2px -3px 8px red,10px 10px 8px red
```

# 盒子阴影

```
  box-shadow:

​    h-shadow  必需的。水平阴影的位置。允许负值

​    v-shadow  必需的。垂直阴影的位置。允许负值

​    blur  可选。模糊距离

​    spread 可选。阴影的大小

​    color  可选。阴影的颜色。

​    inset  可选。从外层的阴影（开始时）改变阴影内侧阴影



  box-shadow:10px 10px 10px 20px red;
```

# 文本的换行

```
  word-wrap:break-word

​    首先尝试把长单词换到下一行显示，如果在一行仍然有超出，会在单词内部断句。

  word-break:break-all;

​    不会把长单词换到下一行，直接在单词内部进行断句（粗暴断句）
```

# 背景模块

```
 背景图原点的改变(背景的起始点)：

​    background-origin:

​      padding-box 背景图像填充框的相对位置  默认值

​      border-box 背景图像边界框的相对位置

​      content-box 背景图像的相对位置的内容框   



  背景的裁切：

​    background-clip:

​      padding-box 背景图像填充框的相对位置  

​      border-box 背景图像边界框的相对位置  默认值

​      content-box 背景图像的相对位置的内容框 



  背景图的大小：

​    background-size:宽度 高度

​      属性值的设置：

​        固定大小： 100px 200px

​        百分比：  100%  100%

​        cover   成比例放大，直到铺满整个容器。

​        contain  成比例放大，当背景图的宽或者高达到最大则停止



  多背景图的设置：

​    background:url(./1.jpg) no-repeat left top,url(./2.jpg) no-repeat right bottom;

​    如果想添加背景颜色 background-color:red;
```

# 颜色模式

```
 red\green\blue\pink\orange。。。。。。

  十六进制表示颜色值： #ff0000 #00ff00 

  rgb(255,0,0);

  rgba(250,0,0,.5);   //让背景色透明！内容不透明

  了解：

​    HSL(357,81%,36%)

​    HSLA(357,81%,36%,0.5)
```

# 图片边框

```
 图片边框

​    border-image 属性是一个简写属性，用于设置以下属性:

​      border-image-source 用在边框的图片的路径。

​      border-image-slice 图片边框向内偏移(不加单位)。

​        不加单位！

​        第一个值横向的两刀

​        第二个值纵向的两刀

​        fill属性值：保持中间 的 图片显示。

​      border-image-repeat 图像边框是否应平铺(repeat)、铺满(round)或拉伸(stretch)

​      border-image-outset 边框图像区域超出边框的量(值是一个倍数)
```

# 圆角

```
  border-radius:20px

​    一个属性值：

​      按照属性值为半径 在矩形区域的四个角 画圆。

  border-radius:20px 40px;

​    第一个属性值：左上角以及右下角

​    第二个属性值：右上角以及左下角

  border-radius:20px 40px 80px;

​    第一个值：左上角

​    第二个值: 左下角 右上角

​    第三个值：右下角

  border-radius:20px 50px 80px 100px;

​    从左上角开始 顺时针设置。

  border-radius:20px/50px

​    /前面的代表水平半径

​    /后面的代表垂直半径

  border-radius: 10px 20px 30px 40px / 40px 20px 30px 10px;
```

# 增加宽高的属性值

```
法定属性值：

  fill-available、fit-content、max-content、min-content

  fill-available：

​    作用：让元素自适应父元素宽或者是高。

​    面试题： fill-available 和 width:100%的区别

​      对padding的影响

  fit-content: 让一个块元素，适应内容的一个宽

  max-content

  min-content
```

# 导入iconfont

1.去iconfont官网

2.搜索并添加需要的图标到购物车

3.直接下载代码

4.放在你所在的站点里面

5.通过 link 导入 iconfont.css

# css3事件

```
  pointer-events: none  禁止一些事情触发

  pointer-events: none  穿透遮罩，让当前元素遮住的元素有时间触发
```

# 怪异盒模型（宽度计算）

```
  标准盒模型

​    border长在元素的宽高以外，padding会把盒子撑大
准模式下它的宽度计算公式为width + padding(左右) + border(左右)+ margin(左右) 。

  怪异盒模型(IE盒模型)

​    特点：border和padding长在元素宽高内部的。

   标准盒模型：  box-sizing:content-box

   怪异盒模型：  box-sizing:border-box
   异盒模型的宽度计算公式为width+margin（左右）
```

# 弹性盒模型

```
作用：控制 "子元素" 的布局方式

​    显示规则：所有的子元素都会在 "主轴" 进行排列

​    主轴、侧轴：主轴和侧轴是相对而言的，

​      如果x轴为主轴，y轴是侧轴

​      如果y轴为主轴，x轴是侧轴

​    设置方法：如果想控制某个元素的布局，必须让父元素形成弹性盒子
```

```
  一、display:flex; 形成弹性盒

​      a:弹性盒子 子元素的默认排列状态：

​        因为弹性盒子默认的x轴为主轴：所以子元素默认都横向排列.

​      b:如果父元素是弹性盒：那子元素都能设置宽高.

​      c:如果父元素为弹性盒，让子元素在弹性盒里面左右上下居中，只要需要给子元素设置margin:auto
```

```
  二、改变主轴的排列方式（指定主轴）

​      flex-direction:

​        属性值：

​          row         x轴为主轴

​          row-reverse    横向反向排列

​          column       y轴为主轴

​          column-reverse   纵向反向排列
```

```
三、子元素在弹性盒子里面的 主轴的对齐方式

​      justify-content 属性

​        justify-content: flex-start;  设置子元素在**主轴上的对齐方式**。属性值可以是：

​        flex-start           从主轴的起点对齐（默认值）

​        flex-end            从主轴的终点对齐

​        center             居中对齐

​        space-around          在父盒子里平分

​        space-between          两端对齐 平分
```

```
四、侧轴的对齐方式

​      align-items 侧轴对齐

​        flex-start     从侧轴开始的方向对齐

​        flex-end      从侧轴结束的方向对齐

​        baseline      基线 默认同flex-start

​        center       中间对齐

​        stretc        拉伸
```

```
   五、控制子元素在弹性盒子里面是否换行

​      flex-wrap

​        wrap        换行

​        wrap-reverse    反向换行

​        nowrap       不换行
```

```
   六、行与行之间的对齐方式

​      align-content:

​        flex-start

​        flex-end

​        center

​        space-betweeen

​        space-around

​        stretch(拉伸)

​      注：默认情况下algin-center在侧轴执行的时候，会把默认的间距给合并，对于单行文本，该属性不起作用
```

```
七、flex-flow属性是flex-direction和flex-wrap的简写形式，默认是row-nowrap
```

```
 flex-grow

用于将弹性盒子的可用空间，分配给弹性元素。可以使用整数或小数声明。 一个数字，规定项目将相对于其他灵活的项目进行扩展的量。

  flex-shrink

与 `flex-grow` 相反 `flex-shrink` 是在弹性盒子装不下元素时定义的缩小值一个数字，规定项目将相对于其他灵活的项目进行收缩的量。 flex-shrink:0; 弹性盒子内部的子元素不再进行挤压，正常显示。

  flex-basis

flex-basis 属性定义了在分配多余空间之前，项目占据的主轴空间（main size）。浏览器根据这个属性，计算主轴是否有多余空间。可以是长度单位，也可以是百分比。`flex-basis`的优先级高于`width、height`属性。
```



# cale计算

```
	  <style>
        * {
            margin: 0;
            padding: 0;
        }
        body,
        html {
            height: 100%;
        }
        .left {
            width: 200px;
            height: 80%;
            background: orange;
            float: left;
        }
        .right {
            width: calc(100% - 200px);
            height: 100%;
            background: pink;
            float: left;
        }
    </style>
    
    
    <div class="left"></div>
    <div class="right">1</div>
```

# 弹性盒添加在子元素上面的属性

```
 一：align-self:  针对的是某个子元素在侧轴的对齐方式。

​      注意：align-self 属性可重写灵活容器的 align-items 属性。

​      属性值

​        auto    默认值。元素继承了它的父容器的 align-items 属性。如果没有父容器则为 "stretch"。

​        Stretch   元素被拉伸以适应容器。

​        Center   元素位于容器的中心。

​        flex-start   元素位于容器的开头。

​        flex-end    元素位于容器的结尾。



​    二：order:

​      数字越大越往后排，默认为0，支持负数。

​    

​    三： flex:1;

​      把父元素（弹性盒子）剩余空间自动分配(主轴上面的空间)。



​      复合属性。设置或检索弹性盒模型对象的子元素如何分配空间

​      详细属性值：

​        缩写「flex: 1」, 则其计算值为「1 1 0%」

​        缩写「flex: auto」, 则其计算值为「1 1 auto」

​        flex: none」, 则其计算值为「0 0 auto」

​        flex: 0 auto」或者「flex: initial」, 则其计算值为「0 1 auto」，即「flex」初始值
```

#  常见的布局方法

```
1、**table 表格布局**：早期使用的布局，如今用得很少。

2、**float 浮动 + margin**：为了兼容低版本的IE浏览器，很多网站（比如腾讯新闻、网易新闻、淘宝等）都会采用 float 布局。

3、**inline-block 布局**：对外的表现是行内元素（不会独占一行），对内的表现是块级元素（可以设置宽高）。

4、**flex 布局**：为布局而生，非常灵活，是最为推荐的布局写法。

​	注： flex 布局不支持 IE9 及以下的版本。如果你的页面不需要处理 IE浏览器的兼容性问题，则可以放心大胆地使用 flex 布局。

flex 是一种现代的布局方式，是 W3C 第一次提供真正用于布局的 CSS 规范。

5、响应式布局。
```

# 如何让一个块级元素水平垂直居中

```
方式一：绝对定位 + margin（需要指定子元素的宽高，不推荐）

方式二：绝对定位 + translate（无需指定子元素的宽高，推荐）

方式3：flex 布局（待改进）

方式4： flex 布局 + margin: auto（推荐）
```

# 如何让一个内联元素垂直居中

```
1、伪元素实现

 /* 100% 高度的 afrer before 加上 inline block */

 .parent::before {

​      content: '';

​      height: 100%;

​      display: inline-block;

​      vertical-align: middle;

​    }
2、父元素不设高度，用padding实现块级元素居中
3、table自带功能
4、margin-top:-50%
5、translate:-50%
6、absolute:margin auto
7、flex


```



# 多列布局

```
  1、column-count

​    分成几列显示

  2、column-gap:

​    每一列的间隔

  3、column-rule

​    column-rule:10px solid red;

  4、column-fill

​    设置或检索对象所有列的高度是否统一

​    auto：列高度自适应内容

​    balance：所有列的高度以其中最高的一列统一

  5、column-span

​    设置或检索对象元素是否横跨所有列。

​    none：不跨列

​    all：横跨所有列

  6:column-width:

​    列宽

  7：columns:

​    column-width 和 column-count 简写

​    columns:300px 3;
	8：防止元素断裂
	
	 break-inside: avoid;
```



# 响应式布局

​	响应式布局：

​			为了适应不同的设备、分辨率

​			不同的设备（PC电脑端、平板电脑端、手机端）

​	响应式的优势：

​			1：一套项目 能适应不同的设备、灵感

​			2：能够快捷解决多设备显示适应问题

​			3：从显示上： 相对而言用户体验比较好一些。

​	响应式的缺点：

​			1：开发成本偏高（项目组）

​					产品规划项目 一套不能满足

​					UI一套设计图不能满足 （移动、PC）

​					前端布局：一套布局方案不能满足

​					数据：PC  移动

​			2：兼容各种设备工作量大，效率低下

​			3：代码累赘，会出现隐藏无用的元素，加载事件加长

​			4：其实这是一种折中性质的设计解决方案，多方向因素影响面达不到最佳效果

​			5：会出现用户混淆

​			绝大部分项目：

​					PC ->  官网

​					移动 ->  移动端网页、app\小程序..

​			为什么要讲响应式：

​					利用响应式的思想，做移动端项目的适配（只考虑手机端的项目，不考虑PC端 ）

# 媒体查询

 

```
 媒体查询：

​    监测设备的特性，根据所指定的条件，设置不同的css样式。

​    （例如：监测浏览器窗口的宽度，如果小于320px body背景为红色）

​    媒体查询一般监测：视口的宽度、浏览器窗口的宽、屏幕的比例、横屏、竖屏......

  媒体查询的组成：

​    @media 设备类型[all\screen] and (条件表达式) and (条件表达式){

​      css样式

​    }

​    注：and关键字两侧必须有空格，条件表达式不需要分号结束



  设备范围

  默认样式  注意：默认样式要写在最前面

​    /* 打印样式 */

​      @media print {}

​    /* 手机等小屏幕手持设备 */

​      @media screen and (min-width: 320px) and (max-width: 480px) {}

​    /* 平板之类的宽度 1024 以下设备 */

​      @media only screen and (min-width: 321px) and (max-width: 1024px) {}

​    /* PC客户端或大屏幕设备: 1028px 至更大 */

​      @media only screen and (min-width: 1029px) {}

​    /* 竖屏 */

​      @media screen and (orientation:portrait) {对应样式}

​    /* 横屏 */

​      @media screen and (orientation:landscape){对应样式}



  媒体查询注意的点：

​    媒体查询做样式微调。



​    常见的样式的调整：

​      font-size:

​      float:

​      display:

​      width:

​      height:
```

## meta标签的设置

```

        <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">

​      width = device-width：宽度等于当前设备的宽度

​      initial-scale： 初始的缩放比例（默认设置为1.0）

​      minimum-scale：允许用户缩放到的最小比例（默认设置为1.0）

​      maximum-scale：允许用户缩放到的最大比例（默认设置为1.0）

​      user-scalable：用户是否可以手动缩放（默认设置为no，因为我们不希望用户放大缩小页面）
```



# 移动端适配	

详细讲解：[https://juejin.im/post/5cddf289f265da038f77696c]: 

## 视口

```
视口(`viewport`)代表当前可见的计算机图形区域。在`Web`浏览器术语中，通常与浏览器窗口相同，但不包括浏览器的`UI`， 菜单栏等——即指你正在浏览的文档的那一部分。

一般我们所说的视口共包括三种：布局视口、视觉视口和理想视口，它们在屏幕适配中起着非常重要的作用。
```



## PPI、DPI、DPR		

### PPI

```
PPI(Pixel Per Inch)`：每英寸包括的像素数。

`PPI`可以用于描述屏幕的清晰度以及一张图片的质量。

使用`PPI`描述图片时，`PPI`越高，图片质量越高，使用`PPI`描述屏幕时，`PPI`越高，屏幕越清晰。

在上面描述手机分辨率的图片中，我们可以看到：`iPhone XS Max` 和 `iPhone SE`的`PPI`分别为`458`和`326`，这足以证明前者的屏幕更清晰。
```

由于手机尺寸为手机对角线的长度，我们通常使用如下的方法计算`PPI`:

![\frac{\sqrt{水平像素点数^2+垂直像素点数^2}}{尺寸}](https://juejin.im/equation?tex=%5Cfrac%7B%5Csqrt%7B%E6%B0%B4%E5%B9%B3%E5%83%8F%E7%B4%A0%E7%82%B9%E6%95%B0%5E2%2B%E5%9E%82%E7%9B%B4%E5%83%8F%E7%B4%A0%E7%82%B9%E6%95%B0%5E2%7D%7D%7B%E5%B0%BA%E5%AF%B8%7D)

`iPhone 6`的`PPI`为 ![\frac{\sqrt{1334^2+750^2}}{4.7}=325.6](https://juejin.im/equation?tex=%5Cfrac%7B%5Csqrt%7B1334%5E2%2B750%5E2%7D%7D%7B4.7%7D%3D325.6)，那它每英寸约含有`326`个物理像素点。



### DPI

`

```
DPI(Dot Per Inch)`：即每英寸包括的点数。

这里的点是一个抽象的单位，它可以是屏幕像素点、图片像素点也可以是打印机的墨点。

平时你可能会看到使用`DPI`来描述图片和屏幕，这时的`DPI`应该和`PPI`是等价的，`DPI`最常用的是用于描述打印机，表示打印机每英寸可以打印的点数。

一张图片在屏幕上显示时，它的像素点数是规则排列的，每个像素点都有特定的位置和颜色。

当使用打印机进行打印时，打印机可能不会规则的将这些点打印出来，而是使用一个个打印点来呈现这张图像，这

些打印点之间会有一定的空隙，这就是`DPI`所描述的：打印点的密度。打印机的`DPI`越高，打印图像的精细程度

就越高，同时这也会消耗更多的墨点和时间。
```



### DPR

```
设备像素比`device pixel ratio`简称`dpr`，即物理像素和设备独立像素的比值。 

怎么确定dpr!!!

​    根据UI设计图

​      如果设计图宽度 640px dpr 取2

​      如果设计图宽度 750px dpr 取2

​      如果设计图宽度 1125px dpr 取3
```

##  移动端适配方案

## 媒体查询

  如果用媒体查询取更改html的font-size值：

​    设置范围：

​      @media all and (max-width:320px){

​        html{

​          font-size:12px

​          /*1rem == 12px*/

​        }

​      }

​      @media all and (min-width:321px) and (max-width:375px){

​        html{

​          font-size:14px

​          /*1rem == 14px*/

​        }

​      }

​      @media all and (min-width:376px){

​        html{

​          font-size:16px;

​          /*1rem == 16px*/

​        }

​      }

  如果用媒体查询取更改html的font-size值弊端：

​      1：相对( 设置范围 )更改了html的font-size ，达不到最佳的适配效果

​      2：font-size值不方便计算

### vh、vw方案

`vh、vw`方案即将视觉视口宽度 `window.innerWidth`和视觉视口高度 `window.innerHeight` 等分为 100 份。

上面的`flexible`方案就是模仿这种方案，因为早些时候`vw`还没有得到很好的兼容。

- `vw(Viewport's width)`：`1vw`等于视觉视口的`1%`
- `vh(Viewport's height)` :`1vh` 为视觉视口高度的`1%`
- `vmin` :  `vw` 和 `vh` 中的较小值
- `vmax` : 选取 `vw` 和 `vh` 中的较大值



### rem方案

#### rem介绍

```
 em     作为font-size的单位时，其代表父元素的字体大小，em作为其他属性单位时，代表自身字体大小

 rem针对的是根元素

​      [相对大小的单位]

​      [相对与根元素的html font-size的大小]

​      [等比缩放]
```

#### rem布局

​	详细介绍：https://yanhaijing.com/css/2017/09/29/principle-of-rem-layout/

​	其实就是上面提到的等比缩放，一般是基于宽度，试想一下如果UE图能够等比缩放，那该多么美好啊

假设我们将屏幕宽度平均分成100份，每一份的宽度用x表示，`x = 屏幕宽度 / 100`，如果将x作为单位，x前面的

数值就代表屏幕宽度的百分比

```
	p {width: 50x} /* 屏幕宽度的50% */
```

### 面试题：width:100%  和  width:100vw  绝对相等吗

​		 width:100vw  包括滚动条的

​		 width:100% 按父元素百分比设置的

​			注：手机端滚动条是不占空间的，PC端是占据空间的

### vw&rem布局适配方案

 

```
 适配：让html的font-size的值 跟随视口发生变化

​    1：为了方便计算 html 的 font-size:100px;

​    2: 因为100px 不会随着 视口发生改变。

​    3: 怎么把100px 转成 vw ???????????
```



              第一种情况：
                例如：设计图 宽度 750px
                考虑设备像素比例dpr  为  2
                750px / 2 == 375px
                适配的核心设备（iphone 6/7/8）
                设备视口宽度 375px
                100vw == 375px
    
                1vw == 3.75px
                ?vw == 100px
    
                26.67vw == 100px
    
            第二种情况：
                例如：设计图 宽度 640px;
                考虑dpr 2
                640px / 2 == 320px
                适配核心设备（iphone 5）
                设备视口的宽 320px
                100vw == 320px
                1vw == 3.2px
                ?vw == 100px
                31.25vw == 100px
    
        记住一句话：
            如果你是用 vw + 结合 rem 做页面布局适配:
    
            UI设计图为 750px   html{font-size:26.67vw}
            UI设计图为 640px   html{font-size:31.25vw}

## fiexible适配方案

```
  flexible.js 插件！

  1：先引入flexible.js

        <script src="url"></script>

  2: 去掉meta标签（1：1比例，禁止缩放）


  3：应用：

​    例如：从ps里面量出height  88px；

​    css设置的时候， 0.88rem;
```

## 1像素边框写法

   

```
 .bottom-border:after{

​      content:"";

​      width:100%;

​      height:1px;

​      background:red;

​      position:absolute;

​      left:0;bottom:0;

​      transform:scaleY(0.5);

​      transform-origin: center bottom;

​    }
```

## 网络布局

```
网格(grid)布局:

​    控制子元素(不包括子元素的子元素)

  1:开启网格布局:

​    display:grid;

  2:划分行和列

​    grid-template-columns: 

​    grid-template-rows:

​    说明: 根据属性值的个数来确定几列或者几行


​    功能函数或者关键字：

​    a: 功能函数 repeat(重复的个数，重复的值);

​    b: 关键字：

​      auto-fill关键字( 自动填充 )

​      当容器的大小不固定，但是项目大小固定，分配的列数。

​    c：fr  片段（ 把网格划分之后，某一列 所占的份数 ）

​    d : 关键字：auto 自动填充。

​    e: minmax(最小值，最大值)

  3：grid-template-columns: [c1] 100px [c2] 100px [c3] auto [c4];

​    grid-template-rows: [r1] 100px [r2] 100px [r3] auto [r4];

​    指定网格布局为3行x3列，因此有4根垂直网格线和4根水平网格线。方括号里面依次是这八根线的名字。

  4：网格间距：

​    grid-row-gap:20px /* 行间距 */

​    grid-column-gap:20px /* 列间距 */

​    grid-gap:30px 30px  /* 复合式写法 */

  5: grid-template-areas: 'a b c'

​              'd e f'

​              'g h i';

​        将整个网格容器分为9个区域，每个区域对应一个单元格

​        通过grid-area 指定项目名称

  6:grid-auto-flow:  更改子元素所排列的顺序。

​    column||ro

  7：设置整个内容区域在容器里面的水平 | 垂直 对齐方式

​    justify-items: start | end | center | stretch;

​    align-items: start | end | center | stretch;

​    place-items: <justify-items> <align-items>  /*复合式写法*/

​      start：对齐单元格的起始边缘。

​      end：对齐单元格的结束边缘。

​      center：单元格内部居中。

​      stretch：拉伸，占满单元格的整个宽度（默认值）。

  8：grid-column ， grid-row 
​      1 / 3 

​        从第一条（横/纵）网格线 到第三条网格线
```

## 图片整合

```
  图片整合：（ css精灵、css图片精灵、雪碧图、CSS Sprites ）

​    优势：

​      为了缓解服务端的压力，加载速度的提升。

​      相对减小图片的体积。


  图片整合：

​    一定保证背景为透明

​    尽量保证上下排列（上下留出足够的空间）

  精灵图的使用：

​    background-position:
```

# 兼容



### 浏览器的四大内核

#### Trident   代表作：IE

```txt
元老级内核之一，由微软开发，并于1997年10月首次在ie 4.0中使用，凭借其windows垄断优势，Trident市场占有率一直很高。然而垄断并非，没有竞争就没有进步，长期以往，Trident内核一度停滞不前，更新缓慢，甚至一度与W3C标准脱节。2011年，从ie 9开始，Trident开始支持HTML5和CSS 3，因此我们也经常会看到有些网站在浏览时会提示用户（在Internet Explorer 9.0+以上浏览效果最佳）。前端程序员做浏览器兼容一般也不再会考虑ie 8之前的浏览器了。
```

#### Gecko 代表作：Mozilla

```txt	
元老级内核之一，由Netscape公司Mozilla组织开发。1998年，Netscape在于IE浏览器竞争失利之后，成立了非正式组织Mozilla，由其开发新一代内核，后命名为“Gecko”。FireFox也是这班人开发出来了，因此这也就是Mozilla一直使用的内核。
Gecko的特点是代码完全公开，因此其开发程度很高，全世界的程序员都可以为其编写代码，增加功能。
```

#### WebKit : 苹果 & 谷歌旧版本

```txt
这是苹果公司开发的内核，也是其旗下产品Ssfari浏览器使用的内核。Webkit引擎包含了WebCode排版引擎和JavaScriptCode解析引擎，分别是从KDE的KHTML和KJS衍生而来，它们都是自由软件，在GPL条约下授权，同时支持BSD系统开发。
Chrome、360极速浏览器以及搜狗高速浏览器也使用Webkit作为内核（在脚本理解方面，Chorome使用自己研发的V8引擎）。
```

#### Blink : 代表作：谷歌 & 欧鹏

```
这是由Google和Opera Software开发的浏览器排版引擎，Google计算将这个渲染引擎作为Chromium计划的一部分，并且在2013年4月公布了这一消息。这一渲染引擎是开源引擎Webkit中WebCore组件的一个分支，并且在Chrome（28及往后版本）、Opera（15及往后版本）和Yandex浏览器中使用
```

#### Presto   ( Opera前内核 已经废弃 )

扩展：**五大浏览器是指**：Chrome、IE、Firefox、safari、Opera



**四大内核分别是**：Trident（也称IE内核）、webkit、Blink、Gecko。



1、IE浏览器内核：Trident内核，也是俗称的IE内核；

2、Chrome浏览器内核：统称为Chromium内核或Chrome内核，以前是Webkit内核，现在是Blink内核；

3、Firefox浏览器内核：Gecko内核，俗称Firefox内核；

4、Safari浏览器内核：Webkit内核；

5、Opera浏览器内核：最初是自己的Presto内核，后来是Webkit，现在是Blink内核；

6、360浏览器、猎豹浏览器内核：IE+Chrome双内核；

7、搜狗、遨游、QQ浏览器内核：Trident（兼容模式）+Webkit（高速模式）；

8、百度浏览器、世界之窗内核：IE内核；

9、2345浏览器内核：以前是IE内核，现在也是IE+Chrome双内核；



### 为什么会出现浏览器兼容问题？

```txt
由于各大主流浏览器由不同的厂家开发，所用的核心架构和代码也很难重和，这就为各种莫名其妙的Bug(代码错误）提供了温床。再加上各大厂商出于自身利益考虑而设置的种种技术壁垒，都让CSS应用起来比想象得要麻烦。浏览器的兼容问题是我们必须去克服的。
```

## 常见的BUG

#### IE低版本常见CSS解析Bug及hack

```txt
1)图片有边框BUG
当图片加<a href=“#”></a>在IE上会出现边框
Hack:给图片加border:0;或者border:0    none;


2)图片间隙
div中的图片间隙BUG
描述：在div中插入图片时，图片会将div下方撑大大约三像素。
hack1:将</div>与<img>写在一行上；
hack2:将<img>转为块状元素，给<img>添加声明：display:block;


3)  双倍浮向（双倍边距）（只有IE6出现）
描述：当Ie6及更低版本浏览器在解析浮动元素时，会错误地把浮向边边界（margin）加倍显示。
hack:给浮动元素添加声明：display:inline;


4)默认高度（IE6、IE7）
描述：在IE6及以下版本中，部分块元素拥有默认高度（在16px左右；）
hack1:给元素添加声明：font-size:0;
hack2：给元素添加声明：overflow:hidden;

```



#### 非IE  BUG

```txt
5)表单元素对齐不一致
描述：表单元素行高对齐方式不一致
hack:给表单元素添加声明：float:left;


6)按钮元素默认大小不一

描述：各浏览器中按钮元素大小不一致
hack1： 统一大小/（用a标记模拟）
hack2:input外边套一个标签，在这个标签里写按钮的样式，把input的边框去掉。
hack3:如果这个按钮是一个图片，直接把图片作为按钮的背景图即可。


8)鼠标指针bug
描述：cursor属性的hand属性值只有IE9以下浏览器识别，其它浏览器不识别该声明，cursor属性的pointer属性值IE6.0以上版本及其它内核浏览器都识别该声明。
hack:    如统一某元素鼠标指针形状为手型，
应添加声明：cursor:pointer


cursor:         ;
auto默认
crosshair加号
text文本
wait等待
help帮助
progress过程
inherit继承
move移动
ne-resize向上或向右移动
pointer手形



9)透明属性
兼容其他浏览器写法：opacity:value;(value的取值范围0-1;
	例：opacity:0.5;)
IE浏览器写法：filter:alpha(opacity=value);取值范围 1-100(整数)
```



### 过滤器

```txt
  1.下划线属性过滤器
  当在一个属性前面增加了一个下划线后，由于符合标准的浏览器不能识别带有下划线的属性而忽略了这个声明，但是在IE6及更低版本浏览器中会继续解析这个规则。
  
  语法：选择符{_属性：属性值；}
 

  2. !important关键字过滤器
  
  它表示所附加的声明具有最高优先级的意思。但由于IE6及更低版本不能识别它，
我们可以利用IE6的这个Bug作为过滤器来兼容ＩＥ６和其它标准浏览器。

  语法：选择符{属性：属性值!important;}
 

  3. *属性过滤器

  当在一个属性前面增加了*后，该属性只能被IE7浏览器识别，其它浏览器混略该属
性的作用。

 语法：选择符{*属性：属性值；}


  4.   \9  ：IE版本识别；其它浏览器都不识别
语法：选择符{属性：属性值\9;}

  5.   \0  :   IE8 及以上版本识别；其它浏览器都不识别

```



## CSS Bug、CSS Hack和Filter

+ CSS Bug: CSS样式在各浏览器中解析不一致的情况，或者说CSS样式在浏览器中不能正确显示的问题称为CSS bug.
+ CSS Hack:  CSS中，Hack是指一种兼容CSS在不同浏览器中正确显示的技巧方法，因为它们都属于个人对CSS代码的非官方的修改，或非官方的补丁。有些人更喜欢使用patch(补丁)来描述这种行为。
+ Filter:表示过滤器的意思，它是一种对特定的浏览器或浏览器组显示或隐藏规则或声明的方法。本质上讲，Filter是一种用来过滤不同浏览器的Hack类型。
+ 

# 常见布局方案介绍

```
rem+100%  混合布局

移动端布局：rem布局（等比缩放）

移动端布局：100%布局 （流式布局）
```





<style>
        *{
            margin: 0;
            padding: 0;
        }
        ul,ol,li{
            list-style:none;
        }
        a{
            text-decoration: none;
        }
        .nav{
            width: 600px;
            height: 40px;
            background: oldlace;
        }
        .nav li{
            float: left;
            margin-left:10px ;
        }
        .nav li a{
            /* 转成块状元素 */
            display:block;
            width: 100px;
            height: 40px;
            background: pink;
            font-size: 12px;
            line-height: 40px;
            color: gray;
            text-align: center;
        }
        .nav li a:hover{
            background: cyan;
        }
    </style>
<ul class="nav">
# 导航栏写法

    <li>
    
            <a href="">导航项目</a>
    
    </li>
    
    <li>
    
            <a href="">导航项目</a>
    
    </li>
    
    <li>
    
            <a href="">导航项目</a>
    
    </li>
    
    <li>
    
            <a href="">导航项目</a>
    
    </li>
    
    <li>
    
            <a href="">导航项目</a>
    
    </li>   
    </ul>

 














# 项目前期规划

##     1: 页面的版心 1002px;

##     2:   命名规范

​      外围结构ID名称：

​        a : 板块内容 

​        b : 驼峰式命名法 newsLeft

​      版心区域：

​        连字符名法：

​          news-wrap

​      内部内容块命名”

​        下划线：

​          news_con

##     3:  css样式表

​      a: 外部样式表！

​      b: 先写一套重置样式。（把所有默认的样式清除！）

​      c: 在创建一个属于当前页面自己的样式！

# 补充

```
一个页面划分结构
logo画满  nav 左右留点 
/*five-photo
case1为例
先划分上下 在划分左右（左右那块用一个大盒子包起来）
case2为例
标题 h2 样式写法 case h2{ ; ;}
先划分上下三个盒子、在划分左右*/
1.上下结构：  
   左右结构：
```



# 页面设计

![photo-nine](G:\nz-201\day7\07day-吴海桂(作业)\photo-nine.jpg)

## 公共样式

```
	当前整个网站里面，公共的样式

​	网络头部 和 底部的样式...

​	公共样式

​			.float_left{ float:left;}

​			.float_right{ float:right}

​			.clear_margin{ margin:0!important;}

​			.clear_border{border;0!important}

			.clear_bg{background:none!important;}

```

​			.

## 页面的重置样式

```
@charset "utf-8";

/* 重置样式 */

*{

  margin:0;

  padding:0;

}

h1,h2,h3,h4,h5,h6{

  font-size:16px;

  font-weight:normal; /*清除加粗*/

}

ul,ol,li{

  list-style:none; /*去掉列表符号*/

}

b,strong{

  font-weight:normal; /*清除加粗*/

}

em,i{

  font-style: normal; /*倾斜清除*/

}

a,u{

  text-decoration: none; /*去掉下划线*/

}

img{

  border:0; /*清除图片在有超链接的时候，存在一个蓝色的边框*/

}

input{

  outline:none;/*清除INPUT 聚焦时的 蓝色边框*/

}
```



## 页面的主框架

### logo

 <div class="logo-wrap">
        <h1 class="logo_l">
            <a href="#">
                <img src="./images/logo_03.jpg" alt="">
            </a>
        </h1>
        <form action="" class="logo_r">
            <input class="search_txt" type="text" value="search...">
            <input class="btn" type="button">
        </form>
    </div>

### nav

<div id="nav">
        <!-- 导航的结构用ul实现 -->
        <ul class="nav-wrap">
            <!-- 导航项的嵌套 -->
            <li>
                <a href="#">集团介绍</a>
            </li>
            <li>
                <a href="#">集团介绍</a>
            </li>
            <li>
                <a href="#">集团介绍</a>
            </li>
            <li>
                <a href="#">集团介绍</a>
            </li>
            <li>
                <a href="#">集团介绍</a>
            </li>
            <li>
                <a href="#">集团介绍</a>
            </li>
            <li>
                <a href="#">集团介绍</a>
            </li>
            <li class="border_none">
                <a href="#">集团介绍</a>
            </li>
        </ul>
    </div>

### banner

 <div id="banner">
        <div class="banner-wrap">
            <!-- 后期banner图 都是放在版心里面的！！！ -->
            <!-- <img src="./images/banner_02.jpg" alt=""> -->
        </div>
    </div>

### news

<div class="news-wrap">
        <div class="news_l">
            <h3 class="news_tit">公司新闻</h3>
            <!-- 新闻条的嵌套 -->
            <ul class="news_list">
                <li>
                    <a href="#">新闻内容新闻内容新闻内容新闻内容</a>
                    <span>2020-02-11</span>
                </li>
                <li>
                    <a href="#">新闻内容新闻内容新闻内容新闻内容</a>
                    <span>2020-02-11</span>
                </li>
                <li>
                    <a href="#">新闻内容新闻内容新闻内容新闻内容</a>
                    <span>2020-02-11</span>
                </li>
                <li>
                    <a href="#">新闻内容新闻内容新闻内容新闻内容</a>
                    <span>2020-02-11</span>
                </li>
                <li>
                    <a href="#">新闻内容新闻内容新闻内容新闻内容</a>
                    <span>2020-02-11</span>
                </li>
                <li>
                    <a href="#">新闻内容新闻内容新闻内容新闻内容</a>
                    <span>2020-02-11</span>
                </li>
            </ul>
        </div>


        <div class="news_c">
            <h3 class="news_tit">公司介绍</h3>
            <p class="txt1">公司成立于2020 <br><span>公司成立于2020</span> </p>
            <p class="txt2">公司已经成为公司已经成为公司已经成为公司已经成为公司已经成为</p>
        </div>
        <div class="news_r">
            <h3 class="news_tit">人才招聘</h3>
            <p>培养一类技术人才培养一类技术人才培养一类技术人</p>
            <a href="#"><img src="./images/abg_03.jpg" alt=""></a>
        </div>
    </div>

### case

<div class="case-wrap">
        <h2>市场项目</h2>
        <div class="case_show">
            <dl>
                <dt><img src="./images/banner_02.jpg" alt=""></dt>
                <dd>文本介绍文本介绍文本介绍文本介绍文本介绍文本介绍文本介绍</dd>
            </dl>
            <dl>
                <dt><img src="./images/banner_02.jpg" alt=""></dt>
                <dd>文本介绍文本介绍文本介绍文本介绍文本介绍文本介绍文本介绍</dd>
            </dl>
            <dl>
                <dt><img src="./images/banner_02.jpg" alt=""></dt>
                <dd>文本介绍文本介绍文本介绍文本介绍文本介绍文本介绍文本介绍</dd>
            </dl>
            <dl class="margin_0">
                <dt><img src="./images/banner_02.jpg" alt=""></dt>
                <dd>文本介绍文本介绍文本介绍文本介绍文本介绍文本介绍文本介绍</dd>
            </dl>
        </div>
    </div>

### links

<div id="links">
        <div class="links-wrap">
            <div class="links_l">
                <h3 class="links_tit">产品中心</h3>
                <div class="list_box">
                    <ul>
                        <li>
                            <a href="#">汽车电机</a>
                        </li>
                        <li>
                            <a href="#">汽车电机汽车</a>
                        </li>
                        <li>
                            <a href="#">汽车电机</a>
                        </li>
                        <li>
                            <a href="#">汽车电汽</a>
                        </li>
                        <li>
                            <a href="#">汽车电机</a>
                        </li>
                    </ul>
                    <ul>
                        <li>
                            <a href="#">汽车电机</a>
                        </li>
                        <li>
                            <a href="#">汽车汽车电</a>
                        </li>
                        <li>
                            <a href="#">汽车电机</a>
                        </li>
                        <li>
                            <a href="#">汽车电机</a>
                        </li>
                        <li>
                            <a href="#">汽车电机</a>
                        </li>
                    </ul>
                    <ul class="margin_0">
                        <li>
                            <a href="#">汽车电机</a>
                        </li>
                        <li>
                            <a href="#">汽车电机汽车电机</a>
                        </li>
                        <li>
                            <a href="#">汽车电机</a>
                        </li>
                        <li>
                            <a href="#">汽车电机</a>
                        </li>
                        <li>
                            <a href="#">汽车电机</a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="links_c">
                <h3 class="links_tit">技术研发</h3>
                <div class="list_box">
                    <ul class="margin_0">
                        <li>
                            <a href="#">汽车电机</a>
                        </li>
                        <li>
                            <a href="#">汽车电机汽车电机</a>
                        </li>
                        <li>
                            <a href="#">汽车电机</a>
                        </li>
                        <li>
                            <a href="#">汽车电机</a>
                        </li>
                        <li>
                            <a href="#">汽车电机</a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="links_r">
                <h3 class="links_tit">营销网络</h3>
                <div class="map_box">
                    <img src="./images/map_03.jpg" alt="">
                </div>
            </div>
        </div>
    </div>

### footer

<div class="footer-wrap">
        <p class="footer_left">
            <a href="#">网站地图</a>
            <a href="#">网站地图</a>
            <a href="#">网站地图</a>
            <a class="border_none" href="#">网站地图</a>
        </p>
        <p class="footer_right">
            备案信息&copy;备案信息&copy;备案信息&copy;备案信息&copy;备案信息&copy;备案信息&copy;备案信息&copy;备案信息&copy;
        </p>
    </div>

## 页面的样式

### logo

```
.logo-wrap{

  height:100px;

}

.logo_l{

  width:281px;

  height:66px;

  float:left;

  /* 用padding 控制图片的位置 */

  padding:34px 0 0 20px;

}

.logo_r{

  width:248px;

  height:61px;

  float:right;

  /* 用padding-top 把输入框和按钮 挤下来 */

  padding-top:39px;

}

.logo_r .search_txt{

  width:181px;

  height:26px;

  background:#f1f1f1;

  border:1px solid #e5e5e5;

  border-right:none;

  color:#8a8a8a;

  text-transform: uppercase;/*控制大小写*/

  /* 用padding 把文字往右移动 */

  padding-left:14px;

  float:left;

}

.logo_r .btn{

  width:30px;

  height:28px;

  background:#f1f1f1 url(../images/btn_03.jpg) no-repeat center;

  border:1px solid #e5e5e5;

  border-left:0;

  float:left;

}
```

### nav

```
#nav{

  /* 外围结构：黑色平铺的元素 */

  /* 宽度没有设置：当前元素的宽和窗口保持同宽 */

  /* 高度让版心撑开 */

  background:#303030;

}

.nav-wrap{

  width:975px;

  height:58px;

  /* 添加padding-left 把所有的li往右侧挤27px */

  padding-left:27px;

}

.nav-wrap li{

  float:left;

  width:119px;

  height:58px;

  border-right:1px solid #494949;

  /* 设置文本样式 */

  text-align: center; /*左右居中*/

  line-height:58px;

  font-size:12px;

}

.nav-wrap li a{

  color:#fff;

}

.nav-wrap .border_none{

  border-right:0;

}

  /*

​    导航的实现步骤：

​      1：给li添加浮动。

​      2: 分析所有导航项的共性！！

​      3: 修改特殊的导航项的样式。

  */

  /* 

​    导航遗留的问题：

​      超链接区域不够大！用户体验不够好！

  */
```

### banner

```
#banner{

  background:url(../images/banner_02.jpg) no-repeat center;

}

.banner-wrap{

  height:465px;

}
```

### news

```
.news-wrap{

  height:240px;

}

.news_l,.news_c,.news_r{

  height:240px;

  float:left;

}

/* 新闻板块标题统一添加类名，用相同的样式 */

.news_tit{

  /* 宽是跟随父元素的宽，高被文本撑开的 */

  font-size:18px;

  color:#414550;

  /* 单行文本消除文本上下的距离误差：line-height ：文本大小 */

  line-height:18px;

  padding-top:36px;

}

.news_l{

  width:479px;

  padding-left:21px;

}

.news_list li{

  width:437px;

  height:24px;/*量取的是行高*/

  background:url(../images/list_bg_03.jpg) no-repeat left center;

  line-height:24px;

  padding-left:13px;

}

.news_list li a{

  float:left;

  font-size:12px;

  color:#4e4e4e;

}

.news_list li span{

  float:right;

  font-size:12px;

  color:#a9a9a9;

}

.news_list{

  margin-top:24px;

}



  /* 

​    新闻条的实现步骤 ：

​      1:如果新闻后面有时间的情况下：

​        结构：

​          <li>

                        <a href="#">新闻内容新闻内容新闻内容新闻内容</a>

​            <span>2020-02-11</span>

​          </li>

​      2：给li设置大小：

​        高:从PS上 量取行高！



​      3: 如果新闻后面有时间，给a 和 放时间的标签，添加一左一右的浮动。



​      4: 设置文本样式！



​      5： 给li添加背景图，当作li的列表符号！！



​      6: 给li添加line-height 让文本上下居中，并且列表符号的背景图上下居中！



​      7:给li添加padding-left 把文字往右挤 露出列表符合。

  */





.news_c{

  width:220px;

  background:#f1f1f1;

  padding-left:20px;

}

.news_c .txt1{

  font-size:12px;

  color:#575757;

  line-height:25px;

  margin-top:34px;

}

.txt1 span{

  font-size:10px;

}

.news_c .txt2{

  font-size:12px;

  line-height:24px;

  color:#888;

  padding-right:29px;

  margin-top:15px;

}



.news_r{

  width:217px;

  background:#fbfbfb url(../images/newsrbg_03.jpg) no-repeat right bottom;

  border-left:1px solid #fff;

  padding-left:24px;

}

.news_r p{

  font-size:12px;

  line-height:24px;

  color:#585858;

  padding-right:38px;

  margin-top:21px;

  margin-bottom:22px;

}
```

### case

```
.case-wrap{

  height:306px;

}

.case-wrap h2{

  font-size:18px;

  color:#3e4750;

  line-height:18px;

  padding:31px 0 19px 22px;

}

.case_show{

  height:220px;

}

.case_show dl{

  width:211px;

  float:left;

  margin:0 20px;

}

.case_show dl dt{

  width:211px;

  height:136px;

}

.case_show dl dt img{

  width:100%;

  height:100%;

}

.case_show dl dd{

  font-size:12px;

  line-height:24px;

  color:#525252;

  margin-top:13px;

}

.case_show .margin_0{

  margin-right:0;

}
```

### links

```
#links{

  background:#e5e5e5;

}

.links-wrap{

  height:250px;

}

.links_l,.links_c,.links_r{

  height:250px;

  float:left;

}

.links_tit{

  font-size:16px;

  color:#5d5d5d;

  line-height:16px;

  padding:31px 0 11px 12px;

  border-bottom:1px solid #c1c1c1;

}

.list_box{

  height:155px;

  padding-left:5px;

  padding-top:15px;

}

.list_box li{

  height:24px;

  background:url(../images/listbg_03.jpg) no-repeat left center;

  font-size:12px;

  line-height:24px;

  padding-left:13px;

}

.list_box li a{

  color:#717171;

}

.list_box ul{

  float:left;

  margin-right:70px;

}

.list_box .margin_0{

  margin:0;

}





.links_l{

  width:452px;

  margin-left:20px;

}

.links_c{

  width:152px;

  margin:0 50px;

}

.links_r{

  width:256px;

}

.map_box{

  /* 图片默认情况下：给父元素添加 text-align:center 能使图片居中 */

  text-align: center;

  padding-top:16px;

}
```

> ### footer

```
.footer-wrap{

  height:82px;

}

.footer_left{

  width:275px;

  height:58px;

  padding:24px 0 0 15px;

  float:left;

}

.footer_left a{

  float:left;

  font-size:12px;

  color:#8a8a8a;

  padding:0 7px;

  border-right:1px solid #8a8a8a;

  line-height:12px;

}

.footer_left .border_none{

  border:0;

}



.footer_right{

  height:58px;

  font-size:12px;

  color:#a9a9a9;

  line-height:12px;

  float:right;

  padding:24px 22px 0 0;

}
```



### 公共样式

```
@charset "utf-8";

/* 版心区域的公共样式 */

.logo-wrap,.nav-wrap,.banner-wrap,.news-wrap,.case-wrap,.links-wrap,.footer-wrap{

  width:1002px;

  margin:0 auto;

}
```

