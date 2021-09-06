##  idea
### idea plugin

1. alibaba
2. free mybatis
3. lombok
4. maven helper
5. plantUml
6. translation

## maven
### maven常用依赖包
```xml
<dependency>
    <groupId>com.alibaba</groupId>
    <artifactId>fastjson</artifactId>
    <version>1.2.70</version>
</dependency>

<dependency>
    <groupId>cn.hutool</groupId>
    <artifactId>hutool-all</artifactId>
    <version>5.5.7</version>
</dependency>
```

### mybatis本地打印sql

```properties
1.resource下新建文件 mybatis-config.xml 内容如下
```

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE configuration
        PUBLIC "-//mybatis.org//DTD Config 3.0//EN"
        "http://mybatis.org/dtd/mybatis-3-config.dtd">
<configuration>
    <settings>
        <!-- 打印查询语句 -->
        <setting name="logImpl" value="STDOUT_LOGGING" />
    </settings>
</configuration>
```

```properties
2.application.yml中新增 配置
```

```yml
mybatis:
  config-location: classpath:mybatis-config.xml
```

### 建表sql

```sql
CREATE TABLE `x_demo` (
`id` BIGINT (20) NOT NULL AUTO_INCREMENT COMMENT '自增ID',
`tenant_id` VARCHAR (32) NOT NULL COMMENT 'x',
`session_id` VARCHAR (64) DEFAULT NULL COMMENT 'x',
`cellphone` VARCHAR (45) NOT NULL COMMENT 'x',
`customer_name` VARCHAR (128) DEFAULT NULL COMMENT 'x',
`create_time` datetime NOT NULL COMMENT 'x',
`update_time` datetime DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP COMMENT 'x',
`delete_time` datetime DEFAULT NULL COMMENT 'x',
`is_deleted` TINYINT (1) NOT NULL DEFAULT '0' COMMENT '是否已删除(1-已删除；0-未删除)',
PRIMARY KEY (`id`) USING BTREE
) ENGINE = INNODB DEFAULT CHARSET = utf8mb4 COMMENT = 'x';
```

