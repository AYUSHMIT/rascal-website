---
title: String Equal
keywords:
  - "=="

---

#### Synopsis

Equality operator on string values.

#### Syntax

`Exp~1~ == Exp~2~`

#### Types


| `Exp~1~` | `Exp~2~` | `Exp~1~ == Exp~2~`  |
| --- | --- | --- |
| `str`     |  `str`    | `bool`                |


#### Description

Yields `true` if both arguments are identical and `false` otherwise.

#### Examples


```rascal-shell 
rascal>"abc" == "abc";
bool: true
rascal>"abc" == "defghi";
bool: false
```


