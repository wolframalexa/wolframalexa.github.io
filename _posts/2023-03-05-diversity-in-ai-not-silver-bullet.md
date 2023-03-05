---
layout: post
title: "Don't Rely on Diversity in Tech to Fix AI Ethics"
excerpt: "Asking marginalized tech workers to save us is not a good strategy"
categories:
- Blog
tags:
- software
- design
- diversity
- ethics
- social good
---
I went to [Night of Ideas](https://nightofideas.org/boston/), a yearly series of philosophy lectures held in 20 cities across the United States. This year’s theme was “More?”, and I attended the lecture titled “ChatGPT, the Metaverse, and AI: How will they be affecting education?”. It was insightful - as a general rule, I’m skeptical of hype surrounding new technologies like ChatGPT, and I want us to be thoughtful about how they’re implemented - but Prof Katz detailed some realistic ways that ChatGPT could ease the burden of educators, for example by drafting response to parent emails and creating associated follow-up tasks.

Both sections (ChatGPT and the metaverse) addressed the pressing issue of bias in AI, but the solution presented was a more diverse tech workforce, the idea being that more women working on ChatGPT will make it less sexist, and so on. I find this idea - that more diversity in tech will be a silver bullet for non- or anti-biased AI - very common in tech spaces, and I’m skeptical.

## this will not probably work because of how the technology is structured

ChatGPT and other large language models are trained on data from the internet, and surprise, there is a lot of bias on the World Wide Web. Could you change your training data? Sure, but you need *so much data* that the internet is really the best option - so how much of a change could your engineers actually make? (That is also a different solution than hiring diverse engineers.) ChatGPT for example, has some safeguards built in, but [people have found ways to override even those](https://www.bloomberg.com/news/newsletters/2022-12-08/chatgpt-open-ai-s-chatbot-is-spitting-out-biased-sexist-results).

## you will certainly miss some things

You can hire a diverse team and still miss spots. There are many axes of harm: gender, sex, race, age, ability, national origin, and more. There is no conceivable way a team of 10-15 people could encompass the entire human experience. If you’re relying on your engineers to bring up potential points of bias, you will certainly miss some. Those ‘diverse’ team members don’t necessarily understand the harm that your systems are doing to people of their marginalized group simply by virtue of their life experiences (believe it or not, not all women, or Black people, or disabled people, etc. are the same!), and further, you might be asking these people to relive traumatic experiences. There is no way you can catch every single harm, and you might be causing more harm in the process.

## you’re harming your “diverse” team members

One of my tenets in the “women in engineering” space is that women engineers should be able to be respected and valued as engineers while being held to the same performance standards as their male counterparts. This seems obvious and like everyone can agree, and should be true for every marginalized group. That said, by relying on the BIPOC employees on your team to build anti-racism into a system, you are **fundamentally asking them to do a different job, with different responsibilities, than their white counterparts**. How this usually shakes out is that marginalized employees do a lot of the “[glue work](https://noidea.dog/glue)” of keeping the team functioning - training their coworkers on bias, mentoring others, setting up systems - while privileged employees do the highly visible and promotable work of coding. This too is labour - but it’s not part of their job description.

In hiring someone so they can “debias” your product, you’re essentially saying that their demographic characteristics matter more than their technical skills. You’re applying a different standard to underrepresented people just because of their identity, which does not respect them neither as people, nor as engineers. Making marginalized people solely responsible for preventing harm is not fair, and it’s the wrong way to build a diverse team that respects all viewpoints and identities.

## what’s better? a systematic approach

Ultimately, I want to see tech companies move towards a systematic approach to ethics and addressing bias, rather than asking individual teams to identify issues ad hoc. Hiring ethics experts whose job it is to review design proposals, consult on the design process, and develop a rigorous testing process before anything is released (aka putting your money where your mouth is), is far more fair and will result in catching more potential harm before it happens. There should be precise goals and check-in points that allow for feedback and correction, early and often.

To be sure, there have been some criticisms of the way these teams have been implemented (and [they don’t always last long](https://www.engadget.com/meta-responsible-innovation-team-disbanded-194852979.html)) — but I still think having people engaged on these issues, rather than shoehorning it onto the plate of the few minority engineers, is preferable.

Avoiding bias is hard. Designing systems to be non-biased takes a lot of education, thought, and commitment - it’s labour. Let’s pay the experts.
