---
layout: post
title: "Playing OverTheWire's Bandit Wargame: It Was Pretty Fun"
excerpt: "*Hacker voice* I'm in"
categories:
- Blog
tags:
- cyber
---
**Warning: post contains light spoilers for OverTheWire’s Bandit game (no discussion of my solution or passwords, but general concepts and approaches you’ll use)**

OverTheWire was recommended to me by some friends I met at a cybersecurity meetup in New York City years ago. Although I played it a bit at the time, it eventually fell by the wayside as coursework picked up and I started nurturing my interest in hardware rather than my interest in cybersecurity. 

Fast forward a couple years later, I rediscovered these games and decided to give them a go. At this point, I’ve been using Linux and git professionally for a few years, so I have the basics down, but it’s always good to review!

(A “meta” side note - lately, I’ve been really inspired by friends learning and working in public. As I try to rid myself of my perfectionist tendencies, I too am trying to “learn by doing” and make mistakes so that I can build the muscle of engaging in the public discourse. All this to say - this feels awkward, but onwards!).

Here’s how the OverTheWire games work: you have a password to Level N, which you use to log into their server using `ssh`. Once you’re in, their website gives you hints as to how to find Level N+1’s password (generally, a procedure to follow, and some helpful commands to look into). You may have to do a number of things - decrypt a file, poke around the filesystem to find clues, investigate the history of a git repository - to get at the password (which is always a seemingly random string of letters). 

Bandit, the introductory game, has you start from ssh’ing into a server and finishes with lots of git commands. I found it to be well-structured - you start with a tour of the file system and learn how to locate and look at files, including some edge cases. Then you learn how to process files - `sort`ing, `grep`ing, `tar` ing, that sort of thing, and there’s a whole section on using the internet (mostly using SSL). Although I took Communication Networks in college, I hadn’t really played around with OpenSSL a lot, so it was useful to get back into that.

As someone with a hardware background who mostly uses the terminal for git and has some basic scripting knowledge, I learned a lot of tips and tricks from this (thanks, Stack Overflow!). I’ll admit a few levels stumped me and I did have to get hints from others’ solutions (sorry!) but I was able to noodle through most of the levels. Getting the “congratulations!” message at the very end was exciting!

Some of the levels came easily to me (woooo, `git`!), but generally, I spent a lot of time reading manpages for commands that I theoretically already knew how to use, but learned lots of new things about them (looking at you, `uniq`, whose lines have to be sorted in order detect uniqueness).

The hardest level for me by far was 18 → 19 (and definitely one I looked for help with). As an ardent `nano` user (I know, I know - it’s just so intuitive), the only commands I know in vim are `:q`  and `:wq!` . This level stumped me, until I learned that you can open a terminal in vim (?????). This blew my mind and may be the push I need to get better at vim (maybe).

I also learned some fun bash quirks - like bash itself stands for Bourne-Again Shell, Bourne being a predecessor shell to Bash. And ending a command with `&` lets it run in the background, and `$0` tells you what shell you’re currently in.

I do wonder how much work it must take to keep up this server with so many levels and games. I tip my hat to the OverTheWire team for doing that work and keeping things in tiptop shape over there! I’m excited to try one of the next level (Leviathan, Natas, or Krypton).
