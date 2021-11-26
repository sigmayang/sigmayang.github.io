`‘getattr(object, name[, default])`

作用：

* 获取对象的属性值，如某一个类对象，就可以获得这个类中某一属性的属性值，而如果该类中没有这个属性，则可以设置default值进一步设置这个属性的属性值

例如：

```python
>>>class A(object):
...     bar = 1
... 
>>> a = A()
>>> getattr(a, 'bar')        # 获取属性 bar 值
1
>>> getattr(a, 'bar2')       # 属性 bar2 不存在，触发异常
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'A' object has no attribute 'bar2'
>>> getattr(a, 'bar2', 3)    # 属性 bar2 不存在，但设置了默认值
3
```

