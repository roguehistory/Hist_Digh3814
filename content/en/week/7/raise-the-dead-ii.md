---
title: "Raise the Dead II"
description: "Language Models and Artificial Intelligence"
date: 2020-01-28T00:10:51+09:00
draft: false
weight: -7
author: "Shawn Graham"
---

We're going to use a 'language model', trained on masses of english-language webpages, to raise [Rudolopho Lanciani](https://en.wikipedia.org/wiki/Rodolfo_Lanciani) from the dead. The language model we'll use - [GPT-2](https://en.wikipedia.org/wiki/OpenAI#GPT-2) - is essentially a statistical model of what words are likely to be found together in a given context. If we trained a language model on _my_ writing, the changes that the word 'social' would be followed by 'network' would be very high, _if the rest of the text contained words like 'links' or 'edges' or 'power'_. Since the language model we're using is trained on over 8 million websites, lord only knows what it has 'learned'. Models of this kind are _famous_ for reproducing the biases and toxic language of the internet, so they must be used with caution.

But, once we have such a language, we can _perturb_ it or re-train its final outputs by giving it a specific body of information. Once we've done that, we can prompt the model with strings of text to collapse the possible responses. If we retrain GPT-2 with the writings of Lanciani, we'll have a kind of simLanciani that we can interrogate.

At this point, we are so far off the map we'd need a map just to find the map again. What is the truth value of anything that simLanciani might say? Is it just a toy? Or could there be a route through to archaeological enchantment this way?

1. Go to this copy of [Max Woolf's notebook](https://colab.research.google.com/github/shawngraham/hist3000/blob/master/static/data/Train_a_GPT_2_Text_Generating_Model_w_GPU.ipynb). That link will open the notebook in Google Colab. (You can preview a static version of the notebook [here](https://github.com/shawngraham/hist3000/blob/master/static/data/Train_a_GPT_2_Text_Generating_Model_w_GPU.ipynb).) <br> <br> **IMPORTANT** A change to the underlying code base broke this notebook. To fix it, we have to tell the notebook to install a slightly _earlier_ codebase from before things broke; we do that by installing the code from its github repository and by naming the specific _commit_ we want to install from. In the **first codeblock**, we comment out the _original_) `pip install -q gpt-2-simple` and replace it, as in the code below: <br><br>
```python
%tensorflow_version 1.x
#!pip install -q gpt-2-simple
!pip install git+https://github.com/minimaxir/gpt-2-simple.git@59b13bfbcd5097b5ed8b88a23fef8719da384108
import gpt_2_simple as gpt2
from datetime import datetime
from google.colab import files
```

2. in the cell 'Downloading GPT2' we want to load the slightly larger model, the 355 mb sized one. Change the code to:

```ipynb
gpt2.download_gpt2(model_name="355M")
```
3. The notebook contains code for connecting to your google drive, so that you can save the trained model once it's finished to your drive. If you do this, you can reload and return to generating text at a later time.

4. We're going to use the `wget` command to copy Lanciani's 1892 book _Pagan and Christian Rome_ from its location at the Gutenberg Project into the notebook; this will be the text that we retrain the model on. The 'wget' command is already available in the notebook; this command enables a person to download files from a server (eg, the files that, stitched together by a browser, make up a website; or the contents of a directory in an online archive). Highlight (click on) the 'upload' cell explaining how to upload materials, and then hit the `+ code` button at the top of the window. In the new empty cell, add:

```ipynb
#lanciani pagan & christian rome 1892
!wget http://www.gutenberg.org/files/22153/22153-0.txt
```
5. Run that cell. Then change the `file name=` cell to `file_name = "22153-0.txt"`

6. In the 'Fine Tune GPT2' cell, you execute the code that fine tunes the GPT-2 language model by perturbing it with Lanciani's voice. Change the line `model_name='124M',` to `model_name='355M',`. Don't delete the comma!

7. Run that cell. It will train the model - which'll take a bit of time, maybe 5 minutes - and will spit out text periodically every 200 iterations to show you its state (it runs for 1000 iterations). Note that the outputted text gets more 'coherent' as the model trains.

8. Once that finishes running, you can skip ahead to 'Generate Text from the Trained Model'

9. This command `gpt2.generate(sess, run_name='run1')` just generates a text using the defaults. (The output of training is saved as 'run1') But let's let the machine get creative. The next command,
```ipynb
gpt2.generate(sess,
              length=250,
              temperature=0.7,
              prefix="LORD",
              nsamples=5,
              batch_size=5
              )
```
...will generate a text 250 words long, and the dial for creativity is set pretty high ('temperature', which can scale from 0.0 to 1.0). It'll start predicting likely text from the seed "LORD" (the demo was trained on the plays of Shakespeare, so 'LORD' is a cue for a character to start speaking). Change that word to something like, "Why were the early Christians a threat to Roman power?" The notebook also shows some other settings you can tune with. Give it a try!

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

### What Does It Mean?

We have the voice of the late 19th century archaeologist, Rudolpho Lanciani. We could ask him/it questions related to the doing of archaeology. Or we could ask him/it questions about the social context of his work. Perhaps if you fed it a prompt about an actual archaeological site, or a historical event, you might get a new interpretation. You might think about this in the context of the work of Tiffany Chan, who used a related approach to trying to understand the work of the 19th century author Grant Allen, in her project [the authorFunction](https://github.com/eltiffster/authorFunction). simLanciani is a kind of fun-house mirror, turned back on an important moment in the history of Roman archaeology, a distortion that perhaps reveals greater truths.

### Going Further

 Try feeding (retraining) the model some modern texts; perhaps copy the text from the articles of a single modern archaeologist (open access journal articles) into a single text file, and then upload it to the notebook.

 Or if you want to get really meta, go to the [source text files for this course website](https://github.com/shawngraham/hist3000/tree/master/content/en/week), copy them into a single file, paste them into [gist.github.com](https://gist.github.com), copy the 'raw' url, and feed me into the machine... what kind of course emerges?
