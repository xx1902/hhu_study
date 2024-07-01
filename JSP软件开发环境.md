## 软件开发环境概述

### **背景**

大型程序的组装、调试、修改

参与文档管理

早期的软件工具彼此独立，为使用一个工具必须从另一工具退出。事实上，软件开发过程的各阶段紧密联系。

###  **软件开发环境的概念**

> **将所有工具有机地联系起来，实现各工具有统一的接口和内部格式，前阶段工具产生的信息能被后继阶段的工具利用。**

定义 “软件开发环境是相关的一组软件工具集合，它支持一定的软件开发方法或按照一定的软件开发模型组织而成”。



**软件开发环境基本组成部分**：==工具集、交互系统、环境数据库==

**软件开发环境的分层**：宿主层，核心层，基本层，应用层



**软件开发环境的发展**

* 软件开发环境数据库：  较初级 -> 较完整 -> 智能化

**软件开发环境的分类**

* 按软件开发模型及开发方式分类：瀑布、螺旋、喷泉、原型及结构化方法、面向对象方法等

  * 原型化模型

    * 适用场景

      (1)用户需求不清，管理及业务不稳定，需求经常变化

      (2)规模小，不太复杂 

  * 结构化模型

    * 适用场景

      (1)组织相对稳定、业务处理过程规范、需求明确

      (2)在一定时期内不会发生大的变化的大型复杂系统的开发

  * 面向对象法

    * 使用场景

      ​	利用面向对象的信息建模概念，如实体、关系、属性等，同时运用封装、继承、多态等机制来构造和模拟现实系统的开发方法。

**应用范围：**通用型和专用型

**开发阶段：**前端开发、后端开发

**集成化程度：**

* 操作系统之上；
* 具有真正的数据库，而不是文件库；
* 建立在知识库系统之上，出现集成化工具集

###  **软件工具的概念**

>1.什么是软件工具？
>
>**为支持计算机软件的开发、维护、模拟、移植或管理而研制的程序系统。**
>
>2.软件工具的分类
>
>Reifer和Trattner将软件工具分为6类
>
>   **模拟工具  开发工具  测试和评估工具  运行和维护工具             性能测量工具   程序设计支持工具**

###  **计算机辅助软件工程CASE**

>计算机辅助软件工程：Computer-Aided Software Engineering，缩写为CASE。 
>
>CASE是一组工具和方法集合，可以辅助软件开发生命周期各个阶段进行软件开发。

**画图工具 Visio**

**配置管理工具 Visual Source Safe**      VSS

* Git

* Subversion  SVN

**数据库建模工具 PowerDesigner**

**UML建模工具 Rational Rose**



###  **软件开发模式**

1. **集中式计算模式**

   主机/终端 模式

   <img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240629202824583.png" alt="image-20240629202824583" style="zoom: 33%;" />

   优势：

   * 计算和数据存储能力强
   * 系统维护和管理的费用较低
   * 数据存储管理方便、安全性好

   弊端：

   * 可移植性差
   * 网络负载大
   * 资源利用率低
   * 大型机的初始投资较大

   

2. **客户/服务器（C/S）计算模式**

   前端：客户机 ->微型计算机

   后端：服务器 ->各种类型的主机

   <img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240629203107913.png" alt="image-20240629203107913" style="zoom:33%;" />

   **优势：**充分利用**两端硬件**环境优势，将任务合理分配到客户端与服务端

   ​      充分发挥客户端PC的处理能力，服务器运行数据负荷较轻

   ​      通过异种平台集成，能够协调现有的各种IT基础结构

   ​      安全、稳定、速度快，可脱机操作

   **弊端：**必须在客户端**安装大量的应用程序**（客户端软件）

   ​      客户端安装、调试、维护、升级的成本高、任务量大

   ​      **主要业务逻辑在客户端**增加安全隐患

   ​      开发成本较高，**移植困难**

3. **浏览器/服务器（B/S）计算模式**

   工作页面在浏览器实现

   极少事务逻辑在前端实现

   主要事务逻辑在服务端实现

   <img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240629203537337.png" alt="image-20240629203537337" style="zoom:33%;" />

   **优势：**单一的访问点，方便、快捷、高效；

   ​      用户可以**跨平台**以相同的浏览器界面访问系统；

   ​      **减轻了系统维护**与升级的成本和工作量；

   ​      简化了客户端电脑载荷，降低用户总体成本。

   **弊端：**无法进行脱机应用；

   ​      **受制于 HTML** ，无法使用丰富的效果展示数据；

   ​      应用服务器运行数据负荷重。

4. **胖客户端模式与瘦客户端模式**

   C/S （胖客户端 ） 传统PC ：  服务器和用户端都有数据存储

   B/S （瘦客户端 ）Thin client： 所有的数据都存储在服务器端

5. **富客户端模式**

   富客户端模式（Rich Client ），结合了胖客户端和瘦客户端的**各自优势**并克服其固有缺点。

   对应用程序提出新的要求-*富因特网应用程序*（Rich Internet Applications，RIA），利用富客户端技术RIA集成了桌面应用的**交互性**和传统Web应用的部署**灵活性**。

   富客户端提供可承载已编译客户端应用程序的运行环境，**以文件的形式用HTTP传送，**客户端应用程序使用异步C/S架构连接现有的后端应用服务器。

   

   **优点：**安全、可升级、具有良好适应性的新的面向服务模型安全、可升级、具有良好适应性的新的面向服务模型

   “ 富 ” 的含义主要包含两方面的内容：

   * 丰富的**用户界面**     将界面分解成许多既可以和用户直接交互又可以和服务器进行通信的小单元模块  （以组件为中心）

   * 丰富的**数据模型**     可接受或处理不同类型的数据，包括图像、语音、文本、视频等格式

     

   富客户端技术将**进一步扩展浏览器**功能，使之提供更加高效和友好的用户接口

   富客户端技术可以支持运动的图象、视频、音频、双向的数据通信和创建复杂的窗体，它为创建应用程序用户接口提供了一个高效而完善的开发环境。

​		







## web开发技术概述

### 计算机网络

> 用**通信线路**和**通信设备**将分在不同地点的具有独立功能的多个计算器链接起来，实现彼此之间的**数据通信**和**资源共享**的系统
>
> **简单定义：**连接两台或多台计算机进行通信的系统

**Internet主要技术**

