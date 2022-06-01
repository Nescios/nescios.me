---
title: Python functions
---

## If statement in one line python
```python
value_when_true if condition else value_when_false
```

**Examples Duplicate Encoder:**
```python
def duplicate_encode(word):
    word = word.lower()
    return ''.join(['(' if word.count(letter) == 1 else ')' for letter in word])
```

## Substitution letter + 13

```python
from string import maketrans, lowercase, uppercase

def rot13(message):
  lower = maketrans(lowercase, lowercase[13:] + lowercase[:13])
  upper = maketrans(uppercase, uppercase[13:] + uppercase[:13])
  return message.translate(lower).translate(upper)
```

## Find the odd int

```python
def find_it(seq):
    for i in seq:
        if seq.count(i) % 2 != 0:
            return i
```
