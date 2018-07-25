---
layout: post
title: JavaScript dates are crazy
image: /img/js-logo-sm.png
---

Today I wrote a little program to track which day of #100DaysOfCode I am on.

In doing so I learned that dates in JavaScript are crazy.

```
const notJanuaryFirst = new Date(2018, 1, 1);
```

For instance, why is the month in the date constructor zero based causing the above to return February first?
