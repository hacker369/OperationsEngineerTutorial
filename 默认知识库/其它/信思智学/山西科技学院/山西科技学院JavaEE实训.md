# 山西科技学院 JavaEE 实训

# 一、MVC 设计思想
## 落地实现
该思想实际落地后，我们需要在项目中创建这些包：

+ bean 包：用来编写实体类的包
+ dao 包：用来编写操作数据库代码的包
+ service 包：用来编写业务功能的包
+ controller 包：用来编写接收请求、响应请求代码的包
+ util 包：用来编写工具类的包

## 执行流程
![1719300261923-7f4a7d7f-5703-4f91-bf57-b64dc4f99ea5.png](./img/FW3mVLi4JOY03YXF/1719300261923-7f4a7d7f-5703-4f91-bf57-b64dc4f99ea5-139671.png)

# 二、JDBC 技术
## Navicat 创建数据库
![1719300664446-3737e6d0-5e30-444c-9255-a90ff0f7426a.png](./img/FW3mVLi4JOY03YXF/1719300664446-3737e6d0-5e30-444c-9255-a90ff0f7426a-499785.png)

![1719300748077-46668b9f-7377-47a6-b166-4e56c9de1c89.png](./img/FW3mVLi4JOY03YXF/1719300748077-46668b9f-7377-47a6-b166-4e56c9de1c89-341647.png)

![1719300772056-6cf297c3-afe6-4c4c-8de2-9414e7ac4758.png](./img/FW3mVLi4JOY03YXF/1719300772056-6cf297c3-afe6-4c4c-8de2-9414e7ac4758-613277.png)

## Navicat 创建数据库表
![1719300857163-f6e330d3-9d8e-449c-a44b-d157569f4fb7.png](./img/FW3mVLi4JOY03YXF/1719300857163-f6e330d3-9d8e-449c-a44b-d157569f4fb7-888527.png)

![1719300967027-86c8e45e-ab56-48e6-a731-fd9cad0f48d5.png](./img/FW3mVLi4JOY03YXF/1719300967027-86c8e45e-ab56-48e6-a731-fd9cad0f48d5-225742.png)

**注意：id 字段需要设置为主键、自增**

按 ctrl + s 保存，弹出下面对话框，输入表名。

![1719301034868-b37172b4-5620-4d5f-a2aa-b0ead4070efc.png](./img/FW3mVLi4JOY03YXF/1719301034868-b37172b4-5620-4d5f-a2aa-b0ead4070efc-884476.png)

![1719301067952-21583fba-d4d9-4662-927a-e0d9aeb4bfbf.png](./img/FW3mVLi4JOY03YXF/1719301067952-21583fba-d4d9-4662-927a-e0d9aeb4bfbf-581367.png)

## Navicat 中编写 sql 语句
![1719301159536-731a90f9-839e-48fa-bb6b-d34c94c90506.png](./img/FW3mVLi4JOY03YXF/1719301159536-731a90f9-839e-48fa-bb6b-d34c94c90506-156109.png)

```sql
-- 给student表添加数据
insert into student values(null, '刘备', '男', 58);

-- 查询student表中所有的数据
select * from student;

-- 修改id=2的数据
update student set name='貂蝉', sex='女', age=18 where id=2;

-- 删除id=3的数据
delete from student where id=3;
```

## JDBC 介绍
JDBC 就是使用 Java 操作数据库的一门技术。

## JDBC 入门案例1
### 案例需求
使用 JDBC 能够连接到数据库。

### 创建项目
![1719302529299-b77cc1ae-2776-4932-a9a3-33d18a730391.png](./img/FW3mVLi4JOY03YXF/1719302529299-b77cc1ae-2776-4932-a9a3-33d18a730391-683865.png)

![1719302630424-91618a68-7513-4575-a6ba-ad18547b9c71.png](./img/FW3mVLi4JOY03YXF/1719302630424-91618a68-7513-4575-a6ba-ad18547b9c71-858799.png)

![1719302675846-423de669-9f0e-4400-965a-b8717e65a5d6.png](./img/FW3mVLi4JOY03YXF/1719302675846-423de669-9f0e-4400-965a-b8717e65a5d6-421824.png)

![1719302716456-990f0a26-2723-47a0-a718-3119e907cf44.png](./img/FW3mVLi4JOY03YXF/1719302716456-990f0a26-2723-47a0-a718-3119e907cf44-563141.png)

![1719302748935-6b822832-88d4-48a1-959f-724a69da1827.png](./img/FW3mVLi4JOY03YXF/1719302748935-6b822832-88d4-48a1-959f-724a69da1827-722227.png)

### 导入 MySQL 数据库驱动包
如果你电脑上的 MySQL 是 8.xxx 版本的，需要导入 mysql-connector-j-8.0.32.jar

如果你电脑上的 MySQL 是 5.xxx 版本的，需要导入 mysql-connector-java-5.0.5-bin.jar

![1719302880161-f703efa0-f600-4066-8022-f65201f56b24.png](./img/FW3mVLi4JOY03YXF/1719302880161-f703efa0-f600-4066-8022-f65201f56b24-299782.png)

![1719302898727-ec86709e-52ed-477c-b0f5-e99143a6485e.png](./img/FW3mVLi4JOY03YXF/1719302898727-ec86709e-52ed-477c-b0f5-e99143a6485e-809282.png)

![1719302952762-28c85672-a058-439b-8ce8-3992a598ea0f.png](./img/FW3mVLi4JOY03YXF/1719302952762-28c85672-a058-439b-8ce8-3992a598ea0f-992069.png)

![1719302981596-9e440cf6-7541-4b81-9f1a-4b3f9736e6ef.png](./img/FW3mVLi4JOY03YXF/1719302981596-9e440cf6-7541-4b81-9f1a-4b3f9736e6ef-775793.png)

