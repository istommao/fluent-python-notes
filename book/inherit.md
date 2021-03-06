# 继承的优缺点

- 子类化内置类型的缺点
- 多重继承和方法解析顺序

## 子类化内置类型的问题

> 直接子类化内置类型（如dict、list或str）容易出错，因为内置类型的方法通常会忽略用户覆盖的方法。
> 不要子类化内置类型，用户自己定义的类应该继承collections模块中的类，
> 例如UserDict、UserList和UserString，这些类做了特殊设计，因此易于扩展。


## 多重继承

- `__mro__` 方法解析顺序
- 把接口继承和实现继承区分开
- 使用抽象基类显示表示接口
- 通过 mixin class 重用代码
- 优先使用对象组合，而不是类继承
