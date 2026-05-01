## 2.5.2 Installing MySQL on Linux Using the MySQL APT Repository

|本期版本| 上期版本
|:---:|:---:
`Fri May  1 11:15:55 CST 2026` | -


### Adding the MySQL Apt Repository

```bash
# version w.x.y-z
curl -LR -O https://dev.mysql.com/get/mysql-apt-config_0.8.39-1_all.deb
sudo dpkg -i mysql-apt-config_0.8.39-1_all.deb
```

### Selecting a Major Release Version

```
sudo dpkg-reconfigure mysql-apt-config
```



### Installing MySQL with APT

```bash
apt-get install mysql-server
```





## Ref

- <https://dev.mysql.com/doc/refman/8.4/en/linux-installation-apt-repo.html>
- <https://dev.mysql.com/downloads/repo/apt/>
