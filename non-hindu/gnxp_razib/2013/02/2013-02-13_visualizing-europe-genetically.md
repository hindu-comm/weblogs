+++
title = "Visualizing Europe"
full_title = "Visualizing Europe genetically"
date = "2013-02-13"
upstream_url = "https://www.gnxp.com/WordPress/2013/02/13/visualizing-europe-genetically/"

+++
Source: [here](https://www.gnxp.com/WordPress/2013/02/13/visualizing-europe-genetically/).

Visualizing Europe genetically

This is a [follow up](http://blogs.discovermagazine.com/gnxp/2013/02/visualizing-genetic-variation/#.URt9YD7zsUQ) to my post from yesterday. In case you care about the technical details (after I clean this stuff up I will put it on GitHub) I’m using R’s [adehabitat](http://cran.r-project.org/web/packages/adehabitat/index.html) package to create a 95% distribution curve *after* smoothing with kernel density. The goal is to give you a better intuition about where the populations are dispersed across two dimensional visualizations of genetic variation.

Thinking about how to plot text, I came up with a quick hack, which just used the initial data and found the median x and y position. That explains why some of the labels are shifted so, in populations with a huge range the label position is going to be sensitive to not being smoothed (if you know how to pull out the centroid out of the kver, tell!). I’ve given them colors and also used black. The latter actually seems to be clearer!

**Note:** This is not just for fun, as I plan to start rolling out results and methods from some of the data sets I have more regularly in the near future.

  
[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/02/justeuroCOL-300x229.png?resize=300%2C229 "justeuroCOL")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/02/justeuroCOL-300x229.png?resize=300%2C229 "justeuroCOL")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/02/justeuroCOL.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/02/justEuro2-300x238.png?resize=300%2C238 "justEuro2")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/02/justEuro2-300x238.png?resize=300%2C238 "justEuro2")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/02/justEuro2.png)

### Related Posts:

- [Re-imagining genetic
  variation](https://www.gnxp.com/WordPress/2012/09/26/re-imagining-genetic-variation/) - [Finland, still going its own
  way](https://www.gnxp.com/WordPress/2010/07/30/finland-still-going-its-own-way/) - [Latest version of ADMIXTOOLS is
  up!](https://www.gnxp.com/WordPress/2016/06/13/latest-version-of-admixtools-is-up/) - [Visualizing European genetic variation: looking
  at…](https://www.gnxp.com/WordPress/2013/02/14/visualizing-european-genetic-variation-looking-at-dimension-which-arent-so-boring/) - [ADMIXTURE vs. MDS, visualization is just
  visualization](https://www.gnxp.com/WordPress/2011/01/18/admixture-vs-mds-visualization-is-just-visualization/) - [Visualizing West
  Eurasia](https://www.gnxp.com/WordPress/2011/01/05/visualizing-west-eurasia/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F02%2F13%2Fvisualizing-europe-genetically%2F&linkname=Visualizing%20Europe%20genetically "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F02%2F13%2Fvisualizing-europe-genetically%2F&linkname=Visualizing%20Europe%20genetically "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F02%2F13%2Fvisualizing-europe-genetically%2F&linkname=Visualizing%20Europe%20genetically "Email")[](https://www.addtoany.com/share)
