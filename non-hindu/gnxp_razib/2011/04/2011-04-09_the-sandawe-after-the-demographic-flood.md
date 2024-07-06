+++
title = "The Sandawe after the"
full_title = "The Sandawe after the demographic flood"
date = "2011-04-09"
upstream_url = "https://www.gnxp.com/WordPress/2011/04/09/the-sandawe-after-the-demographic-flood/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/04/09/the-sandawe-after-the-demographic-flood/).

The Sandawe: after the demographic flood

Over the past few days I’ve been trying to read a bit on the [Sandawe](https://en.wikipedia.org/wiki/Sandawe_people). Most of the stuff I’ve been able to find is in the domain of linguistics, and is basically unintelligible to me in any substantive manner. The crux of the curiosity here is that the Sandawe, like their [Hadza neighbors](https://en.wikipedia.org/wiki/Hadza_people), have clicks in their language, and so have been classified with the Khoisan. Here’s some [background](https://en.wikipedia.org/wiki/Sandawe_language#Classification):

> The most promising candidate as a relative of Sandawe are the Khoe > languages of Botswana and Namibia. Most of the putative cognates > Greenberg (1976) gives as evidence for Sandawe being a Khoesan > language in fact tie Sandawe to Khoe. Recently Gueldemann and Elderkin > have strengthened that connection, with several dozen likely cognates, while casting doubts on other Khoisan connections. Although there are not enough similarities to reconstruct a Proto-Khoe-Sandawe language, there are enough to suggest that the connection is real.

I can’t speak to the validity of this at all, obviously. Some scholars do argue that the clicks in the Sandawe language were only acquired through interaction with peoples such as the Hadza, making an analogy to Xhosa, a Bantu language which has been strongly influenced by Khoi dialects. In any case, after having run ADMIXTURE a bunch of times on African population sets, and checked the genetic distances of the inferred ancestral ones, one thing that is clear is that **the Sandawe don’t show a particularly close genetic relationship to the Bushmen, nor do they show a close relationship to the Hadza.** In fact, the Hadza, Pygmies, and Bushmen show a closer relationship to each other, distant as it is, than to the Sandawe. The Sandawe themselves *are* distinctive from their Bantu neighbors, but, their connections seem more clear to the Masai and other peoples to the north.

Some of the anthropological stuff that I did find on the Sandawe not having to do with linguistics considered the issue of their status as hunter-gatherers, and their shift toward a form of agriculture within the past few centuries. Not surprisingly much of this literature consisted of ideologically shrill posturing, denouncing past scholarship for insensitivity and bigotry, while taking their own maximalist position. For example there has been the hypothesis that hunter-gatherer populations tend to be genetically and culturally isolated from agriculturalists, with several African groups used as exemplars. A group of anthropologists argue strenuously that this model may just be a construction of the biases of previous generations of scholars. But they offer little in the way of counterargument, more keen on uncovering the faults in the motives and methods of their predecessors than in building anything anew.

Genetics can help us a little here. Below are the results of ADMIXTURE and PCA I ran for a selection of populations. I pulled in some Behar et al. samples and merged it with the Henn et al. data set. The marker list was pruned down to \~160,000 SNPs. The limited selection of populations was conscious, insofar as I was exploring specific questions about the relationship of East African populations to Eurasian ones. At K = 8 the populations in my data set separated rather well. **Do not take this separation as evidence that this K is a reflection of absolute concrete ancestral populations.** Here’s the bar plot:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/sandawe8.png?resize=600%2C613)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/sandawe8.png?resize=600%2C613)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/sandawe8.png)

Since I’ve been running this data set, with some modifications, for a week now I can pick out some trends which I feel are robust at K = 8. For example, the Eurasian-like admixture you see across eastern Africa seems to be distinctively of a southern nature, centered on Arabia (probably Yemen). This makes total geographical sense. The Ethiopians and Somalis (I have some Somali samples which I threw in with the Ethiopians since the Cushitic Ethiopians seem more similar to the Somalis than to Semitic Ethiopians) lack the genetic influence of Bantus in totality. Rather, they have an affinity with the Nilo-Saharan peoples. Finally, the Sandawe tend to “break out” as a separate population only at higher K’s, generally clustering with the Nilo-Saharan element as long as possible.

Let’s also look at a PCA of the populations above on the first two principal components:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandaweFinal_htm_6c5acab21.jpg?resize=600%2C575)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandaweFinal_htm_6c5acab21.jpg?resize=600%2C575)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandaweFinal_htm_6c5acab21.jpg)

