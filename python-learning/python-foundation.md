# python基础知识

## python内置函数
### 内联函数
<pre name="code" class="python">def my_func(f,arg):
	return f(arg)

my_func(lambda x:2*x*x,5)
</pre>
> Lambdas:内联函数没有命名函数的功能强大，而且一般能用于一个参数的情况，不过可以有多个参数。

<pre name="code" class="python">
# 命名函数
def polynomial(x):
	return x**2+5*x+4
print(polynomial(-4))

# 内联函数——第一种方法
print((lambda x:x**2+5*x+4)(-4))

# 内联函数——第二种方法
double = lambda x:x*2
print(double(7))

# 内联函数——多参形式
add = lambda x,y:x+y
print(add(3,7))
</pre>
### map函数
> map函数主要是用于列表——list或可迭代序列——iterables；map函数需要一个函数和一个列表作为参数，同时返回一个**新的**可迭代序列——每个序列元素均经过函数的处理。
<pre name="code" class="python">
def add_five(x):
	return x+5
nums=[11,22,33,44,55]
result = list(map(add_five,nums)) #result=list(map(lambda x:x+5,nums))
print(result)
</pre>

### filter函数
> filter函数是选择器，参数（函数名，可迭代序列），目的是为了筛选出序列中符合条件的值。
<pre name="code" class="python">
nums = [11,22,33,44,55]
res=list(filter(lambda x:x % 2==0,nums)
print(res)

output:[22,44]
</pre>

### 生成器——Generators
> 生成器是一种迭代器，类似lists和tuples。与列表不同的是，生成器没有索引，不过同样可以用for循环迭代输出，我们可以使用函数和yield语句。
<pre name="code" class="python">
def countdown():
    i=5
    while i>0:
        yield i
        i-=1
for i in countdown():
    print(i) 
</pre>
### 装饰器——Decorators
> 装饰器提供了一种通过其他函数的方式修改函数，在你想扩展函数功能却不想修改函数的时候是一种很棒的方法。
<pre name="code" class="python">
def decor(func):
    def wrap():
        print("============")
        func()
        print("============")
    return wrap
def print_text():
    print("Hello World!")

decorated=decor(print_text)
Decorated()

或：
@decor
def print_text():
    print("Hello World!")
print_text()

output:
============
Hello World!
============
</pre>

> 以上方法不够直接简明，python提供了“@”操作符，通过在函数体上加上“@decor”，下面的函数便被装饰了。

### 集合——set()
> set是一种数据结构，集合内元素拥有互不相同，绝无重复的特点。同时，集合元素不具备排序，没有索引。

## python


## python

