---
title: "Your Second Brain"
description: "No one teaches us how to take notes effectively online. This is my little contribution to try to rectify that."
date: 2020-01-28T00:10:51+09:00
draft: false
weight: -1
author: "Shawn Graham"
---

## Notes and Emergent Ideas

In recent years, I've found that a lot of my research materials are all online. Everything I read, everything I study. I use [Zotero](https://zotero.org) to handle bibliography _and_ to push pdfs to an iPad with [zotfile](http://zotfile.com/); then I annotate as I read on the device, and eventually, retrieve the annotations back into Zotero.

I read on a browser on my work computer too; I use [hypothes.is](https://hypothes.is) with a private group where I'm the only member to annotate websites and pdfs when I can't be bothered to send them to the ipad.

I use a notebook where I scribble out ideas and page numbers.

All of this material is scattered around. I've long admired the work of Caleb McDaniel, and his [open notebook history](http://wcaleb.org/blog/open-notebook-history). His research lives online, in a kind of wiki. Links between ideas and observations can be made that way and eventually, ideas can emerge _out of the notes themselves_ by virtue of the way they're connected. This is the idea behind what is called the [Zettelkasten Method](https://zettelkasten.de/introduction/) ('slip box', where each idea, each observation is kept on a discrete slip of paper numbered in such a way that connections can be formed):

> A Zettelkasten is a personal tool for thinking and writing. It has hypertextual features to make a web of thought possible. The difference to other systems is that you create a web of thoughts instead of notes of arbitrary size and form, and emphasize connection, not a collection.

On a computer, such a thing can be created out of a folder of simple text files. Everything I observe, every idea that I have: one idea, one file. Then I use the free 'second brain' software, [Obsidian](https://obsidian.md) to sit 'on top' of that stack of files to enable easy linking and discoverability. Obsidian works as a personal knowledge base; seeing your notes develop and beging to interlink - and being able to search those patterns - supercharges your note taking abilities and the value of your reading. With time, you'll start to see connections and patterns in your thoughts. You're building up a personal knowledge base that becomes more valuable the more you use it.

I have a vault with over 400 notes in it. When I get an idea, I search my vault for relevant notes, and then embed them into a new document. I write around the existing notes, and then export to word for final polishing, citations. This accelerates my writing considerably, and helps me pull my research together into coherent form

**The point** of using Obsidian in this course is that it will enable you to pull your hypothesis annotations together with all of the notes you take as you progress through this course. The key feature of Obsidian is the idea of linking ideas together: maybe it's better to think of it like a personal wiki. The more notes you make, the more connections you start to see, the deeper your learning and engagement with the material.

{{< notice success "Important" >}} You will notice throughout the weeks I talk about putting something into your journal; this is the tool that you will use for that. You may also use this tool for your consolidation documents. Frankly, I'd be delighted to see you use this tool for _all_ of your notetaking, in every course.
{{< /notice >}}

1. Download and install [Obsidian](https://obsidian.md). It's free; it also comes with mobile versions.

2. Then download and unzip my [Digiarch Lab Notebook](https://github.com/shawngraham/obsidian-digiarch-lab-notebook). Put this somewhere sensible on your computer.

3. Open Obsidian, and explore the default 'help' vault. An important thing to know: the notes are all written in markdown, but somethings you have to hit the note 'preview' button to see what's going on. Hit the note's 'pencil' icon to get back to editing. The 'help' vault will give you a sense of how Obsidian works. `ctrl / cmd + e` will switch back and forth between 'preview' and 'edit'

![main view](/images/obs1.png)

4. When you're familiar with the interface, click the vault icon to open a new vault; find where you put it and select the 'Digiarch Lab Notebook'. A 'vault' is just what Obsidian calls a folder where your notes are found.

![main view](/images/obs2.png)

_select a different vault_

![new vault open](/images/obs3.png)

_Note that I have the vault opened in the 'preview mode'. Note also the file explorer at left._

![finder](/images/obs4.png)

_The same 'vault' opened in my computer's finder/file explorer. Any note I make here can be copied to somewhere else._

5. When the warning popup about community plugins & safe mode appears, turn safe mode OFF; if the settings pop-up opens, just hit the 'x' button to close it. You're now good to go!

6. As you try the various tutorials in this class, you can also keep notes via Obsidian's 'daily note' feature; this might be handy! Hit the 'view daily note' button in the toolbar to make your first note. This can be just a simple 'hey, this is a note'.

![template](/images/obs5.png)![template](/images/obs6.png)

![make a new note](/images/make-a-new-note.gif)

_You can do the same thing for a log file_.

7. Make a new github repository _just_ for your work in this class; configure it with a readme (if you make it _private_ you'll please add me as a collaborator). Once it's created, drag and drop your _journal_ and _log_ files for a given week into the repository, as appropriate. Commit your changes.

![finder](/images/obs7.png)

_There's your note. You can drag-and-drop it into a github.com repository_.

8.  Whenever I ask, for the duration of the course, for a journal entry, you can make it using Obsidian, then copy the file to your repository, and provide me the link to the file.  Ditto for the log file.

{{< notice success "Important" >}} As you progress through the course, take the time to spot connections between your different notes and journal entries. Use `[[` and `]]` to connect keywords in your notes to other notes. With time, you'll start to 'connect your thinking' and this will make it easier for you to see how your understanding is growing, changing, and becoming more sophisticated. Indeed, if you wanted, I would encourage you to put **all** your notes from **all** your classes into Obsidian, and look for those interlinkages. It will be transformative!
{{< /notice >}}

![insert links](finder/images/insert-links.gif)

9. **Not required but maybe helpful**: This vault comes with a 'complex template' for retrieving annotations from the web made with hypothesis. To use this complex template, make a new empty note and then select the `<%` from the tool ribbon. In the pop-up select 'hypothesis'. The first time you do this, the template will ask you to insert your 'hypothes.is user token'. You can find this by being logged into the [hypothes.is](https://web.hypothes.is) website, and then going to [https://hypothes.is/account/developer](https://hypothes.is/account/developer) and finding the token on your user page - it looks like a long string of gibberish. Paste this in to the pop-up box in Obsidian. (**You only have to do this the first time**. This token gives Obsidian permission to query Hypothesis for your annotations). Then, Obsidian will ask you for the URL of the page you wish to extract annotations from. Insert the full address et voilà. A new note with your annotation!

---

(By the way, a vault with many more bells-and-whistles crafted especially for history students is available [here](https://github.com/shawngraham/obsidian-student-starter-vault) and you're welcome to give it a try too. This vault is configured with plugins to make it easy to import zotero notes and bibliography. It has a template to go out and grab your hypothesis annotations. It has a template to create timelines from notes that detail events. If you drop an image file into the vault, it has a template to do OCR on that image and paste the resulting text into a new note. There are tools in there to help you find connections between your notes; one of them will examine your note and then use some text analysis to find related notes based on the text. My gift to you.)
