**练习题**：

1、上面提到了许多魔法方法，如`__new__`,`__init__`, `__str__`,`__rstr__`,`__getitem__`,`__setitem__`等等，请总结它们各自的使用方法。



- `__init__(self[, ...])` 构造器，当一个实例被创建的时候调用的初始化方法

- ```
  rect = Rectangle(4, 5)
  print(rect.getPeri())  # 18
  print(rect.getArea())  # 20
  ```

  - ```
    __new__(cls[, ...])
    ```

    在一个对象实例化的时候所调用的第一个方法，在调用

    ```
    __init__
    ```

    初始化前，先调用

    ```
    __new__
    ```

    - `__new__`至少要有一个参数`cls`，代表要实例化的类，此参数在实例化时由 Python 解释器自动提供，后面的参数直接传递给`__init__`。
    - `__new__`对当前类进行了实例化，并将实例返回，传给`__init__`的`self`。但是，执行了`__new__`，并不一定会进入`__init__`，只有`__new__`返回了，当前类`cls`的实例，当前类的`__init__`才会进入。

- 若`__new__`没有正确返回当前类`cls`的实例，那`__init__`是不会被调用的，即使是父类的实例也不行，将没有`__init__`被调用。

- `__new__`方法主要是当你继承一些不可变的 class 时（比如`int, str, tuple`）， 提供给你一个自定义这些类的实例化过程的途径。

- `__del__(self)` 析构器，当一个对象将要被系统回收之时调用的方法。

- 

- ```
  __str__(self)
  ```

  :

  - 当你打印一个对象的时候，触发`__str__`
  - 当你使用`%s`格式化的时候，触发`__str__`
  - `str`强转数据类型的时候，触发`__str__`

- ```
  __repr__(self)
  ```

  ：

  - `repr`是`str`的备胎
  - 有`__str__`的时候执行`__str__`,没有实现`__str__`的时候，执行`__repr__`
  - `repr(obj)`内置函数对应的结果是`__repr__`的返回值
  - 当你使用`%r`格式化的时候 触发`__repr__`

- `__str__(self)` 的返回结果可读性强。也就是说，`__str__` 的意义是得到便于人们阅读的信息，就像下面的 '2019-10-11' 一样。

  `__repr__(self)` 的返回结果应更准确。怎么说，`__repr__` 存在的目的在于调试，便于开发者使用。

- `__add__(self, other)`定义加法的行为：`+`

- `__sub__(self, other)`定义减法的行为：`-`

- `__mul__(self, other)`定义乘法的行为：`*`

- `__truediv__(self, other)`定义真除法的行为：`/`

- `__floordiv__(self, other)`定义整数除法的行为：`//`

- `__mod__(self, other)` 定义取模算法的行为：`%`

- `__divmod__(self, other)`定义当被 `divmod()` 调用时的行为

- `divmod(a, b)`把除数和余数运算结果结合起来，返回一个包含商和余数的元组`(a // b, a % b)`。

- `__pow__(self, other[, module])`定义当被 `power()` 调用或 `**` 运算时的行为

- `__lshift__(self, other)`定义按位左移位的行为：`<<`

- `__rshift__(self, other)`定义按位右移位的行为：`>>`

- `__and__(self, other)`定义按位与操作的行为：`&`

- `__xor__(self, other)`定义按位异或操作的行为：`^`

- `__or__(self, other)`定义按位或操作的行为：`|`

- 反运算魔方方法，与算术运算符保持一一对应，不同之处就是反运算的魔法方法多了一个“r”。当文件左操作不支持相应的操作时被调用。

  - `__radd__(self, other)`定义加法的行为：`+`
  - `__rsub__(self, other)`定义减法的行为：`-`
  - `__rmul__(self, other)`定义乘法的行为：`*`
  - `__rtruediv__(self, other)`定义真除法的行为：`/`
  - `__rfloordiv__(self, other)`定义整数除法的行为：`//`
  - `__rmod__(self, other)` 定义取模算法的行为：`%`
  - `__rdivmod__(self, other)`定义当被 divmod() 调用时的行为
  - `__rpow__(self, other[, module])`定义当被 power() 调用或 `**` 运算时的行为
  - `__rlshift__(self, other)`定义按位左移位的行为：`<<`
  - `__rrshift__(self, other)`定义按位右移位的行为：`>>`
  - `__rand__(self, other)`定义按位与操作的行为：`&`
  - `__rxor__(self, other)`定义按位异或操作的行为：`^`
  - `__ror__(self, other)`定义按位或操作的行为：`|`

