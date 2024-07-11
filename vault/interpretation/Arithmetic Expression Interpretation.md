---
title: Arithmetic Expressions
---
Arithmetic expressions are built from numbers, variables and proper names with the help of the operators `+`, `-`, `*`, `/`, `^`. 

All operators are left-associative. 

Standard operator precedence applies: `^` precedes `*` and `/`, that precede `+` and `-`. 

Sub-expressions can be put in parentheses to modify the precedence of the operators. This applies specifically to iterated occurrences of the exponentiation operator `^`. 

For example, the expression `2^3^4` stands for `(2^3)^4`. Use brackets to achieve `2^(3^4)`. 

Arithmetic operators have types, meaning that all arguments must eventually stand for numbers.