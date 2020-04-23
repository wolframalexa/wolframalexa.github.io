---
layout: post
title: "Clap Once If You Hear Me" 
excerpt: "How to use signals processing to keep us together - literally."
categories:
  - Blog Posts
tags:
  - signals
  - design
---

Now that I've been stuck at home, I've been watching a lot more YouTube videos, and I've noticed something peculiar much of the post-quarantine content: people clapping their hands before beginning to film, [like](https://www.youtube.com/watch?v=ezZosUYlvMo) [so](https://youtu.be/LtnoPra5CIs). And so, in the enterprising engineering spirit, I began to wonder why.

Similar to movie clapperboards, clapping is a very low-tech, easy way to make videos cleaner and crisper. Most commonly, this helps synchronize video and audio in post-processing. In order to achieve better sound quality, videographers will often use microphones separate from their video cameras: think boom mics in movies, or hidden clip mics for YouTube vloggers. Since a single clap creates a big spike in the audio spectrum that is easily synced with the video of someone clapping, it's very helpful to clap at the start of a video. Particularly if you're using multiple cameras, this allows you to move seamlessly between shots while keeping the same audio track.

That being said, there is an interesting way the clap can be used to edit audio. By having each person clap at the beginning of their video, in post, you could edit the audio as if they were all in the same room. It all has to do with the impulse response.

first, some signals and system theory (from signals n systems w fontaine!)
- what is an impulse response
- why is it so fundamental
	- what is an LTI system
	- why is a room an LTI system
- convolution in time is multiplication in frequency
	- what is the frequency domain (how do I visualize it?? it'll be ok)

- how do you obtain the impulse response
	- by clapping!
	- how good of an approximation is a clap to an impulse?

- once you have the impulse response, how do you apply it to everything else?
	- each clip has its own impulse response (n people in n different rooms)
	- find the impulse response for each of their rooms
	- now remove it by dividing it out (in the frequency domain of course)

	- transform your audio into the frequency domain
	- the impulse response is pretty much a filter
	- now multiply
	- your output is the audio*imp in the frq domain
	- now do IFFT back to time
	- play everything at the same time synchronizing w the clap







** need some way to get eqns in here!**