- `__iadd__(self, other)`定义赋值加法的行为：`+=`

- `__isub__(self, other)`定义赋值减法的行为：`-=`

- `__imul__(self, other)`定义赋值乘法的行为：`*=`

- `__itruediv__(self, other)`定义赋值真除法的行为：`/=`

- `__ifloordiv__(self, other)`定义赋值整数除法的行为：`//=`

- `__imod__(self, other)`定义赋值取模算法的行为：`%=`

- `__ipow__(self, other[, modulo])`定义赋值幂运算的行为：`**=`

- `__ilshift__(self, other)`定义赋值按位左移位的行为：`<<=`

- `__irshift__(self, other)`定义赋值按位右移位的行为：`>>=`

- `__iand__(self, other)`定义赋值按位与操作的行为：`&=`

- `__ixor__(self, other)`定义赋值按位异或操作的行为：`^=`

- `__ior__(self, other)`定义赋值按位或操作的行为：`|=`

- `__neg__(self)`定义正号的行为：`+x`

- `__pos__(self)`定义负号的行为：`-x`

- `__abs__(self)`定义当被`abs()`调用时的行为

- `__invert__(self)`定义按位求反的行为：`~x`

- `__getattr__(self, name)`: 定义当用户试图获取一个不存在的属性时的行为。

- `__getattribute__(self, name)`：定义当该类的属性被访问时的行为（先调用该方法，查看是否存在该属性，若不存在，接着去调用`__getattr__`）。

- `__setattr__(self, name, value)`：定义当一个属性被设置时的行为。

- `__delattr__(self, name)`：定义当一个属性被删除时的行为。

- `__get__(self, instance, owner)`用于访问属性，它返回属性的值。

- `__set__(self, instance, value)`将在属性分配操作中调用，不返回任何内容。

- `__del__(self, instance)`控制删除操作，不返回任何内容。

- `__len__(self)`定义当被`len()`调用时的行为（返回容器中元素的个数）。

- `__getitem__(self, key)`定义获取容器中元素的行为，相当于`self[key]`。

- `__setitem__(self, key, value)`定义设置容器中指定元素的行为，相当于`self[key] = value`。

- `__delitem__(self, key)`定义删除容器中指定元素的行为，相当于`del self[key]`。

- 迭代器有两个基本的方法：`iter()` 和 `next()`。

- `iter(object)` 函数用来生成迭代器。

- `next(iterator[, default])` 返回迭代器的下一个项目。

- `iterator` -- 可迭代对象

- `default` -- 可选，用于设置在没有下一个元素时返回该默认值，如果不设置，又没有下一个元素则会触发 `StopIteration` 异常。

- 把一个类作为一个迭代器使用需要在类中实现两个魔法方法 `__iter__()` 与 `__next__()` 。

  - `__iter__(self)`定义当迭代容器中的元素的行为，返回一个特殊的迭代器对象， 这个迭代器对象实现了 `__next__()` 方法并通过 `StopIteration` 异常标识迭代的完成。
  - `__next__()` 返回下一个迭代器对象。
  - `StopIteration` 异常用于标识迭代的完成，防止出现无限循环的情况，在 `__next__()` 方法中我们可以设置在完成指定循环次数后触发 `StopIteration` 异常来结束迭代。

- 在 Python 中，使用了 `yield` 的函数被称为生成器（generator）。

- 跟普通函数不同的是，生成器是一个返回迭代器的函数，只能用于迭代操作，更简单点理解生成器就是一个迭代器。

- 在调用生成器运行的过程中，每次遇到 `yield` 时函数会暂停并保存当前所有的运行信息，返回 `yield` 的值, 并在下一次执行 `next()` 方法时从当前位置继续运行。

- 调用一个生成器函数，返回的是一个迭代器对象。

2、利用python做一个简单的定时器类

要求:

- 定制一个计时器的类。
- `start`和`stop`方法代表启动计时和停止计时。
- 假设计时器对象`t1`，`print(t1)`和直接调用`t1`均显示结果。
- 当计时器未启动或已经停止计时时，调用`stop`方法会给予温馨的提示。
- 两个计时器对象可以进行相加：`t1+t2`。
- 只能使用提供的有限资源完成。