![1719303004151-1b138361-b37d-4919-9741-d4932c7d712f.png](./img/FW3mVLi4JOY03YXF/1719303004151-1b138361-b37d-4919-9741-d4932c7d712f-825208.png)

![1719303029388-477b0133-bfc3-44e6-80db-ae9bd8fb6a44.png](./img/FW3mVLi4JOY03YXF/1719303029388-477b0133-bfc3-44e6-80db-ae9bd8fb6a44-496424.png)

### 编写代码
![1719303080771-b350b532-765d-456b-848f-93e2cc00926b.png](./img/FW3mVLi4JOY03YXF/1719303080771-b350b532-765d-456b-848f-93e2cc00926b-921340.png)

```java
package com.xszx.dao;

import java.sql.Connection;
import java.sql.DriverManager;

// 连接数据库
public class Demo1 {

    public static void main(String[] args) throws Exception{

        // 加载数据库驱动，如果是 mysql 5.xxx 版本
        Class.forName("com.mysql.jdbc.Driver");
        // 加载数据库驱动，如果是 mysql 8.xxx 版本
        // Class.forName("com.mysql.cj.jdbc.Driver");

        // 获取数据库连接，注意数据库名要写成自己的数据库名字
        String url = "jdbc:mysql://localhost:3306/student_manage?useUnicode=true&characterEncoding=utf-8";
        String user = "root";
        String password = "root"; // 注意密码改为自己数据库的密码
        Connection connection = DriverManager.getConnection(url, user, password);

        System.out.println(connection);
    }
}
```

### 运行结果
![1719303536423-e095404a-19c6-4821-a878-7de613a88362.png](./img/FW3mVLi4JOY03YXF/1719303536423-e095404a-19c6-4821-a878-7de613a88362-230856.png)

![1719303570732-f41fa91a-d72e-4067-b895-da3350b3b0bd.png](./img/FW3mVLi4JOY03YXF/1719303570732-f41fa91a-d72e-4067-b895-da3350b3b0bd-504652.png)

## JDBC 入门案例2
### 案例需求
使用 Java 代码从数据库表中查询所有的数据，打印到控制台。

接着上面的项目中去编写即可。

### 编写代码
```java
package com.xszx.dao;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;
import java.sql.ResultSet;

// 从数据库中查询所有的数据，打印到控制台
public class Demo2 {

    public static void main(String[] args) throws Exception{

        // 加载数据库驱动
        Class.forName("com.mysql.jdbc.Driver");
        // Class.forName("com.mysql.cj.jdbc.Driver"); // mysql 8.xxx 要这样写

        // 获取数据库连接
        String url = "jdbc:mysql://localhost:3306/student_manage?useUnicode=true&characterEncoding=utf-8";
        String user = "root";
        String password = "root"; // 注意密码改为自己的
        Connection connection = DriverManager.getConnection(url, user, password);

        // 编写sql语句
        String sql = "select * from student";

        // 创建预编译语句对象
        PreparedStatement ps = connection.prepareStatement(sql);

        // 执行sql语句，得到一个结果集
        ResultSet rs = ps.executeQuery();

        // 使用while循环遍历结果集，打印到控制台
        while(rs.next()){
            int id = rs.getInt("id");
            String name = rs.getString("name");
            String sex = rs.getString("sex");
            int age = rs.getInt("age");
            System.out.println("id：" + id + ", name：" + name + ", sex：" + sex + ", age：" + age);
        }

        // 关闭连接
        if(connection != null){
            connection.close();
        }
    }
}
```

### 运行结果
![1719305906349-8d33d30a-a847-4369-b45d-3511bbe3b6ab.png](./img/FW3mVLi4JOY03YXF/1719305906349-8d33d30a-a847-4369-b45d-3511bbe3b6ab-813975.png)

## JDBC 入门案例3
### 案例需求
实现 Java 代码将数据添加到数据库中。

### 编写代码
```java
package com.xszx.dao;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;

// 将数据添加到数据库
public class Demo3 {

    public static void main(String[] args) throws Exception{

        // 加载数据库驱动
        Class.forName("com.mysql.jdbc.Driver");

        // 获取数据库连接
        String url = "jdbc:mysql://localhost:3306/student_manage?useUnicode=true&characterEncoding=utf-8";
        String user = "root";
        String password = "root";
        Connection connection = DriverManager.getConnection(url, user, password);

        // 编写sql语句
        String sql = "insert into student values(null, ?, ?, ?)";

        // 创建预编译语句对象
        PreparedStatement ps = connection.prepareStatement(sql);

        // 设置sql语句中的占位符
        ps.setString(1, "曹操");
        ps.setString(2, "男");
        ps.setInt(3, 28);

        // 执行sql语句，执行增删改的sql语句都是调用executeUpdate()，执行查询的sql语句调用executeQuery()
        int i = ps.executeUpdate();

        System.out.println("i = " + i);

        // 关闭数据库连接
        if(connection != null){
            connection.close();
        }
    }
}
```

### 运行结果
![1719306470369-18489c3a-a60a-4fbd-9e75-1908603839f3.png](./img/FW3mVLi4JOY03YXF/1719306470369-18489c3a-a60a-4fbd-9e75-1908603839f3-777844.png)

![1719306487879-723e9e7d-600a-415d-a5ab-3619627d7598.png](./img/FW3mVLi4JOY03YXF/1719306487879-723e9e7d-600a-415d-a5ab-3619627d7598-980185.png)

# 三、Servlet
## Tomcat 服务器
### 介绍
Tomcat 服务器是一个开源免费的 JavaEE 服务器，也就是说，后面我们写的 Java EE 项目需要放在 Tomcat 服务器中去运行。所以，我们需要将 IDEA 和 Tomcat 服务器集成在一块，方便我们写完代码后直接启动服务器运行。

