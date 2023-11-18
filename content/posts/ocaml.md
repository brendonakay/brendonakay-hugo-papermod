---
title: "My 1st post"
date: 2020-09-15T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["ocaml", "functional programming"]
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

# Trying out OCaml
I read a post somewhere that said "OCaml is Rust with garbage collection."
And somewhere else someone related OCaml to Go. So, naturally I became interested.
I've been learning Haskell for the last six months. It's been a journey because
Haskell has so much to offer. Sometimes it's overwhelming.

I am excited that it is statically typed, with effects built into the type
system, ADTs, etc.

Platform tools are working well so far. I appreciate standard platform tools
that are provided by the language maintainers.

Compiling seems to take a while but what can you do. Even Rust suffers from
lengthy compilation AFAIK. It seems to be compilers with rich type systems
suffer from lengthy compilation times, which makes sense.

LOVE the `unit` type. This represents I/O. In Haskell, the Monad is eventually
easy enough to understand, but this is dead simple. I appreciate that.

LSP setup has been easy. Looks like you need to rebuild for the LSP to
pick up a new module.

I really dig the simple module system. A file is a module and lives in `lib/`.
Great. Reminds me of `pkg/` for Go. I wonder if there's an `internal/`
equivalent. Some way to hide private library code.

Public and private entities are defined in the module interface.
These `.mli` files define the public interface for the module. Super simple.

The community website https://ocaml.org/ is absolutely amazing for getting
started and up to speed with OCaml.

My only criticism is that the standard library is pretty sparse. As compared to
Go, which is "batteries included", I find OCaml to be "batteries not included
and some assembly required". Not necessarily a bad thing because there are
usually just a handful of libraries to choose from for some task, and the
community openly supports them.