* TCP 传输控制协议
  * 在发送和接受计算机系统之间维持链接
  * 提供无差错的通信服务
  * 将发送的数据报文还原并组装
  * 利用确认超时机制处理数据丢失问题
* IP 网际协议
  * 定义数据的标准格式
  * 分配相应的ip地址
  * 包含路由选择协议
* DNS

**Intranet**

* 定义

  * 内联网，企业网

  * 使用Internet技术和标准组建

  * 万维网WWW技术和工具，客户端使用 通用浏览器

* 技术特点

  * 容易实施  -> web服务器 和浏览器安装 配置非常方便  开发语言html容易掌握
  * 客户机/应用服务器/数据库服务器三层结构模型
  * 使用标准Internet服务
  * 采用开放标准，增加了系统的灵活性

**DNS域名解析系统**

> 在因特网上作为域名和IP地址相互映射的一个分布式数据库

* 通过主机名得到主机名对应的IP地址的过程叫做**域名解析**
* 整个DNS是由许多域所组成，每个域下又细分更多的域

**URL** 统一资源**定位符**

> 以统一方式唯一确定某个网络资源，相当于通讯地址

**格式：**

* <协议>：// <主机名><文件路径>

* (访问方法)     (资源在何处)

* 访问方法://主机地址/路径名/文件名

URL例子：

* http://www.bta.net.cn/software/home.html



### Web

万维网、Web、WWW、W3、World Wide Web，

一个由许多互相链接的超文本文档组成的系统，通过互联网访问。

<img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240629211645545.png" alt="image-20240629211645545" style="zoom: 33%;" />

**架构：**

* HTML（超文本技术）实现信息与信息的链接
* URI（统一资源**标识符**） 实现全球的精确定位
* HTTP（新的应用层协议）实现分布式的信息共享

**Web网站体系三层结构**

* 浏览器
* 应用服务器
* 数据库服务器

**优点**

1）将**应用系统**处理逻辑与**数据库**系统分开，数据库系统的更新不影响应用系统处理逻辑

2）用专门的应用服务器处理客户请求，并与数据库通信，**提高了数据库的访问效率**

3）将部分任务处理和数据操作移到后台，**简化了客户机的设计**

**页面**

* 静态页面 html     (不存在对数据库的访问)
* 动态页面 ASP PHP JSP

**Web和Internet的区别：**

* Web是在**http协议基础**之上, 利用浏览器进行访问的网站。Web Page指网站内的网页。我们常说的WWW就是这个概念下的内容。
* Internet则是一个**更大的概念**, Internet上**不只有Web**, 还有FTP、P2P、Email及App等其他多种不同的互联网应用方式。 Web只是其中最广泛的一种。
* “Web已死 Internet永生”   传统网站的重要性日益降低, 新生的互联网服务可能会取代其重要性。



### **Web数据库访问技术**

**数据库技术：**管理信息系统的核心和基础，Web技术的重要组成

**数据库：**存放数据的仓库。

**数据库管理系统：**科学地组织和存储信息，高效地获取和维护信息。

**数据库系统：**引入数据库后的计算机系统。   数据库  数据库管理系统  应用系统  数据库管理员  用户

**通过Web方式访问数据库特点：**

* 客户端统一的界面
* 跨平台运行   由于采用了**统一的标准**，用HTML标准开发的数据库应用，可以跨平台运行，减少了开发的工作量。
* 统一的开发标准  开发者需要掌握的**主要技术标准:HTML**，HTML是Web信息的组织方式

**Web数据库访问技术**

* CGI技术
* ASP技术 （动态服务器页面）
  * 是微软公司开发的代替CGI脚本程序的一种应用，ASP的网页文件的格式是 .asp，现在常用于各种动态网站中
* PHP技术 （超文本预处理器）
  * 免费，跨平台，支持ODBC数据库连接
* JSP技术  （服务器页面）
  * 根本是一个简化的Servlet设计
  * 多平台  用JSP开发的Web应用是跨平台的，既能在Linux下运行，也能在其他操作系统上运行。
  



### **Web开发技术**

* HTML技术
* DHTML技术 （动态）  是技术、标准或规范的一种集成： 
* Java Applet技术
  * 小应用程序     可执行代码为class文件
  * Java Applet可提供动画、音频和音乐等多媒体服务
  * 主要应用于各种网页文件中-->增强网页的人机交互
* JavaScript与VBScript
  * JavaScript 最广泛的脚本语言
  * 介于Java与HTML之间、**基于对象**的事件驱动的编程语言
  * **不需要jaava解释器**，直接在Web浏览器中解释执行
  * **VBScript **  VBS和Javascript一样都用于创建客户方的脚本程序，并处理页面上的事件及生成动态内容
* ActiveX控件
  * 可用于拓展Web页面的功能，创建丰富的Internet应用程序
  * 不需要自己编程，就可完成使用ActiveX控件的网页设计

* ASP.NET
  * 完全基于模块和组件，有更好的可扩展性和可定制性
* AJAX
  * **不刷新整个页面**，在页面内与服务器通信
  * **异步通讯**，不需要打断用户操作



**web开发平台**

* .NET开发平台
  * 独立于任何特定的语言或平台

* Java EE开发平台  

  * 纯粹基于**Java**的解决方案
  * J2EE平台的**三大核心技术**SERVLET、JSP和EJB都已先后问世

  

**Web技术发展史**：静态技术->动态技术->Web2.0

web1.0:体现一种被动接受
web2.0:体现一种主动表达
web3.0:体现个性化推荐



### HTML

> HTML语言是**Web客户端**信息展现的**最有效载体**之一，是用于描述网页文档的标记语言。

**标记语言特征**

* 格式化的标记语言

* 文档 = 控制标记 + 显示内容

* 简易性

* 可拓展性

* 与平台无关   

<img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240629225212194.png" alt="image-20240629225212194" style="zoom: 50%;" />