### 安装
Tomcat 服务器![1719328450679-7d4bd2be-2344-4308-b731-79150edff94f.png](./img/FW3mVLi4JOY03YXF/1719328450679-7d4bd2be-2344-4308-b731-79150edff94f-926814.png)直接解压即可使用。

### IDEA 集成 Tomcat 服务器
![1719328550158-eb3553fd-a0ef-4928-938a-612047985039.png](./img/FW3mVLi4JOY03YXF/1719328550158-eb3553fd-a0ef-4928-938a-612047985039-714969.png)

![1719328613331-595a70b6-16ec-4c95-a477-e4fb3902c2ed.png](./img/FW3mVLi4JOY03YXF/1719328613331-595a70b6-16ec-4c95-a477-e4fb3902c2ed-591303.png)

![1719328686014-7821a416-ab43-4049-a02d-184d835433a8.png](./img/FW3mVLi4JOY03YXF/1719328686014-7821a416-ab43-4049-a02d-184d835433a8-697733.png)

![1719328712816-2ca1ba85-02b2-4563-8749-114f2cf0ec4e.png](./img/FW3mVLi4JOY03YXF/1719328712816-2ca1ba85-02b2-4563-8749-114f2cf0ec4e-463885.png)

这样以后我们使用 IDEA 创建 Java EE 项目后就可以使用 Tomcat 服务器来运行项目了。

## Servlet 介绍
+ <font style="color:rgb(51,51,51);">Servlet 是 Server Applet 的简称，称为服务端小程序，用 Java 编写的服务器端程序。</font>
+ <font style="color:rgb(51,51,51);">Servlet 是 JavaWeb 的三大组件 Servlet，Filter，Listener 之一，它属于动态资源。</font>
+ <font style="color:rgb(51,51,51);">Servlet 的作用：</font>
    - <font style="color:rgb(51,51,51);">接收请求</font>
    - <font style="color:rgb(51,51,51);">处理请求</font>
    - <font style="color:rgb(51,51,51);">完成响应</font>

## **<font style="color:rgb(51,51,51);">编写 Servlet 的步骤</font>**
1. <font style="color:rgb(0,0,0);">编写一个类继承 HttpServlet</font>
2. <font style="color:rgb(0,0,0);">重写 service 方法</font>
3. <font style="color:rgb(0,0,0);">配置 Servlet 的映射路径</font>

## <font style="color:rgb(0,0,0);">Servlet 案例1</font>
### 案例需求
实现：Servlet 入门案例。

编写一个 Servlet，启动之后，浏览器发请求访问 Servlet，Servlet 给浏览器响应一句话！

### 创建 JavaEE 项目
![1719328834825-93240bc3-9c95-45ed-beaf-46eef6b822b5.png](./img/FW3mVLi4JOY03YXF/1719328834825-93240bc3-9c95-45ed-beaf-46eef6b822b5-372316.png)

![1719328876564-d0da42d7-1202-41c3-8017-2564d2740f31.png](./img/FW3mVLi4JOY03YXF/1719328876564-d0da42d7-1202-41c3-8017-2564d2740f31-605198.png)

![1719328917131-6b965c9f-10af-4397-ae78-243fc369e6e7.png](./img/FW3mVLi4JOY03YXF/1719328917131-6b965c9f-10af-4397-ae78-243fc369e6e7-680286.png)

![1719328941168-e16e675b-d66a-4268-8e97-ead5312bb883.png](./img/FW3mVLi4JOY03YXF/1719328941168-e16e675b-d66a-4268-8e97-ead5312bb883-198585.png)

### 编写 Servlet 代码
Servlet 用来接收请求，处理请求，并响应结果给浏览器。

Servlet 需要写在 controller 包中。

![1719329057866-6339b31f-a30b-4b46-942a-c85593ac305d.png](./img/FW3mVLi4JOY03YXF/1719329057866-6339b31f-a30b-4b46-942a-c85593ac305d-501985.png)

![1719329210692-d381c6de-6177-4820-8a3f-5a0b5ef3cb61.png](./img/FW3mVLi4JOY03YXF/1719329210692-d381c6de-6177-4820-8a3f-5a0b5ef3cb61-236934.png)

```java
package com.xszx.controller;

import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;

@WebServlet("/hello") // 配置 Servlet 的访问路径
public class HelloServlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
        System.out.println("servlet.......");

        // 给浏览器响应一句话
        resp.getWriter().write("hello servlet~~~");
    }
}
```

### 启动服务器
![1719329302949-9d0ae746-2524-4f30-a6b9-34745fc94df0.png](./img/FW3mVLi4JOY03YXF/1719329302949-9d0ae746-2524-4f30-a6b9-34745fc94df0-340615.png)

启动服务器后，IDEA 会打开浏览器，并出现如下网址：

![1719329367612-596f96c7-8687-4e9e-b06c-b29c8cf04ee1.png](./img/FW3mVLi4JOY03YXF/1719329367612-596f96c7-8687-4e9e-b06c-b29c8cf04ee1-377190.png)

然后我们接着网址路径后面写访问我们 Servlet 的路径：

![1719329506059-e780c649-374a-4527-9d4e-aa0eb8a1f298.png](./img/FW3mVLi4JOY03YXF/1719329506059-e780c649-374a-4527-9d4e-aa0eb8a1f298-937428.png)

### 问题解决
启动会报如下错误：

![1719366121143-87fea1c8-0065-460e-8bbc-6c3cca9a604b.png](./img/FW3mVLi4JOY03YXF/1719366121143-87fea1c8-0065-460e-8bbc-6c3cca9a604b-080163.png)

原因：Tomcat 服务器的 8080 端口号被占用了。

