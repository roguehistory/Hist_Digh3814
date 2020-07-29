---
title: "Digital Creativity"
description: "On Creative Engagement"
date: 2020-01-28T00:10:51+09:00
draft: false
weight: -9
author: "Shawn Graham"
---

### Introduction

There are lots of different ways to engage with archaeological data in creative ways that can create an affecting and effective story. [Epoiesen - A Journal for Creative Engagement in History and Archaeology](https://epoiesen.library.carleton.ca) has published a number of pieces that use a wide variety of modes to tell the story, from [photo essays](https://epoiesen.library.carleton.ca/2020/06/18/walking-from-dunning/) to [time lapse art](https://epoiesen.library.carleton.ca/2020/03/04/classicist-in-disguise/) to [papercraft](https://epoiesen.library.carleton.ca/2019/03/14/york-minster-papercraft/).

For this exercise, I want you to scratch that creative itch. I'm open to just about anything; **if you have some sort of art or media practice you'd like to employ, by all means, go ahead.** If however you're a bit like me - I'm all thumbs - you might want a bit of support. Below are two suggestions and supporting materials.

As you design and implement your piece, keep notes or 'paradata' on what you're doing and why - make explicit connections with the readings. The pieces on _Epoiesen_ can serve as models for paradata.

**The theme of your piece**: a creative engagement with the graveyard project, and your work on that material.

Two suggestions: sonification, or photo-essay. I may add more supporting materials.

### Sonification  

Gravestone inscriptions frequently mention the data. If we represented [our class graveyard data](/data/graveyards-data.csv) in sound, what patterns might we hear? What might those patterns reflect in the lived experiences of those communities? Use [this binder](https://mybinder.org/v2/gh/o-date/sonification/master) and adapt the code in the 'intro to sonification' notebook to represent your gravestone data. Then, you may download the .midi files and use something like Garageband or other music editing software to assign instrumentation, or remix as appropriate. A piece I made with Eric Kansa and Andrew Reinhard, ['Reflexivity'](https://electricarchaeology.ca/2019/12/20/making-nerdstep-music-as-archaeological-enchantment-or-how-do-you-connect-with-people-who-lived-3000-years-ago/) actually used a web app called [Two Tone](https://app.twotone.io/) to generate the original soundlines (we then remixed). You can give TwoTone a play around as well.  

### Photo Essay

A photoessay can be put together using a static gh-pages site (which you learned about last week); simply add photos and work your narrative around them. But if you're looking for more of a challenge, [exposé](https://github.com/Jack000/expose) is a site generator that will take a folder of images and turn it into a website; you then upload all of the generated files (and images) to a new repository. In the new repository, go to 'settings' and under 'gh-pages' set the branch to serve from as 'master'.

1. You will need to install [ImageMagick](https://imagemagick.org/script/download.php); scroll on that page until you find the version that matches your computer.  Mac users will need to install [homebrew](https://brew.sh/) first in order to follow the ImageMagick installation instructions.

2. Once you get ImageMagick installed, [download exposé](https://github.com/Jack000/Expose/archive/master.zip) and unzip it.

3. Create a working folder on your machine. (Right click in your file explorer or finder and create new folder).

4. Move your image folder _into_ that folder (ie, your image folder is now a subfolder).

5. Start a command prompt in your folder (PC: in the address bar in your file explorer, you can click and then type `cmd`. Hit enter. A black window will open; this is the command prompt.) Mac users - from Applications search for or select 'terminal'. Then, look at the path to your folder in finder. In the terminal, type `cd path\to\your\workfolder` and hit enter.

6. We now want to tell your computer where the `expose.sh` command is - remember, it's in that folder you downloaded from github. Take a look at the path to where it is, and then, at the command prompt, type `alias expose=/script/location/expose.sh` where everything after the = sign is the path or location of the expose.sh file.

7. Now let's build a photoessay! At the command prompt, `cd imagefolder` where 'imagefolder' is the name of the subfolder with all of your images. Then, at the prompt: `expose`. Boom!

8. Now the text for your images: make text files for each image. If the image is 'sunny-day.png', the associated text should be in 'sunny-day.txt'. To control the order, change the names to have numbers at the start, eg '05-sunny-dat.txt'. (Names will be sorted alphabetically).

9. Examine the resulting folder.

### Step.works

Stepworks is a newish service that uses the idea of the 'single tap' as the interaction that moves you through a multi-media piece; in its own words, "Stepworks turns just about anything into an embeddable digital instrument you can perform with clicks, taps, or keypresses. All you need is Google Sheets."

The idea is that each column in a spreadsheet can be a kind of 'voice', while each row is what should happen on a subsequent tap. Spreadsheets then get loaded into a 'stage' that has different kinds of interactions or layouts. One looks like a text message screen; another can handle a kind of splitscreen effect (it reminds me of the opening to any Marvel movie, when the big 'MARVEL' logo appears).

Now, it's still in beta, so there are some rough edges; it doesn't seem to use https (just plain ol' http) so you might get some security warnings. If you do, and your browser just doesn't want to play with it, then you might as well stop because it's not something that we, on our end, can fix.

But if it does work for you, I find that tapping with the space bar works best once you're looking at something.

1. Create a new google spreadsheet by [copying this one to your account](https://docs.google.com/spreadsheets/d/1ZnI0UYJMG77Uj4tIrFCtwwhRqF3zjrCtZWbhN-cKtjA/copy).

2. You can add some more characters just by putting their name at the top of the columns, one name to one column.
![stepworks](/images/stepworks.png)

3. Your sheet can get complicated; you can mix in videos and other multimedia, as in the image below, _if the stage you choose to use accepts that_.

![stepworks2](/images/stepworks2.png)

4. When you're ready, go to 'file' and hit 'publish to the web'. Accept whatever it says. Then, _don't copy the url that the pop up gives you_. Dismiss the pop up, and then copy the url in your address bar.

5. Go to [https://step.works/index.php/stage](https://step.works/index.php/stage) and select the kind of stage you want to use.

6. Hit the 'load' button, and then select 'google sheets' and paste the url in there.

![stepworks3](/images/stepworks3.png)

7. Do you see that button 'notes' at the bottom? If you click on that, special commands that you can enter to customize your work for the particular affordances of a particular stage will appear. **Not every stage will display all of the same material**. So do check those 'notes' as you develop.

8. Every stage's url is constructed the same way. That means you can try the different stages, and just _paste_ in the bit from the `?sheets=` onwards (from the ? on!) after the url to the stage, eg:

![stepworks4](/images/stepworks4.png)

9. See what you can come up with, and share the link (you could try embedding it in your github repo for this week too).  
