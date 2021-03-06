# 二、python基本语法
## （一）变量
1.参考文档

python官方文档：https://docs.python.org/3/tutorial/index.html

2.概念：
在程序设计中，变量是一种存储数据的载体。计算机中的变量是实际存在的数据或者说是存储数据的一块内存空间，变量的值可以被读取和修改，这是所有计算和控制的基础。

3.命名规则：

1）硬性规则：
- 变量名由字母（广义的Unicode字符，不包括特殊字符）、数字和下划线构成，数字不能开头。
- 大小写敏感
- 不要跟关键字（有特殊含义的单词）和系统保留字（如函数、模块等的名字）冲突。

2）PEP8 要求：
- 用小写字母拼写，多个单词用下划线连接。
- 受保护的实例属性用单个下划线开头。
- 私有的实例属性用两个下划线开头。

## （二）数字

1.int：整型

2.float：浮点型

3.complex：复杂型

举例：
```
int_a = 1
float_a = 2.3
complex_a = 3k

print(type(int_a))
print(type(float_a))
print(type(complex_a))
```

（三）字符串

1. \:转义符

例：
```
a = 'stringdikdkld\\n'
print(a)
print("-----")
```
由于“\”做了转义，所以结果是：
```
stringdikdkld\n
-----
```

2. r:忽略转义符的作用
```
a = r'stringdikdkld\\n'
print(a)
print("-----")
```
由于“r”做了忽略转义符处理，所以结果是：
```
stringdikdkld

-----
```

3.  `+ `以及空格: 多个字符串连接

1）举例1：
```
a = "aaaaa"
b = "bbbbb"
print(a+b)
```
"+"号可以将两个变量连接起来显示，所以结果是：
`aaaaabbbbb`

2）举例2：
`print("ccccc" "ddddd")`

空格也可以连接字符串，但是必须把字符串写全，不可用于变量，所以结果是：
`cccccddddd`

4. f+{}/format ：引用语法

1）用法1：
```
a = "aaaaa"
b = f"bbbbb{a}"
print(b)
```
结果：
`bbbbbaaaaa`


2）用法2：
```
a = "aaaaa"
b = "bbbbb{}"
print(b.format(a))
```
结果：
`bbbbbaaaaa`


3）多个引用
```
a = "aaaaaa"
b = "bbbbbb"
c = "cccccc"
d = "ddddd{}{}{}"
print(d.format(a,b,c))
```
结果：
`dddddaaaaaabbbbbbcccccc`

4）有多个引用时可使用变量进行赋值
```
a = "aaaaaa"
b = "bbbbbb"
c = "cccccc"
d = "ddddd{}{}{}"
print(d.format(x=a,y=b,z=c))
```
结果：
`dddddaaaaaabbbbbbcccccc`

## （四）列表
1.定义

list(列表)是python中使用最频繁的数据类型，在其他语言中通常就做数组。

2.索引

列表的索引从0开始，索引就是数据在列表中的位置编号，索引又称为下标。
```
list_a = [1,2,3,"ddd"."s"]
print(list_a[0])
print(list_a[1])
print(list_a[2])
print(list_a[-1])
```
注： -1 是倒数第一个元素。

