# 定义函数
- 下面是一个打印问候的简单函数
```python
def greet_user():
    """显示简单的问候"""
    print('你好')
#调用这个函数   
greet_user()
```
# 向函数传递信息
- 只要稍做修改，就可以让greet_user()函数在问候用户时以其名字作为抬头。为止，可在函数定义def greet_user()的括号内添加username。这样，可让函数接受你给username指定的任何值。现在，这个函数要求你在调用它时给username 指定一个值。因此在调用greet_user()时，可将一个名字传递给它，如下代码所示：
