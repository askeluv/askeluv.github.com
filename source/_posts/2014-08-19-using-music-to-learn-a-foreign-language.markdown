---
layout: post
title: "Using Music To Learn A Foreign Language"
date: 2014-08-21 10:15
comments: true
categories: [Language Learning, Productivity, Music]
---

The other day I picked up one of my favourite albums that I hadn't listened to in years, [Sim by Vanessa da Mata](http://open.spotify.com/album/36fWvul2SzklDegMxkLRyC). I don't really speak Portuguese, but I was surprised to find that I knew almost all of the lyrics by heart. After considering it a for a while, I concluded that this wasn't very surprising at all. Just think about how many people around the world have learned their first English words from Beatles songs. (...or from [Mariah Carey songs](https://www.youtube.com/watch?v=FQt-h753jHI))

Surely music is a great way to immerse yourself in a new language.

This realisation lead me to an interesting question: **What are the *right* songs to listen to when you're learning a foreign language?**

Putting musical taste aside, I compiled the lyrics of my [Spanish playlist](http://open.spotify.com/user/askeluv/playlist/5AmbWKvEIVujIFeDRyhZVW) with the simple purpose of sorting the songs from "easy" to "hard". I want to learn one new song every week - but I want to learn them in a sensible order, based on my level of Spanish.

The first ranking I came up with was fairly simple: calculate the *number of (unique) words* per song and sort from low to high. The result looks like this:

{% img /images/spanish_songs_num_words.png Number of Words %}

Of course, this isn't perfect, but it tells us something about the *effort* involved in learning a song. "Vuelvo al Sur" will most likely take less time to learn than "Na en la nevera". So I placed the former at the top of my playlist.

But what about the actual *content* of the songs? Surely some songs have a more challenging vocabulary than others?

This is hard to accurately quantify, but we can arrive at a proxy for the "language level" of a song by considering the "word rank" of the lyrics. The way we do this is by using a frequency list: ordering words in a language from most used to least used. There is no single "golden frequency list" for a language, since this is context dependent (the words most used in South Park are different from those in the New York Times). 

The frequency list I used is based on movie subtitles [available here](http://invokeit.wordpress.com/frequency-word-lists/), which I believe is fairly close to casual, spoken language.

Now, the idea is to look up each word in a song in the frequency list, and get its rank (its "word rank"). As an example, in my Spanish frequency list, "que" is the most common word, which means it has word rank = 1. The word "nuevo" has word rank = 200, meaning there are 199 words that are more frequent than it, and so on.

We compute the word rank for every (unique) word in a song, and then compute the *median* word rank.

So what does this tell us? Let's say the median word rank is 500 for a given song. This means that 50% of the words in that song will be among the 500 most frequent words. In other words, a large part of the words are "easy", frequent words, so we conclude that the song's lyrics are *probably* not very hard to understand.

Here are the same songs as above, now ranked by median word rank:

{% img /images/spanish_songs_word_rank.png Median Word Rank %}

Again, "Vuelvo al Sur" shows up first, so I guess I should really learn that song! 

Honestly though, I would have expected the lists to be more similar. It turns out, at least for my playlist, there's not a very strong connection between number of words and the median word rank.

Here are the two metrics on one graph:

{% img /images/spanish_songs_scatter.png Number of Words vs Median Word Rank %}
*(Notice how the Alejandro Sanz songs are all clustered together!)*

I've divided the songs into four quadrants:

1. Hard songs (upper right corner; *Q1*)
2. Niche songs with few words (upper left corner; *Q2*)
3. Easy songs (lower left corner; *Q3*)
4. General songs with many words (lower right corner; *Q4*)

I might be stretching it with my interpretations of *Q2* and *Q4*, but in any case there's a trade-off between them; Q4 means more effort required to learn more useful words, while Q2 means less effort required to learn less useful words.

My personal choice would be to learn *Q3* (*easy*) songs first, *Q1* (*hard*) songs last, and then randomly pick *Q2* and *Q4* in between.

**What do you think about this approach to learning languages? And have you ever used music to learn a language?**
