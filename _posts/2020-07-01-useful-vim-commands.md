---
layout: post
title: Useful Vim Commands
tags: [vim, linux]
comments: true
---

The following list contains some of the useful and my favorites vim commands I've come across. The list is in no particular order and I'll update it as I come across awesome ones. 

## 1. Search and Replace


![Crepe](/assets/img/posts/1/find-replace-command.png){: .mx-auto.d-block :}

~~~
%s/Pikachu/Pikachu and Bulbasaur/gc
~~~

This is a very powerful command if you want to replace a single occurrence or all.

This first **Pikachu** is the search term, followed by **Pikachu and Bulbasaur** which is the term to be replaced.

![Crepe](/assets/img/posts/1/replace-with-pikachu.png){: .mx-auto.d-block :}

Hit Enter, and you will be given a few options:
*   **y** - yes, to replace currently highlighted text.
*   **n** - no, not to replace currently highlighted text.
*   **a** - all, to apply changes to all the terms.
*   **q** - quits, without changing anything.
*   **l** - do the last change, then exit.


