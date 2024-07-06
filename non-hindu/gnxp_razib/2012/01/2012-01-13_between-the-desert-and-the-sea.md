+++
title = "Between the desert and"
full_title = "Between the desert and the sea"
date = "2012-01-13"
upstream_url = "https://www.gnxp.com/WordPress/2012/01/13/between-the-desert-and-the-sea/"

+++
Source: [here](https://www.gnxp.com/WordPress/2012/01/13/between-the-desert-and-the-sea/).

Between the desert and the sea

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/01/250px-Zinedine_Zidane_2008.jpg?resize=250%2C260)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/01/250px-Zinedine_Zidane_2008.jpg?resize=250%2C260)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/01/250px-Zinedine_Zidane_2008.jpg)  
[Zinedine Zidane](https://en.wikipedia.org/wiki/Zinedine_Zidane), a [Kabyle](https://en.wikipedia.org/wiki/Kabyle_people)

There is a new paper in *PLoS Genetics* out which purports to characterize the ancestry of the populations of northern Africa in greater detail. This is important. The [HGDP data set](http://hagsc.org/hgdp/files.html) does have a North African population, the [Mozabites](https://en.wikipedia.org/wiki/Mozabite_people), but it’s not ideal to represent hundreds of millions of people with just one group. The first author on this new paper is Brenna Henn, who was also first author on another paper [with a diverse African data set](http://blogs.discovermagazine.com/gnxp/2011/03/where-in-the-world-did-anatomically-modern-humans-come-from/). Importantly **the data was posted online.** Unfortunately though most of the populations didn’t have too many markers. This isn’t an issue in an of itself, but it becomes a big deal when trying to combine it with other data sets. If you limit the markers to those which intersect across two data sets you start to thin them down a lot, to the point where they’re not useful. Though the the results of the paper are worth talking about, **the authors claim that they’ll be putting the [data online](http://bhusers.upf.edu/dcomas/?p=607)**. This is important because they used a large number of markers, so the intersections will be nice (I can, for example, envisage exploring the relationship between the North Africans and the IBS Iberian sample in the near future).

As for the paper itself, [Genomic Ancestry of North Africans Supports Back-to-Africa Migrations](http://www.plosgenetics.org/article/info%3Adoi%2F10.1371%2Fjournal.pgen.1002397):  

> Proposed migrations between North Africa and neighboring regions have > included Paleolithic gene flow from the Near East, an Arabic migration > across the whole of North Africa 1,400 years ago (ya), and > trans-Saharan transport of slaves from sub-Saharan Africa. Historical > records, archaeology, and mitochondrial and Y-chromosome DNA have been > marshaled in support of one theory or another, but there is little > consensus regarding the overall genetic background of North African > populations or their origin and expansion. We characterize the > patterns of genetic variation in North Africa using \~730,000 single > nucleotide polymorphisms from across the genome for seven populations. > We observe two distinct, opposite gradients of ancestry: an > east-to-west increase in likely autochthonous North African ancestry > and an east-to-west decrease in likely Near Eastern Arabic ancestry. > The indigenous North African ancestry may have been more common in > Berber populations and appears most closely related to populations > outside of Africa, but divergence between Maghrebi peoples and Near > Eastern/Europeans likely precedes the Holocene (\>12,000 ya). We also > find significant signatures of sub-Saharan African ancestry that vary > substantially among populations. These sub-Saharan ancestries appear > to be a recent introduction into North African populations, dating to about 1,200 years ago in southern Morocco and about 750 years ago into Egypt, possibly reflecting the patterns of the trans-Saharan slave trade that occurred during this period.

The model outline here is straightforward:

– A population of West Eurasian provenance migrated across the fringe of the southern Mediterranean \>10,000 years B.P. (Maghrebi)

– This was later overlain by a later West Asian migration (Near Eastern)

– A third major element here seems to be Sub-Saharan African admixture, which these authors claim is rather new (post-Roman)

Two of the methods used will be familiar to readers of this weblog. They used ADMIXTURE to generate barplots which fractionate putative ancestral components given K number of components. Second, they also use PCA to visualize the largest components genetic variation within the samples on a plane.

\[nggallery id=33\]

As you “move up” the K’s you note that Maghrebi populations “split” from the Near Eastern reference, the Qataris. This is supported by the PCA, which shows that there is a dimension of variation which separates Near Easterners & Europeans from Maghrebis. The authors note that this dimension is orthogonal to the Sub-Saharan African vs. Eurasian component. That suggests that the putative Maghrebi component is likely to be part of the set of “Out of Africa” populations, rather than an African population which simply experienced continuous gene flow with West Eurasians.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/01/journal.pgen_.1002397.g003-e1326436469454.png?resize=300%2C259)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/01/journal.pgen_.1002397.g003-e1326436469454.png?resize=300%2C259)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/01/journal.pgen_.1002397.g003.png)They also estimate a Fst, a statistic which partitions genetic variation within and between groups. The value between Sub-Saharan Africans and Europeans is \~0.15 using HGDP SNP data, and between Europeans and East Asians \~0.10. Using the Tuscans and Qataris as European and West Asian references against the North African populations along their east-west cline they estimate Fsts from \~0.03 to \~0.06. The higher end values are from populations which are less admixed with Near Eastern elements, and the colored polygons illustrate the domain generated by ADMIXTURE Fsts across *inferred* ancestral components. You also see in the chart estimated time of divergence. I won’t get into the assumptions in the model, but the authors do note that \~12,000 years B.P. seems to be the *low bound*estimate for when the Maghbrebis diverged from other West Eurasians. This is important, because it predates agriculture.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/01/hennfig3.jpg?resize=300%2C240)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/01/hennfig3.jpg?resize=300%2C240)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/01/hennfig3.jpg)The final set of methods outlined in this paper looked at ancestry on a more fine-grained genomic scale. To the left you see a plot where each horizontal bar represents an individual’s chromosome 1 (among a set of North Africans). Each color in that bar indicates a component of ancestry (except the black, which are centromeres). This sort of information is important, because saying someone is 50% X and 50% Y summarizes information to the point of eliding it. An individual who is a first generation product of a Chinese-European marriage is going to have the same ancestral proportions as someone who is a Uyghur for those respective populations. But a fine-scale mapping of the genomic ancestry would look very different, **because the history of the admixture is very different.**

