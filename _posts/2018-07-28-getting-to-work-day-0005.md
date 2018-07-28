---
layout: post
title: Getting to work
image: /img/clojure-logo.jpg
tags:
 - 100 days of clojure
---

# Day 5 of #100DaysOfClojure

Ok, I've done a lot of ground work up to this point and not much actual learning. I am changing that today.  I read some of Living Clojure and completed two exercises on 4Clojure.

## Lists and Vectors

Today in my reading I found that even though lists and vectors have similar functionality, there is a reason to use one over the other. Lists are made to me accessed in a functional manner where you can pop an item off the head and then use recursion with the rest of the list. Vectors are made to allow indexing into them. So when I want to access the nth item in a sequence, I should use a vector rather than a list because it wil be more performant.

## Solved

Today on 4Clojure I solved two problems:

* [Reverse a sequence](http://www.4clojure.com/problem/23) - where you cannot use reverse or rseq
* [Palendrome detector](http://www.4clojure.com/problem/27) - where you create a function that detects if the input is a palendrome

### Reverse a sequence
Here is my solution for reversing a sequence
```
(fn reverse-it [se]
  (reduce (fn reducer [new n] (cons n new)) [] se)
)
```
### Palendrome detector
Here is my solution to detect palendromes
```
(fn pal [x]
  (=
   (clojure.string/join "" x)
   (clojure.string/join "" (reverse x))
  )
)
```
