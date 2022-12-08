---
title: Factorial
---

#### Synopsis

Compute the factorial function.

#### Syntax

#### Types

#### Function

#### Description

#### Examples

The [factorial](http://en.wikipedia.org/wiki/Factorial)
of a number `n` is defined as `n * (n-1) * (n-2) * ... * 1`.
Here is the Rascal version:
```rascal-include
demo::basic::Factorial
```
          
<1> `fac1` is defined using a conditional expression to distinguish cases.
<2> `fac2` distinguishes cases using pattern-based dispatch ([Rascal Functions]((Rascal:Function))).
    Here the case for `0` is defined.
<3> Here all other cases for `fac2` are defined (as indicated by the `default` keyword).
<4> `fac3` shows a more imperative implementation of factorial.

Here is how to use `fac`:

```rascal-shell
import demo::basic::Factorial;
fac1(47);
```

NOTE: Indeed, Rascal supports arbitrary length numbers.
 
Here is an example of `fac2`:
```rascal-shell,continue
fac2(47);
```

#### Benefits

#### Pitfalls

