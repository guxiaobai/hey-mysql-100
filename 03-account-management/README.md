## Account Management

|本期版本| 上期版本
|:---:|:---:
`Mon May  9 14:58:44 CST 2022` | -

###  如何让 root 用户可以远程登陆

[15.7.1.1 ALTER USER Statement](https://dev.mysql.com/doc/refman/8.4/en/alter-user.html)

```bash
# 认证插件
sudo mysql -u root -e "ALTER USER 'root'@'localhost' IDENTIFIED WITH caching_sha2_password by '';"
```


[15.7.1.7 RENAME USER Statement](https://dev.mysql.com/doc/refman/8.4/en/rename-user.html)

```bash
# 主机名
sudo mysql -u root -e "RENAME USER 'root'@'localhost' TO 'root'@'%';"
```

[`bind_address`](https://dev.mysql.com/doc/refman/8.0/en/server-system-variables.html#sysvar_bind_address)


```
SHOW VARIABLES LIKE 'bind%';
```

```bash
sudo sed -i -r 's/(^bind-address\s+).*/\1= 0.0.0.0/g' /etc/mysql/mysql.conf.d/mysqld.cnf
sudo systemctl restart mysql.service
```