---
title: Datatypes
---

#### Synopsis

Built-in and user-defined datatypes.

#### Syntax

#### Types

#### Function

#### Description

Rascal provides a rich set of datatypes:

*  [Boolean](/Rascal/Expressions/Values/Boolean) (`bool`).
*  Infinite precision [Integer](/Rascal/Expressions/Values/Integer) (`int`), 
   [Real](/Rascal/Expressions/Values/Real) (`real`), and [Number](/Rascal/Expressions/Values/Number) (`num`).
*  [String](/Rascal/Expressions/Values/String)s (`str`) that can act as templates with embedded expressions and statements. 
*  Source code [Location](/Rascal/Expressions/Values/Location)s (`loc`) based on an extension of Universal Resource Identifiers (URI) that allow precise description of text areas in local and remote files.
*  Date and time values ([DateTime](/Rascal/Expressions/Values/DateTime), `datetime`).
*  [List](/Rascal/Expressions/Values/List) (`list`).
*  [Tuple](/Rascal/Expressions/Values/Tuple) (`tuple`).
*  [Set](/Rascal/Expressions/Values/Set) (`set`).
*  [Map](/Rascal/Expressions/Values/Map) (`map`) 
*  [Relation](/Rascal/Expressions/Values/Relation) (`rel`). 
*  Untyped tree structures ([Node](/Rascal/Expressions/Values/Node), `node`).  
*  User-defined algebraic datatypes ([Algebraic Data Type](/Rascal/Declarations/AlgebraicDataType), `data`) allow the introduction of problem-specific types and are a subtype of node. 
  This makes it possible to have typed
  and untyped views on the same data. 
  A special case are syntax trees that are the result of parsing source files are represented 
  as datatypes (`Tree`).


There is a wealth of built-in operators and library functions available on the standard datatypes. 

These built-in datatypes are closely related to each other:

*  In a list all elements have the same static type and the order of elements matters. A list may contain the same value more than once.
*  In a set all elements have the same static type and the order of elements does not matter.
  A set contains an element only once. In other words, duplicate elements are eliminated 
  and no matter how many times an element is added to a set, it will occur in it only once.
*  In a tuple all elements (may) have a different static type. Each element of a tuple may have a label that can be used to select that  
  element of the tuple.
*  A relation is a set of tuples which all have the same static tuple type.
*  A map is an associative table of (key, value) pairs. Key and value (may) have different static 
  type and a key can only be associated with a value once.

#### Examples

Here are some examples of the built-in data types:
| _Type_                    | _Examples_ |
| --- | --- |
| `bool`                    | `true`, `false` |
| `int`                     | `11, 101, 1-11, 1123456789` |
| `real`                    | `1.01, 11.0232e201, 1-25.5` |
| `str`                     | `"abc"`, `"first\nnext"`, `"result: <X>"` |
| `loc`                     | `\|file:///etc/passwd\|` |
| `dateTime`                | `$2101-09-05T07:16:19.714+0200$` |
| `tuple[_T<sub>1</sub>,...,T~n~]`	| `<1,2>`, `<"john", 43, true>` |
| `list[T]`               | `[]`, `[1]`, `[1,2,3]`, `[true, 2, "abc"]` |
| `set[T]`                | `{}`, `{1,2,3,5,7}`, `{"john", 4.0}` |
| `rel[_T<sub>1</sub>,...,T~n~]`   | `{<1,2>,<2,3>,<1,3>}`, `{<1,10,100>, <2,20,200>}` |
| `map[T, U]`           | `()`, `(1:true, 2:false)`, `("a":1, "b":2)` |
| `node`                    | `f()`, `add(x,y)`, `g("abc", [2,3,4])` |


A fragment of the datatype that defines the abstract syntax for statements (assignment, if, while) in a programming language would look as follows:

```rascal
data STAT = asgStat(Id name, EXP exp)
          | ifStat(EXP exp,list[STAT] thenpart,
                           list[STAT] elsepart) 
          | whileStat(EXP exp, list[STAT] body)
          ;
```

Here are some examples how Rascal responds to values of the above built-in datatypes:

```rascal-shell
rascal>true;
bool: true
rascal>101;
int: 101
rascal>3.14;
real: 3.14
rascal>"Rascal";
str: "Rascal"
rascal>|file:///etc/passwd|;
loc: |file:///etc/passwd|
rascal>$2101-09-05$;
datetime: $2101-09-05$
rascal>[30, 20, 10];
list[int]: [30,20,10]
rascal><"Rascal", 100000>;
tuple[str,int]: <"Rascal",100000>
rascal>{"apples", "oranges", "bananas"};
set[str]: {"oranges","bananas","apples"}
rascal>{<"apples", 10, 15>, <"oranges", 5, 7>, <"bananas", 9, 11>};
rel[str,int,int]: {
  <"apples",10,15>,
  <"bananas",9,11>,
  <"oranges",5,7>
}
rascal>("apples" : 100, "oranges": 150, "bananas": 75);
map[str, int]: ("oranges":150,"bananas":75,"apples":100)
rascal>"abc"(1, 2, 3);
node: "abc"(1,2,3)
```


#### Benefits


