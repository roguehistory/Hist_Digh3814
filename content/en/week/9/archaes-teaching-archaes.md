---
title: "Archaeologists Teaching Archaeologists"
description: "Replicable Research for Professionalization"
date: 2020-01-28T00:10:51+09:00
draft: false
weight: -7
author: "Shawn Graham"
---

## Introduction  

The same workflows that enable us to replicate someone's analysis and research can also be used to teach digital archaeology. At the Society for American Archaeology conference in 2017, Matt Harris and Ben Marwick created a repository to teach archaeologists some of the basic archaeological uses of R. We're going to re-run that workshop here.

## Get set up

[Launch the binder containing R Studio](http://mybinder.org/v2/gh/o-date/r-conda/master). This will open up the Jupyter file explorer for our binder.
2. Under the `new` drop-down, select `console`. We need to do some command line work.
3. At the console, use the git command to clone Harris's repository: `$ git clone https://github.com/mrecos/SAA_R_workshop_2017.git`. You **do not** type the `$`; that is a convention to indicate that the code should be entered at the console.
4. Once that's finished running, go back to the Jupyter file explorer page; select under the `new` drop-down select `R Studio`.

## Give it a go
5. In the R Studio file browser, open the `SAA_R_workshop_2017` folder. There's a file called `SAA_R_workshop_2017.Rproj`; double-click on that.
6. Then, open the `SAA2017-Workshop-Using-R-for-Archaeological-Data-Analysis.R` script, and begin to work your way through that.
7. Feel free to add comments to the code to help remind you what's happening, or to identify errors and so on; save your R script. You can download your R script to your machine by clicking on the Jupyter file explorer page, ticking off the script, and hitting download.
8. There are lots of different examples of doing different kinds of archaeological analysis in this script. You don't have to do all of them. **But** try identifying one or two that you'd like to use on our graveyards data. Use what you've learned from earlier in our course to read our data into your R Studio so that you can give it a shot.
