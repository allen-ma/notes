# Spring Cloud工程搭建

代码构建

- 约定>配置>编码

## 总父工程

project

	- module

父工程步骤

- New Project
- 聚合总父工程名字
- Maven选版本
- 工程名字
- 字符编码
  - Editor->File Encodings:全改成UTF-8，勾选Transparent native-to-ascii conversion

- 注解生效激活
  - Build,Execution,Deployment->Compiler->Annotation Processors:勾选Enable antiontation processing
- java编辑版本选8
  - Build,Execution,Deployment->Java Compiler:Target bytecode version:8
- File Type过滤

## 父工程pom文件

DependencyManagemen和Dependencies

## 支付模块的构建

1. 建model

2. 改pom

3. 写yml

4. 主启动

5. 业务类

业务模块流程

1. 建表SQL
2. entity
3. dao
4. service
5. controller

## 热部署Devtools

1. Adding devtools to your project(子工程)

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-devtools</artifactId>
    <scope>runtime</scope>
    <optional>true</optional>
</dependency>
```

2. Adding plugin to your pom.xml(父工程)

```xml
<build>
    <plugins>
        <plugin>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-maven-plugin</artifactId>
            <version>2.3.0.RELEASE</version>
            <configuration>
                <fork>true</fork>
                <addResources>true</addResources>
            </configuration>
        </plugin>
    </plugins>
</build>
```

## 订单模块构建

订单模块调用支付模块

## 工程重构

新建common模块，将实体类抽取出来

将common模块clean，install

在需要的地方其maven坐标引入









