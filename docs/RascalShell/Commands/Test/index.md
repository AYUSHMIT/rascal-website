---
title: Test Command
---

#### Synopsis

Run tests.

#### Syntax

* `:test`

#### Description

Run Rascal tests. The tests in all currently imported modules are executed and the results are reported
in the terminal.

#### Examples

Execute the tests in an imported module:


```rascal-shell 
rascal>import demo::basic::Factorial;
ok
rascal>test
```

Execute the tests in the `Integers` module in the Rascal test suite:

```rascal-shell 
rascal>test lang::rascal::tests::basic::Integers
```