解决：修改 Tomcat 服务器的端口号：

![1719363850717-f00c4832-0ce5-42f4-a529-43e5b8765451.png](./img/FW3mVLi4JOY03YXF/1719363850717-f00c4832-0ce5-42f4-a529-43e5b8765451-962839.png)

![1719363886266-4b286d29-a348-4df5-b88f-34499ce2099c.png](./img/FW3mVLi4JOY03YXF/1719363886266-4b286d29-a348-4df5-b88f-34499ce2099c-263200.png)

## Servlet 案例2
### 案例需求
实现：Servlet 接收请求参数，并响应结果给浏览器；另外设置请求与响应的编码方式。

### 编写 Servlet
```java
package com.xszx.controller;

import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;

@WebServlet("/hello2")
public class HelloServlet2 extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        // 1. 设置编码方式
        req.setCharacterEncoding("utf-8");
        resp.setCharacterEncoding("utf-8");
        resp.setContentType("text/html;characterEncoding=utf-8");

        // 2. 获取请求参数
        String name = req.getParameter("name");

        // 3. 给浏览器输入一句话
        resp.getWriter().write("hello, " + name);
    }
}
```

### 启动服务器访问
![1719366684438-f3df94d9-66bc-4567-ba37-5f361efb64b4.png](./img/FW3mVLi4JOY03YXF/1719366684438-f3df94d9-66bc-4567-ba37-5f361efb64b4-195123.png)

## Servlet 案例3
### 案例需求
实现：Servlet 将请求转发到 jsp 页面。

### 编写 Servlet
```java
package com.xszx.controller;

import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;

@WebServlet("/hello3")
public class HelloServlet3 extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
        // 设置编码
        req.setCharacterEncoding("utf-8");
        resp.setCharacterEncoding("utf-8");
        resp.setContentType("text/html;charset=utf-8");

        // 将请求转发到 success.jsp 页面，浏览器就能看到这个页面中的内容了！
        req.getRequestDispatcher("success.jsp").forward(req, resp);
    }
}
```

### 编写页面
![1719367418329-4ba3b077-4b35-459a-9e90-7b8134a64d05.png](./img/FW3mVLi4JOY03YXF/1719367418329-4ba3b077-4b35-459a-9e90-7b8134a64d05-451399.png)

![1719367453078-610d5f50-85df-478f-9ab6-878f3218ab75.png](./img/FW3mVLi4JOY03YXF/1719367453078-610d5f50-85df-478f-9ab6-878f3218ab75-720490.png)

```html
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<html>
<head>
    <title>Title</title>
</head>
<body>
    <h1>哈哈</h1>
    <h3>你好坏！</h3>
    <a href="https://www.baidu.com">点我跳转到百度</a>
</body>
</html>
```

### 启动服务器访问
![1719367673966-a8d4b481-a846-4101-93cd-07b061304c5b.png](./img/FW3mVLi4JOY03YXF/1719367673966-a8d4b481-a846-4101-93cd-07b061304c5b-709527.png)

## Servlet 案例4
### 案例需求
实现：Servlet 将请求转发到 jsp 页面，并在 request 域对象中携带简单数据，将数据展示在页面中。

### 编写 Servlet
```java
package com.xszx.controller;

import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;

@WebServlet("/hello4")
public class HelloServlet4 extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
        
        // 设置编码方式
        req.setCharacterEncoding("utf-8");
        resp.setCharacterEncoding("utf-8");
        resp.setContentType("text/html;charset=utf-8");
        
        // 往 request 域对象中放一些数据
        req.setAttribute("name", "周芷若");
        
        // 将请求转发到 demo1.jsp 页面
        req.getRequestDispatcher("demo1.jsp").forward(req, resp);
    }
}
```

### 编写页面
```html
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<html>
<head>
    <title>Title</title>
</head>
<body>
    <%-- ${xxx} 可以从域对象中根据键取值 --%>
    你好，${name}!
</body>
</html>
```

### 启动服务器访问
![1719368635407-96423884-22e1-4442-b60e-9f2eda382905.png](./img/FW3mVLi4JOY03YXF/1719368635407-96423884-22e1-4442-b60e-9f2eda382905-285493.png)

jsp 页面就是负责展示数据的！

## Servlet 案例5
### 案例需求
实现：Servlet 将请求转发到 jsp 页面，并在 request 域对象中携带对象数据，将数据展示在页面中。

### 编写实体类
#### 编写实体类属性
```java
package com.xszx.bean;

public class Student {
    private Integer id;
    private String name;
    private String sex;
    private Integer age;
}
```

#### 生成无参构造方法
![1719370211463-4e47446a-08d2-4225-980b-eaff41c87855.png](./img/FW3mVLi4JOY03YXF/1719370211463-4e47446a-08d2-4225-980b-eaff41c87855-335340.png)

![1719370254882-5d769a4f-b55e-45af-85a5-8e19c064da24.png](./img/FW3mVLi4JOY03YXF/1719370254882-5d769a4f-b55e-45af-85a5-8e19c064da24-408111.png)

![1719370354534-a6efd39a-5184-41ad-839c-47efef35d3e6.png](./img/FW3mVLi4JOY03YXF/1719370354534-a6efd39a-5184-41ad-839c-47efef35d3e6-148219.png)

#### 生成有参构造方法
![1719370381788-e3694c19-f217-422a-b6f8-2c4d4640a3eb.png](./img/FW3mVLi4JOY03YXF/1719370381788-e3694c19-f217-422a-b6f8-2c4d4640a3eb-569212.png)

![1719370395217-cc3cd7b9-7d73-4ac1-a712-73c879f2bd23.png](./img/FW3mVLi4JOY03YXF/1719370395217-cc3cd7b9-7d73-4ac1-a712-73c879f2bd23-816777.png)

