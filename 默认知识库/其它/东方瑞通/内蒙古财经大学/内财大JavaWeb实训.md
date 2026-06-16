# 内财大 JavaWeb 实训

# 实训内容介绍

## 实训目标

为了让学生了解、熟悉企业软件开发模式及流程，提高学生软件编程技术的实战能力。

本实训项目采用案例驱动模式，并模拟企业的实际项目开发流程，通过指导老师来带领学生完成项目的前期调研、策划、需求分析、总体设计、详细设计、编码、测试、文档及PPT编写等环节的工作任务，写作完成一个项目的开发，提高学生的项目实战能力。并达成以下的目标：

1. <font style="color:rgb(0,0,0);">掌握JavaWeb开发环境及Tomcat的搭建；熟悉JavaEE技术规范，了解Servlet，jsp，EL，JSTL等</font>
2. <font style="color:rgb(0,0,0);">指导学生进行需求分析报告的拟定以及实训报告的编写</font>
3. <font style="color:rgb(0,0,0);">熟练掌握EL常用标签及用法，熟练使用JSP搭建网页界面</font>
4. <font style="color:rgb(0,0,0);">熟悉JSTL表达式，以及各自的用法和应用场景</font>
5. <font style="color:rgb(0,0,0);">掌握Request和Response技术</font>
6. <font style="color:rgb(0,0,0);">掌握JSP四大作用域</font>
7. <font style="color:rgb(0,0,0);">熟练掌握项目在Tomcat发布和访问</font>

## <font style="color:rgb(0,0,0);">实训周期</font>

<font style="color:rgb(0,0,0);">本实训案例需3周（15天）</font>

## <font style="color:rgb(0,0,0);">项目相关知识点</font>

<font style="color:rgb(0,0,0);">本项目的顺利实施离不开对基础知识的掌握，下表列出所需的核心技术知识点：</font>

* Java 语言：是我们本次实训过程中主要的编程语言
* MySQL 数据库：存储项目中的数据
* JDBC：操作数据库
* Servlet：服务端小程序
* JSP：页面
* EL、JSTL：页面展示数据
* Filter：过滤器
* 等等

# Java 介绍及环境搭建

## Java 概述

* 是 SUN（Standford University Network，斯坦福大学网络公司）1995年推出的一门高级编程语言
* 是一种面向 Internet 的编程语言。java 一开始富有吸引力是因为 java 程序可以在 web 浏览器中运行。这些 java 程序被称为java小程序（applet）。applet 使用现代的图形用户界面与 web 用户进行交互。applet 内嵌在 html 代码中
* 随着 java 技术在 web 方面的不断成熟，已经成为 web 应用程序的首选开发语言

## 应用方向

Java 语言的应用方向主要体现在以下几个方面：

* 企业级应用：

主要指复杂的大企业的软件系统、各种类型的网站。Java的安全机制一级它的跨平台的优势，使它在分布式系统领域开发中有广泛的应用。应用领域包括金融、电信、交通、电子商务等。

* Android 平台应用：

Android 应用程序使用Java语言编写。Android开发水平的高低很大程度上取决于Java语言核心能力是否扎实

* 大数据平台开发：

各类框架有Hadoop，spark，storm，flink等，就这类技术生态圈来讲，还有各种中间件如flume，kafka，sqoop等等，这些框架以及工具大多数是用Java编写而成，但提供诸如Java，Scala，Python，R等各种语言API供编程。

## JDK

### 什么是 JDK

* JDK（Java Development Kit，java开发工具包）
  * JDK是提供给Java开发人员使用的，其中包含了java的开发工具和JRE。所以安装了JDK，就不需要再单独安装JRE了
  * 其中的开发工具：编译工具（javac.exe）、打包工具（jar.exe）等
* JRE（Java Runtime Environment，Java运行环境）
  * 包括Java虚拟机（JVM，Java Virtual Machine）和Java程序所需的核心类库等
  * 如果想要运行一个开发好的Java程序，计算机中只需要安装JRE即可
* Java 虚拟机（Java Virtual Machine）
  * JVM 是一个虚拟的计算机，具有指令集并使用不同的存储区域。负责执行指令，管理数据、内存、寄存器。
  * 对于不同的平台，有不同的虚拟机
  * Java 虚拟机机制屏蔽了底层运行平台的差别，实现了“一次编译，到处运行”
* 结构示意图

![1724490431250-74231850-f560-47a2-a639-7d0e05b176ba.png](./img/TvMXBSJiS74TOLoG/1724490431250-74231850-f560-47a2-a639-7d0e05b176ba-891155.png)

JDK = JRE + 开发工具集（例如javac编译工具等）

JRE = JVM + JavaSE标准类库

### 安装 JDK

* 傻瓜式安装，下一步即可
* 建议：安装路径中不要有中文或空格等特殊符号
* 当提示安装JRE时，正常在JDK安装时已经装过了，但是为了后续使用eclipse等开发工具不报错，建议也根据提示安装JRE

安装步骤截图如下：

![1724490534167-e502e055-3801-42b4-9dbc-bb5491185d31.png](./img/TvMXBSJiS74TOLoG/1724490534167-e502e055-3801-42b4-9dbc-bb5491185d31-242847.png)

![1724492318095-668f93dd-1bce-45cd-939f-f84f444a36e6.png](./img/TvMXBSJiS74TOLoG/1724492318095-668f93dd-1bce-45cd-939f-f84f444a36e6-852862.png)

![1724492334429-de46f476-8036-4460-8503-d6d858d16270.png](./img/TvMXBSJiS74TOLoG/1724492334429-de46f476-8036-4460-8503-d6d858d16270-201605.png)

![1724492349329-068a2423-db65-4cd5-9e23-5c3c26d7d8d6.png](./img/TvMXBSJiS74TOLoG/1724492349329-068a2423-db65-4cd5-9e23-5c3c26d7d8d6-429227.png)

![1724492371217-7b0be2cd-a1fc-487c-803b-7e9042d3e834.png](./img/TvMXBSJiS74TOLoG/1724492371217-7b0be2cd-a1fc-487c-803b-7e9042d3e834-414669.png)

![1724492391562-fc7704f5-aa2a-4ab9-a5d5-d9eb853f77c0.png](./img/TvMXBSJiS74TOLoG/1724492391562-fc7704f5-aa2a-4ab9-a5d5-d9eb853f77c0-726561.png)

![1724492407258-4e0a90d9-46c6-47be-9b1d-4de95b5350cd.png](./img/TvMXBSJiS74TOLoG/1724492407258-4e0a90d9-46c6-47be-9b1d-4de95b5350cd-379712.png)

![1724492457754-3e94cac5-bbcc-4543-9b11-827b62fd42f4.png](./img/TvMXBSJiS74TOLoG/1724492457754-3e94cac5-bbcc-4543-9b11-827b62fd42f4-430415.png)

![1724492505528-ae6e0c17-ac15-48ba-8a87-f5bc629cda7d.png](./img/TvMXBSJiS74TOLoG/1724492505528-ae6e0c17-ac15-48ba-8a87-f5bc629cda7d-881073.png)

安装完成！

### <font style="color:rgb(0,0,0);">配置环境变量</font>

配置环境变量的目的：在任何电脑的目录都可以使用 JDK 中的工具。

![1724490701528-13899af1-e336-458f-bbe6-10d9e421e9a2.png](./img/TvMXBSJiS74TOLoG/1724490701528-13899af1-e336-458f-bbe6-10d9e421e9a2-920717.png)

![1724490744464-58d47ef4-1ffb-4e11-8885-6d814fcd5da1.png](./img/TvMXBSJiS74TOLoG/1724490744464-58d47ef4-1ffb-4e11-8885-6d814fcd5da1-191551.png)

![1724490751867-b1a93386-e916-4c7b-b12c-12aa50c5293e.png](./img/TvMXBSJiS74TOLoG/1724490751867-b1a93386-e916-4c7b-b12c-12aa50c5293e-940657.png)

![1724490762364-e281a53c-ac47-4515-aeaa-8b9880b41e70.png](./img/TvMXBSJiS74TOLoG/1724490762364-e281a53c-ac47-4515-aeaa-8b9880b41e70-447153.png)

![1724490974716-d1df23d5-7f60-4276-b32d-7949836af012.png](./img/TvMXBSJiS74TOLoG/1724490974716-d1df23d5-7f60-4276-b32d-7949836af012-851754.png)

![1724490987227-2f516ee0-c09c-4202-83dd-408cdb7b7b3c.png](./img/TvMXBSJiS74TOLoG/1724490987227-2f516ee0-c09c-4202-83dd-408cdb7b7b3c-014659.png)

环境变量配置完成！

### <font style="color:rgb(0,0,0);">检测环境变量是否配置正确</font>

1. 使用 windows+r，打开运行窗口

![1724491092962-c3fa24dd-aba0-4d2b-b0ff-c6a1c664b759.png](./img/TvMXBSJiS74TOLoG/1724491092962-c3fa24dd-aba0-4d2b-b0ff-c6a1c664b759-316487.png)

2. 在窗口中输入cmd，点击确定

![1724491103484-635226df-fd20-40ef-a4a3-0c6746027a88.png](./img/TvMXBSJiS74TOLoG/1724491103484-635226df-fd20-40ef-a4a3-0c6746027a88-324151.png)

3. 出现黑窗口（dos命令窗口）

![1724491117479-42229823-e09b-4bcd-960d-b87bc01be7ce.png](./img/TvMXBSJiS74TOLoG/1724491117479-42229823-e09b-4bcd-960d-b87bc01be7ce-934413.png)

4. 在黑窗口中输入java，回车

![1724491128724-9d1fb7b6-9492-45d0-9057-9d65f2762006.png](./img/TvMXBSJiS74TOLoG/1724491128724-9d1fb7b6-9492-45d0-9057-9d65f2762006-106961.png)

5. 在黑窗口中输入javac，回车

![1724491159386-8bcc68ad-439d-41e5-990e-3674d000b156.png](./img/TvMXBSJiS74TOLoG/1724491159386-8bcc68ad-439d-41e5-990e-3674d000b156-039002.png)

## IDEA

### 介绍

IDEA，全称IntelliJ IDEA，是 Java 语言的集成开发环境，IDEA 在业界被公认为是最好的 java 开发工具之一，尤其在智能代码助手、代码自动提示、重构、J2EE支持、Ant、JUnit、CVS 整合、代码审查、创新的GUI 设计等方面的功能可以说是超常的。

### 安装

![1724491950161-608d4947-dbce-4e71-a618-ecd7f8419b17.png](./img/TvMXBSJiS74TOLoG/1724491950161-608d4947-dbce-4e71-a618-ecd7f8419b17-214669.png)

![1724491991698-579ea7f2-e86e-4fa2-8bb5-ada7b05348fd.png](./img/TvMXBSJiS74TOLoG/1724491991698-579ea7f2-e86e-4fa2-8bb5-ada7b05348fd-994807.png)

![1724492014178-a0c4869b-5f22-4a3d-b3e4-68c871238e8e.png](./img/TvMXBSJiS74TOLoG/1724492014178-a0c4869b-5f22-4a3d-b3e4-68c871238e8e-290162.png)

![1724492096246-d52fae9f-2169-4e1c-a0e6-59363439b956.png](./img/TvMXBSJiS74TOLoG/1724492096246-d52fae9f-2169-4e1c-a0e6-59363439b956-670267.png)

![1724492109531-176f3ca8-efcf-418c-b6ab-08b871df117c.png](./img/TvMXBSJiS74TOLoG/1724492109531-176f3ca8-efcf-418c-b6ab-08b871df117c-045562.png)

![1724492138781-457d07d1-2376-48b4-9ef0-06f4d672c0c4.png](./img/TvMXBSJiS74TOLoG/1724492138781-457d07d1-2376-48b4-9ef0-06f4d672c0c4-071197.png)

![1724492234358-5063e418-2084-4372-90ef-a9eb500ddcbc.png](./img/TvMXBSJiS74TOLoG/1724492234358-5063e418-2084-4372-90ef-a9eb500ddcbc-087106.png)

![1724492246899-8c066ba8-0c27-46eb-a544-2d55aed45b41.png](./img/TvMXBSJiS74TOLoG/1724492246899-8c066ba8-0c27-46eb-a544-2d55aed45b41-674015.png)

上图就是安装完后 IDEA 在桌面的快捷方式。

### 配置

双击桌面的 IDEA 快捷方式图标，打开 IDEA

![1724492641439-07e24024-43ba-4893-bc50-c5b6fc25ad27.png](./img/TvMXBSJiS74TOLoG/1724492641439-07e24024-43ba-4893-bc50-c5b6fc25ad27-490883.png)

![1724492681615-685528d2-fc57-422e-bf59-9f3f47938d45.png](./img/TvMXBSJiS74TOLoG/1724492681615-685528d2-fc57-422e-bf59-9f3f47938d45-262136.png)

![1724492712956-83828363-9421-4a82-846a-5622c0737f03.png](./img/TvMXBSJiS74TOLoG/1724492712956-83828363-9421-4a82-846a-5622c0737f03-870587.png)

![1724492818485-23e1753d-1beb-4323-a8ee-676b182ab1fe.png](./img/TvMXBSJiS74TOLoG/1724492818485-23e1753d-1beb-4323-a8ee-676b182ab1fe-951608.png)

![1724492843931-b23845c7-6b21-483f-88af-2596b5cd7930.png](./img/TvMXBSJiS74TOLoG/1724492843931-b23845c7-6b21-483f-88af-2596b5cd7930-960372.png)

![1724492863791-272e7caa-0451-4e4d-a141-d7a47570c899.png](./img/TvMXBSJiS74TOLoG/1724492863791-272e7caa-0451-4e4d-a141-d7a47570c899-532730.png)

![1724492910297-bd8469eb-63e1-40e5-abe1-ad6b67481686.png](./img/TvMXBSJiS74TOLoG/1724492910297-bd8469eb-63e1-40e5-abe1-ad6b67481686-504904.png)

![1724492957818-5bb5d9fd-5d32-4ec9-964c-7399366369bd.png](./img/TvMXBSJiS74TOLoG/1724492957818-5bb5d9fd-5d32-4ec9-964c-7399366369bd-402700.png)

### 设置字体大小

![1724493066778-a44549a5-b0aa-4c14-9b55-17f9b47355ad.png](./img/TvMXBSJiS74TOLoG/1724493066778-a44549a5-b0aa-4c14-9b55-17f9b47355ad-252904.png)

![1724493166078-29b55ef2-4016-4f18-aeb7-6f30186290c3.png](./img/TvMXBSJiS74TOLoG/1724493166078-29b55ef2-4016-4f18-aeb7-6f30186290c3-547343.png)

### <font style="color:rgb(0,0,0);">设置忽略大小写&参数提示</font>

![1724493066778-a44549a5-b0aa-4c14-9b55-17f9b47355ad.png](./img/TvMXBSJiS74TOLoG/1724493066778-a44549a5-b0aa-4c14-9b55-17f9b47355ad-252904.png)

![1724493316170-46829582-ae7d-4ad9-91db-897ed95fcf22.png](./img/TvMXBSJiS74TOLoG/1724493316170-46829582-ae7d-4ad9-91db-897ed95fcf22-013693.png)

# 入门案例

## 创建项目

![1724564179585-d85d59b8-936e-4431-8076-2d9ba35ecf93.png](./img/TvMXBSJiS74TOLoG/1724564179585-d85d59b8-936e-4431-8076-2d9ba35ecf93-716223.png)

![1724564203797-629ee317-cd95-4635-bb3e-ec28c4070062.png](./img/TvMXBSJiS74TOLoG/1724564203797-629ee317-cd95-4635-bb3e-ec28c4070062-523479.png)

![1724564220979-73845346-4514-4c82-a12b-0573825ebde0.png](./img/TvMXBSJiS74TOLoG/1724564220979-73845346-4514-4c82-a12b-0573825ebde0-334017.png)

![1724564300999-24d156c6-9fc5-4f69-ab7d-c4d9389ef500.png](./img/TvMXBSJiS74TOLoG/1724564300999-24d156c6-9fc5-4f69-ab7d-c4d9389ef500-642270.png)

![1724564326976-6b9b525e-e594-42ec-b928-ecb44ba64eb0.png](./img/TvMXBSJiS74TOLoG/1724564326976-6b9b525e-e594-42ec-b928-ecb44ba64eb0-384093.png)

## 创建类

![1724564365227-f83457a0-394d-49b4-bc25-0e77b5d83899.png](./img/TvMXBSJiS74TOLoG/1724564365227-f83457a0-394d-49b4-bc25-0e77b5d83899-314169.png)

![1724564393866-b4a487a1-8b38-403c-b3e5-b4058f4ad585.png](./img/TvMXBSJiS74TOLoG/1724564393866-b4a487a1-8b38-403c-b3e5-b4058f4ad585-669639.png)

![1724564413044-8ef7ba44-ebc9-4f40-8c2a-b781bd700495.png](./img/TvMXBSJiS74TOLoG/1724564413044-8ef7ba44-ebc9-4f40-8c2a-b781bd700495-569166.png)

## 编写代码

```java
public class Demo {

    // main方法是程序的入口，写法固定
    // 快捷方式：输入main,然后回车即可快速生成
    public static void main(String[] args) {

        // 输入内容到控制台
        // 快捷方式：输入sout,然后回车即可快速生成
        System.out.println("hello world!");
    }
}
```

## 运行程序

![1724564760088-69b74b72-4c7c-4733-8680-c1995a8a1740.png](./img/TvMXBSJiS74TOLoG/1724564760088-69b74b72-4c7c-4733-8680-c1995a8a1740-238924.png)

:::info
**结果**

:::

![1724564786127-8409d777-549b-4181-b925-2883802dc106.png](./img/TvMXBSJiS74TOLoG/1724564786127-8409d777-549b-4181-b925-2883802dc106-787345.png)

# 变量与数据类型

## 变量的定义

* 变量的概念
  * 内存区域中的一个存储区域
  * 该区域的数据可以在同一类型范围内不断变化
  * 变量是程序中最基本的存储单元。包含变量类型、变量名和存储的值
* 变量的作用
  * 用于在内存中保存数据
* 使用变量注意
  * java中每个变量必须先声明，后使用
  * 使用变量名来访问这块区域的数据
  * 变量的作用域：其定义所在的一对{}内
  * 变量只有在其作用域内才有效
  * 同一个作用域内，不能定义重名的变量
* 变量的定义格式：`数据类型 变量名 = 变量值;`
* 案例

```java
public class Demo2 {

    public static void main(String[] args) {

        // 定义变量
        int age = 20;
        // 使用变量
        System.out.println(age);

        // 声明变量
        int count;
        // 给变量赋值
        count = 5;
        System.out.println(count);
    }
}
```

## 数据类型

### 概述

在java中，对每一种数据都定义了明确的具体数据类型（强类型语言），在内存中分配了不同大小的内存空间。

![1724575163130-cd327ae3-c30b-460c-b863-bfa046ef630e.png](./img/TvMXBSJiS74TOLoG/1724575163130-cd327ae3-c30b-460c-b863-bfa046ef630e-355842.png)

### 整数类型

整数类型中，我们常用的是 int 类型。

```java
public class Demo2 {

    public static void main(String[] args) {

        // 定义变量
        int age = 20;
        // 使用变量
        System.out.println(age);

        // 声明变量
        int count;
        // 给变量赋值
        count = 5;
        System.out.println(count);
    }
}
```

### 浮点类型

浮点数类型，我们常用的是 double。

```java
public class Demo2 {

    public static void main(String[] args) {

        // 定义变量
        double price = 3.5;
        // 使用变量
        System.out.println(price);
    }
}
```

### 布尔类型

* 只能有两个值：true和false
* 在判断和循环结构中使用
* 案例：

```java
public class Demo2 {

    public static void main(String[] args) {

        boolean b = true;
        System.out.println(b);
        if(b){
            System.out.println("是真的！");
        }else{
            System.out.println("是假的！");
        }
    }
}
```

### String 类型

* String不是基本数据类型，属于引用数据类型
* 使用方式与基本数据类型一致。例如：String str = “abcd”;
* 注意：String类型的值必须使用双引号引起来
* 一个字符串可以串接另一个字符串，也可以直接串接其他类型的数据；任何数据类型和字符串类型进行串接得到的结果都是字符串类型
* 案例

```java
public class Demo2 {

    public static void main(String[] args) {

        String s1 = "hello world";
        System.out.println(s1);

        String s2 = "年龄：";
        int age = 20;
        s2 = s2 + age;
        System.out.println(s2);

        String name = "张三";
        System.out.println("姓名：" + name);
    }
}
```

# 运算符

## 概述

运算符是一种特殊的符号，用以表示数据的运算、赋值和比较等。

java中的运算符有：

* 算术运算符
* 赋值运算符
* 比较运算符（关系运算符）
* 逻辑运算符
* <font style="color:rgb(165,165,165);">位运算符</font>
* 三元运算符

## 比较运算符

| **<font style="color:rgb(255,255,255);">比较运算符</font>** | **<font style="color:rgb(255,255,255);">说明</font>** | **<font style="color:rgb(255,255,255);">范例</font>** | **<font style="color:rgb(255,255,255);">结果</font>** |
| --- | --- | --- | --- |
| **=\*\*\*\*=** | 相等于 | 4 == 3 | false |
| **!\*\*\*\*=** | 不等于 | 4 != 3 | true |
| **<** | 小于 | 4 < 3 | false |
| **>** | 大于 | 4 > 3 | true |
| **<\*\*\*\*=** | 小于等于 | 4 <= 3 | false |
| **>=** | 大于等于 | 4 >= 3 | true |

比较运算符的结果都是boolean类型的，也就是要么是true，要么是false

比较运算符`==`不能误写成`=`

```java
public class Demo2 {

    public static void main(String[] args) {

        int i = 20;
        int j = 10;
        System.out.println(i == j); // ==是比较运算，false
        System.out.println(i = j); // =是赋值运算，10
    }
}
```

## 逻辑运算符

逻辑与：&		逻辑或：|		**<font style="background-color:#ECAA04;">逻辑非：!	</font>**	逻辑异或：^

**<font style="background-color:#ECAA04;">短路与：&&</font>**\*\*		\*\***<font style="background-color:#ECAA04;">短路或：||</font>**

| **<font style="color:rgb(255,255,255);">a</font>** | **<font style="color:rgb(255,255,255);">b</font>** | **<font style="color:rgb(255,255,255);">a && b</font>** | **<font style="color:rgb(255,255,255);">a || b</font>** | **<font style="color:rgb(255,255,255);">!a</font>** |
| --- | --- | --- | --- | --- |
| **t\*\*\*\*rue** | **t\*\*\*\*rue** | true | true | false |
| **t\*\*\*\*rue** | **f\*\*\*\*alse** | false | true | false |
| **f\*\*\*\*alse** | **t\*\*\*\*rue** | false | true | true |
| **f\*\*\*\*alse** | **f\*\*\*\*alse** | false | false | true |

规律：

与：两边都是true时结果才是true

或：两边有一个是true时结果就是true

非：就是取反

```java
public class Demo2 {

    public static void main(String[] args) {

        int age = 20;
        String s = "放假";

        // 比较两个字符串是否相等，使用equals方法
        if(age >= 18 && s.equals("放假")){
            System.out.println("可以独自出去玩啦！");
        }else{
            System.out.println("不能出去玩！");
        }
    }
}
```

# 程序流程控制

## 概述

* 流程控制语句是用来控制程序中各语句执行顺序的语句，可以把语句组合成能完成一定功能的小逻辑模块
* 流程控制方式采用结构化程序设计中规定的三种基本流程结构，即：
  * 顺序结构
    * 程序从上到下逐行地执行，中间没有任何判断和跳转
  * 分支结构
    * 根据条件，选择性地执行某段代码
    * 有if-else和switch-case两种分支语句
  * 循环结构
    * 根据循环条件，重复性的执行某段代码
    * 有while、do-while、和for三种循环语句
    * 注：JDK1.5提供了foreach循环，方便遍历集合、数组元素

## 分支结构-if-else结构

if语句的三种格式：

:::info
**第一种**

:::

```java
if(条件表达式){
	执行代码块;
}
```

![1724579825517-231056a8-cf8c-4070-94d6-77e76f46f897.png](./img/TvMXBSJiS74TOLoG/1724579825517-231056a8-cf8c-4070-94d6-77e76f46f897-827177.png)

:::info
**第二种**

:::

```java
if(条件表达式){
	执行代码块1;
}else{
	执行代码块2;
}
```

![1724579862560-8e2e3c28-33e6-445a-a26d-d2d32a293efd.png](./img/TvMXBSJiS74TOLoG/1724579862560-8e2e3c28-33e6-445a-a26d-d2d32a293efd-713648.png)

:::info
**第三种**

:::

```java
if(条件表达式1){
	执行代码块1;
}
else if(条件表达式2){
	执行代码块2;
}
...
else{
	执行代码块n;
}
```

![1724579924076-9db17422-9ce8-4e49-94ee-b9388aaa88da.png](./img/TvMXBSJiS74TOLoG/1724579924076-9db17422-9ce8-4e49-94ee-b9388aaa88da-606648.png)

案例：

```java
public class Demo2 {

    public static void main(String[] args) {

        int heartBeats = 150;
        if(heartBeats < 60 || heartBeats > 120){
            System.out.println("需要做进一步的检查！");
        }
        System.out.println("检查结束");

        int age = 20;
        if(age < 18){
            System.out.println("你是一个未成年！");
        }else{
            System.out.println("你已经成年了！");
        }

        int score = 95;

        if(score < 60){
            System.out.println("成绩不合格！");
        }else if(score < 70){
            System.out.println("成绩一般！");
        }else if(score < 85){
            System.out.println("成绩良好！");
        }else{
            System.out.println("成绩优秀！");
        }
    }
}
```

## 循环结构

### 概述

* 在某些条件满足的情况下，反复执行特定代码的功能
* 循环语句分类：
  * for循环
  * while循环
  * do-while循环
* 循环语句的四个组成部分
  * 初始化部分
  * 循环条件部分
  * 循环体部分
  * 迭代部分

![1724580403325-6d9cdc57-6810-436b-816b-a08617b1f29d.png](./img/TvMXBSJiS74TOLoG/1724580403325-6d9cdc57-6810-436b-816b-a08617b1f29d-631742.png)

### for循环的使用

* 循环结构的4个要素是：

① 初始化条件

② 循环条件（是boolean类型）

③ 循环体

④ 迭代条件

* for循环结构

```java
for(①;②;④){
	③
}
```

* 执行过程：①-②-③-④-②-③-④-……②
* 案例

```java
public class Demo2 {

    public static void main(String[] args) {

        // 输出5遍 hello world
        for(int i = 1; i <= 5; i++){
            System.out.println("hello world");
        }

        // 遍历100以内的偶数,输出所有偶数的和,输出偶数的个数
        int sum = 0; // 记录所有偶数的和
        int count = 0; // 记录偶数的个数

        for(int i = 1; i <= 100; i++){
            if(i % 2 == 0){ // i 是偶数
                sum = sum + i;
                count++;
            }
        }

        System.out.println("所有偶数的和是：" + sum);
        System.out.println("偶数的个数是：" + count);
    }
}
```

# 数组

## <font style="color:rgb(0,0,0);">概述</font>

* 数组（Array），是多个相同类型数据按一定顺序排列的集合，并使用一个名字命名，并通过编号的方式对这些数据进行统一管理

| 姓名 | 张三 | 李四 | 王五 | 赵六 | 关羽 | 张飞 | 刘备 | 宋江 | 吴用 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 身高 | 170.2 | 165.3 | 185.2 | 190 | 165 | 145 | 187.2 | 156.5 | 180 |

* 数组的常见概念
  * 数组名
  * 索引（或下标）
  * 元素
  * 数组的长度
* 数组本身是引用数据类型，而数组中的元素可以是任何数据类型，包括基本数据类型和引用数据类型
* 数组的长度一旦确定，就不能修改
* 我们可以直接通过下标（索引）的方式调用指定位置的元素，速度很快

## 案例

```java
public class Demo2 {

    public static void main(String[] args) {

        // 回顾变量的声明和初始化
        int num; // 声明变量
        num = 10; // 初始化

        // 1.数组的声明
        int[] ids; // 声明
        // 静态初始化：数组的初始化和元素的赋值同时进行
        ids = new int[]{1,2,3,4,5};
        // 动态初始化：数组的初始化和元素的赋值分开进行
        String[] names = new String[4];

        // 2.如何调用数组的指定位置的元素：通过索引的方式调用
        // 数组的索引是从0开始的，到数组的长度-1结束
        names[0] = "张三";
        names[1] = "李四";
        names[2] = "王五";
        names[3] = "赵六";

        // 3.如何获取数组的长度：通过属性 length
        System.out.println(ids.length);
        System.out.println(names.length);

        // 4.如何遍历数组：通过循环遍历
        for (int i = 0; i < names.length; i++) {
            System.out.println(names[i]);
        }
    }
}
```

# 面向对象

## 面向过程(POP)与面向对象(OOP)

* 二者都是一种思想，面向对象是相对于面向过程而言的。面向过程，强调的是功能行为，以函数为最小单位，考虑怎么做。面向对象，将功能封装进对象，强调具备了功能的对象，以类/对象为最小单位，考虑谁来做。
* 面向对象更加强调运用人类在日常的思维逻辑中采用的思想方法与原则，如抽象、分类、继承、聚合、多态等
* 面向对象的三大特征
  * 封装(Encapsulation)
  * 继承(Inheritance)
  * 多态(Polymorphism)

面向对象：Object Oriented Programming

面向过程：Procedure Oriented Programming

举例说明：

“人把大象装进冰箱”。

1. 面向过程：强调的是功能行为，以函数为最小单位，考虑怎么做

a) 把冰箱门打开

b) 抬起大象，塞进冰箱

c) 把冰箱门关闭

2. 面向对象：强调具备了功能的对象，以类/对象为最小单位，考虑谁来做

```java
人{
    打开(冰箱){
        冰箱.打开();
    }
    
    抬起(大象){
        大象.进入(冰箱);
    }
    
    关闭(冰箱){
        冰箱.闭合();
    }
}

冰箱{
    打开(){
        
    }
    
    闭合(){
        
    }
}

大象{
    进入(冰箱){
        
    }
}
```

面向对象的思想要优于面向过程的。在小项目中不好体现，一旦项目大了起来，那立马就体现出来了。

比如，一个刚创业的公司，可能就4、5个人，一个人可能身兼数职，但是一旦企业发展大，还是一个人身兼数职的话，就乱套了。需要我们划分部门，给每个人划分职责，这样每个人做自己应该负责的即可，不会乱，也比较好管理。

**面向对象思想总结：**

* 程序员从面向过程的执行者转化成了面向对象的指挥者
* 面向对象分析方法分析问题的思路和步骤
  * 根据问题需要，选择问题所针对的现实世界中的实体
  * 从实体中寻找解决问题相关的属性的功能，这些属性和功能就形成了概念世界中的类
  * 把抽象的实体用计算机语言进行描述，形成计算机世界中类的定义。即借助某种程序语言，把类构造成计算机能够识别和处理的数据结构
  * 将类实例化成计算机世界中的对象。对象是计算机世界中解决问题的最终工具。

## 类与对象

* 类与对象是面向对象的两个要素
* 类(Class)是对一类事物的描述，是抽象的、概念上的定义
* 对象是实际存在的该类事物的每个个体，因而也被称为实例(instance)
* “万事万物皆对象”

面向对象思想概述：

![1724591430829-a8fa74bd-e448-4883-9c68-c2780973346e.png](./img/TvMXBSJiS74TOLoG/1724591430829-a8fa74bd-e448-4883-9c68-c2780973346e-795210.png)

