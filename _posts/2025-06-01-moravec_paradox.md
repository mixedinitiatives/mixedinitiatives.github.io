---
title: Moravec's Paradox
excerpt: "Hard things are easy. Easy things are hard."
author: Isaac Karth
published: true
---


There's a curious thing about AI that we've known for a long time. It's sometimes called Moravec's Paradox, after Hans Moravec, though a number of other computer scientists in the 1980s also espoused the idea. 

Moravec was writing about the problem of the intelligent robot, "a machine that can think and act as a human, however inhuman it may be in physical or mental detail." (Moravec 1988, p. 2) One of the things that Moravec discusses (in his book _Mind Children_ and elsewhere) is curious phenomenon that, despite building expert systems that could solve complex calculus problems and chess-playing programs that could, even then, defeat chess masters, their robots struggled to do something as simple as building with children's blocks or apply common-sense reasoning that would tell it that a bicycle can't be fixed with antibiotics (Moravec 1994). Researchers had managed to make a computer that could do many tasks that are hard for humans, but had repeatedly been defeated by toddlers at things that seemed trivial. In the artificial intelligence world, hard things are easy, and easy things are hard.

Moravec's answer was to build robots that needed to see and move in the physical world, and thereby learn intelligence from the bottom up. He predicted a sequence of development of universal robots, starting dumb robots, then introducing learning, then giving them the ability to simulate their surroundings, which give you "neatly organized data about the robot and its world that can be married to a reasoning program to produce a machine with most of the abilities of a human being" sometime around 2040. We've made some progress in robotics and the physical world, but the neatly organized progression Moravec describes has been rather upended by the unexpected success of neural networks in the 2010s, back from the dead. We now have something that is a little like the messy bottom-up evolved common-sense understanding that Moravec anticipated, but rather than being based on the directness of the real world, it is instead learned from language and imagery itself.

With enough interaction with this latest incarnation of artificial intelligence, it quickly becomes apparent that the paradox is still with us. The language models are capable of astonishing task generalization but in a way that is often quite spiky: we've invented models that can explain calculus but can't multiply (or spell) and that can (sometimes) [play chess](https://dynomight.net/more-chess/) at a high level but completely fail to grasp how tic-tac-toe works [^1]. The neural net models are spiky, often in ways that are highly counterintuitive. We're used to being able to predict that if someone is good at one thing, they're also good at related thing. That intuition is going to betray you. Hard things are easy, easy things are hard.

My original interest in generativity is in neither the easy things nor the hard things. We can already do the easy things (even if the AI can't). We can already do the hard things (they're just more effort). But the impossible things that generativity enables: _that's_ the really interesting place to be. 


[^1]: Structured prompting makes them better, but in general they're terrible at recognizing what a win condition is in the game, or how to lose gracefully, or really anything we expect a five-year-old child to learn about the game. Language models may, of course, get better at this in the future, but it's a useful illustration of the spiky nature of the models does not have a linear correspondence to the human experience of difficult tasks.

___


### Biblography:

Moravec, Hans. Mind children: The future of robot and human intelligence. Harvard University Press, 1988.

Moravec, Hans. "The universal robot." Interdisciplinary Science and Engineering in the Era of Cyberspace (1993): 35.