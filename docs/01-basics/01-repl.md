# The REPL

Since the early days of the original LISP programming language, Lisp languages
have had a REPL - a "read-eval-print loop" that provides programmers with an
environment wherein code may be dynamically written and evaluated.

Assuming you have set up the prerequisites (see the Zygomys Tour README file
for details), you need only type the following at a terminal:

```
$ zygo
```

At which point the Zygomys REPL will start:

```
zygo version v5.1.1/acef8bb25d1cad8aebed3cedb59b481795ac9fa1
press tab (repeatedly) to get completion suggestions. Shift-tab goes back. Ctrl-d to exit.
zygo>
```

**Note**: for the remainder of this section, text from the
[Structure and Interpretation of Computer Programs](https://mitpress.mit.edu/sites/default/files/sicp/full-text/book/book.html)
will be used.


## Expressions

Expressions representing numbers may be combined with an expression
representing a primitive procedure (such as + or *) to form a compound
expression that represents the application of the procedure to those numbers.
For example:

```lisp
zygo> (+ 137 349)
486
zygo> (- 1000 334)
666
zygo> (* 5 99)
495
zygo> (/ 10 5)
2
zygo> (+ 2.7 10)
12.7
```

The convention of placing the operator to the left of the operands is known as
prefix notation, and it may be somewhat confusing at first because it departs
significantly from the customary mathematical convention. Prefix notation has
several advantages, however. One of them is that it can accommodate procedures
that may take an arbitrary number of arguments, as in the following examples:

```lisp
zygo> (+ 21 35 12 7)
75
zygo>  (* 25 4 12)
1200
```

No ambiguity can arise, because the operator is always the leftmost element
and the entire combination is delimited by the parentheses.

A second advantage of prefix notation is that it extends in a straightforward
way to allow combinations to be nested, that is, to have combinations whose
elements are themselves combinations:

```lisp
zygo> (+ (* 3 5) (- 10 6))
19
```

There is no limit (in principle) to the depth of such nesting and to the
overall complexity of the expressions that the Lisp interpreter can evaluate.
It is we humans who get confused by still relatively simple expressions such
as:

```lisp
zygo> (+ (* 3 (+ (* 2 4) (+ 3 5))) (+ (- 10 7) 6))
57
```

## Naming

A critical aspect of a programming language is the means it provides for using
names to refer to computational objects. We say that the name identifies a
variable whose value is the object.

In the Zygomys dialect of Lisp, we name things with `def`:

```lisp
(def size 2)
```

Once the name `size` has been associated with the number `2`, we can refer to
the value `2` by name:

```lisp
zygo> size
2
zygo> (* 5 size)
10
```

## Functions

We define functions by providing a name, but instead of a value, we need to
provide the arguments the function takes and then the body of the function
itself:

```lisp
zygo> (defn square [n] (* n n))

```

Having defined `square`, we can now use it:

```lisp
zygo> (square 21)
441
zygo> (square (+ 2 5))
49
zygo> (square (square 3))
81
```

We can also use `square` as a building block in defining other functions:

```lisp
(defn sumOfSquares [x y]
  (+ (square x) (square y)))
```

and then use it:

```lisp
zygo> (sumOfSquares 3 4)
25
```

There is much more to cover in the language itself, but for now this should put
you at east with the Zygomys REPL.
