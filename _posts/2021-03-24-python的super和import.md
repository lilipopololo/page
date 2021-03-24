---
layout: post
title: python的super和import以及记录的想法
category: blog
description: 写博客这个这么古老的行为，还有必要拿出来说吗，我看有。
---

##很没劲，尝试写写点 python 代码（最近在学 MVS 多视角获取深度的部分，上学期前两个月真的没想过用神经网络搞，毕竟电脑配置不够使用，但好像 10 年后的方法大多都是神经网络，搞了两个月甚至还学了一些 slam 的知识，但后来看到 colmap 的时候，我觉得能做的大家都做完了，具体来说同时就是这些方法太要求数学功底，再加上我真的有点啃不动了，就放弃转到神经网络了，从 MVSnet 开始看，论文林林总总就只有那么多篇，感觉就是太寂寞没有参照和学习的方向，开题完后已经是彻底摸不清只想混个毕业的状态。这个学期终于定下决心学习 python，从头做起（至少当时觉得 mvsnet——pytorch 那写的好理解，再找其他的直接蒙。所以打算把它当成模板去改尝试构建一个网络，跑步跑得了我可管不了）

**init**: 类的初始化函数，类似于 c++的构造函数
**call\_**: 使得类对象具有类似函数的功能。
每个类都有**init**方法.如果它没有明确定义一个,那么它将从其父类继承一个.在第二个示例中,该类从基础对象类继承**init**和一堆其他方法
class Dog:
def init_instance(self,name):
self.name = name
print('My name is',name)
print(dir(Dog))
结果显示了 Dog(dir 函数不带参数时，返回当前范围内的变量、方法和定义的类型列表；带参数时，返回参数的属性、方法列表。)

['__class__', '__delattr__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__le__', '__lt__', '__module__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', '__weakref__', 'init_instance']

pytorch 中经常有如下的形式出现
class Module(nn.Module):
def **init**(self):
super(Module, self).**init**() # ......

    def forward(self, x):
        # ......
        return x

data = ..... #输入数据

# 实例化一个对象

module = Module()

# 前向传播

module(data)

# 而不是使用下面的

# module.forward(data)

forward
