+++
title = "The Roma have multitudes"
full_title = "The Roma have multitudes"
date = "2013-10-24"
upstream_url = "https://www.gnxp.com/WordPress/2013/10/24/roma-multitudes/"

+++
Source: [here](https://www.gnxp.com/WordPress/2013/10/24/roma-multitudes/).

The Roma have multitudes

![**Credit:** Dbachmann](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/10/Romani_population_average_estimate.png?resize=330%2C250)

**Update:** Turns out [“Maria” is also an ethnic Roma.](http://world.time.com/2013/10/25/mystery-blonde-girl-is-roma-after-all/?xid=rss-topstories&utm_source=feedburner&utm_medium=feed&utm_campaign=Feed%3A+time%2Ftopstories+%28TIME%3A+Top+Stories%29)

[There was a](http://world.time.com/2013/10/25/mystery-blonde-girl-is-roma-after-all/?xid=rss-topstories&utm_source=feedburner&utm_medium=feed&utm_campaign=Feed%3A+time%2Ftopstories+%28TIME%3A+Top+Stories%29) [recent case in Ireland](https://www.theguardian.com/world/2013/oct/24/blonde-girl-roma-parents-returned-dna) of a young Roma girl who was blonde haired and blue eyed being removed from her home, on the suspicion that she was not in fact the biological child of the presumed parents (who, like most Roma, are reportedly of dark complexion, hair, and eye). I even saw a report that a hospital was consulted on the probability of such an outcome, and they said it would be “extremely unusual”. It turns out that **DNA tests confirmed that this girl was the biological child of the putative parents.** And of course all this has be understood in light of the [case of “Maria”](http://www.mirror.co.uk/all-about/missing%20girl%20'maria'%20found) in Greece; a little blonde girl who turned out *not* to be the biological child of the two Roma who claimed her as their daughter (it looks like there was welfare fraud in that case).

My initial response to the Irish case was that consultant should be fired, **because in an admixed population like the Roma it shouldn’t be *that* unusual to have offspring who deviate a great deal from the parental phenotype.** This prompted some interesting reactions. First, there were those who seem blissfully ignorant of the fact that the Roma *are* an admixed population. That’s easy enough to resolve, as there have been scientific papers published on this issue using genome-wide data. Second, there are claims that [very small fraction of Roma have blonde hair and blue eyes (on the order of less than 1%)](https://twitter.com/HBDBibliography/status/393200617436348416). The latter may be a defensible claim, though not indisputably so.

Before we move on I have to clarify that there is a distinction between “Roma” and “Romani.” The latter refers broadly to the populations across Europe which were referred to as “Gypsy,” while the former denotes a set of populations with a center of distribution in Southeast Europe, in particular in the Balkans. In much of Northern and Western Europe there are now two populations of Romani with very distinct histories (and genetics): the Roma who have recently arrived from Southeast Europe, and the various non-Roma groups who have a very long history in their nations of residence (e.g., Finnish Kale).

In terms of various traits we know a fair amount about the [genetics of pigmentation](http://www.sciencedirect.com/science/article/pii/S1084952113000499) in humans. Though the fine grained individual predictive models are coarse, most of the genes which have large effects on population-scale differences are now well characterized. This allows me to produce a model which is reasonably plausible to give you an intuition for why brown-skinned populations can generate a wide range of outcomes in realized phenotype.

Imagine five loci rank-ordered in effect size, gene 1, gene 2, gene 3, gene 4, and gene 5. Each gene comes in two flavors, two alleles. One is a “dark” allele (produces dark pigmentation) and another is a “light” allele. From these you can have a distribution of complexion which is referred to as a “melanin index” (it’s dependent on reflectance). Imagine that you assume each allele at each gene exhibits a melanin index value like so in relation to the aggregate:

Gene 1 = 30, 2  
Gene 2 = 15, 1  
Gene 3 = 10, 1  
Gene 4 = 5, 2  
Gene 5 = 5, 0



What you see above are potential genotypes (all heterozygote implicitly), with their phenotypic values being the sum of the two. One allele at gene 1 contributes 30 melanin units, and the other 2. And so on. Taking the “dark” alleles and assume they’re all homozygote (so doubling them), you get a maximal potential value of 130, and a minimal one of 6 if you make the “light” ones homozygote. But of course in most cases you’ll get a combination. But what would be the outcome for a given set of frequencies? Since I’m lazy I ran a simulation. I set the frequencies of the dark allele for each each like so:

Gene 1 = 60%  
Gene 2 = 45%  
Gene 3 = 35%  
Gene 4 = 46%  
Gene 5 = 50%

Then I generated 10,000 multilocus genotypes, and added a “noise” parameter so that the trait wasn’t totally determined by the genes. This is why the phenotypic value can be higher (and lower, though that bound can go no further than \~0) than what genotype would predict. Here’s the distribution:

[![Rplot07](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/10/Rplot07.png?resize=501%2C340)![Rplot07](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/10/Rplot07.png?resize=501%2C340)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/10/Rplot07.png)

The mean value is 73. The 25th percentile is 55. 1 out of 26 individuals should have an exclusively “light” genotype across all five genes. **The point is that in a polygenic character if you have polymorphism on the genotypic level you’re likely to have it on the phenotypic level.**

[![roma2](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/10/roma2.png?resize=250%2C665)![roma2](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/10/roma2.png?resize=250%2C665)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/10/roma2.png)The second major question is is this even plausible for Roma? Yes. They’ve very admixed. Two recent papers make the case definitively, [Reconstructing Roma History from Genome-Wide Data](http://www.plosone.org/article/info%3Adoi%2F10.1371%2Fjournal.pone.0058633) and [Reconstructing the Population History of European Romani from Genome-wide Data](http://www.sciencedirect.com/science/article/pii/S0960982212012602). These papers used tens of thousands to hundreds of thousands of markers. You can see in the bar plot to the left that the Roma have much higher European-like ancestry proportions than other Indians. It is likely their parental population is Punjabi-like, so it seems that they’re \~50% non-Indian in admixture. The second paper offers up a wider population set for comparison, and it suggests that the Roma did not experience much gene flow with Middle Eastern groups (there are still Roma-related populations in the Middle East, the Dom). Rather, their primary phase of admixture occurred \~1,000 years ago in the Balkans.

[Reconstructing the Population History of European Romani from Genome-wide Data](http://www.sciencedirect.com/science/article/pii/S0960982212012602)has a wide range of Romani populations, and it seems evident that the Western and Northern Romani have more European admixture than the Balkan Roma. It turns out that the Welsh Romani seem ***totally*** Europanized in their genome.That is, they’re basically now a Northern European population, perhaps with some residual South Asian ancestry. Because these Romani originally spoke an Indo-Aryan language it seems that they are genuine Romani in a cultural sense. The Welsh Romani have simply undergone enough gene flow with the surrounding population over the past hundreds of years to lose their genetic distinctiveness.

[![second](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/10/second2.png?resize=204%2C1131)![second](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/10/second2.png?resize=204%2C1131)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/10/second2.png)You can see a broader population wide comparison in this bar plot. European populations are at the top, and below them are the Romani groups. The South Asian admixture is again evident, **but observe the paucity of both of the Middle Eastern components** (you can label them “Northern/Caucasian” or “Southern/Arabian” for convenience; they show up repeatedly in Admixture analyses). The authors of the second paper linked above make much of this, but I would be cautious. I would have preferred that they run Admixture in supervised mode, or perhaps used a formal test of admixture (e.g., D-statistic). But, it is strongly suggestive of the possibility that the Roma sojourn in the Middle East was rather short, and that the true ethnogenesis of the group occurred in the Balkans primarily. And, as I said earlier, the European genetic character of Welsh Romani is pretty obvious in this plot (they cluster with Europeans in the PCA as well).

But, despite the Romani history of admixture in Europe, some of them are genetically very isolated now, and have been for hundreds of years. This seems the case of the Roma, who have had surprisingly little admixtures since the initial settlement. There’s widespread evidence of inbreeding and founder effect across the Romani populations as well, making them both admixed and very distinct. You see long runs of homozygosity, and the clustering bar plots tend to “break out” the Roma rather early on in the steps up the number of populations, similar to what you see in groups such as the Kalash. I believe one of the problems with adducing phylogenetic relationships of the Romani with Y and mtDNA markers was simply that bottleneck effects are more powerful for uniparental lines, and they were buffeted more by the small population size. In sum, when it comes to Roma genetic variation there are a few things to keep in mind:

1\) South Asian source

2\) Admixture with Southeastern Europeans

3\) Long period of relatively genetic continuity and isolation after the initial phase

4\) Genetic homogeneity within the groups. That is, they’re well admixed across most individuals

5\) Lots of novel genetic uniqueness because of high drift rate because of small effective population size

### Related Posts:

- [Saxons, Vikings and
  Celts](https://www.gnxp.com/WordPress/2006/10/28/saxons-vikings-and-celts/) - [On the varieties of
  Roma](https://www.gnxp.com/WordPress/2010/09/28/one-the-varieties-of-roma/) - [Daily Data Dump -
  Monday](https://www.gnxp.com/WordPress/2010/10/04/daily-data-dump-monday-20/) - [The myth of the brown-eyed baltic
  blonde?](https://www.gnxp.com/WordPress/2005/05/02/the-myth-of-the-brown-eyed-baltic-blonde/) - [Harappa Ancestry Project, t-minus one
  day](https://www.gnxp.com/WordPress/2011/01/31/harappa-ancestry-project-t-minus-one-day/) - [Blonde
  Berbers](https://www.gnxp.com/WordPress/2007/09/27/blonde-berbers/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F10%2F24%2Froma-multitudes%2F&linkname=The%20Roma%20have%20multitudes "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F10%2F24%2Froma-multitudes%2F&linkname=The%20Roma%20have%20multitudes "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F10%2F24%2Froma-multitudes%2F&linkname=The%20Roma%20have%20multitudes "Email")[](https://www.addtoany.com/share)
