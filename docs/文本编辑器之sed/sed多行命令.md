## 多行模式意义

+ 配置文件是多行的
+ 也有使用xml或者json格式的配置文件，为多行出现

## 多行匹配模式

命令参数

+ `N`将下一行加入到模式空间
+ `D`删除模式空间中第一个字符到第一个换行符
+ `P`打印模式空间中第一个字符到第一个换行符

## **N**指令

将第二行追加到模式空间

```bash
[root@localhost ~]# cat a.txt
hel
lo
hello
[root@localhost ~]# sed 'N;s/hel\nlo/!!!/' a.txt
!!!
hello
```