[HTML 教程 (w3school.com.cn)](https://www.w3school.com.cn/html/index.asp)

超文本标记语言，由各种标记符组成

* 标记与大小写无关

* 标记可以联合使用，也可以嵌套使用

* 标记可以带有一个或多个属性参数，格式为：

*  <标记 属性1=“属性值1” 属性2=“属性值2” …>

* 注释标记<!--注释内容-->不在浏览器中显示，只供阅读页面代码帮助理解使用。

特点：

* 被WEB浏览器解释并执行（不需要编译）
* 本质上是一维的

```html
<html>
    <head>
        <title>学校</title>
    </head>
    <body>
        <h1>
            河海大学
        </h1>
    </body>
</html>
```

**网页多媒体技术**

* 图像标记 img

* 背景音乐标记 bgsound

* 表格标记 table

* 列表标记 ul ol dl

* 超链接标记 href

  * **屏幕滚动功能**      `<a href="#锚名">链接文本</a> ` `<a name="锚名">“锚”文本</a>`

* 表单标记 form

* 列表框 select

* 窗口框架标记 framset

  * 用来定义主文档中有几个帧并且各个帧是如何排列的；

  * 具有**rows和cols属性**，使用<frameset>标记时这两个属性至少必须选择一个，否则浏览器只显示第一个定义的帧；

  * 放在帧的主文档的<body></body>标记对的**外边**；

  * 可以嵌在其它帧文档中，并可嵌套使用；

  * rows用来规定主文档中各个帧的行定位；

  * 这两个属性的取值可以是百分数、绝对像素值或星号(“\*”)，其中星号代表那些未被说明的空间；

    如果同一个属性中出现多个星号则将剩下的未被说明的空间**平均分配**；

    所有的帧按照rows和cols的值从左到右，从上到下排列。 

  * 放在<frameset>…</frameset>之间，定义具体的帧；

    具有src和name属性，这两个属性都是必须赋值的；

    <img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240629232142676.png" alt="image-20240629232142676" style="zoom:33%;" />

* 定义特定显示区  div

<img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240629233031100.png" alt="image-20240629233031100" style="zoom:33%;" />

### CSS

**背景：**HTML显示特性通过标记属性设置，一旦设置不能随意改变版面和编排文字，也不能由程序控制。

**CSS：**扩展了HTML在排版和文字式样上的功能,可以通过脚本程序控制，使页面表现方式更加灵活，具有动态特性。

美化页面

**样式表**

> 页面样式设定与页面内容分离,把CSS样式信息存成**独立文件**，使多个网页文件共享样式文件。

* 内联式
  * 把css代码直接写在现有的HTML标记中

* 嵌入式
  * 把样式定义放在文档头部，<style></style>标记之间定义，整个页面都以该样式显示

* 外部链接式
  * 多个网页具有相同样式时，可以使用样式文件（后缀是.css）把设定的样式集中起来，使多个网页共享该样式文件


**定义样式格式**

* 选择器 { 规则 }

* 如： h1{ color:blue;}  

### DHTML

>是技术，标准和规范的一种集成
>
>CSS （Cascading Style Sheets，层叠样式单）
>
>CSSL（Client-Side Scripting Language，客户端脚本语言）
>
>HTML DOM（Document Object Model，HTML文档对象模型）
>
>**DHTML**基于HTML，通过CSS技术扩展HTML在样式编排上的不足，使用脚本程序调用或控制浏览器对象和网页对象，使页面具有动态效果和交互功能。

客户端  -> 在本地执行

* 将页面内容对象化
* 通常使用VBScript或JavaScript脚本程序把这些对象组装到一起，实现其动态和交互性；
* 网页无需重新下载
* 所有的功能都是在用户的计算机上实现并完成的，因此提高了响应速度；
* 突破了传统的静态Web页面的局限。



### XML

> **可扩展的标记语言，可以定义其他语言的语言。**
>
> 包括一组相关技术：XSL(可扩展样式语言)、XML链接语言、XML名称空间、XML模式(Schema)
>
> │标准通用标记语言的一个简化子集，专为Web环境而设计的﹔
>
> │面向数据处理的，主要处理动态产生的信息。

特点

* 把**内容和显示格式**分开 -> 使XML文件制作者集中于数据本身 
  * 显示内容在XML文件中，显示方式在样式文件CSS或XSL中

* 不同的样式文件，使相同的数据以不同的方式显示，以利于数据的**重用**

* 减少数据的传送量。



**结构**

* Ⅰ 文件头

  ​	文件头是XML说明部分，它描述了XML文档、版本号、编码信息和其他一些信息。

     `<?xml version="1.0" encoding="GB2312"?>`

  ​	<?……?>：处理指令，以“<?”开始，“?>”结束 

  ​	xml：在“<?”后面的xml说明该文件是XML文件

  ​	version=“1.0”：遵循XML1.0规范

  ​	encoding=“GB2312”：应用中文GB2312字符编码

* Ⅱ 文件体

     文件体用来存放XML文件中被应用程序使用的信息

* Ⅲ 注释

    XML中注释在`<!……>`之间 

**书写规则**

* 区分大小写     <?xml ......>
* 文件的第一行必须是xml文件声明

**功能**

* 异种数据的交互 （不同的数据库）
* 数据的多样化显示
* 分布式计算
* 将数据内容与内容的表现方式分割



### J2EE

> * 适用于小型设备和智能卡的J2ME
> * 适用于桌面系统的J2SE
> * 适用于创建服务器应用程序和服务的**J2EE**

<img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240630083127507.png" alt="image-20240630083127507" style="zoom: 50%;" />

**J2EE组件：**

* J2EE组件是一个**由Java语言编写、封装了功能的软件单元**，能够与相关的一些类和文件一起组成J2EE应用程序，可简化且规范应用系统的开发与部署，进而提高可移植性、安全与再用价值。
* 和“标准的”Java类的不同点在于：它被**装配**在一个J2EE应用程序中，具有固定的格式并遵守J2EE规范，由J2EE服务器对其进行管理。
  * 客户端应用程序和applet是运行在**客户端的组件**。 
  * Java Servlet和Java Server Pages (JSP)是运行在服务器端的**Web组件**。
  * Enterprise JavaBean(EJB)组件是运行在服务器端的**业务组件**。 



**客户端组件**

* Applets(客户端小应用程序)：从Web层接收的一个Web页面可以包含内嵌的applet，需要运行在客户端**安装了Java虚拟机**的Web浏览器上；

* 客户端应用程序：运行在客户机上，能提供强大而灵活易用的用户界面。

**Web组件**

* 既可以是servlet也可以是JSP页面；

  * Servlet是一个Java类，它可以动态地处理请求并作出响应；

  * JSP页面是一个基于文本的文档，它以servlet的方式执行，但是它可以更方便建立动态内容

**业务组件**

* J2EE 将**业务逻辑**从客户端软件中抽取出来，封装在EJB（Enterprise JavaBean）组件中。
* 客户端软件通过网络调用组件提供的服务以实现业务逻辑，而客户端软件的功能单纯到**只负责发送**调用请求和显示处理结果。

* 有三种类型的Enterprise JavaBeans(EJB): 会话EJB, 实体EJB,消息驱动EJB。



**J2EE容器**

J2EE服务器以容器的形式为每一个组件类型提供底层服务（如事务处理、状态管理、多线程、资源池等）

* EJB容器

* Web容器

* 客户端应用程序容器

* Applet容器

**Java Servlet**

> Servlet是用Java编写的Server端程序，与协议和平台无关,采用请求－响应模式提供Web服务,可完成以下任务:

**技术**

* **获取**客户端浏览器通过HTML表单提交的数据及相关信息

* **创建**并返回对客户端的动态响应页面

* **访问**服务器端资源，如文件、数据库

* 为JSP页面**准备**动态数据，与JSP一起协作创建响应的页面

**特点**

* Web浏览器并**不直接和servlet通信**，servlet是由Web服务器加载和执行的；

* servlet是用Java编写的，所以一开始就是**平台无关**的，编写一次就可以在任何平台运行；

* servlet**是持久的**，只需Web服务器加载一次，而且可以在不同请求之间保持服务(例如一次数据库连接)；

* 为JSP页面**准备**动态数据，与JSP一起协作创建响应的页面



**Java Servlet Pages（JSP）技术**

> JSP技术在传统的网页HTML文件中插入**Java程序段**和**JSP标记**，从而形成JSP文件，进而生成页面上的动态内容。
>
> **简化**了Java和Servlet的使用难度，同时通过扩展JSP标记(TAG)提供了网页动态执行的能力。
>
> 仍未超出Java和Servlet的范围，不仅JSP页面上可直接写Java代码，而且**JSP是先被译成Servlet之后**才实际运行的。

**Servlet和JSP关系**

* JSP修改后可以立即看到结果，不需要手工编译，JSP引擎会来做这些工作；
* 而Servlet需要编译，重新启动Servlet引擎等一系列动作。

* JSP提供了一套简单的标签，和HTML融合的比较好，可以使不了解Servlet的人可以做出动态网页来。对于Java语言不熟悉的，会觉得JSP开发比较方便。

<img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240630093151654.png" alt="image-20240630093151654" style="zoom:33%;" />

* JSP先是转义成Servlet之后再运行，第一次JSP更慢
* JSP 是HTML嵌套Java，   JSP会
* Servlet是Java嵌套HTML -> 要发送到浏览器所以嵌套html







## JSP

> 由Sun公司倡导、许多公司参与一起建立的一种动态网页技术标准。
>
> JSP开发的Web应用是跨平台的，既能在Linux下运行，也能在其他操作系统上运行。

* 一个服务器上可以有很多基于JSP的Web应用程序，以满足各种用户的需求。
* 这些Web应用程序必须有一个软件来统一管理和运行，这样的软件被称作**JSP引擎或JSP容器**，而安装JSP引擎的**计算机**被称作一个**支持JSP的Web服务器**。

* Tomcat是一个免费的开源**JSP引擎**，将安装了Tomcat的计算机称作一个**Tomcat服务器**。

### 配置JSP环境

* 安装和配置JDK
* 安装和启动Tomcat服务器 （安装板和解压版）
  * 安装版与解压版Tomcat服务器的区别在于启动方式的不同
    * 安装版的tomcat文件双击后选择路径和jdk配合安装，启动的时候在services.msc服务中启动；
    * 解压版的tomcat文件直接解压后在bin目录中有startup.bat和startup.sh启动（windows下用startup.bat，linux下运行startup.sh）。

  * 在程序运行过程中它们分别运行获取的路径是有差别的。这也是导致许多项目在本地可以运行，但部署到其它计算机上时会报错的原因之一。
    * 在bin目录下启动起来，如果关闭运行窗口的话，tomcat会自动停止运行，而在服务中不会。
    * 一般服务器上都是以服务的方式运行tomcat，所以在读取项目外的配置文件的时候一定要注意路径的问题。

* 测试Tomcat服务器 localhost:8080
* 配置端口 conf -> sever.xml
* 设置Tomcat的环境变量

**JSP页面简介**

* 一个JSP页面中可以有**普通的HTML标记**、JSP规定的JSP标记以及通过标记符号“`<%”，“%>`”加入的Java程序片。

* 一个JSP页面按文本文件保存，**扩展名是.jsp**

  * 文件名必须符合标识符规定；

  * 文件名区分大小写；

```jsp
<!--JSP标记-->
<%@ page contentType=”text/html;charset=gb2312”%>
<!--HTML标记-->
<html>
    <head><title>第一个JSP程序</title></head>
    <body>
<!--Java程序片-->
    <%
          out.println(“Hello World!”);
    %>
<!--HTML标记-->
    </body>
</html>
```

### **设置Web服务目录**

> 只有将编写好的JSP页面文件保存到Tomcat服务器的某个**Web服务目录**中，远程用户才能通过浏览器访问该Tomcat服务器上的JSP页面。
>
> 人们常说的一个网站，实际上就是一个Web服务目录。

* 根目录  \webapps\Root下的文件
* Webapps下的Web服务目录

  * Tomcat服务器安装目录webapps下的任何一个子目录都可以作为一个Web服务目录。如在webapps下新建子目录ch1，那么ch1就成为一个Web服务目录

* 虚拟目录 conf -> server.xml

  * 用记事本打开conf文件夹中的主配置文件server.xml，

    在 </Host>的前面加入

    ​       <Context path="/apple" docBase="D:\MyBook\zhang" debug="0" 

    ​        reloadable="true" />

    保存并重新启动 tomcat服务器!

      http://127.0.0.1:8080/apple/example1_1.jsp

* 相对目录



<img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240630133516423.png" alt="image-20240630133516423" style="zoom: 67%;" />



### jsp运行原理

* 当服务器上的一个JSP页面被第一次请求执行时，服务器上的JSP引擎首先将JSP页面文件转译成一个java文件，并编译这个java文件生成字节码文件，然后执行字节码文件响应客户的请求
* 当**多个客户**请求一个JSP页面时，Tomcat服务器为每个客户启动一个**线程**，该线程负责执行常驻内存的字节码文件来响应相应客户的请求。这些线程由Tomcat服务器来管理，将CPU的使用权在各个线程之间快速切换，以保证每个线程都有机会执行字节码文件。

**字节码文件的主要工作：**

* 把JSP页面中的HTML标记符号（页面的静态部分）交给客户的浏览器负责显示。

* 负责**处理JSP标记**，并将有关的处理结果发送到客户的浏览器。

* **执行**“<%”和“%>”之间的**Java程序片**（JSP页面中的动态部分），并把执行结果交给客户的浏览器显示。

**JSP与Servlet的关系**

* Java Servlet就是编写在服务器端**创建对象的Java类**，习惯上称之为Servlet类，Servlet类的对象习惯上称之为一个Servlet。

* JSP技术就是**以Java Servlet为基础**，提供了Java Servlet的几乎所有好处。但是JSP技术不是Java Servlet技术的全部，它只是Java Servlet技术的一个**成功应用**。

* 对于某些Web应用，就可能需要JSP+Javabean+Servlet来完成，即需要服务器再创建一些Servlet对象，**配合JSP页面**来完成整个Web应用程序的工作。

## JSP基础语法

### 五种元素

==5中元素==

* 普通的**HTML标记符**   ->    客户端
* JSP标记  如**指令标识**，**动作标识**
* **变量和方法的声明**                                                                                                            
* **java程序片段**
* **java表达式**



**声明变量**

* 局部变量  -> 每次刷新页面，局部都会初始化

  ```jsp
  < % int i = 0; % >
  ```

  

* 在`“<%!”和“%>”`标记符之间声明变量，变量的类型可以是Java语言允许的**任何数据类型**，将这些变量称为JSP页面的成员变量。

  * 成员变量  -> 各个用户共享
  
  ```jsp
  <%! int i = 0; %>
      
  <%!  int  a, b=10 , c;
           String tom=null,jerry="love JSP";
           Date date; 
   %>
  
  ```
  
  
  

**声明方法**

> 在“<%!”和“%>”标记符号之间定义方法，所定义的方法在整个JSP页面有效，可以在**Java程序片**中被调用。
>
> **方法内声明的变量**只在该方法内有效，当方法被调用时，方法内声明的变量被分配内存，方法被**调用完毕**即可释放这些变量所占的内存。

* <%!   %>

* 在整个JSP页面中有效
* 方法内定义的变量**只在方法内有效**



### **java程序片段**

> 一个JSP页面中的Java程序片会按其在页面中的**顺序被执行**,而且某个Java程序片中声明的**局部变量在其后继的所有Java程序**片以及表达式内==都有效==。
>
> 可将一个Java程序片分割成**几个Java程序片**,然后在这些Java程序片之间再插入其他标记元素。

* 按顺序执行

* 多个客户同时访问，程序片段将被执行多次，在不同的线程中互不影响

* 程序片的变量是==局部变量==

* 设置共享成员变量，要注意同步 

  <img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240630150342187.png" alt="image-20240630150342187" style="zoom: 67%;" />

  ```jsp
  <%!
    int i_shareMember = 0;
    synchronized void add() { i_shareMember++; }
  %>
  <%
    Date date = new Date();
    add();
    out.print(date + "当前时间段用户访问<br>");
    out.print("刷新之后，共享变量的值为" + this.i_shareMember + ".多个用户访问时其结果不同<br>");
  %>
  ```

* 可以将一个java程序片段分割成几个java程序片段   -> 不同的样式



### **Java表达式**

> 可以在“<%=”和“%>”之间插入一个表达式，这个表达式**必须能求值**。表达式的值由服务器负责计算，并将计算结果用字符串形式发送到用户端显示。
>
> 如：`<%=getDate()%>`
>
> 注意：不可插入语句，`“<%=”`是一个完整的符号，之间不能有空格

* 表达式必须能求值

* <% 和 =不能有空格

  ```jsp
  <%= getDate() % >
   
  现在是<%= calendar.get(Calendar.YEAR) %>年
  ```

### **JSP注释**

**HTML注释**

*  <!-- 注释-->  ==显式==

**JSP注释**

*  <%-- 注释 --%>  ==隐式==

*   JSP注释写在JSP程序中，但不发送给客户。

**Scriptlets注释**

* 包含的是java代码，所以java中的注释规则在Scriptlets中也适用，
* 常用的java注释使用//表示单行注释，使用/* */表示多行注释.   ==隐式==



### **JSP标识**

#### **JSP指令标识**

**page标识**

> page 指令用来定义整个JSP页面的一些属性和这些属性的值，属性值用单引号或双引号括起来。
>
> page 指令与其书写位置无关，习惯把page指令写在JSP页面的最前面。

可以用一个page指定多个属性的值，也可以使用多个page指令分别为每个属性指定值

```jsp
<%@ page import="java.util.Calendar" %>
<%@ page language="java" contentType="text/html; charset=UTF-8"
         pageEncoding="UTF-8" %>
```

* contentType属性

  * `<%@ page contentType="text/html; charset=UTF-8" %>`
  * ==不允许==两次使用page给contentType属性指定不同的属性值
  * 确定 MIME类型 和JSP字符编码

* language属性

  * `<%@ page language="java" %>`
  * 定义脚本语言 'java'

* import属性

  * `<%@ page import="java.util.Calendar" %>`
  * 引入运行环境的包中的类 
  * 默认的import属性值已有" java.lang.\*"、"javax.servlet.\*"、"javax.servlet.jsp.\*"、"javax.servlet.http.\*"等。

* session属性
  * 是否需要使用**内置的**session对象
  * **默认属性**为true

* buffer属性

  * 内置输出流对象out负责将服务器的某些信息或运行结果发送到用户端显示。

  * buffer属性用来指定out设置的缓冲区的大小或不使用缓冲区。例如：

      `  <%@ page buffer= "24kb" %>`

  * 缓冲区的大小 默认为8kb

* autoFlush属性
  * 缓冲区**是否自动刷新**
  * 当autoFlush属性取值false时，如果out的缓冲区填满，就会出现缓存溢出异常。
  * 当buffer的值是“none”时，autoFlush的值就不能设置成false。

* isTreadSafe属性
  * 是否支持多线程

* info属性

  * info属性的属性值是一个字符串，其目的是为JSP页面准备一个**常用且可能要经常修改的字符串**。
    * 例如：`<%@ page info= "we are students" %>`
  * 用`getServletInfo()`获取info属性的属性值



**include指令标记**

include指令标记的作用是在JSP页面出现该指令的位置处，静态插入一个文件，实现代码的复用。

`<%@ include file= "文件的URL" %> `

一个 JSP 页面中的 include 指令的数量不受限制。

静态插入，就是当前JSP页面和插入的文件合并成一个新的JSP页面，然后JSP引擎再将这个新的JSP页面转译成Java文件。

* 静态插入一个文件，实现代码的**复用**
* 把一个复杂的JSP页面分解成**若干个简单的部分**

<img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240630155954682.png" alt="image-20240630155954682" style="zoom:33%;" />

![image-20240630190115352](C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240630190115352.png)



#### **JSP动作标记**

* include动作标记
  
  > include动作标记告诉JSP页面动态包含一个文件，即JSP页面运行时才将文件加入。
  >
  > **<**jsp:include page= "文件的URL"/>
  
  * jsp页面运行时才将文件加入
    * 如果是普通的文本文件，就将文件的内容发送到用户端，由浏览器负责显示；
    * 如果是JSP文件，JSP引擎就执行这个文件，然后将执行的结果发送到用户端浏览器显示。
  
* param动作标记
  * 以  名字-值  对的形式为其他标记提供信息
  * `<jsp:param name= "名字" value= "指定给param的值">`
  * `    String 指定给param的值= request.getParameter("名字");` 获取指定值
  * param标记不能独立使用，需作为jsp:include、jsp:forward、jsp:plugin标记的子标记来使用
  
    > 当该标记与jsp:include动作标记一起使用时，可以将param标记中的值传递到include动作标记要加载的文件中去，被加载的JSP文件可以使用Tomcat服务器提供的request内置对象获取include动作标记的param子标记中name属性所提供的值。
  
    <img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240630171455833.png" alt="image-20240630171455833" style="zoom: 50%;" />
  
    ```jsp
    <jsp:include page="Example3_7_b_param_pythagorean.jsp">
    <jsp:param name="sideA" value="<%= a %>"/>
    <jsp:param name="sideB" value="<%= b %>"/>
    <jsp:param name="sideC" value="<%= c %>"/>
    </jsp:include>
    --------------------
    <%
        String sideA = request.getParameter("sideA");
        String sideB = request.getParameter("sideB");
        String sideC = request.getParameter("sideC");
    %>
    ```
  
    
  
* forward动作标识
  
  * ```jsp
    <jsp:forward page="要转向的页面" />
    <%-- 或者 --%>
    <jsp:forward page="要转向的页面" >
    param子标记
    </jsp:forward>
    ---------------------
    <jsp:forward page="Example3_8_b_forward_excellent.jsp">
    <jsp:param name="number" value="<%=grade%>"/>
    </jsp:forward>
    ---------------------
    <%
        String appraise = request.getParameter("number");
    %>
    <h4>你的成绩为：<%=appraise%></h4>
    ```
  
    
  
  * 从该指令处停止当前页面的执行，转向执行page属性指定的JSP页面
  
  * 可以使用param动作标记**作为子标记传送信息**，要转向的JSP页面用r==equest内置对象==获取param子标记中name属性所提供的值。
  
  * 当forward动作标记不需要param子标记时，==必须==使用第一种形式。
  
  * 当前页面使用forward动作标记转向后，尽管用户看到了转向后的页面的效果，但浏览器地址栏中显示的仍然是==转向前的JSP页面的URL地址==，因此，如果**刷新浏览器的显示**，将再次执行当前浏览器地址栏中显示的JSP页面。
  
* useBean动作标记

  * 第六章详讲
  * 设置Bean的简单属性和索引属性
  * `<jsp:useBean id=“id” scope=“page/request/session/application” typeSpec/>`
  * 其中id表示实例；scope表示此对象可以使用的范围

* setProperty动作标记
  * 此操作与useBean协作，用来设置Bean的简单属性和索引属性。

  * <jsp:setProperty >标签使用Bean给定的setXxx()方法，在Bean中设置一个或多个属性值。利用<jsp:setProperty >设置属性值有多种方法。

    `<jsp:setProperty name=“beanName” propertyDetails/>`

* getProperty动作标识
  * 访问一个Bean属性

  * jsp:getProperty操作是对jsp:setProperty操作的补充，它用来访问一个Bean的属性。

    `<jsp:getProperty name=“userSession” property=“name”/>`





## JSP内置对象

> JSP为简化页面的开发提供了一些内部对象。
>
> JSP的编写者可以直接引用这些内置对象，不需要由JSP的编写者显式声明，也不需要实例化。它们由JSP容器实现和管理，在所有JSP页面中都能使用内部对象。
>
> 内部对象只对Java程序片和Java表达式有用，在声明中不能使用。

### request对象

> **HTTP通信协议**是用户与服务器之间一种提交(请求)信息与响应信息(request/response)的通信协议。
>
> 在JSP中，内置对象**request封装了用户提交的信息**，那么该对象调用相应的方法可以**获取封装的信息**。
>
> 可类比为酒店中住户请求服务时填写的服务单

* **封装**了用户提交的信息

* HTTP请求报文
  * **请求行**：规定了请求的**方式**  （方法 资源  版本号）
  
    Eg:住户通过酒店官网预约或者打电话申请服务
  * **请求头**：说明请求的**服务类型**
  
    Eg:住户申请的具体服务
  * **信息体**：指请求的**正文**
  
    Eg:服务内容
  
* **处理问题**
  
  * **获取用户提交的信息**
  
    >用户通常使用HTML表单向服务器的某个JSP页面提交信息，表单的一般格式是：
    >
    >`<form action= “JSP页面” method= "get | post" >` 
    >
    >​    提交手段
    >
    >`</form>`
    >
    >JSP页面可以让**request对象**用`getParameter(String s)`方法获取表单提交的信息。
  
    * getParameter()
    * 和post提交的最大区别
      * 可以在链接（最上面）中看到
      * post看不到，post遇到中中文可能会乱码  8859-1
  
  * **处理中文信息**
    
    * 重新编码  请求是iso-8859-1  ` byte b[]=str.getBytes("ISO-8859-1");`
    
      > request将获取的信息重新编码，即用ISO-8859-1进行编码，并将编码存放到一个字节数组中，然后再将这个数组转化为字符串。如下所示：
      >
      > 
    
      ```jsp
      <%
      	String str=request.getParameter("message");
      	byte b[]=str.getBytes("ISO-8859-1");
      	str=new String(b);
      %>
      -----
      <%
        byte bytes_name[] = request.getParameter(“names”).getBytes(“iso-8859-1”);
        String str_name = new String(bytes_name);
        out.print(str_name);
      %>
      
      ```
    
      
    
    * 设置编码格式 setCharacterEncoding()
    
      > request在获取信息之前使用**setCharacterEncoding方法**设置自己的编码为gb2312：
      >
      > ​	request.setCharacterEncoding("gb2312");
    
    * **乱码问题：**表单乱码、页面乱码、参数乱码、源文件乱码
    
      **页面乱码：**在JSP页面中，中文显示乱码有两种情况：一种是HTML中的中文乱码，另一种是在JSP中动态输出的中文乱码。
    
      **解决：**页面中使用page指令指定编码必须支持中文编码.
    
      **注意：**`charset`的首字母小写 page 里面的
    
    * 使用==get方法==提交表单的时候正常接收即可，**不需要**转成iso-8859-1格式
    
    * 使用==post方法==提交表单的时候传递的参数如果是中文的话很可能会出现乱码   **通常情况下是使用 ISO-8859-1 字符集进行编码**
    
  * **获取其他信息**
  
    * **getProtocol()：**获得客户向服务器传送数据所使用的通信协议和它版本号，例如：HTTP/1.1。
  
      **getServerName()：**获得接受请求的服务器主机名
  
      **getServerPort ()：**获得服务器主机的端口号
  
      **getRemoteHost()：**获得客户机的全名，如果名字获取不得，则获得客户机的IP地址。
  
      **getRemoteAddr()：**获得发送请求的客户机的IP地址。
  
      **getMethod()：**获得客户提交信息方式，如get、post或put等
  
      **getServletPath()：**获得客户请求的JSP页面的文件目录。
  
      **getContentLength()：**获得客户提交信息长度，以字节为单位。
  
      **getHeader(String name)：**获得HTTP头文件中由参数name指定的头名字的值。
  
      **getHeaderNames()：**获得客户请求中所有头部域的名字。
  
      **getPathInfo()：**获得客户请求时关联到URL的附加路径信息，没有此信息则返回空值。
  
      **getCookies()：**返回客户端的Cookies对象，结果是一个Cookies数组。如果浏览器没有发送Cookies，则返回空值。
  
      **getRequestURL()：**获得发出请求字符串的客户端地址。
  
      **getParameter(String name)：**获得客户提交给服务器的name参数值。
  
      **getParameterNames()：**获得客户提交给服务器的所有参数名。
  
      **getParameterValues(String name)：**获得指定参数所有值。

### respose对象

> 与request对象相对应的对象是response对象，response对象**对客户的请求做出响应**，向客户端发送数据。

Response方法可**分为三类**：

* 设定响应状态码的方法
* 设定表头的方法
* 使用response的sendRedirect(URL url)方法实现用户的重定向

**动态设置MIME（响应）类型**

<img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240630201203575.png" alt="image-20240630201203575" style="zoom: 67%;" />

* 用户可以使用response对象的`setContentType(String s)方法`来改变contentType的属性值

**response的HTTP头**

* addHeader(String head, String value);
* setHeader(String head, String value)；
* 动态添加新的响应头和头的值，将这些头发送给用户的浏览器。**如果添加的头已经存在，则先前的头被覆盖。**
* response.setHeader("Refresh",“5");  -> 每隔5s刷新一次

**response的重定向**

* 可以使用response的`sendRedirect(URL url)方法`实现用户的重定向。

* ```jsp
  <%
    if (!username.equals("root") || !password.equals("123456")) {
      response.sendRedirect("Example4_6_a_response_redirect.jsp");   // 重定向
    }
  %>
  ```

  

**respose的状态行**

* 当**服务器对用户请求进行响应**时，发送的首行称为**状态行**。

* 3位数字的状态码：

  1yy，表示实验性质；

  2yy，表示请求成功；

  3yy，表示请求满足前应采取进一步行动；

  4yy，表示无法满足请求，如404（请求页面不存在）；

  5yy，表示表服务器出现问题，如505

<img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240630204145915.png" alt="image-20240630204145915" style="zoom: 67%;" />

### session对象

<img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240630204545045.png" alt="image-20240630204545045" style="zoom: 33%;" />

> 需要服务器在用户访问的一个会话期中记住客户，为客户提供个性化服务。
>
> Tomcat服务器可以使用**内置session对象**（会话）记录有关连接的信息。
>
> 
>
> 记录有关链接的信息 -> 区分不同用户
>
> 由服务器创建
>
> 放在客户的cookie中
>
> 同一用户的的Id是相同的

**session对象的ID**

* 用户在访问一个Web服务目录期间，**服务器为该用户分配一个session对象**（称作用户的会话），服务器可以在各个页面使用这个session记录当前用户的有关信息。

* 该对象对应一个String类型的ID号，服务器在响应客户请求的同时，把ID号发到客户端，并**写入客户端的cookie**中。

* 当客户**关闭**浏览器后，一个会话结束，服务器端该客户的**session对象被取消**。当客户重新打开浏览器建立新连接时，JSP引擎为该客户再创建一个新的session对象。

  ```jsp
  <%
    String id_a = session.getId();
    out.print("<p>当前session对象的ID号为：</p>" + id_a);
  %>
  ```

**重写URL实现session对象**

> 如果用户不支持Cookie，JSP页面可以通过URL重写来实现session对象的**唯一性。**
>
> 所谓**URL重写**，就是当用户从一个页面重新连接到一个页面时，通过向这个新的URL**添加参数**，把session对象的id传带过去，这样就可以保障用户在该网站各个页面中的session对象是完全相同的。
>
> String str=response.encodeRedirectURL(“second.jsp”);
>
> String str=response.encodeURL(“second.jsp”);
>
> 然后将连接目标写成<%= str %> 即可。

**session对象存储数据**

`session.setAttribute("username", username);`

酒店可以存放行李，session对象同样可以存储数据

* public void setAttribute(String key, Object obj)   存数据

  <img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240630210830810.png" alt="image-20240630210830810" style="zoom:50%;" />

* public Object getAttribute(String key)   取数据

* public Enumeration getAttributeNames()

  <img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240630210955100.png" alt="image-20240630210955100" style="zoom:50%;" />

* public void removeAttribute(String name)   

  <img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240630211028779.png" alt="image-20240630211028779" style="zoom:50%;" />

**session对象生命周期**

> session对象的生存期限依赖于session对象是否**调用invalidate()方法**使得session无效或session对象达到了设置的**最长的“发呆”状态时间**以及是否**关闭服务器**。
>
> 如果关闭服务器，那么用户的session消失，所谓“发呆”状态时间是指用户对某个Web服务目录**发出的两次请求之间的间隔时间**（默认的发呆时间是30分钟）。

* 调用invalidate()方法或者关闭浏览器
* Session达到了最长发呆时间
* 服务器关闭

> 可以通过Tomcat目录conf文件下的配置文件`web.xml`修改默认发呆时间：
>
>   <session-config>
>
> ​       <session-timeout>30</session-timeout>
>
>   </session-config>
>
> session对象也可以**使用相应的函数**获取或设置与生存时间有关的信息：setMaxInactiveInterval(int interval)设置最长发呆时间（单位秒），getMaxInactiveInterval()获取最长发呆时间。

<img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240630212607449.png" alt="image-20240630212607449" style="zoom: 33%;" />

### application对象

<img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240630213020188.png" alt="image-20240630213020188" style="zoom: 25%;" />

**由多个客户端用户共享**，不同web服务目录下的application各不相同

**application**对象一直保持至服务器关闭

**特点**

* 用户存储的数据可以和其他用户共享
* **存储在application对象中的属性可以被该Web应用程序中的所有Servlet程序访问,而不管访问来自哪个客户端**

**Application数据存储**

`  application.setAttribute("allNotices", vector);`

* public void setAttribute(String key, Object obj)

* public Object getAttibue(String key)

* public Enumeration getAttributeNames()

* public void removeAttribue(String key)

### out对象

> out对象可以看作为酒店的**叫醒服务**，即酒店**主动向用户提供服务**
>
> out对象是一个输出流，用来向用户端输出数据。通过out对象直接向用户端写一个由程序动态生成的HTML文件

<img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240630215217199.png" alt="image-20240630215217199" style="zoom:33%;" />

输出信息

* out.print()方法
* out.println()方法

管理缓冲区





## JSP与JavaBean

> JavaBean是一款可重复使用的软件组件，是一个特殊的java类
>
> jsp 显示
>
> javaBean 处理（servlet） 保存数据
>
> MVC开发

* JavaBean是一个**可重复**使用的**软件组件**
* 是遵循一定标准、用**Java**语言编写的一个**类**
* 一般**实现**网页中的**业务逻辑或数据库操作**

**特点**

* 可以实现代码的**重复运用**
* 易编写，易维护，易使用
* 可跨平台

### 编写和使用JavaBean

<img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240630222625296.png" alt="image-20240630222625296" style="zoom: 25%;" />

<img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240630222634932.png" alt="image-20240630222634932" style="zoom:25%;" />

JSP页面加载一个Bean  实例化一个Bean

* JSP调用Bean处理 完成数据的处理
* 并将有关数据的结果存放在bean中

**编写Bean**

==类似于java类==

* 如果类的成员变量的名字是xxx，类中提供两个方法：

  *  getXxx()  用来获取属性xxx

  *  setXxx()  用来修改属性xxx

* 对于boolean类型的成员变量，允许使用“isXxx”  代替set 和 get

* 类中声明的方法的**访问属性**都必须是**public**的。

* 类中声明的**构造方法**必须是**public、无参数**的。 

  <img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240630223020244.png" alt="image-20240630223020244" style="zoom: 67%;" />

**Bean的保存**

<img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240701084849134.png" alt="image-20240701084849134" style="zoom: 33%;" />

使用相应的字节码创建一个Bean

* 建立目录
* 根据包名建立子目录
* 将Bean字节码保存在响应的子目录

<img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240701090229919.png" alt="image-20240701090229919" style="zoom:33%;" />

**使用Bean**

* useBean加载使用

**Bean的生命周期**

* page

  <img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240701090950485.png" alt="image-20240701090950485" style="zoom:33%;" />

* request

  <img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240701091041051.png" alt="image-20240701091041051" style="zoom:33%;" />

* session

  <img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240701091113993.png" alt="image-20240701091113993" style="zoom:33%;" />

* application

  <img src="C:/Users/17363/AppData/Roaming/Typora/typora-user-images/image-20240701091147959.png" alt="image-20240701091147959" style="zoom:33%;" />

### 获取和修改Bean属性

**getProperty动作标记**

**setProperty动作标记**

### Beans的辅助类



## Servlet

### Servlet概述

**servlet工作原理**

* init  初始化一次
* service  每次访问请求调用一次   ->   创建一个线程
* destroy 销毁一次

**init方法**

* super.init  父类中
* 先init(有参 config)
* 后super.init(有参)

* 重写  无参init方法是为了防止程序远在写servlet类重写有参init时忘记写super.init(config)

**编写部署文件 Web.xml**

* Tomcat服务器编写一个部署文件

**提交数据**

* 通过表单JSP
  * 不加 /
* 通过超链接
  * 不加 /

**共享变量**

* servlet类的成员变量是被所有线程共享的数据

**请求转发**

* 同一服务器中的资源
* 一次请求
* 地址栏不变
* 共享请求，响应对象

**重定向**

* 任意服务器资源
* 两次请求
* 地址栏变化
* 重建请求、响应对象



## MVC

* Servlet 控制器  -> 核心
* JSP视图
* JavaBean 模型



## 数据库

> 存储数据的仓库

**DBMS数据库管理系统**

**常用的SQL语句**

增删改查

**关系型数据库**

* 数据都是由表的形式来组织的

* 表是用两维关系（行和列）来反映现实中实体及它的属性
  * 表的每一行都代表实体的一个实例
  * 每一列都代表了实体的一项属性（又叫表的字段）

### **MySQL**

* 建立连接
* 创建数据库
* 建表
* 删除数据库  drop



### JDBC

提供了访问数据库的API

* DriverManager类  数据库不同，管理JDBC驱动
* Connection接口    连接数据库，并担任传送数据的任务
* Statement接口      



**解决乱码**

* 创建数据库时指定数据库的字符编码
* 创建表时，可以指定某个字段使用的字符编码
