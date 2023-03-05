+++
title = "ADMIXTURE, African"
full_title = "ADMIXTURE, African Ancestry Project, and confirmation bias"
date = "2011-05-02"
upstream_url = "https://www.gnxp.com/WordPress/2011/05/02/admixture-african-ancestry-project-and-confirmation-bias/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/05/02/admixture-african-ancestry-project-and-confirmation-bias/).

ADMIXTURE, African Ancestry Project, and confirmation bias

I’ve been running the [African Ancestry Project](http://africanancestryproject.org/) for a while now on the side on Facebook. But it’s getting unwieldy, so I finally set up the [website](http://africanancestryproject.org/). The main reason I started it up is that there have been complaints for a while now of problems with the 23andMe “ancestry painting” and such for some African groups. For example, a Nubian might be 70% “European.” One might argue that this is due to Arab admixture, but this is clearly not so if you look at the PCA plot. What’s going on? Probably a problem with the reference populations (only Yoruba for Africa), ascertainment bias in the chip (they’re tuned to European variation), and the fact that African genetic variance can cause some issues. I don’t know. But the problem has been persistent, and since most of the other genome blogging projects exclude Africans because they’re so genetically diverse I decided to take it on.

Three groups of people have submitted:

– People of the African Diaspora in the New World

– People from Africa, disproportionately Northeast Africans (Horn of African + Nubia, etc.)

– People of some suspected or known minor component of African ancestry

I’m at \~70 participants now. As one reference population set I’ve been using a subset of [Henn et al.](http://blogs.discovermagazine.com/gnxp/2011/03/population-structure-within-africa/) as well as some populations from [Behar et al.](http://www.harappadna.org/2011/01/behar-et-al-data/) I call this my “thin” set since there are only \~40,000 SNPs. A “thick” set has on the order of 300-400 thousand markers. But fewer populations. I’ve been putting the AAP members through ADMIXTURE in batches of 10, but I also run them all together sometimes for apples-to-apples comparisons. Yesterday I ran AF001 to AF070 from K = 2 to K = 14, unsupervised, with the thin reference. If you want to see all the results, [go here](http://africanancestryproject.org/?p=22). Doing all this myself over and over has given me some intuition as to the pitfalls in this sort of analysis. Especially in the area of confirmation bias.

This is how it happens. Let’s say you have a lot of individuals from dozens of populations and hundreds of thousands of markers. Obviously you can modulate the parameters a bit. The number of individuals, the weighting of the various populations, and how thick your marker set is going to be. There’s a practical reason to make your marker set thinner, **the algorithm runs much faster**. But as you reduce the number of markers the outcomes become much noisier. That’s evident when you look at individuals results, and not the population pooled ones. Varying the population set also matters a lot. If you have a sample with 75 Yoruba and 25 Druze vs. 50 Yoruba and 50 Druze, that can produce different results over the same number of Ks. Finally, obviously reducing the number of individuals causes problems with representativeness. Here the results become “noisy” at the population level, as a regional bias can distortion your perception of a given population.

How does this work with confirmation bias? **If you are proactively searching for patterns which align with a particular model or expectation you can often simply modulate the parameters until you obtain “reasonable” results.** An exact same issue crops up with multiple regression. And this need not be conscious. In the course of regular science workers often ignore aberrant results and seek out positive ones. What we’re talking about is a general human bias. Researchers have been known to run experiments and keep tweaking them until the p-value reaches statistical significance. First, this treats the p-value as a “magical” number. That’s really not how it should be viewed, but that’s how it plays out in the course of attempting to get published. Second, the p-value itself is going to vary as well, which is why running an experiment over and over can get you the “right” result. The same general problems can crop up with ADMIXTURE. If you have a dedicated computer you can keep running the algorithm with a range of parameters until you get a “reasonable” result. You may also see bizarre results, and dismiss them out of hand as the program acting wonky. I’ve done it myself. But who knows, perhaps some of the “bizarre” results are stumbling upon a novel insight?

I’m not making a postmodernist pure constructionist argument. These algorithms often give predictable and regular results. And some sought results are harder to attain than others (i.e., you have to keeping fishing in the pool longer until you finally get a “bite”). But, be very careful of relying on one chart or graph as a clincher in any argument. This includes stuff I’m presenting. Attempts at replication are important, but there’s only so much time. That’s why I’m encouraging readers to play with [these programs themselves](http://blogs.discovermagazine.com/gnxp/2011/03/analyzing-ancestry-with-admixture-step-by-step/).

Speaking of confirmation of a model. I thought I’d do a little experiment. Below are the \~70 participants in the AAP at K = 10. I’m not showing you the reference populations. I will tell you that:

1\) The largest number of participants are of New World African Diaspora descent

2\) Second in number are those of mostly non-African descent who have some reputed or known minority African ancestry

3\) A bit more than half a dozen individuals are of Northeast African ancestry, in full or part

4\) One individual has recent Japanese ancestry and another has recent Maya ancestry

5\) A minority of the New World Africans have origins in the Caribbean.

6\) There are only a few individuals of West African national origin in the data set, but they are there

First, look at this image and make your guesses (leave them in the comments, please don’t spoil it for others by identifying who is what by ID after you confirm):

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/af001_af070_k10i.png?resize=600%2C1237)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/af001_af070_k10i.png?resize=600%2C1237)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/af001_af070_k10i.png)

All the plots with reference [results are here](http://africanancestryproject.org/?p=22). Explicit self-identification is [here](http://africanancestryproject.org/?p=17).

### Related Posts:

- [The ethnic breakdown of 23andMe
  customers](https://www.gnxp.com/WordPress/2011/06/13/the-ethnic-breakdown-of-23andme-customers/) - [Are all DTC firms underestimating African ancestry
  in…](https://www.gnxp.com/WordPress/2016/03/28/are-all-dtc-firms-underestimating-african-ancestry-in-southern-europeans/) - [The Dodecad ancestry
  project](https://www.gnxp.com/WordPress/2010/10/25/the-dodecad-ancestry-project/) - [The Malagasy Ancestry
  Project](https://www.gnxp.com/WordPress/2012/05/10/the-malagasy-ancestry-project/) - [Native American ancestry in African
  Americans](https://www.gnxp.com/WordPress/2010/08/17/native-american-ancestry-in-african-americans/) - [Sex differences in ancestry in the New
  World](https://www.gnxp.com/WordPress/2009/11/25/sex-differences-in-ancestry-in-the-new-world/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F05%2F02%2Fadmixture-african-ancestry-project-and-confirmation-bias%2F&linkname=ADMIXTURE%2C%20African%20Ancestry%20Project%2C%20and%20confirmation%20bias "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F05%2F02%2Fadmixture-african-ancestry-project-and-confirmation-bias%2F&linkname=ADMIXTURE%2C%20African%20Ancestry%20Project%2C%20and%20confirmation%20bias "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F05%2F02%2Fadmixture-african-ancestry-project-and-confirmation-bias%2F&linkname=ADMIXTURE%2C%20African%20Ancestry%20Project%2C%20and%20confirmation%20bias "Email")[](https://www.addtoany.com/share)
