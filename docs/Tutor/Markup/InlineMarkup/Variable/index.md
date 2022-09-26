---
title: Variable
---

#### Synopsis

Markup for a variable.

#### Syntax

* `\VarName`
* `\VarName\~Index~`
* `\VarName\^Index^`


#### Description

Variables in text and code are represented by [Italic](../../../../Tutor/Markup/InlineMarkup/Italic/index.md) markup. 
They may be followed by one or more subscripts (enclosed by `~` and `~`) or superscripts (enclosed by `^` and `^`)

#### Examples

* `\Var` gives _Var_.

* `\Var\~1~` gives _Var_~1~.

* `\Var\^1^` gives _Var_^1^.

* `\Var\^1^\~2~` gives _Var_^1^~2~.

#### Pitfalls

* This feature is broken currently. The italics do not work in code fragments and subscripts are broken as well.