* 可以理解为：类= 抽象概念的人；对象= 实实在在的某个人呢
* 面向对象程序设计的重点是类的设计
* 类的设计，其实就是类的成员的设计

## 属性和方法

* 现实世界的生物体，大到鲸鱼，小到蚂蚁，都是由最基本的细胞构成的。同理，Java代码世界是由诸多个不同功能的类构成的
* 现实生物世界中的细胞又是由什么构成的？细胞核、细胞质、。。。那么，Java中用类class来描述事物也是如此。常见的类的成员有：
  * 属性：对应类中的成员变量
  * 行为：对应类中的成员方法
  * field = 属性= 成员变量，method = 成员方法= 函数
* 生活中描述事物无非就是描述事物的属性和行为。如：人有身高、体重等属性，有说话、打球等行为

## 类和对象的创建

```java
public class Person {

    String name;
    String sex;
    int age;

    public void eat(){
        System.out.println("人可以吃饭");
    }

    public void sleep(){
        System.out.println("人可以睡觉");
    }

    public void talk(String language){
        System.out.println("人可以说话，当前说的是：" + language);
    }
}
```

```java
public class Demo3 {

    public static void main(String[] args) {

        // 创建Person类的对象，也称为类的实例化，或实例化类
        Person p1 = new Person();

        // 调用对象的结构：属性和方法
        // 调用属性：对象.属性
        p1.name = "张三";
        p1.sex = "男";
        p1.age = 25;

        System.out.println("姓名：" + p1.name);
        System.out.println("性别：" + p1.sex);
        System.out.println("年龄：" + p1.age);

        // 调用方法：对象.方法
        p1.eat();
        p1.sleep();
        p1.talk("中文");
    }
}
```

类和对象的使用：

1. 创建类，设计类的成员

2. 创建类的对象

3. 通过“对象.属性”或“对象.方法”调用对象的结构

## 体会类的多个对象的关系

```java
public class Person {

    String name;
    String sex;
    int age;

    public void eat(){
        System.out.println("人可以吃饭");
    }

    public void sleep(){
        System.out.println("人可以睡觉");
    }

    public void talk(String language){
        System.out.println("人可以说话，当前说的是：" + language);
    }
}
```

```java
public class Demo3 {

    public static void main(String[] args) {

        // 创建Person类的对象，也称为类的实例化，或实例化类
        Person p1 = new Person();

        // 调用对象的结构：属性和方法
        // 调用属性：对象.属性
        p1.name = "张三";
        p1.sex = "男";
        p1.age = 25;

        System.out.println("姓名：" + p1.name);
        System.out.println("性别：" + p1.sex);
        System.out.println("年龄：" + p1.age);

        // 调用方法：对象.方法
        p1.eat();
        p1.sleep();
        p1.talk("中文");

        // 通过一个类可以创建多个对象，这多个对象都独立的拥有一套类的属性和行为
        Person p2 = new Person();
        p2.name = "李四";
        System.out.println("姓名：" + p2.name);
        System.out.println("性别：" + p2.sex);
        System.out.println("年龄：" + p2.age);

        p2.talk("英文");
    }
}
```

## 方法

* 方法：能够实现某些功能，我们将实现某些功能的代码写在一块形成一个方法
* 方法的声明格式：

```java
权限修饰符 返回值类型 方法名(形参列表){
    方法体
}
```

* 权限修饰符有：private、缺省、protected、public，我们用的最多的就是 private-私有、public-公共的
* 返回值类型：有返回值和无返回值
  * 如果方法有返回值，则必须在声明方法时，指定返回值类型。同时，方法中需要使用 return 关键字来返回指定类型的数据：`return 数据`
  * 如果方法没有返回值，则方法声明时，使用 void 来表示。通常没有返回值的方法中，就不需要写 return
* 我们定义方法时，该不该写返回值？
  * 看题目要求
  * 凭经验：具体问题具体分析
* 形参列表
  * 可以声明0个、1个或者多个形参
  * 格式：`数据类型1 形参1, 数据类型2 形参2, ...`
* 案例：

```java
public class Student {

    String name;
    String sex;
    int age;

    public void eat(){
        System.out.println("学生在吃饭");
    }

    public void sleep(int hours){
        System.out.println("学生每天睡" + hours + "小时");
    }

    public String getInfo(String nation){
        String info = "学生的国籍是：" + nation;
        return info;
    }
}
```

```java
public class Test {

    public static void main(String[] args) {

        Student s1 = new Student();
        s1.name = "张三";
        s1.sex = "男";
        s1.age = 20;

        System.out.println("学生的姓名是：" + s1.name);

        s1.eat();
        s1.sleep(8);
        String info = s1.getInfo("中国");
        System.out.println(info);
    }
}
```

## 练习

### 练习1

编写教师类，并通过测试类创建对象进行测试

| Teacher类 |
| --- |
| 属性：<br/>name:String<br/>age:int<br/>teachAge:int<br/>course:String |
| 方法：say()<br/>输出教师的个人信息 |

```java
public class Teacher {

    String name;
    int age;
    int teachAge;
    String course;

    public void say(){
        System.out.println("姓名：" + name + ", 年龄：" + age +
                ", 教龄：" + teachAge + ", 课程：" + course);
    }
}
```

```java
public class Test {

    public static void main(String[] args) {

        Teacher teacher = new Teacher();
        teacher.name = "宋江";
        teacher.age = 50;
        teacher.teachAge = 30;
        teacher.course = "英语";

        teacher.say();
    }
}
```

### 练习2

创建一个Person类，其定义如下

| Person |
| --- |
| name:String<br/>age:int<br/>sex:String |
| study():void<br/>showAge():void<br/>addAge(int i):int |

要求：

创建Person类的对象，设置该对象的name、age和sex属性，

调用study方法，输出字符串“studying”，调用showAge()方法显示age值，

调用addAge()方法给对象的age属性值增加2岁

```java
public class Person {

    String name;
    String sex;
    int age;

    public void study(){
        System.out.println("studying....");
    }

    public void showAge(){
        System.out.println("年龄：" + age);
    }

    public void addAge(int i){
        age = age + i;
    }
}
```

```java
public class Test {

    public static void main(String[] args) {

        Person person = new Person();
        person.name = "吕布";
        person.sex = "男";
        person.age = 25;

        person.study();
        person.showAge();
        person.addAge(2);
        person.showAge();
    }
}
```

## 封装

问题的引入：

当我们创建一个类的对象后，可以通过"对象.属性"的方式，对对象的属性进行赋值。

这里，赋值操作要受属性的数据类型和存储范围的制约。除此之外，没有其他制约条件。

但是，在实际问题中，我们往往需要给属性赋值加入额外的限制条件。这个条件就不能在属性声明时体现，我们只能通过方法进行限制条件的添加。比如：setAge(int a)

同时，我们需要避免用户再使用"对象.属性"的方式对属性进行赋值，则需要将属性声明为私有的(private)

此时，针对与属性就体现了封装性。

**封装性的体现：**

我们将类的属性xxx私有化(private)，同时，提供公共的(public)方法来获取(getXxx)和设置(setXxx)属性。

**案例：**

```java
public class Goods {

    private String name;
    private double price;

    public void setName(String n){
        name = n;
    }

    public String getName(){
        return name;
    }

    public void setPrice(double p){
        price = p;
    }

    public double getPrice(){
        return price;
    }
}
```

```java
public class Test {

    public static void main(String[] args) {

        Goods goods = new Goods();
        goods.setName("方便面");
        goods.setPrice(2.5);

        System.out.println(goods.getName());
        System.out.println(goods.getPrice());
    }
}
```

## 构造器

构造器，也称之为构造方法。（constructor）

构造器的作用：创建对象

说明：

1. 如果没有显式的定义了类的构造器的话，则系统默认提供一个空参的构造器

2. 定义构造器的格式：权限修饰符 类名(形参列表){}

**案例1：**

```java
public class Goods {

    private String name;
    private double price;

    public Goods(){
        System.out.println("构造器被执行...");
    }

    public void setName(String n){
        name = n;
    }

    public String getName(){
        return name;
    }

    public void setPrice(double p){
        price = p;
    }

    public double getPrice(){
        return price;
    }
}
```

```java
public class Test {

    public static void main(String[] args) {

        // 创建类的对象: new + 构造器
        Goods goods = new Goods();
        goods.setName("方便面");
        goods.setPrice(2.5);

        System.out.println(goods.getName());
        System.out.println(goods.getPrice());
    }
}
```

**案例2：通过构造器给属性赋值**

```java
public class Animal {

    private String name;
    private int age;

    public Animal(){

    }

    public Animal(String n, int a){
        name = n;
        age = a;
    }

    public void setName(String n){
        name = n;
    }

    public String getName(){
        return name;
    }

    public void setAge(int a){
        age = a;
    }

    public int getAge(){
        return age;
    }
    
    public void say(){
        System.out.println("名称：" + name + ", 年龄：" + age);
    }
}
```

```java
public class Test {

    public static void main(String[] args) {

        Animal animal = new Animal("大黄", 5);
        animal.say();
    }
}
```

## 封装+构造器快捷写法

```java
public class Emp {
    
    private String name;
    private String sex;
    private int age;

    // alt + insert ---> Constructor
    public Emp() {
        
    }

    // alt + insert ---> Constructor
    public Emp(String name, String sex, int age) {
        this.name = name;
        this.sex = sex;
        this.age = age;
    }

    // alt + insert ---> Getter and Setter
    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getSex() {
        return sex;
    }

    public void setSex(String sex) {
        this.sex = sex;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    // alt + insert ---> toString
    @Override
    public String toString() {
        return "Emp{" +
                "name='" + name + '\'' +
                ", sex='" + sex + '\'' +
                ", age=" + age +
                '}';
    }
}
```

```java
public class Test {

    public static void main(String[] args) {

        Emp emp = new Emp("武松", "男", 25);
        System.out.println(emp.toString());
    }
}
```

## 继承

### 理解

假如：

Student 类中有姓名、年龄属性，吃饭、睡觉的方法

Teacher类中有姓名、年龄属性，吃饭、睡觉的方法

Customer类中有姓名、年龄属性，吃饭、睡觉的方法

那是不是要写三份这些共同的属性和方法呢？

其实是不需要的，可以通过继承来简化！

![1724681114908-16fa5629-aba9-4b0c-ba76-58e60487063e.png](./img/TvMXBSJiS74TOLoG/1724681114908-16fa5629-aba9-4b0c-ba76-58e60487063e-955586.png)

可以发现继承的好处：

1. 减少了代码的冗余，提高了代码的复用性

2. 便于功能的扩展

### 使用

* 继承的格式：class A extends B{ }
  * A：子类、派生类、subclass
  * B：父类、超类、基类、superclass
* 体现：一旦子类A继承父类B以后，子类A中就获取了父类B中声明的结构：属性、方法。
* 特别地，父类中声明为private的属性或方法，子类继承父类以后，仍然认为获取了父类中私有的结构，只是因为封装性的影响，使得子类不能直接调用父类的结构而已
* 子类继承父类以后，还可以声明自己特有的属性或方法，实现功能的扩展。

```java
public class People {

    private String name;
    private int age;

    public People() {
    }

    public People(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    @Override
    public String toString() {
        return "People{" +
                "name='" + name + '\'' +
                ", age=" + age +
                '}';
    }

    public void eat(){
        System.out.println("吃东西");
    }

    public void sleep(){
        System.out.println("睡觉");
    }
}
```

```java
public class Student extends People{
    
    private int score;

    public Student() {
    }

    public Student(String name, int age, int score) {
        super(name, age);
        this.score = score;
    }

    public int getScore() {
        return score;
    }

    public void setScore(int score) {
        this.score = score;
    }

    @Override
    public String toString() {
        return "Student{" +
                "score=" + score +
                '}';
    }
}
```

```java
public class Teacher extends People {
    
    private int teachAge;

    public Teacher() {
    }

    public Teacher(String name, int age, int teachAge) {
        super(name, age);
        this.teachAge = teachAge;
    }

    public int getTeachAge() {
        return teachAge;
    }

    public void setTeachAge(int teachAge) {
        this.teachAge = teachAge;
    }

    @Override
    public String toString() {
        return "Teacher{" +
                "teachAge=" + teachAge +
                '}';
    }
}
```

```java
public class Test {

    public static void main(String[] args) {
        Student student = new Student("小明", 18, 98);
        student.eat();
        student.sleep();
        System.out.println(student.getName());

        Teacher teacher = new Teacher("张老师", 45, 20);
        teacher.eat();
        teacher.sleep();
        System.out.println(teacher.getName());
    }
}
```

### 继承性的再说明

Java中继承性的规定：

1. 一个类可以被多个类继承

2. Java中类的单继承性：一个类只能有一个父类

## 方法的重写

定义：在子类中可以根据需要对从父类中继承来的方法进行改造，也称为方法的重置、覆盖。在程序执行时，子类的方法将覆盖父类的方法。

```java
public class People {

    private String name;
    private int age;

    public People() {
    }

    public People(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    @Override
    public String toString() {
        return "People{" +
                "name='" + name + '\'' +
                ", age=" + age +
                '}';
    }

    public void eat(){
        System.out.println("吃东西");
    }

    public void sleep(){
        System.out.println("睡觉");
    }
}
```

```java
public class Test {

    public static void main(String[] args) {
        Student student = new Student("小明", 18, 98);
        student.eat(); // 调用的是子类重写后的方法，也就是子类有就用子类的，子类没有就使用父类的
        student.sleep();
        System.out.println(student.getName());
    }
}
```

## 多态

### 多态的理解

多态的意思是：一种物质有多种形态。

多态的关键：有继承的关系。

### 多态的使用

```java
父类 对象名 = new 子类对象();
```

## 接口

### 概述

* 接口就是规范，定义的是一组规则，体现了现实世界中“如果你是/要…则必须能…”的思想。继承是一个“是不是”的关系，而接口实现则是“能不能”的关系。
* 接口的本质是契约，标准，规范，就像我们的法律一样，制定好后大家都要遵守。
* 举例：

![1724773114655-d8f8fccd-9bf3-48b2-ac07-828c09238280.png](./img/TvMXBSJiS74TOLoG/1724773114655-d8f8fccd-9bf3-48b2-ac07-828c09238280-159838.png)

### 接口的使用

```java
接口 对象名 = new 实现类();
List list = new ArrayList();
```

# List 接口

## List 接口介绍

List接口：存储有序的、可重复的数据，底层就是数组！

## List 接口常用实现类

ArrayList: 作为List接口的主要实现类；线程不安全的，效率高；底层使用的是Object\[]elementData数组存储

常用方法：

添加、修改、删除、获取指定数据

```java
import java.util.ArrayList;
import java.util.Date;
import java.util.List;

public class Demo3 {

    public static void main(String[] args) {

        // List 集合，可以存放很多数据，而且是有顺序的。它的底层是数组
        // List 是一个接口，它的主要的实现类 ArrayList

        // 创建List集合对象   泛型
        List<String> list = new ArrayList();

        // 使用add方法往集合中添加数据
        list.add("张无忌");
        list.add("赵敏");
        list.add("周芷若");
        list.add("蛛儿");
//        list.add(456);
//        list.add(new Date());

        // 使用size方法可以获取集合的长度
        System.out.println(list.size());

        // 获取集合中指定位置的元素
        System.out.println(list.get(2));

        // 修改集合中指定位置的元素
        list.set(3, "金毛狮王");

        System.out.println(list.get(3));

        // 删除集合中指定位置的元素
        list.remove(2);

        System.out.println(list.size());

        // 利用for循环遍历集合
        for(int i = 0; i < list.size(); i++){
            System.out.println(list.get(i));
        }
    }
}
```

```java
public class Fruit {

    private String name;
    private double price;

    public Fruit() {
    }

    public Fruit(String name, double price) {
        this.name = name;
        this.price = price;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public double getPrice() {
        return price;
    }

    public void setPrice(double price) {
        this.price = price;
    }

    @Override
    public String toString() {
        return "Fruit{" +
                "name='" + name + '\'' +
                ", price=" + price +
                '}';
    }
}
```

```java
import java.util.ArrayList;
import java.util.List;

public class Demo4 {

    public static void main(String[] args) {

        // 创建一个List集合，并且指定泛型是 Fruit
        List<Fruit> list = new ArrayList<>();

        // 创建3个水果对象
        Fruit fruit1 = new Fruit("苹果", 4.5);
        Fruit fruit2 = new Fruit("香蕉", 3.2);
        Fruit fruit3 = new Fruit("橘子", 2.8);

        // 将水果对象添加到集合中
        list.add(fruit1);
        list.add(fruit2);
        list.add(fruit3);

        // 修改集合中索引是2的元素的信息，改为 草莓 5.2
        Fruit fruit = new Fruit("草莓", 5.2);
        list.set(2, fruit);

        // 删除集合中索引是1的元素
        list.remove(1);

        // 遍历集合中的信息
        for(int i = 0; i < list.size(); i++){
            System.out.println(list.get(i));
        }
    }
}
```

集合！

List、Set、Map集合！

List集合。

# 商品管理系统案例

## Scanner

```java
import java.util.Scanner;

public class Demo6 {

    public static void main(String[] args) {

        // 创建Scanner对象，可以读取控制台的内容
        Scanner scanner = new Scanner(System.in);

        System.out.println("请输入你的名字：");
        String name = scanner.next(); // next()读取用户输入的字符串

        System.out.println("请输入你的年龄：");
        int age = scanner.nextInt(); // nextInt()读取用户输入的整数

        System.out.println("请输入你的体重：");
        double weight = scanner.nextDouble(); // nextDouble()读取用户输入的小数

        System.out.println("姓名：" + name + ", 年龄：" + age + ", 体重：" + weight);
    }
}
```

## 功能介绍

我们在IDEA控制台实现对商品的增、删、该、查的功能。

使用到的知识：

* 类的定义
* 对象的创建
* List集合存储对象数据
* Scanner读取控制台的信息
* 选择结构-if...else
* 循环结构：while循环、for循环
* continue：结束本次循环进入下一次循环
* return：可以结束当前运行的方法

## 项目准备&退出功能

```java
import java.util.Scanner;

public class Demo7 {

    // 商品管理系统
    public static void main(String[] args) {

        System.out.println("=================欢迎使用内财大商品管理系统================");

        // 创建Scanner对象，用来读取用户在控制台输入的内容。
        Scanner scanner = new Scanner(System.in);

        while(true){

            System.out.println("请输入你的操作：1-商品列表展示  2-商品添加  3-商品修改  4-商品删除 5-退出");
            int i = scanner.nextInt(); // 读取到用户输入的数字

            if(i == 1){
                System.out.println("商品列表展示....");
            }else if(i == 2){
                System.out.println("商品添加....");
            }else if(i == 3){
                System.out.println("商品修改....");
            }else if(i == 4){
                System.out.println("商品删除....");
            }else if(i == 5){
                System.out.println("bye bye!");
                return; // 在方法中使用return，表示该方法立马结束了！
            }else{
                System.out.println("别瞎胡输入数字！看清楚！");
            }
        }
    }
}
```

## 实现商品列表展示功能

### 编写商品的实体类

```java
import java.util.Date;

// 商品的实体类
public class Goods {
    
    private String name;
    private double price;
    private Date produceDate; // 生产日期，注意是java.util中的Date
    private String address;

    public Goods() {
    }

    public Goods(String name, double price, Date produceDate, String address) {
        this.name = name;
        this.price = price;
        this.produceDate = produceDate;
        this.address = address;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public double getPrice() {
        return price;
    }

    public void setPrice(double price) {
        this.price = price;
    }

    public Date getProduceDate() {
        return produceDate;
    }

    public void setProduceDate(Date produceDate) {
        this.produceDate = produceDate;
    }

    public String getAddress() {
        return address;
    }

    public void setAddress(String address) {
        this.address = address;
    }

    @Override
    public String toString() {
        return "Goods{" +
                "name='" + name + '\'' +
                ", price=" + price +
                ", produceDate=" + produceDate +
                ", address='" + address + '\'' +
                '}';
    }
}
```

```java
import java.text.SimpleDateFormat;
import java.util.ArrayList;
import java.util.Date;
import java.util.List;
import java.util.Scanner;

public class Demo7 {

    // 商品管理系统
    public static void main(String[] args) {

        System.out.println("======================欢迎使用内财大商品管理系统======================");

        // 创建Scanner对象，用来读取用户在控制台输入的内容。
        Scanner scanner = new Scanner(System.in);

        // 定义一个集合对象，存放商品信息
        List<Goods> list = new ArrayList<>();

        Goods goods1 = new Goods("面包", 8.5, new Date(), "内蒙古呼市");
        Goods goods2 = new Goods("可乐", 3.5, new Date(), "内蒙古包头");
        Goods goods3 = new Goods("马奶酒", 128, new Date(), "内蒙古呼伦贝尔");

        list.add(goods1);
        list.add(goods2);
        list.add(goods3);

        while(true){

            System.out.println("请输入你的操作：1-商品列表展示  2-商品添加  3-商品修改  4-商品删除 5-退出");
            int i = scanner.nextInt(); // 读取到用户输入的数字

            if(i == 1){ // 商品列表展示
                System.out.println("商品名称\t\t商品价格\t\t生产日期\t\t生产地址");
                for(int j = 0; j < list.size(); j++){
                    Goods goods = list.get(j);

                    // 创建格式化日期的对象
                    SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
                    // 格式化日期
                    String str = sdf.format(goods.getProduceDate()); // 2024-05-05

                    System.out.println(goods.getName() + "\t\t" + goods.getPrice() + "\t\t" + str + "\t\t" + goods.getAddress());
                }

            }else if(i == 2){
                System.out.println("商品添加....");
            }else if(i == 3){
                System.out.println("商品修改....");
            }else if(i == 4){
                System.out.println("商品删除....");
            }else if(i == 5){
                System.out.println("bye bye!");
                return; // 在方法中使用return，表示该方法立马结束了！
            }else{
                System.out.println("别瞎胡输入数字！看清楚！");
            }
        }
    }
}
```

## 实现添加商品功能

```java
import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.ArrayList;
import java.util.Date;
import java.util.List;
import java.util.Scanner;

public class Demo7 {

    // 商品管理系统
    public static void main(String[] args) throws ParseException {

        System.out.println("======================欢迎使用内财大商品管理系统======================");

        // 创建Scanner对象，用来读取用户在控制台输入的内容。
        Scanner scanner = new Scanner(System.in);

        // 定义一个集合对象，存放商品信息
        List<Goods> list = new ArrayList<>();

        Goods goods1 = new Goods("面包", 8.5, new Date(), "内蒙古呼市");
        Goods goods2 = new Goods("可乐", 3.5, new Date(), "内蒙古包头");
        Goods goods3 = new Goods("马奶酒", 128, new Date(), "内蒙古呼伦贝尔");

        list.add(goods1);
        list.add(goods2);
        list.add(goods3);

        while(true){

            System.out.println("请输入你的操作：1-商品列表展示  2-商品添加  3-商品修改  4-商品删除 5-退出");
            int i = scanner.nextInt(); // 读取到用户输入的数字

            if(i == 1){ // 商品列表展示
                System.out.println("商品名称\t\t商品价格\t\t生产日期\t\t生产地址");
                for(int j = 0; j < list.size(); j++){
                    Goods goods = list.get(j);

                    // 创建格式化日期的对象
                    SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
                    // 格式化日期
                    String str = sdf.format(goods.getProduceDate()); // 2024-05-05

                    System.out.println(goods.getName() + "\t\t" + goods.getPrice() + "\t\t" + str + "\t\t" + goods.getAddress());
                }

            }else if(i == 2){ // 商品添加

                System.out.print("商品名称：");
                String name = scanner.next(); // 读取到商品名称
                System.out.print("商品价格：");
                double price = scanner.nextDouble(); // 读取商品价格
                System.out.println("生产日期(如:2025-05-08)：");
                String str = scanner.next(); // "2025-05-05"

                // 将字符串的日期转为Date类型的日期
                SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
                Date produceDate = sdf.parse(str);

                System.out.print("生产地址：");
                String address = scanner.next();

                // 将上面读取到的商品的各个信息封装到商品对象中
                Goods goods = new Goods(name, price, produceDate, address);

                // 将goods对象放入list集合
                list.add(goods);

                System.out.println("亲，添加成功！");
            }else if(i == 3){
                System.out.println("商品修改....");
            }else if(i == 4){
                System.out.println("商品删除....");
            }else if(i == 5){
                System.out.println("bye bye!");
                return; // 在方法中使用return，表示该方法立马结束了！
            }else{
                System.out.println("别瞎胡输入数字！看清楚！");
            }
        }
    }
}
```

## 实现修改商品功能

```java
import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.ArrayList;
import java.util.Date;
import java.util.List;
import java.util.Scanner;

public class Demo7 {

    // 商品管理系统
    public static void main(String[] args) throws ParseException {

        System.out.println("======================欢迎使用内财大商品管理系统======================");

        // 创建Scanner对象，用来读取用户在控制台输入的内容。
        Scanner scanner = new Scanner(System.in);

        // 定义一个集合对象，存放商品信息
        List<Goods> list = new ArrayList<>();

        Goods goods1 = new Goods("面包", 8.5, new Date(), "内蒙古呼市");
        Goods goods2 = new Goods("可乐", 3.5, new Date(), "内蒙古包头");
        Goods goods3 = new Goods("马奶酒", 128, new Date(), "内蒙古呼伦贝尔");

        list.add(goods1);
        list.add(goods2);
        list.add(goods3);

        while(true){

            System.out.println("请输入你的操作：1-商品列表展示  2-商品添加  3-商品修改  4-商品删除 5-退出");
            int i = scanner.nextInt(); // 读取到用户输入的数字

            if(i == 1){ // 商品列表展示
                System.out.println("序号\t\t商品名称\t\t商品价格\t\t生产日期\t\t生产地址");
                for(int j = 0; j < list.size(); j++){
                    Goods goods = list.get(j);

                    // 创建格式化日期的对象
                    SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
                    // 格式化日期
                    String str = sdf.format(goods.getProduceDate()); // 2024-05-05

                    System.out.println(j+1 + "\t\t" + goods.getName() + "\t\t" + goods.getPrice() + "\t\t" + str + "\t\t" + goods.getAddress());
                }

            }else if(i == 2){ // 商品添加

                System.out.print("商品名称：");
                String name = scanner.next(); // 读取到商品名称
                System.out.print("商品价格：");
                double price = scanner.nextDouble(); // 读取商品价格
                System.out.print("生产日期(如:2025-05-08)：");
                String str = scanner.next(); // "2025-05-05"

                // 将字符串的日期转为Date类型的日期
                SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
                Date produceDate = sdf.parse(str);

                System.out.print("生产地址：");
                String address = scanner.next();

                // 将上面读取到的商品的各个信息封装到商品对象中
                Goods goods = new Goods(name, price, produceDate, address);

                // 将goods对象放入list集合
                list.add(goods);

                System.out.println("亲，添加成功！");
            }else if(i == 3){ // 商品修改

                System.out.print("请输入修改商品的序号：");
                int id = scanner.nextInt();

                System.out.print("商品名称：");
                String name = scanner.next(); // 读取到商品名称
                System.out.print("商品价格：");
                double price = scanner.nextDouble(); // 读取商品价格
                System.out.print("生产日期(如:2025-05-08)：");
                String str = scanner.next(); // "2025-05-05"

                // 将字符串的日期转为Date类型的日期
                SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
                Date produceDate = sdf.parse(str);

                System.out.print("生产地址：");
                String address = scanner.next();

                // 将上面读取到的商品的各个信息封装到商品对象中
                Goods goods = new Goods(name, price, produceDate, address);

                // 修改list集合中指定位置的元素
                list.set(id-1, goods);

                System.out.println("亲，修改成功~");

            }else if(i == 4){
                System.out.println("商品删除....");
            }else if(i == 5){
                System.out.println("bye bye!");
                return; // 在方法中使用return，表示该方法立马结束了！
            }else{
                System.out.println("别瞎胡输入数字！看清楚！");
            }
        }
    }
}
```

## 实现删除商品功能

```java
import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.ArrayList;
import java.util.Date;
import java.util.List;
import java.util.Scanner;

public class Demo7 {

    // 商品管理系统
    public static void main(String[] args) throws ParseException {

        System.out.println("======================欢迎使用内财大商品管理系统======================");

        // 创建Scanner对象，用来读取用户在控制台输入的内容。
        Scanner scanner = new Scanner(System.in);

        // 定义一个集合对象，存放商品信息
        List<Goods> list = new ArrayList<>();

        Goods goods1 = new Goods("面包", 8.5, new Date(), "内蒙古呼市");
        Goods goods2 = new Goods("可乐", 3.5, new Date(), "内蒙古包头");
        Goods goods3 = new Goods("马奶酒", 128, new Date(), "内蒙古呼伦贝尔");

        list.add(goods1);
        list.add(goods2);
        list.add(goods3);

        while(true){

            System.out.println("请输入你的操作：1-商品列表展示  2-商品添加  3-商品修改  4-商品删除 5-退出");
            int i = scanner.nextInt(); // 读取到用户输入的数字

            if(i == 1){ // 商品列表展示
                System.out.println("序号\t\t商品名称\t\t商品价格\t\t生产日期\t\t生产地址");
                for(int j = 0; j < list.size(); j++){
                    Goods goods = list.get(j);

                    // 创建格式化日期的对象
                    SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
                    // 格式化日期
                    String str = sdf.format(goods.getProduceDate()); // 2024-05-05

                    System.out.println(j+1 + "\t\t" + goods.getName() + "\t\t" + goods.getPrice() + "\t\t" + str + "\t\t" + goods.getAddress());
                }

            }else if(i == 2){ // 商品添加

                System.out.print("商品名称：");
                String name = scanner.next(); // 读取到商品名称
                System.out.print("商品价格：");
                double price = scanner.nextDouble(); // 读取商品价格
                System.out.print("生产日期(如:2025-05-08)：");
                String str = scanner.next(); // "2025-05-05"

                // 将字符串的日期转为Date类型的日期
                SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
                Date produceDate = sdf.parse(str);

                System.out.print("生产地址：");
                String address = scanner.next();

                // 将上面读取到的商品的各个信息封装到商品对象中
                Goods goods = new Goods(name, price, produceDate, address);

                // 将goods对象放入list集合
                list.add(goods);

                System.out.println("亲，添加成功！");
            }else if(i == 3){ // 商品修改

                System.out.print("请输入修改商品的序号：");
                int id = scanner.nextInt();

                System.out.print("商品名称：");
                String name = scanner.next(); // 读取到商品名称
                System.out.print("商品价格：");
                double price = scanner.nextDouble(); // 读取商品价格
                System.out.print("生产日期(如:2025-05-08)：");
                String str = scanner.next(); // "2025-05-05"

                // 将字符串的日期转为Date类型的日期
                SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
                Date produceDate = sdf.parse(str);

                System.out.print("生产地址：");
                String address = scanner.next();

                // 将上面读取到的商品的各个信息封装到商品对象中
                Goods goods = new Goods(name, price, produceDate, address);

                // 修改list集合中指定位置的元素
                list.set(id-1, goods);

                System.out.println("亲，修改成功~");

            }else if(i == 4){ // 商品删除

                System.out.print("请输入要删除的商品的序号：");

                int j = scanner.nextInt();

                list.remove(j - 1);

                System.out.println("亲，删除成功~");
            }else if(i == 5){
                System.out.println("bye bye!");
                return; // 在方法中使用return，表示该方法立马结束了！
            }else{
                System.out.println("别瞎胡输入数字！看清楚！");
            }
        }
    }
}
```

# MySQL 数据库

## 数据库介绍

