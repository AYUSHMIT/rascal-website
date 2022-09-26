---
title: Annotation Declaration
keywords:
  - anno
  - "@"

---

#### Synopsis

Declare an annotation type for nodes. This feature is deprecated; please use [keyword fields](../../../Rascal/Declarations/AlgebraicDataType/index.md) instead.

#### Syntax

`anno AnnoType OnType @ Name`

#### Description

An annotation may be associated with any node value, be it a pure node or some [Algebraic Data Type](../../../Rascal/Declarations/AlgebraicDataType/index.md) derived from it.

Annotations are intended to attach application data to values,
like adding position information or control flow information to source code or adding visualization information to a graph.

An annotation declaration defines:

*  _AnnoType_, the type of the annotation values,
*  _OnType_, the type of the values that are being annotated,
*  _Name_, the name of the annotation.


Any value of any named type can be annotated and the type of these annotations can be declared precisely.

The following constructs are provided for handling annotations:

*  `Val @ Anno`: is an expression that retrieves the value of annotation _Anno_ of value _Val_ (may be undefined!). 

*  `Val₁[@Anno = Val₂]`: is an expression that sets the value of annotation _Anno_ of the value _Val₁_ to _Val₂_
   and returns _Val₁_ with the new annotation value as result. 

*  `Var @ Anno = Val`: is an assignment statement that sets the value of annotation _Anno_ of the value of variable _Var_ to _Val_.

#### Examples

Examples have been removed since this feature is deprecated. 

#### Pitfalls

* Annotations are cumbersome since they change the structure of [Values](../../../Rascal/Expressions/Values/index.md) without changing the semantics of the identity of a value. This is why they are deprecated.

