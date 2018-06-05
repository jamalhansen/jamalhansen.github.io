---
layout: post
title: Supermarket queue kata on CodeWars
image: /img/code-wars.png
---

I'm on day 10 of the #100DaysOfCode challenge and I have been playing with different learning tools.  I signed up for [Codewars](https://codewars.com) and have been solving kata there. 

When solving [The Supermarket Queue](https://www.codewars.com/kata/the-supermarket-queue/train/javascript) kata. I misunderstood the requirements and couldn't figure it out. Anyway, I'll post my code here because I can. 


```
const q = x => new Array(x).fill(0);
const swipe = (x) => {
  const min = Math.min.apply(Math, x.filter(y => y > 0));
  const x1 = [...x].map(y => y - min < 0 ? 0 : y - min);
  return [x1, min];
};
const fill = ([...x], [...q]) => {
  let i = 0;
  while(q.length > 0 && x.some(y => y === 0)) {
    x[i] == 0 ? x[i] = q.pop() : x[i];
    i++;
  }
  return [x, q];
};
const done = (x, q) => x.every(x => !x) && q.length == 0;

function queueTime(customers, n) {
  let checkout = q(n);
  let queue = [...customers];
  let time = 0;
  let min = 0;
  
  while(!done(checkout, queue)) {
    [checkout, queue] = fill(checkout, queue);
    [checkout, min] = swipe(checkout);
    time += min;
  }
  return time;
}
```