![1719370419792-c304c8fa-bc6b-48c9-a970-b84f310d2381.png](./img/FW3mVLi4JOY03YXF/1719370419792-c304c8fa-bc6b-48c9-a970-b84f310d2381-803556.png)

#### 生成 set、get 方法
![1719370449529-959e8517-9615-4154-829b-9e93388bba19.png](./img/FW3mVLi4JOY03YXF/1719370449529-959e8517-9615-4154-829b-9e93388bba19-657899.png)

![1719370464512-b7fea33d-932b-4a16-9bca-1e63d358da4f.png](./img/FW3mVLi4JOY03YXF/1719370464512-b7fea33d-932b-4a16-9bca-1e63d358da4f-379237.png)

![1719370485176-1b99dbac-a0e5-4364-9254-67b8404cdbf6.png](./img/FW3mVLi4JOY03YXF/1719370485176-1b99dbac-a0e5-4364-9254-67b8404cdbf6-179836.png)

#### 最终实体类效果
```java
package com.xszx.bean;

public class Student {
    private Integer id;
    private String name;
    private String sex;
    private Integer age;

    public Student() {
    }

    public Student(Integer id, String name, String sex, Integer age) {
        this.id = id;
        this.name = name;
        this.sex = sex;
        this.age = age;
    }

    public Integer getId() {
        return id;
    }

    public void setId(Integer id) {
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

    public Integer getAge() {
        return age;
    }

    public void setAge(Integer age) {
        this.age = age;
    }
}
```

### 编写 Servlet
```java
package com.xszx.controller;

import com.xszx.bean.Student;

import javax.servlet.ServletException;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;

public class HelloServlet5 extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
        // 设置编码方式
        req.setCharacterEncoding("utf-8");
        resp.setCharacterEncoding("utf-8");
        resp.setContentType("text/html;charset=utf-8");

        // 创建 Student 对象
        Student student = new Student(1, "吕布", "男", 28);

        // 往request域对象中放入一个学生对象
        req.setAttribute("student", student);

        // 将请求转发到 demo2.jsp 页面
        req.getRequestDispatcher("demo2.jsp").forward(req, resp);
    }
}
```

### 编写页面
```html
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<html>
<head>
    <title>Title</title>
</head>
<body>
    <p>学生编号：${student.id}</p>
    <p>学生姓名：${student.name}</p>
    <p>学生性别：${student.sex}</p>
    <p>学生年龄：${student.age}</p>
</body>
</html>
```

### 启动服务器访问
![1719370924448-71ca40d1-5ac6-45f8-aa5a-4d0dd5d74a97.png](./img/FW3mVLi4JOY03YXF/1719370924448-71ca40d1-5ac6-45f8-aa5a-4d0dd5d74a97-638807.png)

## Servlet 案例6
### 案例需求
实现：Servlet 将请求转发到 jsp 页面，并在 request 域对象中携带集合数据，将数据通过 jstl 标签循环展示在页面的表格中。

### 导入 jar 包
![1719372259452-6339e70c-819a-42f2-9368-7b528660214a.png](./img/FW3mVLi4JOY03YXF/1719372259452-6339e70c-819a-42f2-9368-7b528660214a-841337.png)

![1719372290899-fab41162-b14c-406a-a263-052787553a1d.png](./img/FW3mVLi4JOY03YXF/1719372290899-fab41162-b14c-406a-a263-052787553a1d-881735.png)

然后给 lib 中粘贴我们用的 jar 包。

![1719372327631-4cb8fd8f-b4d0-4f7b-a843-c4af99426980.png](./img/FW3mVLi4JOY03YXF/1719372327631-4cb8fd8f-b4d0-4f7b-a843-c4af99426980-392847.png)

让 jar 包生效：

![1719372375254-2e31b402-17a9-4c3f-b97b-2e594b7f2192.png](./img/FW3mVLi4JOY03YXF/1719372375254-2e31b402-17a9-4c3f-b97b-2e594b7f2192-086844.png)

![1719372390159-536de3af-d3a2-4bf1-ab6a-02e6422568c7.png](./img/FW3mVLi4JOY03YXF/1719372390159-536de3af-d3a2-4bf1-ab6a-02e6422568c7-997481.png)

### 编写 Servlet
```java
package com.xszx.controller;

import com.xszx.bean.Student;
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;
import java.util.ArrayList;
import java.util.List;

@WebServlet("/hello6")
public class HelloServlet6 extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
        // 设置编码方式
        req.setCharacterEncoding("utf-8");
        resp.setCharacterEncoding("utf-8");
        resp.setContentType("text/html;charset=utf-8");

        // 创建一个List集合，往集合中放入许多学生对象
        List<Student> list = new ArrayList<>();
        list.add(new Student(1, "张无忌", "男", 26));
        list.add(new Student(2, "赵敏", "女", 18));
        list.add(new Student(3, "周芷若", "女", 22));
        list.add(new Student(4, "蛛儿", "女", 19));

        // 将list集合放入request域对象中
        req.setAttribute("list", list);

        // 将请求转发到 demo3.jsp 页面
        req.getRequestDispatcher("demo3.jsp").forward(req, resp);
    }
}
```

### 编写页面
```html
<%@ page contentType="text/html;charset=UTF-8" language="java" %>

<%-- 引入 jstl 标签库 --%>
<%@taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>
<html>
<head>
    <title>Title</title>
</head>
<body>
    <!-- table 表格标签 -->
    <table border="1">
        <!-- tr 表示行标签 -->
        <tr>
            <!-- td 表示单元格标签 -->
            <td>编号</td>
            <td>姓名</td>
            <td>性别</td>
            <td>年龄</td>
        </tr>

        <!--
            c:forEach 就是循环标签，可以循环集合
            items 表示你要循环集合是谁
            var 表示每次循环得到的数据赋值给哪个变量
        -->
        <c:forEach items="${list}" var="s">
            <tr>
                <td>${s.id}</td>
                <td>${s.name}</td>
                <td>${s.sex}</td>
                <td>${s.age}</td>
            </tr>
        </c:forEach>
    </table>
</body>
</html>
```

