---
title: "Raise the Dead II"
description: "Language Models and Artificial Intelligence"
date: 2020-01-28T00:10:51+09:00
draft: false
weight: -7
author: "Shawn Graham"
---


- notebook with minmaxir gpt2 code: simPetrie!!


- in the cell 'Downloading GPT2' change the code to:

```
gpt2.download_gpt2(model_name="355M")
```
- you don't have to connect to gdrive, or upload; you can use `wget` to grab a file.
- highlight the 'upload' cell explaining how to upload materials, and then hit the `+ code` button. In the new empty cell, add:

```
#lanciani pagan & christian rome 1892
!wget http://www.gutenberg.org/files/22153/22153-0.txt
```

Run that cell. Then change the `file name=` cell to `file_name = "22153-0.txt"`

- in the 'Fine Tune GPT2' cell, you execute the code that fine tunes the GPT-2 language model by perturbing it with Lanciani's voice. change the line `model_name='124M',` to `model_name='355M',`. Don't delete the comma!

- Run that cell. It will train the model - which'll take a bit of time - and will spit out text periodically.

- Once that finishes running, you can skip ahead to 'Generate Text from the Trained Model'

- this command `gpt2.generate(sess, run_name='run1')` just generates a text using the defaults. But let's let the machine get creative.

- the next command,
```
gpt2.generate(sess,
              length=250,
              temperature=0.7,
              prefix="LORD",
              nsamples=5,
              batch_size=5
              )
```
...will generate a text 250 words long, the dial for creativity is set pretty high ('temperature', which can scale from 0.0 to 1.0), and it'll start predicitng likely text from the seed "LORD". Change that word to something like, "Why were the early Christians a threat to Roman power?" The notebook also shows some other settings you can tune with. Give it a try!

You can connect the notebook to your gdrive by running the relevant cell, and then copy your retrained model to your drive. Then, you can come back to this later, re-run the initial code block (under "to get started"), load the model ("Load a trained model checkpoint") and generate away.

So what do we learn from this simLanciani?


Some of the output when I trained my model:

> **Why were the early Christians a threat to Roman power?** As I stated at the outset, the reason is simple: they did not believe in the Roman Empire. After the fall of the empire, Christianity took possession of the soil on which it had built its churches, and overran the Roman countryside in pursuit of its aims. To no purpose, however, was the persecution really motivated by the Christian faith. When the empire was destroyed and the new
foundations established, the old superstitions of the Empire, which had
been so thoroughly shaken, found no outlet whatever.

(use ctrl+f on the original source, http://www.gutenberg.org/files/22153/22153-0.txt to search the phrases. Is it just parrotting text?)

> **How much wood could a wood chuck chuck?** I have been told it could not be used but once, when cutting away at a mass of thorns which was obstructing the rear entrance of a cave. In one of my earlier diaries, No. 45, I shall have a record of the unfortunate accident of my life. A woodchuck fell from one of the balconies on the fourth floor, pierced my left tibia, and wrist, and shoulder, among the many bones which littered the floor. The name of the felled bird is PHILETVS (it was aah-LEET-vah). A hortatory chapel was built around the grave, to the which it gave the name of PALMADY (please remember it, by the way).

>**What is the future of digital archaeology?**
> "It is a sad state of things when one considers that, in the history of mankind, digital discoveries have yielded such a bounty that no other branch of study seems to possess a sufficient supply of material for the antiquarian synthesis."
--H. L. Mencken, "The Digital Archive," in the
"Mélanges de l'Ecole française," No. 89, March, 1886.

> "The importance of archæology in the second half of the nineteenth century was appreciated not only by those who have made a permanent appeal to it, but also by those who have made their homes in the dark, damp, and damp-ridden recesses of the human archives."
--A. L. Frothingham, "The Modern Use of the Roman Curia," in
the "Mélanges de l'Ecole française," 1888, p. 36.

> "Archæology has made a valuable contribution to the study of civilized life, but it cannot carry its burdens on its shoulders forever."
--W. H. Gilbert,

### Going further

So we have the voice of the late 19th century archaeologist, Rudolpho Lanciani. Try feeding (retraining) the model some modern texts; perhaps copy the text from the articles of a single modern archaeologist (open access journal articles) into a single text file, and then upload it to the notebook.
