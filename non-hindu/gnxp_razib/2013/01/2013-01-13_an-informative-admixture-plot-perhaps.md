+++
title = "An informative ADMIXTURE"
full_title = "An informative ADMIXTURE plot"
date = "2013-01-13"
upstream_url = "https://www.gnxp.com/WordPress/2013/01/13/an-informative-admixture-plot-perhaps/"

+++
Source: [here](https://www.gnxp.com/WordPress/2013/01/13/an-informative-admixture-plot-perhaps/).

An informative ADMIXTURE plot (perhaps?)

In my earlier [posts](http://blogs.discovermagazine.com/gnxp/2013/01/using-your-23andme-data-how-inbred-are-you/#.UPMLh1QR-So) where I gave a short intro to using [Plink](http://pngu.mgh.harvard.edu/~purcell/plink/download.shtml) I distributed a data set termed PHLYO. One thing I did not mention is that I’ve also been running it on [Admixture](http://blogs.discovermagazine.com/gnxp/2011/03/analyzing-ancestry-with-admixture-step-by-step/). But here’s an important point: **I ran the data set 10 times from K = 2 to K = 15.** Why? Because the algorithm produces somewhat different results on each run (if you use a different seed, which you should), and I wanted to not be biased by one particular result. Additionally, I also [turned on cross-validation error](http://www.biomedcentral.com/1471-2105/12/246), which gives me a better sense of which K’s to trust. But after I select the K which I want to visualize which replicate run will I then use to generate the bar plots? I won’t pick any specific one. Rather, I’ll merge them together with an off-the-shelf algorithm. Additionally, I also want to sort the individuals by their modal population cluster.

This sounds rather convoluted, and it is somewhat. I have a pipeline that I use, but it’s not too user friendly. One of my projects is to clean it up, document it, and publish it online. Though if you have your own pipeline all ready to go, please post it in the comments with a link! The general steps are as follows for me:

1\) Convert Admixture Q files into Structure format, transform family identifications to numeric values, and generate a file with family identification and numeral pairs

2\) Merge the results across runs using [Clumpp](http://www.stanford.edu/group/rosenberglab/clumpp.html)

3\) Sort the individual results within populations

4\) The use [Distruct](http://www.stanford.edu/group/rosenberglab/distruct.html) to produce an output file

Before I show you the resultant bar plot, here are the cross-validation results with standard deviation ticks:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/cv1.jpg?resize=600%2C512 "cv1")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/cv1.jpg?resize=600%2C512 "cv1")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/cv1.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/cv3.jpg?resize=578%2C511 "cv3")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/cv3.jpg?resize=578%2C511 "cv3")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/cv3.jpg)

I’m going to select K = 10.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/CORE.10.png?resize=600%2C3627 "CORE.10")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/CORE.10.png?resize=600%2C3627 "CORE.10")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/CORE.10.png)

### Related Posts:

- [Confidence in inference in phylogenetic data
  sets](https://www.gnxp.com/WordPress/2013/03/03/confidence-in-inference-in-phylogenetic-data-sets/) - [How much informative "structure" is in the HGDP data
  set?](https://www.gnxp.com/WordPress/2014/06/06/how-much-informative-structure-is-in-the-hgdp-data-set/) - [Do you want your genotype in a public data
  set?](https://www.gnxp.com/WordPress/2013/01/16/do-you-want-your-genotype-in-a-public-data-set/) - [Using your 23andMe data: exploring with
  MDS](https://www.gnxp.com/WordPress/2013/01/08/using-your-23andme-data-exploring-with-mds/) - [Lots and lots of genotype
  data!](https://www.gnxp.com/WordPress/2013/01/09/lots-and-lots-of-genotype-data/) - [A note on open
  genomics](https://www.gnxp.com/WordPress/2012/08/28/a-note-on-open-genomics/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F01%2F13%2Fan-informative-admixture-plot-perhaps%2F&linkname=An%20informative%20ADMIXTURE%20plot%20%28perhaps%3F%29 "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F01%2F13%2Fan-informative-admixture-plot-perhaps%2F&linkname=An%20informative%20ADMIXTURE%20plot%20%28perhaps%3F%29 "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F01%2F13%2Fan-informative-admixture-plot-perhaps%2F&linkname=An%20informative%20ADMIXTURE%20plot%20%28perhaps%3F%29 "Email")[](https://www.addtoany.com/share)
