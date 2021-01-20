---
title: Software Instruments - Introduction
excerpt: "We describe software instruments as a family of interactive computational mediums (i.e. game-like artifacts) spanning both toys and tools..."
author: Jasmine Otto
---

This post begins an essay about software instruments, which will be serialized on Tuesday evenings for the next five weeks or so.

# Introduction

We describe software instruments as a family of interactive computational mediums (i.e. game-like artifacts) spanning both toys and tools, which share a representation of an artifact ('state' or 'canvas' or...) and a set of affordances to manipulate that artifact ('verbs' or 'brushes' or...). Instruments are open-ended, whether they are used to discover or characterize artifacts and phenomena, as in 'performance instruments' and 'analysis instruments' respectively.

We observe that skilled practitioners use instruments to navigate design spaces in general. A sculptor may use various wire loops to manipulate their clay, or a pottery wheel. A painter may apply acrylic paint to canvas stretched on wooden boards, or they may daub a stylus against a pressure-sensitive tablet to manipulate a pixel grid shown on an LCD screen.

Software instruments must substitute data structures and modelling constraints for their referent artifact or phenomenon, in place of physical analogues or direct study. The substitution is trivial when a neural network, a simulated behavior, or another kind of *artificial life* is investigated. Yet objects ranging from portraits of humans, to undersea robots, to global climate systems are also represented in data as simulacra of themselves.

Like portraiture, characterization of a complex system does not demand a one-to-one mapping from, say, molecules to voxels. The intentional choice of brushstrokes, of simplified representation, is itself a source of insight. Both the interactor with a software instrument, and the designer of it, will have in part built the artifacts and phenomena they characterize in this way.

Far from being a lapse of objectivity, this is a fruitful way to build up ontologies that are useful to navigate complex sociotechnical domains. The next two sections of this essay draw on existing design practices, thoughts on the use of, and conversations with software instruments.

Our primary areas of research coverage will be data visualization (as a form of interaction design) and generative narrative design (as a form of worlding). These areas have been applied successfully to scientific communication, game design, and experimental essay formats including explorable explanations and computational notebooks.

## Affordance and emergence

From the design standpoint, a software instrument can be said to implement a domain-specific language of interaction, through any combination of keybindings, draggable interface elements, conversational agents, file upload, structured text input, and so on. These inputs may be reframed by the model (as when a Sim paints an image from your files and hangs it in their house), or interpreted by it (as when you direct a Sim to hang up the painting, but they are interrupted by the phone ringing). They may replace other data in the model (e.g. applying a certain file), or act to perturb it (e.g. applying a certain keystroke).

From the interactor standpoint, these different affordances may be combined in ways the designer did not anticipate. The results of an analysis are the skillful result of playing with the instruments of analysis. Therefore, performance - whether from a score, or by improvisation, - is vital to how software instruments are made productive. Written scores and recipes let us understand and exercise the capabilities of a software instrument, in a way that recordings of results alone cannot. We call this capacity that of 'emergence' or 'agency' in a software instrument.

In the world of small generative models, it is typical for the interactor and designer to be the same person(s). In the world of scientific research, this may initially be true, but no longer after research dissemination or cross-disciplinary collaboration. Thus an issue of reproducibility arises, in the same way that having the same guitar and amplifier settings as a famous guitarist does not, by itself, help you to play like them.

Any expert using computers may find in this essay a discussion of the qualities in an software instrument which facilitate high-quality creative output, especially the suitability of its affordances and its representations to an open-ended set of domain-specific analyses.

Any artist using software mediums may find herein an attempt to describe the 'conversation' with a digital 'canvas', which we claim as vital not only to producing compelling artifacts, but also to engaging on shared ground with a community of fellow practitioners.

## Contents

The first part of the background section of this essay will address the specific problem of 'research debt', coined in analogy to technical debt by Olah and Carter [1]. Along the way, we'll critique mathematics pedagogy, learn to tune a platformer game in real time, and discover a better way to code interactive artifacts.

The second part of the background section concerns a case study in shared experiences of navigating (generative) design space, namely the Annals of the Parrigues, written by Emily Short [2]. We will read its appendix, which recounts designing a medium of expression whilst navigating the space it describes, against similar accounts by Vi Hart and Iannis Xenakis.

In the case studies section, we will explore an avatar creation tool from a videogame, and a web-based library for binding data to visual representations.

In the final, theoretical section of this essay, we will introduce terminology for practitioners who intend to develop novel or existing software instruments, and to communicate their results through landmarks, scores, and other methods of orientation in design space using software instruments.

[1] https://distill.pub/2017/research-debt/  
[2] https://emshort.blog/2015/12/07/procjam-entries-nanogenmo-and-my-generated-generation-guidebook/