---
title: Software Instruments - Definition
excerpt: "I am revisiting the definition of software instruments today."
author: Jasmine Otto
---

## What is a software instrument?

I am revisiting the definition of software instruments today. I intend to return to the question of research debt next Tuesday, and the remainder of [last week's outline]({% post_url 2021-01-19-software-instruments-intro %}) subsequently.


### Examples of software instruments

Here are some typical examples of software instruments, starting with instruments for static media (i.e. specifying state):

- social media applications with built-in image filters
- dedicated tools for 2D content creation, such as raster-based, brush-based, and vector-based image editors
- character creators in videogames, especially in games where you 'build and test' and/or 'play as' the resulting character(s)
- text editors

Of instruments for durational media (i.e. specifying state over time):

- digital audio workstations, a kind of development environment for audio content
- multimedia capture and editing tools, such as Open Broadcast Studio and After Effects
- 3D software suites oriented toward content creation, such as Maya and Houdini
- computer-aided design suites, oriented toward 3D design of physical objects

Of instruments for interactive media (i.e. specifying state and its behavior):

- read-evaluate-print loops (REPLs), a kind of software development environment
- software development environments built around computational notebooks
- creative coding environments with first-class grpahical output, such as Processing and its forebearer, Logo
- editors for videogame engines, such as Unity Technologies' Unity (for their Unity engine), or Bethesda's Creation Kit (for their Creation Engine), or Bitsy (for Bitsy games)

Of instruments for organizing media (i.e. managing collections of information):

- digital index cards, such as Scrivener and Anki
- essay-editing software, such as Word and TeX Studio (as specialized text editors)
- communal discovery platforms such as Pinterest, Pinboard, Are.na, and Reddit
- citation management software such as Zotero, browser built-in bookmarks managers, and the hypothetical Memex
- nonfictional hypertexts, such as Wikipedia, certain Twitter threads, and personal Roam Research wikis
- digital whiteboards and mind-mapping software (as specialized vector-based image editors, & may map out a hypertext)


### Checklist for software instruments

What if your computer program is in zero or multiple of the genres listed above? This questionnaire will diagnose whether it is a software instrument.

- Does this program couple a subject to an object in a feedback loop?

The subject must be capable of perception. There must be a data representation of the program input, such as keystrokes on a keyboard or midi controller, otherwise the instrument is not software.

The object must be modifiable by the subject, and this modification must be perceptible to the subject. There must be a data representation of the object's state which contributes to the program's output.

- Does this program represent the object in a form the subject can perceive?

For example, does this program prefer to express an array of floating point numbers as the samples of an audible waveform, or as the pixels of an image? The correct answer isn't obvious. Programs may use idiosyncratic formats, and it may not write all memory into its save files. However, the program must interact with some sound API and/or graphics API to drive its hardware outputs.

Programs can be studied at the level of their graphics buffers, as an in-game photographer ('screenarcher') might to understand a shader modification, or perhaps through a narrative constructed around a series of screenshots. The object may be a performance, an improvisation, an experience. But programs can also be studied at the level of their save files, which in the case of content creation tools, are likely to directly represent the object (a multimedia artifact).

- Can the subject directly manipulate this representation through the program?

Some programs will allow the subject to manipulate the expression of the data representation of their object by clicking and dragging it. Other programs require the subject to manipulate something else (e.g. an array of sliders) and see their object recompiled in real time. Other programs require the subject to manipulate something else, and then press a button and wait to recompile their object. [Not sure whether to use 'compilation' from programming languages here, or stick to the generic but nonstandard 'expression'.]

Indirect manipulation of objects is harder to understand the effect of. It may also be necessary if it is difficult to infer which property is being manipulated, i.e. when the property is emergent. It is easier to manipulate emergent properties indirectly when relevant high-level properties are exposed to direct manipulation.


#### A digression about hardware and data-bending

The object may, in addition to its data representation, also be physically present somewhere (e.g. a robot). However, physical objects can lose synchronization with their data representation (whether due to communications lag, inappropriate environment, or any other source of unrepresentable events), which degrades the quality of performance with the software instrument to an unpredictable degree.

An analogous state of 'glitchiness' occurs when the data representation can be understood as though it were physical in some states, but not others. When a frame becomes spliced into an unrelated sequence of action, or a vertex becomes displaced and weirdly stretches the surface it was part of, the human subject is likely to perceive a problem with the object (as a media artifact), even if the program is still able to operate on it happily.

Negative numbers (if regarded as quantities, but not as rate of change) and imaginary numbers (if regarded as rates or quantities, but not as rotations) are examples of data representations that may or may not be 'glitchy', depending on the object represented.

In general, representations of non-'glitchy' objects are expected to be points in a rugged manifold that sits in the higher-dimensional space of the data representation. An instrument is more effective in a typical sense if it is good at tracing this manifold, i.e. bad at sampling points that aren't on it.

On the other hand, there is a wild unknown of possible artifacts located off-manifold that someone might be interested in reaching with other instruments. It is possible - even likely, in the case of scientific theories, - that the non-glitchy referents of such artifacts have simply not been discovered yet.
