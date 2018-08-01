---
layout: post
title: Two more 4clojures
image: /img/clojure-logo.jpg
tags:
 - 100 days of clojure
---

# Day 8 of #100DaysOfClojure

I solved 2 prolems on 4clojure today. I'm happy that I am making progress and learning some new functions. Today I used get for the first time.

* [Drop every nth item](http://www.4clojure.com/problem/41)
* [Intro to some](http://www.4clojure.com/problem/48)

## Solutions

Intro to some was pretty straightforward. Drop every nth item was more challenging. Looking back there was probably a way to solve this using the nth function but I used indexed-map in mine

```
#(map 
  (fn [x] (get x 1))
  (filter 
    (fn [x] (not= (mod (get x 0) %2) 0))
    (map-indexed (fn [idx itm] [(+ idx 1) itm]) %1)
  )
)
```
