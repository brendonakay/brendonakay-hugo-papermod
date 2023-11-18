---
title: "Types" # TODO make a better name
date: 2020-09-15T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["types", "type theory", "compilers"]
author: "Me"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Desc Text."
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/<path_to_repo>/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

# Purpose

1. Introduction programming language type systems
2. How types help us reason about programs
3. A taste of some applications of type theory (TODO reword this)


# Prelude about types and compilers
Once upon a time we only used assembly. For x86 assembly language, running on 64-bit Linux, a "Hello World!" program looks like this:
```
          global    _start

          section   .text
_start:   mov       rax, 1                  ; system call for write
          mov       rdi, 1                  ; file handle 1 is stdout
          mov       rsi, message            ; address of string to output
          mov       rdx, 13                 ; number of bytes
          syscall                           ; invoke operating system to do the write
          mov       rax, 60                 ; system call for exit
          xor       rdi, rdi                ; exit code 0
          syscall                           ; invoke operating system to exit

          section   .data
message:  db        "Hello, World", 10      ; note the newline at the end
```
credit: https://cs.lmu.edu/~ray/notes/x86assembly/

As our programs grew in complexity the need for high-level programming languages grew. So, we wrote compilers that could translate code written in a high-level language to assembly.

The first commercially available programming language, FORTRAN, came packaged with built in data types. Such as `INTEGER`, `REAL`, `DOUBLE PRECISION`, `COMPLEX`, and `LOGICAL`.

Languages like C would allow you to create custom data types in the form of `sturct`s, which are a form of product types, but more on this later.


## Definition of a type system
Let's start with a [Wikipedia definition](https://en.wikipedia.org/wiki/Type_system).
> In computer programming, a type system is a logical system comprising a set of rules that assigns a property called a type (for example, integer, floating point, string) to every term (a word, phrase, or other set of symbols).
also...
> A type system dictates the operations that can be performed on a term.

Programming languages can implement type systems in a few different ways. They can be statically typed, where validation checks are done at compile time.
They can be dynamically typed, where validation checks are done at run time. Or, they a combination of the two.

Compilers of programming languages can also support type inference. Which is the automatic detection of the type of an expression in the language.

We can also have composite data types, which are combinations of types.

## Examples
### Go
Go is a statically typed, compiled, programming language. Go supports type inference with the `:=` instantiation operator. Unfortunately, this is all Go provides for automatic type detection. Go programs are rather verbose, but the benefit is the programmer can easily reason what the program is doing.

The following is the function signature for the commonly used method `Printf` in the `fmt` standard library package.

```Golang
func Printf(format string, a ...any) (n int, err error)
```

We can see the first parameter is a `string`, followed by a variadic parameter that can take one or more `any` (which is a type alias for `interface{}`). These are the format string and its variables. The function returns a number and an error, which represent the number of bytes written and any error encountered.

### Python
Python is a dynamically typed, interpreted, programming language. Recently Python introduced type hints, but [does not enforce these types](https://docs.python.org/3/library/typing.html) at compile time. You must rely on third party libraries to do type checking.

Looking for the comparison implementation for the above Go standard library `fmt.Printf`, I learned that the [standard `print` function for Python is actually written in C](https://github.com/python/cpython/blob/2.7/Python/bltinmodule.c#L1580).

# Why types help us

Used to prevent certain kinds of values from being used with values in operations that would not make sense. These come in the form of type validation errors.

Help us reason about a program. Types are a product of high-level programming languages. (TODO: Expand on this. Maybe mention how higher level programming languages arose from the increasing complexity of assembly programs.)

From the Python documentation [Typing Python Libraries](https://typing.readthedocs.io/en/latest/source/libraries.html) :

  Why provide type annotations?

  Providing type annotations has the following benefits:

    Type annotations help provide users of libraries a better coding experience by enabling fast and accurate completion suggestions, class and function documentation, signature help, hover text, auto-imports, etc.

    Users of libraries are able to use static type checkers to detect issues with their use of libraries.

    Type annotations allow library authors to specify an interface contract that is enforced by tools. This lets the library implementation evolve with less fear that users are depending on implementation details. In the event of changes to the library interface, type checkers are able to warn users when their code is affected.

    Library authors are able to use static type checking themselves to help produce high-quality, bug-free implementations.

Keep in mind Python can also be used as a scripting language. Usually for scripting, types aren't necessary. Or, at least explicit type annotations. A type inferencing system that works behind the scenes would be beneficial in my opinion. For an extreme case of this, check out [Using Haskell as my shell](https://las.rs/blog/haskell-as-shell.html).

Remember, types come in handy when the complexity of your program grows beyond a simple script.

# Algebraic Data Types

# TODO
- Go through inline TODOs
- Create more code examples for each section
- Final section on type theory
- Generics (refer to Dillon's talk)

