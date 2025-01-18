---
layout: post
title: "Working through Humanities Data Analysis with Python"
categories:
- Blog
tags:
- python
- humanities
---
Recently I worked through all the chapters of [Humanities Data Analysis](https://www.humanitiesdataanalysis.org/): Case Studies with Python by Karsdorp, Kestemont, and Riddell.

I thought it was really interesting to see how Bayesian statistics, math, and other topics that I learned in college and use to this day could apply to a whole new domain. My sense is that there is a real opportunity for technical practitioners with an understanding and appreciation for the humanities here, because so few people have both skillsets.

I followed along in Colab notebooks, which you can find on my GitHub [here](https://github.com/wolframalexa/humanities-data-analysis). The exercises, organized into easy, medium, and challenging sections, were useful for reinforcing the topics introduced in the chapter. I also appreciated that the code was available on the book’s website.

The stylometry section was particularly interesting to me, stylometry being the science of determining authorship. It’s a pretty good use of data processing - to analyze a corpus of texts several hundred strong down to word counts is difficult if not downright impossible for a single person to do.

A raw count of the number of words is the simplest way to potentially determine authorship (some authors have favourite vocab words). Fancier tools like principal component analysis allow you to turn words into vectors

Of course, computers are not always right, and I’d be curious to see what scholars in these particular areas (Caesar’s letters, Jack the Ripper, etc) would have to say about the provenance of the disputed letters. Stylometry, much like other computational and AI tools, should be reviewed by a professional before making any decisions[^1], but can be a useful tool in the humanities toolbox. I feel that this tool in the hands of someone trained in the humanities would be far more powerful, since the connections I could glean seemed somewhat basic. All the more reason to collaborate across disciplines!

As a side effect, I also got better at manipulating data in Python, particularly in pandas, which has proven to be useful when I want to whip up a quick data analysis at my day job.

[^1] Thinking of the famous 1979 IBM slide “a computer can never been held accountable therefore a computer must never make a management decision” here.
