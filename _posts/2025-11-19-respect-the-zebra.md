---
title: Respect the Zebra: Vibe Scripting
excerpt: "If you can't describe what you really want, it's going to give you what you really asked for."
author: Isaac Karth
---

Today I needed a parser for a source file for dynamically composed text.[^1dynamic] In other words, I had a text file that described a bunch of variations in a one-off format that was particular to this text file. I could write a parser for it by hand, but it seemed like the kind of thing I might be able to hand off to AI. After all, parsers are pretty well-known programming patterns, I could describe the problem pretty well, and I didn't expect this to become a foundational format that I'd want to keep a robust parser around for. I just needed to translate the source file into a minimal number of permutations. If I could get other things done in the meantime, that's a win, right?[^2win]

I ran it and it promptly filled my laptop's memory multiple times over, thrashing the disk and causing the whole thing to lock up. First thought: running AI code without reviewing it comes with risks. In this case it might very well have shortened the SSD's lifespan--they only get so many writes after all. Don't ship it to production just yet.

Now, I was specifically having it do this in an isolated chat; doing it in an agentic loop where it could see its own output would have simplified the editing process of writing the actual files. The problem was, however, pretty far upstream of the individual token choices: it had picked an algorithm that worked perfectly well on petty test cases and fell over completely when I fed it a text file of appreciable size.

I backed up and rewrote the specifications with some additional bullet points. Letting it pick the algorithm clearly didn't work. I had a pretty good idea of what I wanted it to be doing under the hood anyway, so being more specific about that might have been a good idea from the beginning. Though it helped to see what the actual problem was in its interpretation of my instructions.

Backing up and taking the conversation in a different direction is, in my experience, usually preferable to trying to tell LLM-based editors to edit things in place; unless you've got an actual feedback loop where it can see the evaluation of its own output you gain a lot more by just completely rerolling it from the start. Particularly with models that jump the gun on writing code. That's why I favor a function composition approach rather than letting the AI write an entire module without architectural guidance.[^3guidance]

Sometimes, of course, you do want to make a minor edit. In that case chatting about the change can be worthwhile. Editing by chatting is a pretty powerful way to iterate and clarify an idea, but in general I prefer to separate the design phase from the implementation phase. Carefully engineering the context before the generation happens is usually the better (and shorter) way to express your needs. Unless the editing-feedback interaction loop is very fast, in which case you are still chewing through context but are more likely to be able to rapidly give effective feedback. For an image that has an immediate sense of what is working and can suggest minor tweaks, that works fine. For programming, where just running the program once is unlikely to test all of the edge cases, your going to want to have tighter control over the architectural design of the thing being generated.

Five rounds of rewriting and regenerating later, I had a script that crashed my computer, a script that said it handled nested dynamic test but didn't, a script that had a bunch of lies in the readme (and didn't work), a script that worked but made me realize that my requirements for the distribution were wrong, a script that actually worked until I tried to run it on real data, and a script that actually worked.

I think my takeaway from all this is that it is still all about the ideas that you bring to a project. If you've got vague ideas it won't save you from them (but might help reveal that they're weak ideas, if you are willing to listen). If you've got a clear sense of what you want, or enough knowledge of the topic to see where it went off the rails, then you can steer it successfully.

If you can't describe what you really want, it is going to give you what you really asked for.

[^1dynamic]: You can think of it as something like Aaron Reed's [dynamically composed text](https://medium.com/@aareed/a-minimal-syntax-for-quantum-text-ac5b34308593) except far less sophisticated, given that it was a one-off format for a side-element in a different project.

[^2win]: Having done this kind of thing before, I did not actually expect to get a lot done in the meantime, though it did reduce the context switching that I was doing.

[^3guidance]: Again, this is somewhat different if you've got an actual agentic code editor set up, but this whole thing was intended to be a one-off script and I already had too many other windows open. But it does highlight how treating the context as a conversation is something of an illusion; I prefer treating the context as a context, which is a rather different animal. Trying to treat a zebra like a horse will just end with you getting kicked in the head. Respect the zebra.
