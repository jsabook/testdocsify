# 脚本的参数

+ $0代表的是上一条语句执行是否成功，如果执行成功，那么$0=0

+ $1 代表的是执行该脚本的第一个参数，script.sh param1 param2 
  + 其中$1就是等于param1
  + 其中$2就等于param2

```bash

[root@localhost ~]# cat casedemo.sh
#!/bin/bash
case "$1" in
   "start"|"START")
    echo $0 start...
    ;;
    "stop")
    echo $0 stop...
    ;;
    "restart"|"reload")
    echo $0 restart
    ;;
    *)
    echo Usage:$0 "{start|stop}"
    ;;
esac
[root@localhost ~]# bash casedemo.sh stop
casedemo.sh stop...
[root@localhost ~]# bash casedemo.sh start
casedemo.sh start...
[root@localhost ~]# bash casedemo.sh reload
casedemo.sh restart
```



