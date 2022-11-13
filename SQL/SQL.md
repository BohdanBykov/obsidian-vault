 ***

# Structured Query Language
	 Used to create databases


## Commands:

### - create user
```sh
mysql> CREATE USER 'john'@'1.1.1.1' IDENTIFIED BY 'password';
Query OK, 0 rows affected (0.02 sec)
```

### - set password
```sh
mysql> ALTER USER 'john'@'1.1.1.1' IDENTIFIED BY 'password'
    -> ;
Query OK, 0 rows affected (0.05 sec)

```

### - give permissions to the user
```sh
mysql> GRANT CREATE, DROP, SELECT, UPDATE, DELETE on database to 'john'@'1.1.1.1';
Query OK, 0 rows affected (0.01 sec)

mysql> FLUSH PRIVILEGES;
Query OK, 0 rows affected (0.01 sec)

mysql> SHOW GRANTS FOR 'john'@'1.1.1.1';
+-------------------------------------------------------------------------------+
| Grants for site@172.17.0.1                                                               |
+-------------------------------------------------------------------------------+
| GRANT USAGE ON *.* TO `site`@`1.1.1.1`                                                |
| GRANT SELECT, UPDATE, DELETE, CREATE, DROP ON `database`.`table` TO `john`@`1.1.1.1` |
+-------------------------------------------------------------------------------+
2 rows in set (0.00 sec)

mysql> 
```

### - remove permission
```sh
mysql> REVOKE SELECT, DELETE, CREATE, DROP ON database.table FROM 'site'@'1.1.1.';
Query OK, 0 rows affected (0.05 sec)

mysql> 
```

### - show  user permissions
```sh
mysql> SHOW GRANTS FOR 'john'@'1.1.1.1';
+-------------------------------------------------------------------------------+
| Grants for john@1.1.1.1                                                               |
+-------------------------------------------------------------------------------+
| GRANT USAGE ON *.* TO `john`@`1.1.1.1`                                                |
| GRANT SELECT, UPDATE, DELETE, CREATE, DROP ON `database`.`table` TO `john`@`1.1.1.1` |
+-------------------------------------------------------------------------------+
2 rows in set (0.00 sec)

mysql> 
```

### - create database
```sh
mysql> create database qwerty;
Query OK, 1 row affected (0.02 sec)
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| qwerty             |
| sys                |
| testdb             |
+--------------------+
6 rows in set (0.01 sec)

mysql> 
```

### - delete database
```sh
mysql> drop database qwerty;
Query OK, 0 rows affected (0.03 sec)

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sys                |
| testdb             |
+--------------------+
5 rows in set (0.00 sec)

mysql> 
```

### - use database
```sh
mysql> use testdb;
Database changed
mysql> 
```

### - show tables of the db
```sh
mysql> show tables;
Empty set (0.00 sec)

mysql> 
```

### - create table user
```sh
mysql> create table user(
    -> user_id int auto_increment primary key,
    -> firstname varchar(100),
    -> lastname varchar(100)
    -> );
Query OK, 0 rows affected (0.04 sec)

mysql> show tables;
+------------------+
| Tables_in_testdb |
+------------------+
| user             |
+------------------+
1 row in set (0.00 sec)
```

### - input data into table
```sh
mysql> insert into user (firstname, lastname) values("fname", "lname");
Query OK, 1 row affected (0.02 sec)

```

### - show all table data
```sh
mysql> select * from user;
+---------+-----------+----------+
| user_id | firstname | lastname |
+---------+-----------+----------+
|       1 | fname     | lname    |
+---------+-----------+----------+
1 row in set (0.00 sec)

mysql> 
```
### 