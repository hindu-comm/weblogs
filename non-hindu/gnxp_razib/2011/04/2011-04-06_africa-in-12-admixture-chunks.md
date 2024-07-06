+++
title = "Africa in 12 ADMIXTURE"
full_title = "Africa in 12 ADMIXTURE chunks"
date = "2011-04-06"
upstream_url = "https://www.gnxp.com/WordPress/2011/04/06/africa-in-12-admixture-chunks/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/04/06/africa-in-12-admixture-chunks/).

Africa in 12 ADMIXTURE chunks

Some have asked what the point is in poking around African population structure when [Tishkoff et al.](http://www.sciencemag.org/content/324/5930/1035.abstract) and [Henn et al.](http://www.pnas.org/content/early/2011/03/01/1017511108) have done such a good job in terms of coverage. First, **it is nice to run your own analyses so you can slice & dice to your preference, and not rely on the constrained menu provided by others.** There’s value in home cooking; you can flavor to your taste. Second, you never know what data people might leave on your doorstep. I’ve received the genotypes of three Somalis. Nothing too surprising, a touch more Cushitic than the Ethiopians in [Behar et al.](http://www.harappadna.org/2011/01/behar-et-al-data/), but interesting nonetheless.

Also, you can see how ADMIXTURE tends to come to weird conclusions in certain circumstances. Below is a K = 12 run \~50,000 SNPs. I’ve included in a few Behar et al. and HGDP populations to the Henn et al. set, as well as pruned a lot of the African groups which seem redundant in terms of information. I’ve added a few geographically informative labels as well.

Observe below that there is a Fulani cluster. **I think this is pretty much an artifact.** At K = 7 the Fulani have a majority component which is modal in West Africa & Bantu speakers, and a minority component which is identical to the one modal in [Mozabite Berbers](https://en.wikipedia.org/wiki/Mozabite_people) from Algeria. The Mozabites reside in the far northern Sahara, and their modal component drops off as one goes east toward western Asia and the eastern Mediterranean. I suspect that what is showing up in ADMIXTURE is the ancient hybridization of the Fulani, and perhaps their demographic expansion from this core group. We have some glimmers of the prehistory of the Fulani, and no expectation for them to be such a distinctive cluster, so I naturally jump to these inferences. **But it does make me reconsider the nature of the “Sandawe,” “Mbuti” or “San” clusters in ADMIXTURE.** These populations are culturally distinctive in deep ways from their neighbors, so a reflexive inference one might make is that they’re “pure” ancient substrate groups which have been overlain and marginalized by their Bantu neighbors. But their prehistory is far murkier than the Fulani because of their geographical isolation, so there is far less to go on. These “ancient” isolated groups themselves may have gone through the same sort of distinctive recent ethnogenesis processes which we presume occurred with the Fulani (also, in the plot below the Biaka are pure; but in most of the bar plots they have a minor element which they share with their neighbors, probably due to greater admixture and interaction between western Pygmies and their Bantu neighbors than among the easter ones).

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/af1.jpg?resize=600%2C548)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/af1.jpg?resize=600%2C548)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/af1.jpg)

OK, now let’s prune some of the “pure” and extraneous populations. Additionally, I’ll remove some of the K’s. So the proportions are going to be recalculated with a new base. So, keep in mind that the South African Bantus show elevated West African in part because the Khoisan proportion was removed, inflating the percentages for all the other elements.  
[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/af2.jpg?resize=600%2C560)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/af2.jpg?resize=600%2C560)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/af2.jpg)

Now let’s look at the pairwise Fst values between inferred populations. Remember, this **measures the proportion of genetic variance which can be attributed to *between* population differences.** The bigger the value, the larger the genetic distance. I’ll given the inferred populations labels, but don’t take that too seriously.

------------------------------------------------------------------------

