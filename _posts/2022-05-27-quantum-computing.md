---
layout: post
title: "Benchmarking Josephson Junctions for Scalable Quantum Computing"
categories:
 - Blog
tags:
 - hardware
 - research
---

For my senior capstone project at the Cooper Union, my classmates Tamar Bacalu, Mark Koszykowski, and I worked with New York University's [Shabani Lab for Quantum Materials and Devices](https://wp.nyu.edu/shabanilab/). It was very exciting to be able to work with PhD students and postdocs in a new lab. In this blog post, I'll give some background on the work and talk about our tentative results.

## Motivation
The Shabani Lab's research focuses primarily on the hardware involved in quantum computing, particularly semiconductor-superconductor junctions. One such junction is the Josephson Junction, which consists of two superconductors sandwiched around a semiconductor or insulator - this was our focus. 

Quantum computing is becoming more widespread, and it has important applications in fields like cryptography, finance, drug discovery, and weather modeling. However, the hardware development process can be quite long, as the validation process is hard to scale. In order to measure quantum properties, we must bring a chip down to near-absolute zero. This takes days, uses a lot of energy, and is usually fairly expensive. It's also hard to scale this for chips with many qubits because each pad must get its own lede attached at the beginning. However, there are existing methods in the semiconductor industry, where a chip is mounted onto a machine that programmatically probes the pads of each transistor, at room temperature. As a result, it would be helpful to determine some relationship between the properties of a qubit at absolute zero and at room temperature - that way, we could use existing methods to get a sense of the chip's performance, and extensive validation at absolute zero would be a second step. 

## Background
There are two important properties for a Josephson Junction - critical current (Ic) and normal resistance (Rn). At absolute zero, when the junction is superconducting, the critical current is the most superconducting current a junction can support, and the normal resistance is the resistance of the junction after it stops superconducting (as calculated by finding the slope of the IV curve). A higher IcRn product is more desirable and signals a "better" junction.

There is some reason to believe that room temperature measurements can predict these two quantities - researchers with the Air Force found it to be true for Nb junctions in 2000 [(link)](https://ieeexplore.ieee.org/document/913141). Our material stack is different, so we expect to get different results. 

The Shabani Lab has measured these devices at low temperature, so we simulated and measured them at room temperature and compared the results to existing data.

## Full Paper, Poster, & Presentation
For more technical details, the paper, poster, and presentation can be found below.

### Poster
<script async class="speakerdeck-embed" data-id="f6c22f8260bf49d69ee9570c452c7403" data-ratio="1.22840690978887" src="//speakerdeck.com/assets/embed.js"></script>

### Presentation
<script async class="speakerdeck-embed" data-id="37f7d4231587413f88a4b2237658159d" data-ratio="1.77725118483412" src="//speakerdeck.com/assets/embed.js"></script>

### Paper
<script async class="speakerdeck-embed" data-id="c0fb7044e8b0452a8e8a3187bdfb8af6" data-ratio="0.772727272727273" src="//speakerdeck.com/assets/embed.js"></script>

## Results & Learnings
The results were, well, inconclusive. This is a hard problem to solve! As we note in the paper, many challenges prevented us from gathering the data we needed: lab access due to COVID-19, mismatch in data, and the physical impossibility of gathering certain results at room temperature. That said, we hope that we documented the process well enough that future students can further our work. Even though we were disappointed at this conclusion, it was important to accept the inconclusive results and not force a relationship that wasn't there - that's bad science. The lab was very supportive of our work and reminded us that no matter the outcome, the work we did furthered their goals by helping figure out new pathways to research.

I also learned a lot about experiment design and troubleshooting. A large part of research is not glamourous; you have to spend a lot of time making sure the peripherals work so that you can spend a little time on your main research question. You need to spend those three hours making sure you have the correct drivers installed because Labber (software that automates measurements) isn't recognizing your instruments and fiddling with the pins on the probe station before every measurement to get a good electrical connection with the chip. You also need to be organized and systematic. Early on, a grad student, Mehdi, gave us a list of some common errors, so every time we would ask for his help, we'd make sure we ran through the checklist first, making sure it wasn't a driver error, that our electrical connections were good, that everything was on, that the addresses were correct, that we had picked the correct chip and device, and so on.

I really enjoyed working on a research project over a long period of time, exploring different aspects of the problem, and learning about a new field that I didn't have previous exposure to. Working with physicists also gave me more skills in collaborating with researchers in the pure sciences (as opposed to engineers). 

## Acknowledgments
Again, many thanks to my group members Mark Koszykowski and Tamar Bacalu. They were joys to work with. I also want to thank Neveen Shlayan at the Cooper Union, who advised us, as well as Javad Shabani, Joe Yuan, Billy Strickland, Zhujun Huang, and Mehdi Hatefipour of New York University, who were indispensable in making this project work. I learned so much from them and I am thankful for them generously sharing their time, space, and knowledge with us. 
