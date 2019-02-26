# Zygomys Tour

*A port of the Go Tour to Zygomys*

[![][logo]][logo-large]


## About

The text from this tour is taken wholesale from
[A Tour of Go](https://tour.golang.org/list), with minor adaptations applied
where necessary for a Lisp. Unlike the Go tour, though, this doesn't have an
AppEngine instance -- you'll need to run it locally on your machine.

Additionally, a section was added for running code from the REPL. The text for
the REPL section was adapted from the
[Structure and Interpretation of Computer Programs](https://mitpress.mit.edu/sites/default/files/sicp/full-text/book/book.html).

[Zygomys](https://github.com/glycerine/zygomys) is a Lisp written in Go that
also allows for Go interop.


## Prerequisites

* You will need to have
[installed the Go programming language](https://golang.org/doc/install).
* You will need to have downloaded `zygo`: `go get github.com/glycerine/zygomys/cmd/zygo`


## The Tour

### Basics

The starting point, learn all the basics of the language.

Using the REPL, declaring variables, calling functions, and all the things you
need to know before moving to the next lessons.

* [zygo, the Zygomys REPL](docs/01-basics/01-repl.md) - Learn how to run the
  REPL and execute code from it.
* [Packages, variables, and functions](docs/01-basics/02-packages-variables-and-functions.md) -
  Learn the basic components of any Zygomys program.
* [Flow control statements: for, if, else, switch and defer](docs/01-basics/03-flow-control-statements.md) -
  Learn how to control the flow of your code with conditionals, loops, switches
  and defers.
* [More types: structs, slices, and maps](docs/01-basics/04-more-types.md) -
  Learn how to define types based on existing ones: this lesson covers structs,
  arrays, slices, and maps.


### Methods and Interfaces

Learn how to define methods on types, how to declare interfaces, and how to put
everything together.

* [Methods and interfaces](docs/02-methods-and-interfaces/01-methods-and-interfaces.md) -
  This lesson covers methods and interfaces, the constructs that define objects
  and their behavior.


### Concurrency

Zygomys provides concurrency features as part of the core language.

This module goes over goroutines and channels, and how they are used to
implement different concurrency patterns.

* [Concurrency](docs/03-concurrency/01-concurrency.md) - Go provides
  concurrency constructions as part of the core language. This lesson presents
  them and gives some examples on how they can be used.


## License

Copyright © 2019, Zygomys-Aided Enrichment Center

Apache License, Version 2.0.




<!-- Named page links below: /-->

[logo]: https://raw.githubusercontent.com/zygosc/resources/master/logos/zygomys-science-innovators-logo-250x.png
[logo-large]: https://raw.githubusercontent.com/zygosc/resources/master/logos/zygomys-science-innovators-logo-1000x.png
