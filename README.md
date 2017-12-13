# Spring

# 使用SpringBoot 来集成 Spring SpringMVC Mybatis
## 核心需要的配置:

### Core 配置类中 所需要贴的注解:
*@Configuration : 把此类当做配置类 <br>
*@EnableAutoConfiguration : 开启自动扫描配置<br>
*@ComponentScan : 扫描当前目录下所有的包(IoC注解)<br>
*@MapperScan(basePackages = "com.szl.p2p.base.mapper") : 扫描mapper接口 文件<br>
*@EnableTransactionManagement : 启动事务注解<br>

## application.properties 配置文件中 需配置的东西:

### 端口配置,默认8080:
*server.port=80 ;<br>

### 数据库连接池:
*spring.datasource.type=com.alibaba.druid.pool.DruidDataSource  :  //数据库连接池类型<br>
*spring.datasource.driver-class-name=com.mysql.jdbc.Driver  :  //数据库连接池的驱动<br>
*spring.datasource.url=mysql:jdbc://localhost:3306/p2p  :  //要连接的数据库<br>
*spring.datasource.username=root  :  //数据库账号<br>
*spring.datasource.password=admin  :  //数据库密码<br>

### Mybatis配置:
*mybatis.config-location=classpath:mybatis-config.xml  :  // 引入mybatis的配置文件<br>
*mybatis.mapper-locations=classpath:com/szl/p2p/base/mapper/*Mapper.xml  :  // 扫描Mapper.xml文件<br>
*mybatis.type-aliases-package=com.szl.p2p.base.domain  :  // 给包加别名(简单类名)<br>

### 日志:
*logging.level.root=info  //全局日志级别<br>
*logging.level.com.szl.p2p.base.mapper=trace  // mapper操作sql的日志级别<br>
