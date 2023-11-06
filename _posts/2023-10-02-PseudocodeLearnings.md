---
toc: true
comments: false
layout: post
title: Pseudocode Learnings
description: Things I learnt from the Collegeboard MC about Pseudocode
courses: { compsci: {week: 12} }
type: tangibles
---

All of the Keywords are capital in Pseudocode, but lowercase in Python.

`a ← b` is the same as `a = b`, assigment operator is just a left arrow instead of an equal to symbol.
<br>
`DISPLAY("Hello World")` is the same as `print("Hello World")`
<br>
<br>
`RANDOM(a, b)`will translate to 
<br>
`import random`
<br>
`random.randint(a, b)`
<br>
<br>
`REPEAT n TIMES`
<br>
`{`
    <br>
  `(block of statements)`
  <br>
`}`
<br>
translates to
<br>
`for i in range(n):`
<br>
    `(block of statements)`
<br>
<br>
Collegeboard Pseudocode uses a REPEAT UNTIL loop, whereas Python uses a while loop. The difference is that UNTIL runs the loop until a condition is met, but a while loop runs the loop while the condition is true. They are kind of opposites.
<br>
<br>
`FOR EACH item IN aList`
<br>
`{`
<br>
 `(block of statements)`
 <br>
`}`
<br>
translates to
<br>
`for i in aList:`
<br>
    `(block of statements)`
<br>
<br>
`PROCEDURE procName(parameter1, parameter2, ...)`
<br>
`{`
<br>
 `(block of statements)`
<br>
`}`
<br>
translates to
<br>
`def funcName(parameter1, parameter2):`
<br>
    `(block of statements)`
<br>
<br>
The only main difference is that Python doesn't need the curly brackets in a loop or function definition.