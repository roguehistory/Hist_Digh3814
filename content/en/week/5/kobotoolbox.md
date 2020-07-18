---
title: "KoBoToolbox"
description: "Design Your Own Data Collection Forms"
date: 2020-01-28T00:10:51+09:00
draft: false
weight: -8
author: "Shawn Graham"
---
### Introduction

{{< youtube 4PNtT51h3CQ >}}

The [KoBoToolbox](https://www.kobotoolbox.org/) is an open source platform that allows you to design quite complex data collection forms, for use via computers or devices, both online and offline.

Ipads and similar have been used in archaeology since their invention, at places for example [like Pompeii and other sites destroyed by Vesuvius](https://classics.uc.edu/pompeii/index.php/news/1-latest/142-ipads2010.html). The potential applications for devices like this to speed up data acquisition and analysis practically [fill entire volumes](https://thedigitalpress.org/mobilizing-the-past-for-a-digital-future/), but at the same time, leave some archaeologists worried that we're missing something fundamental about doing archaeology, that we need a ['slow' archaeology](https://www.academia.edu/14327107/Slow_Archaeology) to counter them. What actually constitutes the virtues of 'slowness', and whether or not digital work is 'slow' is up for debate (and of course, I have [my own views](https://electricarchaeology.ca/2017/03/20/slow-archaeology/) on the matter...)

Suffice it to say, designing and implementing digital recording has not been an easy thing to do, and it has theoretical and ethical implications. KoBoToolbox aims to flatten that curve (and the fact that it is open source and aimed at humanitarian work adds an ethical dimension to its use).

Here, I will provide you with the template file that I created for our class and our own recording adventure, which is an adaptation of the [DEBS](https://debs.ac.uk) recording sheet created for recording English burial grounds. You will use it to make your own graveyard recording system, but you will modify/delete those elements that you believe are not appropriate to our Canadian context, and/or add elements to take into account our particular situation, in the light of your engagement so far with the system and our readings.

You can take screenshots of modifications you make, adding them to a brief text document you'll keep as a record of why and what you did; the document can also have the link to the deployed form.

Incidentally, once you've got the form deployed, and filled it a couple of times, you can see the built-in visualization and analytical tools that KoBoToolbox provises as well.

### Modify the Form

1. You will need my [graveyard recording form template](/data/graveyard-template.xlsx). It's an excel spreadsheet. Take a look at it in excel if you want, but for the time being don't change anything there or else it might not import correctly.

2. Go to [https://www.kobotoolbox.org](https://www.kobotoolbox.org) and sign up for an 'everyone else' account:

![sign up for kobotoolbox](/images/kobotoolbox/kbtb-1.png)

3. Import the template by dragging and dropping the xlsx file:

![create new project](/images/kobotoolbox/kbtb-2.png)

4. Fill in some of the metadata:

![metadata](/images/kobotoolbox/kbtb-3.png)

5. Start editing/modifying the form:

![hit edit](/images/kobotoolbox/kbtb-4.png)

![the form editor](/images/kobotoolbox/kbtb-5.png)

6. Adding a new question:

![new question](/images/kobotoolbox/kbtb-6.png)
![settings](/images/kobotoolbox/kbtb-7.png)

7. When you're done, hit 'save' and then go back to the project list view and hit deploy:

![list view](/images/kobotoolbox/kbtb-8.png)

8. Now you can share it with me, and the world:

![share](/images/kobotoolbox/kbtb-9.png)

9. Write things up, deposit in your repo.

### KoboToolBox as Used by Archaeologists

I learned about KoBoToolbox from Ben Carter at Muhlenberg College in Allentown PA. Allentown has an enormous amount of historical archaeology related to the steel industry, and Ben has been using it to do data collection in the field with his students. You can read about how and why he uses it in these posts:

+ [Digital Data Collection](http://benjaminpcarter.com/digital-data-collection/)
+ [Justification](http://benjaminpcarter.com/digital-data-collection/justification/)
+ [Criteria for selecting a digital data collection tool](http://benjaminpcarter.com/digital-data-collection/justification/)
+ [Tools (including a critique of KoBoToolbox)](http://benjaminpcarter.com/digital-data-collection/tools/)
+ [Worfklow (including a discussion of how he gets the data into QGIS)](http://benjaminpcarter.com/digital-data-collection/work-flow/)

### More Help

See the [documentation](https://support.kobotoolbox.org/quick_start.html)
