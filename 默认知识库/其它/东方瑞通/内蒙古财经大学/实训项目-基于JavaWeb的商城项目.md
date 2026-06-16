# 实训项目-基于 JavaWeb 的商城项目

# 项目介绍
## 项目介绍
+ <font style="color:rgb(51, 51, 51);">该商城是一个全品类的电商购物网站（B2C）</font>
+ <font style="color:rgb(51, 51, 51);">用户可以在线购买商品、加入购物车、下单、支付</font>
+ <font style="color:rgb(51, 51, 51);">用户可以对商品进行点赞以及评论已购买商品</font>
+ <font style="color:rgb(51, 51, 51);">管理员可以在后台管理商品的上下架、促销活动</font>
+ <font style="color:rgb(51, 51, 51);">管理员可以监控商品销售状况</font>
+ <font style="color:rgb(51, 51, 51);">客服可以在后台处理退款操作</font>
+ <font style="color:rgb(51, 51, 51);">希望未来 3 到 5 年可以支持千万用户的使用</font>

## <font style="color:rgb(51, 51, 51);">项目效果</font>
![1719405571119-4a52cc57-1f0a-44c2-b2db-caf841bbc2ec.png](./img/s71mE7pPNSXM61Nw/1719405571119-4a52cc57-1f0a-44c2-b2db-caf841bbc2ec-765364.png)

![1719405610567-060e94cf-c00b-4775-a567-891355ba1b91.png](./img/s71mE7pPNSXM61Nw/1719405610567-060e94cf-c00b-4775-a567-891355ba1b91-116736.png)

![1719405648500-004df352-8bc4-468e-aa77-0c0177569cc8.png](./img/s71mE7pPNSXM61Nw/1719405648500-004df352-8bc4-468e-aa77-0c0177569cc8-645652.png)

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

# 数据库设计
## 分析
![1719407430936-f1f731f9-c0c0-4a77-9d94-95e852e1e30d.png](./img/s71mE7pPNSXM61Nw/1719407430936-f1f731f9-c0c0-4a77-9d94-95e852e1e30d-980277.png)

分析页面中商品信息，我们需要设计一张商品表 goods，字段应该有：

| 字段名称 | 字段类型 | 说明 |
| --- | --- | --- |
| id | int | 主键、自增，商品编号 |
| name | varchar | 商品名称 |
| originalprice | int | 原价 |
| currentprice | int | 现价 |
| picture | varchar | 商品图片的路径 |


## 创建数据库及表
![1719411093182-d27b17c8-e95f-429e-9f05-cb274f1c380c.png](./img/s71mE7pPNSXM61Nw/1719411093182-d27b17c8-e95f-429e-9f05-cb274f1c380c-795042.png)

![1719411170688-c03b0d31-2ccc-4362-aff7-133b97807599.png](./img/s71mE7pPNSXM61Nw/1719411170688-c03b0d31-2ccc-4362-aff7-133b97807599-993850.png)

![1719411208196-0defee7f-26d1-470c-8791-a4dca8805ec3.png](./img/s71mE7pPNSXM61Nw/1719411208196-0defee7f-26d1-470c-8791-a4dca8805ec3-983019.png)

![1726190652925-973c8f65-5870-4d78-a287-c31ed84fd47e.png](./img/s71mE7pPNSXM61Nw/1726190652925-973c8f65-5870-4d78-a287-c31ed84fd47e-603640.png)

![1719411310374-5b7f325f-74ca-4d26-9999-0bc621989582.png](./img/s71mE7pPNSXM61Nw/1719411310374-5b7f325f-74ca-4d26-9999-0bc621989582-360442.png)

# 功能实现
## 创建 JavaEE 项目
![1719411479395-0249727b-6fac-4e09-8b9d-e10e5bab962d.png](./img/s71mE7pPNSXM61Nw/1719411479395-0249727b-6fac-4e09-8b9d-e10e5bab962d-187712.png)

![1719411517757-0af43a70-e698-46f8-af26-b5ca649b3029.png](./img/s71mE7pPNSXM61Nw/1719411517757-0af43a70-e698-46f8-af26-b5ca649b3029-290344.png)

![1719411556865-a17b4793-68e0-416c-b77e-057e8acc6ab2.png](./img/s71mE7pPNSXM61Nw/1719411556865-a17b4793-68e0-416c-b77e-057e8acc6ab2-555101.png)

![1719411581295-61a939ab-cedd-4920-a26f-1e2028180218.png](./img/s71mE7pPNSXM61Nw/1719411581295-61a939ab-cedd-4920-a26f-1e2028180218-331303.png)

## 导入 jar 包
**在 WEB-INF 文件夹中创建 lib 文件夹：**

