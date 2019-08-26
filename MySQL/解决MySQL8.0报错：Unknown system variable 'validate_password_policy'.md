# 解决MySQL8.0报错：Unknown system variable 'validate_password_policy'

创建MySQL用户时出现

`ERROR 1819 (HY000): Your password does not satisfy the current policy requirements`

然后修改密码政策出现

```
mysql>  set global validate_password_policy=0;
ERROR 1193 (HY000): Unknown system variable 'validate_password_policy'
```

找到原因
在MySQL 8.0之前参数是
>validate_password_policy

8.0版本之后是
>validate_password.policy

**注意 ‘_’ 和 ‘.’ 的区别**

参考[解决MySQL8.0报错：Unknown system variable 'validate_password_policy'](https://blog.csdn.net/qq_34545939/article/details/83623606)
