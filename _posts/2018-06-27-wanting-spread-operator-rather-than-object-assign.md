---
layout: post
title: Spread operator and object assign
image: /img/nodejs.jpg
---

Today, I tried to combine two objects in node. The actual values and the default ones. I wanted to use the spread operator to make this simple.

```
const complete = {...default, ...specified}
```

This didn't seem to work in node so I googled around and found Object.assign()

```
const complete = Object.assign(default, specified)
```

When my second test failed, it took me a few hours to find out that his was modifying my default values. The fix was rather simple, but it took me forever to find

```
const complete = Object.assign({}, default, specified)
```

I would like to find out how to use the spread operator for this in node.
