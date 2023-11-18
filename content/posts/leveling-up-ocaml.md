---
title: "Leveling Up OCaml"
date: 2023-11-18
# weight: 1
# aliases: ["/first"]
tags: ["ocaml", "functional programming", "advent of code"]
author: "Me"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Solving Advent of Code puzzles with OCaml"
#canonicalURL: "https://canonical.url/to/page"
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

# Advent of Code

I thought I'd level up my skills with OCaml by practicing last
year's Advent of Code puzzles.

To learn idiomatic OCaml I am referencing a public repo https://github.com/EvgenyPetrovsky/aoc2022_ocaml
I am going through and adding comments in areas to further clarify my
understanding.

My goal is to only use day 1 as a reference and work on the rest of the days
myself.

I also want to build a module that optionally retrieves the day's input. Maybe
optionally store it in an input folder? Functional programming makes this an
easy task since the types are static. I know where to "plug in" my module.

This will also be a lesson in Functors and Modules.

# Progress
I had a lot of challenges with Nix starting this out. I'll talk more about those in another post.

Modules and Functors were pretty straight forward if you understand Go interfaces. I sense that there are deeper differences between Go interfaces and OCaml Functors.

