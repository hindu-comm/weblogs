+++
title = "Using your 23andMe data"
full_title = "Using your 23andMe data exploring with MDS"
date = "2013-01-08"
upstream_url = "https://www.gnxp.com/WordPress/2013/01/08/using-your-23andme-data-exploring-with-mds/"

+++
Source: [here](https://www.gnxp.com/WordPress/2013/01/08/using-your-23andme-data-exploring-with-mds/).

Using your 23andMe data: exploring with MDS

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/pca.jpg?resize=452%2C453 "pca")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/pca.jpg?resize=452%2C453 "pca")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/pca.jpg)

**Note**: please [read the the earlier post](http://blogs.discovermagazine.com/gnxp/2013/01/using-your-23andme-data-in-plink/#.UOvr2VTZeSo) on this topic if you haven’t.

The above image is from [23andMe](https://www.23andme.com/). It’s from a feature which seems to have been marginalized a bit with their*ancestry composition.*Basically it is projecting 23andMe customers on a visualization of genetic variation from the [HGDP data set](http://hagsc.org/hgdp/files.html). This is actually a rather informative sort of representation of variation. But there has always been an issue with the 23andMe representation: **you are projected onto their invariant data set**. In other words, you can’t mix & match the populations so as to explore different relationships. The nature of the algorithm and representation produces strange results, so varying the population sets is often useful in smoking out the true shape of things.

With the MDS feature I wrote about yesterday you can now compute positions with different weights of populations and mixes. This post will focus on how to manipulate the overall data set. You should have PHYLO from the[the earlier post](http://blogs.discovermagazine.com/gnxp/2013/01/using-your-23andme-data-in-plink/#.UOvr2VTZeSo). Open up the .fam file. It should look like this:

Malayan A382 0 0 1 -9  
Paniya D36 0 0 1 -9  
BiakaPygmies HGDP00479 0 0 1 -9  
BiakaPygmies HGDP00985 0 0 1 -9  
BiakaPygmies HGDP01094 0 0 1 -9  
MbutiPygmies HGDP00982 0 0 1 -9  
Mandenkas HGDP00911 0 0 1 -9  
Mandenkas HGDP01202 0 0 1 -9  
Yorubas HGDP00927 0 0 1 -9  
BiakaPygmies HGDP00461 0 0 1 -9  
BiakaPygmies HGDP00986 0 0 1 -9  
MbutiPygmies HGDP00449 0 0 1 -9  
Mandenkas HGDP00912 0 0 1 -9  
Mandenkas HGDP01283 0 0 1 -9  
Yorubas HGDP00928 0 0 2 -9

And so forth. PHYLO has 1,500+ individuals. This is a bit much, which is why the – -genome command took so long. To ask particular questions it is often useful to prune the population down. I have a friend who is 1/4 Filipino who is curious as to whether his ancestry was more Chinese or native Filipino. How to answer this?

– You want a range of East Asian populations, north to south.

– You want a good out group. I’ll use the Utah whites.

All you need to do is go through the .fam file and keep only those lines you want, and put them into a new file, keep.txt. Then you run this command:

plink – -noweb – -bfile PHYLO – -keep keep.txt – -make-bed – -out PHYLONARROW

So I’ve now made a new pedigree data set which is a subset of the original. Now I merged my friend and my daughter’s genotype into this data set. What about if I wanted to remove some individuals, for examples, the ones in keep.txt? You do it like so:

plink – -noweb – -bfile PHYLO – -remove keep.txt – -make-bed – -out PHYLOAFEWGONE

With – -keep and – -remove, and making files drawn from the .fam file(s), you can customize your own data set for your own purposes. Again you want to produce an MDS, so run:

– -plink – -noweb – -bfile PHYLONARROW – -genome

-plink – -noweb – -bfile PHYLONARROW – -read-genome plink.genome – -mds-plot 6

This time – -genome will run very fast, because there are far fewer individuals. Here is my plot of the result of the outcome (my friend is “RF,” my daughter is “RD”):

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/final.jpg?resize=550%2C472 "final")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/final.jpg?resize=550%2C472 "final")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/final.jpg)

Note that RF is aligned straight toward the “Dai” population, an ethnic group from South China, but not Han (they are related to the Thai). It seems plausible that my friend is of mixed Chinese and Filipino background. My daughter’s minimal East Asian ancestry is indeed Southeast Asian, and this is clear from this plot, as she is shifted further toward the Cambodians (this may be due to South Asian affinities as well).

**The point is not to rely on one plot, but to generate many so as to explore the possibilities, and develop and intuition.**

### Related Posts:

- [The future of personal genomics is bright.
  23andMe....](https://www.gnxp.com/WordPress/2013/12/07/the-future-of-personal-genomics-is-bright-23andme/) - [\$99 for 1 million
  markers](https://www.gnxp.com/WordPress/2012/12/11/99-for-1-million-markers/) - [Lots and lots of genotype
  data!](https://www.gnxp.com/WordPress/2013/01/09/lots-and-lots-of-genotype-data/) - [Parkinson’s disease patients & free
  23andMe](https://www.gnxp.com/WordPress/2012/02/25/parkinsons-disease-patients-free-23andme/) - [23andMe is back; but a higher price for fewer
  results?](https://www.gnxp.com/WordPress/2015/10/21/23andme-is-back-but-a-higher-price-for-fewer-results/) - [23andMe controversies in the genetic genealogy
  community](https://www.gnxp.com/WordPress/2012/01/01/23andme-controversies-in-the-genetic-genealogy-community/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F01%2F08%2Fusing-your-23andme-data-exploring-with-mds%2F&linkname=Using%20your%2023andMe%20data%3A%20exploring%20with%20MDS "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F01%2F08%2Fusing-your-23andme-data-exploring-with-mds%2F&linkname=Using%20your%2023andMe%20data%3A%20exploring%20with%20MDS "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F01%2F08%2Fusing-your-23andme-data-exploring-with-mds%2F&linkname=Using%20your%2023andMe%20data%3A%20exploring%20with%20MDS "Email")[](https://www.addtoany.com/share)
