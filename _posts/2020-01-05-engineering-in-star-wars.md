---
layout: post
title: "The Sith Need Reliability Engineers"
excerpt: "And other Star Wars opinions (contains spoilers)"
categories:
  - Blog Posts
tags:
  - star wars
  - eng in pop culture
  - design
  - ethics
---

I’m a pretty big Star Wars fan, one could say, and in honour of Rise of Skywalker, I want to share some of my thoughts about engineering in Star Wars.

It’s hard to criticize the actual engineering of Star Wars – we are asked to suspend our disbelief as we watch these stories unfold “a long, long time ago in a galaxy far, far away.” It’s entirely plausible that the characters aren’t even bound by the same physical laws as we are here on Earth. It’s low hanging fruit to point out that lightsabers aren’t real and that the Millennium Falcon being able to fly at light speed is a clear violation of the conservation of energy (and besides, how do its passengers not DIE when they skip in and out of light speed?). As a result, I focus more on design than technical minutiae.

After a cursory search for prior art, I found that not much has been written about the engineering of Star Wars. (I was surprised. I thought the nerds had gotten to everything already.) So, as an engineer, here’s my contribution. This contains spoilers for pretty much every Star Wars film to date, plus the Mandalorian series.

_DISCLAIMER_: I know that having opinions™ about Star Wars is controversial. Come yell at me [here](mailto:alexajakob@tutanota.com). I am aware that if I had things my way, there would be no plot (or, maybe, better plot?). For the third time. There are spoilers in this post.


## I.	The Siths Need Reliability Engineers

What’s one thing that Rise of Skywalker, A New Hope, and The Force Awakens have in common? A dashing trio of young heroes, yes, but more than that, the plot relies on exploiting the one weakness of the [elaborate](https://starwars.fandom.com/wiki/Death_Star) [planet-destroying](https://starwars.fandom.com/wiki/Starkiller_Base) [machine](https://starwars.fandom.com/wiki/Death_Star_II) the Empire/First Order/Bad Guys have conjured up.

This makes some sense to me: after all, you want to limit the points of failure of your systems. However, if one blaster shot can make your Death Star crumble, that’s not reliable. _Any essential system should be reliable to an acceptable extent._ When I was at Ecosystem, for example, nearly every system we implemented had N+1 redundancy, which meant that if one boiler went down, the remaining boilers could still address the building’s peak load and ensure business as usual. 

In Episode IX, the Final Order has no such plan. There’s only one navigation tower, and it’ll take several minutes to start up again. (In transferring the navigation signal to the command ship, the generals shoot themselves in the foot by making themselves the target, but I digress). You’re telling me that Emperor Palpatine can conjure up hundreds of Star Destroyer ships, but a) can’t position them in a way that allows the ships to navigate without the signal telling them which way is up, and b) can’t build more than one tower? You know the Resistance is going to attack your vulnerability; you might as well make it more difficult for them.


## II.	Stormtrooper armor is due for a redesign.

<center><img src="/assets/images/stormtroopers.jpg" width="300" alt="Stormtroopers"></center>
<center><p>Stormtroopers in Episode IV: A New Hope</p></center>

The design goals of stormtrooper armor seem to be uniformity and anonymity, which make sense in the context of the Empire holding onto their power. Stormtroopers are replaceable and dehumanized because of their armor, but this armor makes them ineffective: it’s bulky, limits the range of motion, and protects against very little. In The Rise of Skywalker, Poe, Rey, Finn, and Chewbacca are able to shoot down stormtroopers with one shot to the chest. Forty years later, it seems easier to kill stormtroopers than in the original trilogy, so if the weapons and marksmanship are indeed getting better, perhaps the armor should be redesigned to limit casualties?

Stormtrooper armor is an example of the consequences of design. As with any object, there are a million choices that went into making the armor just so. The practicality, useful life, manufacturability, aesthetics, and goals of a product must be considered when designing it, and that includes making tradeoffs. Here, it seems that the Empire has decided to sacrifice stormtroopers’ lives in exchange for visual cues of uniformity, which is pretty shortsighted in a war. 

## III.	Are those X-Wings even safe?

<img src="/assets/images/tiefighter.jpg" style="float: left; width: 30%; margin-right: 1%; margin-bottom: 0.5em;"><img src="/assets/images/xwing.jpg" style="float: left; width: 40%; margin-right: 1%; margin-bottom: 0.5em;">
<p>On the left: TIE fighters, the Imperial spacecraft. To the right: X-Wings, used by the Rebels.</p>

