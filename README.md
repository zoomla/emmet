# emmet快速语法介绍
Emmet快速语法


前端开发利器 Emmet 介绍与基础语法教程

在前端开发的过程中，编写 HTML、CSS 代码始终占据了很大的工作比例。特别是手动编写 HTML 代码，效率特别低下，因为需要敲打各种“尖括号”、闭合标签等。而现在 Emmet 就是为了提高代码编写的效率而诞生的，它提供了一种非常简练的语法规则，然后立刻生成对应的 HTML 结构或者 CSS 代码，同时还有多种实用的功能帮助进行前端开发。

你可能听说过一款强大的功能相似的工具：Zen Coding，那个比较老了，而现在的 Emmet 则是 Zen Coding 的升级版，由 Zen Coding 的原作者进行开发等。 Emmet 严格意义上来说，并不是一款软件或者工具，它是一款编辑器插件，必须要基于某个编辑器使用。目前它支持如下编辑器：

Sublime Text 2
TextMate 1.x
Eclipse/Aptana
Coda 1.6 and 2.x
Espresso
Chocolat (可以通过 “Install Mixin” 对话框安装)
Komodo Edit/IDE ( Tools → Add-ons)
Notepad++
PSPad
<textarea>
CodeMirror2/3
Brackets
在上面列表点击你目前使用的编辑器，就可以获得对应的插件文件，安装之后就可以使用 Emmet 的相关功能了。由于 Sublime text 2 是目前最好最强大的前端开发代码编辑器，所以本文就以 Sublime text 2 为例，讲解 Emmet 的安装、基础语法。

在 Sublime text 2 中安装 Emmet
Sbulime text 2 安装插件肯定要通过 Package Control 这个插件了，如果你还没有安装这个插件，抓紧先去安装一下吧。安装完成之后，我们摁下“shift + ctrl + p”呼出面板，输入“pci”即可锁定“Package Control：Install Package”这个功能，回车之后就可以看到一个列表，我们继续输入“emmet”即可找到这个插件，回车之后等待一会就安装完成了。 

Visual Studio中的 Emmet 
在visual studio 中的插件管理中搜索Web Essentials这样一个插件，直接安装就行了。

开始使用 Emmet
Emmet 可以快速的编写 HTML 和 CSS 以及实现其他的功能。它根据当前文件的“语言”来判断要使用 HTML 语法还是 CSS 语法来解析。例如当前文件的后缀为 .html 那 Sublime text 2 就会用 HTML 的方式来解析高亮这个文件，Emmet 也会根据 HTML 的语法把你输入的指令编译成 HTML 结构。如果是在一个 .c 的 C语言 文件中，你根据 Emmet 的语法编写出来的指令，是不会被编译的。

此外，在没有后缀的文件中，你可以摁下“shift + ctrl + p”呼出面板，输入“seth”就可以选择当前文档是使用 HTML 的模式还是其他编程语言的模式来解释。下面就是一条 Emmet 的指令：

#page>div.logo+ul#navigation>li*5>a{Item $}
我们把它复制到 Sublime text 2 中已经打开的 HTML 文件中，这时候敲击一下 TAB 键，你就会发现这行指令变成了下面的 HTML 结构：

<div id="page">
    <div class="logo"></div>
    <ul id="navigation">
        <li><a href="">Item 1</a></li>
        <li><a href="">Item 2</a></li>
        <li><a href="">Item 3</a></li>
        <li><a href="">Item 4</a></li>
        <li><a href="">Item 5</a></li>
    </ul>
</div>
怎么样？很神奇吧，仅仅写一行代码，就可以生成这么一个复杂的 HTML 结构，而且还可以声称对应的 class 、id 和内容。这行指令你现在可能还看不懂，下面会详细讲解语法，你现在只需要知道 Emmet 的工作流程：打开 HTML 或 CSS 文件->按语法编写指令->摁下 TAB 键->生成！

Emmet 生成 HTML 结构基础语法
生成 HTML 文档初始结构 HTML 文档的初始结构，就是包括 doctype、html、head、body 以及 meta 等内容。你只需要输入一个 “!” 就可


1. 生成html格式
输入 html:5

 
2. 简写Div
分享7个超实用的Emmet（zen coding）HTML代码使用技巧

大家可以看到，不管你是否添加了div，Emmet都会自动生成需要div元素。

含糊标签名称
这个技巧属于implicit tag names特性，你不需要指定div或者li，Emmet会自动帮助你生成，如下：

分享7个超实用的Emmet（zen coding）HTML代码使用技巧

3. 带有DOM导航的链式缩写
如果你使用Emmet来扩展简单的class名称生成div的话。这个方式可以帮助你省去大量的时间。你只需要记住如下语法：

> 子节点：在DOM树下一层添加创建一个元素
+ 同级别：在DOM树同一层添加创建一个元素
^ 向上层：向上一层添加创建创建一个元素。
分享7个超实用的Emmet（zen coding）HTML代码使用技巧

分享7个超实用的Emmet（zen coding）HTML代码使用技巧

向上一层
分享7个超实用的Emmet（zen coding）HTML代码使用技巧

如果需要的话你可以向上多层，如下：

分享7个超实用的Emmet（zen coding）HTML代码使用技巧

4. 使用分组来简化你的代码结构
有的时候你可能会发现使用向上符号比较复杂，这时候可能使用分组更加的合理。如下：

分享7个超实用的Emmet（zen coding）HTML代码使用技巧

一个更复杂一些的例子，如下：

分享7个超实用的Emmet（zen coding）HTML代码使用技巧

5. 插入文本和属性
如果你需要生成HTML，内容和属性也是你常常需要添加的。很多开发人员只是使用Emmet来生成框架，然后再添加内容。其实你可以在生成页面框架的过程中同时添加属性和内容。

从下面代码可以看到，你输入的文字和属性都可以分别通过大括号和中括号来生成。

