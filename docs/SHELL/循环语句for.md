# for循环

```bash

[root@localhost ~]# bash for.sh
a is 1
a is 2
a is 3
a is 4
a is 5
a is 6
a is 7
a is 8
a is 9
[root@localhost ~]# cat for.sh
for a in {1..9}
do
  echo "a is $a "
done

```

其中 for in后面更着的是一个列表

类似的还有下面这个例子

```bash
[root@localhost demosh]# bash for2.sh
anaconda-ks.cfg
casedemo.sh
for2.sh
for.sh
ifelif.sh
ifelse.sh
ifinif.sh
[root@localhost demosh]# cat for2.sh
#!/bin/bash
for filename  in `ls *`
do
  echo "$filename"
done

```

使用for循环要点

列表中包含多个变量，变量使用空格分隔。

# C语言风格的for循环

```bash
for((变量初始化；循环判断条件；变量变化步长))
do
  shell command
done
```