如今数据库已经无处不在了。一个网站需要有数据库来存储数据；一个学校需要用数据库来存储学生和教师的信息；一个公司需要用数据库来存储员工的信息和公司的资料。 要学习数据库，必须先要了解数据库是如何存储数据的。数据存储分为3个阶段即：

人工管理阶段：

* 这个阶段，数据都是依靠人工进行整理和保存的。（老人们把手机号记在电话本上）
* 缺点：使用这种方式来管理数据很不方便。

文件系统阶段：

* 这个阶段，随着科技的发展数据可以存储在计算机的磁盘上，例如咱们前期课程中将数据存储到.txt文件中以及.xml文件
* 优点：相对于人工管理阶段而言，文件系统使得数据管理变得简单
* 缺点：这些文件中的数据没有进行结构化处理，査询起来还不是很方便，而且频繁的IO操效率低。

数据库系统阶段：

* 数据库是指长期存储在计算机内、有组织的和可共享的数据集合，简而言之，数据库 就是一个存储数据的仓库。
* 优点：表是数据库存储数据的基本单位，一张表由多个字段组成，所以查询起来比较方便

数据库产品有很多：

MySQL、Oracle、SQLserver、DB2等等。

## 安装和配置 MySQL

按照下图去安装MySQL：

双击安装包：

![1724891189758-345865fc-d9fa-440b-bf2e-62014a6df3dd.png](./img/TvMXBSJiS74TOLoG/1724891189758-345865fc-d9fa-440b-bf2e-62014a6df3dd-880989.png)

![1724891218351-179a297e-47ca-43ed-ac9a-4118296f35d4.png](./img/TvMXBSJiS74TOLoG/1724891218351-179a297e-47ca-43ed-ac9a-4118296f35d4-799111.png)

![1724891256893-04691c79-1b0e-461c-b8a3-e1b1f479a486.png](./img/TvMXBSJiS74TOLoG/1724891256893-04691c79-1b0e-461c-b8a3-e1b1f479a486-774767.png)

![1724891300891-3b5f2f56-0cba-4838-9244-7bb05f354090.png](./img/TvMXBSJiS74TOLoG/1724891300891-3b5f2f56-0cba-4838-9244-7bb05f354090-420958.png)

![1724891337253-f0c3ab17-874e-4aa0-813e-781c2c24e61a.png](./img/TvMXBSJiS74TOLoG/1724891337253-f0c3ab17-874e-4aa0-813e-781c2c24e61a-397631.png)

![1724891361967-30efb6cd-0b9d-4db8-9e2f-b4c500eafed4.png](./img/TvMXBSJiS74TOLoG/1724891361967-30efb6cd-0b9d-4db8-9e2f-b4c500eafed4-778117.png)

![1724891385251-fb9526b7-b8c1-408a-997b-257de509d429.png](./img/TvMXBSJiS74TOLoG/1724891385251-fb9526b7-b8c1-408a-997b-257de509d429-553356.png)

![1724891408315-6c8f032e-73d7-416b-9618-50d846b9907d.png](./img/TvMXBSJiS74TOLoG/1724891408315-6c8f032e-73d7-416b-9618-50d846b9907d-387156.png)

![1724891527023-80ebc4b6-9aa0-45f3-9da5-7e902cc02e04.png](./img/TvMXBSJiS74TOLoG/1724891527023-80ebc4b6-9aa0-45f3-9da5-7e902cc02e04-940448.png)

![1724891543608-77f5f10e-5ca1-47cb-be43-860c3f372ac6.png](./img/TvMXBSJiS74TOLoG/1724891543608-77f5f10e-5ca1-47cb-be43-860c3f372ac6-477432.png)

![1724891558690-ecdb3246-631f-43f4-a5ab-50188d42fc97.png](./img/TvMXBSJiS74TOLoG/1724891558690-ecdb3246-631f-43f4-a5ab-50188d42fc97-053658.png)

![1724891742524-03bba1fa-02b6-499b-8486-adb3054570a2.png](./img/TvMXBSJiS74TOLoG/1724891742524-03bba1fa-02b6-499b-8486-adb3054570a2-428765.png)

![1724891757616-e8fca05d-4824-488b-a597-8cd230e16f8b.png](./img/TvMXBSJiS74TOLoG/1724891757616-e8fca05d-4824-488b-a597-8cd230e16f8b-366531.png)

![1724891772165-0afe82dd-b634-4c95-a8cd-7855efef7ed1.png](./img/TvMXBSJiS74TOLoG/1724891772165-0afe82dd-b634-4c95-a8cd-7855efef7ed1-043109.png)

## Navicat 介绍及安装

* Navicat是一款功能非常强大的MySQL数据库管理和开发工具，其可以支持MySQL 3.21及以上的版本。
* 这款工具支持触发器、存储过程、函数、事务处理、视图和用 户管理等功能。
* Navicat的图形化界面非常的友善，用户使用和管理都很方便。
* 这款工具支持中文，并且有免费版本提供。

Navicat的安装：

1. 将我们发送的 Navicat.zip 压缩包解压
2. 双击navicat.exe就可以运行了

:::info
使用Navicat连接MySQL数据库

:::

![1724892284102-21c915b6-4d61-40ad-a16c-d5aff903a50f.png](./img/TvMXBSJiS74TOLoG/1724892284102-21c915b6-4d61-40ad-a16c-d5aff903a50f-634429.png)

![1724892383202-b0707151-f883-45c7-ba33-002f4be0d5af.png](./img/TvMXBSJiS74TOLoG/1724892383202-b0707151-f883-45c7-ba33-002f4be0d5af-837216.png)

![1724892400711-c2c15bbc-fd32-4fba-b5c2-d814d844ffcf.png](./img/TvMXBSJiS74TOLoG/1724892400711-c2c15bbc-fd32-4fba-b5c2-d814d844ffcf-492288.png)

![1724892428925-875a099d-efd9-4bcb-9a03-902d574405ff.png](./img/TvMXBSJiS74TOLoG/1724892428925-875a099d-efd9-4bcb-9a03-902d574405ff-078049.png)

## 创建数据库

使用SQL语句的方式：`create database 数据库名称 default character set utf8; `

使用Navicat客户端的方式：

![1724895263692-e60eefee-a50a-429f-a0bc-1d30a63d2efb.png](./img/TvMXBSJiS74TOLoG/1724895263692-e60eefee-a50a-429f-a0bc-1d30a63d2efb-109919.png)

![1724895316477-31840d9e-3278-4e4b-919d-4ddfad55bbab.png](./img/TvMXBSJiS74TOLoG/1724895316477-31840d9e-3278-4e4b-919d-4ddfad55bbab-629434.png)

![1724895342457-09c97e8b-adc9-4e27-9776-20889f3bde7f.png](./img/TvMXBSJiS74TOLoG/1724895342457-09c97e8b-adc9-4e27-9776-20889f3bde7f-950397.png)

## 数据类型介绍

* 整数类型：我们常用的就是 int
* 浮点数类型：我们常用的就是 double
* 日期类型：我们使用 date
* 字符串类型：使用的是 varchar

## 创建表

使用sql语句的方式：

```sql
create table 表名(
  字段名1 数据类型 【约束】,
  字段名2 数据类型 【约束】,
  字段名1 数据类型 【约束】，
  ...
);
-- 一般我们在创建表的时候会直接给id设置主键并自增

-- 案例
-- 创建表
create table user(
	id int primary key auto_increment,
	name varchar(30),
	sex varchar(10),
	age int,
	birthday date
);
```

使用Navicat的方式：

![1724896091592-0bbe5b29-20f8-4028-82aa-4138e610406e.png](./img/TvMXBSJiS74TOLoG/1724896091592-0bbe5b29-20f8-4028-82aa-4138e610406e-269245.png)

![1724896247648-5b11ecd8-cc08-4327-93f4-b8f2f8c84d3e.png](./img/TvMXBSJiS74TOLoG/1724896247648-5b11ecd8-cc08-4327-93f4-b8f2f8c84d3e-366184.png)

然后输入 Ctrl + s，保存

![1724896278875-5c18bfc6-4d0a-4af5-8921-046a873e22d3.png](./img/TvMXBSJiS74TOLoG/1724896278875-5c18bfc6-4d0a-4af5-8921-046a873e22d3-248539.png)

## 插入数据

:::info <font style="color:rgb(51, 51, 51);">为表的所有字段插入数据</font>

:::

```sql
INSERT INTO 表名 VALUES（值1,值2,值n）;
```

<font style="color:rgb(51, 51, 51);">其中，"表名”参数指定记录插入到哪个表中；'‘值n”参数表示要插入的数据。“值1” 到“值n”分别对应着表中的每个字段。表中定义了几个字段，INSERT语句中就应该对应有几个值。</font>**<font style="color:rgb(51, 51, 51);">插入的顺序与表中字段的顺序相同</font>**<font style="color:rgb(51, 51, 51);">。而且，取值的数据类型要与表中对应字段的数据类型一致。</font>

:::info <font style="color:rgb(51, 51, 51);">为表的指定字段插入数据</font>

:::

```sql
INSERT INTO 表名(字段1,字段2，…，字段m) VALUES(值1,值2,...,值m);
```

<font style="color:rgb(51, 51, 51);">其中，“字段m”参数表示表中的字段名称，此处指定表的部分字段的名称；“值m” 参数表示指定字段的值，每个值与相应的字段对应。</font>

## 修改数据

<font style="color:rgb(51, 51, 51);">更新数据是更新表中已经存在的记录。通过这种方式可以改变表中已经存在的数据。 例如，学生表中某个学生的家庭住址改变了，这就需要在学生表中修改该同学的家庭地址。 在MySQL中，通过UPDATE语句来更新数据。</font>

<font style="color:rgb(51, 51, 51);">在MySQL中，UPDATE语句的基本语法形式如下：</font>

```sql
UPDATE 表名
SET 字段1=值1,字段2=值2,
...
字段n=值n
[WHERE条件表达式];
```

<font style="color:rgb(51, 51, 51);">其中，“字段n”参数表示需要更新的字段的名称；“值n”参数表示为字段更新的新数据；“条件表达式”参数指定更新满足条件的记录。</font>

<font style="color:rgb(51, 51, 51);">注意：更新全部字段就是为当前表中所有字段设置取值，但是一般是不更新主键字段的。</font>

:::info <font style="color:rgb(51, 51, 51);">不带条件更新数据操作【了解】</font>

:::

<font style="color:rgb(51, 51, 51);">大家看到我们上面完成的更新操作，设置了条件 id=1001，如果没有设置任何条件，那么会将数据库中所有数据都会更新。一般很少这么操作，所以作为了解知识，大家操作一次看一下效果即可。</font>

## 删除数据

<font style="color:rgb(51, 51, 51);">删除数据是删除表中已经存在的记录。通过这种方式可以删除表中不再使用的记录。 例如，学生表中某个学生退学了，这就需要从学生表中删除该同学的信息。</font>

<font style="color:rgb(51, 51, 51);">MySQL中，DELETE语句的基本语法形式如下：</font>

```sql
DELETE FROM 表名［WHERE条件表达式］;
```

<font style="color:rgb(51, 51, 51);">其中，“表名”参数指明从哪个表中删除数据；“WHERE条件表达式”指定删除表中的哪些数据。如果满足where条件的数据有多条，那么执行DELETE语句可以同时删除多条记录。如果没有该条件表达式，数据库系统就会删除表中的所有数据。</font>

## 基本查询

<font style="color:rgb(51, 51, 51);">查询数据是数据库操作中最常用的操作。通过对数据库的查询，用户可以从数据库中获取需要的数据。数据库中可能包含着无数的表，表中可能包含着无数的记录。因此，要获得所需的数据并非易事。MySQL中可以使用SELECT语句来查询数据。根据查询的条件不同，数据库系统会找到不同的数据。通过SELECT语句可以很方便地获取所需的信息。</font>

<font style="color:rgb(51, 51, 51);">在以后的实际项目开发中，查询操作几乎无处不在。</font>

### <font style="color:rgb(51, 51, 51);">SQL基本查询语法</font>

<font style="color:rgb(51, 51, 51);">MySQL中，SELECT的基本语法形式如下：</font>

```sql
SELECT 字段列表

FROM 表名

[WHERE 条件表达式1]

[GROUP BY 字段1 [HAVING 条件表达式2]]

[ORDER BY 字段2 [ASC|DESC]]
```

* “字段列表”参数表示需要査询的字段名；
* “表名”参数表示从此 处指定的表中查询数据，表可以有多个；
* “条件表达式1”参数指定查询条件；
* “字段1”参数指按该字段中的数据进行分组；
* “条件表达式2”参数表示满足该表达式的数据才能输出；
* “字段2”参数指按该字段中的数据进行排序，排序方式由ASC,和DESC两个参数指出ASC参数表示按升序的顺序进行排序，这是默认参数；DESC参数表示按降序的顺序进行排序。

**案例：**

```sql
-- 创建表
CREATE TABLE student (
  id INT primary key auto_increment,
  NAME VARCHAR(20),
  age INT,
  sex VARCHAR(5),
  address VARCHAR(100),
  math INT,
  english INT
);

-- 插入记录
insert into student values
(1,'马云',55,'男','杭州',66,78),
(2,'马化腾',45,'女','深圳',98,87),
(3,'马景涛',55,'男','香港',56,77),
(4,'柳岩',20,'女','湖南',76,65),
(5,'柳青',20,'男','湖南',86,NULL),
(6,'刘德华',57,'男','香港',99,99),
(7,'马德',22,'女','香港',99,99),
(8,'德玛西亚',18,'男','南京',56,65),
(9,'唐僧',25,'男','长安',87,78),
(10,'孙悟空',18,'男','花果山',100,66),
(11,'猪八戒',22,'男','高老庄',58,78),
(12,'沙僧',50,'男','流沙河',77,88),
(13,'白骨精',22,'女','白虎岭',66,66),
(14,'蜘蛛精',23,'女','盘丝洞',88,88);

-- 查询数据
SELECT id,name,age,english,math FROM student;
```

### <font style="color:rgb(51, 51, 51);">查询所有字段</font>

<font style="color:rgb(51, 51, 51);">查询所有字段是指查询表中所有字段的数据。这种方式可以将表中所有字段的数据都査询出来。MySQL中有两种方式可以查询表中所有的字段。</font>

<font style="color:rgb(51, 51, 51);">1.列出表的所有字段</font>

```sql
SELECT id,name,age,sex,address,math,english FROM student;
```

<font style="color:rgb(51, 51, 51);">2.使用“\*”查询所有字段</font>

```sql
语法：SELECT * FROM 表名；
例如：
SELECT * FROM student;
```

<font style="color:rgb(51, 51, 51);">“\*”可以表示所有的字段。这样就不用列出表中所有字段的名称了。但是，使用这种方式查询时，只能按照表中字段的顺序进行排列，不能改变字段的排列顺序。</font>

### <font style="color:rgb(51, 51, 51);">查询指定字段</font>

<font style="color:rgb(51, 51, 51);">査询数据时，可以在SELECT语句的“属性列表”中列出所要查询的字段。这种方式可以指定需要查询的字段，而不需要查询出所有的字段。</font>

```sql
SELECT id,name,math FROM student;
```

### <font style="color:rgb(51, 51, 51);">查询指定记录</font>

<font style="color:rgb(51, 51, 51);">SELECT语句中可以设置查询条件。用户可以根据自己的需要来设置查询条件，按条件进行查询。查询的结果必须满足查询条件。例如，需要査找id为1的学员记录， 那么可以设置“id=1”为查询条件。这样查询结果中的记录就都会满足“id=1” 这个条件。WHERE子句可以用来指定査询条件。其语法规则如下：</font>

```sql
SELECT 属性列表 FROM 表名 WHERE 条件表达式
SELECT * FROM student WHERE id=1;
```

## 单表高级查询

<font style="color:rgb(51, 51, 51);">上次课，我们通过WHERE子句来指定査询条件。我们仅操作最简单的比较查询条件。where条件还有如下表达式。今天我们将一一学习这些单表高级查询操作。</font>

| **<font style="color:rgb(51, 51, 51);">查询条件</font>** | **<font style="color:rgb(51, 51, 51);">符号或关键字</font>** |
| :--- | :--- |
| <font style="color:rgb(51, 51, 51);">比较</font> | <font style="color:rgb(51, 51, 51);">=、<、<=、>、>=、!=、<>、!>、!<</font> |
| <font style="color:rgb(51, 51, 51);">指定范围</font> | <font style="color:rgb(51, 51, 51);">BETWEEN AND、NOT BETWEEN AND</font> |
| <font style="color:rgb(51, 51, 51);">指定集合</font> | <font style="color:rgb(51, 51, 51);">IN、NOT IN</font> |
| <font style="color:rgb(51, 51, 51);">匹配字符</font> | <font style="color:rgb(51, 51, 51);">LIKE、NOT LIKE</font> |
| <font style="color:rgb(51, 51, 51);">是否为空值</font> | <font style="color:rgb(51, 51, 51);">IS NULL. IS NOT NULL</font> |
| <font style="color:rgb(51, 51, 51);">多个查询条件</font> | <font style="color:rgb(51, 51, 51);">AND、OR</font> |

### <font style="color:rgb(51, 51, 51);">带IN关键字的查询</font>

<font style="color:rgb(51, 51, 51);">IN关键字可以判断某个字段的值是否在指定的集合中。如果字段的值在集合中，则满足查询条件，该记录将被査询出来；如果不在集合中，则不满足查询条件。其语法规则如下：</font>

```sql
[NOT] IN (值1,值2，…，值n)
```

<font style="color:rgb(51, 51, 51);">其中，“NOT”是可选参数，加上NOT表示不在集合内满足条件；“值n”表示集合中的元素值，各元素值之间用逗号隔开，字符型元素需要加上单引号。</font>

```sql
#查询id为1和2的学员信息
SELECT * FROM student WHERE id IN (1,2);
```

### <font style="color:rgb(51, 51, 51);">带BETWEEN AND的范围查询</font>

<font style="color:rgb(51, 51, 51);">BETWEEN AND关键字可以判读某个字段的值是否在指定的范围内。如果字段的值在指定范围内，则满足查询条件，该记录将被查询岀来。如果不在指定范围内，则不满足查询条件。</font>

<font style="color:rgb(51, 51, 51);">其语法规则如下：</font>

```sql
[NOT] BETWEEN 取值 1 AND 取值 2
```

```sql
#查询数学成绩在80到99之间的学生信息
SELECT * FROM student WHERE math BETWEEN 80 AND 99;
```

<font style="color:rgb(51, 51, 51);">注意：BETWEEN AND查询结果包含两端的值。</font>

### <font style="color:rgb(51, 51, 51);">查询空值</font>

<font style="color:rgb(51, 51, 51);">IS NULL关键字可以用来判断字段的值是否为空值(NULL)。如果字段的值是空值, 则满足查询条件，该记录将被查询出来。如果字段的值不是空值，则不满足查询条件。其语法规则如下：</font>

```sql
IS [NOT] NULL
```

<font style="color:rgb(51, 51, 51);">其中，“NOT”是可选参数，加上NOT表示字段不是空值时满足条件。</font>

<font style="color:rgb(51, 51, 51);">案例：查询学员表中英语成绩为空的学员信息</font>

```sql
SELECT * FROM student WHERE english IS NULL;
```

<font style="color:rgb(51, 51, 51);">注意：IS NULL是一个整体，不能将IS换成"=”。如果将IS换成"=”将不能查询出任何结果，数据库系统会出现“Empty set (0.00 sec)”这样的提示。同理，IS NOT NULL中的IS NOT不能换成“!=”。如果使用IS NOT NULL关键字，将査询出该段的值不为空的所有记录</font>

<font style="color:rgb(51, 51, 51);">案例：查询学员表中英语成绩不为空的学员信息</font>

```sql
SELECT * FROM student WHERE english IS NOT NULL;
```

### <font style="color:rgb(51, 51, 51);">带AND的多条件查询</font>

<font style="color:rgb(51, 51, 51);">AND关键字可以用来联合多个条件进行查询。使用AND关键字时，只有同时满足所有查询条件的记录会被查询出来。如果不满足这些査询条件的其中一个，这样的记录将被排除掉。</font>

<font style="color:rgb(51, 51, 51);">AND关键字的语法规则如下：</font>

```sql
条件表达式1 AND 条件表达式2 [... AND 条件表达式n]
```

<font style="color:rgb(51, 51, 51);">其中，AND可以连接两个条件表达式。而且，可以同时使用多个AND关键字，这样可以连接更多的条件表达式。</font>

<font style="color:rgb(51, 51, 51);">案例：查询学员表中性别为男并且年龄大于35的学员信息</font>

```sql
SELECT * FROM student WHERE sex='男' AND age>35;
```

### <font style="color:rgb(51, 51, 51);">带OR的多条件查询</font>

<font style="color:rgb(51, 51, 51);">OR关键字也可以用来联合多个条件进行查询，但是与AND关键字不同。使用OR关键字时，只要满足这几个査询条件的其中一个，这样的记录将会被查询出来。如果这些查询条件中的任何一个都不满足，这样的记录将被排除掉。OR关键字的语法规则如下：</font>

```sql
条件表达式1 OR 条件表达式2 ［... OR 条件表达式n］
```

<font style="color:rgb(51, 51, 51);">其中，</font>**<font style="color:rgb(51, 51, 51);">OR</font>**<font style="color:rgb(51, 51, 51);">可以用来连接两个条件表达式。而且，可以同时使用多个</font>**<font style="color:rgb(51, 51, 51);">OR</font>**<font style="color:rgb(51, 51, 51);">关键字，这样可以连接更多的条件表达式。</font>

<font style="color:rgb(51, 51, 51);">案例：查询学生表中的性别为男或者年龄大于35的学员信息</font>

```sql
SELECT * FROM student WHERE sex='男' OR age>35;
```

**<font style="color:rgb(119, 119, 119);">OR可以和AND一起使用。当两者一起使用时，AND要比OR先运算。</font>**

<font style="color:rgb(51, 51, 51);">案例：下面同时使用OR和AND关键字查询student表中的记录</font>

<font style="color:rgb(51, 51, 51);">查询学员表中性别为男并且年龄大于35的学员信息或者数学成绩80的学员信息</font>

### <font style="color:rgb(51, 51, 51);">去除重复查询结果</font>

<font style="color:rgb(51, 51, 51);">案例：查询学员表的性别分类</font>

```sql
SELECT DISTINCT sex FROM student;
```

### <font style="color:rgb(51, 51, 51);">对查询结果排序</font>

<font style="color:rgb(51, 51, 51);">从表中查询出来的数据可能是无序的，或者其排列顺序不是用户所期望的顺序。为了使查询结果的顺序满足用户的要求，可以使用ORDER BY关键字对记录进行排序。</font>

<font style="color:rgb(51, 51, 51);">ORDER BY语法规则如下：</font>

```sql
ORDER BY 字段1［ASC|DESC］, 字段2［ASC|DESC］...
```

<font style="color:rgb(51, 51, 51);">其中，“属性名”参数表示按照该字段进行排序；ASC参数表示按升序的顺序进行排序；DESC参数表示按降序的顺序进行排序。默认的情况下，按照ASC方式进行排序。</font>

<font style="color:rgb(51, 51, 51);">ORDER BY可以基于多个属性进行排序，优先满足最左侧排序条件。如果最左侧排序条件相同的情况下，再基于后面的属性排序。</font>

<font style="color:rgb(51, 51, 51);">案例：查询所有学员信息按照数学成绩从低到高（升序）排序展示</font>

```sql
SELECT * FROM student ORDER BY math ASC; #ASC是默认排序方式，所以ASC是可以省略的
SELECT * FROM student ORDER BY math;
```

<font style="color:rgb(51, 51, 51);">上面查询结果显示是按照数学成绩升序的。但是发现有的学生数学成绩是相同的，我们可以再满足数据成绩升序的情况下，再跟进年龄升序查询。</font>

<font style="color:rgb(51, 51, 51);">相关SQL如下:</font>

```sql
SELECT * FROM student ORDER BY math ASC,age ASC;
```

### 模糊查询

可以根据指定的值进行模糊查询，使用like关键字。

```sql
-- 查询姓马的同学 %表示任意多个任意字符
select * from student where name like '马%';

-- 查询名字是以 "精" 结尾的同学的信息
select * from student where name like '%精';

-- 查询名字中包含 "德" 的学生的信息
select * from student where name like '%德%';

-- 查询名字中第2个字是"德"的学生信息
select * from student where name like '_德%';
```

### <font style="color:rgb(51, 51, 51);">分组查询</font>

<font style="color:rgb(51, 51, 51);">GROUP BY关键字可以将查询结果按某个字段或多个字段进行分组。字段中值相等的为一组。</font>

<font style="color:rgb(51, 51, 51);">GROUP BY关键字与集合函数一起使用时，可以通过集合函数计算分组中的总记录、 最大值、最小值等。</font>

<font style="color:rgb(51, 51, 51);">案例:查询学生表根据性别分组，显示每组的人数。</font>

```sql
SELECT sex , COUNT(*) AS '人数' FROM student GROUP BY sex;
```

<font style="color:rgb(51, 51, 51);">如果加上“HAVING条件表达式”，可以限制输出的结果。只有满足条件表达式的结果才会显示。</font>

<font style="color:rgb(51, 51, 51);">案例:查询学生表根据性别分组，显示人数大于5的小组。</font>

```sql
SELECT sex , COUNT(*) AS '人数' FROM student GROUP BY sex HAVING COUNT(*)>5;
```

### <font style="color:rgb(51, 51, 51);">用LIMIT分页查询</font>

<font style="color:rgb(51, 51, 51);">査询数据时，可能会查询出很多的记录。而用户需要的记录可能只是很少的一部分。 这样就需要来限制查询结果的数量。LIMIT是MySQL中的一个特殊关键字。其可以用来 指定査询结果从哪条记录开始显示。还可以指定一共显示多少条记录。</font>

```sql
LIMIT 初始位置，记录数
```

<font style="color:rgb(51, 51, 51);">其中，“初始位置”参数指定从哪条记录开始显示；“记录数”参数表示显示记录的条数。第一条记录的位置是0,第二条记录的位置是1。后面的记录依次类推。</font>

```sql
SELECT * FROM student LIMIT  0,2;
```

## 聚合函数

<font style="color:rgb(51, 51, 51);">聚合函数包括 COUNT()、SUM()、AVG()、MAX()和 MIN()。 其中，COUNT()用来统计记录的条数;SUM()用来计算字段的值的总和；AVG()用来计算字段的值的平均值;MAX() 用来查询字段的最大值；MIN()用来査询字段的最小值。当需要对表中的记录求和、求平均值、查询最大值和查询最小值等操作时，可以使用聚合函数。例如，需要计算学生成绩表中的平均成绩，可以使用AVG()函数。GROUP BY关键字通常需要与聚合函数一起使用。</font>

### <font style="color:rgb(51, 51, 51);">COUNT函数</font>

<font style="color:rgb(51, 51, 51);">COUNT函数用来统计表中记录的条数。如果要统计student表中有多少条记录，可以使用COUNT()函数。如果要统计student表中不同性别的人数，也可以使用COUNT()函数。</font>

<font style="color:rgb(51, 51, 51);">案例:统计student表中学生的总数：</font>

```sql
SELECT COUNT(*) FROM student;
```

### <font style="color:rgb(51, 51, 51);">SUM函数</font>

<font style="color:rgb(51, 51, 51);">SUM()是求和函数。使用SUM()函数可以求出表中某个字段取值的总和。</font>

<font style="color:rgb(51, 51, 51);">例如， 可以用SUM()函数来求班级学生的数学总成绩。</font>

```sql
SELECT SUM(math) FROM student;
```

<font style="color:rgb(51, 51, 51);">注意：SUM()函数只能计算数值类型的字段，包括INT类型、FLOAT类型、DOUBLE 类型、DECIMAL类型等。字符类型的字段不能使用SUM()函数进行计算。使用 SUM()函数计算字符类型字段时，计算结果都为0。</font>

### <font style="color:rgb(51, 51, 51);">AVG函数</font>

<font style="color:rgb(51, 51, 51);">AVG()函数是求平均值的函数。使用AVG()函数可以求出表中某个字段取值的平均值。 例如，可以用AVG()函数来求平均年龄，也可以使用AVG()函数来求学生的平均成绩。</font>

<font style="color:rgb(51, 51, 51);">案例：我们使用AVG()函数求一下班级数学成绩的平均值</font>

```sql
SELECT AVG(math) FROM student;
```

<font style="color:rgb(51, 51, 51);">结果显示，AVG()函数计算岀math字段的平均值。AVG()函数经常与GROUP BY字段 一起使用，来计算每个分组的平均值。</font>

<font style="color:rgb(51, 51, 51);">案例：我们可以根据性别分组，然后统计各性别组数学成绩的平均值。</font>

```sql
SELECT sex,AVG(math) FROM student GROUP BY sex;
```

### <font style="color:rgb(51, 51, 51);">MAX函数</font>

<font style="color:rgb(51, 51, 51);">MAX()函数是求最大值的函数。使用MAX()函数可以求出表中某个字段取值的最大值。例如，可以用MAX()函数来查询最大年龄，也可以使用MAX()函数来求各科的最高成绩。</font>

<font style="color:rgb(51, 51, 51);">案例：我们获取student表数学最高分</font>

```sql
SELECT MAX(math) FROM student;
```

### <font style="color:rgb(51, 51, 51);">MIN函数</font>

<font style="color:rgb(51, 51, 51);">M1N()函数是求最小值的函数。使用MIN()函数可以求出表中某个字段取值的最小值。 例如，可以用MIN()函数来查询最小年龄，也可以使用MIN()函数来求各科的最低成绩。</font>

<font style="color:rgb(51, 51, 51);">案例：我们获取student表数学最低分</font>

```sql
SELECT MIN(age) FROM emp;
```

## 连接查询

如果要查询的数据涉及到多张表，就需要用关联查询。

表与表之间的关系：

* 一对一
* 一对多
* 多对多

关联查询有：

* 内连接：将两张表中能够关联上的数据都查询出来
* 左连接：将左表中的数据都查询出来，右表中能关联上的数据就正常显示，关联不上的不显示
* 右连接：将右表中的数据都查询出来，左表中能关联上的数据就显示，关联不上的不显示

```sql
-- 查询员工的信息及其部门信息，使用内连接
select * from emp e inner join dept d on e.did=d.did;

-- 查询所有的员工信息及其部门信息，使用左连接
select * from emp left join dept on emp.did=dept.did;

-- 查询所有的员工信息及其部门信息，使用右连接
select * from emp right join dept on emp.did=dept.did;
```

## 商品管理系统表结构设计

# JDBC

## JDBC 介绍

<font style="color:rgb(51, 51, 51);">JDBC（Java DataBase Connectivity,java数据库连接）是一种用于执行SQL语句的Java API，可以为多种关系数据库提供统一访问，它由一组用Java语言编写的类和接口组成。JDBC提供了一种基准，据此可以构建更高级的工具和接口，使数据库开发人员能够编写数据库应用程序。</font>

## <font style="color:rgb(51, 51, 51);">JDBC核心类接口介绍</font>

<font style="color:rgb(51, 51, 51);">JDBC中的核心类有：DriverManager、Connection、Statement，和ResultSet！</font>

**<font style="color:rgb(51, 51, 51);">DriverManager（驱动管理器）</font>**

> DriverManger（驱动管理器）的作用：
>
> 获取Connection：如果可以获取到Connection，那么说明已经与数据库连接上了。
>
> 其实我们今后只需要会用DriverManager的getConnection()方法即可

**<font style="color:rgb(51, 51, 51);">Connection连接对象：</font>**

