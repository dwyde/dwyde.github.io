---
title: Moonshot Papers
layout: default
---
<p class="date">2020-10-01</p>

I wrote four papers on fundamental questions in math and science.

Original ideas on these topics are usually wrong,
but hope springs eternal.

<h1>Contents</h1>
<ul>
<li><a href="#quantum">Quantum Mechanics</a></li>
<li><a href="#negation">Negation</a></li>
<li><a href="#diagonal">Diagonal Arguments</a></li>
<li><a href="#halting">The Halting Problem</a></li>
</ul>

<h1><a name="quantum">Quantum Mechanics</a></h1>
Do the laws of physics affect big and small things differently?

*A Deterministic Interpretation of Quantum Mechanics*,
<a href="/docs/wyde-quantum.pdf">4 pages</a>.

Quantum mechanics describes particles with wave-like behavior,
entangled particles whose measurements are correlated, and other phenomena that
are hard to explain with ideas developed before 1900.

Different interpretations of quantum mechanics make the same real-world predictions but tell divergent stories about why and how things happen.
Bohm's interpretation handles the wave-particle duality well, but its explanation of entanglement
is incompatible with relativity.

A modified version of Bohm's interpretation can explain entanglement as a past
interaction between two independent particles. This new theory is deterministic and resolves paradoxes such as Schr&ouml;dinger's cat and Wigner's friend.

<h1><a name="negation">Negation</a></h1>
What is the opposite of a self-referential sentence?

*Two Ways to Negate Self-Referential Sentences*, <a href="/docs/wyde-negation.pdf">2 pages</a>.

One form of the liar paradox is "this sentence is false."
Trying to evaluate this paradoxical statement leads to a type of infinite loop: if it is true it must be false, and if it is false it must be true.

Kurt G&ouml;del's incompleteness theorems are based on an undecidable sentence, roughly
"this statement is not provable." As in the liar paradox, neither that sentence nor its negation is provable. 

One way to bypass the liar paradox and G&ouml;del's incompleteness theorems is to have the negation
of a self-referential sentence refer to the new sentence (itself) rather than to the original statement.

With this approach, the negation of the liar sentence is "this sentence is true," which resolves
the paradox. A similar analysis applies to G&ouml;del's undecidable sentence.


<h1><a name="diagonal">Diagonal Arguments</a></h1>
What do we learn when we try to list the elements of an infinite set?

*Diagonal Arguments and Infinite Sets*, <a href="/docs/wyde-diagonal.pdf">2 pages</a>.

A diagonal argument is a proof technique that creates a contradiction by attempting to list every element of an infinite set.

Georg Cantor used a diagonal argument to prove that the infinite set of real numbers is larger than
the infinite set of natural numbers. Alonzo Church used a similar proof to show that some
algorithms are impossible to implement.

I think Cantor's and Church's diagonal arguments prove only that it is
impossible to list every element of an infinite set. In each case, the argument should
end before the final step that proves the intended result.

<h1><a name="halting">The Halting Problem</a></h1>
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

