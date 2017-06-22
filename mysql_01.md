# SQL指令

## 创建数据库

        注意：创建数据库之前要先连接Mysql服务器
        命令：create database <数据库名>
        例1：建立一个名为xhkdb的数据库 mysql> create database stu;

## 显示数据库

        show databases （注意：最后有个s） mysql> show databases;
        
## 删除数据库

        drop database <数据库名> 例如：删除名为 xhkdb的数据库 mysql> drop database xhkdb;
## 使用数据库

        命令： use <数据库名>

## 创建数据表

命令：create table <表名> ( <字段名1> <类型1> [,..<字段名n> <类型n>]);

```sql
mysql> create table information(sno char(15) not null primary key,sname char(20),sage int default 20,schoolno char(15),foreign key (schoolno) references school(schoolno));
```

## 显示数据库中的表

在use数据库的情况下

        命令：show tables;
        
## 表结构

    desc 表名 //查看表格结构

## 删除表

    命令：drop table <表名>

## 表插入数据

    命令：insert into <表名> [( <字段名1>[,..<字段名n > ])] values ( 值1 )[, ( 值n )]
    insert into course(cno,cname) values('01','java');

## 查询表中的数据

    查询所有行 命令： select <字段1，字段2，...> from < 表名 > where < 表达式 > 
    select * frmo course where cno = '01';

## 修改表中数据

    update 表名 set 字段=新值,... where 条件 
    update MyClass set name='Mary' where id=1;