> <font style="color:rgb(51, 51, 51);">Connection对象表示连接，与数据库的通讯都是通过这个对象展开的：</font>
>
> <font style="color:rgb(51, 51, 51);">Connection最为重要的一个方法就是用来获取Statement对象；</font>
>
> <font style="color:rgb(51, 51, 51);">Statement stmt = con.createStatement(); </font>

**<font style="color:rgb(51, 51, 51);">Statement执行对象：</font>**

> <font style="color:rgb(51, 51, 51);">Statement是用来向数据库发送SQL语句的，这样数据库就会执行发送过来的SQL语句：</font>
>
> <font style="color:rgb(51, 51, 51);">INT executeUpdate(String sql)：执行更新操作（insert、update、delete等）；</font>
>
> <font style="color:rgb(51, 51, 51);">ResultSet executeQuery(String sql)：执行查询操作，数据库在执行查询后会把查询结果，查询结果就是ResultSet；</font>

**<font style="color:rgb(51, 51, 51);">ResultSet查询结果集对象：</font>**

> ResultSet对象表示查询结果集，只有在执行查询操作后才会有结果集的产生。结果集是一个二维的表格，有行有列。操作结果集要学习移动ResultSet内部的“行光标”，以及获取当前行上的每一列上的数据：
>
> boolean next()：使“行光标”移动到下一行，并返回移动后的行是否存在；
>
> XXX getXXX(String 列名)：获取当前行指定列上的值，参数就是列名

## JDBC获取数据库连接

### 导入数据库驱动包

创建lib文件夹，将数据库驱动包粘贴到lib文件夹中，然后添加到类路径生效。

![1724935384208-c7965f0c-1dce-4983-b255-ae4afe833fd1.png](./img/TvMXBSJiS74TOLoG/1724935384208-c7965f0c-1dce-4983-b255-ae4afe833fd1-989074.png)

### 编写代码

```java
import java.sql.Connection;
import java.sql.DriverManager;

public class Demo1 {

    public static void main(String[] args) throws Exception {
        // 加载数据库驱动
        Class.forName("com.mysql.jdbc.Driver");

        // 获取数据库连接
        String url = "jdbc:mysql://localhost:3306/test";
        String user = "root";
        String password = "123456";
        Connection connection = DriverManager.getConnection(url, user, password);

        System.out.println(connection);
    }
}
```

**结果：**

![1724935537251-9fe39164-33a0-4f60-a3c1-c1c59dcc35da.png](./img/TvMXBSJiS74TOLoG/1724935537251-9fe39164-33a0-4f60-a3c1-c1c59dcc35da-048708.png)

## PreparedStatement 介绍

PreparedStatement叫预编译对象，PreparedStatement是Statement的子接口，你可以使用PreparedStatement来替换Statement。

使用Connection的prepareStatement(String sql)：即创建它时就让它与一条SQL模板绑定；

调用PreparedStatement的setXXX()系列方法为问号设置值

调用executeUpdate()或executeQuery()方法执行增删改查操作。但要注意，调用没有参数的方法；

## PreparedStatement实现增删改查操作

### 数据库准备

:::info
创建数据库

:::

![1724935781158-20da520b-801b-42d9-8835-69afa2d6276a.png](./img/TvMXBSJiS74TOLoG/1724935781158-20da520b-801b-42d9-8835-69afa2d6276a-469271.png)

:::info
创建数据库表

:::

![1724936168592-6e19c5c4-493d-4098-be12-04ae971d9cf5.png](./img/TvMXBSJiS74TOLoG/1724936168592-6e19c5c4-493d-4098-be12-04ae971d9cf5-959455.png)

![1724935855017-4303d4d1-e3c1-4519-8500-5dde6f49e624.png](./img/TvMXBSJiS74TOLoG/1724935855017-4303d4d1-e3c1-4519-8500-5dde6f49e624-646054.png)

### PreparedStatement 实现新增

```java
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;

public class Demo2 {

    // 添加功能
    public static void main(String[] args) throws Exception {
        // 1.加载数据库驱动
        Class.forName("com.mysql.jdbc.Driver");

        // 2.获取数据库连接
        String url = "jdbc:mysql://localhost:3306/jdbc_demo?useUnicode=true&characterEncoding=utf8";
        String user = "root";
        String password = "123456";
        Connection connection = DriverManager.getConnection(url, user, password);

        // 3.编写sql语句
        String sql = "insert into user values(null, ?, ?, ?)";

        // 4.创建预编译语句对象
        PreparedStatement ps = connection.prepareStatement(sql);

        // 5.给sql语句中占位符赋值
        ps.setString(1, "曹操");
        ps.setString(2, "男");
        ps.setInt(3, 20);

        // 6.执行sql语句
        int i = ps.executeUpdate();
        System.out.println("受影响的行数：" + i);

        // 7.关闭连接
        if(connection != null){
            connection.close();
        }
    }
}
```

### PreparedStatement 实现修改

```java
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;

public class Demo3 {

    // 修改功能
    public static void main(String[] args) throws Exception {

        // 1.加载数据库驱动
        Class.forName("com.mysql.jdbc.Driver");

        // 2.获取数据库连接
        String url = "jdbc:mysql://localhost:3306/jdbc_demo?useUnicode=true&characterEncoding=utf8";
        String user = "root";
        String password = "123456";
        Connection connection = DriverManager.getConnection(url, user, password);

        // 3.编写sql
        String sql = "update user set name=?, sex=?, age=? where id=?";

        // 4.创建预编译语句对象
        PreparedStatement ps = connection.prepareStatement(sql);

        // 5.给sql语句中的占位符赋值
        ps.setString(1, "吕布");
        ps.setString(2, "男");
        ps.setInt(3, 28);
        ps.setInt(4, 1);

        // 6.执行sql语句
        int i = ps.executeUpdate();
        System.out.println("受影响的行数：" + i);

        // 7.关闭连接
        if(connection != null){
            connection.close();
        }
    }
}
```

### PreparedStatement 实现删除

```java
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;
import java.sql.SQLException;

public class Demo4 {

    // 删除功能
    public static void main(String[] args) throws Exception {
        // 1.加载数据库驱动
        Class.forName("com.mysql.jdbc.Driver");

        // 2.获取数据库连接
        String url = "jdbc:mysql://localhost:3306/jdbc_demo?useUnicode=true&characterEncoding=utf8";
        String user = "root";
        String password = "123456";
        Connection connection = DriverManager.getConnection(url, user, password);

        // 3.编写sql语句
        String sql = "delete from user where id=?";

        // 4.创建预编译语句对象
        PreparedStatement ps = connection.prepareStatement(sql);

        // 5.设置sql中占位符的值
        ps.setInt(1, 2);

        // 6.执行sql
        int i = ps.executeUpdate();
        System.out.println("受影响的行数：" + i);

        // 7.关闭连接
        if(connection != null){
            connection.close();
        }
    }
}
```

### PreparedStatement 实现查询1

**查询所有的数据**

```java
import java.sql.*;

public class Demo5 {

    // 查询功能
    public static void main(String[] args) throws Exception {
        // 1.加载数据库驱动
        Class.forName("com.mysql.jdbc.Driver");

        // 2.获取数据库连接
        String url = "jdbc:mysql://localhost:3306/jdbc_demo?useUnicode=true&characterEncoding=utf8";
        String user = "root";
        String password = "123456";
        Connection connection = DriverManager.getConnection(url, user, password);

        // 3.编写sql语句
        String sql = "select * from user";

        // 4.创建预编译语句对象
        PreparedStatement ps = connection.prepareStatement(sql);

        // 5.执行sql，得到结果集
        ResultSet rs = ps.executeQuery();

        // 6.遍历结果集
        while(rs.next()){
            int id = rs.getInt("id");
            String name = rs.getString("name");
            String sex = rs.getString("sex");
            int age = rs.getInt("age");

            System.out.println("编号：" + id + ", 姓名：" + name + ", 性别：" + sex + ", 年龄：" + age);
        }

        // 7.关闭连接
        if(connection != null){
            connection.close();
        }
    }
}
```

### PreparedStatement 实现查询2

**根据id条件查询**

```java
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;
import java.sql.ResultSet;

public class Demo6 {

    // 查询功能
    public static void main(String[] args) throws Exception {
        // 1.加载数据库驱动
        Class.forName("com.mysql.jdbc.Driver");

        // 2.获取数据库连接
        String url = "jdbc:mysql://localhost:3306/jdbc_demo?useUnicode=true&characterEncoding=utf8";
        String user = "root";
        String password = "123456";
        Connection connection = DriverManager.getConnection(url, user, password);

        // 3.编写sql语句
        String sql = "select * from user where id=?";

        // 4.创建预编译语句对象
        PreparedStatement ps = connection.prepareStatement(sql);

        // 5.设置sql中占位符的值
        ps.setInt(1, 1);

        // 6.执行sql，得到结果集
        ResultSet rs = ps.executeQuery();

        // 6.遍历结果集
        while(rs.next()){
            int id = rs.getInt("id");
            String name = rs.getString("name");
            String sex = rs.getString("sex");
            int age = rs.getInt("age");

            System.out.println("编号：" + id + ", 姓名：" + name + ", 性别：" + sex + ", 年龄：" + age);
        }

        // 7.关闭连接
        if(connection != null){
            connection.close();
        }
    }
}
```

### PreparedStatement 实现查询3

```java
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;
import java.sql.ResultSet;

public class Demo8 {

    // 查询功能
    public static void main(String[] args) throws Exception {
        // 1.加载数据库驱动
        Class.forName("com.mysql.jdbc.Driver");

        // 2.获取数据库连接
        String url = "jdbc:mysql://localhost:3306/jdbc_demo?useUnicode=true&characterEncoding=utf8";
        String user = "root";
        String password = "123456";
        Connection connection = DriverManager.getConnection(url, user, password);

        // 3.编写sql语句
        String sql = "select * from user where name=? and age=?";

        // 4.创建预编译语句对象
        PreparedStatement ps = connection.prepareStatement(sql);

        // 5.给sql语句中占位符赋值
        ps.setString(1, "吕布");
        ps.setInt(2, 28);

        // 6.执行sql，得到结果集
        ResultSet rs = ps.executeQuery();

        // 7.遍历结果集
        while(rs.next()){
            int id = rs.getInt("id");
            String name = rs.getString("name");
            String sex = rs.getString("sex");
            int age = rs.getInt("age");

            System.out.println("编号：" + id + ", 姓名：" + name + ", 性别：" + sex + ", 年龄：" + age);
        }

        // 7.关闭连接
        if(connection != null){
            connection.close();
        }
    }
}
```

### PreparedStatement 实现查询4

```java
public class User {
    
    private int id;
    private String name;
    private String sex;
    private int age;

    public User() {
    }

    public User(int id, String name, String sex, int age) {
        this.id = id;
        this.name = name;
        this.sex = sex;
        this.age = age;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getSex() {
        return sex;
    }

    public void setSex(String sex) {
        this.sex = sex;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    @Override
    public String toString() {
        return "User{" +
                "id=" + id +
                ", name='" + name + '\'' +
                ", sex='" + sex + '\'' +
                ", age=" + age +
                '}';
    }
}
```

```java
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;
import java.sql.ResultSet;
import java.util.ArrayList;
import java.util.List;

public class Demo7 {

    // 查询功能
    public static void main(String[] args) throws Exception {
        // 1.加载数据库驱动
        Class.forName("com.mysql.jdbc.Driver");

        // 2.获取数据库连接
        String url = "jdbc:mysql://localhost:3306/jdbc_demo?useUnicode=true&characterEncoding=utf8";
        String user = "root";
        String password = "123456";
        Connection connection = DriverManager.getConnection(url, user, password);

        // 3.编写sql语句
        String sql = "select * from user";

        // 4.创建预编译语句对象
        PreparedStatement ps = connection.prepareStatement(sql);

        // 5.执行sql，得到结果集
        ResultSet rs = ps.executeQuery();

        // 6.遍历结果集，封装到 list 集合中
        List<User> list = new ArrayList<>();
        while(rs.next()){
            int id = rs.getInt("id");
            String name = rs.getString("name");
            String sex = rs.getString("sex");
            int age = rs.getInt("age");

            User u = new User(id, name, sex, age);
            list.add(u);
        }

        // 7.遍历list集合
        for (User u : list) {
            System.out.println(u);
        }

        // 8.关闭连接
        if(connection != null){
            connection.close();
        }
    }
}
```

# <font style="color:rgb(51, 51, 51);">DBUtils 工具</font>

## 概述

<font style="color:rgb(51, 51, 51);">DBUtils 是 Apache 的工具，是一个对 JDBC 简单封装的工具。提供了一些通用的 JDBC 操作方法。</font>

## <font style="color:rgb(51, 51, 51);">DBUtils 工具的使用方式</font>

* 导入 DBUtils 工具的 jar 包
* 常用的 API 方法
  * **QueryRunner** 类： 此类中含有可以执行更新操作或者查询操作
    * update(.....)： 用于更新操作（DDL、DML）
    * query(.....)： 用于查询操作（DQL）
  * ResultSetHandler 接口：用于封装查询之后的结果
    * BeanHandler： 把结果集的第一行数据封装成 JavaBean 对象
    * **BeanListHandler**：把结果集的每一行数据封装成 JavaBean 对象，再把这个 JavaBean 放入List 集合中
    * ScalarHandler：把结果集的第一行第一列取出。通常用于聚合函数查询。例如（count()/max()）
    * 如果表的字段名称和 JavaBean 的属性名称不一致时，需要让 JavaBean 类实现 ResultSetHandler 接口，指定字段和属性的对应关系

## 编写工具类

使用 JDBC 时，我们不论做什么操作都要获取连接，并且操作完之后都要关闭连接。所以，我们可以写一个工具类，编写好这两个方法，以后直接调用即可。

```java
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;

public class JDBCUtils {

    static{
        try {
            // 加载数据库驱动
            Class.forName("com.mysql.jdbc.Driver");
        } catch (ClassNotFoundException e) {
            e.printStackTrace();
        }
    }

    // 获取数据库连接
    public static Connection getConnection(){
        String url = "jdbc:mysql:///jdbc_demo?useUnicode=true&characterEncoding=utf8";
        String username = "root";
        String password = "123456";
        Connection connection = null;
        try {
            connection = DriverManager.getConnection(url, username, password);
        } catch (SQLException e) {
            e.printStackTrace();
        }
        return connection;
    }

    // 关闭连接
    public static void closeConnection(Connection connection){
        if(connection != null){
            try {
                connection.close();
            } catch (SQLException e) {
                e.printStackTrace();
            }
        }
    }
}
```

## QueryRunner 实现添加功能

```java
import org.apache.commons.dbutils.QueryRunner;

import java.sql.Connection;
import java.sql.SQLException;

public class Demo1 {

    public static void main(String[] args) throws SQLException {
        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql语句
        String sql = "insert into user values(null, ?, ?, ?)";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.执行SQL语句
        int i = queryRunner.update(connection, sql, "曹操", "男", 55);
        System.out.println("受影响的行数：" + i);

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);
    }
}
```

## QueryRunner 实现修改功能

```java
import org.apache.commons.dbutils.QueryRunner;

import java.sql.Connection;
import java.sql.SQLException;

public class Demo2 {

    public static void main(String[] args) throws SQLException {
        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql语句
        String sql = "update user set name=?, sex=?, age=? where id=?";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.执行SQL语句
        int i = queryRunner.update(connection, sql, "貂蝉", "女", 18, 1);
        System.out.println("受影响的行数：" + i);

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);
    }
}
```

## QueryRunner 实现删除功能

```java
import org.apache.commons.dbutils.QueryRunner;

import java.sql.Connection;
import java.sql.SQLException;

public class Demo3 {

    public static void main(String[] args) throws SQLException {
        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql语句
        String sql = "delete from user where id=?";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.执行SQL语句
        int i = queryRunner.update(connection, sql, 1);
        System.out.println("受影响的行数：" + i);

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);
    }
}
```

## QueryRunner 实现查询所有功能

```java
public class User {
    
    private int id;
    private String name;
    private String sex;
    private int age;

    public User() {
    }

    public User(int id, String name, String sex, int age) {
        this.id = id;
        this.name = name;
        this.sex = sex;
        this.age = age;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getSex() {
        return sex;
    }

    public void setSex(String sex) {
        this.sex = sex;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    @Override
    public String toString() {
        return "User{" +
                "id=" + id +
                ", name='" + name + '\'' +
                ", sex='" + sex + '\'' +
                ", age=" + age +
                '}';
    }
}
```

```java
import org.apache.commons.dbutils.QueryRunner;
import org.apache.commons.dbutils.handlers.BeanListHandler;

import java.sql.Connection;
import java.sql.SQLException;
import java.util.List;

public class Demo4 {

    public static void main(String[] args) throws SQLException {
        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql语句
        String sql = "select * from user";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.执行SQL语句
        List<User> list = queryRunner.query(connection, sql, new BeanListHandler<>(User.class));

        for(int i = 0; i < list.size(); i++){
            System.out.println(list.get(i));
        }

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);
    }
}
```

## QueryRunner 实现条件查询

```java
import org.apache.commons.dbutils.QueryRunner;
import org.apache.commons.dbutils.handlers.BeanListHandler;

import java.sql.Connection;
import java.sql.SQLException;
import java.util.List;

public class Demo5 {

    public static void main(String[] args) throws SQLException {
        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql语句
        String sql = "select * from user where sex=? and age > ?";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.执行SQL语句
        List<User> list = queryRunner.query(connection, sql, new BeanListHandler<>(User.class), "男", 18);

        for(int i = 0; i < list.size(); i++){
            System.out.println(list.get(i));
        }

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);
    }
}
```

## QueryRunner 实现根据id查询

```java
import org.apache.commons.dbutils.QueryRunner;
import org.apache.commons.dbutils.handlers.BeanHandler;
import org.apache.commons.dbutils.handlers.BeanListHandler;

import java.sql.Connection;
import java.sql.SQLException;
import java.util.List;

public class Demo6 {

    public static void main(String[] args) throws SQLException {
        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql语句
        String sql = "select * from user where id=?";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.执行SQL语句
        User user = queryRunner.query(connection, sql, new BeanHandler<>(User.class), 1);

        System.out.println(user);

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);
    }
}
```

# 利用 MySQL + JDBC 改造商品管理系统

## pojo 包介绍

pojo 用来存放实体类。

## dao 包介绍

dao 包用来编写操作数据库的代码。data access object

## utils 包介绍

utils 包用来存放工具类。

包名：公司域名的反写。

百度：www.baidu.com，com.baidu.pojo	com.baidu.utils

com.zs.pojo com.zs.dao com.zs.utils

## 准备工作

### 导入jar包

![1725260447277-0410da31-a323-45b5-9172-e019b1888ee0.png](./img/TvMXBSJiS74TOLoG/1725260447277-0410da31-a323-45b5-9172-e019b1888ee0-310947.png)

### 创建包结构

![1725260476971-70203672-a809-4e3e-9a39-f51ad951ef09.png](./img/TvMXBSJiS74TOLoG/1725260476971-70203672-a809-4e3e-9a39-f51ad951ef09-435295.png)

### 编写实体类

```java
package com.lhp.pojo;

import java.util.Date;

public class Goods {

    private int id;
    private String name;
    private double price;
    private Date producedate; // java.util.Date
    private String address;

    public Goods() {
    }

    public Goods(int id, String name, double price, Date producedate, String address) {
        this.id = id;
        this.name = name;
        this.price = price;
        this.producedate = producedate;
        this.address = address;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public double getPrice() {
        return price;
    }

    public void setPrice(double price) {
        this.price = price;
    }

    public Date getProducedate() {
        return producedate;
    }

    public void setProducedate(Date producedate) {
        this.producedate = producedate;
    }

    public String getAddress() {
        return address;
    }

    public void setAddress(String address) {
        this.address = address;
    }

    @Override
    public String toString() {
        return "Goods{" +
                "id=" + id +
                ", name='" + name + '\'' +
                ", price=" + price +
                ", producedate=" + producedate +
                ", address='" + address + '\'' +
                '}';
    }
}
```

### 编写工具类

```java
package com.lhp.utils;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;

// 数据库的工具类
public class JDBCUtils {

    static{ // 静态代码块，在静态代码块中的代码只会执行一次！

        // 加载数据库驱动
        try {
            Class.forName("com.mysql.jdbc.Driver");
        } catch (ClassNotFoundException e) {
            e.printStackTrace();
        }
    }


    // 获取数据库连接的方法
    public static Connection getConnection(){

        String url = "jdbc:mysql:///jdbc_demo?useUnicode=true&characterEncoding=utf8";
        String username = "root";
        String password = "123456";
        Connection connection = null;
        try {
            connection = DriverManager.getConnection(url, username, password);
        } catch (SQLException e) {
            e.printStackTrace();
        }

        return connection;
    }


    // 关闭数据库连接的方法
    public static void closeConnection(Connection connection){
        if(connection != null){
            try {
                connection.close();
            } catch (SQLException e) {
                e.printStackTrace();
            }
        }
    }
}
```

### 编写基本的系统结构

```java
package com.lhp;

import java.util.Scanner;

// 商品管理系统
public class GoodsManage {

    public static void main(String[] args) {

        // 创建Scanner对象，用来读取用户在控制台输入的内容
        Scanner scanner = new Scanner(System.in);
        System.out.println("********************欢迎使用商品管理系统**********************");

        while(true){
            System.out.println("请输入操作：1-商品列表展示 2-商品添加 3-商品修改 4-商品删除 5-退出系统");

            // 读取用户输入的操作数字
            int num = scanner.nextInt();

            if(num == 1){ // 商品列表展示
                // 查询goods表中的所有的数据

            }else if(num == 2){ // 商品添加

            }else if(num == 3){ // 商品修改

            }else if(num == 4){ // 商品删除

            }else if(num == 5){ // 退出
                System.out.println("bye bye!");
                return; // 结束整个方法
            }else{
                System.out.println("请输入正确的数字！");
            }
        }
    }
}
```

## 实现商品列表展示功能

### 编写dao层代码

```java
package com.lhp.dao;

import com.lhp.pojo.Goods;
import com.lhp.utils.JDBCUtils;
import org.apache.commons.dbutils.QueryRunner;
import org.apache.commons.dbutils.handlers.BeanListHandler;

import java.sql.Connection;
import java.sql.SQLException;
import java.util.List;

// 操作goods表
public class GoodsDao {

    // 查询
    public List<Goods> findAll() throws SQLException {

        // 获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 编写sql语句
        String sql = "select * from goods";

        // 创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 调用查询方法
        List<Goods> list = queryRunner.query(connection, sql, new BeanListHandler<>(Goods.class));

        return list;
    }


    // 添加....
}
```

### 主程序类

```java
package com.lhp;

import com.lhp.dao.GoodsDao;
import com.lhp.pojo.Goods;

import java.sql.SQLException;
import java.util.List;
import java.util.Scanner;

// 商品管理系统
public class GoodsManage {

    public static void main(String[] args) throws Exception {

        // 创建Scanner对象，用来读取用户在控制台输入的内容
        Scanner scanner = new Scanner(System.in);
        System.out.println("********************欢迎使用商品管理系统**********************");

        while(true){
            System.out.println("请输入操作：1-商品列表展示 2-商品添加 3-商品修改 4-商品删除 5-退出系统");

            // 读取用户输入的操作数字
            int num = scanner.nextInt();

            if(num == 1){ // 商品列表展示
                // 查询goods表中的所有的数据
                GoodsDao goodsDao = new GoodsDao();
                List<Goods> list = goodsDao.findAll();

                System.out.println("商品编号\t\t商品名称\t\t商品价格\t\t生产日期\t\t生产地址");
                for (Goods g : list) { // 增强for循环
                    System.out.println(g.getId() + "\t\t" + g.getName() + "\t\t" +
                            g.getPrice() + "\t\t" + g.getProducedate() + "\t\t" + g.getAddress());
                }

            }else if(num == 2){ // 商品添加

            }else if(num == 3){ // 商品修改

            }else if(num == 4){ // 商品删除

            }else if(num == 5){ // 退出
                System.out.println("bye bye!");
                return; // 结束整个方法
            }else{
                System.out.println("请输入正确的数字！");
            }
        }
    }
}
```

## 实现商品添加功能

### 编写dao层代码

```java
package com.lhp.dao;

import com.lhp.pojo.Goods;
import com.lhp.utils.JDBCUtils;
import org.apache.commons.dbutils.QueryRunner;
import org.apache.commons.dbutils.handlers.BeanListHandler;

import java.sql.Connection;
import java.sql.SQLException;
import java.util.List;

// 操作goods表
public class GoodsDao {

    // 查询
    public List<Goods> findAll() throws SQLException {

        // 获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 编写sql语句
        String sql = "select * from goods";

        // 创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 调用查询方法
        List<Goods> list = queryRunner.query(connection, sql, new BeanListHandler<>(Goods.class));

        return list;
    }


    // 添加....
    public void addGoods(Goods g) throws SQLException {

        // 获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 编写sql语句
        String sql = "insert into goods values(null, ?, ?, ?, ?)";

        // 创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 调用方法执行sql语句
        queryRunner.update(connection, sql, g.getName(), g.getPrice(), g.getProducedate(), g.getAddress());

        // 关闭连接
        JDBCUtils.closeConnection(connection);
    }
}
```

### 编写主程序类

```java
package com.lhp;

import com.lhp.dao.GoodsDao;
import com.lhp.pojo.Goods;

import java.sql.SQLException;
import java.text.SimpleDateFormat;
import java.util.Date;
import java.util.List;
import java.util.Scanner;

// 商品管理系统
public class GoodsManage {

    public static void main(String[] args) throws Exception {

        // 创建Scanner对象，用来读取用户在控制台输入的内容
        Scanner scanner = new Scanner(System.in);
        System.out.println("********************欢迎使用商品管理系统**********************");

        while(true){
            System.out.println("请输入操作：1-商品列表展示 2-商品添加 3-商品修改 4-商品删除 5-退出系统");

            // 读取用户输入的操作数字
            int num = scanner.nextInt();

            if(num == 1){ // 商品列表展示
                // 查询goods表中的所有的数据
                GoodsDao goodsDao = new GoodsDao();
                List<Goods> list = goodsDao.findAll();

                System.out.println("商品编号\t\t商品名称\t\t商品价格\t\t生产日期\t\t生产地址");
                for (Goods g : list) { // 增强for循环
                    System.out.println(g.getId() + "\t\t" + g.getName() + "\t\t" +
                            g.getPrice() + "\t\t" + g.getProducedate() + "\t\t" + g.getAddress());
                }

            }else if(num == 2){ // 商品添加
                System.out.print("商品名称：");
                String name = scanner.next();
                System.out.print("商品价格：");
                double price = scanner.nextDouble();
                System.out.print("生产日期(2020-05-05)：");
                String str = scanner.next();

                // 将字符串的日期转为Date类型的日期
                SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
                Date producedate = sdf.parse(str);

                System.out.print("生产地址：");
                String address = scanner.next();

                // 将上面的信息封装到goods对象中
                Goods goods = new Goods(0, name, price, producedate, address);

                // 调用goodsDao中的添加方法，并传递goods对象
                GoodsDao goodsDao = new GoodsDao();
                goodsDao.addGoods(goods);

                System.out.println("添加成功！");
            }else if(num == 3){ // 商品修改

            }else if(num == 4){ // 商品删除

            }else if(num == 5){ // 退出
                System.out.println("bye bye!");
                return; // 结束整个方法
            }else{
                System.out.println("请输入正确的数字！");
            }
        }
    }
}
```

## 实现商品修改功能

### 编写dao层代码

```java
package com.lhp.dao;

import com.lhp.pojo.Goods;
import com.lhp.utils.JDBCUtils;
import org.apache.commons.dbutils.QueryRunner;
import org.apache.commons.dbutils.handlers.BeanListHandler;

import java.sql.Connection;
import java.sql.SQLException;
import java.util.List;

// 操作goods表
public class GoodsDao {

    // 查询
    public List<Goods> findAll() throws SQLException {

        // 获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 编写sql语句
        String sql = "select * from goods";

        // 创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 调用查询方法
        List<Goods> list = queryRunner.query(connection, sql, new BeanListHandler<>(Goods.class));

        return list;
    }


    // 添加....
    public void addGoods(Goods g) throws SQLException {

        // 获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 编写sql语句
        String sql = "insert into goods values(null, ?, ?, ?, ?)";

        // 创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 调用方法执行sql语句
        queryRunner.update(connection, sql, g.getName(), g.getPrice(), g.getProducedate(), g.getAddress());

        // 关闭连接
        JDBCUtils.closeConnection(connection);
    }

    // 根据id修改商品
    public void updateGoods(Goods g) throws SQLException {

        // 获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 编写sql语句
        String sql = "update goods set name=?, price=?, producedate=?, address=? where id=?";

        // 创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 调用方法执行sql
        queryRunner.update(connection, sql, g.getName(),g.getPrice(),g.getProducedate(),g.getAddress(),g.getId());

        // 关闭连接
        JDBCUtils.closeConnection(connection);
    }
}
```

### 主程序类

```java
package com.lhp;

import com.lhp.dao.GoodsDao;
import com.lhp.pojo.Goods;

import java.sql.SQLException;
import java.text.SimpleDateFormat;
import java.util.Date;
import java.util.List;
import java.util.Scanner;

// 商品管理系统
public class GoodsManage {

    public static void main(String[] args) throws Exception {

        // 创建Scanner对象，用来读取用户在控制台输入的内容
        Scanner scanner = new Scanner(System.in);
        System.out.println("********************欢迎使用商品管理系统**********************");

        while(true){
            System.out.println("请输入操作：1-商品列表展示 2-商品添加 3-商品修改 4-商品删除 5-退出系统");

            // 读取用户输入的操作数字
            int num = scanner.nextInt();

            if(num == 1){ // 商品列表展示
                // 查询goods表中的所有的数据
                GoodsDao goodsDao = new GoodsDao();
                List<Goods> list = goodsDao.findAll();

                System.out.println("商品编号\t\t商品名称\t\t商品价格\t\t生产日期\t\t生产地址");
                for (Goods g : list) { // 增强for循环
                    System.out.println(g.getId() + "\t\t" + g.getName() + "\t\t" +
                            g.getPrice() + "\t\t" + g.getProducedate() + "\t\t" + g.getAddress());
                }

            }else if(num == 2){ // 商品添加
                System.out.print("商品名称：");
                String name = scanner.next();
                System.out.print("商品价格：");
                double price = scanner.nextDouble();
                System.out.print("生产日期(2020-05-05)：");
                String str = scanner.next();

                // 将字符串的日期转为Date类型的日期
                SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
                Date producedate = sdf.parse(str);

                System.out.print("生产地址：");
                String address = scanner.next();

                // 将上面的信息封装到goods对象中
                Goods goods = new Goods(0, name, price, producedate, address);

                // 调用goodsDao中的添加方法，并传递goods对象
                GoodsDao goodsDao = new GoodsDao();
                goodsDao.addGoods(goods);

                System.out.println("添加成功！");
            }else if(num == 3){ // 商品修改

                System.out.println("请输入要修改的商品的编号：");
                int id = scanner.nextInt();

                System.out.print("商品新名称：");
                String name = scanner.next();
                System.out.print("商品新价格：");
                double price = scanner.nextDouble();
                System.out.print("生产日期(2020-05-05)：");
                String str = scanner.next();

                // 将字符串的日期转为Date类型的日期
                SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
                Date producedate = sdf.parse(str);

                System.out.print("生产地址：");
                String address = scanner.next();

                // 将上面的信息封装到goods对象中
                Goods goods = new Goods(id, name, price, producedate, address);

                // 调用goodsDao中的添加方法，并传递goods对象
                GoodsDao goodsDao = new GoodsDao();
                goodsDao.updateGoods(goods);

                System.out.println("修改成功！");

            }else if(num == 4){ // 商品删除

            }else if(num == 5){ // 退出
                System.out.println("bye bye!");
                return; // 结束整个方法
            }else{
                System.out.println("请输入正确的数字！");
            }
        }
    }
}
```