There are many inferences in the paper which I won’t address. Rather, let me focus on this one assertion:

> After accounting for putative recent admixture (Figure 1), the > indigenous Maghrebi component (k-based) **is estimated to have > diverged from Near Eastern/Europeans between 18–38 Kya** (Figure 3), > under a range of Ne and k values. We hence suggest that the ancestral Maghrebi population separated from Near Eastern/Europeans prior to the Holocene, and that the Maghrebi populations do not represent a large-scale demic diffusion of agropastoralists from the Near East.

This is not implausible on the face of it. The component of ancestry modal in the Mozabite HGDP sample tends to have a relatively high Fst in relation to other West Eurasian groups. I had wondered if this was due to ancient Sub-Saharan African admixture which had produced a particular stabilized hybrid, but these results indicate that the component is no closer than other West Eurasians. **What I’m confused and skeptical about are the range of divergence times which different papers are producing which seem somewhat implausible *taken together*.**

There are papers which posit that East Asians separated from Europeans \~25,000 years B.P. This is in the same range as the divergence between Maghrebis and West Eurasians, but the Maghrebi genetic distance (Fst) is about 1/2 as great. Also, these sets of results which generate a “bunching” together of the separation of many extant non-African lineages in the 20-40,000 year range imply very rapid differentiation after the “Out of Africa” event, if that event did occur \~50,000 years ago (at least for most Eurasians, even assuming a revised model whereby Australian Aboriginals derive from an earlier wave). One at a time any given divergence estimate may be broadly plausible, **but the literature is just not particularly coherent on this matter, and it often seems archaeologically implausible.**

**Citation:** Henn BM , Botigué LR , Gravel S , Wang W , Brisbin A , et al. 2012 Genomic Ancestry of North Africans Supports Back-to-Africa Migrations. PLoS Genet 8(1): e1002397. doi:10.1371/journal.pgen.1002397

***Image Credit:** [Raphaël Labbé](https://en.wikipedia.org/wiki/File:Zinedine_Zidane_2008.jpg)*

### Related Posts:

- [African genetic
  structure](https://www.gnxp.com/WordPress/2009/04/30/african-genetic-structure/) - [Population structure within
  Africa](https://www.gnxp.com/WordPress/2011/03/16/population-structure-within-africa/) - [Out of South
  Africa?](https://www.gnxp.com/WordPress/2011/03/07/out-of-south-africa/) - [An algorithm is just an
  algorithm](https://www.gnxp.com/WordPress/2012/04/23/an-algorithm-is-just-an-algorithm/) - [Why not release data for phylogenetic
  papers?](https://www.gnxp.com/WordPress/2013/03/01/why-not-release-data-for-phylogenetic-papers/) - [Buddy, can you spare an
  SNP?](https://www.gnxp.com/WordPress/2007/09/20/buddy-can-you-spare-an-snp/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F01%2F13%2Fbetween-the-desert-and-the-sea%2F&linkname=Between%20the%20desert%20and%20the%20sea "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F01%2F13%2Fbetween-the-desert-and-the-sea%2F&linkname=Between%20the%20desert%20and%20the%20sea "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F01%2F13%2Fbetween-the-desert-and-the-sea%2F&linkname=Between%20the%20desert%20and%20the%20sea "Email")[](https://www.addtoany.com/share)
