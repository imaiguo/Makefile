# Makefile

​
在Linux上常常写代码，快速使用gcc编译代码如下方法：
```shell
CC = g++
EXEC = hello
OBJS = hello.o
all: $(EXEC)
$(EXEC): $(OBJS)
$(CC) -o $@ $^
clean:
rm -f $(OBJS)
```

重要说明：文件的编码格式一定是UTF-8无BOM格式的。同时注意使用TAB键

Makefile有三个非常有用的变量。分别是$@，$^，$<代表的意义分别是

$@--目标文件，$^--所有的依赖文件，$<--第一个依赖文件。 

​