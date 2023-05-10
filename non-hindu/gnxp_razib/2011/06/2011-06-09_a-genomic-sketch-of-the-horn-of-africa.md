+++
title = "A genomic sketch of the"
full_title = "A genomic sketch of the Horn of Africa"
date = "2011-06-09"
upstream_url = "https://www.gnxp.com/WordPress/2011/06/09/a-genomic-sketch-of-the-horn-of-africa/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/06/09/a-genomic-sketch-of-the-horn-of-africa/).

A genomic sketch of the Horn of Africa

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/Iman_model.jpg?resize=200%2C362)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/Iman_model.jpg?resize=200%2C362)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/Iman_model.jpg)  
Iman, a Somali model

Since I started up the [African Ancestry Project](http://africanancestryproject.org/) one of the primary sources of interest has been from individuals whose family hail for Northeast Africa. More specifically, the Horn of Africa, Ethiopia, Eritrea, and Somalia. The problem seems to be that 23andMe’s “ancestry painting” algorithm uses West African Yoruba as a reference population, and East Africans are often not well modeled as derivative of West Africans. So, for example, the Nubian individual who I’ve analyzed supposedly comes up to be well over 50% “European” in ancestry painting. Then again, I”m 55-60% “European” as well according that method! So we shouldn’t take these judgments to heart too much. Obviously something was off, and thanks to Genome Bloggers like [Dienekes Pontikos](https://dodecad.blogspot.com/) we know what the problem was: **the populations of the Horn of Africa have almost no distinctive “Bantu” element to connect them with West Africans like the Yoruba**. Additionally, a closer inspection shows that the “Eurasian” component present in these populations is very specific as well, almost totally derived from Arabian-like sources. When breaking apart the West Eurasian populations it is no surprise that Northern Europeans and Arabians are among the most distant pairs, even excluding recent Sub-Saharan African admixture. The HapMap Utah European American sample and the Nigerian Yoruba are very suboptimal for people with eastern African background. In contrast, African Americans are a mixture of West Africans and Northern Europeans, so the ancestry painting algorithm has nearly perfect reference populations for them. The results for African Americans may not be very detailed and rich, but they’re probably pretty accurate at the level of grain which they’re offering results.

Though I’m happy to give people of Northeast African ancestry more detailed results than 23andMe, one of my motivations for the [African Ancestry Project](http://africanancestryproject.org/) was to obtain a data set which would allow me to explore the genomic variation in the east of Africa myself. This region is a strong candidate for “source” populations for non-Africans within the last 100,000 years, and, it seems to have experienced rapid population turnover within the last 2,000-3,000 years. My data set is not particularly adequateto my ambitions, yet. But I do now have 5 unrelated Somalis. To my knowledge there hasn’t much exploration of Somali genomics using thick-marker SNP chips, so why not? N = 5 is better than N = 0 in these cases of extreme undersampling.

Before I proceed to methods and results, I want to note that I put up most of my files [here](https://docs.google.com/leaf?id=0B8Tdg8RZEWOONDM5OWFlOGUtM2FiYy00MTAwLWFjZjMtMDU4M2E4ODY5MzYy&hl=en_US&authkey=CKTitdYJ). It’s a \~25 MB compressed folder with images, spreadhseets, as well as raw output from ADMIXTURE and EIGENSOFT. I hope readers will take this as an invitation to poke around themselves.

  
Since my focus was on the Horn of Africa the coverage of populations is relatively constrained compared to what I normally run. From the HapMap I took the Yoruba, Masai, and Luhya. I renamed Masai “Nilotic Kenya” and the Luhya “Bantu Kenya.” The [Behar et al.](http://www.nature.com/nature/journal/v466/n7303/abs/nature09103.html) data set has a fair number of Ethiopians, gentiles and Jews. A reader helpfully labelled the various ethnicities by ID. I was going to do that myself, but because this tedious work was done for me I felt much more motivated to produce something instead of putting this task off! From the Behar et al. I also took some Arab populations, as well as Georgians, Lithuanians and Belorussians. I combined the two latter populations into “Baltic.” Syrians and Jordanians were converted to “Levantine” in the bar plots. I left Saudis, Yemenis, and Yemeni Jews disaggregated. Finally, I added some individuals from the AAP: **all the people from the Horn of Africa who are unmixed in ancestry, as well as my Nubian individual.** In the display that follows AAP members are combined with the ethnic groups which are appropriate in Behar et al.: Oromos, Amharas, and Tigray. Ethiopian Jews (the Beta Israel) I left as is. To mix it up I also brought over the Sandawe from Henn et al. The Somalis are all from AAP. They do not seem related (close relatives generally form their own cluster).

I tried to balance my populations in an ad hoc fashion. I took only \~30 Yoruba, but decided to add in more Masai, because they seemed to be a mixed population rather than a reference, and I wanted to flesh out their variation. I removed individuals who were closely related as per Zack Ajmal’s findings in his review of his reference data sets. After combining the data sets I was left with \~210,000 SNPs, with less than 0.1% missing. I ran this from K = 2 to K = 8 in ADMIXTURE, and, I also generated the top six independent dimensions of genetic variation in EIGENSOFT. I also took the Fst values from ADMIXTURE of the inferred ancestral populations and generated MDS representations of the genetic distances (though the original file can be found in the attached folder).

There are several different types of plots below. The MDS and PCA should be rather straightforward. But a little explanation for the ADMIXTURE bar plots. There are three for every K. First, average results by population. Second, a fine-grained display of all the individuals from all the populations. Third, a fine-grained display of some populations of interest. **Please note that in the second set of plots I don’t label all the individuals by population, since it would unreadable.** But they go alphabetically, so you should be able to see where populations start, and where they end.

Before I you even look at the results and we discuss them, there is one clear issue which jumps out: **there are closely related individuals or clans in the Masai data set which I need to remove in future runs.** Though these individuals hogged up higher K’s it didn’t effect the relationships across other populations, so I decided to publish this now before refining it for the future. It’s a learning experience. You can see that these individuals form their own clusters in the MDS and PCA as well. At least the problem reoccurs systematically using different methodologies.

(note: some of the images are larger than shown, so if you want to see better labels for the fine-grained plots, **get the image URL and look at it separately**)

\[zenphotopress album=287 sort=sort_order number=50\]





The fact that the Masai “break down” at K = 6 is really problematic, as there’s information that’s probably lost here. But several immediate observations:

1\) The Somalis, like the Ethiopian groups, show almost no impact from the Bantu expansion. This is contrast to the one Nubian individual, who may have more West African ancestry through intermediate groups, or through direct contact with Bantus who were enslaved and brought to Sudan.

2\) When you break apart West Eurasian ancestry the Ethiopian and Somali groups have their contribution almost exclusively from an ancestral component in southern Arabia. This makes some sense because of geography, but when you look at the fractions of “northern” admixture even among Yemeni Jews the proportions are not reflected among the Horn of Africa groups. One hypothesis which is consistent with this might be that the admixture event between the Arabian-like group occurred at a time when south Arabians were more genetically isolated and distinct from populations to the north. I suspect this is almost certainly going to be true before the camel, let alone Islam. Interestingly, just as the Nubian individual has more West African affinities, they also have more European affinities. The Nubian individual’s ancestry is simply more cosmopolitan than that of Ethiopians and Somalis, which is not historically that surprising.

3\) There is a rough rank order of admixture estimates. In terms of Africanness it goes from Somali \> Oromo \> Beta Israel \~ Amhara \> Tigray. The sample sizes are small though, so we should be cautious. The Amhara seem to vary the most. One might suspect that the Amhara, being the traditional core ethnicity of Ethiopia of late, assimilated other groups. If you look at the PCA the Somali actually look the most “East African” of the groups on PC 2. Note also the linear pattern of distribution other Ethiopians and the Masai toward Arabians and Bantu respectively. This is suggestive of some sort ancient admixture event between an East African substrate and other populations. I will label this population “Ancestral East Africans” (AEA).

4\) The relationship of the Sandawe to the other groups is interesting. It seems clear that the Sandawe are related to the AEA, but are somewhat at a remove. Note that a “Sandawe” component is often found in low proportions outside of the Sandawe across East Africa. While the Ethiopians and Somalis do not have a Bantu aspect to their ancestry, they may have an “Ancestral Sandawe” (AS) one.

