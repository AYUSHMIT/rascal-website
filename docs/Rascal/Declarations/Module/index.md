---
title: Module Declaration
keywords:
  - module

---

#### Synopsis

Declare a module.

#### Syntax

```rascal
module _Name_
_Imports_;
_Declaration<sub>1</sub>_;
...
_Declaration~n~_;
```

#### Types

#### Function

#### Description

A module declaration consists of:

*  A module name.
*  Zero or more imports;
*  Zero or more declarations.


The module name _Name_ will be used when the current module is imported in another module. 
A module name is in general a qualified name of the form:
```rascal
_Name<sub>1</sub>_::_Name<sub>2</sub>_:: ... ::_Name~n~_
```
which corresponds to a path relative to the root of the current workspace.

The constituents of a module are shown in the figure below.

![](/assets/Rascal/Declarations/Module/module-parts.png)


An [Import](/Rascal/Declarations/Import) declares other modules that are used by the current module.
Following imports, a module may contain declarations (in arbitrary order, but a [Syntax Definition](/Rascal/Declarations/SyntaxDefinition) can
occur directly following the imports) for:

*  [Syntax Definition](/Rascal/Declarations/SyntaxDefinition)
*  [Variable](/Rascal/Declarations/Variable)
*  [Function](/Rascal/Declarations/Function)
*  [Algebraic Data Type](/Rascal/Declarations/AlgebraicDataType)
*  [Alias](/Rascal/Declarations/Alias)
*  [Annotation](/Rascal/Declarations/Annotation)
*  [Tag](/Rascal/Declarations/Tag)


Each declaration may contain a `private` or `public` keyword that determines 
the _visibility_ of the declared entity. 

The entities that are _visible inside_ a module are

*  The private or public entities declared in the module itself.

*  The public entities declared in any imported module.


The only entities that are _visible outside_ the module, are the public entities declared in the module itself. If different imported modules declare the same visible name, it can be disambiguated by explicitly qualifying it with its module name:

```rascal
_Module_ :: _Name_
```

Each module resides in a separate file with extension `.rsc`.

#### Examples

Here is the `Hello` module:


```rascal

module demo::basic::Hello

import IO;

void hello() {
   println("Hello world, this is my first Rascal program");
}

```

                
It defines a module with the name `demo::basic::Hello` and imports the [IO](/Library/IO) library.
Finally, it declares the `hello` function.

The actual source of this module can be found in `library/demo/basic/Hello.rsc` in the Rascal sources.

More ways to write this example are discussed in the [Hello](/Recipes/Basic/Hello) example in [Recipes](/Recipes/).

#### Benefits


