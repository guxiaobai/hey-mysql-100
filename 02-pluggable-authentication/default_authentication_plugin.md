|本期版本| 上期版本
|:---:|:---:
`Sat May  2 20:29:36 CST 2026` | -

### ✔️ 总结一句话

`default_authentication_plugin` 只是“默认值提供者”，只在 `CREATE/ALTER USER` 没指定插件时才生效，对已有用户和认证过程本身都不直接影响。



## [`default_authentication_plugin`](https://dev.mysql.com/doc/refman/8.0/en/server-system-variables.html#sysvar_default_authentication_plugin)

```bash
SHOW VARIABLES LIKE 'default_authentication_plugin';
```

```ini
[mysqld]
default_authentication_plugin=mysql_native_password
```

```bash
echo 'default_authentication_plugin=mysql_native_password' | sudo tee -a /etc/mysql/mysql.conf.d/mysqld.cnf
```



## [Features Removed in MySQL 8.4](https://dev.mysql.com/doc/refman/8.4/en/mysql-nutshell.html#mysql-nutshell-removals)

- The `default_authentication_plugin` system variable, deprecated in MySQL 8.0.27, is removed as of MySQL 8.4.0. Use [`authentication_policy`](https://dev.mysql.com/doc/refman/8.4/en/server-system-variables.html#sysvar_authentication_policy) instead.






## Ref

- <https://dev.mysql.com/doc/refman/8.0/en/pluggable-authentication.html>