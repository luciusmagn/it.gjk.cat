nazev = "Boolean výrazy"
tagy = ["python", "bool"]
+++
# Boolean výrazy

Boolean výrazy jsou výrazy které obsahují dvě možné hodnoty : `True` nebo `False`.

## Operátory

Tyhle základní logické operátory rozlišujeme v pythonu :

### `<`, `>` - menší než, větší než
```python
>>> 2 < 3
True
>>> 2 > 3
False
```

### `==`, `!=` - rovnost, nerovnost

```python
>>> 2 == 2
True
>>> 2 != 3
True
```

### `and`, `or` - logické 'a' a 'nebo'

```python
>>> True and True
True
>>> True and False # a obracene
False
>>> False and False
False
```
```python
>>> True or True
True
>>> True or False # a obracene
True
>>> False or False
False
```

### `not` - negace

```python
>>> not True
False
>>> not False
True
```

