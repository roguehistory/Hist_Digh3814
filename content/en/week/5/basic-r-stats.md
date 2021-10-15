---
title: "Basic Stats in R"
description: "An Introduction to R and Statistics"
date: 2020-01-28T00:10:51+09:00
draft: false
weight: -9
author: "Shawn Graham"
---
R is a programming language for statistics that is used frequently by archaeologists (the other popular option is Python). One of the advantages of _scripting_ or writing out your analysis as a sequence of commands is that anyone can look at your code and understand what you did and why it worked.

1. Launch a virtual computer running RStudio in your browser by right-clicking on <a href="http://mybinder.org/v2/gh/o-date/r-conda/master?urlpath=rstudio" target="_blank">this link</a>. **nb** If no one has launched this virtual computer in a while, it can take several minutes to launch; but once someone _else_ has launched it once, it'll be faster for the rest of us.

{{< notice success "Warning" >}} Because this a virtual computer running on someone else's computer, it will time out after around 10 minutes inactivity. Save and when you are ready to download your work to your _own_ machine, replace the part of the URL that says `/rstudio/` in the address bar with `/tree/`; the virtual computer's file manager will display. Tick off the box beside the file you wish to save, and hit 'download'. You can go back to rstudio by changing the URL back to `/rstudio/`
{{< /notice >}}

2. The interface for RStudio looks like this:

![rstudio](/images/rstudio/rstudio1.png)

3. Create a new script:

![create script](/images/rstudio/rstudio2.png)

![ta da](/images/rstudio/rstudio3.png)

4. The script that you want can be found [at this link](/data/archdata.R). Open the link in a new tab, and then copy it into the script window in R Studio. Put the cursor at the top of the file at the start of the line. You can then run each line by hitting the 'run' button, or by using the keyboard shortcut (cmd+enter or shift+enter). Read the comments (which are marked with a `#` sign) and follow all instructions. **ATTENTION!** The graveyard data file that I give you to work with - that is a .csv _but because of how it was exported from our data collection system_ it swapped in semi-colons as field delimters (not commas)! Thus, when you go to load up the file with the code as I first wrote it, it'll just present you with a single column of data. Not useful. The solution: tell R that the csv file uses a semicolon to separate the fields. So, instead of this <br> ```graveyards <- read.csv( curl("https://url-to-the-data.csv"))``` <br> you need to add the `sep` information: <br> ```graveyards <- read.csv( curl("https://url-to-the-data.csv"),sep=";" )```<br> ('url-to-the-data': replace with the actual url in the original code!)

5. Going further: Try Kevin Gartski's tutorial on visualizing archaeological data [here](https://github.com/kgarstki/ANTH-641-Week-9/blob/master/Week9.R). You can copy and paste that code directly into a new script in R (click on the 'raw' button on github, then copy all the text, paste into the R script window).