|                                                |        |      |      |      |         |       |           |          |         |       |          |       |
|------------------------------------------------|--------|------|------|------|---------|-------|-----------|----------|---------|-------|----------|-------|
| Fst divergences between estimated populations: |        |      |      |      |         |       |           |          |         |       |          |       |
|                                                | Fulani | San  | Euro | Maya | Nilotic | Biaka | W African | SW Asian | Sandawe | Mbuti | Mozabite | Bantu |
| Fulani                                         | 0.00   | 0.19 | 0.15 | 0.26 | 0.11    | 0.13  | 0.09      | 0.14     | 0.10    | 0.18  | 0.12     | 0.10  |
| San                                            | 0.19   | 0.00 | 0.27 | 0.37 | 0.16    | 0.11  | 0.13      | 0.25     | 0.13    | 0.13  | 0.23     | 0.13  |
| European                                       | 0.15   | 0.27 | 0.00 | 0.18 | 0.17    | 0.22  | 0.19      | 0.05     | 0.15    | 0.26  | 0.06     | 0.19  |
| Maya                                           | 0.26   | 0.37 | 0.18 | 0.00 | 0.27    | 0.31  | 0.28      | 0.19     | 0.25    | 0.36  | 0.20     | 0.28  |
| Nilotic                                        | 0.11   | 0.16 | 0.17 | 0.27 | 0.00    | 0.10  | 0.07      | 0.17     | 0.08    | 0.14  | 0.13     | 0.07  |
| Biaka                                          | 0.13   | 0.11 | 0.22 | 0.31 | 0.10    | 0.00  | 0.07      | 0.21     | 0.09    | 0.09  | 0.18     | 0.07  |
| W African                                      | 0.09   | 0.13 | 0.19 | 0.28 | 0.07    | 0.07  | 0.00      | 0.17     | 0.07    | 0.12  | 0.14     | 0.05  |
| SW Asian                                       | 0.14   | 0.25 | 0.05 | 0.19 | 0.17    | 0.21  | 0.17      | 0.00     | 0.14    | 0.25  | 0.06     | 0.18  |
| Sandawe                                        | 0.10   | 0.13 | 0.15 | 0.25 | 0.08    | 0.09  | 0.07      | 0.14     | 0.00    | 0.13  | 0.12     | 0.07  |
| Mbuti                                          | 0.18   | 0.13 | 0.26 | 0.36 | 0.14    | 0.09  | 0.12      | 0.25     | 0.13    | 0.00  | 0.22     | 0.12  |
| Mozabite                                       | 0.12   | 0.23 | 0.06 | 0.20 | 0.13    | 0.18  | 0.14      | 0.06     | 0.12    | 0.22  | 0.00     | 0.14  |
| Bantu                                          | 0.10   | 0.13 | 0.19 | 0.28 | 0.07    | 0.07  | 0.05      | 0.18     | 0.07    | 0.12  | 0.14     | 0.00  |

------------------------------------------------------------------------

Here’s the **genetic distance between non-African groups and African ones** on a bar plot**.**

**[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/fstdist.jpg?resize=600%2C495)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/fstdist.jpg?resize=600%2C495)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/fstdist.jpg)**

Some consistent trends:

– Mbuti and Khoisan show the largest distance from non-Africans.

– Biaka are next. Again, this may be due to admixture between Biaka and neighboring groups, or, a closer relationship between the Biaka Pygmies and the non-Khoisan/Mbuti African groups with reference to the last common ancestors.

– Roughly equal distance of Bantus and West Africans.

– Marginally smaller distances between the Nilotic cluster and non-Africans.

– Finally, a **consistently smaller difference between non-Africans and the Sandawe cluster.**

As always we need to remember that these probably aren’t pure concrete real ancestral groups. I have no hesitation in presuming some low level consistent gene flow over time between the western Mediterranean groups of which Mozabites are part and some of the Nilotic populations in north-central Africa. This equilibration of gene frequencies would reduce the Fst value naturally. Second, the *relative* closeness of the Sandawe cluster jumped out at me initially when I looked at the African data. It just strikes me as weird.

