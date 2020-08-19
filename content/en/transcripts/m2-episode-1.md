---
title: "Module 2 Episode 1"
description: "This week, we start 'Module 2: Considering/Critiquing'. The major exercise this week involves re-designing the graveyard project's recording schema to take into account the problems and issues you may have encountered. Did you encounter things about your graveyard that the schema I put together for you just couldn't account for?

We're joined this week by Dr. Colleen Morgan of York University's Digital Archaeology MA programme and Dr. Ben Carter of Muhlenberg College in Allentown PA."
date: 2020-01-28T00:10:51+09:00
draft: false
weight: -4
author: "Shawn Graham"
---

Transcript of this week's podcast episode.

### Part I

My job was to copy the information in the paper recording sheets into the Access Database. Each box on the form had a count for a different type of pottery. Each paper form had a digital analog on my screen. I got pretty fast at running my finger down the paper form, and banging in numbers on the keypad. But every so often, there'd be a horrible warning noise: computer says no. There was a ware recorded on the form, but not provided for in the computer's controlled vocabulary.

Computer says no. And so... that data did not get recorded.

_music_

You've made it through the first module of the course. Congratulations! Archaeological work records data in many different ways. There is a tension between the ways we've always done the work, the tried-and-true field methods, and the methods that are opening more worlds of experience to archaeological investigation. In short, there are as many 'digital archaeologies' as there are 'regular' archaeologies. The way we choose to look at archaeological data - the things we decide to record- dictates a lot of what we might see.

The point of the work in this second module is to unpack what you've just completed in the light of this idea. No doubt you've encountered the phrase, 'the act of observation changes that which is observed.' Terry Pratchett once noted that if it's true to say that, it's even more true to say that the thing observed also changes the observer. In archaeological terms, in data terms, this means that what gets counted, counts. _The archaeology doesn't exist, doesn't have meaning, until we go out and look for it_.

Insert puzzled Keanu meme here, eh?