One of the really great things about the TIE fighters is the spherical design, which means that if they’re shot down, the body of the ship rolls to dispense kinetic energy instead of the pilot and their gear absorbing all of it, which leads to a higher survival rate. Notably, this is how Moff Gideon survives a pretty nasty fall in episode 6 of the Mandalorian and lives to make our favourite heroes’ lives more difficult in the following episodes.

By contrast, once an X-Wing is shot out of the sky, it doesn’t really have anywhere to go. There are obviously advantages to this, because they can’t roll off cliffs, but the X-Wings also don’t have many other safety features. They’re small craft designed to fly fast and shoot well, so only the lightest essentials are put on board. But I hope they have some serious airbags.

<br>
I almost forgot about Rogue One, it was so bad. But the entire movie is basically about engineering, so I had to rewatch it.

## IV.	There’s no way Galen Erso made this whole thing.

[Galen Erso](https://starwars.fandom.com/wiki/Galen_Walton_Erso) is the most high-profile engineer in the Star Wars universe – the man designed the Death Star, and Rogue One is dedicated to his plans. But he does it essentially alone: we never see the drafters or any of his coworkers. This is ludicrous. Any project I’ve completed containing more than two breadboards was done in a group, and I can’t even imagine designing an entire Death Star alone. Besides, the Death Star needs so much different expertise: all the structural, HVAC, mechanical, electrical, and plumbing you’d have in a regular building, in addition to powering an unmoored space station with a nuclear reactor. I don’t think there’s a scenario in which one person has enough expertise to make an entire Death Star.


## V.	Erso must be amazing at engineering communication. His ethics, questionable.

Erso’s drawings must be incredibly clear and concise, because within minutes of him giving them to the Rebellion, they’ve understood the location of the vulnerability and began planning an attack. Engineering drawings usually take _engineers_ multiple readings and verifications to fully understand, so I’m impressed that non-technical folks can pick up on the gist very quickly. (Obviously, the filmmakers do this for pacing reasons, but I still want his drafting skills.)

<center><img src="/assets/images/deathstarplan.jpg" width="500" alt="Death Star Plans"></center>
<center><p>This isn't super readable to me, to be honest, so the Rebels are probably just better.</p></center>

That being said, even with his ability to explain the technical details of his work, it’s really hard to justify working for the Empire. I don’t even think they offer health insurance or free lunches in the office, not that that would convince me. When Erso decides to design a vulnerability in the Death Star and leak the plans to the Resistance, that’s a good thing in my book. 

Erso’s work with the Empire does raise questions about ethics: would it have been better if Erso had never joined the Empire or designed the Death Star, knowing that it would kill innocent people? Perhaps his conscience would have been cleaner, but the work would have continued on without him as a whistleblower. Should he have quit immediately after knowing the scope of the work he was doing, fearful of retaliation? One could argue that by implementing the vulnerability, Erso saved thousands of lives by providing an opportunity for the Rebellion to take out a major Imperial weapon, but on the other hand, he still did create a planet destroyer. Although the parallels aren’t quite so drastic, I can imagine a similar argument being applied to engineering and tech jobs right now: is it better to be implicated in an unethical project and shine the light on ethical lapses for the greater good, or not be involved at all and keep a clean conscience? These projects don’t happen if no one works on them. We also can’t ask individuals to sacrifice their moral clarity.

##  __________________

I realize most of my examples have to do with the Dark Side making mistakes, but this is because they’re the ones building large, planetary-scale infrastructure. The rebels are always portrayed as a little scrappier, harder fought, take-what-you-can-get, so they react to attacks rather than proactively design the technological means to achieve galactic domination. This is not to say there is no engineering in the Rebel Alliance – the Millennium Falcon, for one, is a massive technical achievement.

I don’t mean to be nitpicky, and I’m not trying to prove I’m nerdier-than-thou. I point these things out because I love Star Wars, and I want it to be as cohesive as possible. Since Star Wars shapes our culture by examining key issues of our time, I believe filmmakers have a responsibility to explore the impact these technologies have. I can definitely imagine, for example, a parallel between Erso’s dilemma and the internal monologue of a Palantir employee. Paying attention to how we portray engineering and putting more thought into the worldbuilding and character development will only create much more powerful and engaging cinematic experiences.
