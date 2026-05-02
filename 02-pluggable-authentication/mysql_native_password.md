## 8.4.1.1 Native Pluggable Authentication

> mysql_native_password 认证插件自 MySQL 8.0.34 起被弃用，MySQL 8.4 默认禁用，MySQL 9.0.0 起移除。



服务器端插件内置于服务器中，但 默认情况下已禁用。要启用它

```ini
[mysqld]
mysql_native_password=ON
```



MySQL 8.4（及更高版本）中的 MySQL 客户端程序使用 caching_sha2_password 默认认证

```bash
mysql --default-auth=mysql_native_password ...
```



## Ref



- <https://dev.mysql.com/doc/refman/8.4/en/native-pluggable-authentication.html>
