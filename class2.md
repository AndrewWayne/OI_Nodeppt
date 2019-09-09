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
## :fa-quote-left: 我们今天要火箭速度，有12个知识点，还是得快一点。
<slide class = "slide-top">
:::{.content-left}
### Contents
***
- [计算机语言](#slide=5){.animated.fadeInUp}
- [:fa-star:数制转换](#slide=9){.animated.fadeInUp}
- [信息编码](#slide=12){.animated.fadeInUp}
- [信息安全](#slide=13){.animated.fadeInUp}
- [:fa-star:数在计算机中的表示](#slide=14){.animated.fadeInUp}
- [计算机网络](#slide=17){.animated.fadeInUp}
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
> #### *Some Concept*
>> 程序，是⼀系列的操作步骤，比如我们常说“做事要走程序”⽐如我们社团申请，举报学校就要走程序。

>> 计算机程序，就是⼈告诉计算机的⼀系列操作步骤，也就是⼀系列的指令。

>> 计算机语言，就是⼀种⼈⽤于与计算机进⾏沟通，下发指令的语言。

<slide class="slide-top">
:::flexblock
### 机器语言
我们知道，计算机内部是以二进制存储数据的。同理，对于指令自然也是以二进制存储的。

所以我们就可以直接用二进制代码来写程序，比如“计算8+4”就可以写为“00001000 00000100 00000100”。*但我们要知道不同CPU的指令集是不一样的*。

显然地，这玩意儿很反人类，但这是计算机可以*直接识别直接运行*的语言，故我们称之为“机器语言”。

---

### 汇编语言
由于二进制代码直接编程十分*蛋，聪明的人类就利用一些助记符，比如一些单词 “mov” 之类的来代替二进制码然后编程，这让编程轻松了很多，不过汇编程序必须经过翻译后才能运行。

然鹅由于汇编语言并没有做出本质上的改变，只是给二进制命令改了个名，我们仍将其称为低级语言。其具有编写逻辑困难并十分反智等特点，而且由于不同CPU指令集不同，所以汇编程序的可移植性也奇差。

:fa-star:**汇编程序速度并不一定是最快的。程序的运行速度只取决于最后的指令条数以及CPU执行速度。**
:::
<slide class="slide-top">
### 高级语言
***
到了高级语言，就比较像人说的语言了。但由于像人的语言，所以计算机常常是不能理解的。这时候就像汇编语言一样有一个翻译程序，但高级语言就不是简单的助记符替换了。高级编程语言一般分两种，编译型 语言和解释型语言。
:::flexblock
编译型语言：C/C++  Basic

---

解释型语言：PHP Python Swift Java Matlab
:::

这两者的运行特点就像他们的名字一样，编译型语言是编译一次就可以转成计算机可以直接运行的机器语言程序（如.exe文件）但是由于他们是直接编译的，依赖于计算机的不同，所以跨平台能力比较差，但是运行速度高。

解释性语言则是每次运行前编译，先解释再运行，导致运行效率降低，但是因为其依托于虚拟机/解释器所以跨平台性能好。

高级语言还可分为面向过程语言和面向对象语言。（区别自然是有没有对象）

<slide>
:::card{.border.blink}
### 碎片知识点：
- 于 1967 年出现的 Simula67 是历史上第一个面向对象语言
- Smalltalk 被公认为第二个面向对象的程序设计语言，和第一个IDE
- C 和 Pascal 是纯面向过程语言
- 就算没有对象也可以学面向对象的程序设计语言 C++
:::
<slide class="slide-top bg-black-blue">
## 数制转换{.text-landing.text.shadow}
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
:::{.content-left}
## 数在计算机中的表示{.text-shadow}
这是个比较难的东西……
- 整数表示
- 实数表示
<slide class="slide-top">
### 整数表示：原码，补码，反码
***
我们之前已经学会了进制转换，也知道了数据在计算机中是以二进制的形式存储的。所以对于负数，计算机中又是怎么存储的呢？

- 有原码，补码，反码三种方式

对于数 $x$ ，我们规定 $[x]$ 是 $x$ 的二进制形式字符串，$x_y$ 表示 $x$ 的原码， $x_b$ 表示补码，$x_f$ 表示反码，并规定对于任意数字 $x$。$\sim x$ 表示对于 $x$ 的二进制上每一位取反，也就是 1 变 0， 0 变 1。

 - 有如下公式：转换时仅比 $x$ 增加一位，即符号位。字符串的加号是连接符号。
:::flexblock {.blink.border}
$$ x_y = \left\{ \begin{aligned} "0"+[x] (x \geq 0)\\ "1"+[x] (x \leq 0) \end{aligned} \right. $$

---

$$ x_b = \left\{ \begin{aligned} x_y (x \geq 0)\\ \lbrack x_f+1\rbrack (x \leq 0) \end{aligned} \right. $$

---

$$ x_f = \left\{ \begin{aligned} x_y (x \geq 0)\\ "1"+[\sim x] (x \leq 0) \end{aligned} \right. $$
:::
简单的用语言来描述一下就是，原码就是本来数的二进制码的最高位上加一个符号位，正数为 0 ，负数为 1 ，而反码正数的时候与原码相同，负数情况是给原码出符号位之外每一位取反，补码则是正数与原码相同，负数是反码+1。

**::fa-star:: 注意一点，由于计算机中存储整数是定长的，也就是说二进制的位数是恒定的，所以我们上面在计算补码，反码时都要保证最后算出来的位数和原码相同，如果多了就要舍去那位数**

试一试：写出 2 ，-5 ，0 的原码，补码，反码。

::fa-star:: 注意到了吗？0 有两种原码，两种反码，但是只有一种补码！{.tobuild.fadeInUp}

::fa-star:: 其实不难发现，补码就是负数对于字长取模{.tobuild.fadeInUp}
<slide class="slide-top">
### 实数表示：定点数，浮点数
---
定点数，顾名思义，就是小数点固定的数，而浮点数，再看名字，就是小数点位置浮动的数。

- 整数就是一种十分常见的定点数，它是一种小数点固定在最后一位之后的数。
- 因为定点数表示小数的精度明显不够，浮点数应运而生。这是一种小数点位置不固定的数，它由一个定点数，乘一个基数的幂次得到，所以浮点数被分为尾数和阶码，尾数表示有效数值，而阶码表示小数点位置，定义 $E$ 为阶码，$s$ 为符号，$M$ 为尾数，得到计算公式 $V = (-1)^s * M * 2^E$ 这与人类采用的十进制科学计数法十分相似 $114514 = 1.14514 * 10^5$ 这样我们可以固定小数点的位置。

| IEEE 754 浮点数 | 位数 | E 的长度 | M 的长度 |
| --- | --- | --- | --- |
| 单精度浮点数 | 32 | 8 | 23 |
| 双精度浮点数 | 64 | 11 | 52 |

对于浮点数感兴趣的同学推荐看一下[这篇文章](陈许雯.pptx)
<slide class="bg-black-blue slide-top">
:::{.content-left}
## 计算机网络{.text-landing.text-shadow}
这一部分内容比较多，你们先看，我挑点讲。

[获取资料](NOIP初赛复习.doc){.button.ghost}
:::
:::{.content-right}
#### 定义补充：
**网络** 利用通信线路和设备，把分布在不同地理上的多台计算机连接起来，其是通信技术与计算机技术相结合的产物，网络中计算机与计算机之间的通信依靠协议进行。

**协议** 是计算机收、发数据的规则。
<slide class="slide-top">
### 分类：
:::flexblock{blink}
#### 按地域类型分：

- 局域网（LAN

- 城域网（MAN）

- 广域网（WAN）

---

#### 按拓扑结构分：

- 星形
- 总线形
- 环形
- 树形
- 网状形
:::

<slide class = "slide-top">
### OSI七层网络模型与TCP/IP五层模型
:::card{.border.blink}
**每层功能介绍：(TCP/IP)**

- 应用层：支持网络应用，应用协议仅仅是网络应用的一个组成部分，运行在不同主机上的进程则使用应用层协议进行通信。主要的协议有：http、ftp、telnet、smtp、pop3等。{.tobuild.fadeInUp}

- 传输层：负责为信源和信宿提供应用程序进程间的数据传输服务，这一层上主要定义了两个传输协议，传输控制协议即TCP和用户数据报协议UDP。{.tobuild.fadeInUp}

- 网络层：负责将数据报独立地从信源发送到信宿，主要解决路由选择、拥塞控制和网络互联等问题。{.tobuild.fadeInUp}

- 数据链路层：负责将IP数据报封装成合适在物理网络上传输的帧格式并传输，或将从物理网络接收到的帧解封，取出IP数据报交给网络层。{.tobuild.fadeInUp}

- 物理层：负责将比特流在结点间传输，即负责物理传输。该层的协议既与链路有关也与传输介质有关。{.tobuild.fadeInUp}
:::
:::card
![](./pic2.png)
---
![](./pic3.png)
:::
<slide class="slide-top">
### 网络协议简单介绍：

- HTTP：超文本传输协议，指定了客户端可能发送给服务器什么样的消息以及得到什么样的响应。是浏览器与服务器之间的信息传递规范。

- FTP：文件传输协议，观名易知。用于在网络上进行文件传输。

- SMTP：简单邮件传输协议，用来发邮件。

- POP3：邮件协议3，用来收邮件。

- IMAP：交互邮件访问协议，用来收邮件，邮件客户端实现与服务器直接同步。

- IP：互联网协议，分配给用户上网使用的网际协议的设备的数字标签，一般分 IPv4 和 IPv6 。IPv4 地址长度有32位，一搬写作 x.x.x.x 其中 0 ≤ x ≤ 255。[了解更多](https://baike.baidu.com/item/IP/224599)

- TCP：传输控制协议，TCP/IP 模型中在第4层传输层，见上页图片。

- Telnet：远程终端协议，用来远程访问服务器之类的。是Internet远程登录服务的标准协议和主要方式。

<slide class="bg-black-blue">

### 已知函数 $f(x) = (1+a)x + \frac{3}{x} + |(1-a)x + \frac{3}{x} - 4| \space (x > 0)$ 的最小值为3，则实数 $a$ 的值为____
