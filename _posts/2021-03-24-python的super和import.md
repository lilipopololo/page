---
layout: post
title: python的super和import以及记录的想法
category: blog
description: 写博客这个这么古老的行为，还有必要拿出来说吗，我看有。
---

###

每个类都有**init**方法.如果它没有明确定义一个,那么它将从其父类继承一个.在第二个示例中,该类从基础对象类继承**init**和一堆其他方法
class Dog:
def init_instance(self,name):
self.name = name
print('My name is',name)
print(dir(Dog))
结果显示了 Dog(dir 函数不带参数时，返回当前范围内的变量、方法和定义的类型列表；带参数时，返回参数的属性、方法列表。)

['__class__', '__delattr__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__le__', '__lt__', '__module__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', '__weakref__', 'init_instance']