分享7个超实用的Emmet（zen coding）HTML代码使用技巧

6. 添加多个class到一个元素 
这个非常简单，你只需要使用逗号来添加多个class，如下：

分享7个超实用的Emmet（zen coding）HTML代码使用技巧

7.  重复添加
这可能是最让人舒服的操作了，帮助你重复添加元素：

分享7个超实用的Emmet（zen coding）HTML代码使用技巧

如果你整合分组功能，那么你将能够处理更复杂的HTML生成：

分享7个超实用的Emmet（zen coding）HTML代码使用技巧

8. 自动列表记数 
如果你需要按顺序生成HTML元素，这个技巧你一定喜欢，使用$符号可以帮助你生成一系列数字，支持class，id，属性，内容等等。如下：

分享7个超实用的Emmet（zen coding）HTML代码使用技巧

注意如果你需要生成2位的数字，使用两个$符号即可。 



补充阅读：http://docs.emmet.io/cheat-sheet/

 

Syntax

Child: >

nav>ul>li

<nav>    <ul>        <li></li>    </ul> </nav>

Sibling: +

div+p+bq

<div></div> <p></p> <blockquote></blockquote>

Climb-up: ^

div+div>p>span+em^bq

<div></div> <div>    <p><span></span><em></em></p>    <blockquote></blockquote> </div>

div+div>p>span+em^^bq

<div></div> <div>    <p><span></span><em></em></p> </div> <blockquote></blockquote>

Grouping: ()

div>(header>ul>li*2>a)+footer>p

<div>    <header>        <ul>            <li><a href=""></a></li>            <li><a href=""></a></li>        </ul>    </header>    <footer>        <p></p>    </footer> </div>

(div>dl>(dt+dd)*3)+footer>p

<div>    <dl>        <dt></dt>        <dd></dd>        <dt></dt>        <dd></dd>        <dt></dt>        <dd></dd>    </dl> </div> <footer>    <p></p> </footer>

Multiplication: *

ul>li*5

<ul>    <li></li>    <li></li>    <li></li>    <li></li>    <li></li> </ul>

Item numbering: $

ul>li.item$*5

<ul>    <li class="item1"></li>    <li class="item2"></li>    <li class="item3"></li>    <li class="item4"></li>    <li class="item5"></li> </ul>

h$[title=item$]{Header $}*3

<h1 title="item1">Header 1</h1> <h2 title="item2">Header 2</h2> <h3 title="item3">Header 3</h3>

ul>li.item$$$*5

<ul>    <li class="item001"></li>    <li class="item002"></li>    <li class="item003"></li>    <li class="item004"></li>    <li class="item005"></li> </ul>

ul>li.item$@-*5

<ul>    <li class="item5"></li>    <li class="item4"></li>    <li class="item3"></li>    <li class="item2"></li>    <li class="item1"></li> </ul>

ul>li.item$@3*5

<ul>    <li class="item3"></li>    <li class="item4"></li>    <li class="item5"></li>    <li class="item6"></li>    <li class="item7"></li> </ul>

ID and CLASS attributes

#header

<div id="header"></div>

.title

<div class="title"></div>

form#search.wide

<form id="search" class="wide"></form>

p.class1.class2.class3

<p class="class1 class2 class3"></p>

Custom attributes

p[title="Hello world"]

<p title="Hello world"></p>

td[rowspan=2 colspan=3 title]

<td rowspan="2" colspan="3" title=""></td>

[a='value1' b="value2"]

<div a="value1" b="value2"></div>

Text: {}

a{Click me}

<a href="">Click me</a>

p>{Click }+a{here}+{ to continue}

<p>Click <a href="">here</a> to continue</p>

Implicit tag names

.class

<div class="class"></div>

em>.class

<em><span class="class"></span></em>

ul>.class

<ul>    <li class="class"></li> </ul>

table>.row>.col

<table>    <tr class="row">        <td class="col"></td>    </tr> </table>

 

HTML

All unknown abbreviations will be transformed to tag, e.g. foo → <foo></foo>.

!

Alias of html:5

<!DOCTYPE html> <html lang="en"> <head>    <meta charset="UTF-8" />    <title>Document</title> </head> <body>    </body> </html>

a

<a href=""></a>

a:link

<a href="http://"></a>

a:mail

<a href="mailto:"></a>

abbr

<abbr title=""></abbr>

acronym, acr

<acronym title=""></acronym>

base

<base href="" />

basefont

<basefont />

br

<br />

frame

<frame />

hr

<hr />

bdo

<bdo dir=""></bdo>

bdo:r

<bdo dir="rtl"></bdo>

bdo:l

<bdo dir="ltr"></bdo>

col

<col />

link

<link rel="stylesheet" href="" />

link:css

<link rel="stylesheet" href="style.css" />

link:print

<link rel="stylesheet" href="print.css" media="print" />

link:favicon

<link rel="shortcut icon" type="image/x-icon" href="favicon.ico" />

link:touch

<link rel="apple-touch-icon" href="favicon.png" />

link:rss

<link rel="alternate" type="application/rss+xml" title="RSS" href="rss.xml" />

link:atom

<link rel="alternate" type="application/atom+xml" title="Atom" href="atom.xml" />

link:import, link:im

<link rel="import" href="component.html" />

meta

<meta />

meta:utf

<meta http-equiv="Content-Type" content="text/html;charset=UTF-8" />

meta:win

<meta http-equiv="Content-Type" content="text/html;charset=windows-1251" />

meta:vp

<meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0" />

meta:compat

<meta http-equiv="X-UA-Compatible" content="IE=7" />

style

<style></style>

script

<script></script>

script:src

<script src=""></script>

img

<img src="" alt="" />

img:srcset, img:s

<img srcset="" src="" alt="" />

img:sizes, img:z

<img sizes="" srcset="" src="" alt="" />

picture

<picture></picture>

source, src

<source />

source:src, src:sc

