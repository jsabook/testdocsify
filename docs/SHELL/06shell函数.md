# 函数的定义

自定义函数

```bash
function fname(){
shell command1
shell command2
}
```

函数的执行

```
fname
```

第二种定义方式

```
fname(){
shell command1
shell command2
}
```

直接将function省掉



# 函数的参数

如果想要给函数增加参数

函数作用范围的变量

local 变量名

函数的参数

`$1 $2 $3 ... $n`

```bash

[root@localhost mp3dir]# cdls(){
> cd $1
> ls
> }
[root@localhost demosh]# cdls /tmp
10.sh
systemd-private-752912361d68446a9ffd69740493b6fc-chronyd.service-mGqMXt
systemd-private-b472b6c8990f4b4298a5a457a6d186bb-chronyd.service-tfliIr
vmware-root_658-2697598381
vmware-root_666-2731021219
vmware-root_678-2722697728
[root@localhost tmp]# cdls /home/
test  test1  test122  test2  test22  user1  user2
```