![1719411655840-173b338b-025a-4c1f-b392-c3df6efeeb80.png](./img/s71mE7pPNSXM61Nw/1719411655840-173b338b-025a-4c1f-b392-c3df6efeeb80-189772.png)

![1719411677694-4dc9eab7-db4a-4ccc-a26a-5e2f1e03cd4f.png](./img/s71mE7pPNSXM61Nw/1719411677694-4dc9eab7-db4a-4ccc-a26a-5e2f1e03cd4f-620567.png)

**粘贴我们用的 4 个 jar 包到 lib 文件夹：**

![1726190802583-ce51eb44-069c-419b-829e-4622cbb4f6b6.png](./img/s71mE7pPNSXM61Nw/1726190802583-ce51eb44-069c-419b-829e-4622cbb4f6b6-984765.png)

**使 jar 包生效：**

![1726190850254-0f352f88-b1fb-463d-8080-5635d26b00e4.png](./img/s71mE7pPNSXM61Nw/1726190850254-0f352f88-b1fb-463d-8080-5635d26b00e4-188073.png)

![1726190863985-dd887b78-5b3c-450e-9b68-2173b53c59aa.png](./img/s71mE7pPNSXM61Nw/1726190863985-dd887b78-5b3c-450e-9b68-2173b53c59aa-274746.png)

**jar 包变成下图效果，说明生效：**

![1726190884654-3fb3f51b-e803-49bd-80fb-a1aa21d8969e.png](./img/s71mE7pPNSXM61Nw/1726190884654-3fb3f51b-e803-49bd-80fb-a1aa21d8969e-925309.png)

## 导入静态资源
将我们每个人选择的模板页面及资源复制粘贴到项目的 **web** 目录中。

![1719412461601-49ec7e29-8247-41ee-ac87-d58b811d8838.png](./img/s71mE7pPNSXM61Nw/1719412461601-49ec7e29-8247-41ee-ac87-d58b811d8838-819783.png)

最终效果：

![1719412526037-2b72489f-3b2f-4a70-98b0-3134a520b459.png](./img/s71mE7pPNSXM61Nw/1719412526037-2b72489f-3b2f-4a70-98b0-3134a520b459-769743.png)

## 创建包结构
![1726191585309-75b70d38-059d-4405-a293-7422cd6da7b0.png](./img/s71mE7pPNSXM61Nw/1726191585309-75b70d38-059d-4405-a293-7422cd6da7b0-273813.png)

## 编写工具类
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

        String url = "jdbc:mysql:///mall?useUnicode=true&characterEncoding=utf8";
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

## 编写实体类
在 pojo 包中编写实体类。

```java
package com.lhp.pojo;

public class Goods {

    private int id;
    private String name;
    private int originalprice;
    private int currentprice;
    private String picture;

    public Goods() {
    }

    public Goods(int id, String name, int originalprice, int currentprice, String picture) {
        this.id = id;
        this.name = name;
        this.originalprice = originalprice;
        this.currentprice = currentprice;
        this.picture = picture;
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

    public int getOriginalprice() {
        return originalprice;
    }

    public void setOriginalprice(int originalprice) {
        this.originalprice = originalprice;
    }

    public int getCurrentprice() {
        return currentprice;
    }

    public void setCurrentprice(int currentprice) {
        this.currentprice = currentprice;
    }

    public String getPicture() {
        return picture;
    }

    public void setPicture(String picture) {
        this.picture = picture;
    }

    @Override
    public String toString() {
        return "Goods{" +
                "id=" + id +
                ", name='" + name + '\'' +
                ", originalprice=" + originalprice +
                ", currentprice=" + currentprice +
                ", picture='" + picture + '\'' +
                '}';
    }
}
```

## 编写 dao 层代码
```java
package com.lhp.dao;

import com.lhp.pojo.Goods;
import com.lhp.utils.JDBCUtils;
import org.apache.commons.dbutils.QueryRunner;
import org.apache.commons.dbutils.handlers.BeanListHandler;

import java.sql.Connection;
import java.sql.SQLException;
import java.util.List;

public class GoodsDao {

    // 查询所有的商品
    public List<Goods> findAll(){

        // 1.获取数据库连接
        Connection connection = JDBCUtils.getConnection();

        // 2.编写sql语句
        String sql = "select * from goods limit 0, 8";

        // 3.创建QueryRunner对象
        QueryRunner queryRunner = new QueryRunner();

        // 4.调用方法执行sql语句
        List<Goods> list = null;
        try {
            list = queryRunner.query(connection, sql, new BeanListHandler<>(Goods.class));
        } catch (SQLException e) {
            e.printStackTrace();
        }

        // 5.关闭连接
        JDBCUtils.closeConnection(connection);
        
        return list;
    }
}
```

