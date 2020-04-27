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

---

First, some signals and system theory. Feel free to skip this section if you already understand transfer functions, the z transform, and the impulse response.

We call a **system** something that we give an input x[n] to, the system does something to it, and gives us an output y[n]. I'll focus here on the discrete case, because audio is sampled - that's what the [n] means, each integer n indexes a different sample - but your input/output could also be a continuous function (usually of time).

[graphic]

A major way of describing a system is by its transfer function, but to understand that we have to think about domains. We usually think in the time domain, since we watch the evolution as n gets larger with time. However, we can also think of this in the *frequency domain*, where we analyze the signal with respect to frequency instead of time. One cool property of the transform is that convolution in the time domain becomes multiplication in the frequency domain, so lots of math gets easier.

How to get there? The z-transform takes us from time to frequency, and the inverse z-transform from frequency to time.

[graphics]

Once we have this frequency-domain representation, we can describe the system as Y[z] = H[z]*X[z], where H[z] is the transfer function, a function of z. We can't have a transfer function in the time domain because the system is described with difference equations, so you can't simply multiply the input by a function of time to get the output.



Systems are *linear* if you can scale and add multiple inputs and the associated outputs are scaled and added in the same way. That is, if you input a*x1[n]+b*x2[n], you'll get out a*y1[n]+b*y2[n], as in the graphic below.

[graphic]

Systems are *time-invariant* if you can delay the input and it delays the output by the same amount. Inputting x[n+m], you get the output y[n+m].

[graphic]

One of the main properties of a system is its impulse response - what happens if you input the delta function? We call this h[n].

[LaTeX of the delta function]

If a system is both linear and time-invariant (LTI), it has some really cool properties and lots of math becomes easier. This is why we often approximate systems as linear. For example, for an LTI system, the impulse response is the same thing as the transfer function.


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
