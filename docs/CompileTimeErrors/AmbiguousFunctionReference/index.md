---
title: AmbiguousFunctionReference
---

#### Synopsis

An ambiguous function name

#### Syntax

#### Types

#### Function
       
#### Usage

#### Description

Warning: How to generate this error? 

#### Examples


```rascal-shell
rascal>data D = d(int x);
ok
rascal>data D2 = d(str x);
ok
rascal>d(3).x
int: 3
rascal>d("a").x
str: "a"
```

#### Benefits


