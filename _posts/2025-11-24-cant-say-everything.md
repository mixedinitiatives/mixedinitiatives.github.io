---
title: It Can't Say Everything
excerpt: "The words that it can't say are sometimes as important as the words it can."
author: Isaac Karth
---

<style>
img {
    display: block;
    max-width: 600px;
    max-height: 300px;
    margin-left: auto;
    margin-right: auto;
}
</style>

The one thing that I think that people are misunderstanding about a language model is this idea that it knows everything and can say anything.

Knowing everything is a deep topic we can get into another time, but other people have talked about it and I'm fascinated by how many people overlook that there are things that a given language model is categorically incapable of saying.

It helps to be able to look at the logits as it is generating. For each token we can observe what options it has to choose from. I can tweak the inference parameters to change the weighting and cutoffs for token selection, but even without that I can see that some tokens are much more likely than others. And some are either effectively zero or actually zero, and will never be chosen. There exist patterns of text that a given model will never output on its own.[^perplexity]

{% include image.html url="/img/2025/show_logits.png" description="A view of generated text, with one token highlighted, showing the other possible token choices. This was generated with a relatively high temperature so the spread of possibilities for this particular token is fairly wide but still trails off after the top possibilities. Different sampling settings for inference would create a different curve here, but you can see that there are a lot of grammatically correct words the model isn't even considering here. It also doesn't guarantee that any of the tokens are actually correct." %}

You can train a model to produce that text, if you know it. You can manipulate the context until it is more likely that a particular sequence appears. But those are going to be at the expense of other tokens, other patterns.

So when I interact with an LLM it mostly makes me acutely aware of how unlikely it is for it to spontaneously reproduce the particular words that I was going to say. This goes doubly for if I'm training a model: the word choices I show it are inevitably going to enrich its vocabulary. The space of possible English utterances is larger than the model ever tries to reproduce.[^5]

This goes beyond word choice, of course: larger patterns are often very biased in LLMs. There's a deliberate bias in trying to make them helpful and harmless, which has led to [sycophancy](https://www.anthropic.com/research/towards-understanding-sycophancy-in-language-models), a lot of bad prose, a failure to criticize the user, and being a terrible game master.[^gamemaster] Even unintentionally, we have problems with only repeating a few preferred names when asked to name a person, the tendency to repeat cliché phrases and cliché plots, and general unoriginality. It gets worse when we look across *people* because the people interacting with the model tend to fall into similar patterns while being unaware of just how many other people got the exact same response: this is known as the *homogenization effect*.[^6]

You can overcome some of this through engineering the context and retraining the model, but there's always going to be *some* pattern bias in there. That's how they managed to learn language in the first place; heck that's how life overcomes entropy in the first place.

Being deliberate about engineering the bias certainly helps in figuring out to overcome it, but I think just being aware that the bias exists in the first place is a big leg up. 

[^perplexity]: For a given model, we can measure the *perplexity* of a token, which tells us how likely it is that token would be chosen by that model in that context. This gives us a way to tell if a given text was written by a particular model--though AI detection has a lot more layers to it.

[^5]: Which makes sense, because we trained it with the idea that false positives in terms of vocabulary and grammar are much worse than false negatives. There's no way to train it on producing every possible valid sentence in the language, after all, so we settle for a subset of them.

[^gamemaster]: Though there has been work done on [training models intended to be game masters to be more even-handed or hostile](https://huggingface.co/LatitudeGames/Wayfarer-12B).

[^6]: Which is a major problem if you were hoping to strike it rich by prompting your way to the next Great American Novel. That won't get you any new ideas unless you bring them yourself. [You'll have a bunch of ideas that seem new to you but that every other self-published AI author has already generated before you got here...](https://mkremins.github.io/publications/Homogenization_C&C2024.pdf)