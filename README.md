# About Python Dict

```
In [1]: d = dict.fromkeys(['a', 'b'], ['one', 'two'])

In [2]: d
Out[2]: {'a': ['one', 'two'], 'b': ['one', 'two']}

In [3]: # fromkeys создает словарь

In [4]: d.clear()

In [5]: d
Out[5]: {}

In [6]: d = dict.fromkeys(['a', 'b'], ['one', 'two'])

In [7]: d
Out[7]: {'a': ['one', 'two'], 'b': ['one', 'two']}

In [8]: z = d

In [9]: z
Out[9]: {'a': ['one', 'two'], 'b': ['one', 'two']}

In [10]: d['c'] = 'three'

In [11]: d
Out[11]: {'a': ['one', 'two'], 'b': ['one', 'two'], 'c': 'three'}

In [12]: z
Out[12]: {'a': ['one', 'two'], 'b': ['one', 'two'], 'c': 'three'}

In [13]: y = d.copy()

In [14]: y
Out[14]: {'a': ['one', 'two'], 'b': ['one', 'two'], 'c': 'three'}

In [15]: d['d'] = 'four'

In [16]: d
Out[16]: {'a': ['one', 'two'], 'b': ['one', 'two'], 'c': 'three', 'd': 'four'}

In [17]: y
Out[17]: {'a': ['one', 'two'], 'b': ['one', 'two'], 'c': 'three'}

In [18]: d.get('a')
Out[18]: ['one', 'two']

In [19]: d.get('e')

In [20]: print(d.get('e'))
None

In [21]: # get возвращает значение ключа, если нет - None

In [22]: d.items()
Out[22]: dict_items([('a', ['one', 'two']), ('b', ['one', 'two']), ('c', 'three'), ('d', 'four')])

In [23]: for k, v in d.items():
    ...:     print(k, v)
    ...:     
a ['one', 'two']
b ['one', 'two']
c three
d four

In [24]: d.keys()
Out[24]: dict_keys(['a', 'b', 'c', 'd'])

In [25]: # keys - вернет ключи

In [26]: d.pop('a')
Out[26]: ['one', 'two']

In [27]: d
Out[27]: {'b': ['one', 'two'], 'c': 'three', 'd': 'four'}

In [28]: # pop - удаляет ключ и возвращает значение

In [29]: d.popitem('b')
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-29-69cb5cb0883c> in <module>()
----> 1 d.popitem('b')

TypeError: popitem() takes no arguments (1 given)

In [30]: d.popitem()
Out[30]: ('d', 'four')

In [31]: d
Out[31]: {'b': ['one', 'two'], 'c': 'three'}

In [32]: d.popitem()
Out[32]: ('c', 'three')

In [33]: d.popitem()
Out[33]: ('b', ['one', 'two'])

In [34]: d
Out[34]: {}

In [35]: d.popitem()
---------------------------------------------------------------------------
KeyError                                  Traceback (most recent call last)
<ipython-input-35-83c64cff336b> in <module>()
----> 1 d.popitem()

KeyError: 'popitem(): dictionary is empty'

In [36]: # popitem удаляет и возвращает пару - ключ и значение

...

In [41]: y
Out[41]: {'a': ['one', 'two'], 'b': ['one', 'two'], 'c': 'three'}

In [42]: y.setdefault('a')
Out[42]: ['one', 'two']

In [43]: y.setdefault('d')

In [44]: y
Out[44]: {'a': ['one', 'two'], 'b': ['one', 'two'], 'c': 'three', 'd': None}

In [45]: # .setdefault(key[, default]) - возвращает значение ключа, но если его 
    ...: нет, не бросает исключение, а создает ключ с значением default (по умол
    ...: чанию None)

In [46]: y
Out[46]: {'a': ['one', 'two'], 'b': ['one', 'two'], 'c': 'three', 'd': None}

In [47]: d = {'e' : 'f'}

In [48]: y.update(d)

In [49]: y
Out[49]: {'a': ['one', 'two'], 'b': ['one', 'two'], 'c': 'three', 'd': None, 'e': 'f'}

In [50]: # update расширяет словарь

In [51]: y.values()
Out[51]: dict_values([['one', 'two'], ['one', 'two'], 'three', None, 'f'])

In [52]: # values - возвращает значения в словаре
```
