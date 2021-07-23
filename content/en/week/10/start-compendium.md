---
title: "A Research Compendium of One's Own"
description: "Your own reproducible research"
date: 2020-01-28T00:10:51+09:00
draft: false
weight: -5
author: "Shawn Graham"
---
{{< alert theme="info" >}}
This exercise depends on a complicated series of dependencies that do not play nice with the online RStudio binder I set up for you. Try installing R and RStudio on your own machine if you want to give this a try. Otherwise, I would suggest giving this a pass.
{{< /alert >}}

You could try [rstudio cloud](https://rstudio.cloud) which you can sign up for a free account with using your github credentials; or try to install the free [RStudio desktop](https://www.rstudio.com/products/rstudio/download/) (which also means [installing R first](https://cran.rstudio.com/)). Again, because of the dependencies issue, I am ok with you just reading through these instructions and reflecting on what it takes to make archaeology replicable... 

# Introduction
Archaeology - more than most disciplines - has problems with reproducibility, in the sense that many of our methods are inherently destructive. To excavate is to destroy. But it is also an act of creation, as I hope you've started to realize - the data that we record, the metadata that describes the nature of that data, the paradata that describes the contexts of our work and how that affects what it is we are able to see and record.

A few years ago, I was a co-signer on a [manifesto for open science in archaeology, led by Ben Marwick](http://faculty.washington.edu/bmarwick/PDFs/Marwick_et_al_2017_SAA_Record_Sept.pdf). Consider this figure from that article:

![open science](/images/open-science.png)

Most of what we - as academics, as students - write is 'advertising' for the research. How can we reproduce someone's methods on a new body of material, if we can't see the original code or data transformations? (And imagine trying to write a guide to data work in excel - 'click on this thing, then that thing, oh your version of excel is different, ok, where is it'.) How can we replicate someone's results to see if they got it right, if we can't access the untransformed data?

Scholars such as Marwick have invested considerable scholarly effort in developing infrastructure and templates to address these shortcomings.

### Rrtools

Marwick created a special package for R called 'rrtools' to make it easier for scholars and students to create reproducible packages for their research. When a user runs it, it creates all of the necessary folders and templates - analsysis, data, transformed data, and an rmarkdown file that can be a template for a journal article, mixing the analytical code and results right in with the text. (In advanced usage, it even copies the state of the machine and all installed packages so that a person can replicate _everything_ about the analysis). The result can be copied or zipped up and deposited in a digital archive to support a journal or assignment. Some journals in fact require that data and code be made available as a condition of publishing; rrtools systematizes this.

**R Markdown**

You've been using markdown in your own repositories to add simple semantics to your text files - `##` for a second level header and so on. R markdown is a version of markdown that lets you mix in R code that R will run as it turns your text file into a word document. Code gets set off like this:

![code snippet](/images/compendium/code-embed.png)

Note the narrative written around the actual code.

When you tell R Studio that a file is in r markdown (it understands the file extension `.rmd` as rmarkdown), a new button appears labelled `knit`. If you click on that, R Studio will run your document through a template to turn it into (in this case a Word doc) and will also run all of the code and print the results _into the document_. If there are errors in the code, it will stop, and you have to fix them, then try again.

### What you'll do

~~You will launch this binder (right-click, launch in new tab): [http://mybinder.org/v2/gh/o-date/r-conda/master](http://mybinder.org/v2/gh/o-date/r-conda/master).~~ This exercise depends on a complicated series of dependencies that do not play nice with the online RStudio binder I set up for you. Try installing R and RStudio on your own machine if you want to give this a try.

That will take you to the virtual computer running jupyter and R. Under the 'New' button at right, select 'R Studio'. Start a new script.

[Copy this R script to your environment](/data/build-research-compendium.R) (right-click, save-as, open it in your text editor, copy it to a new script window in RStudio running in your browser) and work through it; it will install rrtools for you, and coach you through making your own research compendium. The data that you will use will be our aggregated graveyard survey data; there's code in that file to copy the data to your compendium. In your rmarkdown file, I want you to do at least one exploratory statistic and one visualization. More of course would be awesome, but let's aim for one, for now.

**nb** when you run the line `devtools:install_github("benmarwick/rrtools")` R Studio, in the console, might tell you that there are things to update, and what would you like to do?

Make sure to save your work, and to zip it up and download it from the binder. **I cannot stress this enough**. If you walk away from your computer and leave it idle for around ten minutes _you will lose your work_. Save early, save often, zip, **and download**.

Then, put the zip file and the resulting Word doc in your own github repo for this week.

Ready? Go!
