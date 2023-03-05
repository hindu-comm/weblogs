+++
title = "Phylogenetics implies"
full_title = "Phylogenetics implies AustroAsiatic are intrusive to India"
date = "2013-01-29"
upstream_url = "https://www.gnxp.com/WordPress/2013/01/29/phylogenetics-implies-austro-asiatic-are-intrusive-to-india/"

+++
Source: [here](https://www.gnxp.com/WordPress/2013/01/29/phylogenetics-implies-austro-asiatic-are-intrusive-to-india/).

Phylogenetics implies Austro-Asiatic are intrusive to India

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/549px-South_Asian_Language_Families.jpg?resize=549%2C599 "549px-South_Asian_Language_Families")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/549px-South_Asian_Language_Families.jpg?resize=549%2C599 "549px-South_Asian_Language_Families")](http://blogs.discovermagazine.com/gnxp/files/20%2013/01/549px-South_Asian_Language_Families.jpg)

Most people in South Asia speak one of two varieties of language, Indo-Aryan and Dravidian. These two are not particularly closely related. Indo-Aryan is an Indo-European language, as is evident in the plethora of obvious [cognates](https://en.wikipedia.org/wiki/Cognate) with other Indo-European dialects. I have a minimal fluency in Bengali, the easternmost of the Indo-European languages, and quite a bit more fluency with English, one of the most westernmost, and it was evident to me rather early on (e.g., *grass* vs. *gash*, *man* vs. *manush*, *nose* vs. *nak*). In contrast to me Dravidian languages are peculiar because the accent and cadence are clearly South Asian, but they are utterly impenetrable (though there are many loan words into Indo-Aryan from Dravidian).

  
[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/300px-Austroasiatic-en.svg_1.png?resize=300%2C342 "300px-Austroasiatic-en.svg")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/300px-Austroasiatic-en.svg_1.png?resize=300%2C342 "300px-Austroasiatic-en.svg")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/300px-Austroasiatic-en.svg_1.png)But in this post I’m going to explore the genetic relationships of the people who speak a subgroup of Austro-Asiatic languages indigenous to India, that of the Munda. The traditional question has always been whether the Austro-Asiatic languages are from India, or, whether they are from Southeast Asia. **More precisely, did the Munda culture come to India, or is the Munda culture a relic of the original Austro-Asiatic domain in eastern India?**

As background I believe it is important that readers understand that the territory between Vietnam and that of the Munda was likely dominated by Austro-Asiatic dialects \~2,000 years ago. Both the Burmese and Thai arrived in the historic period from southern China, and overthrew Mon or Khmer cultures which flourished in lowland Southeast Asia. In the case of both the Burmese and Thai it was a situation where the newcomers imposed their language upon the indigenous population, but by and large adopted most elements of high culture from the natives (e.g., Theravada Buddhism). The monarchies of Thailand and Burma drew directly from the Indic-inflected polities of the Khmer and Mon.

