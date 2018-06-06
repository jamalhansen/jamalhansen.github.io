---
layout: post
title: Every and some in javascript
image: /img/2018-06-05-array-find-js.png
---

Last night when [working through the simple cipher exercise](http://exercism.io/submissions/688481148d0b4ec8900838675a547de2) on [exercism.io](https://exercism.io), I submitted a solution that an array filter to find characters that I didn't want in an array. 

This seemed clunky because I didn't need to find all the values that were invalid, I only needed to find one to throw an error. 

I found the find array function which was an improvement. 

Fortunately I got feedback from [mgmatola](http://exercism.io/mgmatola) that clued me in to the every() and some() array functions.

Using these clarified my intent that I am looking for exceptions rather than the rule. 

```
const validateKey = (key) => {
  return key.split('').every(val => values.includes(val));
}
```