The PCA looks a little different from the ones you’re used to seeing because there are only West Eurasian and African groups in the sample. So the second component is not the familiar west-east axis in Eurasia, but the separation between the Mbuti and other Africans. On the far right of the plot you have Orcadians, then Druze, Saudis, and Yemenis. Then you have Horn of Africa populations, Ethiopians and Somalis along the vertical axis. Then Masai and Sandawe, and Luhya, a Kenyan Bantu group. The Masai are a confusing group. Even after removing problem individuals who might be related there tends to be a choppiness in the Masai results. The Sandawe on the other hand are more consistent by and large.

The genetic distances of the inferred ancestral groups aren’t too surprising. Here are MDS visualizations:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst12.png?resize=599%2C543)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst12.png?resize=599%2C543)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst12.png)

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst21.png?resize=598%2C557)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst21.png?resize=598%2C557)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst21.png)

One of the consistent trends you see is that the Masai are closer to Eurasians than the Sandawe, **but, the “Masai” modal ancestral component is no closer, or even further, from Eurasians than the “Sandawe” ancestral component**. At higher K’s once the “Sandawe” element partitions out it is extremely dominant among the Sandawe, and found in lower fractions among other East African groups, *especially* non-Bantu such as the Masai. I wouldn’t put too much stock in the high proportion in the Ethiopians above, as the outcomes are rather scattered across the K’s and population combinations. The Masai are a population who always seem to have a low fraction of Eurasian-like “Arabian”, and this is what drags the population toward the Eurasians as in the PCA above. The Sandawe seem to lack this admixture; rather, their affinity with Eurasians is deeper and may not be due to admixture at all (ADMIXTURE itself is not perfect, and may transform an admixed group into a “pure” component, as we can see sometimes as among the Fulani or among South Asians, and, I suspect the Mozabites).

Back to the Sandawe and their position in the history of East Africa. Unlike the Pygmies and Khoisan they are ***not*** basal in relation to other human lineages from what I can see here. That is, they don’t “split off” as early from the main cluster of branches in a phylogenetic tree of human populations. In fact, unlike the Pygmies and Khoisan, and like the Masai, they are *closer* to Eurasians than the West African or Bantu peoples. In other words, they’re *less* basal. In fact, the Sandawe may be closer to Eurasians than most of the Nilotic groups when recent admixture with Eurasians is removed from the picture.

I do not know if the Sandawe are indigenous to their region of Tanzania. If I had to bet money I’d say not, and that some scholarly suppositions for a northerly origin may be plausible based on the affinities with the Masai and even Cushitic and Semitic peoples of Ethiopia and Somalia. The distinctiveness of the Sandawe from their Bantu neighbors seems clear, and there is no special closeness to the Khoisan of Southern Africa.
Many anthropologists and historians have pointed out that some groups can “revert” to hunting and gathering facultatively. But the total Bantu domination of much of East Africa suggests to me that this is was not the case with the Sandawe. I think a plausible model is that the Sandawe were part of the substrate of East African hunter-gatherers who have mostly been eliminated and absorbed by the Bantu. In the north related peoples contributed to the emergent Nilo-Saharan and Ethiopian and Cushitic societies, which were able to avoid being swamped by the Bantu because of ecology and their own agricultural traditions. In this model the Sandawe affinities to Khoisan groups was more a matter of horizontal cultural borrowing and influence due to proximity, than a close genetic relationship.

### Related Posts:

- [The great Eurasian
  explosion](https://www.gnxp.com/WordPress/2012/09/17/the-great-eurasian-explosion/) - [Africa's hidden people hold the keys to the
  past](https://www.gnxp.com/WordPress/2012/12/02/africas-hidden-people-hold-the-keys-to-the-past/) - [Africa in 12 ADMIXTURE
  chunks](https://www.gnxp.com/WordPress/2011/04/06/africa-in-12-admixture-chunks/) - [The deep origins of East African
  Hunter-Gatherers](https://www.gnxp.com/WordPress/2019/02/19/the-deep-origins-of-east-african-hunter-gatherers/) - [The islands of genetic uniqueness in the
  swell](https://www.gnxp.com/WordPress/2011/04/08/the-islands-of-genetic-uniqueness-in-the-swell/) - [Azores to Atlantis: Africa through the
  shadows](https://www.gnxp.com/WordPress/2012/07/27/azores-to-atlantis-africa-through-the-shadows/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F04%2F09%2Fthe-sandawe-after-the-demographic-flood%2F&linkname=The%20Sandawe%3A%20after%20the%20demographic%20flood "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F04%2F09%2Fthe-sandawe-after-the-demographic-flood%2F&linkname=The%20Sandawe%3A%20after%20the%20demographic%20flood "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F04%2F09%2Fthe-sandawe-after-the-demographic-flood%2F&linkname=The%20Sandawe%3A%20after%20the%20demographic%20flood "Email")[](https://www.addtoany.com/share)
