seanlisp
========

My personal homespun lisp interpreter written in c. Mostly written by Daniel Holden while following his excellently written ebook [Build Your Own Lisp](http://www.buildyourownlisp.com/) with my additions of course.

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
``lisp
```

## TODO
* A Garbage Collector
* Lexical Scoping
* Macros

# Language Features

## Operators

## Symbolic Expression

## Quoted expression

## Variables

## Functions

## Conditions

## Strings

## Recursion

## MIT License

Copyright (C) Sean Westfall

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