## 实现商品删除功能

### 编写dao层代码

```java
package com.lhp.dao;

import com.lhp.pojo.Goods;
import com.lhp.utils.JDBCUtils;
import org.apache.commons.dbutils.QueryRunner;
import org.apache.commons.dbutils.handlers.BeanListHandler;

import java.sql.Connection;
import java.sql.SQLException;
import java.util.List;

// 操作goods表
public class GoodsDao {

    // 查询
    public List<Goods> findAll() throws SQLException {

        // 获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 编写sql语句
        String sql = "select * from goods";

        // 创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 调用查询方法
        List<Goods> list = queryRunner.query(connection, sql, new BeanListHandler<>(Goods.class));

        return list;
    }


    // 添加....
    public void addGoods(Goods g) throws SQLException {

        // 获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 编写sql语句
        String sql = "insert into goods values(null, ?, ?, ?, ?)";

        // 创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 调用方法执行sql语句
        queryRunner.update(connection, sql, g.getName(), g.getPrice(), g.getProducedate(), g.getAddress());

        // 关闭连接
        JDBCUtils.closeConnection(connection);
    }

    // 根据id修改商品
    public void updateGoods(Goods g) throws SQLException {

        // 获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 编写sql语句
        String sql = "update goods set name=?, price=?, producedate=?, address=? where id=?";

        // 创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 调用方法执行sql
        queryRunner.update(connection, sql, g.getName(),g.getPrice(),g.getProducedate(),g.getAddress(),g.getId());

        // 关闭连接
        JDBCUtils.closeConnection(connection);
    }

    // 根据id删除
    public void deleteGoods(int id) throws SQLException {
        // 获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 编写sql语句
        String sql = "delete from goods where id=?";

        // 创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 调用方法执行sql
        queryRunner.update(connection, sql, id);

        // 关闭连接
        JDBCUtils.closeConnection(connection);
    }
}
```

### 编写主程序类

```java
package com.lhp;

import com.lhp.dao.GoodsDao;
import com.lhp.pojo.Goods;

import java.sql.SQLException;
import java.text.SimpleDateFormat;
import java.util.Date;
import java.util.List;
import java.util.Scanner;

// 商品管理系统
public class GoodsManage {

    public static void main(String[] args) throws Exception {

        // 创建Scanner对象，用来读取用户在控制台输入的内容
        Scanner scanner = new Scanner(System.in);
        System.out.println("********************欢迎使用商品管理系统**********************");

        while(true){
            System.out.println("请输入操作：1-商品列表展示 2-商品添加 3-商品修改 4-商品删除 5-退出系统");

            // 读取用户输入的操作数字
            int num = scanner.nextInt();

            if(num == 1){ // 商品列表展示
                // 查询goods表中的所有的数据
                GoodsDao goodsDao = new GoodsDao();
                List<Goods> list = goodsDao.findAll();

                System.out.println("商品编号\t\t商品名称\t\t商品价格\t\t生产日期\t\t生产地址");
                for (Goods g : list) { // 增强for循环
                    System.out.println(g.getId() + "\t\t" + g.getName() + "\t\t" +
                            g.getPrice() + "\t\t" + g.getProducedate() + "\t\t" + g.getAddress());
                }

            }else if(num == 2){ // 商品添加
                System.out.print("商品名称：");
                String name = scanner.next();
                System.out.print("商品价格：");
                double price = scanner.nextDouble();
                System.out.print("生产日期(2020-05-05)：");
                String str = scanner.next();

                // 将字符串的日期转为Date类型的日期
                SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
                Date producedate = sdf.parse(str);

                System.out.print("生产地址：");
                String address = scanner.next();

                // 将上面的信息封装到goods对象中
                Goods goods = new Goods(0, name, price, producedate, address);

                // 调用goodsDao中的添加方法，并传递goods对象
                GoodsDao goodsDao = new GoodsDao();
                goodsDao.addGoods(goods);

                System.out.println("添加成功！");
            }else if(num == 3){ // 商品修改

                System.out.println("请输入要修改的商品的编号：");
                int id = scanner.nextInt();

                System.out.print("商品新名称：");
                String name = scanner.next();
                System.out.print("商品新价格：");
                double price = scanner.nextDouble();
                System.out.print("生产日期(2020-05-05)：");
                String str = scanner.next();

                // 将字符串的日期转为Date类型的日期
                SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
                Date producedate = sdf.parse(str);

                System.out.print("生产地址：");
                String address = scanner.next();

                // 将上面的信息封装到goods对象中
                Goods goods = new Goods(id, name, price, producedate, address);

                // 调用goodsDao中的添加方法，并传递goods对象
                GoodsDao goodsDao = new GoodsDao();
                goodsDao.updateGoods(goods);

                System.out.println("修改成功！");

            }else if(num == 4){ // 商品删除

                System.out.print("请输入要删除的商品的编号：");
                int id = scanner.nextInt();

                GoodsDao goodsDao = new GoodsDao();
                goodsDao.deleteGoods(id);

                System.out.println("删除成功！");
            }else if(num == 5){ // 退出
                System.out.println("bye bye!");
                return; // 结束整个方法
            }else{
                System.out.println("请输入正确的数字！");
            }
        }
    }
}
```

## 实现商品条件查询功能

### 编写dao层代码

```java
package com.lhp.dao;

import com.lhp.pojo.Goods;
import com.lhp.utils.JDBCUtils;
import org.apache.commons.dbutils.QueryRunner;
import org.apache.commons.dbutils.handlers.BeanListHandler;

import java.sql.Connection;
import java.sql.SQLException;
import java.util.List;

// 操作goods表
public class GoodsDao {

    // 查询
    public List<Goods> findAll() throws SQLException {

        // 获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 编写sql语句
        String sql = "select * from goods";

        // 创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 调用查询方法
        List<Goods> list = queryRunner.query(connection, sql, new BeanListHandler<>(Goods.class));

        return list;
    }


    // 添加....
    public void addGoods(Goods g) throws SQLException {

        // 获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 编写sql语句
        String sql = "insert into goods values(null, ?, ?, ?, ?)";

        // 创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 调用方法执行sql语句
        queryRunner.update(connection, sql, g.getName(), g.getPrice(), g.getProducedate(), g.getAddress());

        // 关闭连接
        JDBCUtils.closeConnection(connection);
    }

    // 根据id修改商品
    public void updateGoods(Goods g) throws SQLException {

        // 获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 编写sql语句
        String sql = "update goods set name=?, price=?, producedate=?, address=? where id=?";

        // 创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 调用方法执行sql
        queryRunner.update(connection, sql, g.getName(),g.getPrice(),g.getProducedate(),g.getAddress(),g.getId());

        // 关闭连接
        JDBCUtils.closeConnection(connection);
    }

    // 根据id删除
    public void deleteGoods(int id) throws SQLException {
        // 获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 编写sql语句
        String sql = "delete from goods where id=?";

        // 创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 调用方法执行sql
        queryRunner.update(connection, sql, id);

        // 关闭连接
        JDBCUtils.closeConnection(connection);
    }

    // 条件查询
    public List<Goods> findByName(String name) throws SQLException { // 米

        // 获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 编写sql语句
        String sql = "select * from goods where name like ?";

        // 创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 调用方法执行sql语句
        List<Goods> list = queryRunner.query(connection, sql, new BeanListHandler<>(Goods.class), "%" + name + "%");

        // 关闭连接
        JDBCUtils.closeConnection(connection);

        return list;
    }
}
```

### 编写主程序类

```java
package com.lhp;

import com.lhp.dao.GoodsDao;
import com.lhp.pojo.Goods;

import java.sql.SQLException;
import java.text.SimpleDateFormat;
import java.util.Date;
import java.util.List;
import java.util.Scanner;

// 商品管理系统
public class GoodsManage {

    public static void main(String[] args) throws Exception {

        // 创建Scanner对象，用来读取用户在控制台输入的内容
        Scanner scanner = new Scanner(System.in);
        System.out.println("********************欢迎使用商品管理系统**********************");

        while(true){
            System.out.println("请输入操作：1-商品列表展示 2-商品添加 3-商品修改 4-商品删除 5-条件查询 6-退出系统");

            // 读取用户输入的操作数字
            int num = scanner.nextInt();

            if(num == 1){ // 商品列表展示
                // 查询goods表中的所有的数据
                GoodsDao goodsDao = new GoodsDao();
                List<Goods> list = goodsDao.findAll();

                System.out.println("商品编号\t\t商品名称\t\t商品价格\t\t生产日期\t\t生产地址");
                for (Goods g : list) { // 增强for循环
                    System.out.println(g.getId() + "\t\t" + g.getName() + "\t\t" +
                            g.getPrice() + "\t\t" + g.getProducedate() + "\t\t" + g.getAddress());
                }

            }else if(num == 2){ // 商品添加
                System.out.print("商品名称：");
                String name = scanner.next();
                System.out.print("商品价格：");
                double price = scanner.nextDouble();
                System.out.print("生产日期(2020-05-05)：");
                String str = scanner.next();

                // 将字符串的日期转为Date类型的日期
                SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
                Date producedate = sdf.parse(str);

                System.out.print("生产地址：");
                String address = scanner.next();

                // 将上面的信息封装到goods对象中
                Goods goods = new Goods(0, name, price, producedate, address);

                // 调用goodsDao中的添加方法，并传递goods对象
                GoodsDao goodsDao = new GoodsDao();
                goodsDao.addGoods(goods);

                System.out.println("添加成功！");
            }else if(num == 3){ // 商品修改

                System.out.println("请输入要修改的商品的编号：");
                int id = scanner.nextInt();

                System.out.print("商品新名称：");
                String name = scanner.next();
                System.out.print("商品新价格：");
                double price = scanner.nextDouble();
                System.out.print("生产日期(2020-05-05)：");
                String str = scanner.next();

                // 将字符串的日期转为Date类型的日期
                SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
                Date producedate = sdf.parse(str);

                System.out.print("生产地址：");
                String address = scanner.next();

                // 将上面的信息封装到goods对象中
                Goods goods = new Goods(id, name, price, producedate, address);

                // 调用goodsDao中的添加方法，并传递goods对象
                GoodsDao goodsDao = new GoodsDao();
                goodsDao.updateGoods(goods);

                System.out.println("修改成功！");

            }else if(num == 4){ // 商品删除

                System.out.print("请输入要删除的商品的编号：");
                int id = scanner.nextInt();

                GoodsDao goodsDao = new GoodsDao();
                goodsDao.deleteGoods(id);

                System.out.println("删除成功！");
            }else if(num == 5){ // 条件查询

                System.out.print("请输入商品名称(支持模糊查询)：");
                String name = scanner.next();

                GoodsDao goodsDao = new GoodsDao();
                List<Goods> list = goodsDao.findByName(name);

                if(list != null && list.size() > 0){
                    System.out.println("商品编号\t\t商品名称\t\t商品价格\t\t生产日期\t\t生产地址");
                    for (Goods g : list) { // 增强for循环
                        System.out.println(g.getId() + "\t\t" + g.getName() + "\t\t" +
                                g.getPrice() + "\t\t" + g.getProducedate() + "\t\t" + g.getAddress());
                    }
                }else{
                    System.out.println("没有符合条件的商品！");
                }

            } else if(num == 6){ // 退出
                System.out.println("bye bye!");
                return; // 结束整个方法
            }else{
                System.out.println("请输入正确的数字！");
            }
        }
    }
}
```

## 实现登录功能

### 准备用户表

用户表用来存储用户的信息，比如：账号、密码。

![1725327997308-ea993db2-77c6-448e-8a67-47a0be78176e.png](./img/TvMXBSJiS74TOLoG/1725327997308-ea993db2-77c6-448e-8a67-47a0be78176e-549147.png)

### 分析登录业务

1. 系统一旦运行之后，需要让用户输入账号和密码
2. 用户输入账号和密码，我们使用`scanner`去读取用户输入的账号和密码，比如：账号abc、密码123
3. 根据用户输入的账号和密码查询 user 表，如果能够查询到一条数据，说明登录成功，可以继续使用系统
4. 如果查询不到数据，说明登录失败，退出系统！

### 编写实体类

```java
package com.lhp.pojo;

public class User {
    
    private int id;
    private String username;
    private String password;

    public User() {
    }

    public User(int id, String username, String password) {
        this.id = id;
        this.username = username;
        this.password = password;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getUsername() {
        return username;
    }

    public void setUsername(String username) {
        this.username = username;
    }

    public String getPassword() {
        return password;
    }

    public void setPassword(String password) {
        this.password = password;
    }

    @Override
    public String toString() {
        return "User{" +
                "id=" + id +
                ", username='" + username + '\'' +
                ", password='" + password + '\'' +
                '}';
    }
}
```

### 编写dao层代码

```java
package com.lhp.dao;

import com.lhp.pojo.User;
import com.lhp.utils.JDBCUtils;
import org.apache.commons.dbutils.QueryRunner;
import org.apache.commons.dbutils.handlers.BeanHandler;

import java.sql.Connection;
import java.sql.SQLException;

// 操作user表的
public class UserDao {

    // 根据用户名和密码查询数据
    public User findByUsernameAndPassword(String username, String password) throws SQLException {

        // 获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 编写sql语句
        String sql = "select * from user where username=? and password=?";

        // 创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 调用方法执行sql
        User user = queryRunner.query(connection, sql, new BeanHandler<>(User.class), username, password);

        // 关闭连接
        JDBCUtils.closeConnection(connection);

        return user;
    }
}
```

### 编写主程序类

```java
package com.lhp;

import com.lhp.dao.GoodsDao;
import com.lhp.dao.UserDao;
import com.lhp.pojo.Goods;
import com.lhp.pojo.User;

import java.sql.SQLException;
import java.text.SimpleDateFormat;
import java.util.Date;
import java.util.List;
import java.util.Scanner;

// 商品管理系统
public class GoodsManage {

    public static void main(String[] args) throws Exception {

        // 创建Scanner对象，用来读取用户在控制台输入的内容
        Scanner scanner = new Scanner(System.in);

        System.out.print("请输入账号：");
        String username = scanner.next();

        System.out.print("请输入密码：");
        String password = scanner.next();

        UserDao userDao = new UserDao();
        User user = userDao.findByUsernameAndPassword(username, password);

        // 判断user是否有值
        if(user == null){
            System.out.println("账号或密码错误！");
            return; // 结束
        }


        System.out.println("**********************欢迎使用商品管理系统************************");

        while(true){
            System.out.println("请输入操作：1-商品列表展示 2-商品添加 3-商品修改 4-商品删除 5-条件查询 6-退出系统");

            // 读取用户输入的操作数字
            int num = scanner.nextInt();

            if(num == 1){ // 商品列表展示
                // 查询goods表中的所有的数据
                GoodsDao goodsDao = new GoodsDao();
                List<Goods> list = goodsDao.findAll();

                System.out.println("商品编号\t\t商品名称\t\t商品价格\t\t生产日期\t\t生产地址");
                for (Goods g : list) { // 增强for循环
                    System.out.println(g.getId() + "\t\t" + g.getName() + "\t\t" +
                            g.getPrice() + "\t\t" + g.getProducedate() + "\t\t" + g.getAddress());
                }

            }else if(num == 2){ // 商品添加
                System.out.print("商品名称：");
                String name = scanner.next();
                System.out.print("商品价格：");
                double price = scanner.nextDouble();
                System.out.print("生产日期(2020-05-05)：");
                String str = scanner.next();

                // 将字符串的日期转为Date类型的日期
                SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
                Date producedate = sdf.parse(str);

                System.out.print("生产地址：");
                String address = scanner.next();

                // 将上面的信息封装到goods对象中
                Goods goods = new Goods(0, name, price, producedate, address);

                // 调用goodsDao中的添加方法，并传递goods对象
                GoodsDao goodsDao = new GoodsDao();
                goodsDao.addGoods(goods);

                System.out.println("添加成功！");
            }else if(num == 3){ // 商品修改

                System.out.println("请输入要修改的商品的编号：");
                int id = scanner.nextInt();

                System.out.print("商品新名称：");
                String name = scanner.next();
                System.out.print("商品新价格：");
                double price = scanner.nextDouble();
                System.out.print("生产日期(2020-05-05)：");
                String str = scanner.next();

                // 将字符串的日期转为Date类型的日期
                SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
                Date producedate = sdf.parse(str);

                System.out.print("生产地址：");
                String address = scanner.next();

                // 将上面的信息封装到goods对象中
                Goods goods = new Goods(id, name, price, producedate, address);

                // 调用goodsDao中的添加方法，并传递goods对象
                GoodsDao goodsDao = new GoodsDao();
                goodsDao.updateGoods(goods);

                System.out.println("修改成功！");

            }else if(num == 4){ // 商品删除

                System.out.print("请输入要删除的商品的编号：");
                int id = scanner.nextInt();

                GoodsDao goodsDao = new GoodsDao();
                goodsDao.deleteGoods(id);

                System.out.println("删除成功！");
            }else if(num == 5){ // 条件查询

                System.out.print("请输入商品名称(支持模糊查询)：");
                String name = scanner.next();

                GoodsDao goodsDao = new GoodsDao();
                List<Goods> list = goodsDao.findByName(name);

                if(list != null && list.size() > 0){
                    System.out.println("商品编号\t\t商品名称\t\t商品价格\t\t生产日期\t\t生产地址");
                    for (Goods g : list) { // 增强for循环
                        System.out.println(g.getId() + "\t\t" + g.getName() + "\t\t" +
                                g.getPrice() + "\t\t" + g.getProducedate() + "\t\t" + g.getAddress());
                    }
                }else{
                    System.out.println("没有符合条件的商品！");
                }

            } else if(num == 6){ // 退出
                System.out.println("bye bye!");
                return; // 结束整个方法
            }else{
                System.out.println("请输入正确的数字！");
            }
        }
    }
}
```

# HTML

## HTML 简介

Hyper Text Markup Language（超文本标记语言），简写为：HTML。

HTML通过标签来标记要显示的网页中的各个部分。网页文件本身是一种文本文件，通过在文本文件中添加标记符，可以告诉浏览器如何显示其中的内容。（如：文字如何处理，画面如何安排，图片如何显示等）。

## HTML 入门案例

### 创建项目

![1725281094299-21119eb7-11d2-4435-b4ba-ad7083220c2b.png](./img/TvMXBSJiS74TOLoG/1725281094299-21119eb7-11d2-4435-b4ba-ad7083220c2b-175977.png)

![1725281118878-9429a24b-61f7-4e9d-be7c-47312d648d62.png](./img/TvMXBSJiS74TOLoG/1725281118878-9429a24b-61f7-4e9d-be7c-47312d648d62-597667.png)

![1725281136112-dbbdfe0c-78e4-45d5-b21c-dbdb1404a41c.png](./img/TvMXBSJiS74TOLoG/1725281136112-dbbdfe0c-78e4-45d5-b21c-dbdb1404a41c-620391.png)

### 创建HTML文件

![1725281184071-547dbdbe-d425-405f-80a8-5160accfff33.png](./img/TvMXBSJiS74TOLoG/1725281184071-547dbdbe-d425-405f-80a8-5160accfff33-091463.png)

![1725281195611-ec1e123a-bf28-4e8b-ad73-d71df0453fea.png](./img/TvMXBSJiS74TOLoG/1725281195611-ec1e123a-bf28-4e8b-ad73-d71df0453fea-813182.png)

### 编写内容

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>我是标题</title>
</head>
<body>
    <h1>大家好~</h1>
</body>
</html>
```

### 运行

![1725281263294-af18aef4-14e9-4a19-92b5-e17712fa3823.png](./img/TvMXBSJiS74TOLoG/1725281263294-af18aef4-14e9-4a19-92b5-e17712fa3823-340185.png)

![1725281275177-152bd5f0-4e78-4cb2-a78b-ad3768ff6632.png](./img/TvMXBSJiS74TOLoG/1725281275177-152bd5f0-4e78-4cb2-a78b-ad3768ff6632-208672.png)

## HTML 标签介绍

* 标签的格式：`<标签名>数据</标签名>`
* 标签名大小写不敏感
* 标签拥有自己的属性
  * 基本属性：`bgcolor="red"`					可以简单修改样式效果
  * 事件属性：`onclick="alert('学习使我快乐！')"`	可以直接设置事件响应后的代码
* 标签又分为：单标签和双标签
  * 单标签格式：<标签名/>		比如：br、hr
  * 双标签格式：<标签名>数据\</标签名>		比如：title、h

## 常用标签

### **<font style="color:rgb(0,0,0);">标题标签</font>**

需求：在页面演示标题1到标题6

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>标题标签</title>
</head>
<body>

    <!--需求：在页面演示标题1到标题6-->
    <!--
        h1 - h6 都是标题标签
        h1最大
        h6最小
        align属性是对齐属性：
            left：左对齐(默认)
            center：居中
            right：右对齐
    -->
    <h1 align="left">标题1</h1>
    <h2 align="center">标题2</h2>
    <h3 align="right">标题3</h3>
    <h4>标题4</h4>
    <h5>标题5</h5>
    <h6>标题6</h6>
    <h7>标题7</h7>
</body>
</html>
```

### **<font style="color:rgb(0,0,0);">超链接标签</font>**

超链接：点击网页中能跳转的基本就是超链接。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>超链接标签</title>
</head>
<body>

    <!--
        a标签是超链接标签
          href属性可以设置跳转的路径
          target属性设置以什么方式跳转
              _self   在当前窗口中跳转，默认
              _blank  在新窗口中跳转
    -->
    <a href="https://www.baidu.com">百度</a><br/>
    <a href="https://www.baidu.com" target="_self">百度</a><br/>
    <a href="https://www.baidu.com" target="_blank">百度</a>

</body>
</html>
```

### 列表标签

使用无序列表的方式把中国古代四大美女展示出来

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>列表标签</title>
</head>
<body>

    <!--使用无序列表的方式把中国古代四大美女展示出来。-->
    <!--
        ul是无序列表
            type属性可以修改列表前面的符号
        li是列表项
        
        ol是有序列表
    -->
    <ul>
        <li>西施</li>
        <li>王昭君</li>
        <li>貂蝉</li>
        <li>杨玉环</li>
    </ul>
    <ol>
        <li>西施</li>
        <li>王昭君</li>
        <li>貂蝉</li>
        <li>杨玉环</li>
    </ol>
</body>
</html>
```

### img标签

使用img标签来显示一张图片，并修改宽高和边框属性。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>图片标签</title>
</head>
<body>

    <!--使用img标签来显示一张图片，并修改宽高和边框属性。-->
    <!--
        img标签是图片标签，用来显示图片
            src属性可以设置图片的路径
            width属性设置图片的宽度
            height属性设置图片的高度
            border属性设置图片边框的大小
            alt属性设置图片找不到时的提示文字

        在JavaSE中路径也分为相对路径和绝对路径
            相对路径：从工程名开始算
            绝对路径：盘符:/目录/文件名

        在web中路径分为相对路径和绝对路径
            相对路径：
                .       表示当前文件所在的目录
                ..      表示当前文件所在的上一级目录
                文件名   表示当前文件所在目录的文件，相当于 ./文件名   ./可以省略

             绝对路径：
                正确格式是：http://ip:port/工程名/资源路径
                错误格式是：盘符:/目录/文件名
    -->

    <img src="../imgs/01.jpg" width="200" height="300" border="1" alt="图片找不到"/>
    <img src="../imgs/02.jpg" width="200" height="300"/>
    <img src="../imgs/03.jpg" width="200" height="300"/>

</body>
</html>
```

### table标签

需求1：做一个带表头的，三行、三列的表格，并显示边框

需求2：修改表格的宽度、高度，表格的对齐方式，单元格间距

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>

    <!--
        需求1：做一个带表头的，三行、三列的表格，并显示边框
        需求2：修改表格的宽度、高度，表格的对齐方式，单元格间距

        table 表格标签
            border属性设置表格边框
            width属性设置表格宽度
            height属性设置表格高度
            align属性设置表格在页面中的对齐方式
            cellspacing属性设置单元格间距
        tr 行标签
        th 表头标签
        td 单元格标签
            align 设置单元格文本对齐方式

        b 加粗标签
    -->

    <table align="center" border="1" width="300" height="300" cellspacing="0">
        <tr>
            <td>1.1</td>
            <td>1.2</td>
            <td>1.3</td>
        </tr>
        <tr>
            <td>2.1</td>
            <td>2.2</td>
            <td>2.3</td>
        </tr>
        <tr>
            <td>3.1</td>
            <td>3.2</td>
            <td>3.3</td>
        </tr>
    </table>

</body>
</html>
```

### 表单标签

表单就是HTML页面中用来收集用户信息的所有元素集合，然后把这些信息发送给服务器。

需求：创建一个人人网信息注册的表单界面。包含用户名，密码，确认密码。性别（单选），兴趣爱好（多选），国籍（下拉列表）。隐藏域，自我评价（多行文本域）。重置，提交。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>form表单标签</title>
</head>
<body>

    <!--
        创建一个人人网信息注册的表单界面。包含用户名，密码，确认密码。
        性别（单选），兴趣爱好（多选），国籍（下拉列表）。隐藏域，自我评价（多行文本域）。重置，提交。

        form标签就是表单
            input type=text     是文本输入框  value设置默认显示内容
            input type=password 是密码输入框  value设置默认显示内容
            input type=radio    是单选框      name属性可以对其进行分组    checked="checked"表示默认选中
            input type=checked  是复选框     checked="checked"表示默认选中
            input type=reset    是重置按钮   value属性可以修改按钮上的文本
            input type=submit   是提交按钮   value属性可以修改按钮上的文本
            input type=buttom   是普通按钮   value属性可以修改按钮上的文本
            input type=file     是文件输入框，在上传文件时使用
            input type=hidden   是隐藏域，当我们需要发送给服务器某些信息，而这些信息不需要用户参与，就可以将其隐藏

            select标签是下拉列表框
            option标签是下拉列表框中的选项 selected="selected"设置默认选中

            textarea表示多行文本输入框（起始标签和结束标签中的内容是默认值）
                rows 属性可以设置显示几行的高度
                cols 属性可以设置每行显示几个字符宽度
    -->
    <form>
        用户名称：<input type="text" value="默认值" /><br>
        用户密码：<input type="password" value="abc"><br>
        确认密码：<input type="password" value="abc"><br>
        性别：<input type="radio" name="sex" checked="checked">男<input type="radio" name="sex">女 <br>
        兴趣爱好：<input type="checkbox" checked="checked">Java <input type="checkbox">JavaScript <input type="checkbox">HTML
        <br>
        国籍：<select>
                <option>---请选择---</option>
                <option selected="selected">中国</option>
                <option>美国</option>
                <option>日本</option>
            </select><br>
        自我评价：<textarea cols="20" rows="10">我是默认值</textarea><br>
        <input type="reset" value="重置按钮"><br>
        <input type="submit" value="提交按钮"><br>
        <input type="button" value="我是button按钮"><br>

        <input type="file"><br>
        <input type="hidden" name="name" value="123"><br>
    </form>

</body>
</html>
```

### 表单提交细节

* form标签是表单标签
  * action属性设置提交的服务器地址
  * method属性设置提交的方式：get（默认）或post
* 表单提交的时候，数据没有发送给服务器的三种情况：
  * 表单项没有name属性值
  * 单选、复选、下拉列表中的option标签都需要添加value属性，以便发送给服务器
  * 表单项不在提交的form标签中
* get请求的特点是：
  * 浏览器地址栏中的地址是：action属性+?+请求参数
  * 请求参数的格式是：name=value\&name=value
  * 不安全
  * 它有数据长度的限制
* post请求的特点是：
  * 浏览器地址栏中只有action属性值
  * 相对于get请求要安全
  * 理论上没有数据长度的限制

### 其他标签div、span、p

需求：div、span、p标签的演示。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>其他标签</title>
</head>
<body>

    <!--需求：div、span、p标签的演示。-->
    <!--
        div标签       默认独占一整行
        span标签      它的长度是数据的长度
        p段落标签       默认会在段落上方或下方各空出一行来（如果已有就不再空）
    -->

    <div>div标签1</div>
    <div>div标签2</div>
    <span>span标签1</span>
    <span>span标签2</span>
    <p>p标签1</p>
    <p>p标签2</p>
</body>
</html>
```

# CSS

网页都是由三部分组成：

* 结构(html)：页面中的内容，比如：输入框、标题、按钮
* 表现(css)：页面中字体大小、颜色、背景
* 行为(js)：页面中可以与用户进行交互

## CSS 概述

CSS是层叠样式表，是用于（增强）控制网页样式并允许将样式信息与网页内容分离的一种标记性语言。

## CSS 语法介绍

**语法规则：**

![1725355365164-b4da06e3-6cef-4892-a873-c921bad572c1.png](./img/TvMXBSJiS74TOLoG/1725355365164-b4da06e3-6cef-4892-a873-c921bad572c1-718474.png)

\*\*选择器：\*\*浏览器根据“选择器”决定受CSS样式影响的HTML元素（标签）

\*\*属性：\*\*是你要改变的样式名，并且每个属性都有一个值。属性和值被冒号分开，并由大括号包围，这样就组成了一个完整的样式声明，例如：p{color:blue}

\*\*多个声明：\*\*如果要定义不止一个声明，则需要用分号将每个声明分开。虽然最后一条声明的最后可以不加分号（但尽量在每条声明的末尾都加上分号）

**例如：**

```css
p{
    color:red;
    font-size:30px;
}
```

注：一般每行只描述一个属性。

**CSS注释：/*注释内容*/**

## CSS 的使用方式

### 第一种使用方式

在标签的style属性上设置“key:value;key2:value2”，修改标签样式。

需求1：分别定义两个div、span标签，分别修改每个div标签的样式为：边框1个像素，实线，红色。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>

    <!--分别定义两个div、span标签，分别修改每个div标签的样式为：边框1个像素，实线，红色。-->
    <div style="border: 1px solid red;">div标签1</div>
    <div style="border: 1px solid red;">div标签2</div>
    <span style="border: 1px solid red;">span标签1</span>
    <span style="border: 1px solid red;">span标签2</span>
</body>
</html>
```

**问题：这种方式的缺点？**

1. 如果标签多了，样式多了，代码量非常庞大！

2. 可读性非常差

css代码没什么复用性可言

### 第二种使用方式

在head标签中，使用style标签来定义各种自己需要的css样式。

格式如下：

```css
xxx {
    样式名:样式值;
    样式名2:样式值2;
}
```

需求1：分别定义两个div、span标签，分别修改每个div标签的样式为：边框1个像素，实线，红色。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>

    <!--style标签专门用来定义css样式代码-->
    <style>

        /*分别定义两个div、span标签，分别修改每个div标签的样式为：边框1个像素，实线，红色。*/
        div{
            border:1px solid red;
        }

        span{
            border:1px solid red;
        }
    </style>

</head>
<body>

    <div>div标签1</div>
    <div>div标签2</div>
    <span>span标签1</span>
    <span>span标签2</span>
</body>
</html>
```

\*\*问题：\*\*这种方式的缺点？

1. 只能在同一页面内复用代码，不能在多个页面中复用css代码

2. 维护起来不方便，实际的项目中会有成千上万的页面，要到每个页面中去修改，工作量太大了

### 第三种使用方式

把CSS样式写成一个单独的css文件，再通过link标签引入即可复用。

