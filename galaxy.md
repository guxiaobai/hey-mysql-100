# community.mysql

```bash
ansible-galaxy collection install community.mysql
```

```bash
ansible -m apt -a "name=python3-pymysql state=present"
```


```bash
ansible -m mysql_user -a "name=hey host=% password=123456 priv=*.*:ALL state=present"
```

## Ref



- <https://galaxy.ansible.com/ui/repo/published/community/mysql/>