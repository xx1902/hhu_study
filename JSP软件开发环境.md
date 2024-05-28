**画图工具 Visio**

**配置管理工具 Visual Source Safe**      VSS

* Git

* Subversion  SVN

**数据库建模工具 PowerDesigner**

**UML建模工具 Rational Rose**





## web开发技术概述

### 计算机网络

> 用通信线路和通信设备将分在不同地点的具有独立功能的多个计算器链接起来，实现彼此之间的数据通信和资源共享的系统

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

**DNS域名解析系统**

> 在因特网上作为域名和IP地址相互映射的一个分布式数据库

* 通过主机名得到主机名对应的IP地址的过程叫做域名解析
* 整个DNS是由许多域所组成，每个域下又细分更多的域

**URL** 统一资源**定位符**

以统一方式唯一确定某个网络资源，相当于通讯地址



### Web

**架构：**

* HTML（超文本技术）实现信息与信息的链接
* URI（统一资源**标识符**） 实现全球的精确定位
* HTTP（新的应用层协议）实现分布式的信息共享

**Web网站体系三层结构**

* 浏览器
* 应用服务器
* 数据库服务器

**Web数据库访问技术**

* CGI技术
* ASP技术 （动态服务器页面）
* PHP技术 （超文本预处理器）
  * 免费，跨平台，支持ODBC数据库连接
* JSP技术  （服务器页面）
  * 多平台

**Web开发技术**

* HTML技术
* DHTML技术 （动态）
* Java Applet技术
  * 小应用程序
  * 主要应用于各种网页文件中-->增强网页的人机交互
* JavaScript与VBScript
  * JavaScript 最广泛的脚本语言
  * 基于对象的事件驱动的编程语言
  * 不需要jaava解释器，直接在Web浏览器中解释执行
* ActiveX控件
* ASP.NET
  * 完全基于模块和组件，有更好的可扩展性和可定制性
* AJAX
  * 不刷新整个页面，在页面内与服务器通信
  * 异步通讯，不需要打断用户操作

### HTML

[HTML 教程 (w3school.com.cn)](https://www.w3school.com.cn/html/index.asp)

超文本标记语言，由各种标记符组成

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
* 列表标记 ul ol
* 超链接标记 href
* 表单标记 form
* 列表框 select
* 窗口框架标记 framset
* 定义特定显示区  div



### CSS

美化页面

样式表

* 内联式
* 嵌入式
* 外部链接式



### DHTML

>是技术，标准和规范的一种集成

客户端  -> 在本地执行

* 将页面内容对象化
* 网页无需重新下载



### XML

把内容和显示格式分开 -> 使XML文件制作者集中于数据本身 

复用

功能

* 异种数据的交互 （不同的数据库）
* 数据的多样化显示

语法

* 区分大小写<?xml  >
* 文件的第一行必须是xml文件声明



### J2EE

J2EE组件：由java语言编写、封装了功能的软件单元

Java Servlet技术

Java Servlet Pages技术

* JSP先是转义成Servlet之后再运行，第一次JSP更慢
* JSP 是HTML嵌套Java，   JSP会
* Servlet是Java嵌套HTML -> 要发送到浏览器所以嵌套html







## JSP

配置JSP环境

* 安装和配置JDK
* 安装和启动Tomcat服务器 （安装板和解压版）
* 测试Tomcat服务器 localhost:8080
* 配置端口 conf -> sever.xml
* 设置Tomcat的环境变量

设置Web服务目录

* 根目录
* Webapps下的Web服务目录
* 虚拟目录 conf -> .xml
* 相对目录



## JSP基础语法

**5中元素**

* HDML   ->    客户端
* JSP标记  如指令标识，动作标识
* 变量和方法的声明                                                                                                            
* java程序片段
* java表达式



**变量**

* 局部变量  -> 每次刷新页面，局部都会初始化

  ```jsp
  < % int i = 0; % >
  ```

  

* 成员变量  -> 各个用户共享

  ```jsp
  < % ! int i  0; % >
  ```

  

**方法**

* < % !   % >

* 在整个JSP页面中有效
* 方法内定义的变量只在方法内有效

**程序片段**

* 按顺序执行

* 多个客户同时访问，程序片段将被执行多次，在不同的线程中互不影响

* 程序片的变量是局部变量

* 设置共享成员变量，要注意同步 

  ```jsp
  < % ! 
     int i = 0;
     snchronized void add(){
     i ++;
     }
   % >
     <%-- 程序片段 --%>
  < %
      out.print
     % >
  ```

* 可以将一个java程序片段分割成几个java程序片段   -> 不同的样式



**Java表达式**

* 表达式必须能求值

* <% 和 =不能有空格

  ```jsp
  <%= getDate() % >
  ```

**JSP注释**

HTML <!-- 注释-->  显式

JSP注释 <%-- 注释 --%>

java注释 //



**JSP指令标识**

**page标识**

* page标识
  * 可以用一个page指定多个属性的值，也可以使用多个page指令分别为每个属性指定值
* contentType属性
  * 不允许两次使用page给contentType属性指定不同的属性值
  * 确定 MIME类型 和JSP字符编码
* language属性
  * 定义脚本语言 'java'
* import属性
  * 引入运行环境的包中的类 
* session属性
  * 是否需要使用内置的session对象
  * 默认属性为true
* buffer属性
  * 缓冲区的大小 默认为8kb
* autoFlush属性
  * 缓冲区是否自动刷新
* isTreadSafe属性
  * 是否支持多线程
* info属性
  * 定义一个常用且可能要经常使用的字符串
  * 用getServletInfo()获取info属性的属性值

**include指令标记**

* 静态插入一个文件，实现代码的复用
* 把一个复杂的JSP页面分解成若干个简单的部分





**JSP动作标记**

* include动作标记
  * jsp页面运行时才将文件加入
* param动作标记
  * 以  名字-值  对的形式为其他标记提供信息
  * 不能独立使用

* forward动作标识
  * 从该指令处停止当前页面的执行，转向执行page属性指定的JSP页面
  * 显示的仍然是转向前的JSP页面的URL地址
* useBean动作标记
  * 设置Bean的简单属性和索引属性
* setProperty动作标记
  * 设置Bean的简单属性和索引属性
* getProperty动作标识
  * 访问一个Bean属性





## JSP内置对象

### request对象

* 封装了用户提交的信息
* HTTP请求报文
  * 请求行
  * 请求头
  * 信息体
* 处理问题
  * 获取用户提交的信息
    * getParameter()
    * 和post提交的最大区别
      * 可以在链接（最上面）中看到
      * post看不到，post遇到中中文可能会乱码  8859-1
  * 处理中文信息
    * 重新编码  请求是iso-8859-1
    * 设置编码格式 setCharacterEncoding()
  * 获取其他信息

### respose对象

> 用于响应客户请求

方法包括

* 设定响应状态码的方法
* 设定表头的方法
* URL重写

动态设置MIME（响应）类型

* setContentType()

response的HTTP头

* addHeader()
* setHeader()

response的重定向

* sendRedirect()

respose的状态行

* 状态码

### session对象

> 记录有关链接的信息 -> 区分不同用户

session对象的ID

* 服务器为用户分配一个session对象
* 关闭浏览器后，会话结束，再次开启会创建一个新的session对象
