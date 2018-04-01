# 对象引用与垃圾回收

## 本章要讨论的一些问题

- 可变参数做函数默认值引发的问题
- 垃圾回收

## Python中的变量名只是一个名字

```python
arr = ['Hello', 'world']
lst = arr
arr.append('new item')
print(lst)
>>> ['Hello', 'world', 'new item']
```

## 弱引用

> 弱引用不会增加对象的引用数量

```python
import weakref

data = {'Hello', 'world'}
data2 = data

def finish():
    print('Finsh ...')

fin = weakref.finalize(data, finish)
fin.alive

del data
fin.alive

data2 = {}

fin.alive
```
