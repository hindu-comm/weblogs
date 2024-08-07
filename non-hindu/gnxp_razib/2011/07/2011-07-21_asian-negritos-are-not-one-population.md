+++
title = "Asian Negritos are not"
full_title = "Asian Negritos are not one population"
date = "2011-07-21"
upstream_url = "https://www.gnxp.com/WordPress/2011/07/21/asian-negritos-are-not-one-population/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/07/21/asian-negritos-are-not-one-population/).

Asian Negritos are not one population

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/Ati_woman.jpg?resize=200%2C216)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/Ati_woman.jpg?resize=200%2C216)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/Ati_woman.jpg)  
Negrito, Philippines.***Credit:** [Ken Ilio](https://en.wikipedia.org/wiki/File:Ati_woman.jpg)*

In the [post below](http://blogs.discovermagazine.com/gnxp/2011/07/to-the-antipode-of-asia/) I mentioned that the Malaysian and Philippine Negritos seem to be two very distinct populations. This was something I wanted to explore in more detail, so I naturally decided to poke around the [Pan-Asian SNP](http://www.genomeweb.com/arrays/hugo-pan-asian-snp-consortium-maps-genetic-diversity-asia) data set. The aims are made somewhat more difficult by the fact that there are only \~56,000 markers in the data set (as opposed to \~600,000 in the HGDP and more than 1 million in the HapMap). Additionally, the intersection with other data sets is small. For example, only \~20,000 SNPs with the HGDP. With all that in mind I hazarded that something is better than nothing. Relatives and HapMap populations were removed from the data set (thanks [Zack](http://www.harappadna.org/)). Additionally, I beefed up the South Asian populations with the Gujaratis from the HapMap,which had an intersection of \~32,000 SNPs. After a few test runs I decided to remove the [Mlabri](https://en.wikipedia.org/wiki/Mlabri_language). They always shook out very early as a separate population from many others nearby, and, their genetic distances were very high. This tribe is only numbered in the hundreds, and I wouldn’t be surprised if they’ve been subjected to a lot of population bottlenecks, resulting in some very distinctive allele frequencies.

But before I move to the results, let’s back up for a moment. Who are the [“Negritos”](https://en.wikipedia.org/wiki/Mlabri_language)? As suggested by the term Negrito refers to a range of populations which are characterized by small size and African-like features (very dark skin and frizzy hair). In general their distribution is limited to Southeast Asia (there are suggestions that a Negrito population may only recently have gone extinct in Australia’s rainforests, but that’s speculative. On a more antique scale there are records which may be interpreted to suggest the existence of Negritos in Taiwan as late as 1900, and in southern China within the past 1,000 years). So you can bracket their distribution from the Andaman Islands to the Philippines, with isolated groups in the Malay peninsula. Negritos are presumed to be the original inhabitants of Southeast Asia before the arrival of rice farmers from the north. Like the Pygmies of Africa most of the Negritos speak languages whic hare known in other populations. Those of the Philippines speak Austronesian dialects. Interestingly those of Malaysia speak an Austro-Asiatic language, and so have affinities with many groups to their north linguistically, being surrounded by Austronesian speakers. Only the Andaman Islanders have a distinctive language, which makes sense seeing as how they have been relatively isolated from mainland Asian influences.

I ran ADMIXTURE from K = 4 to K = 12. K = 8 seemed the most informative to me (at higher K’s the major dynamic is that the Philippine Negritos start fragmenting into many distinct clusters). I’ve made a few cosmetic changes. With this East and Southeast Asia heavy data set there’s almost no difference between all the various Indian groups, so I amalgamated them together. I also did the same for related populations geographically adjacent which exhibited no genetic difference (e.g., Central and East Javanese).

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/K8all1.jpg?resize=500%2C1015)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/K8all1.jpg?resize=500%2C1015)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/K8all1.jpg)

The distinctiveness of the two Negrito groups is rather obvious. But what makes it even more obvious are the Fst values across two inferred clusters.

|                     |          |           |       |            |         |           |                |              |
|---------------------|----------|-----------|-------|------------|---------|-----------|----------------|--------------|
|                     | NE Asian | P Negrito | Hmong | Melanesian | S Asian | M Negrito | Austro-Asiatic | Austronesian |
| NE Asian            | 0        | 0.101     | 0.046 | 0.099      | 0.095   | 0.098     | 0.07           | 0.045        |
| Philippines Negrito | 0.101    | 0         | 0.11  | 0.105      | 0.113   | **0.124** | 0.108          | 0.096        |
| Hmong               | 0.046    | 0.11      | 0     | 0.108      | 0.107   | 0.099     | 0.072          | 0.058        |
| Melanesian          | 0.099    | 0.105     | 0.108 | 0          | 0.099   | 0.113     | 0.104          | 0.1          |
| S Asian             | 0.095    | 0.113     | 0.107 | 0.099      | 0       | 0.104     | 0.103          | 0.108        |
| Malaysian Negrito   | 0.098    | **0.124** | 0.099 | 0.113      | 0.104   | 0         | 0.086          | 0.098        |
| Austro-Asiatic      | 0.07     | 0.108     | 0.072 | 0.104      | 0.103   | 0.086     | 0              | 0.062        |
| Austronesian        | 0.045    | 0.096     | 0.058 | 0.1        | 0.108   | 0.098     | 0.062          | 0            |

What’s clearly evident here is that **the largest genetic distance across any two inferred populations is between the Malaysian and Philippine Negrito clusters!** Let’s visualize the relationships a bit:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/mds1.jpg?resize=400%2C364)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/mds1.jpg?resize=400%2C364)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/mds1.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/MDS2.jpg?resize=400%2C365)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/MDS2.jpg?resize=400%2C365)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/MDS2.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/MDS3.jpg?resize=400%2C365)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/MDS3.jpg?resize=400%2C365)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/MDS3.jpg)

