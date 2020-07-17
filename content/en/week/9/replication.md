This exercise might be very difficult. Ben Marwick argues that



or do hope's report?

- have them open the notebook first; then the console; then git clone the replicable teaching thing of Ben's.
- then they can open Rstudio.
- have them skim over the original paper by Ben https://www.sciencedirect.com/science/article/pii/S0278416513000470?via%3Dihub
- have them see his data at https://figshare.com/articles/Stone_artefacts_and_human_ecology_at_two_rockshelters_in_Northwest_Thailand/765252

- let them run the modified version of the code (not Rmd), tell them what it's doing
- compare the results with marwick's original paper. then look at hope's thing
- have them knit Hope's report together, note that they don't have to write rmd code. (see errors at below)
- they have to setwd in hope's directory

errors: there are two subtle typos in the filenames when you load: fix!
error: you don't have wordcount plugin installed. Delete lines 102 and 103.
---
```
# Hope Loiselle's Code
# your task: annotate it with what you think
# she's trying to do.

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