I don’t want to say more until I get the Masai data set fixed (and I might make recourse to some of Dienekes’ “tricks,” as well as supervised runs). But overall I would say that the ethnogesis of the Semitic and Cushitic people of the Horn of Africa pre-dates the Bantu expansion. I will do some more playing with this, but they do not seem to generate a “Ethiopian-Somali” cluster so easily as South Asians do. This may be because they are never numerous in any of these analyses. Or, it may be due to the possibility that the admixture event was recent enough that the underlying populations are not as obscured as amongst South Asians. I lean toward the latter, for now. As in South Asia, I do not think that the ethnogenesis of the families of Ethiopian peoples is quite a “one off” admixture event. It is suggestive that you have two major language families, Semitic and Cushitic, in this region.

*Image credit: [Wikimedia](https://en.wikipedia.org/wiki/File:Iman_(model).jpg)*

### Related Posts:

- [ADMIXTURE, African Ancestry Project, and confirmation
  bias](https://www.gnxp.com/WordPress/2011/05/02/admixture-african-ancestry-project-and-confirmation-bias/) - [The power of one (Nubian that
  is)](https://www.gnxp.com/WordPress/2011/05/26/the-power-of-one-nubian-that-is/) - [Modern humans in Arabia \>100,000 years
  ago](https://www.gnxp.com/WordPress/2011/11/30/modern-humans-in-arabia-100000-years-ago/) - [The non-European admixture in
  Afrikaners](https://www.gnxp.com/WordPress/2021/07/14/the-non-european-admixture-in-afrikaners/) - [In Africa....](https://www.gnxp.com/WordPress/2005/08/11/in-africa/) - [My Goodness My
  Guinea-ness?](https://www.gnxp.com/WordPress/2011/04/01/my-goodness-my-guinea-ness/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F06%2F09%2Fa-genomic-sketch-of-the-horn-of-africa%2F&linkname=A%20genomic%20sketch%20of%20the%20Horn%20of%20Africa "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F06%2F09%2Fa-genomic-sketch-of-the-horn-of-africa%2F&linkname=A%20genomic%20sketch%20of%20the%20Horn%20of%20Africa "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F06%2F09%2Fa-genomic-sketch-of-the-horn-of-africa%2F&linkname=A%20genomic%20sketch%20of%20the%20Horn%20of%20Africa "Email")[](https://www.addtoany.com/share)
