---
title: Software Instruments - Research Debt
excerpt: "A community of practice has research debt when its students and researchers know they need to learn some topic X, but the avalable exposition on topic X is very dense..."
author: Jasmine Otto
---

[Last week]({% post_url 2021-2-5-software-instruments-performance %}), we talked about practice and performance in a computational medium, using instruments to navigate an artifact space. This week, we use our instruments to play in another sense - to 'think the unthinkable', by embedding skill into our representations of and operations on difficult problems.

Next week, we will have our first case study of a software instrument (The Sims 3 Create-A-Sim). In two weeks, the second (a reading of The Wisdom and Madness of Crowds, as if we were porting it to D3.js). After that, we will take a break for revisions.

## Research debt, and its counters

At first glance, it isn't obvious that we have any skill transfer problems in science or engineering. Maybe the problem with math teaching, what makes people afraid of math, is just a problem with math.

Olah and Carter write [1]:
> Often, some individuals have a much more developed version of an idea than is publicly shared. There are a lot of reasons for not sharing it (in particular, they’re often not traditionally publishable).

Mathematics is extreme in this regard, because mathematicians have a lot of explanations that only make sense to other mathematicians, and only if that person takes a lot of time to find the background that makes the explanation make sense. (Surprisingly, mathematicians just do this. They aren't busy with other things, and they can't be.)

Mathematics has a lot of research debt, in other words.

A community of practice has research debt when its students and researchers know they need to learn some topic X, but the public exposition on topic X is very dense and requires a few years to digest.

This becomes a problem when people keep re-inventing knowledge about topic X, but using a different terminology that is less inscrutable to them. Usually it is specialized to their use case, which angers people who are using the otherwise inscrutable terminology, if they realize it is the same thing at all.

Any topic can be and will be a topic X, but the more abstraction it contains, the worse this situation gets. I'm going to assert that science and engineering contain a large and increasing amount of abstraction, in the present historical moment.

#### Grounding

Interactive articles are unreasonably effective at cutting through research debt. They are both demonstration, and instructions for a computer to reproduce that demonstration. They are more portable than other forms of software, because they can run in a browser or in a computational notebook environment.

Conrad Wolfram has talked about [2] using interactive articles to tackle mathematics pedagogy, a kind of research debt that every schoolchild runs into, using rich visual output and parameter sweeps.


When Wolfram focuses on the pupil and their notebook of calculations, and how much faster a computer is than a page for this usage, he resides in the parts of the interaction loop. When Bret Victor expands on [3] the idea of representation and direct manipulation of the parameters, he resides in the arcs of the interaction loop.

Nielsen's notes on Victor continue [4] to discuss the data visualization operations of linked brushing and drilling down. But he is getting at the building blocks of them now, the operational logics* of an interactive article.
> * The operation of "tying" two quantities together, to form a single linked entity.
> * The operation of scrubbing a number.
> * The operation of "searching" over the graph. 

* See Joe Osborn's catalog [5] from his dissertation. Note 'linking' the scrubbing slider to the parameter, 'controlling' that slider with the mouse, and 'spatial matching' over the parameteerized space of graphs.

#### Reproducibility

Many computational notebooks are not articles themselves, but distributed alongside papers, providing a reproducible computational component. It is better to share notebooks than to share scripts because a notebook can encapsulate more of its own environment configuration, and is therefore more likely to run on someone else's computer. Some scripts (and other scientific softwares) are distributed in Docker containers for this reason.

It is typical to share both software and libraries through a package-management system, such as Python's pip, Javascript's npm, or Scala's sbt (to name a few). Because scientific software written in Python often has non-Python dependencies (such as the Math Kernel Library, or other C++ and Fortran code), the Anaconda distribution of Python has a specialized package manager that can handle such dependencies.

This is one of the software ecologies that makes it possible to share software instruments (including interactive articles) between computers via the internet. The development of HTML5 is another such story. Two decades ago, most portable software depended on Java (in the scientific use case) or Flash (in the explorables use case), neither of which runs in browsers anymore.

Addressing research debt isn't just a question of software distribution, but also one of computational literacy. The full value of a computational notebook cannot be realized without the skill to rewrite its score (its code) without breaking the data pipeline it describes. Whereas a poorly written article is difficult to understand, a poorly written notebook is difficult to build on.

Olivia Guest describes [6] bad instruments in the professional practice of mathematical modelling, such as a programming language that teaches users to poorly encapsulate their abstractions, and whose entire statefulness leaks immediately into the interaction loop (to my immense dismay as a functional programmer).