使用HTML的<link rel="stylesheet" href="xxx.css">引入。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>

    <!--link标签专门用来引入css样式代码-->
    <link rel="stylesheet" href="../css/01-style.css">
</head>
<body>

    <!--分别定义两个div、span标签，分别修改每个div标签的样式为：边框1个像素，实线，红色。-->
    <div>div标签1</div>
    <div>div标签2</div>
    <span>span标签1</span>
    <span>span标签2</span>
</body>
</html>
```

```css
div{
    border: 1px solid blue;
}

span{
    border: 1px solid red;
}
```

## 选择器

选择器：就是你要给页面中哪些元素设置样式！

### 标签选择器

标签选择器的格式是：

```css
标签{
	样式名：样式值;
}
```

标签选择器，可以将页面中的所有的该标签都选中，使用设置的这个样式。

\*\*需求：\*\*在所有div标签上修改字体颜色为蓝色，大小为30个像素。边框为1像素黄色实线。

并且修改所有span标签的字体颜色为黄色，字体大小为20个像素，边框为5像素蓝色虚线。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>标签名选择器</title>

    <style>
        div{
            color: blue;
            font-size: 30px;
            border: 1px solid yellow;
        }
        span{
            color: yellow;
            font-size: 20px;
            border: 5px dashed blue;
        }
    </style>

</head>
<body>

    <!--
        在所有div标签上修改字体颜色为蓝色，大小为30个像素。边框为1像素黄色实线。
        并且修改所有span标签的字体颜色为黄色，字体大小为20个像素，边框为5像素蓝色虚线。

    -->
    <div>div标签1</div>
    <div>div标签2</div>
    <span>span标签1</span>
    <span>span标签2</span>

</body>
</html>
```

### id 选择器

id选择器的格式是：

```css
#id属性值{
  样式名:样式值;
}
```

id选择器，可以让我们通过id属性去选择标签使用这个样式。

说明：在一个页面中id是唯一的！

\*\*需求：\*\*分别定义两个div标签，第一个div标签定义为id为id001，然后根据id属性定义css样式修改字体颜色为蓝色，字体大小为30像素，边框为1像素黄色实线。

第二个div标签定义为id为id002，然后根据id属性定义css样式，修改字体颜色为红色，字体大小为20个像素，边框为5像素蓝色点线。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>id选择器</title>

    <style>
        #id001{
            color: blue;
            font-size: 30px;
            border: 1px solid yellow;
        }
        
        #id002{
            color: red;
            font-size: 20px;
            border: 5px dotted blue;
        }

    </style>

</head>
<body>

    <!--
        分别定义两个div标签，第一个div标签定义为id为id001，
        然后根据id属性定义css样式修改字体颜色为蓝色，字体大小为30像素，边框为1像素黄色实线。
        第二个div标签定义为id为id002，然后根据id属性定义css样式，
        修改字体颜色为红色，字体大小为20个像素，边框为5像素蓝色点线。

    -->
    <div id="id001">div标签1</div>
    <div id="id002">div标签2</div>

</body>
</html>
```

### class 选择器

class选择器的格式是：

```css
.class属性值{
	样式名:样式值;
}
```

class选择器，可以给所有相同class值的标签设置同样的样式。

说明：标签的class值是可以重复的，也就是多个标签可以有相同的class值。

需求1：修改class属性值为class01的span或div标签，字体颜色为蓝色，字体大小为30像素，边框为1像素黄色实线。

需求2：修改class属性值为class02的div标签，字体颜色为灰色，字体大小为26像素，边框为1像素红色实线。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>class选择器</title>

    <style type="text/css">
        .class01{
            color: blue;
            font-size: 30px;
            border: 1px solid yellow;
        }

        .class02{
            color: grey;
            font-size: 26px;
            border: 1px solid red;
        }

    </style>
</head>
<body>

    <!--
        需求1：修改class属性值为class01的span或div标签，字体颜色为蓝色，字体大小为30像素，边框为1像素黄色实线。
        需求2：修改class属性值为class02的div标签，字体颜色为灰色，字体大小为26像素，边框为1像素红色实线。
    -->
    <div class="class01">div标签class01</div>
    <div class="class02">div标签class02</div>
    <span class="class01">span标签class01</span>
    <span>span标签</span>

</body>
</html>
```

### 组合选择器

组合选择器的格式是：

```css
选择器1，选择器2，选择器n{
	样式名:样式值;
}
```

组合选择器可以让多个选择器共用同样的样式代码！

需求：修改`class="class01"`的标签和`id="id01"`的标签，字体颜色为蓝色，字体大小为20像素，边框为1像素黄色实线。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>组合选择器</title>
    <style>
        .class01, #id01{
            color: blue;
            font-size: 20px;
            border: 1px solid yellow;
        }
    </style>
</head>
<body>

    <!--
        需求：修改class=”class01”的标签和id=”id01”的标签，字体颜色为蓝色，字体大小为20像素，边框为1像素黄色实线。
    -->
    <div class="class01">div标签class01</div>
    <span id="id01">span标签id01</span><br>
    <div>标签</div>
    <div>div标签</div>
</body>
</html>
```

## CSS 常用样式

* 字体颜色：
  * color：red；
  * 颜色可以写颜色名，如：black、blue、green、yellow等
  * 颜色也可以写rgb值和16进制值，比如：rgb(165,213,155)，#09AB21
* 宽度：
  * width：19px；
  * 宽度值可以写像素值：19px
  * 也可以写百分比值：20%
* 高度：
  * height：20px；
  * 宽度值可以写像素值：20px
  * 也可以写百分比值：20%
* 背景颜色：
  * background-color：#bfa;
* 字体大小：
  * font-size：30px；
* 边框：
  * border：1px solid red；
* 元素居中：
  * margin-left：auto；
  * margin-right：auto；
* 文本居中：
  * text-align：center；
* 去掉超链接下划线：
  * text-decoration：none；
* 表格相关

```css
table{
		border:1px solid red;
		border-collapse:collapse;
}
td,th{
		border:1px solid red;
}
```

* 列表样式：

```css
ul{
		list-style:none;
}
```

\*\*案例： \*\*

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>常用样式</title>

    <style>
        div{
            color: red;
            border: 1px solid blue;
            width: 300px;
            height: 300px;
            background-color: #bfa;
            font-size: 30px;

            margin-left: auto;
            margin-right: auto;

            text-align: center;
        }

        a{
            text-decoration: none;
        }

        table{
            border: 1px solid red;
            border-collapse: collapse;
        }

        td{
            border: 1px solid red;
        }

        ul{
            list-style: none;
        }
    </style>
</head>
<body>
    <ul>
        <li>张三</li>
        <li>李四</li>
        <li>王五</li>
    </ul>

    <table>
        <tr>
            <td>1.1</td>
            <td>1.2</td>
        </tr>
        <tr>
            <td>2.1</td>
            <td>2.2</td>
        </tr>
    </table>

    <a href="https://www.baidu.com">百度一下</a>

    <div>我是div标签</div>

</body>
</html>
```

## 登录案例

# JavaScript

## JS 介绍

* JavaScript语言诞生主要是完成页面的数据验证。因此它运行在客户端，需要运行浏览器来解析执行JavaScript代码。JS是Netscape网景公司的产品，最早取名为LiveScript，为了吸引更多Java程序员，更名为JavaScript，简称JS。
* JS是弱类型，Java是强类型。
  * JS中：`var i = 3; i = "abc";`
  * Java中：`int a = 5; a = 15;`
* 特点：
  * 交互性：它可以做的就是信息的动态交互
  * 安全性：不允许直接访问本地硬盘
  * 跨平台性：只要是可以解释JS的浏览器都可以执行，和平台无关

## JS 的使用方式

### 第一种使用方式

只需要在head标签或者body标签中，使用script标签来书写JS代码。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>


    <script type="text/javascript">
        //alert是JS语言提供的一个警告框函数
        //它可以接收任意类型的参数，这个参数就是警告框的提示信息
        alert("hello JS!");
    </script>
</head>
<body>

</body>
</html>
```

### 第二种使用方式

在单独的JS文件中编写JS代码，然后在HTML页面中使用script标签引入该文件。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>

    <!--使用script标签来引入外部的js文件，scr属性用来设置js文件的路径（绝对路径或相对路径）-->
    <!--script标签可以用定义js代码，也可以用来引入js文件。但是两个功能二选一，不能同时做这两件事。-->
    <script type="text/javascript" src="abc.js"></script>

    <!--以下写法是错误的！-->
    <!--<script type="text/javascript" src="abc.js">-->
        <!--alert("hehehehehe");-->
    <!--</script>-->

</head>
<body>

</body>
</html>
```

## JS 的变量

什么是变量？变量是可以存放某些值的内存的命名。

JS的变量类型：

* 数值类型		number
* 字符串类型	string
* 对象类型		object
* 布尔类型		boolean
* 函数类型		function

JS中的变量定义格式：

var 变量名;

var 变量名= 值;

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>变量</title>

    <script>

        var i;
        alert(i);//undefined
        i = 12;

        i = "abc";

        var a = 12;
        var b = "abc";
    </script>

</head>
<body>

</body>
</html>
```

## 函数的定义

### 函数的第一种定义方式

函数的定义方式有两种。

第一种，可以使用function关键字来定义函数，格式如下：

```javascript
function 函数名(形参列表){
	函数体;
}
```

在JS中如何定义带有返回值的函数呢？

只需要在函数体内直接使用return语句返回值即可。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>函数</title>

    <script>

        //定义一个无参函数
        function fun(){
            alert("无参函数fun()被调用了...");
        }

        //调用函数
        fun();

        //定义一个有参函数
        function fun2(a, b){
            alert("有参函数fun2()被调用了... a = " + a + ", b = " + b);
        }

        fun2(12, "abc");

        //定义带有返回值的函数
        function sum(num1, num2){
            var result = num1 + num2;
            return result;
        }

        alert(sum(12, 25));

    </script>
</head>
<body>

</body>
</html>
```

### 函数的第二种定义方式

函数的第二种定义方式，格式如下：

var 函数名= function(形参列表){函数体}

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>函数的第二种定义方式</title>

    <script>
        
        var fun1 = function () {
            alert("无参函数。。。");
        }

        fun1();

        var fun2 = function(a, b){
            alert("有参函数，a = " + a + ", b = " + b);
        }

        fun2(1, 3);

        var fun3 = function(num1, num2){
            return num1 + num2;
        }

        alert(fun3(12, 20));
        
    </script>
</head>
<body>

</body>
</html>
```

## JS 中的事件

### 事件介绍

什么是事件？事件是电脑输入设备与页面进行交互的响应。

常用的事件：

* onload加载完成事件。页面加载完成之后，常用于做js代码初始化操作。
* onclick鼠标单击事件。常用于按钮的点击响应操作。
* onblur失去焦点事件。常用于输入框失去焦点后验证其输入内容是否合法。
* onchange内容发生改变事件。常用于下拉列表和输入框内容发生改变后操作。
* onsubmit表单提交事件。常用于表单提交前，验证所有表单项是否合法。

### 事件的注册

什么是事件的注册（绑定）？

其实就是告诉浏览器，当事件响应后要执行哪些操作代码，叫事件注册或事件绑定。

事件的注册分为两种：

**静态注册事件**：通过HTML标签的事件属性直接赋予事件响应后的代码，这种方式叫静态注册。

**动态注册事件**：是指先通过js代码得到标签的dom对象，然后再通过dom对象.事件名 = function(){ }这种形式赋予事件响应后的代码，叫做动态注册。

动态注册基本步骤：

1. 获取标签对象

2. 标签对象.事件名 = function(){ }

### onload事件

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>

    <script type="text/javascript">

        function onloadFun(){
            alert(789);
        }

        //动态注册onload事件,这个是固定写法
        window.onload = function(){
            alert(987);
        }

    </script>
</head>
<!--
    静态注册onload事件的方式，onload事件是页面加载完成后自动执行的
-->
<!--<body onload="alert(123); alert(456)">-->
<!--<body onload="onloadFun();">-->

<body>

</body>
</html>
```

### onclick 事件

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>

    <script type="text/javascript">

        function fun1(){
            alert(111);
        }

        //页面加载完成后自动做的事情
        window.onload = function(){

            //根据元素的id获取元素，既然是根据元素id获取元素，那就得保证这行代码得是在页面元素加载完成才能执行
            //所以我们把这些方法写在onload中
            var btn = document.getElementById("btn2");
            // alert(btn);

            //动态注册onclick事件
            btn.onclick = function(){
                alert(222);
            }
        }
    </script>

</head>
<body>

    <!--静态注册onclick事件-->
    <button onclick="fun1()">按钮1</button>
    <button id="btn2">按钮2</button>

</body>
</html>
```

### onblur 事件

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>

    <script type="text/javascript">

        function fun1(){
            console.log(123);
        }

        window.onload = function(){
            var p = document.getElementById("password");

            //动态注册onblur事件
            p.onblur = function(){
                console.log(456)
            }
        }
    </script>

</head>
<body>
    <!--静态注册onblur事件-->
    账号：<input type="text" onblur="fun1()"><br>
    密码：<input type="password" id="password">

</body>
</html>
```

### onchange事件

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>

    <script type="text/javascript">

        function fun1(){
            alert("女神被改变了！");
        }

        window.onload = function(){
            var s1 = document.getElementById("s1");
            s1.onchange = function(){
                alert("女神被改变了！");
            }
        }
    </script>
</head>
<body>

    请选择你心目中的女神：
    <!--静态注册内容改变事件-->
    <select onchange="fun1();">
        <option>---请选择---</option>
        <option>柳岩</option>
        <option>景甜</option>
        <option>智恩</option>
    </select>

    <!--动态注册内容改变事件-->
    <select id="s1">
        <option>---请选择---</option>
        <option>柳岩</option>
        <option>景甜</option>
        <option>智恩</option>
    </select>
</body>
</html>
```

### onsubmit 事件

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>

    <script type="text/javascript">

        function fun1(){
            alert("表单要提交了，现在进行表单项的验证! 验证不通过！");
            return false; //这里返回true，表示表单可以提交，返回false表示表单不能提交了。
        }

        window.onload = function(){
            var form = document.getElementById("form");
            form.onsubmit = function(){
                alert("表单要提交了，现在进行表单项的验证! 验证不通过！");
                return false;
            }
        }

    </script>

</head>
<body>

    <!--静态注册表单提交事件-->
    <form action="http://localhost:8080" method="get" onsubmit="return fun1()">

        <input type="submit" value="提交">

    </form>

    <!--动态注册表单提交事件-->
    <form action="http://localhost:8080" method="get" id="form">
        <input type="submit">
    </form>

</body>
</html>
```

# Tomcat 服务器

## JavaWeb 相关概念

* **什么是JavaWeb**

JavaWeb是指，所有通过Java语言编写的可以通过浏览器访问的程序的总称。JavaWeb是基于请求和响应来开发的。

* **什么是请求(Request)**

请求是指客户端给服务器发送数据

* **什么是响应(Response)**

响应是指服务器给客户端回传数据

* **请求和响应的关系**

请求和响应是成对出现的，有请求就有响应

![1725442332412-0fed80d1-26f9-4d20-9ee2-6c3530670717.png](./img/TvMXBSJiS74TOLoG/1725442332412-0fed80d1-26f9-4d20-9ee2-6c3530670717-537150.png)

## Web资源的分类

Web资源按实现的技术和呈现的效果的不同，可以分为静态资源和动态资源两种。

* 静态资源：HTML、CSS、JS、txt、mp4视频、jpg图片等
* 动态资源：jsp页面、Servlet程序等

## 常见的Web服务器

* \*\*<font style="background-color:#FBDE28;">Tomcat</font>\*\*\*\*：\*\*由Apache组织提供的一种Web服务器，提供对jsp和Servlet的支持。它是一种轻量级的JavaWeb容器（服务器），也是当前应用最广的JavaWeb服务器（免费）
* Jboss：是一个遵从JavaEE规范的、开源的、纯Java的EJB服务器，它支持所有的JavaEE规范（免费）
* GlassFish：由Oracle公司开发的一款JavaWeb服务器，是一款强健的商业服务器，达到产品级质量（应用很少）
* Resin：是CAUCHO公司的产品，是一个非常流行的服务器，对Servlet和jsp提供了良好的支持，性能也比较优良，resin自身采用Java语言开发（收费，应用比较多）
* Weblogic：是Oracle公司的产品，是目前应用最广泛的Web服务器，支持JavaEE规范。而且不断完善以适应新的开发要求，适合大型项目（收费，用的不多，适合大公司）

## Tomcat 服务器的安装

解压资料中提供的 apache-tomcat-8.5.31.zip 压缩包即可。

![1725442665100-136dc951-110e-41a5-81e0-c997aef83f8e.png](./img/TvMXBSJiS74TOLoG/1725442665100-136dc951-110e-41a5-81e0-c997aef83f8e-791851.png)

1. bin：	用来存放Tomcat服务器的可执行程序

2. conf：	用来存放Tomcat服务器的配置文件

3. lib：	用来存放Tomcat服务器的jar包

4. logs：	用来存放Tomcat服务器运行时输出的日志信息

5. temp：	用来存放Tomcat服务器运行时产生的临时数据

6. webapps：用来存放Tomcat服务器部署的工程

7. work：	是Tomcat工作时的目录，用来存放Tomcat运行时jsp翻译为Servlet的源码和Session钝化的目录（钝化和序列化一个意思）

## IDEA 整合 Tomcat 服务器

![1725442782142-0495804f-0e56-40fa-ad80-23c07b16f8ca.png](./img/TvMXBSJiS74TOLoG/1725442782142-0495804f-0e56-40fa-ad80-23c07b16f8ca-731112.png)

![1725442867987-50428897-53d7-469c-9ea7-6bfc80af3948.png](./img/TvMXBSJiS74TOLoG/1725442867987-50428897-53d7-469c-9ea7-6bfc80af3948-969491.png)

![1725442930495-b3d4b93b-d65d-4306-b1c1-7b4adcd0b884.png](./img/TvMXBSJiS74TOLoG/1725442930495-b3d4b93b-d65d-4306-b1c1-7b4adcd0b884-507221.png)

然后一路点击OK。

## 测试IDEA整合Tomcat是否成功

![1725442992742-7e14d15e-fc9a-4235-913e-679ae6f477fa.png](./img/TvMXBSJiS74TOLoG/1725442992742-7e14d15e-fc9a-4235-913e-679ae6f477fa-732045.png)

![1725443047855-03e979f9-cca6-4d0c-91af-57bbdc63e77f.png](./img/TvMXBSJiS74TOLoG/1725443047855-03e979f9-cca6-4d0c-91af-57bbdc63e77f-736189.png)

# Servlet

## 什么是 Servlet

* Servlet是JavaEE规范之一，规范就是接口
* Servlet是JavaWeb三大组件之一，三大组件分别是：Servlet程序，Filter过滤器，Listener监听器
* Servlet是运行在服务器上的一个Java小程序，它可以接收客户端发送过来的请求，并响应数据给客户端

## Servlet 入门案例

### 创建项目

以后我们创建的都是 Java Enterprise 项目。

![1725443152260-d04799f9-86b5-4dae-b15f-e6dfe2ea92bc.png](./img/TvMXBSJiS74TOLoG/1725443152260-d04799f9-86b5-4dae-b15f-e6dfe2ea92bc-278196.png)

![1725443368955-aba2d40c-ef9f-4f1b-a776-46b228a83f47.png](./img/TvMXBSJiS74TOLoG/1725443368955-aba2d40c-ef9f-4f1b-a776-46b228a83f47-841328.png)

![1725443216716-81c8e2fe-7021-4ca5-ae9a-a2a781569c7a.png](./img/TvMXBSJiS74TOLoG/1725443216716-81c8e2fe-7021-4ca5-ae9a-a2a781569c7a-308408.png)

![1725443247270-9dc7dfaf-ea14-4098-a07b-5232a386da22.png](./img/TvMXBSJiS74TOLoG/1725443247270-9dc7dfaf-ea14-4098-a07b-5232a386da22-856724.png)

![1725443399659-8092dea1-dca0-4aca-a0cb-25fdb1b5b9e8.png](./img/TvMXBSJiS74TOLoG/1725443399659-8092dea1-dca0-4aca-a0cb-25fdb1b5b9e8-313127.png)

### 编写Servlet类

```java
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;

// 1. 编写一个类，继承HttpServlet类
@WebServlet("/hello") // 3. 编写Servlet的访问路径，必须是 / 开头！
public class HelloServlet extends HttpServlet {
    
    // 2. 重写父类中的service方法，里面写自己的代码
    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        System.out.println("hello...");
        
        // 给浏览器响应一句话
        resp.getWriter().write("hello world!!!");
    }
}
```

### 启动项目并访问

![1725443624764-734e3dc8-ba6e-4687-85d1-7356acaa41ba.png](./img/TvMXBSJiS74TOLoG/1725443624764-734e3dc8-ba6e-4687-85d1-7356acaa41ba-985955.png)

![1725443719679-0691f136-c507-44e6-b48f-3d40d7893dc3.png](./img/TvMXBSJiS74TOLoG/1725443719679-0691f136-c507-44e6-b48f-3d40d7893dc3-164642.png)

## 入门案例总结

编写Servlet的步骤：

1. 编写一个类继承 HttpServlet
2. 重写service方法
3. 标注注解

## HttpServletRequest类的介绍

每次只要有请求进入Tomcat服务器，Tomcat服务器就会把请求过来的http协议信息解析好封装到Request对象中，然后传递到service方法（doGet和doPost）中给我们使用。我们可以通过HttpServletRequest对象获取到所有请求的信息。

## **<font style="color:rgb(0,0,0);">HttpServletRequest类常用方法</font>**

* **getParameter()			获取请求的参数**
* getParameterValues()		获取请求的参数（多个值的时候使用）
* **setAttribute(key, value)	设置域数据 (HttpServletRequest也是一个域对象)**
* **getAttribute(key)			获取域数据**
* getRequestDispatch()		获取请求转发对象

## **<font style="color:rgb(0,0,0);">获取请求的参数值</font>**

### 编写Servlet

```java
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;

@WebServlet("/demo1")
public class Demo1Servlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        // 接收本次请求中的账号和密码
        String username = req.getParameter("username");
        String password = req.getParameter("password");

        if(username.equals("zs") && password.equals("123")){
            resp.getWriter().write("login success！");
        }else{
            resp.getWriter().write("username or password is error！");
        }
    }
}
```

### 编写html页面

```html
<html>
<head>
    <title>$Title$</title>
</head>
<body>

<form action="demo1" method="post">
    账号：<input type="text" name="username"><br>
    密码：<input type="password" name="password"><br>
    <input type="submit" value="登录">
</form>

</body>
</html>
```

## 解决POST请求中文乱码的问题

```java
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;

@WebServlet("/demo1")
public class Demo1Servlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        // 解决post请求中文乱码问题
        req.setCharacterEncoding("utf-8");

        String username = req.getParameter("username");
        String password = req.getParameter("password");

        System.out.println("username:" + username);
        System.out.println("password:" + password);
    }
}
```

## 请求转发

![1725458748781-6360ec0b-9283-440b-bcd8-5b07294a3db1.png](./img/TvMXBSJiS74TOLoG/1725458748781-6360ec0b-9283-440b-bcd8-5b07294a3db1-924302.png)

**<font style="background-color:rgb(255,255,0);">请求转发的特点：</font>**

1. 浏览器地址栏没有变化，还是在第一次访问的Servlet那里

2. 它们是一次请求

3. 它们共享Request域中的数据

4. 可以转发到WEB-INF目录下

5. 不可以转发到工程以外的资源

```java
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;

@WebServlet("/demo2")
public class Demo2Servlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        System.out.println("demo2被访问！");
        
        // 往请求中放数据
        req.setAttribute("age", 20);
        // 转发到demo3
        req.getRequestDispatcher("/demo3").forward(req, resp);
    }
}
```

```java
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;

@WebServlet("/demo3")
public class Demo3Servlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        // 防止请求中文乱码
        req.setCharacterEncoding("utf-8");

        // 获取请求参数
        String name = req.getParameter("name");
        
        // 获取request中的数据
        Object age = req.getAttribute("age");
        System.out.println("name:" + name);
        System.out.println("age:" + age);

        // 转发到html页面
        req.getRequestDispatcher("/success.html").forward(req, resp);
    }
}
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<form action="demo2" method="post">
    姓名：<input type="text" name="name">
    <input type="submit">
</form>
</body>
</html>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    业务办理成功！！！
</body>
</html>
```

## base标签的作用

为了简化路径的编写，我们在项目中往往写的是相对路径。

但是相对路径大家容易写错。可以在页面中使用 base 标签来简化！

![1725459540698-3a825cd9-068b-4626-94b8-d298aebc4e6e.png](./img/TvMXBSJiS74TOLoG/1725459540698-3a825cd9-068b-4626-94b8-d298aebc4e6e-401488.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <!--
        写了base标签后，该页面中所有的相对路径跳转都基于它！
    -->
    <base href="http://localhost:8080/javaweb_demo1_war_exploded/">
</head>
<body>
<form action="demo4" method="post">
    姓名：<input type="text" name="name">
    <input type="submit">
</form>
</body>
</html>
```

```java
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;

@WebServlet("/demo4")
public class Demo4Servlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        req.setCharacterEncoding("utf-8");

        String name = req.getParameter("name");
        System.out.println(name);
    }
}
```

## HttpServletResponse类的介绍

* HttpServletResponse类和HttpServletRequest类一样，每次请求进来，Tomcat服务器都会创建一个Response对象传递给Servlet程序去使用。
* HttpServletRequest表示请求过来的信息，HttpServletResponse对象表示所有响应的信息。
* 我们如果要设置返回给客户端的信息，都可以通过HttpServletResponse对象来进行设置。

## 给客户端回传字符串数据

```java
PrintWriter writer = resp.getWriter();
writer.write("response content!!!");
```

## 解决响应的中文乱码

```java
resp.setCharacterEncoding("utf-8");
resp.setContentType("text/html;charset=utf-8");
```

## 请求重定向

请求重定向，是指客户端给服务器发请求，然后服务器告诉客户端说，我给你一个新地址，你去新地址去访问，叫请求重定向。

![1725459895338-28eeb23c-bcd5-4bb3-ade7-d7094f786f35.png](./img/TvMXBSJiS74TOLoG/1725459895338-28eeb23c-bcd5-4bb3-ade7-d7094f786f35-545037.png)

**请求重定向的特点：**

1. 浏览器地址栏会发生改变

2. 相当于两次请求

3. 不能共享Request域中的数据

4. 不能重定向到WEB-INF下的资源

5. 可以重定向到工程外的资源

**案例**

```java
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;

@WebServlet("/demo5")
public class Demo5Servlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        System.out.println("demo5 被访问了！！！");

        // 请求重定向到demo6
        resp.sendRedirect(req.getContextPath() + "/demo6");
    }
}
```

```java
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;

@WebServlet("/demo6")
public class Demo6Servlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        System.out.println("demo6 被访问！！！");

        resp.getWriter().write("<a href='#'>业务处理完成</a>");
    }
}
```

测试：

通过浏览器访问demo5，在控制台会发现demo5和demo6都被访问，而且浏览器地址栏的地址也变为demo6的了。

# JSP

## JSP概述

jsp的全名是：java server pages，java服务器页面。

jsp的主要作用是代替Servlet程序回传HTML页面的数据。

因为Servlet程序回传HTML页面数据是一件非常繁琐的事情，开发成本和维护成本都很高。

**在JSP页面中可以方便我们去动态的展示出数据库查询出来的数据！**

案例：

```java
import javax.servlet.ServletException;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;
import java.io.PrintWriter;


public class PrintHtml extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
        resp.setContentType("text/html; charset=utf-8");
        PrintWriter writer = resp.getWriter();
        writer.write("<!DOCTYPE html>\r\n");
        writer.write("<html lang=\"en\">\r\n");
        writer.write("<head>\r\n");
        writer.write("    <meta charset=\"UTF-8\">\r\n");
        writer.write("    <title>Title</title>\r\n");
        writer.write("</head>\r\n");
        writer.write("<body>\r\n");
        writer.write("     我是test.html页面中的内容。\r\n");
        writer.write("</body>\r\n");
        writer.write("</html>\r\n");
    }
}
```

```html
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<html>
<head>
    <title>Title</title>
</head>
<body>
    我是jsp页面数据。
</body>
</html>
```

## JSP小结

**如何创建jsp页面？**

![1725461760555-472af2e3-fa55-4564-b0d2-1aa878ba6e36.png](./img/TvMXBSJiS74TOLoG/1725461760555-472af2e3-fa55-4564-b0d2-1aa878ba6e36-372082.png)![1725461772990-ee8cce5e-d956-4d34-9746-659b1643fc2b.png](./img/TvMXBSJiS74TOLoG/1725461772990-ee8cce5e-d956-4d34-9746-659b1643fc2b-772997.png)

**如何访问\*\*\*\*jsp页面？**

jsp页面和HTML页面一样，都是存放在web目录下，访问也跟访问HTML页面一样。

比如：

在web目录下有如下的文件：

web

a.html页面			访问地址是：<u><font style="color:rgb(5,99,193);">h</font></u><u><font style="color:rgb(5,99,193);">ttp://ip:port/</font></u>工程路径/a.html

b.jsp页面				访问地址是：<u><font style="color:rgb(5,99,193);">http://ip:port/工程路径/b.jsp</font></u>

## JSP页面的本质

jsp页面本质上是一个Servlet程序。

当我们第一次访问jsp页面的时候，tomcat服务器会帮我们把jsp页面翻译成为一个java源文件，并且对它进行编译成为 .class文件。

以下是jsp翻译过来的java源代码：

![1725461826847-52f4ccb7-7384-449f-bbed-467ad5b3d4e6.png](./img/TvMXBSJiS74TOLoG/1725461826847-52f4ccb7-7384-449f-bbed-467ad5b3d4e6-726595.png)

以下是HttpJspBase的源代码：

![1725461843398-8d5c3b0e-0a15-4965-8124-a4431fc49652.png](./img/TvMXBSJiS74TOLoG/1725461843398-8d5c3b0e-0a15-4965-8124-a4431fc49652-506388.png)

可以看出，HttpJspBase类直接继承了HttpServlet类。也就是说，jsp翻译出来的java类，它间接的继承了HttpServlet类，也就是说，翻译出来的jsp其实是一个Servlet程序。

总结：通过翻译的java源代码可以得到结论：jsp就是Servlet程序。

## 四个域对象

* pageContext(PageContextImpl类)		当前JSP页面范围内有效
* **request**(HttpServletRequest类)		一次请求内有效
* **session**(HttpSession类)				一个会话范围内有效（打开浏览器访问服务器，直到关闭浏览器）
* application(ServletContext类)			整个web工程范围内都有效（只要web工程不停止，数据都在）

**域对象**是可以像Map一样存取数据的对象，四个域对象功能一样，不同的是它们对数据的存取范围。

虽然四个域对象都可以存取数据，但它们在使用上是有优先顺序的。四个域在使用的时候，优先顺序分别是它们从小到大的范围的顺序：

pageContext ===>>> request ===>>> session ===>>> application

## EL表达式

### 什么是EL表达式

* EL表达式的全称是：Expression Language，是表达式语言
* EL表达式的作用是：主要是在jsp页面中进行数据的输出
* EL表达式的格式是：${表达式}

### EL表达式搜索四个域的顺序

EL表达式主要是在jsp页面中输出数据，主要是输出域对象中的数据。

<font style="background-color:rgb(255,255,0);">当四个域中都有相同的key的数据的时候，EL表达式会按照四个域的从小到大的顺序去搜索，找到后就输出。</font>

### EL表达式案例1

需求：使用EL表达式获取普通的数据展示到页面中。

浏览器访问Servlet，在Servlet中往request域对象中放了一些数据，然后将请求转发到jsp页面，

在jsp页面中可以从request域对象中取出刚刚放的哪些数据（通过EL表达式取出）

```java
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import javax.servlet.http.HttpSession;
import java.io.IOException;

