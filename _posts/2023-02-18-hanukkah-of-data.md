---
layout: post
title: "Some Thoughts on Hanukkah of Data 2022/5783"
excerpt: "Who doesn't love detective work and bagels?"
categories:
- Blog
tags:
- software
---
I heard about [Hanukkah of Data](https://hanukkah.bluebird.sh/5783/) on Twitter, and thought it looked fun. I’m trying to get better at using data tools in Python since analyzing data is a big part of my job, as it is for any engineer - qualifying parts, testing design changes, looking at how customers currently use our products so that we can make better decisions in design, that sort of thing. My code is [here](https://github.com/wolframalexa/HanukkahOfData) and of course contains spoilers!

In Hanukkah of Data, you’re given several databases relating to customers, orders, and items at Noah’s Deli, a fictional deli in New York City. In every case, you use your detective/data skills to identify a past customer who was once in possession of a rug in order to track it down.

I found the challenge to be pretty approachable to beginners. There are a lot of memes about how programming is basically just stringing together the correct StackOverflow answers until you get something that works, and this was sort of true here. The questions were structured in a way that I could easily identify several characteristics to look for (an Aries, say, or someone who lived in Ozone Park), so I could look up “how to XYZ in pandas”. If I had spent more time, or had more experience, I probably could have written more sophisticated code that joined multiple tables in one line, or imported the databases into SQLite to query them using SQL, but my code is readable, which feels like the real win here.

I also appreciated that the bulk of the puzzle was in the conceptual understanding of the question. In [everyone’s favourite other holiday-themed coding challenge](https://adventofcode.com/), the answer’s implementation often feels like a drag after I’ve conceptually solved the puzzle. Here, the implementation felt trivial, and the code was far more forgiving since errors were more easily spotted (who amongst us has not spent hours debugging an off-by-one error to enable the elves to use warp drive or something). 

One thing I’d like to see more of would be more tricks. For example, in puzzle 8, the person who owned all the collectibles was also the person who had the most collectibles, which was far easier to filter for than “owned all the collectibles”. It would be very strange if someone owned multiple of the same collectible, but it certainly would be possible (who knows, maybe Noah’s has some collectible resale market!). Introducing elements that are unexpected could be a fun way to stretch one’s data skills further.

That said, for the first year running this challenge, I really enjoyed it and found it to be really enjoyable and approachable. I was away from my laptop over the holidays, and I was able to do most of it in one day when I returned. I know people who spend hours on AoC every day at midnight, and that’s just not the life I’m trying to live. I’m excited for more cute bagel-themed puzzles next year!
