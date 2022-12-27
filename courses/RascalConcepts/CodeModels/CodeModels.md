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

You can use any of Rascal's [Values]((Rascal:Expressions-Values)) to represent facts about source code. 
For example, [Algebraic Data Types]((Rascal:Declarations-AlgebraicDataType)) can be used to define 
abstract syntax trees and ((Values-Relation)) are used to represent call graphs. 
We consistently use [Locations]((Rascal:Values-Location)) to refer to source code artifacts, 
either physically (`|file:///tmp/HelloWorld.java|`) or logically (`|java+class://java/lang/Object|`).

Specifically we have standardized a set of models to represent source code which are ready 
for computing metrics: [M3]((Library:analysis::m3)). This M3 model consists of: 

*  An open (extensible) set of [Relations]((Rascal:Values-Relation)) between source code artifacts.
*  A number of extensible [Algebraic Data Types]((Rascal:Declarations-AlgebraicDataType))
  for representing abstract syntax trees. 


The core language independent model can be found here: [analysis::m3]((Library:analysis::m3)).

Extensions for representing facts about specific languages:

* [lang::java::m3]((Library:lang::java::m3)).

#### Examples

#### Benefits

#### Pitfalls