## 编写 controller 层代码
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
import java.util.List;

@WebServlet("/findAll")
public class FindAllServlet extends HttpServlet {

    @Override
    protected void service(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

        // 设置编码方式
        req.setCharacterEncoding("utf-8");
        resp.setCharacterEncoding("utf-8");
        resp.setContentType("text/html;charset=utf-8");

        // 调用dao层方法
        GoodsDao goodsDao = new GoodsDao();
        List<Goods> list = goodsDao.findAll();

        // 将数据放入request域对象中
        req.setAttribute("list", list);

        // 转发到index.jsp
        req.getRequestDispatcher("/index.jsp").forward(req, resp);
    }
}
```

## 删除页面及更改后缀
删除原有的 index.jsp 页面。

![1719414638175-e2f2be76-5c87-445f-bbaf-4d7c039f2fc7.png](./img/s71mE7pPNSXM61Nw/1719414638175-e2f2be76-5c87-445f-bbaf-4d7c039f2fc7-808370.png)`

修改 index.html 文件的后缀，改为 index.jsp

![1719414703665-e7aa4a5b-61f9-4c75-81e3-80816cc4292f.png](./img/s71mE7pPNSXM61Nw/1719414703665-e7aa4a5b-61f9-4c75-81e3-80816cc4292f-033991.png)

![1719414738760-98748c39-cb81-466b-813b-8ccc438e2e92.png](./img/s71mE7pPNSXM61Nw/1719414738760-98748c39-cb81-466b-813b-8ccc438e2e92-460982.png)

![1719414808499-1970fcf5-ef58-4227-b7c7-425a24ae469f.png](./img/s71mE7pPNSXM61Nw/1719414808499-1970fcf5-ef58-4227-b7c7-425a24ae469f-011649.png)

## 修改页面代码
在 index.jsp 页面中顶部加入下面两行代码：

```html
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<%@ taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>
```

![1719414962893-a681ea6b-3ad0-4cc1-bb66-bd97615fb65f.png](./img/s71mE7pPNSXM61Nw/1719414962893-a681ea6b-3ad0-4cc1-bb66-bd97615fb65f-552766.png)

删除多余的 li 元素：

![1719415180697-54df8cb0-e255-46c8-88da-4c44afb42429.png](./img/s71mE7pPNSXM61Nw/1719415180697-54df8cb0-e255-46c8-88da-4c44afb42429-586815.png)

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

## 数据库插入测试数据


## 启动服务器访问
![1719415389778-75ccdf91-6563-41b2-b128-7c1e38150096.png](./img/s71mE7pPNSXM61Nw/1719415389778-75ccdf91-6563-41b2-b128-7c1e38150096-734849.png)

![1719545818364-78287189-4595-4891-8f41-ed807fedcee6.png](./img/s71mE7pPNSXM61Nw/1719545818364-78287189-4595-4891-8f41-ed807fedcee6-448693.png)

# 提交的资料
## 项目源码
![1719545880667-c23604a0-3066-439c-9784-2794912c5365.png](./img/s71mE7pPNSXM61Nw/1719545880667-c23604a0-3066-439c-9784-2794912c5365-424726.png)

将项目复制到桌面，然后将项目打包，比如：xxx.zip、xxx.rar

## 数据库文件
![1719545962013-946fbc34-09ef-4f82-b33a-d028db8c080c.png](./img/s71mE7pPNSXM61Nw/1719545962013-946fbc34-09ef-4f82-b33a-d028db8c080c-020666.png)

![1719545989893-3e54aee6-1404-4d49-9e0e-73ad87a1babd.png](./img/s71mE7pPNSXM61Nw/1719545989893-3e54aee6-1404-4d49-9e0e-73ad87a1babd-638467.png)

![1719546010998-b734a535-2f99-428f-9afb-5ce0b75b24c7.png](./img/s71mE7pPNSXM61Nw/1719546010998-b734a535-2f99-428f-9afb-5ce0b75b24c7-359602.png)

![1719546027951-a529b632-3808-47e8-a596-148129de66aa.png](./img/s71mE7pPNSXM61Nw/1719546027951-a529b632-3808-47e8-a596-148129de66aa-334697.png)

## 实训报告\答辩的 PPT
如果学校发了《实训报告》，那我们就只需要写好《实训报告》，根据它答辩就行。

如果学校没发《实训报告》，那需要每个同学写一份答辩的 PPT。包含但不限于：项目背景、项目介绍、技术选型、实现功能、遇到的问题及解决办法、总结、感悟、心得等等。



> 更新: 2024-09-13 16:37:09  
> 原文: <https://www.yuque.com/u41736172/az9urv/nxgot4btrrc25ih1>