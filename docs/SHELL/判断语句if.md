# if-then

if-then基本用法

	+ if [测试条件成立] 或者 命令返回值为0
	+ then 执行相应命令
	+ fi结束

`[]`等于 `tset`

下面一个是个简单的if语句

```bash
[root@localhost ~]# if test $UID = 0
> then
>   echo " root user "
> fi
 root user

```

等价于

```bash
[root@localhost ~]#  if [ $UID = 0 ]
> then
>   echo " user root "
> fi
 user root
```

注意的是`[]`内左右必须要有两个空格。`[ $UID = 0]`与`[$UID = 0 ]`都是错误的`[ $UID = 0 ]`是正确的。

test 命令最短的定义可能是评估一个表达式；如果条件为真，则返回一个 0 值。如果表达式不为真，则返回一个大于 0 的值 — 也可以将其称为假值。

# if-else

```bash
[root@localhost ~]# cat ifelse.sh
#!/bin/bash
if [ $UID = 0 ]
then
  echo " root user "
else
  echo " other user"
fi
```

输出

```bash
[root@localhost ~]# bash ifelse.sh
 root user
```



# if-elif

```BASH
[root@localhost ~]# cat ifelif.sh
#!/bin/bash
if [ $UID = root ]
then
  echo " root user "
elif [ $UID = user1 ]
then
  echo " user1 user"
else
  echo " other user"
fi
[root@localhost ~]# bash ifelif.sh
 other user

```

要点：

+ 判断语句后面一定会跟上一个then，无论是if又或者是elif。
+ else后面可以直接跟上执行语句



# 嵌套if语句

```bash
[root@localhost ~]# bash ifinif.sh
 please run
 run 10.sh
[root@localhost ~]# cat ifinif.sh
#!/bin/bash
if [ $UID = 0 ]
then
  echo " please run "
  if [ -x /tmp/10.sh ]
  then
    /tmp/10.sh
   else
     chmod +x /tmp/10.sh
     /tmp/10.sh
   fi
else
  echo " switch user root "
fi
```





