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