Here’s Wikipedia on the [Sandawe](https://en.wikipedia.org/wiki/Sandawe_people):

> The Sandawe are an agricultural ethnic group based in the Kondoa district of Dodoma Region in central Tanzania. In 2000 the Sandawe population was estimated to number 40,000. >
> The Sandawe language is a tonal language with clicks, apparently > related to the Khoe languages of southern Africa. Recent research suggests that the ancestors of the Khoe were pastoralists, and migrated into southern Africa from the northeast, perhaps from the region of the modern Sandawe.

But the Sandawe don’t seem to be that close to the South African Bushmen samples. Here’s a multidimensional scaling of the Fst relationships of selected inferred ancestral African groups (weight the x-axis more):

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst11.png?resize=600%2C558)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst11.png?resize=600%2C558)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst11.png)

An aspect of PCA plots which *always* jumps out you is the gap between African groups and non-African ones, often spanned by populations which have likely recent admixture. One hypothesis to explain this is that there’s been little gene flow between Africa and the rest of the world since the Out of Africa event. Probably due to ecology (the Sahara). But here’s another explanation: **the Bantu expansion has wiped clean much of the genetic variation of central and eastern Africa, the very variation which might span in part the African vs. non-African gap.** The archaeology and anthropology indicate that both the groups currently dominant in much of eastern Africa and down to the south, the Bantu and Nilotic peoples, are intrusive on the scale of the past 3,000 years. So groups like the Hadza and the Sandawe are presumed to be relics of the older cultural and genetic variation. This may be why the Sandawe are closer to Eurasians than other African groups once you control for clear likely admixture (e.g., the Fulani). Or, it may be that the Sandawe themselves have an older admixture event due to back-migration from Eurasia….

Finally, let me leave you with a bunch of MDS plots which visualize the Fst differences.  
[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst1.png?resize=600%2C564)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst1.png?resize=600%2C564)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst1.png)  
[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst2.png?resize=600%2C531)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst2.png?resize=600%2C531)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst2.png)  
[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst3.png?resize=600%2C565)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst3.png?resize=600%2C565)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst3.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst4.png?resize=600%2C556)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst4.png?resize=600%2C556)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst4.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst5.png?resize=600%2C555)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst5.png?resize=600%2C555)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst5.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst6.png?resize=600%2C547)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst6.png?resize=600%2C547)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst6.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst7.png?resize=600%2C555)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst7.png?resize=600%2C555)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst7.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst8.png?resize=600%2C550)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst8.png?resize=600%2C550)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst8.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst9a.png?resize=600%2C551)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst9a.png?resize=600%2C551)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst9a.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst9b.png?resize=600%2C545)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst9b.png?resize=600%2C545)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst9b.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst9c.png?resize=600%2C546)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst9c.png?resize=600%2C546)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst9c.png)[![ ](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst10.png?resize=600%2C557)![ ](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst10.png?resize=600%2C557)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/Fst10.png)

### Related Posts:

- [Population structure within
  Africa](https://www.gnxp.com/WordPress/2011/03/16/population-structure-within-africa/) - [The genetic palimpsest of the Horn of
  Africa](https://www.gnxp.com/WordPress/2019/01/10/the-genetic-palimpsest-of-the-horn-of-africa/) - [A genomic sketch of the Horn of
  Africa](https://www.gnxp.com/WordPress/2011/06/09/a-genomic-sketch-of-the-horn-of-africa/) - [Tutsi genetics,
  ii](https://www.gnxp.com/WordPress/2011/08/31/tutsi-genetics-ii/) - [The genetic affinities of
  Ethiopians](https://www.gnxp.com/WordPress/2011/01/10/the-genetic-affinities-of-ethiopians/) - [The Fulani have an old "Berber" (?)
  element](https://www.gnxp.com/WordPress/2012/01/16/the-fulani-have-an-old-berber-element/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F04%2F06%2Fafrica-in-12-admixture-chunks%2F&linkname=Africa%20in%2012%20%20ADMIXTURE%20chunks "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F04%2F06%2Fafrica-in-12-admixture-chunks%2F&linkname=Africa%20in%2012%20%20ADMIXTURE%20chunks "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F04%2F06%2Fafrica-in-12-admixture-chunks%2F&linkname=Africa%20in%2012%20%20ADMIXTURE%20chunks "Email")[](https://www.addtoany.com/share)
