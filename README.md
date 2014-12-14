seanlisp
========

My personal homespun lisp interpreter written in c. Mostly written by Daniel Holden while following his excellently written ebook [Build Your Own Lisp](http://www.buildyourownlisp.com/) with of course my additions.

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

## Language Features