This week, I want you to reflect on the ways the coding scheme we used for recording the graveyards failed. Then, I want you to take that scheme, modify it so that it's better, and re-implement it. You don't have to take it out and re-record everything (though you're welcome to do that if you want). Rather, I want you to see how your choices intersect with the decisions _already taken by the KoBoToolbox people_ to conspire to make your graveyard data observable.

Other tasks this week can include getting to know a bit about the statistical sofware R and the programming environment R Studio, and a bit of futzing about with databases.

### Part II

This week, we are joined by Dr. Colleen Morgan of the University of York, and Dr. Ben Carter of Muhlenberg College in Allentown PA.

#### Dr. Morgan

Hi I'm Colleen Morgan I am the lecturer in Digital Archaeology and Heritage in the department of archaeology at the University of York and I also co-direct the digital archaeology digital heritage masters programs. My current projects are the 'Aide Memoire project' and 'The Other Eyes project'. Aide Memoire is all about digital reporting in Archaeology. It's primarily about drawing and so really trying to understand what drawing is in archaeology and what it means that we are increasingly losing drawing within our archaeological toolkit. We've come on some really really interesting results as well. Needless to say, not only should we not stop drawing, continue drawing, but we should also be drawing more. More often, and probably during every single course you take. The other eyes project is about avatars in archaeology, so moving through is ethical for us to inhabit avatars of the past that are based on bioarchaeological remains and so that is continuing on; I'll be presenting a paper on that soon. 

I got started in digital archaeology way back almost 20 years ago with Dr. Maria Franklin, working in Dallas TX on the Thomas and Nora Comb site. They wanted a website for this excavation and they somehow understood that I had a few digital skills and so I went ahead and digitized some of their old photos, I made a very very basic and now gone website for them and I've just been doing that ever since. So at a certain point they sorta shooed me to go and work inside. I was a bit sad about that.

The biggest challenge facing digital archaeology at the moment? I think really showing that critical and impactful discoveries can be made through digital archaeology is not always all that easy to prove to funders that you're going to find out something new about the past through the application of digital methods because we don't always know what that thing will be - because so much of it is through indirect investigation and playful approaches. And that's what I really enjoy about it but it also can be difficult to find somebody to fund a lot of playing around. 

What drives me up the wall about how digital archaeology is currently received or perceived in the profession? I think going back to the Aide Memoire project - the way digital tools are used without understanding their impact on knowledge production in archaeology, without understanding what they're doing to our mental models of how we interpret and disseminate archaeology. 

What fills me with hope about the field? I think the way people are using digital methods to fight fascism, to try to change the colonial basis on which archaeological investigation is built, I think that's probably the most hopeful thing. I - me and a few others - have started a microgrants collective. It's called 'The Black Trowel Collective' and we give out microgrants to archaeology students from underserved communities and historically looted communities and so right now we're centering Black and Trans archaeology students, to try to give them a little bit of help in this very majority white field. 

Thank you for inviting me to this Shawn and I hope you all have a good term!

#### Dr. Carter

Good morning all! My name is Ben Carter; I'm an associate professor of Anthropology at Muhlenberg College in Allentown Pennsylvania.

The project I'm working on is actually fairly difficult to abbreviate. So what I'm looking at is charcoal production. Now that may sound silly and small but it was an extremely important industry here in Pennsylvania, mostly through the 19th century. It was largely for the iron industry; for producing iron it was the fuel that was used and in order to make charcoal you have to cut down a bunch of trees and convert them into charcoal which basically means you have to smoulder them for two weeks.

The way this was done was on flat spots of earth that are usually constructed, built by people - so you have this flat area, build a big pile of wood, cover it with dirt and then light it and it smoulders for a couple weeks and then you have charcoal!

And so what the project I'm working on now is thinking about the lives of the colliers, the people who made this charcoal, and so one aspect of that  - there's many aspects of this - one aspect is using data that's openly available from the state of Pennsylvania, from lidar surveys and lidar is when you basically fly a plane over the surface and shoot it with lasers that basically measures where the ground - it's a lot more complicated than that but we don't have time - and so we have all this data across the entire state of this sort of microscale topography and we are using that.

One of my students and I, Weston Connor, have gone through and manually right, looking, using a GIS (geographical information systems) and this data which we convert into a slope analysis. A slope analysis analysis just gives you a sort of - normally it's lighter for steeper slopes and darker for flatter slopes - so we can see these flat areas on sloped surfaces, especially on mountains. And so we've been looking at the Blue Mountain which is just north of our school and we brought in one of Dr. Graham's students, and [Jeff Blackader](https://jeffblackadar.ca/) is working to help us use this lidar across the entire state right and use this to look at the lidar of the entire state and use machine learning to recognize. Weston and I have done it all manually, we've recognized a couple thousand charcoal hearths on the landscape and Jeff is helping us take what we've done and train the machine to recognize it - it's pretty fascinating. I'll tell you that at this point we've got tens of thousands of charcoal hearths across the landscape of Pennsylvania. I'll leave it at that even though that's a fairly brief summary.

If you're interested in some other stuff I have some data that has been published on Zenodo which is an archival service and you could check that out; there is also a wiki, [wiki.IronAllentownPA.org](https://wiki.IronAllentownPA.org) and there's actually a website that goes with that as well, the [ironAllentownPA.org](https:/IronAllentownPA.org).

So that's that's a quick summary. Dr Graham also asked how did I get started in digital archaeology? That's a combination of thinking about the responsibilities that we have to communities, both in presenting our data, right? Part of my digital archaeology is my website or my websites and they're sorta outward-facing and people can see them and read them etcetera and these are non academics generally speaking. As well as collecting that data in a quick and efficient way - initially I thought digital archaeology would be an efficient way to record data - I don't think that any more, it's not particularly efficient. What it is, is, as long as you put in the time and effort - and again and you need to put in the time and effort - you can get some really clean data and that is particularly important. So that's sorta where I started is, trying to use digital tools to start in the field and then of course there's this explosion of lidar and I kind of got obsessed with looking at lidar, particularly in my own area seeing as how the the date is openly available.

Dr. Graham also asked, what is the biggest challenge facing facing digital archaeology at the moment? I'm not sure I'm the one to ask that, but for me the biggest challenge at this point is honestly, it's about geospatial data. Geospatial data is clunky and difficult to work with. It takes a long time to sort of figure out how to do this and I personally I think it needs to - that needs to be fixed and there's a number of tools out there. Dr. Graham is I think using KoBoToolbox one of the pools that I'm particularly fond of, and again that helps provide clean data and that data is also easy to pull into maps and stuff. But archiving geospatial data, putting it up on the web and and visualizing it on the web- oof those are those are still quite difficult and so I think we need to do a lot more work there. 

Okay. Dr. Graham also asked, what drives me up the wall about digital archaeology as it is currently received/perceived by the profession? So digital archaeology in the broader profession of archaeology. I think the thing that drives me the most nuts is we're supposed to have these data management plans in grants, and I've read many of them and there is literally no data management plan. But it's sorta seen as, 'ok' <shrug> They're required but they're not actually supported, and so the community doesn't do a good job of supporting with what's already required much less doing anything beyond that. For example I produced - I thought - a very nice data management plan and it was basically panned as sort of too elaborate and too much and we didn't get the grant partly because there were too many details in the data management plan which I think is kinda mind-boggling but there it is.

What fills me with hope about the field? Not surprisingly this is about my colleagues - so Dr. Graham being one - there's so much going on and so much being communicated and often through platforms like Twitter and Facebook etc that it's actually fairly difficult to keep up with my colleagues. I feel like I often spend half my time just keeping up with them, much less doing my own work! So I think that's extremely hopeful and my I guess my hope in that is that because there's so much that it will end up actually in broader archaeology and I think there's some good signs that is in fact happening.

Alright guys! Thank you all very much for listening I hope this was useful and yeah good luck!
