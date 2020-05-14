# 魔法函数

## all 
python模块中的__all__，用于模块导入时限制，如：from module import * 此时被导入模块若定义了__all__属性，则只有__all__内指定的属性、方法、类可被导入；若没定义，则导入模块内的所有公有属性，方法和类。

## slot
 使用__slots__

如果我们想要限制class的属性怎么办？比如，只允许对Student实例添加name和age属性。 为了达到限制的目的，Python允许在定义class的时候，定义一个特殊的__slots__变量，来限制该class能添加的属性： 

``` 
class Student(object): 
	slots = ('name', 'age') # 用tuple定义允许绑定的属性名称 
```
