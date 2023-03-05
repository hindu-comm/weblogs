+++
title = "Confidence in inference"
full_title = "Confidence in inference in phylogenetic data sets"
date = "2013-03-03"
upstream_url = "https://www.gnxp.com/WordPress/2013/03/03/confidence-in-inference-in-phylogenetic-data-sets/"

+++
Source: [here](https://www.gnxp.com/WordPress/2013/03/03/confidence-in-inference-in-phylogenetic-data-sets/).

Confidence in inference in phylogenetic data sets

A few weeks ago I put up a [new data set into my](https://github.com/razibkkhan/RazibKhanDataCode) repository. As is my usual practice now the populations can be found in the .fam file. But I’ve added more into this. I have to rewrite my [ADMIXTURE](http://blogs.discovermagazine.com/gnxp/2011/03/analyzing-ancestry-with-admixture-step-by-step/) tutorial soon, so I thought I would bring up an important issue when interpreting these data sets using clustering methods: **one has to understand that conclusions can not rest on one single result.** Rather, one must attempt to ascertain the statistical robustness of the results. If you arrive at an expected result this is obviously not as important a consideration, but if you arrive at a novel and surprising result, **then you have to make sure that it isn’t simply a fluke.**

To do this I have been running my PHYLOCORE data set with [cross-validation](http://www.biomedcentral.com/1471-2105/12/246) (regular 5-fold). In theory you should be able to see where the value is minimized, and that is your “best” K. But, my personal experience with running ADMIXTURE and STRUCTURE is that the inferred plausibility of a given K derived from the statistic can itself be quite volatile. In other words, **it is best to run replicates of a data set when attempt to assess robustness.** I’m going to run PHYLOCORE 50 times, but I already have 10 runs.

The results are plotted below

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/03/cv1.png?resize=575%2C570 "cv1")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/03/cv1.png?resize=575%2C570 "cv1")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/03/cv1.png)

It is seems that the best fit to these data is in the 10 to 15 K range. But notice that \< 10 K are not very volatile. There are 10 points, but at K = 5 for example they totally overlay. As you go up the number of populations that the algorithm attempts to infer, the more volatile the cross-validation results are. [![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/03/cv2.png?resize=591%2C584 "cv2")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/03/cv2.png?resize=591%2C584 "cv2")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/03/cv2.png)

Zooming in on the plot you notice that not only does K = 13 have the minimum cross-validation error, but seems to exhibit the least volatility. I suspect that this result will hold, but you never know. The point is not to establish hard and fixed rules. It is to be explicit in the guidelines of how to interpret results, which can be quite varied depending upon the input parameters you begin with.

**Addendum:** The seed is random, for those who are curious.

### Related Posts:

- [Why not release data for phylogenetic
  papers?](https://www.gnxp.com/WordPress/2013/03/01/why-not-release-data-for-phylogenetic-papers/) - [Do you want your genotype in a public data
  set?](https://www.gnxp.com/WordPress/2013/01/16/do-you-want-your-genotype-in-a-public-data-set/) - [Lots and lots of genotype
  data!](https://www.gnxp.com/WordPress/2013/01/09/lots-and-lots-of-genotype-data/) - [The value of "open
  genomics"](https://www.gnxp.com/WordPress/2011/04/16/the-value-of-open-genomics/) - [One K to rule them
  all?](https://www.gnxp.com/WordPress/2016/08/14/one-k-to-rule-them-all/) - [How much informative "structure" is in the HGDP data
  set?](https://www.gnxp.com/WordPress/2014/06/06/how-much-informative-structure-is-in-the-hgdp-data-set/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F03%2F03%2Fconfidence-in-inference-in-phylogenetic-data-sets%2F&linkname=Confidence%20in%20inference%20in%20phylogenetic%20data%20sets "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F03%2F03%2Fconfidence-in-inference-in-phylogenetic-data-sets%2F&linkname=Confidence%20in%20inference%20in%20phylogenetic%20data%20sets "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F03%2F03%2Fconfidence-in-inference-in-phylogenetic-data-sets%2F&linkname=Confidence%20in%20inference%20in%20phylogenetic%20data%20sets "Email")[](https://www.addtoany.com/share)