Observe that Philippine Negrito cluster tends to have an affinity for Austronesians and the Malaysian Negrito one has one for the Austro-Asiatics. You can tell from the different tribes that there’s varied admixture with Austronesians in the former case, but what about the Malaysian Negritos? (who are of the Jehai and [Kensui](https://en.wikipedia.org/wiki/Kensiu_language) affiliation) Here’s the individual bar plot:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/K8Negrito.jpg?resize=346%2C760)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/K8Negrito.jpg?resize=346%2C760)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/K8Negrito.jpg)

There’s a substantial Austro-Asiatic admixture in this population. We have seen before that ADMIXTURE’s inferred population clusters are only a *rough* guide to the real populations which existed in the past. The reality is that the history of the human race has been characterized by repeated fissions and fusions of populations, so all ADMIXTURE clusters are going to be composites anyway depending on the chronology which you are using. The affinity of the Malaysian and Philippine Negrito clusters to the ones geographically close to them suggest to me that they’re telling us about ancient admixture events which have been recombined to the point that a new composite population naturally falls out of the algorithm. It may be that after Taiwan the Philippines was the first major landfall of the original Austronesians, so they may have had a substantial impact on the Negritos very early one. This is already clear in most of the Negrito tribes even with ADMIXTURE. In the case of the Malaysian Negritos the admixture is less extreme, but the fact that they speak an Austro-Asiatic language points to hybridization.

I also ran some principal component analyses. Basically each dimension represents an independent axis of variation in the genetic data set. The first component of variation is clearly the west-east one ins Eurasia. Note that it’s 5 times larger than the second dimension. I’ve highlighted the two Negrito populations. Observe that in general they don’t manifest a particular close relationship:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/D1byD2.jpg?resize=600%2C551)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/D1byD2.jpg?resize=600%2C551)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/D1byD2.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/D2byD3.jpg?resize=600%2C551)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/D2byD3.jpg?resize=600%2C551)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/D2byD3.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/D2byD4.jpg?resize=600%2C551)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/D2byD4.jpg?resize=600%2C551)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/D2byD4.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/D2byD6.jpg?resize=600%2C548)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/D2byD6.jpg?resize=600%2C548)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/D2byD6.jpg)

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/661px-Map_of_Sunda_and_Sahul.jpg?resize=300%2C220)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/661px-Map_of_Sunda_and_Sahul.jpg?resize=300%2C220)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/661px-Map_of_Sunda_and_Sahul.jpg)So what’s the moral of this story? **Don’t judge a book by its cover!** Up until the waters rose with the end of the last Ice Age \~12,000 years ago the southeast region of Eurasia, and out toward Oceania, were far less fragmented. Biogeographically you have Sundaland where Malaysia and western Indonesia are today. To the east there was Sahul, which combined Australia and New Guinea. Expanding out to India and southeast to Australia physical anthropologists in the 20th century posited the [Australoid race](https://en.wikipedia.org/wiki/Australoid_race). Using ADMIXTURE and PCA you *can* see shadows of an Ice Age Southeast Eurasian race which extended from India to Australia. Shadows because outside of Australia and Melanesia it is either a thin submerged layer, or it persists as residual tribes such as the Ati of the Philippines or the Semang of Malaysia.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/300px-Malaya_1905.jpg?resize=300%2C213)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/300px-Malaya_1905.jpg?resize=300%2C213)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/07/300px-Malaya_1905.jpg)  
Malaysian Negritos \~1900

But these populations had their own population structure and distinctions. My bet would be that the Malaysian Negritos are closer to the Onge of the Andaman Islanders, and that these two groups emerged out of a *western* branch of Sundalanders. The Philippine Negritos are from an *eastern* branch, and their closer affinity to Melanesians *may* be due to longstanding gene flow across the two populations (another option is that very old Austronesian admixture in both has shifted their non-Austronesian components closer together in allele frequency). Overall, I suspect that the past \~10,000 years have been radically different from the past insofar as population replacement and expansion has occurred on a scale never before seen due to the demographic impact of agriculture. The remaining Negritos may be the tip of the iceberg in terms of the genetic diversity which disappeared as the hunters gave way to the farmers.

***Image credit:** [Maximilian Dörrbecker](https://en.wikipedia.org/wiki/File:Map_of_Sunda_and_Sahul.png)*

### Related Posts:

- [Shadows of phenotypes
  lost](https://www.gnxp.com/WordPress/2011/07/22/shadows-of-phenotypes-lost/) - [1000 Genomes data, 290,000
  SNPs](https://www.gnxp.com/WordPress/2015/09/30/1000-genomes-data-290000-snps/) - [Genomics to complex
  traits](https://www.gnxp.com/WordPress/2009/02/18/genomics-to-complex-traits/) - [Was H. luzonensis
  Denisovan?](https://www.gnxp.com/WordPress/2021/08/14/was-h-luzonensis-denisovan/) - [Out of Africa onward to
  Wallacea](https://www.gnxp.com/WordPress/2011/09/22/out-of-africa-onward-to-wallacea/) - [The Merina of Madagascar are Malay and
  Bantu](https://www.gnxp.com/WordPress/2011/09/09/the-merina-of-madagascar-are-malay-and-bantu/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F07%2F21%2Fasian-negritos-are-not-one-population%2F&linkname=Asian%20Negritos%20are%20not%20one%20population "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F07%2F21%2Fasian-negritos-are-not-one-population%2F&linkname=Asian%20Negritos%20are%20not%20one%20population "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F07%2F21%2Fasian-negritos-are-not-one-population%2F&linkname=Asian%20Negritos%20are%20not%20one%20population "Email")[](https://www.addtoany.com/share)
