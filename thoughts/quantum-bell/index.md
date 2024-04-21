---
title: Bell Tests and Coin Flips
layout: default
---
<p class="date">2024-04-03</p>


# Introduction

I previously wrote a [paper](/thoughts/quantum-local-realism/) on an
interpretation of quantum mechanics. It makes the same predictions as
existing explanations while sounding a lot like classical physics.

My goal with this post is to give a less formal explanation of that theory,
with a few new ideas.


# Overview

I'm going to start with a thought experiment. Its setting is classical
physics, but the ideas should help illustrate some important aspects of
quantum mechanics.

I'll then go into more detail on photon polarization, and how it may be
possible to explain certain parts of quantum mechanics in a straightforward fashion.


# Coin Flips

I'm going to design a machine for flipping coins, with a few unusual features.

First, I need two coin flippers. Each flipper can be thought of as a mechanical
thumb. I can place a coin on a platform, then push a button, and the machine will
flip the coin. The coin may land on either side; I don't know which, but, if
I knew all of the variables down to a microscopic level, it seems like I might
be able to use the laws of physics to predict which way it will land.

I'll have a way of controlling the angle of the platform on which a coin is
placed. Some people think it's necessary to be able to set the angle randomly,
rather than with a manual dial, or else I might have a loophole
in the integrity of the experiment. That concern is hopefully going to seem
unnecessary when I'm done, but people spend a lot of time
[worrying about it](https://en.wikipedia.org/wiki/Bell_test#Notable_experiments).

The two coin flippers should be made as similar to each other as possible. In
theory, the same coin should have the same result if it were able to
be exactly copied and then flipped separately by both flippers.

I also need to make special coins. I have a coin processor at the start
of each trial. It takes a standard US quarter as input, then melts it down and
creates two new coins. Each new coin has one side marked heads and one side
marked tails. The new coins will be flipped, one at each flipper.
A pair of coins has the property that, if the angles of the flippers are
the same, either both coins will land on heads or both coins will land on tails.

I can try to model what will happen if I set the two flippers to different angles
before flipping each pair of coins. It turns out that, if I call the difference
between the angles of the flippers &theta;, the chance that the coins agree should
vary with cos<sup>2</sup>(&theta;). You might imagine that there is some function
that determines the correlation, and in this particular setup, that's what it is.
It means that even slight differences in the angles of the flippers can lead
to a result with one heads and one tails.

To run the experiment, I first make the coin flippers very far apart from each
other. Then, I create a series of pairs of coins. For each pair, I send one
coin to one flipper and the other coin to the other flipper. I try to disturb
the coins as little as possible in transit, to avoid them getting knocked out of
sync in an effect called
[decoherence](https://en.wikipedia.org/wiki/Quantum_decoherence).
Then, I flip them.

For each pair of coins, I vary the angles of the flippers as unpredictably as I
can. After a number of trials, I compare the rate of heads-heads and
tails-tails pairs against the predicted value.


# Bell Tests

There is a very similar experiment in quantum mechanics called a
[Bell test](https://plato.stanford.edu/entries/bell-theorem/#EarlExpeTestBellIneq).
In one version, it uses photons instead of coins and polarizers instead of
flippers.

Bell tests are usually interpreted to rule out certain kinds of 
[local](https://doi.org/10.1088/1751-8113/47/42/424010)
theories.
That means people think, if the flippers are far enough apart, something must
happen faster than the speed of light in order for them to agree at
a rate of cos<sup>2</sup>(&theta;). That would be in conflict with relativity,
and is generally regarded as a
[surprising and deep result](https://www.nobelprize.org/prizes/physics/2022/popular-information/).

Given the way they were created as a pair, it seems possible that the coins have
some sort of shared state. One might then wonder by what physical mechanism the
coins always agree on the same result when they are flipped at the same angle,
even when they are far away from each other.

An alternative view is
[superdeterminism](https://en.wikipedia.org/wiki/Superdeterminism),
which says that the angle of one flipper and a coin landing heads or tails at
the other flipper are caused by a common event in their past. Many people
seem to think that this means there is no
[free will](https://doi.org/10.3389/fphy.2020.00139),
and reject the idea based on that, rather than on whether they
think that kind of correlation makes any sense on its own. A related view to
superdeterminism is
[retrocausality](https://plato.stanford.edu/entries/bell-theorem/#OptiLeftOpenExpeViolBellIneq),
the idea that the future causes the past.

It seems that these coin flips are quite tricky to explain.


# A Simpler Explanation

A simpler explanation is that the states of the two coins in a pair are
synchronized, rather than shared. Each coin is completely separate from the
other, but they will still agree if sent to identical flippers.

In that case, the main thing left to explain is why the
correlation is cos<sup>2</sup>(&theta;) when the angle varies. This is where the
analogy between the classical and quantum versions starts to break down: for
coins, it isn't clear why it would be that value; however, for Bell tests,
that is what is observed.


# An Interpretation of Quantum Mechanics

The paper I linked to at the beginning of this post goes into more detail on
an interpretation of quantum mechanics that I'm going to describe now.

The idea is to start with
[Bohmian mechanics](https://en.wikipedia.org/wiki/De_Broglie%E2%80%93Bohm_theory),
then try to remove its nonlocality.

Bohmian mechanics explains the
[double-slit experiment](https://plato.stanford.edu/entries/qm-bohm/#TwoSlitExpe)
by each particle having
an associated wave. The wave goes through both slits, while the
particle goes through only one slit. The particle is drawn where the interference
of the wave is constructive, and not to where it is destructive.
That is the cause of the interference pattern in the double-slit experiment.

I'll use the explanation for the wave-particle duality and the double-slit
experiment from Bohmian mechanics. Entanglement involves nonlocality in
normal Bohmian mechanics, but I will instead use the coin experiment's
synchronized states explanation for entanglement and thus Bell tests.
The resulting theory is local and deterministic.

A
[common criticism](https://doi.org/10.1017/CBO9780511622687)
of Bohmian mechanics is that it requires extra math.
I think that's a small price to pay for being able to say the precise
position of a particle, rather than just a probability distribution of
where the particle is.

Imagine I asked you to guess a number chosen uniformly at random from 1 to 100,
then told you its square. You could say it has a 50% chance of it being even,
or you could do some extra math and tell me the exact number.


# Malus's Law

There are several ways in which cos<sup>2</sup>(&theta;) comes up that are
related to the topics in this article.

One example is
[Malus's law](https://en.wikipedia.org/wiki/Polarizer#Malus'_law_and_other_properties).
It says that if you put one linear polarizer after
another, with an angle of &theta; between them, the intensity of light that
passes through both is proportional to cos<sup>2</sup>(&theta;).

It can normally be assumed that the light involved when applying Malus's
law isn't polarized in any particular way. That is, it's a collection of
photons with varying polarizations, distributed roughly
[uniformly at random](https://en.wikipedia.org/wiki/Optics#Changing_polarization).

Photons are quanta, so a photon must either completely pass through or
completely be blocked at a polarizing filter. The intensity of the light
will be linearly related to the number of photons that pass through. So, one
would expect each photon to have a chance of cos<sup>2</sup>(&theta;) of
passing through both filters.

In this article's interpretation, there is no randomness. Each photon has some
internal state that causes it to pass through a polarizing filter with a
probability that depends on cos<sup>2</sup>(&theta;). Given that internal state
and the angle of polarization, whether the photon passes through is
deterministic: the probability results from a lack of knowledge about
the state and polarization.

There's an
[experiment](https://en.wikipedia.org/wiki/Polarizer#Malus'_law_and_other_properties)
in which one polarizing filter is at 0&deg; and another
is at 90&deg; behind it. In that case, almost no light gets through. Then, a
third filter is inserted between them at 45&deg;, and some light gets through.
All of the photons entering the second filter should be polarized the same way;
that some but not all of them get through can be explained by varying internal
state.


# Waves

It may be possible to think of a photon as like a particle or a wave,
given the assumption that it has an associated wave as in Bohmian
mechanics. One advantage of thinking of a photon as like a wave is that it
provides another possible explanation for the cos<sup>2</sup>(&theta;) value.

The energy in a wave is proportional to the
[amplitude squared](https://en.wikipedia.org/wiki/Intensity_(physics)).
A
[linear filter](https://en.wikipedia.org/wiki/Photon_polarization#Passage_of_a_classical_wave_through_a_polaroid_filter)
blocks the part of a wave that is moving in one dimension,
while allowing the rest to pass through. The proportion of the energy of
a wave moving in the direction that passes through the filter is
cos<sup>2</sup>(&theta;), since the amplitude depends on cos(&theta;).
Part of the wave passing through may be less relevant to polarization
because photons are quanta, but there is some conceptual overlap.

It may also be worth noting that the
[Born rule](https://en.wikipedia.org/wiki/Born_rule), in simple cases, says
that the probability of making a measurement depends on the amplitude
of the wave function, squared. That seems like it could be related to
the above points if the wave function is seen as physically real,
and possibly to the explanation for the double-slit experiment in
Bohmian mechanics.


# Conclusion

It seems that some results in quantum mechanics, such as Bell tests
and double-slit experiment, can be explained in an intuitive way.

It may be possible to have an interpretation of quantum mechanics that
preserves locality, particles having a defined state
[at all times](https://en.wikipedia.org/wiki/Copenhagen_interpretation),
one result
[per measurement](https://en.wikipedia.org/wiki/Many-worlds_interpretation),
and other ideas from classical physics.