@WebServlet("/demo3")
public class Demo3Servlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        // 设置编码方式
        req.setCharacterEncoding("utf-8");
        resp.setCharacterEncoding("utf-8");

        // 往request域对象中放数据
        req.setAttribute("name", "张三");
        req.setAttribute("age", 18);

        // 获取session域对象
        HttpSession session = req.getSession();
        // 往session域对象中放数据
        session.setAttribute("sex", "男");

        // 转发到jsp页面
        req.getRequestDispatcher("/demo1.jsp").forward(req, resp);
    }
}
```

```html
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<html>
<head>
    <title>Title</title>
</head>
<body>
    <%-- 使用${属性名}的方式从域对象中获取数据 --%>
    姓名：${name}<br>
    性别：${sex}<br>
    年龄：${age}
</body>
</html>
```

### EL表达式案例2

需求：使用EL表达式获取对象数据并展示。

```java
public class User {
    
    private int id;
    private String name;
    private String sex;
    private int age;

    public User() {
    }

    public User(int id, String name, String sex, int age) {
        this.id = id;
        this.name = name;
        this.sex = sex;
        this.age = age;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getSex() {
        return sex;
    }

    public void setSex(String sex) {
        this.sex = sex;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    @Override
    public String toString() {
        return "User{" +
                "id=" + id +
                ", name='" + name + '\'' +
                ", sex='" + sex + '\'' +
                ", age=" + age +
                '}';
    }
}
```

```java
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;

@WebServlet("/demo4")
public class Demo4Servlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        // 设置编码方式
        req.setCharacterEncoding("utf-8");
        resp.setCharacterEncoding("utf-8");

        // 创建对象
        User user = new User(1, "苏明玉", "女", 20);

        // 给request域对象中放入数据
        req.setAttribute("user", user);

        // 转发到页面
        req.getRequestDispatcher("/demo2.jsp").forward(req, resp);
    }
}
```

```html
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<html>
<head>
    <title>Title</title>
</head>
<body>

    <ul>
        <li>编号：${user.id}</li>
        <li>姓名：${user.name}</li>
        <li>性别：${user.sex}</li>
        <li>年龄：${user.age}</li>
    </ul>

</body>
</html>
```

### 总结

上面的两个案例中演示了使用EL表达式获取简单的数据及对象数据并展示。

那如果是集合数据，应该怎么展示？

## JSTL标签库

### JSTL标签库的介绍

* JSTL标签库的全称是JSP Standard Tag Library，JSP标准标签库。是一个不断完善的开放源代码的JSP标签库
* EL表达式主要是为了替换jsp中的表达式脚本，而JSTL标签库主要是为了替换代码脚本。这样使得整个jsp页面变的更加简洁

JSTL由五个不同功能的标签库组成：

| **功能** | **URI** | **前缀** |
| :---: | :---: | :---: |
| <font style="background-color:rgb(255,255,0);">核心标签库</font><font style="background-color:rgb(255,255,0);">—</font><font style="background-color:rgb(255,255,0);">重点</font> | <font style="background-color:rgb(255,255,0);">h</font><font style="background-color:rgb(255,255,0);">ttp://java.sun.com/jsp/jstl/core</font> | <font style="background-color:rgb(255,255,0);">c</font> |
| 格式化 | http://java.sun.com/jsp/jstl/fmt | fmt |
| 函数 | http://java.sun.com/jsp/jstl/functions | fn |
| 数据库（不使用） | http://java.sun.com/jsp/jstl/sql | sql |
| xml（不使用） | http://java.sun.com/jsp/jstl/xml | x |

### 标签库的使用步骤

1. 先导入jstl标签库的jar包（两个）
   1. jstl-1.2.jar
   2. standard-1.1.2.jar
2. 使用taglib指令引入标签库

![1725530071953-5242c984-6026-4e20-b3b7-3d47fb538172.png](./img/TvMXBSJiS74TOLoG/1725530071953-5242c984-6026-4e20-b3b7-3d47fb538172-357425.png)

### forEach标签

作用：遍历输出使用。

案例：(需要在项目中导入相关jar包)

```java
public class User {

    private int id;
    private String name;
    private String sex;
    private int age;

    public User() {
    }

    public User(int id, String name, String sex, int age) {
        this.id = id;
        this.name = name;
        this.sex = sex;
        this.age = age;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getSex() {
        return sex;
    }

    public void setSex(String sex) {
        this.sex = sex;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    @Override
    public String toString() {
        return "User{" +
                "id=" + id +
                ", name='" + name + '\'' +
                ", sex='" + sex + '\'' +
                ", age=" + age +
                '}';
    }
}
```

```java
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;
import java.util.ArrayList;
import java.util.List;

@WebServlet("/demo5")
public class Demo5Servlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        // 设置编码方式
        req.setCharacterEncoding("utf-8");
        resp.setCharacterEncoding("utf-8");

        List<User> list = new ArrayList<>();
        list.add(new User(1, "张无忌", "男", 20));
        list.add(new User(2, "赵敏", "女", 18));
        list.add(new User(3, "周芷若", "女", 22));
        
        req.setAttribute("list", list);
        
        req.getRequestDispatcher("/demo3.jsp").forward(req, resp);
    }
}
```

```html
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<%@taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>
<html>
<head>
    <title>Title</title>
</head>
<body>
    
    <table border="1">
        <tr>
            <td>编号</td>
            <td>姓名</td>
            <td>性别</td>
            <td>年龄</td>
        </tr>
        <c:forEach items="${list}" var="u">
            <tr>
                <td>${u.id}</td>
                <td>${u.name}</td>
                <td>${u.sex}</td>
                <td>${u.age}</td>
            </tr>
        </c:forEach>
    </table>
</body>
</html>
```

## 综合案例-动态展示数据库数据

### 创建数据库及表

![1725610513052-ebcdb292-a8e8-4c40-858e-bb39797cf5c9.png](./img/TvMXBSJiS74TOLoG/1725610513052-ebcdb292-a8e8-4c40-858e-bb39797cf5c9-793310.png)

### 创建JavaWeb项目

![1725610591734-2df9a23f-6761-42ce-b531-53ddbf366b46.png](./img/TvMXBSJiS74TOLoG/1725610591734-2df9a23f-6761-42ce-b531-53ddbf366b46-330333.png)

### 导入相关的jar包

![1725610702018-50c4a187-3ca6-47ee-a3ec-0e50b5da644c.png](./img/TvMXBSJiS74TOLoG/1725610702018-50c4a187-3ca6-47ee-a3ec-0e50b5da644c-691019.png)

### 创建包结构

![1725610844254-dd4f17c5-c720-472f-a1a1-6ea5c1160709.png](./img/TvMXBSJiS74TOLoG/1725610844254-dd4f17c5-c720-472f-a1a1-6ea5c1160709-777436.png)

controller包中编写各种Servlet！

### 编写数据库工具类

![1725611116692-e0642435-67cc-4cf9-8bfa-4ecd39250e43.png](./img/TvMXBSJiS74TOLoG/1725611116692-e0642435-67cc-4cf9-8bfa-4ecd39250e43-159024.png)

```java
package com.lhp.utils;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;

// 数据库工具类
public class JDBCUtils {

    static{
        // 加载数据库驱动
        try {
            Class.forName("com.mysql.jdbc.Driver");
        } catch (ClassNotFoundException e) {
            e.printStackTrace();
        }
    }

    // 获取数据库连接
    public static Connection getConnection(){
        String url = "jdbc:mysql:///demo?useUnicode=true&characterEncoding=utf-8";
        String username = "root";
        String password = "123456";
        Connection connection = null;
        try {
            connection = DriverManager.getConnection(url, username, password);
        } catch (SQLException e) {
            e.printStackTrace();
        }
        return connection;
    }

    // 关闭连接
    public static void closeConnection(Connection connection){
        if(connection != null){
            try {
                connection.close();
            } catch (SQLException e) {
                e.printStackTrace();
            }
        }
    }
}
```

### 编写实体类

```java
package com.lhp.pojo;

public class User {
    
    private int id;
    private String name;
    private String sex;
    private int age;
    private String address;

    public User() {
    }

    public User(int id, String name, String sex, int age, String address) {
        this.id = id;
        this.name = name;
        this.sex = sex;
        this.age = age;
        this.address = address;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getSex() {
        return sex;
    }

    public void setSex(String sex) {
        this.sex = sex;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public String getAddress() {
        return address;
    }

    public void setAddress(String address) {
        this.address = address;
    }

    @Override
    public String toString() {
        return "User{" +
                "id=" + id +
                ", name='" + name + '\'' +
                ", sex='" + sex + '\'' +
                ", age=" + age +
                ", address='" + address + '\'' +
                '}';
    }
}
```

### 编写dao层代码

```java
package com.lhp.dao;

import com.lhp.pojo.User;
import com.lhp.utils.JDBCUtils;
import org.apache.commons.dbutils.QueryRunner;
import org.apache.commons.dbutils.handlers.BeanListHandler;

import java.sql.Connection;
import java.sql.SQLException;
import java.util.List;

public class UserDao {

    // 查询user表中所有的数据
    public List<User> findAll(){

        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql语句
        String sql = "select * from user";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.调用方法执行sql
        List<User> list = null;
        try {
            list = queryRunner.query(connection, sql, new BeanListHandler<>(User.class));
        } catch (SQLException e) {
            e.printStackTrace();
        }

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);

        return list;
    }
}
```

### 编写controller层代码

```java
package com.lhp.controller;

import com.lhp.dao.UserDao;
import com.lhp.pojo.User;

import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;
import java.util.List;

@WebServlet("/findAll")
public class FindAllServlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        // 设置编码方式
        req.setCharacterEncoding("utf-8");
        resp.setCharacterEncoding("utf-8");
        resp.setContentType("text/html;charset=utf-8");

        // 创建UserDao对象
        UserDao userDao = new UserDao();
        List<User> list = userDao.findAll();

        // 将数据放入request域对象中
        req.setAttribute("list", list);
        
        // 将请求转发到user.jsp
        req.getRequestDispatcher("/user.jsp").forward(req, resp);
    }
}
```

### 编写jsp页面

```html
<%@ page contentType="text/html;charset=UTF-8" language="java" %>

<!-- 引入JSTL标签库 -->
<%@taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>
<html>
<head>
    <title>Title</title>
    <style>
        table{
            width: 500px;
            border-collapse: collapse;
            border: 1px solid red;
            margin: 30px auto;
            text-align: center;
            font-size: 25px;
        }

        tr,td{
            border: 1px solid red;
            height: 50px;
        }
        h1{
            text-align: center;
        }
    </style>
</head>
<body>
    <h1>用户信息展示</h1>
    <hr>
    <table>
        <tr>
            <td>编号</td>
            <td>姓名</td>
            <td>性别</td>
            <td>年龄</td>
            <td>门派</td>
        </tr>

        <c:forEach items="${list}" var="u">
            <tr>
                <td>${u.id}</td>
                <td>${u.name}</td>
                <td>${u.sex}</td>
                <td>${u.age}</td>
                <td>${u.address}</td>
            </tr>
        </c:forEach>
    </table>
</body>
</html>
```

### 启动项目测试

![1725613081235-fa0f7808-ca1b-4014-b5be-e261c05050ab.png](./img/TvMXBSJiS74TOLoG/1725613081235-fa0f7808-ca1b-4014-b5be-e261c05050ab-230069.png)

## session

* Session 也是一个域对象，类似于我们之前学习的 request 对象
* Session 作为域对象也是可以存储数据的，存数据使用`setAttribute(键, 值)`，取数据使用`getAttribute(键)`
* Session 的生命周期简单来说就是从浏览器访问服务器开始，到浏览器关闭结束
* Session 是存储在服务器中的，所以如果服务器重启，Session 也就消失了
* 我们经常在 Session 中存储用户登录的信息

## 综合案例-登录功能

### 需求分析

* 用户在登录页面输入账号和密码，点击登录按钮
* 浏览器提交表单信息到达服务器
* Servlet中需要获取用户输入的账号和密码
* 根据用户输入的账号和密码查询user表
* 如果能查到一条数据，说明登录成功，给用户呈现登录成功后系统的页面
* 如果查不到数据，说明账号或密码错误，让用户重新登录，最好给与提示！

### 创建数据库表

![1725797420373-94142f6c-eb49-4404-9011-eeba4568720c.png](./img/TvMXBSJiS74TOLoG/1725797420373-94142f6c-eb49-4404-9011-eeba4568720c-860411.png)

### 创建JavaWeb项目

![1725797484430-1259b168-5bba-4aa2-bb47-d1f21fbd03eb.png](./img/TvMXBSJiS74TOLoG/1725797484430-1259b168-5bba-4aa2-bb47-d1f21fbd03eb-901955.png)

![1725797509089-b93d7b35-86ea-4647-9b4f-30990e1382d2.png](./img/TvMXBSJiS74TOLoG/1725797509089-b93d7b35-86ea-4647-9b4f-30990e1382d2-808374.png)

![1725797539760-8d675013-724e-4088-b016-95f9b0ef71f0.png](./img/TvMXBSJiS74TOLoG/1725797539760-8d675013-724e-4088-b016-95f9b0ef71f0-086449.png)

![1725797552051-e22d9ff3-eb80-420c-94f0-db4d6cfd09b0.png](./img/TvMXBSJiS74TOLoG/1725797552051-e22d9ff3-eb80-420c-94f0-db4d6cfd09b0-757233.png)

### 导入相关jar包

![1725797609452-8765a83a-f283-408b-af76-76c0aeea6ac6.png](./img/TvMXBSJiS74TOLoG/1725797609452-8765a83a-f283-408b-af76-76c0aeea6ac6-001908.png)

### 创建包结构

![1725797655843-ff9f79b7-cbce-40e8-a314-2b355ab0913c.png](./img/TvMXBSJiS74TOLoG/1725797655843-ff9f79b7-cbce-40e8-a314-2b355ab0913c-136764.png)

### 导入工具类

![1725797717415-953e5c17-ad69-4dfb-aaed-5c1f7137f1fc.png](./img/TvMXBSJiS74TOLoG/1725797717415-953e5c17-ad69-4dfb-aaed-5c1f7137f1fc-887928.png)

```java
package com.lhp.utils;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;

// 数据库工具类
public class JDBCUtils {

    static{
        // 加载数据库驱动
        try {
            Class.forName("com.mysql.jdbc.Driver");
        } catch (ClassNotFoundException e) {
            e.printStackTrace();
        }
    }

    // 获取数据库连接
    public static Connection getConnection(){
        String url = "jdbc:mysql:///jdbc_demo?useUnicode=true&characterEncoding=utf-8";
        String username = "root";
        String password = "123456";
        Connection connection = null;
        try {
            connection = DriverManager.getConnection(url, username, password);
        } catch (SQLException e) {
            e.printStackTrace();
        }
        return connection;
    }

    // 关闭连接
    public static void closeConnection(Connection connection){
        if(connection != null){
            try {
                connection.close();
            } catch (SQLException e) {
                e.printStackTrace();
            }
        }
    }
}
```

### 编写实体类

在pojo包中编写实体类。

```java
package com.lhp.pojo;

public class User {
    
    private int id;
    private String username;
    private String password;

    public User() {
    }

    public User(int id, String username, String password) {
        this.id = id;
        this.username = username;
        this.password = password;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getUsername() {
        return username;
    }

    public void setUsername(String username) {
        this.username = username;
    }

    public String getPassword() {
        return password;
    }

    public void setPassword(String password) {
        this.password = password;
    }

    @Override
    public String toString() {
        return "User{" +
                "id=" + id +
                ", username='" + username + '\'' +
                ", password='" + password + '\'' +
                '}';
    }
}
```

### 编写dao层代码

```java
package com.lhp.dao;

import com.lhp.pojo.User;
import com.lhp.utils.JDBCUtils;
import org.apache.commons.dbutils.QueryRunner;
import org.apache.commons.dbutils.handlers.BeanHandler;

import java.sql.Connection;
import java.sql.SQLException;

public class UserDao {
    
    // 根据用户名和密码查询用户
    public User findByUsernameAndPassword(String username, String password){
        // 获取数据库连接
        Connection connection = JDBCUtils.getConnection();
        // 编写sql语句
        String sql = "select * from user where username=? and password=?";
        // 创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();
        // 调用方法执行sql
        User user = null;
        try {
            user = queryRunner.query(connection, sql, new BeanHandler<>(User.class), username, password);
        } catch (SQLException e) {
            e.printStackTrace();
        }
        return user;
    }
}
```

### 编写controller层代码

```java
package com.lhp.controller;

import com.lhp.dao.UserDao;
import com.lhp.pojo.User;

import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;

@WebServlet("/login")
public class LoginServlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        // 设置编码方式
        req.setCharacterEncoding("utf-8");
        resp.setContentType("text/html;charset=utf-8");
        resp.setCharacterEncoding("utf-8");

        // 接收请求参数
        String username = req.getParameter("username");
        String password = req.getParameter("password");

        // 调用dao层方法
        UserDao userDao = new UserDao();
        User user = userDao.findByUsernameAndPassword(username, password);

        // 判断是否可以登录
        if(user == null){ // 登录失败

            // 往request对象中存储数据
            req.setAttribute("msg", "账号或密码错误");

            // 转发到登录页面
            req.getRequestDispatcher("/login.jsp").forward(req, resp);
        }else{ // 登录成功

            // 将登录成功的信息放入session中
            req.getSession().setAttribute("user", user);

            // 重定向到系统页面
            resp.sendRedirect(req.getContextPath() + "/main.jsp");
        }
    }
}
```

### 编写login.jsp页面

```html
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<html>
<head>
    <title>Title</title>
</head>
<body>
<span>${msg}</span>
<form action="login" method="post">
    <input type="text" name="username" placeholder="账号"><br>
    <input type="password" name="password" placeholder="密码"><br>
    <input type="submit" value="登录">
</form>
</body>
</html>
```

### 编写main.jsp页面

```html
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<html>
<head>
    <title>Title</title>
</head>
<body>
    <h1>xxx后台管理系统</h1>
    <h3>欢迎${user.username}登录</h3>
</body>
</html>
```

### 启动项目测试

# 利用 Servlet+JDBC+MySQL+JSP 改造商品管理系统

## 项目介绍

本项目是对于我们之前做的商品管理系统的改造。

通过 Servlet + JDBC + MySQL + JSP 技术的综合应用将商品管理系统内容"写活"。

主要的功能有：

* 商品列表展示功能
* 商品添加功能
* 商品修改功能
* 商品删除功能
* 商品条件查询功能
* 登录功能
* 退出功能
* 登录过滤器

说明：

之前我们做商品管理系统的时候，只涉及到一张商品表。本次我们涉及到3张表：

* 用户表 user
* 商品表 goods
* 商品分类表 category

商品表与商品分类表是有关联关系的。

## 设计数据库表

### 创建数据库

![1725799090417-d22dcb10-f60e-4952-80b8-2761f1ad3f6d.png](./img/TvMXBSJiS74TOLoG/1725799090417-d22dcb10-f60e-4952-80b8-2761f1ad3f6d-963476.png)

![1725799116714-3756dc7d-fd8e-4c6c-bb0a-36efd01e6bd2.png](./img/TvMXBSJiS74TOLoG/1725799116714-3756dc7d-fd8e-4c6c-bb0a-36efd01e6bd2-573596.png)

### 创建用户表

用户表名称：user

![1725799153182-dff449a9-4b50-4b75-aec3-f9030bc3be03.png](./img/TvMXBSJiS74TOLoG/1725799153182-dff449a9-4b50-4b75-aec3-f9030bc3be03-911659.png)

![1725799198356-5c096605-301d-4886-91e6-55dedc5d22fd.png](./img/TvMXBSJiS74TOLoG/1725799198356-5c096605-301d-4886-91e6-55dedc5d22fd-088203.png)

注意 id 字段是主键、自增的。

插入几条数据：

![1725799246836-0ad983da-1bef-4a48-b24d-d03a0d80e211.png](./img/TvMXBSJiS74TOLoG/1725799246836-0ad983da-1bef-4a48-b24d-d03a0d80e211-110426.png)

### 创建商品分类表

商品分类表名称：category

![1725799324076-f5f4505e-236b-4377-8e8e-3b753918bbb7.png](./img/TvMXBSJiS74TOLoG/1725799324076-f5f4505e-236b-4377-8e8e-3b753918bbb7-544874.png)

插入几条数据：

![1725799393999-c04443a4-b9b4-411b-b758-b0d97fe2725d.png](./img/TvMXBSJiS74TOLoG/1725799393999-c04443a4-b9b4-411b-b758-b0d97fe2725d-997196.png)

### 创建商品表

商品表名称：goods

![1725799499213-39d4554c-c37f-4117-ab09-23b62f59533e.png](./img/TvMXBSJiS74TOLoG/1725799499213-39d4554c-c37f-4117-ab09-23b62f59533e-585558.png)

插入几条数据：

![1725799660567-ce0d3d96-fe41-4a3d-9d85-4160420c54a3.png](./img/TvMXBSJiS74TOLoG/1725799660567-ce0d3d96-fe41-4a3d-9d85-4160420c54a3-049178.png)

## 搭建项目环境

### 创建项目

![1725801774443-c43dc634-11bf-4052-a4f0-7b9d435d3968.png](./img/TvMXBSJiS74TOLoG/1725801774443-c43dc634-11bf-4052-a4f0-7b9d435d3968-099608.png)

![1725802205725-7575d8fd-06a0-4cbe-bb36-996bde70ca66.png](./img/TvMXBSJiS74TOLoG/1725802205725-7575d8fd-06a0-4cbe-bb36-996bde70ca66-170162.png)

![1725802243598-15df573f-fd2b-4f0a-b537-48fe0f1c0c3d.png](./img/TvMXBSJiS74TOLoG/1725802243598-15df573f-fd2b-4f0a-b537-48fe0f1c0c3d-433983.png)

![1725802261257-e6e1807e-a0a9-4f34-aaf8-50fb87fc7963.png](./img/TvMXBSJiS74TOLoG/1725802261257-e6e1807e-a0a9-4f34-aaf8-50fb87fc7963-883818.png)

### 导入相关jar包

![1725802616368-71d6b25d-27ea-4e87-b8d2-ab673234dd67.png](./img/TvMXBSJiS74TOLoG/1725802616368-71d6b25d-27ea-4e87-b8d2-ab673234dd67-323478.png)

![1725802636251-cc6d45ed-1c0b-4507-978e-1703fe4508e9.png](./img/TvMXBSJiS74TOLoG/1725802636251-cc6d45ed-1c0b-4507-978e-1703fe4508e9-677482.png)

![1725802532136-413a010a-ea3e-4379-8ad1-3825259befdd.png](./img/TvMXBSJiS74TOLoG/1725802532136-413a010a-ea3e-4379-8ad1-3825259befdd-706528.png)

### 创建包结构

![1725802780530-d6efb25c-43a5-4b91-9503-1a336c1a1017.png](./img/TvMXBSJiS74TOLoG/1725802780530-d6efb25c-43a5-4b91-9503-1a336c1a1017-339937.png)

### 导入数据库工具类

```java
package com.lhp.utils;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;

// 数据库工具类
public class JDBCUtils {

    static{
        // 加载数据库驱动
        try {
            Class.forName("com.mysql.jdbc.Driver");
        } catch (ClassNotFoundException e) {
            e.printStackTrace();
        }
    }

    // 获取数据库连接
    public static Connection getConnection(){
        String url = "jdbc:mysql:///goods_manage?useUnicode=true&characterEncoding=utf-8";
        String username = "root";
        String password = "123456";
        Connection connection = null;
        try {
            connection = DriverManager.getConnection(url, username, password);
        } catch (SQLException e) {
            e.printStackTrace();
        }
        return connection;
    }

    // 关闭连接
    public static void closeConnection(Connection connection){
        if(connection != null){
            try {
                connection.close();
            } catch (SQLException e) {
                e.printStackTrace();
            }
        }
    }
}
```

### 编写用户实体类

```java
package com.lhp.pojo;

public class User {
    
    private int id;
    private String username;
    private String password;

    public User() {
    }

    public User(int id, String username, String password) {
        this.id = id;
        this.username = username;
        this.password = password;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getUsername() {
        return username;
    }

    public void setUsername(String username) {
        this.username = username;
    }

    public String getPassword() {
        return password;
    }

    public void setPassword(String password) {
        this.password = password;
    }

    @Override
    public String toString() {
        return "User{" +
                "id=" + id +
                ", username='" + username + '\'' +
                ", password='" + password + '\'' +
                '}';
    }
}
```

### 编写商品分类实体类

```java
package com.lhp.pojo;

public class Category {
    
    private int cid;
    private String cname;

    public Category() {
    }

    public Category(int cid, String cname) {
        this.cid = cid;
        this.cname = cname;
    }

    public int getCid() {
        return cid;
    }

    public void setCid(int cid) {
        this.cid = cid;
    }

    public String getCname() {
        return cname;
    }

    public void setCname(String cname) {
        this.cname = cname;
    }

    @Override
    public String toString() {
        return "Category{" +
                "cid=" + cid +
                ", cname='" + cname + '\'' +
                '}';
    }
}
```

### 编写商品实体类

```java
package com.lhp.pojo;

import java.util.Date;

public class Goods {

    private int id;
    private String name;
    private double price;
    private Date producedate;
    private String address;
    private int cid;

    public Goods() {
    }

    public Goods(int id, String name, double price, Date producedate, String address, int cid) {
        this.id = id;
        this.name = name;
        this.price = price;
        this.producedate = producedate;
        this.address = address;
        this.cid = cid;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public double getPrice() {
        return price;
    }

    public void setPrice(double price) {
        this.price = price;
    }

    public Date getProducedate() {
        return producedate;
    }

    public void setProducedate(Date producedate) {
        this.producedate = producedate;
    }

    public String getAddress() {
        return address;
    }

    public void setAddress(String address) {
        this.address = address;
    }

    public int getCid() {
        return cid;
    }

    public void setCid(int cid) {
        this.cid = cid;
    }

    @Override
    public String toString() {
        return "Goods{" +
                "id=" + id +
                ", name='" + name + '\'' +
                ", price=" + price +
                ", producedate=" + producedate +
                ", address='" + address + '\'' +
                ", cid=" + cid +
                '}';
    }
}
```

### 编写组合实体类

因为在商品列表展示页面，展示的信息有商品表的信息、商品分类表的信息，而我们目前的实体类中没有一个实体类能够包含这两张表的信息。

所以，我们需要写一个"大类"，该类中包含商品的信息、商品分类的信息。我们称为组合类！

```java
package com.lhp.pojo;

import java.util.Date;

public class GoodsVo { // view object
    private int id;
    private String name;
    private double price;
    private Date producedate;
    private String address;
    private int cid;
    private String cname;

    public GoodsVo() {
    }

    public GoodsVo(int id, String name, double price, Date producedate, String address, int cid, String cname) {
        this.id = id;
        this.name = name;
        this.price = price;
        this.producedate = producedate;
        this.address = address;
        this.cid = cid;
        this.cname = cname;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public double getPrice() {
        return price;
    }

    public void setPrice(double price) {
        this.price = price;
    }

    public Date getProducedate() {
        return producedate;
    }

    public void setProducedate(Date producedate) {
        this.producedate = producedate;
    }

    public String getAddress() {
        return address;
    }

    public void setAddress(String address) {
        this.address = address;
    }

    public int getCid() {
        return cid;
    }

    public void setCid(int cid) {
        this.cid = cid;
    }

    public String getCname() {
        return cname;
    }

    public void setCname(String cname) {
        this.cname = cname;
    }

    @Override
    public String toString() {
        return "GoodsVo{" +
                "id=" + id +
                ", name='" + name + '\'' +
                ", price=" + price +
                ", producedate=" + producedate +
                ", address='" + address + '\'' +
                ", cid=" + cid +
                ", cname='" + cname + '\'' +
                '}';
    }
}
```

## 实现商品列表展示功能

### 编写dao层代码

```java
package com.lhp.dao;

import com.lhp.pojo.GoodsVo;
import com.lhp.utils.JDBCUtils;
import org.apache.commons.dbutils.QueryRunner;
import org.apache.commons.dbutils.handlers.BeanListHandler;

import java.sql.Connection;
import java.sql.SQLException;
import java.util.List;

public class GoodsDao {
    
    // 查询所有商品及商品分类信息
    public List<GoodsVo> findAll(){
        Connection connection = JDBCUtils.getConnection();
        String sql = "select * from goods g left join category c on g.cid=c.cid";
        QueryRunner queryRunner = new QueryRunner();
        List<GoodsVo> list = null;
        try {
            list = queryRunner.query(connection, sql, new BeanListHandler<>(GoodsVo.class));
        } catch (SQLException e) {
            e.printStackTrace();
        }
        JDBCUtils.closeConnection(connection);
        return list;
    }
}
```

### 编写controller层代码

```java
package com.lhp.controller;

import com.lhp.dao.GoodsDao;
import com.lhp.pojo.GoodsVo;

import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;
import java.util.List;

@WebServlet("/findAll")
public class FindAllServlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
        
        req.setCharacterEncoding("utf-8");
        resp.setCharacterEncoding("utf-8");
        resp.setContentType("text/html;charset=utf-8");

        GoodsDao goodsDao = new GoodsDao();
        List<GoodsVo> list = goodsDao.findAll();
        
        req.setAttribute("list", list);
        
        req.getRequestDispatcher("/list.jsp").forward(req, resp);
    }
}
```

### 编写index.jsp页面

```html
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<html>
<head>
    <title>$Title$</title>
</head>
<body>

<a href="findAll" target="_blank">商品列表展示</a>
</body>
</html>
```

### 编写list.jsp页面

```html
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<%@taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>
<html>
<head>
    <title>Title</title>
</head>
<body>
    <h1>商品信息列表展示</h1>
    <hr>

    <table border="1">
        <tr>
            <td>商品编号</td>
            <td>商品名称</td>
            <td>商品价格</td>
            <td>生产日期</td>
            <td>生产地址</td>
            <td>商品分类</td>
            <td>操作</td>
        </tr>
        <c:forEach items="${list}" var="g">
            <tr>
                <td>${g.id}</td>
                <td>${g.name}</td>
                <td>${g.price}</td>
                <td>${g.producedate}</td>
                <td>${g.address}</td>
                <td>${g.cname}</td>
                <td>
                    <a href="#">删除</a>
                    <a href="#">修改</a>
                </td>
            </tr>
        </c:forEach>
    </table>
</body>
</html>
```

### 启动项目测试

![1725803866938-e62c17e8-d8c5-4596-881f-1250370d3d3a.png](./img/TvMXBSJiS74TOLoG/1725803866938-e62c17e8-d8c5-4596-881f-1250370d3d3a-748092.png)

![1725803879654-e984b57b-3e2f-4bf1-a0ff-5ae6f608806e.png](./img/TvMXBSJiS74TOLoG/1725803879654-e984b57b-3e2f-4bf1-a0ff-5ae6f608806e-592883.png)

![1725803898283-4cecb4b0-3518-4f83-8abe-ff59d3062828.png](./img/TvMXBSJiS74TOLoG/1725803898283-4cecb4b0-3518-4f83-8abe-ff59d3062828-345436.png)

## 实现商品添加功能

### 编写dao层代码

```java
package com.lhp.dao;

import com.lhp.pojo.Goods;
import com.lhp.pojo.GoodsVo;
import com.lhp.utils.JDBCUtils;
import org.apache.commons.dbutils.QueryRunner;
import org.apache.commons.dbutils.handlers.BeanListHandler;

import java.sql.Connection;
import java.sql.SQLException;
import java.util.List;

public class GoodsDao {

