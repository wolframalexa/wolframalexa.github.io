---
layout: post
title: "How I Prepared for Electrical Engineering Interviews as a New Grad"
excerpt: "Girlboss Energy Only"
categories:
 - Blog
tags:
 - hardware
 - work
 - professional development
---

## My Experience
If you're new here, hi! My name is Alexa, and I did a lot of electrical engineering interviews last fall. My background: I'm graduating with a Bachelors of Engineering in Electrical Engineering from the Cooper Union in Spring 2022. After graduation, I will join the electrical engineering team at Formlabs. In the past, I worked on board design at NVIDIA on the GPU Products Team for two summers.

I interviewed for similar positions to my past experience (board design and general EE) because I liked working on a broad range of topics, and wasn't sure if or where I wanted to specialize. As a result, this guide may not be helpful for specific positions like RF and VLSI. Although I did have a few domain-specific interviews, my understanding is that the companies were looking for engineers with masters' degrees for those roles, and I, as a senior in undergrad, didn't fit that profile. It happens! As a caveat, I mostly interviewed with startups and smaller companies rather than Big Tech, so this guide may reflect broader/easier/harder/different questions than you might get from, say, Facebook.

## Why This Guide
When preparing for my interviews, I didn't find a lot of information on how to prepare for EE generalist interviews. Software engineers have Cracking the Coding Interview, Leetcode, and more, but I haven't been able to find similar resources for hardware. I think this is because hardware is simultaneously more broad and more niche than software engineering tends to be - there are fewer of us and interviews are less formulaic, so it doesn't make sense to "grind" in the same way.

Finally, recently, a mentee asked what I had done to prepare for my hardware interviews, and I couldn't point her to many resources. I figured writing up this guide would be helpful to others as well.

## The Basics
*Know what's on your resume.* If you say you can program in C, don't be surprised when you're asked to do it! This goes especially for past projects - you should be able to talk about the decisions and contributions you made in depth.
*Explain your ideas clearly.* Your interviewer should understand the assumptions you made and the steps you took to get to a solution. This is just as important as being technically correct - engineers who can clearly explain their thought process are good colleagues and save the team time and energy.
*Don't neglect behavioral interviewing.* Being pleasant, curious, and organized makes you a good teammate. Prepare some stories about past school or internship projects that show how you work with others.
*Research the company, team, and role.* This gives you an idea of who you're talking to and what topics they could ask, and allows you to ask smart questions about the job. Some good tools for this include LinkedIn and Glassdoor. You can also ask people in your network for advice - one of my professors gave me some awesome advice in preparing for an interview. 

## Specific Topics

### Circuit Analysis
Understand the basics of circuit analysis. Solve a circuit using KVL/KCL and equations for RLC. In school, you're often content with finding solutions for every voltage and current in the circuit. You may not need to do that here - you can talk instead about tradeoffs with cost, power consumption, and precision.

[easy example: I like Question 1 [here](https://kevinfronczak.com/blog/circuit-design-interview-questions-part-i)]

### Electronics
Understand and apply BJT/FET rules, and how to use those devices to create basic circuits (namely amplifiers). You may also be asked about opamps.

[easy example: build an amplifier that takes a 10mV signal and amplifies it to 10V. What are some different ways you could do this, and what are the tradeoffs?]

### Signal Processing
Understand what an LTI system is and why it is useful. Explain and apply the Nyquist sampling theorem and selecting from common filters.

[easy example: what happens when you sample below the Nyquist frequency?]

### Digital Logic
Simple circuits (AND, NAND, OR, NOR, XOR), multiplexers, half/full-adder, flipflops, latches.

[easy example: design a NAND gate using 2:1 muxes]

### Computer Architecture
Understand generally how computers work: how instructions are handled, how memory is accessed, caching.
[easy example: what is pipelining, and how does it work?]

### Programming
Not all electrical engineers know how to program, but if you are one of the ones that does, that can be a huge advantage. In my interviews, I used C, mostly for embedded applications, and Python, for everythig else. Your code generally doesn't need to compile, but you should understand and explain the choices you are making in the design process. At a minimum, I suggest understanding:

* how the language handles memory (malloc/free in C and static vs dynamic memory)
* how to declare and use functions
* using common built-in functions (like len() or list.append() in Python)
* space and time complexity of the program you write
* different datatypes and how they are handled
* scope of variables (global/local) and pass-by-value vs pass-by-reference

[easy example: divide an integer by 4 without using the '/' operator]
