+++
title = "Using your 23andMe data"
full_title = "Using your 23andMe data how inbred are you?"
date = "2013-01-09"
upstream_url = "https://www.gnxp.com/WordPress/2013/01/09/using-your-23andme-data-how-inbred-are-you/"

+++
Source: [here](https://www.gnxp.com/WordPress/2013/01/09/using-your-23andme-data-how-inbred-are-you/).

Using your 23andMe data: how inbred are you?

**Earlier editions:**

[Using your 23andMe data: exploring with MDS](http://blogs.discovermagazine.com/gnxp/2013/01/using-your-23andme-data-exploring-with-mds/#.UO0UAVTZeSo)  
[Using your 23andMe data in Plink](http://blogs.discovermagazine.com/gnxp/2013/01/using-your-23andme-data-in-plink/#.UO0ULVTZeSo)

From[Reconstructing Indian Population History](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC2842210/):

> …**We hypothesize that founder effects are responsible for an even > higher burden of recessive diseases in India than consanguinity**. To > test this hypothesis, we used our data to estimate the probability > that two alleles from a group share a common ancestor more recently > than that group’s divergence from other Indians, and compared this to > the probability that an individual’s two alleles share an ancestor in > the last few generations due to consanguinity…Nine of the 15 Indian > groups for which we could make this assessment had a higher > probability of recessive disease due to founder events than to > consanguinity, including all the Indo-European speaking groups (Table 2). It is important to systematically survey Indian groups to identify those with the strongest founder effects, and to prioritize them for studies to identify recessive diseases and map genes.

South Asian populations exhibit a lot of between population genetic distance, and not simply as a function of geography. With more markers and an expansive data set [Dan MacArthur](http://blogs.discovermagazine.com/gnxp/2012/12/a-lighter-shade-of-brown-dan-macarthur-look-east-or-south/#.UO0VTFTZeSo) will be able to assess exactly which South Asian caste his ancestry is from.

But this is an issue where I have fancied myself an outlier. My own background is moderately heterogeneous, and I’ve always explained to people that I’m not inbred like most South Asians, only half in jest (from what I can tell Muslims in the subcontinent have castes too, though they may somewhat different terminology). I know that my paternal grandmother came from a Brahmin family (clear by the customs preserved in the family even in her generation), while my maternal grandfather was almost certainly from a group with a Kayastha origin (going by surname, and who my mother actually clusters with). My maternal grandmother had considerable non-Bengali ancestry, which does show up in Middle Eastern signatures in my mother.

But this is talk. **Am I truly not as inbred as the average brown?** Leveraging methods which I discussed earlier (see posts above) I can very quickly check this.

  
First, you need to prune your data set to a reasonably homogeneous reference population which resembles your own ethnic makeup. The way you infer the extent of inbreeding is simply to look at the distribution of genetic variants, and see how shifted away from the population norm you are. Since different populations have different background distributions putting yourself within the wrong reference set leads to absurdity. **Compared to a Bushmen reference every non-African would come out as inbred.** The computation is not faulty, but it’s not giving you useful information.

In the .fam file of PHYLO I picked out every single non-Pakistani South Asian as my reference, mostly Gujarati, but with some South Indians as well. By looking at the expected genotypes by pooling this population together I want to get a sense of my own place. Additionally I’ll add my daughter and my 1/4 Filipino friend as controls, in that they should be way less “inbred” than everyone else since they are the products of recent admixture.

After using the – -keep function of Plink I merged the file with my own, my daughter’s, and friend’s. There were north of 90,000 SNPs, more than sufficient for the simple computation I wanted to do. I’ll output the [F-statistic](http://www.genetic-genealogy.co.uk/Toc115570144.html) with the – -het function like so:

plink – -noweb – -bfile DATASET – -het

The output is in plink.het. You’ll see the labels in the leftmost column, and the statistic you want in the rightmost column. In the results below are sorted from most to least inbred, at least using the F-statistic as a measure of that (this isn’t really totally accurate because the population isn’t really a homogeneous random mating set, but I think it gets the intuition out there):

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/webpreview_htm_4b9d2430.jpg?resize=575%2C1770 "webpreview_htm_4b9d2430")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/webpreview_htm_4b9d2430.jpg?resize=575%2C1770 "webpreview_htm_4b9d2430")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/webpreview_htm_4b9d2430.jpg)

The reason that my daughter and my friend have negative values is that they have way fewer homozygotes than you should get my chance. But they’re recent admixtures, so question of inbreeding is near not-even-wrong for them. The Plink documentation says that negative F values are noise (they are not contamination in this case), but I think I’ll chalk it up to a not-totally-homogeneous population. My position this list is not as low as I’d like, but I’ll take it. I believe I can still claim I’m less inbred than the average brown.

### Related Posts:

- [Using your 23andMe data: exploring with
  MDS](https://www.gnxp.com/WordPress/2013/01/08/using-your-23andme-data-exploring-with-mds/) - [Lots and lots of genotype
  data!](https://www.gnxp.com/WordPress/2013/01/09/lots-and-lots-of-genotype-data/) - [The Dodecad ancestry
  project](https://www.gnxp.com/WordPress/2010/10/25/the-dodecad-ancestry-project/) - [\$99 for 1 million
  markers](https://www.gnxp.com/WordPress/2012/12/11/99-for-1-million-markers/) - [The future of personal genomics is bright.
  23andMe....](https://www.gnxp.com/WordPress/2013/12/07/the-future-of-personal-genomics-is-bright-23andme/) - [I am free of rare homozygous recessives! (well,
  perhaps)](https://www.gnxp.com/WordPress/2012/09/30/i-am-free-of-rare-homozygous-recessives-well-perhaps/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F01%2F09%2Fusing-your-23andme-data-how-inbred-are-you%2F&linkname=Using%20your%2023andMe%20data%3A%20how%20inbred%20are%20you%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F01%2F09%2Fusing-your-23andme-data-how-inbred-are-you%2F&linkname=Using%20your%2023andMe%20data%3A%20how%20inbred%20are%20you%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F01%2F09%2Fusing-your-23andme-data-how-inbred-are-you%2F&linkname=Using%20your%2023andMe%20data%3A%20how%20inbred%20are%20you%3F "Email")[](https://www.addtoany.com/share)
