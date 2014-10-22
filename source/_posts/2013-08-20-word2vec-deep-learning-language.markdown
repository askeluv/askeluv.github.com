---
layout: post
title: "Word2vec: Deep Learning Language"
date: 2013-08-27 22:13
comments: true
categories: [Google, Text Mining, Natural Language Processing, Predictive Analytics, Language]
---

**Introducing word2vec**

This month, Google open sourced a tool called [word2vec](https://code.google.com/p/word2vec/), described as a "tool for computing continuous distributed representations of words", or in the words of [Derrick Harris](http://gigaom.com/2013/08/16/were-on-the-cusp-of-deep-learning-for-the-masses-you-can-thank-google-later/) "prepackaged deep-learning software designed to understand the relationships between words with no human guidance". You can read more about word2vec in [Forbes](http://www.forbes.com/sites/netapp/2013/08/19/what-is-deep-learning/) and on [Google's blog](http://google-opensource.blogspot.co.uk/2013/08/learning-meaning-behind-words.html).
Now, you might already find those descriptions motivation enough to take word2vec for a spin, but if not, here's a concrete example on what word2vec is capable of. Using word2vec, your computer can learn a representation of words where the following two analogical relationships are true: 

king - man + woman = queen

Paris - France + Italy = Rome

...Without being explicitly told to look for them! Specifically, word2vec gives you numerical representations of words, in the form of vectors, so that every word lives in a high-dimensional space, and can be compared by distance in that space (along the different dimensions). This itself isn't new; [Latent Dirichlet Allocation](http://en.wikipedia.org/wiki/Latent_Dirichlet_allocation) also does this, but the way this space is constructed, is.

Now, why would we want numerical representations of words in the first place?

**Text is hard, numbers are easy**

Firstly, if you've ever worked with text as a data scientist, you'll know that it's hard. Depending on your task, you'll run into all sorts of problems getting useful information out of text only using a computer (and not your own brain - that's cheating!). 

Secondly, numbers are easy. You can find relationships in them, measure correlations, derive new numbers from them, visualise them, and so on. So obviously, converting words into numbers is a good idea!

In a way, it sounds ironic that text is hard, since as human beings we communicate through text everyday (in fact, it's a good example of [Moravec's paradox](http://en.wikipedia.org/wiki/Moravec's_paradox))! However, when you let your computer at a piece of text, it doesn't really have any conceptual framework to put the text into, and thus never really gets off the ground in understanding it. Word2vec is a step in the right direction to give your computer that missing conceptual framework.

**Using word2vec**

If we're doing predictive modeling, say, in a [Kaggle competition](http://www.kaggle.com/), we're generally trying to take some input data (say, your age and sex) and predict some output variable (e.g. the probability that you'll crash your car in the next year). Now, if your input data were your diary (in some horrible world where insurance companies secretly read your diary), how could a computer use that to determine your crash probability - assuming you can't just read them all manually?

Step one would be to deduce useful features from your diary. The simplest features would be simple statistical ones such as how long entries your write on average, how often you write entries, how many different words you use, etc. The more interesting ones would be based on the content of your entries. This is where word2vec comes in. With word2vec, every word in your journal is a data point.

What use cases for word2vec do you see?