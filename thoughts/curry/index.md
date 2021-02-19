---
title: Curry's Paradox
layout: default
---
<p class="date">2021-02-18</p>

Curry's paradox arises from statements of the form "If this sentence is true, then [a false proposition]." <a href="https://en.wikipedia.org/wiki/Curry%27s_paradox#In_natural_language" title="Wikipedia - Curry's Paradox">Wikipedia</a> gives the example of "If this sentence is true, then Germany borders China."
Unlike the liar paradox, Curry's paradox does not directly use negation (<a href="https://plato.stanford.edu/entries/curry-paradox/" title="Stanford Encyclopedia of Philosophy">SEP</a>).

I have two observations about Curry's paradox:

1. Its negation is true.
1. It is equivalent to the liar paradox.

Both points require that the negation of a self-referential sentence refers to the new sentence (itself) rather than to the original one, which I have <a href="/thoughts/moonshot-papers/#negation" title="Two Ways to Negate Self-Referential Sentences">previously discussed</a> for the liar paradox and G&ouml;del's incompleteness theorems.

# Negating Curry's Paradox
Curry's paradox features implications of the form *p &rarr; q*, where *p* is "This sentence is true" and *q* is a false proposition. The negation of such an implication is *p &and; &not;q*. Taking the example from earlier, we have "This sentence is true and Germany does not border China," which is true.

# Equivalence to the Liar Paradox
*p &rarr; q* is logically equivalent to *&not;p &or; q*. Curry's paradox uses a false *q*, so
*&not;p &or; q* reduces to *&not;p*. The negation of "This sentence is true" is "This sentence is false," which is the liar paradox.

# Validity Curry
In their paper "Two flavors of Curry's paradox," Beall and Murzi give a variant of Curry's paradox called v-Curry, where "v" stands for "validity". An example version is "The argument from me to absurdity is valid." Its negation, "The argument from me to absurdity is not valid," is true.

# Conclusion
A different way of negating self-referential sentences resolves two forms of Curry's paradox.
