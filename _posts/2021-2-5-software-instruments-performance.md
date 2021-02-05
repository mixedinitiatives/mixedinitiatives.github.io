---
title: Software Instruments - Performance
excerpt: "This week is about design space, and its navigation via generative instruments."
author: Jasmine Otto
---

This week is about design space, and its navigation via [software instruments]({% post_url 2021-1-26-software-instruments-def %}). This is the second background section of the series. Next week, we will have the first background section on research debt, which wasn't meant to be self-demonstrating in its indefinite deferral.

### Pens and turtles

Students are often introduced to imperative programming using the Logo language introduced by Papert, which provides a software instrument called a 'turtle'.

A turtle carries a pen, which traces its movement on the canvas. The turtle can be directed to move forward, or to turn by a certain amount, and to repeat a block of such instructions a given number of times.

It turns out that many remarkable figures can be produced by stringing together these instructions and varying their parameterization. Logo is a prototypical example of a 'generative system'.

The Logo environment converts a sequence of instructions into a turtle-made drawing on the screen. The programmer converts this drawing into a modified set of instructions, because they are trying to make or discover another form. This execution-evaluation loop (per Norman) comprises an exploration of the artifact space (see Compton on expressive range) of Logo.

### Practicing with the turtle

All instruments participate in an execution-evaluation loop, as exemplified in 1963 by Sketchpad (cite Sutherland). The loop is the functional unit in a cybernetic system, which consists of a set of subjects, and a set of arcs of interaction between them. For example, a programmer and their Logo environment together comprise a cybernetic system, because the environment executes the programmer's expression of their intent (in terms of Logo affordances), and the programmer evaluates whether the thing they intended really happened or if their instructions went awry somehow.

A (cybernetic) performance comprises of an inner 'practice' loop, involving the player and their instrument, and an outer 'presentation' loop, involving the practice and its audience.

Practices may be improvised (by the player selecting their next action based on the response they anticipate), based on a score (the player selects their next action by consulting a script), or typically combining the two (when the script underspecifies the next action). Performances inherit this property of the practice. In these cases, the player is likely to account for the audience in both their action selection (at the moment-to-moment level of improvisation) and their choice of scores (if they are aware of such choices).

In Reveal Codes, Rita Raley characterizes the navigation of hypertext as a practice with a complex system, one that "functions to separate the digital from the analog", which is echoed in our distinction between the model (whose instance is an artifact) in a software instrument, and its referent which cannot be represented as data.

(Raley describes 'performance' as sequences of actions with a hypertextual instrument but not necessarily an audience, so we will call this sense *practice*. She also describes 'practice' as a form of reading and writing hypertext, implying a long-form conversation within a hypertext community, so we will call this sense *performance*.)

We can substitute any artifact for Raley's hypertext, only if it is the object of a software instrument. We will find that this instrument's expressive range is a complex meaning-making system, as she has described. 

### Performing with the turtle

What is so surprising about practices - that is, action sequences taken in an interaction loop with the artifact that they describe, - is that they illuminate the 'grain of the medium' (cite Barthes), i.e. an attractor structure on the artifact space.

This is most clearly demonstrated by the anecdote about 'failing quickly' as a pedagogical method. Those students who were instructed to create one hundred pots over a semester, were creating higher-quality pots by the end of it than students who had focused their entire energies that semester on one pot.

Recall that generative systems, including Logo and similarly 'rich output' programming environments, describe artifacts in terms of action sequences written in a domain-specific language (e.g. the turtle's vocabulary of 'move forward this far', 'turn by this many degrees', 'set pen up or down'). We call these descriptions 'scores', after the scripts that musicians consult to help them learn a given song.

Musical scores are incomplete, because many inflections and dynamics in the song as it is played are not written down and must be learned 'by ear', i.e. imitation of a presently-existing instance of the song, which is transient. Also, scores are partially transferrable between instruments, as it is possible to play a score written for one instrument on a related instrument, but only by skillfully modifying the score to not make it unrecognizable.

We will discover these properties in software instruments later. For now, imagine the difficulty of learning Photoshop without seeing someone's demo, or of re-writing a Python script into Javascript.

### Analysis of turtle-like systems

Emily Short's characterization of the generative meta-medium (and specifically, her own hypertextual machine collaborator), in the appendix to Annals of the Parrigues, breaks it into the following five complementary lenses ('aspects'):

- Salt, which governs structured processes like crystal growth and tilings.
- Mushroom, which governs branching processes like rhizomic growth and Markov chains.
- Venom, which governs spiky distributions of semantic weight, like when 'distribution' and 'semantics' appear in a sentence together.
- Beeswax, which governs mass-curated processes and crowdsourced collections.
- Egg, which governs singly-curated processes and moments of authorship.

These lenses of analysis apply to instruments, which impose on generative processes enacted with them in related ways. For instace, salt implies structure, mushroom implies self-propulsive energy, and venom implies standout moments. Now think of a generative text which continuously produces utterances that use the same grammatical structure, but which vary in their payload, from 'blossom petals' to 'nuclear runoff'.

By combining aspects and a medium, we have just described a Twitterbot, a kind of artifact described (along with its accompanying creative scene in the 2010s) by Veales and Cook at length. Beeswax seems to describe the 'like' count of a generated tweet, while egg describes the choice by someone to retweet it. Salt, then, also describes the predictable layout of the bot's Twitter page.

We should not be surprised that a characterization of the 'practice' (i.e. bot-making) is equally applicable to the 'performance' (i.e. Twitter presence), which is another interaction loop inside which practice is nested.

It is not possible to circumscribe the possible action sequences with a given instrument in the abstract. Although practice and theory (which we will discuss next section!) together indicate 'rules of design' (goals and constraints on action sequences) that make good artifacts easier to find, these rules are almost never hard and fast.

 For example, one affordance of a guitar is to play semitones on the fretboard. Because it sounds dissonant if you play notes together that do not share a scale (a patterned subset of semitones, characterized as a sequence of intervals), so players learn to move within e.g. the blues scale. As long as the key of the song doesn't change, the player can "improvise freely" over the matching blues scale, meaning that they can choose arbitrarily between next actions that follow the rule without making any mistake. But it is equally important that this rule can be learned, and that it can be unlearned - because it would be very boring to play only one blues scale all the time, and besides, you might want to play in a different key.

With our intuition pump primed in this way, we hope to have motivated a future research project of describing software instruments, whose operational logics serve to navigate the 'rugged landscape' of artifact space.


