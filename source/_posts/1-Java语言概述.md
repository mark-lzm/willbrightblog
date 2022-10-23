# 1-Java语言概述

## 一、整体语言概述



<!-- ![image-20220802103614465](.\image\image-20220802103614465.png) -->

---

## 二、Java语言概述

### 1.基础常识

- 软件：即一系列按照特定顺序组织的计算机数据和指令的集合。分为：**系统软件** 和 **应用软件**
  - 系统软件：`windows , mac os , linux, unix, android, ios,....`
  - 应用软件：`word, ppt, 画图板,...`

- 人机交互方式： 图形化界面  vs  命令行方式

- 应用程序 = 算法 + 数据结构

### 2.计算机语言的发展迭代史

- 第一代：机器语言 - 指令以二进制代码形式存在。

- 第二代：汇编语言 - 使用助记符表示一条机器指令。

- 第三代：高级语言
  - 面向过程：`C、Pascal、Fortran`
  - 面向对象：`Java、JS、Python、Scala,...`

> **Java语言版本迭代概述**
>
> 1991年 Green项目，开发语言最初命名为Oak (橡树)
>
> 1994年，开发组意识到Oak 非常适合于互联网
>
> 1996年，发布JDK 1.0，约8.3万个网页应用Java技术来制作
>
> 1997年，发布JDK 1.1，JavaOne会议召开，创当时全球同类会议规模之最
>
> 1998年，发布JDK 1.2，同年发布企业平台J2EE
>
> 1999年，Java分成J2SE、J2EE和J2ME，JSP/Servlet技术诞生
>
> 2004年，发布里程碑式版本：JDK 1.5，为突出此版本的重要性，更名为JDK 5.0
>
> 2005年，J2SE -> JavaSE，J2EE -> JavaEE，J2ME -> JavaME
>
> 2009年，Oracle公司收购SUN，交易价格74亿美元
>
> 2011年，发布JDK 7.0
>
> 2014年，发布JDK 8.0，是继JDK 5.0以来变化最大的版本
>
> 2017年，发布JDK 9.0，最大限度实现模块化
>
> 2018年3月，发布JDK 10.0，版本号也称为18.3
>
> 2018年9月，发布JDK 11.0，版本号也称为18.9

- 是**SUN**（**S**tanford **U**niversity **N**etwork，斯坦福大学网络公司) 1995年推出的一门高级编程语言。
- Java之父**James Gosling**

### 3.Java语言的特点

1. **面向对象**

   两个基本概念：**类、对象**

   三大特性：**封装、继承、多态**

2. **健壮性**

   1. 吸收了C/C++语言的优点，去掉了其影响程序健壮性的部分（如指针、内存的申请与释放等），提供了一个**相对安全**的**内存管理**和**访问机制**。
   2. 自动的垃圾回收机制

3. **跨平台性**

   通过Java语言编写的应用程序，在**不同的系统平台**上都可以**运行**。

   原理：在需要运行 java 应用程序的操作系统上，安装一个**Java虚拟机**（**JVM** **J**ava **V**irtual **M**achine)

> 白皮书特点：
>
> 1）简单性
> 2）面向对象
> 3）分布式
> 4）健壮性
> 5）安全性
> 6）体系结构中立
> 7）可移植性
> 8）解释型
> 9）高性能
> 10）多线程
> 11）动态性

### 4.Java两种核心机制

1. Java虚拟机 (Java Virtual Machine)
2. 垃圾收集机制 (Garbage Collection)

#### 1.核心机制 — Java虚拟机

- JVM是一个**虚拟的计算机**，具有**指令集并使用不同的存储区域。负责执行指令，管理数据、内存、寄存器。**
- JVM实现 **“一次编译，到处运行”**

#### 2.核心机制 — 垃圾回收

- 不再使用的内存空间应回收 —— 垃圾回收。
- 垃圾回收在Java程序运行过程中自动进行，程序员无法精确控制和干预。
- **Java程序还会出现 内存泄漏 和 内存溢出 的问题吗？ Yes!**

---

## 三、开发环境的搭建

### 1. JDK、JRE、JVM的关系



<img src=".\image\image-20220802110804207.png" alt="image-20220802110804207" style="zoom:50%;" />

- **JDK(Java Development Kit Java开发工具包)**

  JDK是提供给Java开发人员使用的， 其中包含了**java的开发工具**，也包括了**JRE**。所以安装了JDK，就不用在单独安装JRE了。

  - 其中的开发工具： 编译工具(javac.exe) 、打包工具(jar.exe)等

  >  JDK = JRE + 开发工具集（ 例如Javac编译工具等）

- **JRE(Java Runtime Environment Java运行环境)**

  包括Java虚拟机(JVM Java Virtual Machine)和Java程序所需的核心类库等，如果想要运行一个开发好的Java程序， 计算机中只需要安装JRE即可。

  > JRE = JVM + Java SE标准类库

### 2.下载并安装JDK

- 下载：官网，GitHub

- 安装：傻瓜式安装：JDK 、JRE

- **配置环境变量 path**

  <img src=".\image\image-20220802112338542.png" alt="image-20220802112338542" style="zoom:50%;" />

---

## 四、第一个Java程序

<img src=".\image\image-20220802112309949.png" alt="image-20220802112309949" style="zoom:50%;" />



```java
//创建一个java源文件：HelloWorld.java
class HelloWorld{
	public static void main(String[] args){
		System.out.println("Hello,World!");
	}
}
```

```java
//编译
javac HelloWorld.java
```

```java
//运行
java HelloWord
```

---

## 五、注释与API文档

### 1. 注释:Comment

- 单行注释：`//注释内容`
- 多行注释：`/* 注释内容 */`
- 文档注释：`/** 注释内容 */`

特点：

1. 单行注释和多行注释，注释了的内容不参与编译。换句话说，编译以后生成的 `.class` 结尾的字节码文件中不包含注释掉的信息
2. 文档注释内容可以被JDK提供的工具 javadoc 所解析，生成一套以网页文件形式体现的该程序的说明文档。
3. 多行注释不可以嵌套使用

### 2. Java API 文档

- API: application programming interface。习惯上：将语言提供的类库，都称为API
- API文档：针对于提供的类库如何使用，给的一个说明书。类似于《新华字典》