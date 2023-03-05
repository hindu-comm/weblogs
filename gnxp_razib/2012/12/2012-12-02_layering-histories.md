+++
title = "Layering genetic"
full_title = "Layering genetic histories"
date = "2012-12-02"
upstream_url = "https://www.gnxp.com/WordPress/2012/12/02/layering-histories/"

+++
Source: [here](https://www.gnxp.com/WordPress/2012/12/02/layering-histories/).

Layering genetic histories

As a follow up to my [post from yesterday](http://blogs.discovermagazine.com/gnxp/2012/12/northern-europeans-and-native-americans-are-not-more-closely-related-than-previously-thought/), I decided to run [TreeMix](https://code.google.com/p/treemix/) on a data set I happened to have had on hand (see [Inference of Population Splits and Mixtures from Genome-Wide Allele Frequency Data](http://www.plosgenetics.org/article/info%3Adoi%2F10.1371%2Fjournal.pgen.1002967) for more on TreeMix). Basically I wanted to display a tree with, and without, gene flow.

The technical details are straightforward. I [LD pruned](http://pngu.mgh.harvard.edu/~purcell/plink/summary.shtml#prune) \~550,000 SNPs down to \~150,000. I ran TreeMix without and with migration parameters with the Bantu Kenya population being the root. Finally, when I did turn on the migration parameter I set it for 5. You can see the results below.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/noflow.png?resize=570%2C589)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/noflow.png?resize=570%2C589)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/noflow.png)

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/flow.png?resize=582%2C596)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/flow.png?resize=582%2C596)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/flow.png)

Most of the flows are pretty expected. The West Eurasian flow from the Turks to the Uygurs makes sense, because there is a large West Asian component to what the Uygurs have (from East Iranians?). The Chuvash are a Turkic group with minor, but significant, Turkic component. The HGDP Russian sample does have some East Eurasian ancestry. And the Moroccans also have African ancestry. But your guess is as good as mine with the Bantu flow in. These are I think Kenya, so it might be trying to interpret Nilotic admixture as generalized Eurasian.

**A minor note:** installing TreeMix and generating the appropriate files from pedigree format is not to difficult. But you might have confusion in how to generate the pedigree input file. You do it like so in PLINK:

    ./plink --noweb --bfile YourFile --freq --within YourGroupNamesFile --out YourOutPutFile

It’s the last you want to put into TreeMix’s python conversion script. The YourGroupNamesFile is basically the .fam file with an extra column, the population names for each individual.

### Related Posts:

- [TreeMix: Who were the West Eurasian ancestors of
  Ethiopians?](https://www.gnxp.com/WordPress/2012/12/02/who-were-the-west-eurasian-ancestors-of-ethiopians/) - [PCA remains the swiss-army-knife to explore
  population…](https://www.gnxp.com/WordPress/2017/11/16/pca-remains-the-swiss-army-knife-to-explore-population-structure/) - [The ancient scramble for
  Eurasia](https://www.gnxp.com/WordPress/2016/05/19/the-ancient-scramble-for-eurasia/) - [Unveiling the genealogical
  lattice](https://www.gnxp.com/WordPress/2012/12/18/unveiling-the-genealogical-lattice/) - [Why not release data for phylogenetic
  papers?](https://www.gnxp.com/WordPress/2013/03/01/why-not-release-data-for-phylogenetic-papers/) - [Phylogenetics implies Austro-Asiatic are intrusive to
  India](https://www.gnxp.com/WordPress/2013/01/29/phylogenetics-implies-austro-asiatic-are-intrusive-to-india/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F12%2F02%2Flayering-histories%2F&linkname=Layering%20genetic%20histories "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F12%2F02%2Flayering-histories%2F&linkname=Layering%20genetic%20histories "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F12%2F02%2Flayering-histories%2F&linkname=Layering%20genetic%20histories "Email")[](https://www.addtoany.com/share)
