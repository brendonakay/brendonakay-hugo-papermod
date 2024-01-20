---
title: "Baseball Statistics and Linear Algebra"
date: 2020-09-15T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["ocaml", "linear algebra", "baseball"]
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

Motivated to replicate this experiment after reading this article
[https://medium.com/sports-analytics/the-elegance-of-markov-chains-in-baseball-f0e8e02e7ac4]

## Primary goal Replicate the above experiment, using Markov Chains to calculate
run percentages in baseball. In the process, learn more about linear algebra and
numerical computation programming language libraries.

Except I don't want to just download the Python repo and run the experiment. I
want to actually learn what's going on here. So, my intention is to replicate
this experiment in OCaml using the scientific library
[`owl`](https://ocaml.org/p/owl/1.1).

My development environment will be packaged up using Nix Flakes and
[`opam-nix`](https://github.com/tweag/opam-nix)

`owl` has a wonderful website for their library [https://ocaml.xyz/]

Some of these resources are old and not very informative about transition states
in baseball, the game itself, and some of the more linear algebra stuff, which I
certainly need help with.

Of course I eventually run into some newbie Nix flake issues. I am still
learning how to use `dune`, too, so that combined with `opam` and `opam-nix` is
kind of a struggle. I see now that I need to update the `depends` attribute in
my dune file, then I build the new opam file using `dune build @check`. That's a
bit of a process, but surprisingly it's on-par or even simpler than Haskel's.

I think I have to abandon using Owl or OCaml for this effort. The tools are
almost impossible to set up. They're outdated. I understand some of this is my
fault and my environment, but I'm starting to lose site of my original goal;
which is to expand my understanding of linear algebra by learning about Markov
Chains and their applications to baseball.

I found a nice theoretical article and it gives its examples in Julia. I've
always wanted to learn Julia so I'm hoping this goes a lot smoother. It's a
newer language and made for this purpose.

Okay, so using `julia` was _infinitely_ easier to set up and get working with
than Owl ever could have been. I simply followed the easy instructions (using
the julia CLI itself!) and now have a very simple nix flake and juila set up.
I'm in love.

The package manager in Julia is so nice.

# Resources and further reading
https://github.com/calestini/markov-baseball/blob/master/markov_chain.py
https://statshacker.com/blog/2018/05/07/the-markov-chain-model-of-baseball/
https://julia.quantecon.org/introduction_dynamics/finite_markov.html

# TODO How do I do resource/subscript links?
