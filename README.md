# Hey MySQL 100

## 组件安装

| 名称                           | 说明                      |
| ------------------------------ | ------------------------- |
| mysql-server                   | 服务器                    |
| mysql-workbench-community      | 工作台                    |
| libmysqlclient21               | 共享客户端                |
| mysql-cluster-community-server | MySQL NDB 集群 - SQL 节点 |




检查版本

```
select version();
```

### macOS

```bash
brew install mysql@8.4
brew services start mysql@8.4
fish_add_path /opt/homebrew/opt/mysql@8.4/bin
```

### Ubuntu

> `20.04 LTS`

```bash
sudo apt-get install -y mysql-server mysql-client libmysqlclient21 libmysqlclient-dev
```


## Ref

- [MySQL :: Developer Zone](https://dev.mysql.com/)