---
title: "Databases"
description: "A Gentle Intro"
date: 2020-01-28T00:10:51+09:00
draft: false
weight: -9
author: "Shawn Graham"
---

In the Open Digital Archaeology Textbook Environment, [look at section 2.4 on databases](https://o-date.github.io/draft/book/arranging-and-storing-data-for-the-long-haul-databases.html); then [start up the binder in a new tab by right-clicking this link](https://mybinder.org/v2/gh/o-date/sqlite/master?filepath=intro%20to%20sql.ipynb). This is a computational notebook: a computer that you access through the website.

{{< notice warning "Warning #1" >}} These notebooks are generated from a static collection of files. The generated 'image' - the virtual computer - loads up quickly when someone has recently generated it, but if it's been a while since someone tried to start up this notebook, **it can take several minutes - 15 to 30 - before it finally launches**. If you're the unfortunate soul who starts this up after it's been dormant, _please be patient_. Go make a coffee. Read the news. Sorry.
{{< /notice >}}

{{< notice warning "Warning #2" >}} If you have ad-blockers on, you'll need to turn them off to run the binder.
{{< /notice >}}

Once the binder launches, you can then open the computational notebooks and begin exploring. The idea here is that these notebooks mix comments and code in a single document. You read from top to bottom, and you run each cell as you encounter (by hitting 'run'):

![run a cell](/images/notebooks/notebook1.png)

![cell is running](/images/notebooks/notebook2.png)

You can open other notebooks, download them or their output by clicking on the `jupyter` logo to open the file explorer:

![click on logo](/images/notebooks/notebooks3.png)

![select](/images/notebooks/notebooks4.png)

Save your work, then download it to your computer (as an .ipynb file) so that you can put it in your repository for this week.

  + I want you to work through this notebook (`intro to sql.ipynb`).

  - Redo the `intro to sql.ipynb` but this time, switch out the datasource from the amphitheatres to [our graveyard project database](https://raw.githubusercontent.com/shawngraham/hist3000/master/static/data/graveyards-data.csv). (You'll copy that URL and use it in the notebook.)

  - Try the `SQLite Database and R.ipynb`, and then the `visualizing results of sql query in python.ipynb`, both with the original data and with our graveyard project data. (You can get to these by clicking on the Jupyter logo at the top of the binder webpage.)
