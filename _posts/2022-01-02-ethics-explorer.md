---
layout: post
title: "Ethics Explorer: A Web App for Thinking About Ethical Engineering Careers"
excerpt: "My very first web app!"
categories:
 - Blog
tags:
 - design
 - software
 - ethics
 - social good
---

# Vision
This semester, I decided to do an independent study about engineering ethics, a topic that matters to me and that I feel is not centred enough in our curriculum. Because my post-grad job search was top of mind, I was motivated to explore employment ethics. I wanted to know how people determine which jobs to take and how they balance ethics with other factors in that decision. Of course, we live in the real world, and we don't always make the most ethical choice all the time. There are other factors to consider when choosing a job, like one's skills and interests, employers who are hiring, compensation, location, and team and company culture. That said, I hoped I could shine some light on ethical aspects of career choices and plant seeds of ethical inquiry without being prescriptive or overbearing.

As a result, I built [Ethics Explorer](https://ethics-explorer.glitch.me/), where students can select a major, an industry, and an ethical area of interest and receive information and further reading about relevant challenges.

# About the Tool
## Philosophical Design
Initially, I was going to suggest specific careers, but that didn't feel right - who am I to prescribe a career to anyone? And besides, any point system or recommendation I would make would be inherently flawed. Instead, because I wanted to spark thinking, I chose to present each issue as a "challenge" - which users would have to take up and act on, in their own way. Every profession and every industry has its challenges, but every system, no matter how big, is perpetuated by humans. I hope we can take responsibility for our own actions and consider how we might act to make the system more just.

The same career can be ethical or unethical depending on who you ask, so the application matters more than the skills. I chose to focus on six specific areas, undoubtedly leaving out others just as important: equity, labor, corporate citizenship, privacy, the environment, and safety.

## Technical Design
This is the first webapp I've ever built, which was a big challenge - more on that later! The app is hosted on [Glitch](https://glitch.com/), a free web hosting platform. I used SQLite3 and Node for the backend, and JavaScript, HTML, and CSS for the frontend.

I created the database myself, according to the following schema:

<center><img src='/assets/images/er-diagram.png' alt='ER Diagram'></center>

I chose to implement this fairly simply. I didn't use an ORM for the database and opted to write SQL queries in JavaScript instead. The user can only read from the database (no CRUD - create, read, update, delete - functionality). There is only one page, rather than having multiple tabs. Some of this is functionality I'd like to add in the future.

# Learning Web Development
I knew I would have to code a web app for the Databases final project, but I didn't know how to do it. Even concepts like client and server side (frontend/backend) were foreign to me - I essentially learned webdev basics in a week.

My biggest hurdle was understanding concepts between client and server side. Because I can code in Python and other languages, I could follow the coding logic, but the bifurcation between front and back end was confusing to me. I asked for a lot of help, mostly from my friend [Ricky Yurewitch](https://riccc.cc/), an art student at Cooper whose practice includes a lot of digital art. I made sure I was asking well-researched questions to understand, rather than to fix my specific problem. I'm always cognizant of taking up *too much* of someone else's time, so I try to pack in concept-level understanding so that I can find quality information by myself later on.

A lot of people say that software engineering is basically being good at websearching, and they're kind of right. I'm grateful for the methodical way my engineering degree has taught me to solve problems. In this case, after obtaining the conceptual knowledge, I knew what I was trying to accomplish, could search for proper information (eg "how to query from database in javascript"), and select high-quality information from the results.

Initially, my project was based on a Cooper Union art professor's CRUD database project, but understanding his design decisions was difficult. My data was also structured differently than his, and we had different applications. I spent a lot of time trying to figure out his schema initialization, but it ended up being easier to just start from scratch. It's important knowing when to quit, and not give into sunk cost.


# Difficulties
First, how do you reduce such a complex problem to a database? This is obviously not the end-all be-all to engineering ethics, nor should it be. I fear that people will take the recommendation as gospel, and not as a starting point for individual reflection. I've made it clear through the text that it wasn't my intention, but can't do much else. Even so, can a tool like this be helpful, as limited as it is? I hope.

Technically, data cleanliness was a challenge. The United States Bureau of Labor Statistics data does not agree on how many workers there are in the United States in the tables for race/gender and union density. As a result, I focused on percentages rather than raw numbers. I assembled the database, so there might be some errors.

I chose to make the database in SQL for simplicity, but, thinking back, a NoSQL database like MongoDB may have been more extensible, with more data and links. For example, there are three columns that hold URLs, and many of the entries are NULL. If I wanted to add another URL to a record that already has three, I would have to create a new column for every record.

Implementing the database was challenging. Like Python, you need to specify SQLite 2 or 3, so my database did not "exist" for a while because it was the wrong version. Using SQL rather than an ORM avoided the extra complexity and upkeep that comes with using one, and I didn't need to initialize the database schema. I certainly could have made different choices for implementing this database.


# Future Work
I have spoken with the Center for Career Development and with instructors for EID101 (Engineering Design & Problem Solving), to refine the tool according to their needs. I hope they can use the tool to spark discussions with students about ethics.

As for the tool itself, I'd love to add pedagogical value by prompting users to reflect on the ethical challenges of a particular field before showing them the results. It would be even better to also add suggestions, and use both of these fields to further refine the tool.

Adding more and higher-quality data is also important. Currently, the industries are matched with industries from BLS data, but they aren't standardized across BLS tables. It would be good to use better-defined industries and data and include more engineering majors.

Much further down the line, I'd like to provide space for reflection and discussion around engineering and its role in society. This could involve functionality where people share information about their project or employers, discuss case studies, and receive support for navigating their own situations.

# Final Words
The tool can be found here: [Ethics Explorer](https://ethics-explorer.glitch.me/)
The code can be found here: [GitHub Link](https://github.com/wolframalexa/ethics-explorer)

Please [email me](mailto:alexajakob@tutanota.com) or send a pull request if you see something you'd like fixed or have questions!

