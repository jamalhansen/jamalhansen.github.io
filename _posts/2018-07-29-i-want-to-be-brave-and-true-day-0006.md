---
layout: post
title: I want to be brave and true
image: /img/clojure-logo.jpg
tags:
 - 100 days of clojure
---

# Day 6 of #100DaysOfClojure

Today I remembered another Clojure book that I purchased a while back that I want to read; Clojure for the brave and true. I will add that as a stretch goal for my 100 days. I've downloaded an ebook from No Starch Press and put it into my google books library for future reading. 

## Living Clojure

I have completed additional reading in Living Clojure, covering maps and sets as well as vars and temporary bindings. It's interesting to see how much of this functional methodology has bled over into Javascript and other languages in recent years. 

## Solutions

I also sovled [Get the caps](http://www.4clojure.com/problem/29) on 4Clojure today. This exercize has you write a fuiction that filters a string for capitalized letters. In doing this, I remembered the syntax for anonymous functions which is handy.

Below is my function
```
(fn cap-filter [x]
  (let [chrs (#(clojure.string/split % #"") x)]
    (clojure.string/join 
     (filter #(not= (str %) (clojure.string/lower-case %)) chrs)
    )
  )
)
```

Many elements of Clojure are still baffling to me, but it's nice to get aquainted with the basic building blocks again.
