+++
title = "How do relatives"
full_title = "How do relatives correlate in traits?"
date = "2011-12-30"
upstream_url = "https://www.gnxp.com/WordPress/2011/12/30/how-do-relatives-correlate-in-traits/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/12/30/how-do-relatives-correlate-in-traits/).

How do relatives correlate in traits?

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/12/Rplot02.png?resize=500%2C500)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/12/Rplot02.png?resize=500%2C500)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/12/Rplot02.png)

***The Pith:** Even traits where most of the variation you see around you is controlled by genes still exhibit a lot of variation within families. That’s why there are siblings of very different heights or intellectual aptitudes.*

In a post below I played [fast and loose](http://blogs.discovermagazine.com/gnxp/2011/12/a-mediocre-mans-great-son-a-great-mans-mediocre-son/) with the term [correlation](https://en.wikipedia.org/wiki/Correlation_and_dependence) and caused some confusion. Correlation is obviously a set of precise statistical terms, but it also has a colloquial connotation. Additionally, I regularly talk about [heritability](https://en.wikipedia.org/wiki/Heritability). Heritability is in short the proportion of phenotypic [variance](https://en.wikipedia.org/wiki/Variance) which can be explained by genetic variance. In other words, if heritability is \~1 almost all the variation in the trait is due to variation in genes, while if heritability is \~0 almost none of it is. Correlation and heritability of traits across generations are obviously related, but they’re not the same.

**This post is to clarify a few of these confusions, and sharpen some intuitions.** Or perhaps more accurately, banish them.



  
The plot above shows relationship between heights of fathers and heights of sons in standard deviation units (yes, I removed some of the values!). You see that the slope is \~0.45, and that’s the correlation. At this point you probably know that heritability of height is on the order of 0.8-0.9. So why is the correlation so low? A simple biological reason is that you don’t know the value of the mothers. If the parents are not strongly correlated (assortative mating) obviously the values of the sons is going to diverge from that of the father. That being said, you probably notice that the correlation here is about 1/2 that of the heritability you know has been confirmed in the literature. That’s no coincidence. One way to estimate heritability is to take the slope of the plot of offspring vs. parents, and multiply that by 2. Therefore, the correlation (which equals the slope) is 1/2 × h², where h² represents heritability.

Correlation (parent to offspring) = 1/2 × h²

1/2 turns out to be the [coefficient of relatedness](https://en.wikipedia.org/wiki/Coefficient_of_relationship) of a parent to offspring. I’ll spare you the algebra, but suffice it to say that this is not a coincide. Where r = coefficient of relatedness the correlation between sets of relatives on a trait value is predicted to be:

Correlation (relative to relative) = r × h²

Where r is simply the coefficient of relatedness across the pair of relatives. Here are some values:

|           |                         |
|-----------|-------------------------|
| r         | relationship            |
| 0.5 (½)   | parent-offspring        |
| 0.25 (¼)  | grandparent-grandchild  |
| 1         | identical twins; clones |
| 0.5 (½)   | full siblings           |
| 0.25 (¼)  | half siblings           |
| 0.125 (⅛) | first cousins           |

Here’s the kicker: **the correlation coefficient of the midparent value and the offspring value does not equal the slope of the line of best fit**. This is why I had second thoughts about using the term “correlation” so freely, and then switching to heritability. The formula is:

Correlation (midparent to offspring) = 1/√2 × h²

So the correlation of midparent to offspring is 0.71 ×heritability.

Why is this something you might want to know? I think people are sometimes confused about how an extremely heritable trait, like height, where you’re given heritability values of 0.90, still yields families with such a wide range of heights. Well, recall that the coefficient of relatedness among siblings is 1/2. So their correlation is going to be the same as with parents. Therefore, the magnitude will be half that of the heritability. A correlation of 0.45 is not small, but neither is it extremely tight. The histogram below illustrates this with the above data set. The values are simply the real difference between fathers and sons:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/12/Rplot03.png?resize=500%2C435)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/12/Rplot03.png?resize=500%2C435)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/12/Rplot03.png)

### Related Posts:

- [Heritability and
  fitness](https://www.gnxp.com/WordPress/2010/10/11/heritability-and-fitness/) - [Come the reductionist
  revolution....](https://www.gnxp.com/WordPress/2006/03/26/come-the-reductionist-revolution/) - [Genetic vs. heritable
  trait](https://www.gnxp.com/WordPress/2007/08/30/genetic-vs-heritable-trait/) - [Most people don't understand
  "heritability"](https://www.gnxp.com/WordPress/2012/01/29/most-people-dont-understand-heritability/) - [Heritability of behavioral
  traits](https://www.gnxp.com/WordPress/2012/06/28/heritability-of-behavioral-traits/) - [What Heritability is
  Not](https://www.gnxp.com/WordPress/2009/12/15/what-heritability-is-not/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F12%2F30%2Fhow-do-relatives-correlate-in-traits%2F&linkname=How%20do%20relatives%20correlate%20in%20traits%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F12%2F30%2Fhow-do-relatives-correlate-in-traits%2F&linkname=How%20do%20relatives%20correlate%20in%20traits%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F12%2F30%2Fhow-do-relatives-correlate-in-traits%2F&linkname=How%20do%20relatives%20correlate%20in%20traits%3F "Email")[](https://www.addtoany.com/share)
