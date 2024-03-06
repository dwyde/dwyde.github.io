---
title: The Halting Problem
layout: default
---
<p class="date">2020-10-01</p>

Are there problems that no computer can solve?

*The Halting Problem: Proofs and Demos*, <a href="/docs/wyde-halting.pdf">7 pages</a>.

A program `halts(f)` determines if a function `f` terminates or runs
forever. `halts` must handle three cases: 1) `f` halts, 2) `f` doesn't halt, and 3)
`f` halts if and only if a call to `halts(f)` returns false. Given these
three types of input, `halts` returns a Boolean: true if `f` halts and false
if `f` runs forever.

Computer science theory says that case 3) programs are contradictions that
show `halts` cannot exist. I argue that all three cases are valid, but it is
unclear how to categorize three types of programs into a true or false output
without grouping two cases together.

After writing this paper, I saw that <a href="http://www.cs.toronto.edu/~hehner/halting.html">Eric Hehner</a> came to similar conclusions. My main contributions are to simplify the problem to 3 inputs being mapped
  to 2 outputs, analyze Alan Turing's 1954 paper in addition to his 1936 one, and provide Python sample code.

