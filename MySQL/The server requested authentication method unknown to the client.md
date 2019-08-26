# The server requested authentication method unknown to the client

又是 MySQL8.0 的变化

原因是MySQL的加密方式变了，解决办法有两种：

一种是改变全局配置回之前的验证方式
```
找到mysql配置文件并加入

default_authentication_plugin=mysql_native_password
```

另一种是单独修改某一个用户的验证方式
```
mysql> mysql -uroot -p

mysql> use mysql;
mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```
