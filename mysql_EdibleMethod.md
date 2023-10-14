# mysql食用说明

## 库操作

`mysql -u root -p`:连接本地数据库

`show databases;`:查看当前的数据库

`create database 库名`:建立名字为XXX的数据库

`drop database 库名`:删除名字为XXX的数据库

`mysqldump -u root -p 库名 > XXX.sql`:XXX数据库导出(在系统中执行,而非在mysql终端里)

`mysql -u root -p 库名 < XXX.sql`:数据库导入(在系统中执行,而非在mysql终端里)

## 表操作

`create table 表名()`:创建名字为XXX的表

`desc 表名`:查看名字为XXX表

`alter table 表名 modify column 列名 数据结构`:操作表中变量修改其的数据结构

`alter table 表名 rename column 列名 to 新列名`:操作表中的变量修改其的变量名称

`alter table 表名 add column 字段 数据结构`:新建表中一个变量,并为其设置一个数据结构

`alter table 表名 drop column 字段`:删除表中的变量

`drop table 表名`:删除表

`insert into 表名(列名) alues (列名的数值(一一对应))`:初始化表中的变量的数值

`select * from 表名;`:查看表中的数值

<!-- `\connect root@localhost`:连接本地数据库 -->