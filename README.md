seanlisp
========

My personal homespun lisp interpreter written in c. Mostly written by Daniel Holden while following his excellently written ebook [Build Your Own Lisp](http://www.buildyourownlisp.com/).

## Installation

Be sure to have a c compiler first. You can make sure with this:
```bash
$ cc --version
```

Then run
```bash
$ cc -std=c99 -Wall seanlisp.c mpc.c -ledit -o seanlisp
$ ./seanlisp
```

And the prompt should look like this:
```bash
Seanlisp Version 0.0.0.1.0
Press Ctrl+c to Exit

seanlisp> (+ 1 2)
3
seanlisp>
```

A Hello World Example:
```lisp
seanlisp> def {main} {print {"hello world"}}
()
seanlisp> main
{print {"hello world"}}
seanlisp> eval main
{"hello world"}
()
```

## TODO
* A Garbage Collector
* Variable Hashtable
* Lexical Scoping
* Macros

# Language Features

## Operators
Seanlisp uses reverse polish notation, the operator comes before the variables.
It supports four operators:
'+', '-', '*' or '/'

Basic operatrions can be written like so:
```lisp
seanlisp> (+ 1 2 6)
seanlisp> (+ 6 (* 2 9))
seanlisp> (/ (* 10 2) (+ 4 2))
```
and as you can see, are processed in a list.

Lists can be defined like so:
```lisp
seanlisp> list 1 2 3 4 5 6 7
{1 2 3 4 5 6 7}
```

## Quoted expression

You may also use an eval operator to evaluate expressions in quoted expressions
```lisp
eval
```

## Variables

Varialbes have to be defined with a Quoted expression:
```
seanlisp> def {x} 100
()
seanlisp> x
100
```

## Functions

Lambda expressions are formed using a slash:
```lisp
seanlisp> \ {x y} {+ x y}
seanlisp> def {add} (\ {x y} {+ x y})
seanlisp> add 10 20
30
```

Functions have to be defined like this:
```lisp
seanlisp> 
(fun {map f l} {
  if (== l nil)
    {nil}
    {join (list (f (fst l))) (map f (tail l))}
})
```

## Conditions

seanlisp supports these conditional statements, for literals and variables:
```lisp
seanlisp> > 10 5
1
seanlisp> <= 88 5
0
seanlisp> == 5 6
0
seanlisp> == 5 {}
0
seanlisp> == 1 1
1
seanlisp> != {} 56
```

## Strings
String can be defined like so:
```lisp
seanlisp> "hello world"
"hello world"
```

## Recursion

## Fun with functions

## MIT License

Copyright (C) Sean Westfall

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
