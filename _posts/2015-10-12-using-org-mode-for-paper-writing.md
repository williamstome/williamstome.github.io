---
layout: post
title: "Using Org Mode for Paper Writing"
modified: 2015-10-12
excerpt: ""
tags: [emacs, research]
comments: true
image:
  feature:
  credit:
date: 2015-10-12
---

Anyone in my lab can tell you I'm a fanatical user of emacs
org-mode. In this post, I'd like to share how I use org-mode for paper
writing, and why it's awesome. If you're already convinced you should
be using org mode and just want to know what you need to do to get set
up with it, hop to the last section. 

# What is emacs? #
  
  [Emacs](https://www.gnu.org/software/emacs/) is an open source text editor that is highly customizable, and
  can be used for pretty much anything. While it's primarily used to
  edit text files, it can be used [as a shell](http://ergoemacs.org/emacs/emacs_shell_vs_terminal.html), [to browse the web](http://ergoemacs.org/emacs/emacs_eww_web_browser.html), or
  even [to make
  coffee](http://www.emacswiki.org/emacs/CoffeeMode). For better or
  for worse. For more information on why you should use emacs, read
  [this article](http://batsov.com/articles/2011/11/19/why-emacs/). 

# What is org mode? #
  Emacs has (hundreds? thousands?) many "modes" which define your
  current "context", with different features available in different
  modes. If you're writing C++ code, you'll be in C++ mode, with lots
  of nice C++-specific features easily available. When you want to do
  "organizational" things, you can enter "org-mode", and have lots of
  nice organizational tools at your disposal: time tracking,
  scheduling, todo lists, etc.

# How can I use it for writing papers? #

The easiest way to show you how org-mode can be used for writing
papers will be to just show you the "source code" for a paper written
in org mode, and then show you what the resulting PDF looks like. 

    #+TITLE: A Demonstration of Org-Mode Paper Writing
    #+AUTHOR: Tom Williams
    
    #+BEGIN_ABSTRACT
    In this paper, I demonstrate how to write this paper...
    #+END_ABSTRACT
    
    * Introduction
      In this section I introduce how to write this paper.
      
    * Demonstrations of subsections
      In this section, I demonstrate how to use subsectinos
    ** Subsections
       This is how you use subsections
    *** Subsubsections
        This is how you use subsubsections.
    * Tables
      In this section I show you how to use tables
      
      #+CAPTION: This is the table caption!
      #+NAME: tab:my-table
      | Column | Column |
      |--------+--------|
      | Row    | Row    |
      | Row    | Row    |

    * Formatting
      In this section I show you how to do formatting. *This is
      bold.* /This is italicized./ _This is underlined._ =This is
      written as code.= +This is (stricken?) through.= [fn:: This is a
      footnote]. 

    * Images
      In this section I show you how to include an image.

      #+CAPTION: This is an image!
      #+NAME: fig:my-image
      [[./image.png]]

    * Citations and References
      In this section I show you how to refer to Figure
      \ref{fig:my-image} and Table \ref{tab:my-table}, and how to
      shamelessly self-cite \cite{williams2015aaai}.
      
    #+BIBLIOGRAPHY: bibliography plain

# What do I need to do to get things set up? #