### 启动服务器访问
![1719373247380-081ce7ad-f42f-4ff0-836d-320202df28d7.png](./img/FW3mVLi4JOY03YXF/1719373247380-081ce7ad-f42f-4ff0-836d-320202df28d7-897865.png)

# 四、课题-基于 JavaEE 的商城项目
## 项目介绍
+ <font style="color:rgb(51, 51, 51);">该商城是一个全品类的电商购物网站（B2C）</font>
+ <font style="color:rgb(51, 51, 51);">用户可以在线购买商品、加入购物车、下单、支付</font>
+ <font style="color:rgb(51, 51, 51);">用户可以对商品进行点赞以及评论已购买商品</font>
+ <font style="color:rgb(51, 51, 51);">管理员可以在后台管理商品的上下架、促销活动</font>
+ <font style="color:rgb(51, 51, 51);">管理员可以监控商品销售状况</font>
+ <font style="color:rgb(51, 51, 51);">客服可以在后台处理退款操作</font>
+ <font style="color:rgb(51, 51, 51);">希望未来 3 到 5 年可以支持千万用户的使用</font>

## <font style="color:rgb(51, 51, 51);">项目效果</font>
![1719405571119-4a52cc57-1f0a-44c2-b2db-caf841bbc2ec.png](./img/FW3mVLi4JOY03YXF/1719405571119-4a52cc57-1f0a-44c2-b2db-caf841bbc2ec-327585.png)

![1719405610567-060e94cf-c00b-4775-a567-891355ba1b91.png](./img/FW3mVLi4JOY03YXF/1719405610567-060e94cf-c00b-4775-a567-891355ba1b91-049558.png)

![1719405648500-004df352-8bc4-468e-aa77-0c0177569cc8.png](./img/FW3mVLi4JOY03YXF/1719405648500-004df352-8bc4-468e-aa77-0c0177569cc8-307560.png)

等等。

## 技术选型
### 前端技术
+ HTML：用于表示页面的结构，使用它里面常用的标签，比如：div、a、img 标签等等
+ CSS：用于给页面加样式，对页面进行美化
+ JavaScript：用于给页面加一些动作行为，比如：购物车数量的加减、总金额的计算等等
+ JSP：本质上是 Servlet，是一个动态的网页技术，可以动态展示后端传递的数据

### 后端技术
+ Servlet：服务端小程序，用于接收请求、响应结果
+ JDBC：用户操作数据库，对于数据库进行增删改查的操作

## 开发环境
+ IDEA：2019
+ JDK：1.8
+ MySQL：5.6
+ Tomcat：8.5

## 数据库设计
### 分析
![1719407430936-f1f731f9-c0c0-4a77-9d94-95e852e1e30d.png](./img/FW3mVLi4JOY03YXF/1719407430936-f1f731f9-c0c0-4a77-9d94-95e852e1e30d-554871.png)

分析页面中商品信息，我们需要设计一张商品表 goods，字段应该有：

| 字段名称 | 字段类型 | 说明 |
| --- | --- | --- |
| id | int | 主键、自增，商品编号 |
| name | varchar | 商品名称 |
| original_price | int | 原价 |
| current_price | int | 现价 |
| picture | varchar | 商品图片的路径 |
| create_date | date | 创建日期 |


### 创建数据库及表
![1719411093182-d27b17c8-e95f-429e-9f05-cb274f1c380c.png](./img/FW3mVLi4JOY03YXF/1719411093182-d27b17c8-e95f-429e-9f05-cb274f1c380c-376427.png)

![1719411170688-c03b0d31-2ccc-4362-aff7-133b97807599.png](./img/FW3mVLi4JOY03YXF/1719411170688-c03b0d31-2ccc-4362-aff7-133b97807599-571486.png)

![1719411208196-0defee7f-26d1-470c-8791-a4dca8805ec3.png](./img/FW3mVLi4JOY03YXF/1719411208196-0defee7f-26d1-470c-8791-a4dca8805ec3-428560.png)![1719413734655-5d9d579c-4a46-4104-bbe0-747dc426f044.png](./img/FW3mVLi4JOY03YXF/1719413734655-5d9d579c-4a46-4104-bbe0-747dc426f044-495139.png)

![1719411310374-5b7f325f-74ca-4d26-9999-0bc621989582.png](./img/FW3mVLi4JOY03YXF/1719411310374-5b7f325f-74ca-4d26-9999-0bc621989582-653921.png)

## 功能实现
### 创建 JavaEE 项目
![1719411479395-0249727b-6fac-4e09-8b9d-e10e5bab962d.png](./img/FW3mVLi4JOY03YXF/1719411479395-0249727b-6fac-4e09-8b9d-e10e5bab962d-476268.png)

![1719411517757-0af43a70-e698-46f8-af26-b5ca649b3029.png](./img/FW3mVLi4JOY03YXF/1719411517757-0af43a70-e698-46f8-af26-b5ca649b3029-984113.png)

![1719411556865-a17b4793-68e0-416c-b77e-057e8acc6ab2.png](./img/FW3mVLi4JOY03YXF/1719411556865-a17b4793-68e0-416c-b77e-057e8acc6ab2-650742.png)

![1719411581295-61a939ab-cedd-4920-a26f-1e2028180218.png](./img/FW3mVLi4JOY03YXF/1719411581295-61a939ab-cedd-4920-a26f-1e2028180218-285887.png)