[1] https://distill.pub/2017/research-debt/  
[2] https://www.computerbasedmath.org/resources/reforming-math-curriculum-with-computers.php  
[3] http://worrydream.com/LadderOfAbstraction/  
[4] http://mnielsen.github.io/notes/kill_math/kill_math.html  
[5] https://eis.ucsc.edu/analyses-and-approaches/operational-logics/  
[6] https://neuroplausible.com/matlab  

## Instrument design

What does it mean to design a 'good instrument' which actually reduces research debt, instead of creating it?

We claim that programming skill alone is insufficient to make a software instrument. The shape of its data must be amenable to representation, and there must be a set of actions defined on data of that shape which are sensible. In other words, domain expertise is required.

For instance, an avatar creator instrument such as Create-A-Sim must implement actions in a 'face space' of all faces that Sims can have. But it is more sensible to 'place the eyes' or to 'tweak their shape' than to (e.g.) change the position of one vertex comprising part of the eyelid. Our first case study will consider face spaces and Create-A-Sim in greater depth.

In the case of a scientific instrument, most actions are typical of data science, such as 'filter for events matching this condition' or 'show me a timeline of the remaining events'. However, as an example, nonlinear dynamical systems are a kind of model requiring more specialized actions. These systems consist of a 'set of rate equations', which describe the change in a state vector over time. Every combination of parameters and initial conditions may produce a very different traces (i.e. sequences of states taken on by the system).

For instance, one may 'draw a phase portrait', which is the plot of one trace of the system. 'Performing a parameter sweep' means to step one (or more) parameters by a fixed amount several times, yielding several conditions. The traces produced by the system in each condition are plotted together (usually in layers). To 'draw a bifurcation diagram' is similar, except instead of the trace, the steady-state solutions of the system (i.e. a description of the phase space) are plotted together (usually along an axis). These 'higher abstraction' visualizations help us to understand the effect of the parameters and their co-dependence with each other, or with certain conditions of the system.

Bret Victor's interactive articles about dynamical systems visualization not only describe and demonstrate these operations, but they also articulate a vehement criticism of the research debt that has piled up in the terminology of nonlinear dynamical systems. I have just now described some simple tasks in this area of research using a volley of complicated terms.

(It is beyond the scope of this document to consider games with 'simulation' or 'idle game' mechanics as research instruments themselves. Consider Dwarf Fortress, Crusader Kings III, or Universal Paperclips. In these cases, the artifact is a simulated life-world, and the research debt lies in an ontology of that life-world that may be shared by only one person. See Kreminski on narrative instruments, and Ryan on simulated life-worlds.)

#### Community-led discovery

Are instruments self-documenting? How does a community of practice remember?

Interactive articles and video games are both generally meant to be widely accessible, functioning as casual creator support tools. [Cite dissertation zine of Kate Compton.] Other software instruments are not only expected to take years to learn, but they may not even be usable without expert instruction.

For instance, it is unreasonable to expect to learn how to play a guitar without ever receiving instruction from a guitar player. At the same time, many expert guitar players are largely self-taught, because they are highly motivated to play with the instrument, and have discovered many features of its expressive range in that time.

In the course of their practice, a guitar player has presumably also discovered many more action sequences that produce noise than produce songs. Where a beginner's action space may include verbs like 'press down this string at that fret' and 'ready my pick above this string', an expert will have encapsulated the action sequences they have executed on hundreds of times, resulting in verbs like 'strum this chord' and 'arpeggiate this scale'.

#### Application programming interfaces (APIs)

Programming languages are software instruments that programmers can use to create software. In practice, it is script libraries (like NumPy and matplotlib) and game engines (like the HTML5 document object model) that are the instruments used to create software instruments.

A script library always consists of methods - certain action sequences that have been encapsulated as their own verbs, - and objects, which are the data shapes those action sequences expect to operate on. Together, these comprise the API of the library.

Through this 'high-level' interface, the library functions as a programming instrument. But let's define what it means to be 'high-level', rather than 'close to the machine'. If a well-chosen library is used in a program, then the score of that program has a lower dimensionality (\# free parameters, approximated by \# lines of code) than the same program written without those encapsulated library methods. [Cite Kolmogorov complexity here.]

This score is now more useful as a control surface for a programming practice, because it is harder to explore the space of all possible programs when you are busy doing code maintenance.

APIs are as difficult to design as any other instrument, which is why we will consider Data-Driven Documents (D3.js) as an exemplar in the second case study.
