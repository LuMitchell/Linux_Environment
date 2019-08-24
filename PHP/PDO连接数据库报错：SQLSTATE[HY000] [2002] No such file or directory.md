一开始搜到的办法是
“
这个是由于找不到mysql.sock文件造成的

1.在MySQL里面执行sql语句 show variables like '%sock%'

2.对应返回的结果的字段 socket 的对应的value

3.修改文件在/config/database.php 中的 connections 下的 mysql 添加

‘unix_socket’ => ‘/tmp/mysql.sock’

”

发现不行，最后使用下面的方法


将PDO连接中的host由“localhost”改为“127.0.0.1”即可
