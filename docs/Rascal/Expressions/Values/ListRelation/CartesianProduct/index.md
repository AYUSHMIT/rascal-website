---
title: ListRelation CartesianProduct
keywords:
  - "*"

---

#### Synopsis

Cartesian product of two list relation values.

#### Syntax

`Exp~1~ * Exp~2~`

#### Types


|`Exp~1~`      | `Exp~2~`     | `Exp~1~ * Exp~2~`   |
| --- | --- | --- |
| `list[T~1~]` | `list[T~2~]` | `lrel[T~1~, T~2~]`  |


#### Description

Returns a binary relation that is the [Cartesian product](http://en.wikipedia.org/wiki/Cartesian_product) of two lists.

#### Examples


```rascal-shell 
rascal>[1, 2, 3] * [9];
lrel[int,int]: [
  <1,9>,
  <2,9>,
  <3,9>
]
rascal>[1, 2, 3] * [10, 11];
lrel[int,int]: [
  <1,10>,
  <1,11>,
  <2,10>,
  <2,11>,
  <3,10>,
  <3,11>
]
```


