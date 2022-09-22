---
title: Alias Declaration
keywords:
  - alias

---

#### Synopsis

Declare an alias for a type.

#### Syntax

`alias Name  = Type;`

#### Description

Everything can be expressed using the elementary types and values that are provided by Rascal. 
However, for the purpose of documentation and readability it is sometimes better to use a descriptive name as type indication, rather than an elementary type.  The use of aliases is a good way to document your intentions. 

An alias declaration states that _Name_ can be used everywhere instead of the already defined type _Type_. 
Both types are thus structurally equivalent. 

#### Examples


```rascal-shell
```
Introduce two aliases `ModuleId` and `Frequency` for the type str.
```rascal,continue
alias ModuleId = str;
alias Frequency = int;
```
Another example is an alias definition for a graph containing integer nodes:
```rascal,continue
alias IntGraph = rel[int,int];
```
Note that the Rascal Standard Library provides a graph data type that is defined as follows:
```rascal,continue
alias Graph[&T] = rel[&T, &T];
```
In other words the standard graph datatype can be parameterized with any element type.

See [Type Parameters](../../../Rascal/Declarations/StaticTyping/TypeParameters) for other examples parameterized alias declarations.