### 导入 jar 包
**在 WEB-INF 文件夹中创建 lib 文件夹：**

![1719411655840-173b338b-025a-4c1f-b392-c3df6efeeb80.png](./img/FW3mVLi4JOY03YXF/1719411655840-173b338b-025a-4c1f-b392-c3df6efeeb80-176551.png)

![1719411677694-4dc9eab7-db4a-4ccc-a26a-5e2f1e03cd4f.png](./img/FW3mVLi4JOY03YXF/1719411677694-4dc9eab7-db4a-4ccc-a26a-5e2f1e03cd4f-890860.png)

**粘贴我们用的 3 个 jar 包到 lib 文件夹：**

![1719411786015-6aaf276c-94f1-43f0-a9cc-011ae4b7c3b1.png](./img/FW3mVLi4JOY03YXF/1719411786015-6aaf276c-94f1-43f0-a9cc-011ae4b7c3b1-868459.png)

**使 jar 包生效：**

![1719411873091-e35e9266-fb0b-4392-ae14-d5cccf8f6168.png](./img/FW3mVLi4JOY03YXF/1719411873091-e35e9266-fb0b-4392-ae14-d5cccf8f6168-452590.png)

![1719411889180-76dccff3-719e-413f-9968-275ac223e0f9.png](./img/FW3mVLi4JOY03YXF/1719411889180-76dccff3-719e-413f-9968-275ac223e0f9-942676.png)

**jar 包变成下图效果，说明生效：**

![1719411940370-fc97d83d-9c18-47d1-ac34-478bcb8c2d03.png](./img/FW3mVLi4JOY03YXF/1719411940370-fc97d83d-9c18-47d1-ac34-478bcb8c2d03-906097.png)

### 导入静态资源
将我们每个人选择的模板页面及资源复制粘贴到项目的 **web** 目录中。

![1719412461601-49ec7e29-8247-41ee-ac87-d58b811d8838.png](./img/FW3mVLi4JOY03YXF/1719412461601-49ec7e29-8247-41ee-ac87-d58b811d8838-050388.png)

最终效果：

![1719412526037-2b72489f-3b2f-4a70-98b0-3134a520b459.png](./img/FW3mVLi4JOY03YXF/1719412526037-2b72489f-3b2f-4a70-98b0-3134a520b459-292201.png)

### 编写实体类
实体类写在 com.xszx.bean 包中。

#### 编写实体类属性
```java
package com.xszx.bean;

import java.util.Date;

public class Goods {

    private Integer id;
    private String name;
    private Integer originalPrice;
    private Integer currentPrice;
    private String picture;
    private Date createDate;
}
```

#### 生成 set、get 方法
![1719413470481-6c83cc40-a296-48af-85a1-85b9b532503c.png](./img/FW3mVLi4JOY03YXF/1719413470481-6c83cc40-a296-48af-85a1-85b9b532503c-316862.png)

![1719413492457-13353ec7-8114-48ff-a533-e5c8ce3510fe.png](./img/FW3mVLi4JOY03YXF/1719413492457-13353ec7-8114-48ff-a533-e5c8ce3510fe-151023.png)

![1719413830643-de9f37fe-7534-4a53-8594-9e8017c7d721.png](./img/FW3mVLi4JOY03YXF/1719413830643-de9f37fe-7534-4a53-8594-9e8017c7d721-049903.png)

#### 最终效果
```java
package com.xszx.bean;

import java.util.Date;

public class Goods {

    private Integer id;
    private String name;
    private Integer originalPrice;
    private Integer currentPrice;
    private String picture;
    private Date createDate;

    public Integer getId() {
        return id;
    }

    public void setId(Integer id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public Integer getOriginalPrice() {
        return originalPrice;
    }

    public void setOriginalPrice(Integer originalPrice) {
        this.originalPrice = originalPrice;
    }

    public Integer getCurrentPrice() {
        return currentPrice;
    }

    public void setCurrentPrice(Integer currentPrice) {
        this.currentPrice = currentPrice;
    }

    public String getPicture() {
        return picture;
    }

    public void setPicture(String picture) {
        this.picture = picture;
    }

    public Date getCreateDate() {
        return createDate;
    }

    public void setCreateDate(Date createDate) {
        this.createDate = createDate;
    }
}
```

### 编写 dao 层代码
```java
package com.xszx.dao;

import com.xszx.bean.Goods;

import java.sql.*;
import java.util.ArrayList;
import java.util.List;

public class GoodsDao {

    public List<Goods> findAll(){
        Connection connection = null;
        List<Goods> list = null;
        try {
            // 加载数据库驱动
            Class.forName("com.mysql.jdbc.Driver");

            // 获取数据库连接, 数据库名称要改为自己的
            String url = "jdbc:mysql://localhost:3306/sxkj?useUnicode=true&characterEncoding=utf-8";
            String user = "root";
            String password = "root"; // 密码要改为自己的
            connection = DriverManager.getConnection(url, user, password);

            // 编写sql语句
            String sql = "select * from goods order by create_date desc limit 8";

            // 创建预编译语句对象
            PreparedStatement ps = connection.prepareStatement(sql);

            // 执行sql语句，得到结果集
            ResultSet rs = ps.executeQuery();

            // 遍历结果集，封装数据到list集合中
            list = new ArrayList<>();
            while(rs.next()){
                Goods goods = new Goods();
                goods.setId(rs.getInt("id"));
                goods.setName(rs.getString("name"));
                goods.setOriginalPrice(rs.getInt("original_price"));
                goods.setCurrentPrice(rs.getInt("current_price"));
                goods.setPicture(rs.getString("picture"));
                goods.setCreateDate(rs.getDate("create_date"));
                list.add(goods);
            }
        } catch (ClassNotFoundException e) {
            e.printStackTrace();
        } catch (SQLException e) {
            e.printStackTrace();
        } finally {
            // 关闭连接
            if(connection != null){
                try {
                    connection.close();
                } catch (SQLException e) {
                    e.printStackTrace();
                }
            }
        }

        return list;
    }
}
```

