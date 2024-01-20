---
title: "NixOS"
date: 2024-01-20T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["nix", "pde", "personal development environment"]
author: "Me"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Learning to use NixOS"
canonicalURL: ""
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

# In the beginning
I've been interested in the Nix programming language and package manager ever
since I first heard about it from the functional programming community. It
seemed like it was way more popular in that circle than anywhere else. When I
started looking into Nix I discovered NixOS, a flavor of Linux using the Nix
language to configure and package the kernel.

I first got acquainted with NixOS by installing it on a VirtualBox client, on my
Windows desktop. I used their [VirtualBox image](https://nixos.org/download#nixos-virtualbox). 

Nix has a pretty big learning curve. I wanted to
be comfortable tearing down and rebuilding my environment completely. This is
just a little inconvenient on a laptop, or bare metal. Plus, as I learned
eventually, with the power of Nix I could feel comfortable rebuilding, porting,
or sharing my environment with ease.

Once the image was installed it was time to get going on Nix basics.

# Tutorial hell

Nix is a fully functional programming language and package manager. This gets
confusing, especially for beginners, because there is Nix, NixOS, and Nixpkgs. 
From my journey using and learning NixOS, I know now that: 
 - Nix is the programming language and package manager. It can be installed on
 many operating systems, but I will be using it primarily on NixOS, where it
 comes pre-installed.
 - NixOS is the operating system that is the subject of this article. Like
 Ubuntu, Fedora, or Mint, it is a flavor of linux. Unique to NixOS is that it
 configures and packages the Linux kernel using the Nix language. It supports
 64-bit Intel, AMD, and ARM CPUs at the time of this writing.
 - Nixpkgs is the packages repository used in many nix expressions [1]. A Nix
 Flake, which will be covered in more detail later, often uses some package from
 Nixpkgs.

# Future learning
Next steps for me are overlays and custom packages, packages that I can create
myself in case something is not available on Nixpkgs or another repository.
Dream2Nix looks promising for packaging Python projects.

`nix-env` is a good tool to get used to it on the CLI. A good tool for using nix.

Should move eventually to `home-manager` https://nixos.wiki/wiki/Home_Manager

Learning flakes with `opam-nix` Flakes are the most popular way to package
projects in the modern nix era. As far as my understanding goes.

---

[1] https://nixos.wiki/wiki/Overview_of_the_Nix_Language#Expressions
