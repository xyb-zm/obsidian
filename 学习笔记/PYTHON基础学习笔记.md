# 变量命名规则
1. 变量名只能包含字母，数字和下划线。变量能以字母或下划线大头，但不能以数字大头。例如，可将变量命名为message_1,但是不能将其命名为1_message
2. 变量名不能包含空格，但能使用下划线来分割其中的单词。例如，变量名greeting_message可行，但是变量名greeting message会应发错误。
3. 不要将python关键字和函数名用作变量名。例如，不要将print用作变量名，应为它被python留作特殊用途
4. 变量名应即简短又具有描述性。例如，name比n好，student_name比s_n好，name_length比length_of_persons_name好。
5. 慎用小写字母l和大写字母O，因为它们可能被人看成1和0
## 变量是标签
变量常被描述为可用于存储值得盒子。在你刚接触变量时，这种定义很有帮助，但是他并没有准确的描述python内部表示变量的方式。一种好的多的定义是，变量是可以被赋值的标签，也可以说变量只指向特定的值。
## 字符串
就是一系列字符。在python中，用引号引起的都是字符串，其中的引号可以是单引号，也可以是双引号。
## 在字符串中使用变量
要在字符串中插入变量的值，可先在左引号前面加上f ,再将要插入的变量放在花括号内。这样，python在显示字符串时，将把每个变量都替换为其值。
```python
firt_name = "zhangshan"

last_name = "lishi"

full_name = f"{firt_name} {last_name}"

print(full_name)
```
1. 可以使用title()方法来将姓名设置为合适的格式，首字母大写。如下
```python
print(f"Hello,{full_name.title()}")
```
2. 还可以使用f字符串来创建消息，在把整条消息赋值给变量。
```python
message = f"hello, {full_name.title()}"
print(message)
```
3. \t 使用制表符和换行符来添加空白
![](assets/PYTHON基础学习笔记/file-20260106161647889.png)
4. \n换行符的使用
![](assets/PYTHON基础学习笔记/file-20260106161906646.png)
5. 删除空白,删除右侧空白rstrip()方法，删除左侧空白行lstrip()，删除两端空白行strip()，例如下
```python
a = 'phthon '
print(a)
print(a.rstrip())

```
6. 删除前缀removeprefix()方法，如网址的前缀”https://“,如下例子
```python
url = 'https://www.baidu.com'
new_url = url.removeprefix('https://')
print(new_url)
```
7. 如何在使用字符串时避免语法错误
语法错误是一种你会时不时遇到的错误。当程序包含非法的python代码时，就会导致语法错误。例如，在用单引号引起来的字符串中包含撇号' ,就将导致错误。这是因为这会导致python将第一个单引号和撇号之间的内容视为一个字符串，进而将余下的文本视为python代码，从而引发错误。
```python
#在双引号里使用撇号，python不会报错，可以正常使用

message = "This's a new product."

print(message)

#在单引号里使用撇号，python报错，python无法正确的确定字符串的结束位置。

nessage_two = 'This's a new product.'

print(message_two)
```
8. 数中的下划线,
这种写法可以便于阅读，在python打印这个变量时不会有下划线的。
```python
age = 14_000_000_000
print(age)
```
9. 同时给多给变量赋值。
```python
x,y,z = 0,0,0
print(x)
print(y)
print(z)
```
9. 常量
常量（constant)在程序的整个生命周期内部都保持不变的变量。python没有内置的常量类型，但python程序员会使用大写字母（单词用下划线分割）来指出应将么个变量视为常量，其值应始终不变
MAX_CONNECTION = 5000
10. 注释#为单行注释，```为多行段落注释```
```python
#这是单行注释
```这为多行注释```
# 列表
在python中，用方括号[]表示列表，用逗号分割其中的元素。下面为实例
```python
names = ['张三','李四','王五','赵六','隔壁老王','楼上赵叔']
print(names)

```