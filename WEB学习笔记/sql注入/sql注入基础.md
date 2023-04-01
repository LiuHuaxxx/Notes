# sql注入基础

## 一.注入思路

1. 判断是否存在注入，注入的类型是字符型，数字型还是搜索型

2. 猜解SQL查询语句中的字段数

3. 确定显示的字段顺序

4. 获取当前数据库

5. 获取数据库中的表

6. 获取数据库中的字段名

7. 查询数据

---

## 二.基础

1. **查库**

```sql
select schema_name from information_schema.schemata;
```

2. 查表

```sql
select table_name from information_schema.tables where table_schema=‘表名’;
```

3. 查列

```sql
select column_name from information_schema.columns where table_schema='表名';
```

4. 查字段

```sql
select 列名，列名 from 库名.列名
```


