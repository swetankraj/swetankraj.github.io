---
layout: post
title: Useful Vim Commands
tags: [vim, linux]
comments: true
---

Following list contains some of useful and my favourites vim commands I've come across. The list is in no particular order and I'll update it as I come across. 

## 1. Search and Replace

~~~
%s/Pikachu/Pikachu and Bulbasaur/gc
~~~

![Crepe](/assets/img/posts/1/pikachu-bulbasaur.png){: .mx-auto.d-block :}

This is a very powerful command, if you want to replace single occurence or all.

This first *Pikachu* is the search term, followed by *Pikachu and Bulbasaur* which is the term to be replaced.

Hit Enter, and you will be given few options:
*   *y* - yes, to replace currently highlighted text.
*   *n* - no, not to replace currently highlighted text.
*   *a* - all, to apply changes to all the term.
*   *q* - quits, without changing anything.
*   *l* - do the last change, then exit.

![Crepe](/assets/img/posts/1/replace-with-pikachu.png){: .mx-auto.d-block :}