The recent extensive distribution and variety of Austro-Asiatic languages in Southeast Asia is suggestive of the likelihood that they derive from this area, but it is not a definitive point in that model’s favor. But there are now other genetic lines of inquiry. A few years ago a [paper came out](http://blogs.discovermagazine.com/gnxp/2010/10/sons-of-the-conquerers-the-story-of-india/#.UQfBCVQR-Sp) which reported that the Y chromosomal lineages of the Munda people which connect them to the Southeast Asia are much more diverse in Southeast Asia. This matters because population expansions and migrations tend to homogenize lineages through greater genetic drift, with the “source” population more likely to maintain diversity. Additionally, there was also evidence of a genetic variant in*EDAR*which has the hallmark of recent increase in frequency across eastern Asia. This seems to peg the Munda arrival to the Holocene, not the Pleistocene. Finally, there is the pattern of male lineages exhibiting some concordance with Southeast Asia, but female lineages being entirely indigenous. This is a classic expectation from a model of migration where there was a strong bias toward males because of the mobility of these groups, which lacked women and children.

I decided to further explore the question using the [Estonian Biocenter data sets](http://evolutsioon.ebc.ee/MAIT/public_data/index.html), as well as the HGDP and HapMap. For those of you who are curious about the technical details, I LD pruned the Estonian Biocenter marker set from \~600,000 down to \~130,000. I also put the samples through –geno 0.01 and –mind 0.80 on Plink to get high quality individuals and good coverage on markers. To be explicitly clear, I renamed and combined some of the populations in the original data set (e.g., Chamars = UP_Dalits). I ran a preliminary MDS to make sure that the data wasn’t strange, and it checked out.

So to do the analysis I ran [TreeMix](https://code.google.com/p/treemix/). I used Chinese Americans as the root outgroup population, and wanted 5 migrations, and also tried to correct for any remaining LD by looking across a window of 1,000 SNPs. You can view my first plot below.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/munda.png?resize=640%2C392 "munda")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/munda.png?resize=640%2C392 "munda")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/munda.png)

**The primary thing I would focus on is the gene flow from Cambodians to Munda.**This is exactly what one might expect if the Munda were intrusive to South Asia. More interestingly, observe that there is no gene flow *into* Burmese from the South Asian groups, even though they are much closer proximity to South Asia! This is probably picking up something deep in history then. The fact that the Munda diverge early from other South Asian groups is also in keeping with Admixture or Structure bar plot results: the South Asian ancestry of the Munda is relatively unadmixed.

Next I wanted to focus more on the eastern population flows. So I removed a lot of the western groups which overwhelmed my gene flow edges.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/MUNDA2.png?resize=531%2C415 "MUNDA2")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/MUNDA2.png?resize=531%2C415 "MUNDA2")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/MUNDA2.png)

In this scenario again there is a gene flow parameter from the rough region of the Cambodian node. Perhaps more curious now there is a powerful gene flow parameter into the Burmese from the same locus.Totally intelligible in light of the fact that the modern Burmese are*genetically* a hybrid population between Tibeto-Burman and Mon (Austro-Asiatic).

I’m certainly not ready to assert that the “case is closed.” But it seems that we need to shift our probabilities again toward the intrusive hypothesis.

**Image credit:** [Wikipedia](https://en.wikipedia.org/wiki/File:South_Asian_Language_Families.jpg)

### Related Posts:

- [What if aliens had an Indian
  accent?](https://www.gnxp.com/WordPress/2006/06/15/what-if-aliens-had-an-indian-accent/) - [How to reconstruct the
  Indo-Europeans](https://www.gnxp.com/WordPress/2011/12/16/how-to-reconstruct-the-indo-europeans/) - [Etruscan genetics hits The New York
  Times](https://www.gnxp.com/WordPress/2007/04/04/etruscan-genetics-hits-the-new-york-times/) - [Indo-European
  podcasts](https://www.gnxp.com/WordPress/2021/10/07/indo-european-podcasts/) - [Resolutions in the Indian genetic layer
  cake](https://www.gnxp.com/WordPress/2011/04/23/resolutions-in-the-indian-genetic-layer-cake/) - [There is no mystery to persistence of some languages
  despite…](https://www.gnxp.com/WordPress/2021/09/26/there-is-no-mystery-to-persistence-of-some-languages-despite-gene-flow/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F01%2F29%2Fphylogenetics-implies-austro-asiatic-are-intrusive-to-india%2F&linkname=Phylogenetics%20implies%20Austro-Asiatic%20are%20intrusive%20to%20India "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F01%2F29%2Fphylogenetics-implies-austro-asiatic-are-intrusive-to-india%2F&linkname=Phylogenetics%20implies%20Austro-Asiatic%20are%20intrusive%20to%20India "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F01%2F29%2Fphylogenetics-implies-austro-asiatic-are-intrusive-to-india%2F&linkname=Phylogenetics%20implies%20Austro-Asiatic%20are%20intrusive%20to%20India "Email")[](https://www.addtoany.com/share)
