---
title: Immutable Values
---

#### Synopsis

Immutable values.

#### Description

Values are the basic building blocks of a language and the type of values determines how they may be used.

Rascal is a _value-oriented language_. This means that values are immutable and are always freshly constructed from existing parts.
For instance, replacing an element in a list does not modify the original list but produces a new list that only differs
from the original one in the modified position.

The language also provides variables. A value can be associated with a variable as the result of an explicit assignment statement: during the lifetime of a variable different (immutable) values may be assignment to it. Other ways to associate a value with a variable is by way of function calls (binding of formal parameters to actual values) and as the result of a successful pattern match.

The approach that values are immutable and that variables can be associated with different immutable values during their lifetime avoids
sharing and aliasing problems that exist in many languages. 

#### Examples

First we, create a list value and assign it to two variables `L` and `M`.

```rascal-shell
rascal>L = [1, 2, 3];
list[int]: [1,2,3]
rascal>M = L;
list[int]: [1,2,3]
```
Next we assign a new value to the first element of the list. The effect is that a new list value `[10, 2, 3]` is constructed.

```rascal-shell
rascal>L[0] = 10;
list[int]: [10,2,3]
```
L is now associated with this new value:

```rascal-shell
rascal>L;
list[int]: [10,2,3]
```
But `M` is still associated with the original, unmodified, value.

```rascal-shell
rascal>M;
list[int]: [1,2,3]
```
In pointer-based languages and in object-oriented languages the change to the original value of `L` would also be visible
via `M`.


String values are, like all other values, also immutable. Let's experiment with the [replaceAll](../../Library/String.md#String-replaceAll) function:

```rascal-shell
rascal>import String;
ok
rascal>replaceAll("abracadabra", "a", "A");
str: "AbrAcAdAbrA"
```
Now assign to variables `S` and `T` the string `"abracadabra"` and let's see what happens:

```rascal-shell
rascal>S = "abracadabra";
str: "abracadabra"
rascal>T = S;
str: "abracadabra"
rascal>S = replaceAll("abracadabra", "a", "A");
str: "AbrAcAdAbrA"
rascal>S;
str: "AbrAcAdAbrA"
rascal>T;
str: "abracadabra"
```

To summarize: all values are immutable and variables can during their lifetime be associated with different immutable values.


#### Benefits

*  Immutable values contribute to referential transparence.

#### Pitfalls

*  Immutable values maybe less efficient than mutable ones.


