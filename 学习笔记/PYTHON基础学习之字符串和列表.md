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
3. 使用制表符和换行符来添加空白\t
![](assets/PYTHON基础学习之字符串和列表/file-20260106203002127.png)
4. 换行符的使用\t
![](assets/PYTHON基础学习之字符串和列表/file-20260106203002126.png)
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
8. 数中的下划线
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
10. 常量
常量（constant)在程序的整个生命周期内部都保持不变的变量。python没有内置的常量类型，但python程序员会使用大写字母（单词用下划线分割）来指出应将么个变量视为常量，其值应始终不变
MAX_CONNECTION = 5000

11. 注释#为单行注释，为多行段落注释
```python
#这是单行注释
```
# 列表
在python中，用方括号[]表示列表，用逗号分割其中的元素。下面为实例
1. 访问列表元素
```python
names = ['张三','李四','王五','赵六','隔壁老王','楼上赵叔','zhangshan','lishi','jeak']
print(names)
#下面的代码从列表中提取第一个人名,使用列表的索引进行提取，索引是从0开始，不是从1.
print(names[0])

#也可以使用title()方法让元素输出为首字母大写的形式，这个对英文有效。
print(names[6].title())
print(names[7].title())
print(names[8].title()) 

#访问列表最后一个元素也可以这样,使用-1
print(names[-1])

#下面尝试从列表中提取一个元素，并使用这个元素值创建一条消息，然后打印出来
message = f"My name is {names[0]}."
print(message)
```
2. 修改列表元素
```python
names = ['张三','李四','王五','赵六','隔壁老王','楼上赵叔','zhangshan','lishi','jeak']
print(names)

#修改列表0号元素的值为'张三叔'
names[0] = '张三叔'
print(names)
```
3. 在列表末尾中添加元素
```python
#append()方法动态创建列表易如反掌，可以先创建一个空列表，在使用一系列函数调用append()添加元素。如下例子
name = []
name.append('张三')
name.append('李四')
name.append('jack')
name.append('xybzm')
print(name)
```
4. 在列表中插入元素insert()方法
```python
names = ['张三','李四','王五','赵六','隔壁老王','楼上赵叔','zhangshan','lishi','jeak']
print(names)
#在列表中插入元素用insert()方法可以在列表中任意位置添加新元素。如下例子就是在列表索引0的位置添加一个元素。

#这种操作将列表中所有元素都右移一个位置。
names.insert(0,'五姨')
print(names)
```
5. 从列表中删除元素del
```python
names = ['张三','李四','王五','赵六','隔壁老王','楼上赵叔','zhangshan','lishi','jeak']
print(names)

#删除列表索引0的元素
del names[0]

#删除列表最后一个元素
del names[-1]

#删除列表第二个元素值
del names[1]

print(names)
```

6. 使用pop()方法删除元素，这个方法会删除列表末尾一个元素。
>有时候，你要将元素从列表中删除，并接着使用它的值。例如，你可能要获取一个列表中的联系人，以便在相应的位置显示他的名字。
pop()方法删除列表末尾的元素，并让你能够接着使用它。列表就像一个栈，而删除列表末尾的元素相当于弹出栈顶元素。

```python
names = ['张三','李四','王五','赵六','隔壁老王','楼上赵叔','zhangshan','lishi','jeak']
print(names)

#使用pop()方法删除列表末尾一个元素，并赋值给一个变量
new_names = names.pop()
print(names)
print(f"你删除列表末尾{new_names}\t这个元素")
```

pop()有什么用处呢？假设你在饭店吃饭点菜，结果最后一道菜迟迟没有上来，你就不想要这道菜了，从菜单里删除这道菜，并且打印一条信息。如下

```python
caidan = ['红烧肉','小鸡炖蘑菇','素炒牛肉','辣根雨皮','炖排骨','红烧牛楠','土豆丝','拍黄瓜','遛虾仁']

print(caidan)

#删除菜单里最后一道没有上的菜
caidan_del = caidan.pop()

#pop()方法删除列表任意位置的元素，只需在括号里指定要删除元素的索引即可。如下删除菜单第一道菜
caidan_one = caidan.pop(0)  

print(caidan)
print(f"{caidan_del}客人不要了，不要做了")

print(f"{caidan_one}客人不要了，厨房不要在做了")
```
7. 根据值删除列表里的元素remove()方法
>有时候，你不知道要从列表中删除的值在哪个位置。如果只知道要删除的元素的值，可以用remove()方法。

