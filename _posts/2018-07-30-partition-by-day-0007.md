---
layout: post
title: Parition by identity
image: /img/clojure-logo.jpg
tags:
 - 100 days of clojure
---

# Day 7 of #100DaysOfClojure

Today I wrapped up chapter 1 of Living Clojure. I also solved 3 prolems on 4clojure

* [Pack a sequence](http://www.4clojure.com/problem/31)
* [Compress a sequence](http://www.4clojure.com/problem/30)
* [Duplicate a sequence](http://www.4clojure.com/problem/32)

I had started on compress a sequence yesterday and got frustrated. Today I started workingon duplicating a sequence first and solved it after a number of failed attempts. After realizing that it could be solved by concatenating a sequence of sequences, I stumbled across the partition-by and identity functions. From there the other two fell into place rather easily

## Solutions
Here are my solutions; I solved them in reverse order of listing

### Pack a sequence
```
#(partition-by identity %)
```

### Compress a sequence
```
#(reduce concat (map distinct (partition-by identity %)))
```

### Duplicate a sequence
```
#(reduce concat (map (fn dbl [x] (list x x)) %))
```
