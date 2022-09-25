---
title: DateTime NotEqual
keywords:
  - "!="

---

#### Synopsis

Not equal operator on datetime values.

#### Syntax

`Exp~1~ != Exp~2~`

#### Types

| `Exp~1~`      | `Exp~2~`      | `Exp~1~ != Exp~2~`  |
| --- | --- | --- |
| `datetime`     |  `datetime`    | `bool`                |


#### Description

Yields `true` if both arguments are different `datetime` values and `false` otherwise.

#### Examples


```rascal-shell 
rascal>$2010-07-15$ != $2010-07-14$;
bool: true
rascal>$2010-07-15$ != $2010-07-15$;
bool: false
```