```python
caidan = ['红烧肉','小鸡炖蘑菇','素炒牛肉','辣根雨皮','炖排骨','红烧牛楠','土豆丝','拍黄瓜','遛虾仁']

print(caidan)

#这里注意了remove()方法不想pop()方法可以弹出删除的元素名称，caidan_del变量为None
caidan_del = caidan.remove('拍黄瓜')

print(caidan)
print(f"{caidan_del}客人不要了，厨房不要做了")

#执行的结果是这样的，如下
#['红烧肉', '小鸡炖蘑菇', '素炒牛肉', '辣根雨皮', '炖排骨', '红烧牛楠', '土豆丝', '拍黄#瓜', '遛虾仁']
#['红烧肉', '小鸡炖蘑菇', '素炒牛肉', '辣根雨皮', '炖排骨', '红烧牛楠', '土豆丝', '遛虾仁']
#None客人不要了，厨房不要做了
```

8. 使用remove()方法从列表中删除元素后，也可继续使用它的值，和pop()方法有点不一样，首先要把删除的菜单名称赋值给一个变量，如下实例
```python
caidan = ['红烧肉','小鸡炖蘑菇','素炒牛肉','辣根雨皮','炖排骨','红烧牛楠','土豆丝','拍黄瓜','遛虾仁']

print(caidan)

#这里注意了remove()方法删除列表里的元素，要想在后面还使用这个名称，先把这个菜名赋值给一个变量。这样我们可以使用删除的这个元素名称打印一条信息
caidan_del = '拍黄瓜'
caidan.remove(caidan_del)

print(caidan)
print(f"{caidan_del}客人不要了，厨房不要做了")
```
>注意：remove()方法只删除第一个指定的值。如果要删除的值可能在列表中出现多次，就需要使用循环，确保将每一个值都删除。

## 以名称查找列表元素的索引号index("字符串名")
```python
my_caidan = ['红烧肉','小鸡炖蘑菇','素炒牛肉','辣根鱼皮','炖排骨','红烧牛楠','土豆丝','拍黄瓜','遛虾仁']

print(my_caidan.index("土豆丝"))

#输出结果是：6
```
# 列表管理
1. 使用sort()方法对列表进行永久排序
```python
cars = ['bmw','audi','toyota','subaru','byd','changcheng']
print(cars)
cars.sort()
print(cars)
```

>注意：sort()方法能永久的修改列表元素的排列顺序。

2. 还可以按字母顺序相反的顺序排列列表元素，只需向sort()方法传递参数reverse=True即可，如下实例
```python
cars = ['bmw','audi','toyota','subaru','byd','changcheng']
print(cars)
cars.sort(reverse=True)
print(cars)
```
3. 使用sorted()方法对列表进行临时排序
>要保留列表元素原来的排列顺序，并以特定的顺序呈现他们，可以使用sorted()函数。sorted()函数让你能够按特定顺序显示列表元素，同时不影响它们原来列表的排列顺序。如果是进行临时反向排序可以传入一个参数如sorted(reverse = True)


```python
cars = ['bmw','audi','toyota','subaru','byd','changcheng']
print(cars)

print(f"使用临时排序对列表进行一次排序如下\n{sorted(cars)}")
print(f"打印一下原始列表元素如下\n{cars}")
```

```python
str = ['b','d','a','f','e','h','l','n','o','p','z','g','k','m','r','j','s','w','x','y','c']

print(sorted(str))

#临时对列表进行安字母顺序进行倒排，这里要传入revers=True，这个参数。
print(sorted(str,reverse=True))

print(str)
```
4. 反向打印列表reverse()方法
>注意：reverse()方法不是安字母顺序相反的顺序排列列表元素，只是反转列表元素的排列顺序。
reverse()方法会永久地修改列表元素的排列顺序，但可以随时复原到原来的排列顺序，只需对列表再次调用reverse()即可。
```python
cars = ['bmw','audi','toyota','subaru','byd','changcheng']
print(cars)
cars.reverse()
print(cars)
```
5. 确定列表的长度
```python
cars = ['bmw','audi','toyota','subaru','byd','changcheng']

print(cars)

print(len(cars))
```
6. 使用列表时避免索引错误

>在刚开始使用列表时，很容易犯一种错误。假设你有一个包含三个元素的列表，却要求获得第四个元素。如下面的列表6个元素，列表的元素索引是从0开始的，最后一个元素索引是5。第6个元素根本没有，python就会报错。
>索引错误意味着python在指定的索引处找不到元素，请尝试将索引减1，然后再次运行程序。


```python
cars = ['bmw','audi','toyota','subaru','byd','changcheng']
print(cars[6])
```

>别忘了，每当需要访问最后一个列表元素时，都可以使用索引-1，这在任何情况下都是行之有效的，即便在最后一次访问列表后，其长度发成了变化。


7. 只有列表为空时，使用-1索引获取列表元素时才会报错如下
```python
cars = []
print(cars[-1])
```
>注意：在发生索引错误却找不到解决办法时，请尝试将列表长度打印出来。列表可能与你以为的截然不同，在程序对其进行了动态处理时尤其如此。查看列表或其包含的元素数，可以帮助你排查这种逻辑错误。

