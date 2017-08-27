
# JDBC ：数据库连接池（connection pool）
数据库连接池的基本思想就是为数据库连接建立一个“缓冲池”。预先在缓冲池中放入一定数量的连接，当需要建立数据库连接时，只需从“缓冲池”中取出一个，
使用完毕之后再放回去。
- 数据库连接池负责分配、管理和释放数据库连接，它允许应用程序重复使用一个现有的数据库连接，而不是重新建立一个。
- 数据库连接池在初始化时将创建一定数量的数据库连接放到连接池中，这些数据库连接的数量是由最小数据库连接数来设定的。

JAVA访问数据库的解决方案
连接步骤步骤如下：
- 1.加载驱动类;
- 2.与数据库建立连接；
- 3.执行SQL语句
- 4.处理结果集
- 5.关闭连接

## 第一步：加载驱动类
不同的数据库，参照的字符串不同，ORACLE的连接为：Class.forName("oracle.jdbc.driver.OracleDriver");
这一步执行后，程序可能会抛出： ClassNotFoundException，原因一般有：  
a. 数据库的驱动jar包没有导入到环境变量中  
b. Class.forName中的字符串拼写不正确  
eg：
1) MySQL(http://www.mysql.com)
> Class.forName( "org.gjt.mm.mysql.Driver" );
> cn = DriverManager.getConnection( "jdbc:mysql://MyDbComputerNameOrIP:3306/myDatabaseName", sUsr, sPwd );

2) Oracle(http://www.oracle.com/ip/deploy/database/oracle9i/)classes12.zip
> Class.forName( "com.sybase.jdbc2.jdbc.SybDriver" );
> cn = DriverManager.getConnection( "jdbc:sybase:Tds:MyDbComputerNameOrIP:2638", sUsr, sPwd );
> //(Default-Username/Password: "dba"/"sql")

引用JDBC连接数据库的方法汇总
<http://www.jb51.net/article/91011.htm>


## 两种开源的数据库连接池
JDBC的数据库连接池使用 javax.sql.DataSource 来表示，DataSource 只是一个接口，该接口通常由服务器(Weblogic, WebSphere, Tomcat)提供实现，
也有一些开源组织提供实现：

## DBCP 数据库连接池
 DBCP 是 Apache软件基金组织下的开源连接池实现，该连接池依赖该组织下的另一个开源系统：Common-pool. 如需使用该连接池实现，
 应在系统中增加如下两个 jar 文件：
– Commons-dbcp.jar：连接池的实现
– Commons-pool.jar：连接池实现的依赖库

- Tomcat 的连接池正是采用该连接池来实现的，该数据库连接池既可以与应用服务器整合使用，也可由应用程序独立使用。  

- C3P0 数据库连接池
通常被称为数据源，它包含连接池和连接池管理两个部分，习惯上也经常把 DataSource 称为连接池

## JDBC执行存储过程的四种情况
1)只有输入IN参数，没有输出OUT参数
2)既有输入IN参数，也有输出OUT参数，输出是简单值（非列表）
3)既有输入IN参数，也有输出OUT参数，输出是列表
4)输入输出参数是同一个（IN OUT）