<source src="" type="" />

source:srcset, src:s

<source srcset="" />

source:media, src:m

<source media="(min-width: )" srcset="" />

source:type, src:t

<source srcset="" type="image/" />

source:sizes, src:z

<source sizes="" srcset="" />

source:media:type, src:mt

<source media="(min-width: )" srcset="" type="image/" />

source:media:sizes, src:mz

<source media="(min-width: )" sizes="" srcset="" />

source:sizes:type, src:zt

<source sizes="" srcset="" type="image/" />

iframe

<iframe src="" frameborder="0"></iframe>

embed

<embed src="" type="" />

object

<object data="" type=""></object>

param

<param name="" value="" />

map

<map name=""></map>

area

<area shape="" coords="" href="" alt="" />

area:d

<area shape="default" href="" alt="" />

area:c

<area shape="circle" coords="" href="" alt="" />

area:r

<area shape="rect" coords="" href="" alt="" />

area:p

<area shape="poly" coords="" href="" alt="" />

form

<form action=""></form>

form:get

<form action="" method="get"></form>

form:post

<form action="" method="post"></form>

label

<label for=""></label>

input

<input type="text" />

inp

<input type="text" name="" id="" />

input:hidden, input:h

Alias of input[type=hidden name]

<input type="hidden" name="" />

input:text, input:t

Alias of inp

<input type="text" name="" id="" />

input:search

Alias of inp[type=search]

<input type="search" name="" id="" />

input:email

Alias of inp[type=email]

<input type="email" name="" id="" />

input:url

Alias of inp[type=url]

<input type="url" name="" id="" />

input:password, input:p

Alias of inp[type=password]

<input type="password" name="" id="" />

input:datetime

Alias of inp[type=datetime]

<input type="datetime" name="" id="" />

input:date

Alias of inp[type=date]

<input type="date" name="" id="" />

input:datetime-local

Alias of inp[type=datetime-local]

<input type="datetime-local" name="" id="" />

input:month

Alias of inp[type=month]

<input type="month" name="" id="" />

input:week

Alias of inp[type=week]

<input type="week" name="" id="" />

input:time

Alias of inp[type=time]

<input type="time" name="" id="" />

input:tel

Alias of inp[type=tel]

<input type="tel" name="" id="" />

input:number

Alias of inp[type=number]

<input type="number" name="" id="" />

input:color

Alias of inp[type=color]

<input type="color" name="" id="" />

input:checkbox, input:c

Alias of inp[type=checkbox]

<input type="checkbox" name="" id="" />

input:radio, input:r

Alias of inp[type=radio]

<input type="radio" name="" id="" />

input:range

Alias of inp[type=range]

<input type="range" name="" id="" />

input:file, input:f

Alias of inp[type=file]

<input type="file" name="" id="" />

input:submit, input:s

<input type="submit" value="" />

input:image, input:i

<input type="image" src="" alt="" />

input:button, input:b

<input type="button" value="" />

isindex

<isindex />

input:reset

Alias of input:button[type=reset]

<input type="reset" value="" />

select

<select name="" id=""></select>

select:disabled, select:d

Alias of select[disabled.]

<select name="" id="" disabled="disabled"></select>

option, opt

<option value=""></option>

textarea

<textarea name="" id="" cols="30" rows="10"></textarea>

marquee

<marquee behavior="" direction=""></marquee>

menu:context, menu:c

Alias of menu[type=context]>

<menu type="context"></menu>

menu:toolbar, menu:t

Alias of menu[type=toolbar]>

<menu type="toolbar"></menu>

video

<video src=""></video>

audio

<audio src=""></audio>

html:xml

<html xmlns="http://www.w3.org/1999/xhtml"></html>

keygen

<keygen />

command

<command />

button:submit, button:s, btn:s

Alias of button[type=submit]

<button type="submit"></button>

button:reset, button:r, btn:r

Alias of button[type=reset]

<button type="reset"></button>

button:disabled, button:d, btn:d

Alias of button[disabled.]

<button disabled="disabled"></button>

fieldset:disabled, fieldset:d, fset:d, fst:d

Alias of fieldset[disabled.]

<fieldset disabled="disabled"></fieldset>

bq

Alias of blockquote

<blockquote></blockquote>

fig

Alias of figure

<figure></figure>

figc

Alias of figcaption

<figcaption></figcaption>

pic

Alias of picture

<picture></picture>

ifr

Alias of iframe

<iframe src="" frameborder="0"></iframe>

emb

Alias of embed

<embed src="" type="" />

obj

Alias of object

<object data="" type=""></object>

cap

Alias of caption

<caption></caption>

colg

Alias of colgroup

<colgroup></colgroup>

fst, fset

Alias of fieldset

<fieldset></fieldset>

btn

Alias of button

<button></button>

optg

Alias of optgroup

<optgroup></optgroup>

tarea

Alias of textarea

<textarea name="" id="" cols="30" rows="10"></textarea>

leg

Alias of legend

<legend></legend>

sect

Alias of section

<section></section>

art

Alias of article

<article></article>

hdr

Alias of header

<header></header>

ftr

Alias of footer

<footer></footer>

adr

Alias of address

<address></address>

dlg

Alias of dialog

<dialog></dialog>

str

Alias of strong

<strong></strong>

prog

Alias of progress

<progress></progress>

mn

Alias of main

<main></main>

tem

Alias of template

<template></template>

datag

Alias of datagrid

<datagrid></datagrid>

datal

Alias of datalist

<datalist></datalist>

kg

Alias of keygen

<keygen />

out

Alias of output

<output></output>

det

Alias of details

<details></details>

cmd

Alias of command

<command />

doc

Alias of html>(head>meta[charset=${charset}]+title[ERR:未定义的系统标签({1:Document}})+body

<html> <head>    <meta charset="UTF-8" />    <title>Document</title> </head> <body>    </body> </html>

doc4

Alias of html>(head>meta[http-equiv="Content-Type" content="text/html;charset=${charset}"]+title{1:Document}})+body