### 编写 controller 层代码
```java
package com.xszx.controller;

import com.xszx.bean.Goods;
import com.xszx.dao.GoodsDao;

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

        // 设置编码方式，防止中文乱码
        req.setCharacterEncoding("utf-8");
        resp.setContentType("text/html;charset=utf-8");
        resp.setCharacterEncoding("utf-8");

        // 调用 dao 层方法
        GoodsDao goodsDao = new GoodsDao();
        List<Goods> list = goodsDao.findAll();

        // 将数据放入到 request 域对象中
        req.setAttribute("list", list);

        // 将请求转发到 index.jsp 页面
        req.getRequestDispatcher("index.jsp").forward(req, resp);
    }
}
```

### 删除页面及更改后缀
删除原有的 index.jsp 页面。

![1719414638175-e2f2be76-5c87-445f-bbaf-4d7c039f2fc7.png](./img/FW3mVLi4JOY03YXF/1719414638175-e2f2be76-5c87-445f-bbaf-4d7c039f2fc7-176867.png)

修改 index.html 文件的后缀，改为 index.jsp

![1719414703665-e7aa4a5b-61f9-4c75-81e3-80816cc4292f.png](./img/FW3mVLi4JOY03YXF/1719414703665-e7aa4a5b-61f9-4c75-81e3-80816cc4292f-180084.png)

![1719414738760-98748c39-cb81-466b-813b-8ccc438e2e92.png](./img/FW3mVLi4JOY03YXF/1719414738760-98748c39-cb81-466b-813b-8ccc438e2e92-018086.png)

![1719414808499-1970fcf5-ef58-4227-b7c7-425a24ae469f.png](./img/FW3mVLi4JOY03YXF/1719414808499-1970fcf5-ef58-4227-b7c7-425a24ae469f-281049.png)

### 修改页面代码
在 index.jsp 页面中顶部加入下面两行代码：

```html
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<%@ taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>
```

![1719414962893-a681ea6b-3ad0-4cc1-bb66-bd97615fb65f.png](./img/FW3mVLi4JOY03YXF/1719414962893-a681ea6b-3ad0-4cc1-bb66-bd97615fb65f-795604.png)

删除多余的 li 元素：

![1719415180697-54df8cb0-e255-46c8-88da-4c44afb42429.png](./img/FW3mVLi4JOY03YXF/1719415180697-54df8cb0-e255-46c8-88da-4c44afb42429-183255.png)

使用 c:forEach 循环展示数据：

```html
<c:forEach items="${list}" var="g">
  <li class="product design">
    <a href="#">
      <img src="${g.picture}" alt="Product" />
      <h5>${g.name}</h5>
      <span class="price"><del>￥${g.originalPrice}</del>￥${g.currentPrice}</span>
    </a>
    <div class="wishlist-box">
      <a href="#"><i class="fa fa-arrows-alt"></i></a>
      <a href="#"><i class="fa fa-heart-o"></i></a>
      <a href="#"><i class="fa fa-search"></i></a>
    </div>
    <a href="#" class="addto-cart" title="Add To Cart">加入购物车</a>
  </li><!-- Product /- -->
</c:forEach>
```

images/product-1.jpg

### 数据库插入测试数据


### 启动服务器访问
![1719415389778-75ccdf91-6563-41b2-b128-7c1e38150096.png](./img/FW3mVLi4JOY03YXF/1719415389778-75ccdf91-6563-41b2-b128-7c1e38150096-273862.png)

![1719545818364-78287189-4595-4891-8f41-ed807fedcee6.png](./img/FW3mVLi4JOY03YXF/1719545818364-78287189-4595-4891-8f41-ed807fedcee6-532165.png)

# 五、提交的资料
## 项目源码
![1719545880667-c23604a0-3066-439c-9784-2794912c5365.png](./img/FW3mVLi4JOY03YXF/1719545880667-c23604a0-3066-439c-9784-2794912c5365-526944.png)

将项目复制到桌面，然后将项目打包，比如：xxx.zip、xxx.rar

## 数据库文件
![1719545962013-946fbc34-09ef-4f82-b33a-d028db8c080c.png](./img/FW3mVLi4JOY03YXF/1719545962013-946fbc34-09ef-4f82-b33a-d028db8c080c-095356.png)

![1719545989893-3e54aee6-1404-4d49-9e0e-73ad87a1babd.png](./img/FW3mVLi4JOY03YXF/1719545989893-3e54aee6-1404-4d49-9e0e-73ad87a1babd-888618.png)

![1719546010998-b734a535-2f99-428f-9afb-5ce0b75b24c7.png](./img/FW3mVLi4JOY03YXF/1719546010998-b734a535-2f99-428f-9afb-5ce0b75b24c7-264733.png)

![1719546027951-a529b632-3808-47e8-a596-148129de66aa.png](./img/FW3mVLi4JOY03YXF/1719546027951-a529b632-3808-47e8-a596-148129de66aa-829774.png)

## 实训报告\答辩的 PPT
如果学校发了《实训报告》，那我们就只需要写好《实训报告》，根据它答辩就行。

如果学校没发《实训报告》，那需要每个同学写一份答辩的 PPT。包含但不限于：项目背景、项目介绍、技术选型、实现功能、遇到的问题及解决办法、总结、感悟、心得等等。





> 更新: 2024-06-28 18:06:12  
> 原文: <https://www.yuque.com/u41736172/az9urv/oq6hzg9uyy5anoy9>