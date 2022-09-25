---
title: String GreaterThan
keywords:
  - ">"

---

#### Synopsis

Greater than operator on string values.

#### Syntax

`Exp~1~ > Exp~2~`

#### Types


| `Exp~1~` | `Exp~2~` | `Exp~1~ > Exp~2~`  |
| --- | --- | --- |
| `str`     |  `str`    | `bool`                |


#### Description

Yields `true` if the string value of _Exp_~1~ is strictly lexicographically greater
than the string value of _Exp_~2~, and `false` otherwise.

#### Examples


```rascal-shell 
rascal>"abcdef" > "abc";
bool: true
rascal>"defghi" > "abcdef";
bool: true
rascal>"a" > "abc";
bool: false
```


