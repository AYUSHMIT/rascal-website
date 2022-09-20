---
title: Code Models
---

#### Synopsis

Code models are abstract representations of source code

#### Syntax

#### Types

#### Function
       
#### Usage

#### Description

You can use any of Rascal's [Values](/Rascal/Expressions/Values) to represent facts about source code. 
For example, [Algebraic Data Types](/Rascal/Declarations/AlgebraicDataType) can be used to define 
abstract syntax trees and [Relation](/Rascal/Expressions/Values/Relation) are used to represent call graphs. 
We consistently use [Locations](/Rascal/Expressions/Values/Location) to refer to source code artifacts, 
either physically (`|file:///tmp/HelloWorld.java|`) or logically (`|java+class://java/lang/Object|`).

Specifically we have standardized a set of models to represent source code which are ready 
for computing metrics: #/Libraries#analysis-m3[M3]. This M3 model consists of: 

*  an open (extensible) set of [Relations](/Rascal/Expressions/Values/Relation) between source code artifacts.
*  a number of extensible [Algebraic Data Types](/Rascal/Declarations/AlgebraicDataType)
  for representing abstract syntax trees. 


The core language independent model can be found here: [analysis::m3][Library:analysis::m3](/Library/analysis/m3/index.md).

Extensions for representing facts about specific languages:

* [lang::java::m3][Library:lang::java::m3](/Library/lang/java/m3/index.md).

#### Examples

#### Benefits