    // 添加商品
    public void addGoods(Goods g){
        Connection connection = JDBCUtils.getConnection();
        String sql = "insert into goods values(null, ?, ?, ?, ?, ?)";
        QueryRunner queryRunner = new QueryRunner();
        try {
            queryRunner.update(connection, sql, g.getName(), g.getPrice(), g.getProducedate(), g.getAddress(), g.getCid());
        } catch (SQLException e) {
            e.printStackTrace();
        }
        JDBCUtils.closeConnection(connection);
    }

    // 查询所有商品及商品分类信息
    public List<GoodsVo> findAll(){
        Connection connection = JDBCUtils.getConnection();
        String sql = "select * from goods g left join category c on g.cid=c.cid";
        QueryRunner queryRunner = new QueryRunner();
        List<GoodsVo> list = null;
        try {
            list = queryRunner.query(connection, sql, new BeanListHandler<>(GoodsVo.class));
        } catch (SQLException e) {
            e.printStackTrace();
        }
        JDBCUtils.closeConnection(connection);
        return list;
    }
}
```

### 编写controller层代码

```java
package com.lhp.controller;

import com.lhp.dao.GoodsDao;
import com.lhp.pojo.Goods;

import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;
import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.Date;

@WebServlet("/addGoods")
public class AddServlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        req.setCharacterEncoding("utf-8");
        resp.setCharacterEncoding("utf-8");
        resp.setContentType("text/html;charset=utf-8");

        String name = req.getParameter("name");
        String priceStr = req.getParameter("price");
        double price = Double.parseDouble(priceStr);
        
        String producedateStr = req.getParameter("producedate");
        SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
        Date producedate = null;
        try {
            producedate = sdf.parse(producedateStr);
        } catch (ParseException e) {
            e.printStackTrace();
        }

        String address = req.getParameter("address");
        String cidStr = req.getParameter("cid");
        int cid = Integer.parseInt(cidStr);

        Goods goods = new Goods(0, name, price, producedate, address, cid);
        GoodsDao goodsDao = new GoodsDao();
        goodsDao.addGoods(goods);
        
        // 重定向到查询所有的Servlet，给用户展示最新的商品信息
        resp.sendRedirect(req.getContextPath() + "/findAll");
    }
}
```

### 编写list.jsp页面

![1725804688771-44a702f1-400c-4629-bffa-7446a778515d.png](./img/TvMXBSJiS74TOLoG/1725804688771-44a702f1-400c-4629-bffa-7446a778515d-068310.png)

### 编写add.jsp页面

```html
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<html>
<head>
    <title>Title</title>
</head>
<body>
    <h1>商品信息添加</h1>
    <hr>

    <form action="addGoods" method="post">
        <p>
            商品名称：<input type="text" name="name">
        </p>
        <p>
            商品价格：<input type="text" name="price">
        </p>
        <p>
            生产日期：<input type="date" name="producedate">
        </p>
        <p>
            生产地址：<input type="text" name="address">
        </p>
        <p>
            商品分类：
            <select name="cid">
                <option value="">请选择分类</option>
                <option value="1">酒水</option>
                <option value="2">饮料</option>
                <option value="3">零食</option>
            </select>
        </p>
        <p>
            <input type="submit" value="保存">
        </p>
    </form>
</body>
</html>
```

### 启动项目测试

![1725804904798-e8d95cd7-f61d-4a62-ab47-51094a9dc8ab.png](./img/TvMXBSJiS74TOLoG/1725804904798-e8d95cd7-f61d-4a62-ab47-51094a9dc8ab-500067.png)

![1725804912783-af763db1-d11c-40e7-8e9c-59f225334048.png](./img/TvMXBSJiS74TOLoG/1725804912783-af763db1-d11c-40e7-8e9c-59f225334048-457210.png)

![1725804951339-a1a64069-18ca-405d-81e0-26ed20de7f50.png](./img/TvMXBSJiS74TOLoG/1725804951339-a1a64069-18ca-405d-81e0-26ed20de7f50-285889.png)

![1725804964738-4471dbb0-151d-4401-8190-3d87cd668c23.png](./img/TvMXBSJiS74TOLoG/1725804964738-4471dbb0-151d-4401-8190-3d87cd668c23-797836.png)

## 实现商品回显功能

### 需求分析

1. 在列表展示页面中，点击某条商品信息后面的修改按钮，发请求到后端，并携带一个参数`商品ID`
2. 后端Servlet接收到id，然后根据id查询到要修改的数据
3. 将查到的数据放到request域对象中
4. 将请求转发到修改页面
5. 在修改页面通过EL表达式取出request域对象中的数据回显

### 编写dao层代码

```java
package com.lhp.dao;

import com.lhp.pojo.Goods;
import com.lhp.pojo.GoodsVo;
import com.lhp.utils.JDBCUtils;
import org.apache.commons.dbutils.QueryRunner;
import org.apache.commons.dbutils.handlers.BeanHandler;
import org.apache.commons.dbutils.handlers.BeanListHandler;
import java.sql.Connection;
import java.sql.SQLException;
import java.util.List;

public class GoodsDao {
    
    // 根据id查询商品
    public Goods getById(int id){
        Connection connection = JDBCUtils.getConnection();
        String sql = "select * from goods where id=?";
        QueryRunner queryRunner = new QueryRunner();
        Goods goods = null;
        try {
            goods = queryRunner.query(connection, sql, new BeanHandler<>(Goods.class), id);
        } catch (SQLException e) {
            e.printStackTrace();
        }
        return goods;
    }

    // 添加商品
    public void addGoods(Goods g){
        Connection connection = JDBCUtils.getConnection();
        String sql = "insert into goods values(null, ?, ?, ?, ?, ?)";
        QueryRunner queryRunner = new QueryRunner();
        try {
            queryRunner.update(connection, sql, g.getName(), g.getPrice(), g.getProducedate(), g.getAddress(), g.getCid());
        } catch (SQLException e) {
            e.printStackTrace();
        }
        JDBCUtils.closeConnection(connection);
    }

    // 查询所有商品及商品分类信息
    public List<GoodsVo> findAll(){
        Connection connection = JDBCUtils.getConnection();
        String sql = "select * from goods g left join category c on g.cid=c.cid";
        QueryRunner queryRunner = new QueryRunner();
        List<GoodsVo> list = null;
        try {
            list = queryRunner.query(connection, sql, new BeanListHandler<>(GoodsVo.class));
        } catch (SQLException e) {
            e.printStackTrace();
        }
        JDBCUtils.closeConnection(connection);
        return list;
    }
}
```

### 编写controller层代码

```java
package com.lhp.controller;

import com.lhp.dao.GoodsDao;
import com.lhp.pojo.Goods;

import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;

@WebServlet("/getById")
public class GetByIdServlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        req.setCharacterEncoding("utf-8");
        resp.setCharacterEncoding("utf-8");
        resp.setContentType("text/html;charset=utf-8");

        String idStr = req.getParameter("id");
        int id = Integer.parseInt(idStr);

        GoodsDao goodsDao = new GoodsDao();
        Goods goods = goodsDao.getById(id);
        
        req.setAttribute("goods", goods);
        
        req.getRequestDispatcher("/update.jsp").forward(req, resp);
    }
}
```

### 编写list.jsp页面

![1725807034183-9cca99bd-8845-4f1e-922c-f58b6eec6411.png](./img/TvMXBSJiS74TOLoG/1725807034183-9cca99bd-8845-4f1e-922c-f58b6eec6411-345958.png)

### 编写update.jsp页面

```html
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<%@taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>
<html>
<head>
    <title>Title</title>
</head>
<body>
    <h1>商品信息修改</h1>
    <hr>
    <form action="" method="post">
        <input type="hidden" name="id" value="${goods.id}">
        <p>
            商品名称：<input type="text" name="name" value="${goods.name}">
        </p>
        <p>
            商品价格：<input type="text" name="price" value="${goods.price}">
        </p>
        <p>
            生产日期：<input type="date" name="producedate" value="${goods.producedate}">
        </p>
        <p>
            生产地址：<input type="text" name="address" value="${goods.address}">
        </p>
        <p>
            商品分类：
            <select name="cid">
                <option value="">请选择</option>
                <option value="1" ${goods.cid == 1 ? 'selected' : ''} >酒水</option>
                <option value="2" ${goods.cid == 2 ? 'selected' : ''} >饮料</option>
                <option value="3" ${goods.cid == 3 ? 'selected' : ''} >零食</option>
            </select>
        </p>
        <p>
            <input type="submit" value="保存">
        </p>
    </form>
</body>
</html>
```

### 启动项目测试

![1725807280517-b1431ef8-9350-4ad7-8f02-954e2c2f72fe.png](./img/TvMXBSJiS74TOLoG/1725807280517-b1431ef8-9350-4ad7-8f02-954e2c2f72fe-457501.png)

![1725807303250-823301d8-f6d7-408f-abe7-d8eccd4e1285.png](./img/TvMXBSJiS74TOLoG/1725807303250-823301d8-f6d7-408f-abe7-d8eccd4e1285-748725.png)

## 实现商品修改功能

### 修改update.jsp页面

![1725950696367-0e277dff-a297-4e3c-8abc-19230e964361.png](./img/TvMXBSJiS74TOLoG/1725950696367-0e277dff-a297-4e3c-8abc-19230e964361-446252.png)

### 编写dao层代码

```java
package com.lhp.dao;

import com.lhp.pojo.Goods;
import com.lhp.pojo.GoodsVo;
import com.lhp.utils.JDBCUtils;
import org.apache.commons.dbutils.QueryRunner;
import org.apache.commons.dbutils.handlers.BeanHandler;
import org.apache.commons.dbutils.handlers.BeanListHandler;

import java.sql.Connection;
import java.sql.SQLException;
import java.util.List;

public class GoodsDao {

    // 根据id修改商品信息
    public void updateGoods(Goods g){

        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql
        String sql = "update goods set name=?, price=?, producedate=?, address=?, cid=? where id=?";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.调用方法执行sql
        try {
            queryRunner.update(connection, sql, g.getName(),g.getPrice(),g.getProducedate(),g.getAddress(),g.getCid(),g.getId());
        } catch (SQLException e) {
            e.printStackTrace();
        }

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);
    }

    // 根据id查询商品信息
    public Goods getById(int id){

        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql语句
        String sql = "select * from goods where id=?";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.调用方法执行sql
        Goods goods = null;
        try {
            goods = queryRunner.query(connection, sql, new BeanHandler<>(Goods.class), id);
        } catch (SQLException e) {
            e.printStackTrace();
        }

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);

        return goods;
    }

    // 添加商品
    public void addGoods(Goods g){

        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql语句
        String sql = "insert into goods values(null, ?, ?, ?, ?, ?)";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.调用方法执行sql
        try {
            queryRunner.update(connection, sql, g.getName(), g.getPrice(), g.getProducedate(), g.getAddress(), g.getCid());
        } catch (SQLException e) {
            e.printStackTrace();
        }

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);
    }

    // 查询所有的商品及商品分类信息
    public List<GoodsVo> findAll(){

        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql语句
        String sql = "select * from goods g left join category c on g.cid=c.cid";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.调用方法执行sql语句
        List<GoodsVo> list = null;
        try {
            list = queryRunner.query(connection, sql, new BeanListHandler<>(GoodsVo.class));
        } catch (SQLException e) {
            e.printStackTrace();
        }

        // 5.关闭数据库连接
        JDBCUtils.closeConnection(connection);

        return list;
    }
}
```

### 编写controller层代码

```java
package com.lhp.controller;

import com.lhp.dao.GoodsDao;
import com.lhp.pojo.Goods;

import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;
import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.Date;

@WebServlet("/updateGoods")
public class UpdateGoodsServlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        // 设置编码方式
        req.setCharacterEncoding("utf-8");
        resp.setCharacterEncoding("utf-8");
        resp.setContentType("text/html;charset=utf-8");

        // 接收请求参数
        String idStr = req.getParameter("id");
        int id = Integer.parseInt(idStr);

        String name = req.getParameter("name");
        String priceStr = req.getParameter("price"); // "3.5"
        // 将字符串的价格，转为double类型的价格
        double price = Double.parseDouble(priceStr);

        String producedateStr = req.getParameter("producedate");
        // 将字符串的日期转为Date类型的日期
        SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
        Date producedate = null;
        try {
            producedate = sdf.parse(producedateStr);
        } catch (ParseException e) {
            e.printStackTrace();
        }

        String address = req.getParameter("address");
        String cidStr = req.getParameter("cid");
        // 将字符串的id转为int类型
        int cid = Integer.parseInt(cidStr);

        // 调用GoodsDao中的修改方法
        GoodsDao goodsDao = new GoodsDao();
        Goods goods = new Goods(id, name, price, producedate, address, cid);
        goodsDao.updateGoods(goods);

        // 重定向到FindAllServlet，展示最新的数据
        resp.sendRedirect(req.getContextPath() + "/findAll");
    }
}
```

### 启动项目测试

## 实现商品删除功能

### 需求分析

1. 点击删除按钮后，发请求到后端，并携带参数id
2. 后端Servlet接收请求参数id
3. 调用GoodsDao中的删除方法，根据id删除数据
4. 删除之后重定向到FindAllServlet，展示最新数据

### 编写dao层代码

```java
package com.lhp.dao;

import com.lhp.pojo.Goods;
import com.lhp.pojo.GoodsVo;
import com.lhp.utils.JDBCUtils;
import org.apache.commons.dbutils.QueryRunner;
import org.apache.commons.dbutils.handlers.BeanHandler;
import org.apache.commons.dbutils.handlers.BeanListHandler;

import java.sql.Connection;
import java.sql.SQLException;
import java.util.List;

public class GoodsDao {
    
    // 根据id删除商品
    public void deleteGoods(int id){
        
        // 1.获取数据连接
        Connection connection = JDBCUtils.getConnection();
        
        // 2.编写sql
        String sql = "delete from goods where id=?";
        
        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();
        
        // 4.调用方法执行sql
        try {
            queryRunner.update(connection, sql, id);
        } catch (SQLException e) {
            e.printStackTrace();
        }

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);
    }

    // 根据id修改商品信息
    public void updateGoods(Goods g){

        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql
        String sql = "update goods set name=?, price=?, producedate=?, address=?, cid=? where id=?";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.调用方法执行sql
        try {
            queryRunner.update(connection, sql, g.getName(),g.getPrice(),g.getProducedate(),g.getAddress(),g.getCid(),g.getId());
        } catch (SQLException e) {
            e.printStackTrace();
        }

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);
    }

    // 根据id查询商品信息
    public Goods getById(int id){

        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql语句
        String sql = "select * from goods where id=?";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.调用方法执行sql
        Goods goods = null;
        try {
            goods = queryRunner.query(connection, sql, new BeanHandler<>(Goods.class), id);
        } catch (SQLException e) {
            e.printStackTrace();
        }

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);

        return goods;
    }

    // 添加商品
    public void addGoods(Goods g){

        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql语句
        String sql = "insert into goods values(null, ?, ?, ?, ?, ?)";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.调用方法执行sql
        try {
            queryRunner.update(connection, sql, g.getName(), g.getPrice(), g.getProducedate(), g.getAddress(), g.getCid());
        } catch (SQLException e) {
            e.printStackTrace();
        }

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);
    }

    // 查询所有的商品及商品分类信息
    public List<GoodsVo> findAll(){

        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql语句
        String sql = "select * from goods g left join category c on g.cid=c.cid";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.调用方法执行sql语句
        List<GoodsVo> list = null;
        try {
            list = queryRunner.query(connection, sql, new BeanListHandler<>(GoodsVo.class));
        } catch (SQLException e) {
            e.printStackTrace();
        }

        // 5.关闭数据库连接
        JDBCUtils.closeConnection(connection);

        return list;
    }
}
```

### 编写controller层代码

```java
package com.lhp.controller;

import com.lhp.dao.GoodsDao;

import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;

@WebServlet("/deleteGoods")
public class DeleteGoodsServlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        // 设置编码方式
        req.setCharacterEncoding("utf-8");
        resp.setCharacterEncoding("utf-8");
        resp.setContentType("text/html;charset=utf-8");

        // 接收请求参数
        String idStr = req.getParameter("id");
        int id = Integer.parseInt(idStr);

        GoodsDao goodsDao = new GoodsDao();
        goodsDao.deleteGoods(id);
        
        // 重定向到FindAllServlet展示最新的数据
        resp.sendRedirect(req.getContextPath() + "/findAll");
    }
}
```

### 修改list.jsp页面

![1725954596714-43f4ad2e-9218-4bbd-a99e-08783dc25458.png](./img/TvMXBSJiS74TOLoG/1725954596714-43f4ad2e-9218-4bbd-a99e-08783dc25458-177430.png)

### 启动项目测试

## 实现商品条件查询功能

### 编写dao层代码

```java
package com.lhp.dao;

import com.lhp.pojo.Goods;
import com.lhp.pojo.GoodsVo;
import com.lhp.utils.JDBCUtils;
import org.apache.commons.dbutils.QueryRunner;
import org.apache.commons.dbutils.handlers.BeanHandler;
import org.apache.commons.dbutils.handlers.BeanListHandler;

import java.sql.Connection;
import java.sql.SQLException;
import java.util.List;

public class GoodsDao {

    // 根据商品名称模糊查询
    public List<GoodsVo> findByName(String name){

        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql
        String sql = "select * from goods g left join category c on g.cid=c.cid where g.name like ?";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.调用方法执行sql
        List<GoodsVo> list = null;
        try {
            list = queryRunner.query(connection, sql, new BeanListHandler<>(GoodsVo.class), "%" + name + "%");
        } catch (SQLException e) {
            e.printStackTrace();
        }

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);
        
        return list;
    }


    // 根据id删除商品
    public void deleteGoods(int id){

        // 1.获取数据连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql
        String sql = "delete from goods where id=?";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.调用方法执行sql
        try {
            queryRunner.update(connection, sql, id);
        } catch (SQLException e) {
            e.printStackTrace();
        }

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);
    }

    // 根据id修改商品信息
    public void updateGoods(Goods g){

        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql
        String sql = "update goods set name=?, price=?, producedate=?, address=?, cid=? where id=?";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.调用方法执行sql
        try {
            queryRunner.update(connection, sql, g.getName(),g.getPrice(),g.getProducedate(),g.getAddress(),g.getCid(),g.getId());
        } catch (SQLException e) {
            e.printStackTrace();
        }

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);
    }

    // 根据id查询商品信息
    public Goods getById(int id){

        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql语句
        String sql = "select * from goods where id=?";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.调用方法执行sql
        Goods goods = null;
        try {
            goods = queryRunner.query(connection, sql, new BeanHandler<>(Goods.class), id);
        } catch (SQLException e) {
            e.printStackTrace();
        }

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);

        return goods;
    }

    // 添加商品
    public void addGoods(Goods g){

        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql语句
        String sql = "insert into goods values(null, ?, ?, ?, ?, ?)";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.调用方法执行sql
        try {
            queryRunner.update(connection, sql, g.getName(), g.getPrice(), g.getProducedate(), g.getAddress(), g.getCid());
        } catch (SQLException e) {
            e.printStackTrace();
        }

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);
    }

    // 查询所有的商品及商品分类信息
    public List<GoodsVo> findAll(){

        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql语句
        String sql = "select * from goods g left join category c on g.cid=c.cid";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.调用方法执行sql语句
        List<GoodsVo> list = null;
        try {
            list = queryRunner.query(connection, sql, new BeanListHandler<>(GoodsVo.class));
        } catch (SQLException e) {
            e.printStackTrace();
        }

        // 5.关闭数据库连接
        JDBCUtils.closeConnection(connection);

        return list;
    }
}
```

### 编写controller层代码

```java
package com.lhp.controller;

import com.lhp.dao.GoodsDao;
import com.lhp.pojo.GoodsVo;

import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;
import java.util.List;

// 条件查询的Servlet
@WebServlet("/findByName")
public class FindByNameServlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        // 设置编码方式
        req.setCharacterEncoding("utf-8");
        resp.setCharacterEncoding("utf-8");
        resp.setContentType("text/html;charset=utf-8");

        // 接收请求参数
        String name = req.getParameter("name");

        GoodsDao goodsDao = new GoodsDao();
        List<GoodsVo> list = goodsDao.findByName(name);

        // 将数据放入request域对象中
        req.setAttribute("list", list);

        // 转发到list.jsp页面
        req.getRequestDispatcher("/list.jsp").forward(req, resp);
    }
}
```

### 编写list.jsp页面

![1725958287497-3a93d71e-2da4-4377-9f48-f13adbf3fd1a.png](./img/TvMXBSJiS74TOLoG/1725958287497-3a93d71e-2da4-4377-9f48-f13adbf3fd1a-736623.png)

![1725958310455-589e9df2-f72a-4cdd-a50b-353d3e1aa200.png](./img/TvMXBSJiS74TOLoG/1725958310455-589e9df2-f72a-4cdd-a50b-353d3e1aa200-699777.png)

### 启动项目测试

## 实现登录功能

### 编写dao层代码

```java
package com.lhp.dao;

import com.lhp.pojo.User;
import com.lhp.utils.JDBCUtils;
import org.apache.commons.dbutils.QueryRunner;
import org.apache.commons.dbutils.handlers.BeanHandler;

import java.sql.Connection;
import java.sql.SQLException;

public class UserDao {

    // 根据账号和密码查询用户
    public User findByUsernameAndPassword(String username, String password){

        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql语句
        String sql = "select * from user where username=? and password=?";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.调用方法执行sql
        User user = null;
        try {
            user = queryRunner.query(connection, sql, new BeanHandler<>(User.class), username, password);
        } catch (SQLException e) {
            e.printStackTrace();
        }

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);
        
        return user;
    }
}
```

### 编写controller层代码

```java
package com.lhp.controller;

import com.lhp.dao.UserDao;
import com.lhp.pojo.User;

import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import javax.servlet.http.HttpSession;
import java.io.IOException;

@WebServlet("/login")
public class LoginServlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        // 设置编码方式
        req.setCharacterEncoding("utf-8");
        resp.setCharacterEncoding("utf-8");
        resp.setContentType("text/html;charset=utf-8");

        // 接收请求参数
        String username = req.getParameter("username");
        String password = req.getParameter("password");

        // 调用dao层中的方法
        UserDao userDao = new UserDao();
        User user = userDao.findByUsernameAndPassword(username, password);

        if(user == null){ // 登录失败

            // 往request域对象中放一些数据
            req.setAttribute("msg", "账号或密码错误，请重新登录！");

            // 转发到登录页面
            req.getRequestDispatcher("/index.jsp").forward(req, resp);

        }else{ // 登录成功
            
            // 将登录人的信息放入Session域对象中
            HttpSession session = req.getSession();
            session.setAttribute("user", user);

            // 重定向到findAll
            resp.sendRedirect(req.getContextPath() + "/findAll");
        }
    }
}
```

### 编写index.jsp页面

我们是将 index.jsp 页面作为登录页面的！

```html
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<html>
<head>
    <title>$Title$</title>
</head>
<body>

<span style="color: red">${msg}</span>
<form action="login" method="post">
    账号：<input type="text" name="username"><br>
    密码：<input type="password" name="password"><br>
    <input type="submit" value="登录">
</form>

</body>
</html>
```

### 启动项目测试

## 实现显示登录人功能

![1726016831021-e95204fc-e16c-4c23-8172-15e32d39586e.png](./img/TvMXBSJiS74TOLoG/1726016831021-e95204fc-e16c-4c23-8172-15e32d39586e-361964.png)

## 实现退出功能

### 需求分析

* 在列表展示页面点击退出按钮，发请求到后端
* 后端将该用户的session清掉
* 重定向到登录页面

### 编写controller层代码

```java
package com.lhp.controller;

import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import javax.servlet.http.HttpSession;
import java.io.IOException;

@WebServlet("/logout")
public class LogoutServlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
        
        // 1.将session销毁
        HttpSession session = req.getSession();
        session.invalidate();
        
        // 2.重定向到登录页面
        resp.sendRedirect(req.getContextPath() + "/index.jsp");
    }
}
```

### 编写list.jsp页面

![1726017283370-d191b349-a1b0-4cc8-8637-75a3b19e58fa.png](./img/TvMXBSJiS74TOLoG/1726017283370-d191b349-a1b0-4cc8-8637-75a3b19e58fa-521045.png)

## 实现注册功能

### 编写dao层代码

```java
package com.lhp.dao;

import com.lhp.pojo.User;
import com.lhp.utils.JDBCUtils;
import org.apache.commons.dbutils.QueryRunner;
import org.apache.commons.dbutils.handlers.BeanHandler;

import java.sql.Connection;
import java.sql.SQLException;

public class UserDao {

    // 添加
    public void addUser(User user){

        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql语句
        String sql = "insert into user values(null, ?, ?)";
        
        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();
        
        // 4.调用方法执行sql
        try {
            queryRunner.update(connection, sql, user.getUsername(), user.getPassword());
        } catch (SQLException e) {
            e.printStackTrace();
        }

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);
    }

    // 根据账号和密码查询用户
    public User findByUsernameAndPassword(String username, String password){

        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql语句
        String sql = "select * from user where username=? and password=?";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.调用方法执行sql
        User user = null;
        try {
            user = queryRunner.query(connection, sql, new BeanHandler<>(User.class), username, password);
        } catch (SQLException e) {
            e.printStackTrace();
        }

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);

        return user;
    }
}
```

### 编写controller层代码

```java
package com.lhp.controller;

import com.lhp.dao.UserDao;
import com.lhp.pojo.User;

import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;

@WebServlet("/register")
public class RegisterServlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        // 设置编码方式
        req.setCharacterEncoding("utf-8");
        resp.setCharacterEncoding("utf-8");
        resp.setContentType("text/html;charset=utf-8");
        
        // 接收请求参数
        String username = req.getParameter("username");
        String password = req.getParameter("password");
        
        // 调用dao层方法
        UserDao userDao = new UserDao();
        User user = new User(0, username, password);
        userDao.addUser(user);
        
        // 重定向到登录页面
        resp.sendRedirect(req.getContextPath() + "/index.jsp");
    }
}
```

### 编写index.jsp页面

![1726019231032-303713ab-acac-4813-99b8-b9904d72c54d.png](./img/TvMXBSJiS74TOLoG/1726019231032-303713ab-acac-4813-99b8-b9904d72c54d-235429.png)

### 编写register.jsp页面

```html
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<html>
<head>
    <title>Title</title>
    <script>

        function fun1(){

            // 根据标签的id获取标签元素
            var password = document.getElementById('password').value;
            var password2 = document.getElementById('password2').value;

            // 比较密码和确认密码是否一致
            if(password == password2){
                return true; // 会正常提交表单
            }else{
                alert('两次输入的密码不一致！请重新输入！');
                return false; // 不会提交表单
            }
        }


    </script>
</head>
<body>
    <h1>欢迎注册</h1>
    <hr>

    <form action="register" method="post" onsubmit="return fun1()">
        <input type="text" name="username" placeholder="账号"><br><br>
        <input type="password" id="password" name="password" placeholder="密码"><br><br>
        <input type="password" id="password2" name="password2" placeholder="确认密码"><br><br>
        <input type="submit" value="保存">
    </form>
</body>
</html>
```

### 启动项目测试

## 过滤器（Filter）

### 过滤器概述

过滤器就是将请求进行拦截，判断请求是否符合要求，符合的放行；不符合的挡回去。

比如：口罩就相当于一个过滤器，可以对所有进入我们鼻子的物质进行拦截，如果是大颗粒的有害物质，就挡住，否则就放行。

### 编写过滤器的步骤

1. 编写一个类，实现 Filter 接口
2. 重写接口中的 doFilter 方法
3. 通过注解配置 Filter

### 过滤器入门案例

过滤器我们写在 filter 包中。

```java
package com.lhp.filter;

import javax.servlet.*;
import javax.servlet.annotation.WebFilter;
import java.io.IOException;

// 1.创建一个类，实现Filter接口
@WebFilter("/*") // 3.通过注解配置过滤器的拦截规则，/* 表示拦截所有的请求
public class DemoFilter implements Filter {

    // 初始化方法，该方法会在服务器启动后自动执行
    @Override
    public void init(FilterConfig filterConfig) throws ServletException {

    }

    // 2.重写doFilter方法，该方法就是过滤器的核心方法
    // 过滤器拦截住请求后，就会自动执行这个方法
    @Override
    public void doFilter(ServletRequest servletRequest, ServletResponse servletResponse, FilterChain filterChain) throws IOException, ServletException {
        System.out.println("请求拦住了，执行了doFilter方法..............");

        // 放行请求
        filterChain.doFilter(servletRequest, servletResponse);
    }

    // 销毁方法，该方法就是在服务器停止的时候会自动执行
    @Override
    public void destroy() {

    }
}
```

启动项目测试：

发现随便往服务器发送一个请求，过滤器都会执行！

## 登录过滤器

### 需求说明

通过编写登录过滤器实现：阻止用户未登录的情况下，通过地址栏直接访问。

### 编写登录过滤器

```java
package com.lhp.filter;

import javax.servlet.*;
import javax.servlet.annotation.WebFilter;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import javax.servlet.http.HttpSession;
import java.io.IOException;

// 登录过滤器
@WebFilter("/*")
public class LoginFilter implements Filter {

    @Override
    public void init(FilterConfig filterConfig) throws ServletException {

    }

    // 拦截到请求后，会自动执行该方法
    @Override
    public void doFilter(ServletRequest servletRequest, ServletResponse servletResponse, FilterChain filterChain) throws IOException, ServletException {

        // 将request和response进行转换
        HttpServletRequest request = (HttpServletRequest)servletRequest;
        HttpServletResponse response = (HttpServletResponse)servletResponse;

        // 获取session
        HttpSession session = request.getSession();
        // 获取session中用户的信息
        Object user = session.getAttribute("user");

        // 获取本次请求的路径   /goods_manage_war_exploded/login
        String path = request.getRequestURI();

        if(user != null){ // 说明登录了
            filterChain.doFilter(request, response); // 放行
        }else{ // 说明没登录

            // 否则，拦截，让用户去登录

            // 如果是访问登录页面的请求，放行
            if(path.equals("/goods_manage_war_exploded/") || path.contains("index.jsp")){
                filterChain.doFilter(request, response); // 放行
            }else if(path.contains("login")){// 如果是提交登录表单的请求，放行
                filterChain.doFilter(request, response); // 放行
            }else if(path.contains("register.jsp")){// 如果是访问注册页面的请求，放行
                filterChain.doFilter(request, response); // 放行
            }else if(path.contains("register")){// 如果是提交注册表单的请求，放行
                filterChain.doFilter(request, response); // 放行
            }else{ // 说明你没有登录，还访问一些登录后才能访问的内容，拦截让你登录
                // 转发到登录页面
                request.setAttribute("msg", "请登录后再访问！");
                request.getRequestDispatcher("/index.jsp").forward(request, response);
            }
        }
    }

    @Override
    public void destroy() {

    }
}
```

### 启动项目测试

在没有登录的情况下，直接访问 findAll，会出现如下效果：

![1726039990377-d26525f9-d018-4109-8f61-c48c03659e71.png](./img/TvMXBSJiS74TOLoG/1726039990377-d26525f9-d018-4109-8f61-c48c03659e71-939649.png)


> 更新: 2024-09-11 15:33:15  
> 原文: <https://www.yuque.com/u41736172/az9urv/gfwh4m6wr9u2qo6w>