title: 初赛基础
speaker: 缪慎浩
plugins:
    - echarts
    - katex
<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .anim">

# 初赛基础 {.text-landing.text-shadow}

By 缪慎浩 {.text-intro}

[洛谷团队](https://www.luogu.org/team/show?teamid=10342){.button.ghost}

<slide class="aligncenter">

## What will we learn?

<slide class = "aligncenter" image="http://www.manpingou.com/uploads/allimg/190620/25-1Z620092054N8-lp.jpg .anim">
:::{.content-left}
## :fa-quote-left: 我们今天要火箭速度，一中午解决12个知识点。
<slide class = "slide-top">
:::{.content-left}
### Contents
***
- [计算机语言](#slide=5){.animated.fadeInUp}
- [:fa-star:数制转换](#slide=9){.animated.fadeInUp}
- [信息编码](#slide=12){.animated.fadeInUp}
- [信息安全](#slide=13){.animated.fadeInUp}
- [:fa-star:数在计算机中的表示](#slide=14){.animated.fadeInUp}
- [计算机网络](#slide=3){.animated.fadeInUp}
- [硬件常识](#slide=3){.animated.fadeInUp}
:::
:::{.content-right}
### 打:fa-star:就是重点
***
- [算法常识](#slide=3){.animated.fadeInUp}
- [:fa-star:逻辑运算](#slide=3){.animated.fadeInUp}
- [:fa-star:栈](#slide=3){.animated.fadeInUp}
- [:fa-star:队列](#slide=3){.animated.fadeInUp}
- [:fa-star:树](#slide=3){.animated.fadeInUp}
- [:fa-star:图](#slide=3){.animated.fadeInUp}
- [组合数学（计数，组合](#slide=3){.animated.fadeInUp}
:::
<slide class="bg-black-blue slide-top">
## 计算机语言{.text-landing.text-shadow}
***
> #### *Some Concept*
>> 程序，是⼀系列的操作步骤，比如我们常说“做事要走程序”⽐如我们社团申请，举报学校就要走程序。

>> 计算机程序，就是⼈告诉计算机的⼀系列操作步骤，也就是⼀系列的指令。

>> 计算机语言，就是⼀种⼈⽤于与计算机进⾏沟通，下发指令的语言。

<slide class="slide-top">
:::{.content-left}
### 机器语言
***
我们知道，计算机内部是以二进制存储数据的。同理，对于指令自然也是以二进制存储的。

所以我们就可以直接用二进制代码来写程序，比如“计算8+4”就可以写为“00001000 00000100 00000100”。*但我们要知道不同CPU的指令集是不一样的*。

显然地，这玩意儿很反人类，但这是计算机可以*直接识别直接运行*的语言，故我们称之为“机器语言”。
:::
:::{.content-right}
### 汇编语言
***
由于二进制代码直接编程十分*蛋，聪明的人类就利用一些助记符，比如一些单词 “mov” 之类的来代替二进制码然后编程，这让编程轻松了很多，不过汇编程序必须经过翻译后才能运行。

然鹅由于汇编语言并没有做出本质上的改变，只是给二进制命令改了个名，我们仍将其称为低级语言。其具有编写逻辑困难并十分反智等特点，而且由于不同CPU指令集不同，所以汇编程序的可移植性也奇差。

:fa-star:**汇编程序速度并不一定是最快的。程序的运行速度只取决于最后的指令条数以及CPU执行速度。**
:::
<slide class="slide-top">
### 高级语言
***
到了高级语言，就比较像人说的语言了。但由于像人的语言，所以计算机常常是不能理解的。这时候就像汇编语言一样有一个翻译程序，但高级语言就不是简单的助记符替换了。高级编程语言一般分两种，编译型 语言和解释型语言。
***
:::div{.content-left}
编译型语言：C/C++  Basic
:::
:::div{.content-right}
解释型语言：PHP Python Swift Java Matlab
:::
***
这两者的运行特点就像他们的名字一样，编译型语言是编译一次就可以转成计算机可以直接运行的机器语言程序（如.exe文件）但是由于他们是直接编译的，依赖于计算机的不同，所以跨平台能力比较差，但是运行速度高。

解释性语言则是每次运行前编译，先解释再运行，导致运行效率降低，但是因为其依托于虚拟机/解释器所以跨平台性能好。

高级语言还可分为面向过程语言和面向对象语言。（区别自然是有没有对象）

<slide>
:::{.content-left}
### 碎片知识点：
***
- 于 1967 年出现的 Simula67 是历史上第一个面向对象语言
- Smalltalk 被公认为第二个面向对象的程序设计语言，和第一个IDE
- C 和 Pascal 是纯面向过程语言
- 就算没有对象也可以学面向对象的程序设计语言 C++
<slide class="slide-top bg-black-blue">
## 数制转换{.text-landing.text.shadow}
***
我们仅介绍十进制，二进制，八进制，十六进制的整数及有理数的相互转换。（高考也要求这个东西）

规定：数字后记B为二进制数，D为十进制数，O为八进制数，H为十六进制数。

    例子： 11001001B = 105D = 311O = D9H

<slide class="slide-top">
:::{.content-left}
### 二进制$\leftrightarrows$八进制$\leftrightarrows$十六进制
- O to B 把八进制一位换成二进制三位即可。（看举例）
- B to O 每三位转成8进制即可
- H to B 把每一位转换成二进制四位即可。
- B to H 每四位按权展开即可。
:::
:::{.content-right}
### 十进制$\leftrightarrows$二进制
- D to B 整数部分转为二进制整数可用“除二求余，逆序输出”的方法。
- D to B 小数部分转为二进制小数可用“乘二取整，顺序输出”的方法。（看黑板举例）
- B to D 直接按权值展开
- 注意：二进制无限循环小数可能是个十进制的有限小数，但是十进制无限循环小数，一定不会是个二进制有限小数
:::
<slide class="slide-top">
:::{.content-center}
### 课堂练兵 迅速口答
- $5D + 19H = ? B$
- $15O + 10010B = ? D$
- $98AH + 43D = ? O$
- $43D + 32O = ? H$
- $4O + 14H = ? B$
:::
<slide class="aligncenter bg-black-blue">
## 信息编码{.text-landing.text-shadow}

请自行阅读资料{.text-intro}

[获取资料](NOIP初赛复习.doc){.button.ghost}
<slide class="aligncenter bg-black-blue">
## 信息安全{.text-landing.text-shadow}

请自行阅读资料{.text-intro}

[获取资料](NOIP初赛复习.doc){.button.ghost}
<slide class="slide-top bg-black-blue">
## 数在计算机中的表示{.text-landing.text-shadow}
***
