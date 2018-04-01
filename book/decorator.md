# 函数装饰器和闭包

## 内容概要

- 闭包作用与原理
- nonlocal作用
- 实现装饰器

> 装饰器是可调用的对象，其参数是另一个函数(被装饰的函数)

```python
@decorator
def func():
    print('Hello decorator')

# 普通写法
def func():
    print('Hello func')

new_func = decorator(func)
```

`函数装饰器在导入模块时立即执行, 而被装饰的函数只在调用时运行`

## 闭包

> 闭包是一种函数，它会保留定义函数时存在的自由变量的绑定
> 这样调用函数时，虽然定义作用域不可用了，但依然可以使用那些绑定

## 一个简单的装饰器


## 参数化装饰器

