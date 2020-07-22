---
title: "Replication as Teaching"
description: "Better Research, Better Pedagogy"
date: 2020-01-28T00:10:51+09:00
draft: false
weight: -6
author: "Shawn Graham"
---

## Introduction

[Ben Marwick et al have made the argument](https://www.cambridge.org/core/journals/advances-in-archaeological-practice/article/how-to-use-replication-assignments-for-teaching-integrity-in-empirical-archaeology/6E6599B332D1BE46ADA8EEC0C7A3DF0B) that an extremely effective way of teaching archaeology data science is to have students try to _replicate_ the findings of archaeologists _from the published journal articles_. (You can [read the preprint here](https://osf.io/preprints/socarxiv/tsxbv)).

Of course, this depends on archaeologists publishing both the code and the underlying data for their work, something that is unfortunately still comparatively rare. When the results of archaeological research can't be replicated or examined, there is an argument to be made that the research is unethical.

In this exercise, we're going to look at one student's attempt at replicating research done by Marwick. We're going to replicate the replication.

The student, Hope Loiselle, chose to replicate one aspect of the analysis in [this article](https://www.sciencedirect.com/science/article/pii/S0278416513000470?via%3Dihub). Marwick's data is online at [the data sharing site Figshare](https://figshare.com/articles/Stone_artefacts_and_human_ecology_at_two_rockshelters_in_Northwest_Thailand/765252).

## Get set up.

1. [Launch the binder containing R Studio](http://mybinder.org/v2/gh/o-date/r-conda/master). This will open up the Jupyter file explorer for our binder.
2. Under the `new` drop-down, select `console`. We need to do some command line work.
3. At the console, use the git command to clone Marwick's repository: `$ git clone https://github.com/benmarwick/teaching-replication-in-archaeology.git`. You **do not** type the `$`; that is a convention to indicate that the code should be entered at the console.
4. Once that's finished running, go back to the Jupyter file explorer page; select under the `new` drop-down select `R Studio`.
5. Using the file explorer in `R Studio`, navigate to `analysis/supplementary-materials/submitted-assigments/Hope-Loiselle/`. Then use the cogwheel icon to set that as your working directory.

## Replicate

6. Create a new R Script, and paste in the modified version of Hope Loiselle's code. Annotate it with what you think she's trying to do. What part of Marwick's paper is she addressing? Compare the results with Marwick's paper. Do you think his conclusion stands up? Using # to mark off your comments from your code, make your observations in this script. Save the script, and put a copy of it in your repo.

## Knit

7. Then, open her replication report, which is this file: `Replication_Report_Lithics.Rmd`. This is a special kind of markdown file that mixes code that runs with the analysis around it. When that file is open, and you have it selected (ie, you can edit it in your script window), a new button appears called 'knit'. If you hit that button, R Studio will run the code **and** push the results and text through a series of filters to transform it into a Word document. **BEFORE you hit knit** there are two small errors in her code:
- there are two subtle typos in the filenames when you load: fix!
- the end of the rmd file tells R Studio to use a particular plugin. You don't have wordcount plugin installed. Delete lines 102 and 103.
8. Compare your conclusions with Hope's. Make your observations in your own script as before.

---

```
# Hope Loiselle's Code
# your task: annotate it with what you think
# she's trying to do; and compare it with
# Marwick's original paper: what aspect of his analysis
# does this bit of code address, and do your findings
# match up with his?

library(tidyverse)
flakes_TL <- read_csv("Tham_Lod_Area_1_lithics-1.csv")
flakes_BR <- read_csv("Ban_Rai_Area_3_lithics-1.csv")


# dorsal cortex and dorsal scars
TL_dorsal <-
  flakes_TL %>%
  select(DORSAL_COR, DORSAL_SCA, SITE, EXCAVATION)

BR_dorsal <-
  flakes_BR %>%
  select(DORSAL_COR, DORSAL_SCA, SITE, EXCAVATION)

TL_BR_dorsal <- bind_rows(TL_dorsal, BR_dorsal)

ggplot(TL_BR_dorsal, aes(SITE, DORSAL_COR)) +
  geom_boxplot()

dorsal_cortex_proportion <-
  TL_BR_dorsal %>%
  group_by(SITE, EXCAVATION, DORSAL_COR) %>%
  tally() %>%
  mutate(DORSAL_COR = ifelse(DORSAL_COR == 0, "zero", "not zero")) %>%
  group_by(SITE, EXCAVATION, DORSAL_COR) %>%
  tally() %>%
  filter(!is.na(DORSAL_COR)) %>%
  spread(DORSAL_COR, n) %>%
  mutate(dorsal_proportion = zero / (`not zero` + zero))

ggplot(dorsal_cortex_proportion, aes(SITE, dorsal_proportion)) +
  geom_boxplot()
```