<html> <head>    <meta http-equiv="Content-Type" content="text/html;charset=UTF-8" />    <title>Document</title> </head> <body>    </body> </html>

ri:dpr, ri:d

Alias of img:s

<img srcset="" src="" alt="" />

ri:viewport, ri:v

Alias of img:z

<img sizes="" srcset="" src="" alt="" />

ri:art, ri:a

Alias of pic>src:m+img

<picture>    <source media="(min-width: )" srcset="" />    <img src="" alt="" /> </picture>

ri:type, ri:t

Alias of pic>src:t+img

<picture>    <source srcset="" type="image/" />    <img src="" alt="" /> </picture>

html:4t

Alias of !!!4t+doc4[lang=${lang}]

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd"> <html lang="en"> <head>    <meta http-equiv="Content-Type" content="text/html;charset=UTF-8" />    <title>Document</title> </head> <body>    </body> </html>

html:4s

Alias of !!!4s+doc4[lang=${lang}]

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd"> <html lang="en"> <head>    <meta http-equiv="Content-Type" content="text/html;charset=UTF-8" />    <title>Document</title> </head> <body>    </body> </html>

html:xt

Alias of !!!xt+doc4[xmlns=http://www.w3.org/1999/xhtml xml:lang=${lang}]

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en"> <head>    <meta http-equiv="Content-Type" content="text/html;charset=UTF-8" />    <title>Document</title> </head> <body>    </body> </html>

html:xs

Alias of !!!xs+doc4[xmlns=http://www.w3.org/1999/xhtml xml:lang=${lang}]

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd"> <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en"> <head>    <meta http-equiv="Content-Type" content="text/html;charset=UTF-8" />    <title>Document</title> </head> <body>    </body> </html>

html:xxs

Alias of !!!xxs+doc4[xmlns=http://www.w3.org/1999/xhtml xml:lang=${lang}]

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd"> <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en"> <head>    <meta http-equiv="Content-Type" content="text/html;charset=UTF-8" />    <title>Document</title> </head> <body>    </body> </html>

html:5

Alias of !!!+doc[lang=${lang}]

<!DOCTYPE html> <html lang="en"> <head>    <meta charset="UTF-8" />    <title>Document</title> </head> <body>    </body> </html>

ol+

Alias of ol>li

<ol>    <li></li> </ol>

ul+

Alias of ul>li

<ul>    <li></li> </ul>

dl+

Alias of dl>dt+dd

<dl>    <dt></dt>    <dd></dd> </dl>

map+

Alias of map>area

<map name="">    <area shape="" coords="" href="" alt="" /> </map>

table+

Alias of table>tr>td

<table>    <tr>        <td></td>    </tr> </table>

colgroup+, colg+

Alias of colgroup>col

<colgroup>    <col /> </colgroup>

tr+

Alias of tr>td

<tr>    <td></td> </tr>

select+

Alias of select>option

<select name="" id="">    <option value=""></option> </select>

optgroup+, optg+

Alias of optgroup>option

<optgroup>    <option value=""></option> </optgroup>

pic+

Alias of picture>source:srcset+img

<picture>    <source srcset="" />    <img src="" alt="" /> </picture>

!!!

<!DOCTYPE html>

!!!4t

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">

!!!4s

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">

!!!xt

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">

!!!xs

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">

!!!xxs

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">

c

<!-- ${child} -->

cc:ie6

<!--[if lte IE 6]>    ${child}<![endif]-->

cc:ie

<!--[if IE]>    ${child}<![endif]-->

cc:noie

<!--[if !IE]><!-->    ${child}<!--<![endif]-->

CSS

CSS module uses fuzzy search to find unknown abbreviations, e.g. ov:h == ov-h == ovh == oh.

If abbreviation wasn’t found, it is transformed into property name: foo-bar → foo-bar: |;

You can prefix abbreviations with hyphen to produce vendor-prefixed properties: -foo

Visual Formatting

pos

position:relative;

pos:s

position:static;

pos:a

position:absolute;

pos:r

position:relative;

pos:f

position:fixed;

t

top:;

t:a

top:auto;

r

right:;

r:a

right:auto;

b

bottom:;

b:a

bottom:auto;

l

left:;

l:a

left:auto;

z

z-index:;

z:a

z-index:auto;

fl

float:left;

fl:n

float:none;

fl:l

float:left;

fl:r

float:right;

cl

clear:both;

cl:n

clear:none;

cl:l

clear:left;

cl:r

clear:right;

cl:b

clear:both;

d

display:block;

d:n

display:none;

d:b

display:block;

d:f

display:flex;

d:if

display:inline-flex;

d:i

display:inline;

d:ib

display:inline-block;

d:li

display:list-item;

d:ri

display:run-in;

d:cp

display:compact;

d:tb

display:table;

d:itb

display:inline-table;

d:tbcp

display:table-caption;

d:tbcl

display:table-column;

d:tbclg

display:table-column-group;

d:tbhg

display:table-header-group;

d:tbfg

display:table-footer-group;

d:tbr

display:table-row;

d:tbrg

display:table-row-group;

d:tbc

display:table-cell;

d:rb

display:ruby;

d:rbb

display:ruby-base;

d:rbbg

display:ruby-base-group;

d:rbt

display:ruby-text;

d:rbtg

display:ruby-text-group;

v

visibility:hidden;

v:v

visibility:visible;

v:h

visibility:hidden;

v:c

visibility:collapse;

ov

overflow:hidden;

ov:v

overflow:visible;

ov:h

overflow:hidden;

ov:s

overflow:scroll;

ov:a

overflow:auto;

ovx

overflow-x:hidden;

ovx:v

overflow-x:visible;

ovx:h

overflow-x:hidden;

ovx:s

overflow-x:scroll;

ovx:a

overflow-x:auto;

ovy

overflow-y:hidden;

ovy:v

overflow-y:visible;

ovy:h

overflow-y:hidden;

ovy:s

overflow-y:scroll;

ovy:a

overflow-y:auto;

ovs

overflow-style:scrollbar;

ovs:a

overflow-style:auto;

ovs:s

overflow-style:scrollbar;

ovs:p

overflow-style:panner;

ovs:m

overflow-style:move;

ovs:mq

overflow-style:marquee;

zoo, zm

zoom:1;

cp

clip:;

cp:a

clip:auto;

cp:r

clip:rect(top right bottom left);

rsz

resize:;

rsz:n

resize:none;

rsz:b

resize:both;

rsz:h

resize:horizontal;

rsz:v

resize:vertical;

cur

cursor:${pointer};

cur:a

cursor:auto;

cur:d

cursor:default;

cur:c

cursor:crosshair;

cur:ha

cursor:hand;

cur:he

cursor:help;

cur:m

cursor:move;

cur:p

cursor:pointer;

cur:t

cursor:text;

Margin & Padding

m

margin:;

m:a

margin:auto;

mt

margin-top:;

mt:a

margin-top:auto;

mr

margin-right:;

mr:a

margin-right:auto;

mb

margin-bottom:;

mb:a

margin-bottom:auto;

ml

margin-left:;

ml:a

margin-left:auto;

p

padding:;

pt

padding-top:;

pr

padding-right:;

pb

padding-bottom:;

pl

padding-left:;

Box Sizing

bxz

box-sizing:border-box;

bxz:cb

box-sizing:content-box;

bxz:bb

box-sizing:border-box;

bxsh

box-shadow:inset hoff voff blur color;

bxsh:r

box-shadow:inset hoff voff blur spread rgb(0, 0, 0);

bxsh:ra

box-shadow:inset h v blur spread rgba(0, 0, 0, .5);

bxsh:n

box-shadow:none;

w

width:;

w:a

width:auto;

h

height:;

h:a

height:auto;

maw

max-width:;

maw:n

max-width:none;

mah

max-height:;

mah:n

max-height:none;

miw

min-width:;

mih

min-height:;

Font

f

font:;

f+

font:1em Arial,sans-serif;

fw

font-weight:;

fw:n

font-weight:normal;

fw:b

font-weight:bold;

fw:br

font-weight:bolder;

fw:lr

font-weight:lighter;

fs

font-style:${italic};

fs:n

font-style:normal;

fs:i

font-style:italic;

fs:o

font-style:oblique;

fv

font-variant:;

fv:n

font-variant:normal;

fv:sc

font-variant:small-caps;

fz

font-size:;

fza

font-size-adjust:;

fza:n

font-size-adjust:none;

ff

font-family:;

ff:s

font-family:serif;

ff:ss

font-family:sans-serif;

ff:c

font-family:cursive;

ff:f

font-family:fantasy;

ff:m

font-family:monospace;

ff:a

font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;

ff:t

font-family: "Times New Roman", Times, Baskerville, Georgia, serif;

ff:v

font-family: Verdana, Geneva, sans-serif;

fef

font-effect:;

fef:n

font-effect:none;

fef:eg

font-effect:engrave;

fef:eb

font-effect:emboss;

fef:o

font-effect:outline;

fem

font-emphasize:;

femp

font-emphasize-position:;

femp:b

font-emphasize-position:before;

femp:a

font-emphasize-position:after;

fems

font-emphasize-style:;

fems:n

font-emphasize-style:none;

fems:ac

font-emphasize-style:accent;

fems:dt

font-emphasize-style:dot;

fems:c

font-emphasize-style:circle;

fems:ds

font-emphasize-style:disc;

fsm

font-smooth:;

fsm:a

font-smooth:auto;

fsm:n

font-smooth:never;

fsm:aw

font-smooth:always;

fst

font-stretch:;

fst:n

font-stretch:normal;

fst:uc

font-stretch:ultra-condensed;

fst:ec

font-stretch:extra-condensed;

fst:c

font-stretch:condensed;

fst:sc

font-stretch:semi-condensed;

fst:se

font-stretch:semi-expanded;

fst:e

font-stretch:expanded;

fst:ee

font-stretch:extra-expanded;

fst:ue

font-stretch:ultra-expanded;

Text

va

vertical-align:top;

va:sup

vertical-align:super;

va:t

vertical-align:top;

va:tt

vertical-align:text-top;

va:m

vertical-align:middle;

va:bl

vertical-align:baseline;

va:b

vertical-align:bottom;

va:tb

vertical-align:text-bottom;

va:sub

vertical-align:sub;

ta

text-align:left;

ta:l

text-align:left;

ta:c

text-align:center;

ta:r

text-align:right;

ta:j

text-align:justify;

ta-lst

text-align-last:;

tal:a

text-align-last:auto;

tal:l

text-align-last:left;

tal:c

text-align-last:center;

tal:r

text-align-last:right;

td

text-decoration:none;

td:n

text-decoration:none;

td:u

text-decoration:underline;

td:o

text-decoration:overline;

td:l

text-decoration:line-through;

te

text-emphasis:;

te:n

text-emphasis:none;

te:ac

text-emphasis:accent;

te:dt

text-emphasis:dot;

te:c

text-emphasis:circle;

te:ds

text-emphasis:disc;

te:b

text-emphasis:before;

te:a

text-emphasis:after;

th

text-height:;

th:a

text-height:auto;

th:f

text-height:font-size;

th:t

text-height:text-size;

th:m

text-height:max-size;

ti

text-indent:;

ti:-

text-indent:-9999px;

tj

text-justify:;

tj:a

text-justify:auto;

tj:iw

text-justify:inter-word;

tj:ii

text-justify:inter-ideograph;

tj:ic

text-justify:inter-cluster;

tj:d

text-justify:distribute;

tj:k

text-justify:kashida;

tj:t

text-justify:tibetan;

to

text-outline:;

to+

text-outline:0 0 #000;

to:n

text-outline:none;

tr

text-replace:;

tr:n

text-replace:none;

tt

text-transform:uppercase;

tt:n

text-transform:none;

tt:c

text-transform:capitalize;

tt:u

text-transform:uppercase;

tt:l

text-transform:lowercase;

tw

text-wrap:;

tw:n

text-wrap:normal;

tw:no

text-wrap:none;

tw:u

text-wrap:unrestricted;

tw:s

text-wrap:suppress;

tsh

text-shadow:hoff voff blur #000;

tsh:r

text-shadow:h v blur rgb(0, 0, 0);

tsh:ra

text-shadow:h v blur rgba(0, 0, 0, .5);

tsh+

text-shadow:0 0 0 #000;

tsh:n

text-shadow:none;

lh

line-height:;

lts

letter-spacing:;

lts-n

letter-spacing:normal;

whs

white-space:;

whs:n

white-space:normal;

whs:p

white-space:pre;

whs:nw

white-space:nowrap;

whs:pw

white-space:pre-wrap;

whs:pl

white-space:pre-line;

whsc

white-space-collapse:;

whsc:n

white-space-collapse:normal;

whsc:k

white-space-collapse:keep-all;

whsc:l

white-space-collapse:loose;

whsc:bs

white-space-collapse:break-strict;

whsc:ba

white-space-collapse:break-all;

wob

word-break:;

wob:n

word-break:normal;

wob:k

word-break:keep-all;

wob:ba

word-break:break-all;

wos

word-spacing:;

wow

word-wrap:;

wow:nm

word-wrap:normal;

wow:n

word-wrap:none;

wow:u

word-wrap:unrestricted;

wow:s

word-wrap:suppress;

wow:b

word-wrap:break-word;

Background

bg

background:#000;

bg+

background:#fff url() 0 0 no-repeat;

bg:n

background:none;

bgc

background-color:#fff;

bgc:t

background-color:transparent;

bgi

background-image:url();

bgi:n

background-image:none;

bgr

background-repeat:;

bgr:n

background-repeat:no-repeat;

bgr:x

background-repeat:repeat-x;

bgr:y

background-repeat:repeat-y;

bgr:sp

background-repeat:space;

bgr:rd

background-repeat:round;

bga

background-attachment:;

bga:f

background-attachment:fixed;

bga:s

background-attachment:scroll;

bgp

background-position:0 0;

bgpx

background-position-x:;

bgpy

background-position-y:;

bgbk

background-break:;

bgbk:bb

background-break:bounding-box;

bgbk:eb

background-break:each-box;

bgbk:c

background-break:continuous;

bgcp

background-clip:padding-box;

bgcp:bb

background-clip:border-box;

bgcp:pb

background-clip:padding-box;

bgcp:cb

background-clip:content-box;

bgcp:nc

background-clip:no-clip;

bgo

background-origin:;

bgo:pb

background-origin:padding-box;

bgo:bb

background-origin:border-box;

bgo:cb

background-origin:content-box;

bgsz

background-size:;

bgsz:a

background-size:auto;

bgsz:ct

background-size:contain;

bgsz:cv

background-size:cover;

Color

c

color:#000;

c:r

color:rgb(0, 0, 0);

c:ra

color:rgba(0, 0, 0, .5);

op

opacity:;

Generated content

cnt

content:'';

cnt:n, ct:n

content:normal;

cnt:oq, ct:oq

content:open-quote;

cnt:noq, ct:noq

content:no-open-quote;

cnt:cq, ct:cq

content:close-quote;

cnt:ncq, ct:ncq

content:no-close-quote;

cnt:a, ct:a

content:attr();

cnt:c, ct:c

content:counter();

cnt:cs, ct:cs

content:counters();

ct

content:;

q

quotes:;

q:n

quotes:none;

q:ru

quotes:'\00AB' '\00BB' '\201E' '\201C';

q:en

quotes:'\201C' '\201D' '\2018' '\2019';

coi

counter-increment:;

cor

counter-reset:;

Outline

ol

outline:;

ol:n

outline:none;

olo

outline-offset:;

olw

outline-width:;

olw:tn

outline-width:thin;

olw:m

outline-width:medium;

olw:tc

outline-width:thick;

ols

outline-style:;

ols:n

outline-style:none;

ols:dt

outline-style:dotted;

ols:ds

outline-style:dashed;

ols:s

outline-style:solid;

ols:db

outline-style:double;

ols:g

outline-style:groove;

ols:r

outline-style:ridge;

ols:i

outline-style:inset;

ols:o

outline-style:outset;

olc

outline-color:#000;

olc:i

outline-color:invert;

Tables

tbl

table-layout:;

tbl:a

table-layout:auto;

tbl:f

table-layout:fixed;

cps

caption-side:;

cps:t

caption-side:top;

cps:b

caption-side:bottom;

ec

empty-cells:;

ec:s

empty-cells:show;

ec:h

empty-cells:hide;

Border

bd

border:;

bd+

border:1px solid #000;

bd:n

border:none;

bdbk

border-break:close;

bdbk:c

border-break:close;

bdcl

border-collapse:;

bdcl:c

border-collapse:collapse;

bdcl:s

border-collapse:separate;

bdc

border-color:#000;

bdc:t

border-color:transparent;

bdi

border-image:url();

bdi:n

border-image:none;

bdti

border-top-image:url();

bdti:n

border-top-image:none;

bdri

border-right-image:url();

bdri:n

border-right-image:none;

bdbi

border-bottom-image:url();

bdbi:n

border-bottom-image:none;

bdli

border-left-image:url();

bdli:n

border-left-image:none;

bdci

border-corner-image:url();

bdci:n

border-corner-image:none;

bdci:c

border-corner-image:continue;

bdtli

border-top-left-image:url();

bdtli:n

border-top-left-image:none;

bdtli:c

border-top-left-image:continue;

bdtri

border-top-right-image:url();

bdtri:n

border-top-right-image:none;

bdtri:c

border-top-right-image:continue;

bdbri

border-bottom-right-image:url();

bdbri:n

border-bottom-right-image:none;

bdbri:c

border-bottom-right-image:continue;

bdbli

border-bottom-left-image:url();

bdbli:n

border-bottom-left-image:none;

bdbli:c

border-bottom-left-image:continue;

bdf

border-fit:repeat;

bdf:c

border-fit:clip;

bdf:r

border-fit:repeat;

bdf:sc

border-fit:scale;

bdf:st

border-fit:stretch;

bdf:ow

border-fit:overwrite;

bdf:of

border-fit:overflow;

bdf:sp

border-fit:space;

bdlen

border-length:;

bdlen:a

border-length:auto;

bdsp

border-spacing:;

bds

border-style:;

bds:n

border-style:none;

bds:h

border-style:hidden;

bds:dt

border-style:dotted;

bds:ds

border-style:dashed;

bds:s

border-style:solid;

bds:db

border-style:double;

bds:dtds

border-style:dot-dash;

bds:dtdtds

border-style:dot-dot-dash;

bds:w

border-style:wave;

bds:g

border-style:groove;

bds:r

border-style:ridge;

bds:i

border-style:inset;

bds:o

border-style:outset;

bdw

border-width:;

bdt, bt

border-top:;

bdt+

border-top:1px solid #000;

bdt:n

border-top:none;

bdtw

border-top-width:;

bdts

border-top-style:;

bdts:n

border-top-style:none;

bdtc

border-top-color:#000;

bdtc:t

border-top-color:transparent;

bdr, br

border-right:;

bdr+

border-right:1px solid #000;

bdr:n

border-right:none;

bdrw

border-right-width:;

bdrst

border-right-style:;

bdrst:n

border-right-style:none;

bdrc

border-right-color:#000;

bdrc:t

border-right-color:transparent;

bdb, bb

border-bottom:;

bdb+

border-bottom:1px solid #000;

bdb:n

border-bottom:none;

bdbw

border-bottom-width:;

bdbs

border-bottom-style:;

bdbs:n

border-bottom-style:none;

bdbc

border-bottom-color:#000;

bdbc:t

border-bottom-color:transparent;

bdl, bl

border-left:;

bdl+

border-left:1px solid #000;

bdl:n

border-left:none;

bdlw

border-left-width:;

bdls

border-left-style:;

bdls:n

border-left-style:none;

bdlc

border-left-color:#000;

bdlc:t

border-left-color:transparent;

bdrs

border-radius:;

bdtrrs

border-top-right-radius:;

bdtlrs

border-top-left-radius:;

bdbrrs

border-bottom-right-radius:;

bdblrs

border-bottom-left-radius:;

Lists

lis

list-style:;

lis:n

list-style:none;

lisp

list-style-position:;

lisp:i

list-style-position:inside;

lisp:o

list-style-position:outside;

list

list-style-type:;

list:n

list-style-type:none;

list:d

list-style-type:disc;

list:c

list-style-type:circle;

list:s

list-style-type:square;

list:dc

list-style-type:decimal;

list:dclz

list-style-type:decimal-leading-zero;

list:lr

list-style-type:lower-roman;

list:ur

list-style-type:upper-roman;

lisi

list-style-image:;

lisi:n

list-style-image:none;

Print

pgbb

page-break-before:;

pgbb:au

page-break-before:auto;

pgbb:al

page-break-before:always;

pgbb:l

page-break-before:left;

pgbb:r

page-break-before:right;

pgbi

page-break-inside:;

pgbi:au

page-break-inside:auto;

pgbi:av

page-break-inside:avoid;

pgba

page-break-after:;

pgba:au

page-break-after:auto;

pgba:al

page-break-after:always;

pgba:l

page-break-after:left;

pgba:r

page-break-after:right;

orp

orphans:;

wid

widows:;

Others

!

!important

@f

@font-face {    font-family:;    src:url(|); }

@f+

@font-face {    font-family: 'FontName';    src: url('FileName.eot');    src: url('FileName.eot?#iefix') format('embedded-opentype'),         url('FileName.woff') format('woff'),         url('FileName.ttf') format('truetype'),         url('FileName.svg#FontName') format('svg');    font-style: normal;    font-weight: normal; }

@i, @import

@import url();

@kf

@-webkit-keyframes identifier {    from { }    to { } } @-o-keyframes identifier {    from { }    to { } } @-moz-keyframes identifier {    from { }    to { } } @keyframes identifier {    from { }    to { } }

@m, @media

@media screen {    }

ac

align-content:;

ac:c

align-content:center;

ac:fe

align-content:flex-end;

ac:fs

align-content:flex-start;

ac:s

align-content:stretch;

ac:sa

align-content:space-around;

ac:sb

align-content:space-between;

ai

align-items:;

ai:b

align-items:baseline;

ai:c

align-items:center;

ai:fe

align-items:flex-end;

ai:fs

align-items:flex-start;

ai:s

align-items:stretch;

anim

animation:;

anim-

animation:name duration timing-function delay iteration-count direction fill-mode;

animdel

animation-delay:time;

animdir

animation-direction:normal;

animdir:a

animation-direction:alternate;

animdir:ar

animation-direction:alternate-reverse;

animdir:n

animation-direction:normal;

animdir:r

animation-direction:reverse;

animdur

animation-duration:0s;

animfm

animation-fill-mode:both;

animfm:b

animation-fill-mode:backwards;

animfm:bt, animfm:bh

animation-fill-mode:both;

animfm:f

animation-fill-mode:forwards;

animic

animation-iteration-count:1;

animic:i

animation-iteration-count:infinite;

animn

animation-name:none;

animps

animation-play-state:running;

animps:p

animation-play-state:paused;

animps:r

animation-play-state:running;

animtf

animation-timing-function:linear;

animtf:cb

animation-timing-function:cubic-bezier(0.1, 0.7, 1.0, 0.1);

animtf:e

animation-timing-function:ease;

animtf:ei

animation-timing-function:ease-in;

animtf:eio

animation-timing-function:ease-in-out;

animtf:eo

animation-timing-function:ease-out;

animtf:l

animation-timing-function:linear;

ap

appearance:${none};

as

align-self:;

as:a

align-self:auto;

as:b

align-self:baseline;

as:c

align-self:center;

as:fe

align-self:flex-end;

as:fs

align-self:flex-start;

as:s

align-self:stretch;

bfv

backface-visibility:;

bfv:h

backface-visibility:hidden;

bfv:v

backface-visibility:visible;

bg:ie

filter:progid:DXImageTransform.Microsoft.AlphaImageLoader(src='x.png',sizingMethod='crop');

cm

/* ${child} */

colm

columns:;

colmc

column-count:;

colmf

column-fill:;

colmg

column-gap:;

colmr

column-rule:;

colmrc

column-rule-color:;

colmrs

column-rule-style:;

colmrw

column-rule-width:;

colms

column-span:;

colmw

column-width:;

d:ib+

display: inline-block; *display: inline; *zoom: 1;

fx

flex:;

fxb

flex-basis:;

fxd

flex-direction:;

fxd:c

flex-direction:column;

fxd:cr

flex-direction:column-reverse;

fxd:r

flex-direction:row;

fxd:rr

flex-direction:row-reverse;

fxf

flex-flow:;

fxg

flex-grow:;

fxsh

flex-shrink:;

fxw

flex-wrap: ;

fxw:n

flex-wrap:nowrap;

fxw:w

flex-wrap:wrap;

fxw:wr

flex-wrap:wrap-reverse;

jc

justify-content:;

jc:c

justify-content:center;

jc:fe

justify-content:flex-end;

jc:fs

justify-content:flex-start;

jc:sa

justify-content:space-around;

jc:sb

justify-content:space-between;

mar

max-resolution:res;

mir

min-resolution:res;

op+

opacity: ; filter: alpha(opacity=);

op:ie

filter:progid:DXImageTransform.Microsoft.Alpha(Opacity=100);

op:ms

-ms-filter:'progid:DXImageTransform.Microsoft.Alpha(Opacity=100)';

ord

order:;

ori

orientation:;

ori:l

orientation:landscape;

ori:p

orientation:portrait;

tov

text-overflow:${ellipsis};

tov:c

text-overflow:clip;

tov:e

text-overflow:ellipsis;

trf

transform:;

trf:r

transform: rotate(angle);

trf:rx

transform: rotateX(angle);

trf:ry

transform: rotateY(angle);

trf:rz

transform: rotateZ(angle);

trf:sc

transform: scale(x, y);

trf:sc3

transform: scale3d(x, y, z);

trf:scx

transform: scaleX(x);

trf:scy

transform: scaleY(y);

trf:scz

transform: scaleZ(z);

trf:skx

transform: skewX(angle);

trf:sky

transform: skewY(angle);

trf:t

transform: translate(x, y);

trf:t3

transform: translate3d(tx, ty, tz);

trf:tx

transform: translateX(x);

trf:ty

transform: translateY(y);

trf:tz

transform: translateZ(z);

trfo

transform-origin:;

trfs

transform-style:preserve-3d;

trs

transition:prop time;

trsde

transition-delay:time;

trsdu

transition-duration:time;

trsp

transition-property:prop;

trstf

transition-timing-function:tfunc;

us

user-select:${none};

wfsm

-webkit-font-smoothing:${antialiased};

wfsm:a

-webkit-font-smoothing:antialiased;

wfsm:n

-webkit-font-smoothing:none;

wfsm:s, wfsm:sa

-webkit-font-smoothing:subpixel-antialiased;

wm

writing-mode:lr-tb;

wm:btl

writing-mode:bt-lr;

wm:btr

writing-mode:bt-rl;

wm:lrb

writing-mode:lr-bt;

wm:lrt

writing-mode:lr-tb;

wm:rlb

writing-mode:rl-bt;

wm:rlt

writing-mode:rl-tb;

wm:tbl

writing-mode:tb-lr;

wm:tbr

writing-mode:tb-rl;

 

XSL

tmatch, tm

<xsl:template match="" mode=""></xsl:template>

tname, tn

<xsl:template name=""></xsl:template>

call

<xsl:call-template name="" />

ap

<xsl:apply-templates select="" mode="" />

api

<xsl:apply-imports />

imp

<xsl:import href="" />

inc

<xsl:include href="" />

ch

<xsl:choose></xsl:choose>

xsl:when, wh

<xsl:when test=""></xsl:when>

ot

<xsl:otherwise></xsl:otherwise>

if

<xsl:if test=""></xsl:if>

par

<xsl:param name=""></xsl:param>

pare

<xsl:param name="" select="" />

var

<xsl:variable name=""></xsl:variable>

vare

<xsl:variable name="" select="" />

wp

<xsl:with-param name="" select="" />

key

<xsl:key name="" match="" use="" />

elem

<xsl:element name=""></xsl:element>

attr

<xsl:attribute name=""></xsl:attribute>

attrs

<xsl:attribute-set name=""></xsl:attribute-set>

cp

<xsl:copy select="" />

co

<xsl:copy-of select="" />

val

<xsl:value-of select="" />

each, for

<xsl:for-each select=""></xsl:for-each>

tex

<xsl:text></xsl:text>

com

<xsl:comment></xsl:comment>

msg

<xsl:message terminate="no"></xsl:message>

fall

<xsl:fallback></xsl:fallback>

num

<xsl:number value="" />

详见：https://www.z01.com/blog/techs/2975.shtml
