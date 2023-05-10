+++
title = "The power of one"
full_title = "The power of one"
date = "2011-05-26"
upstream_url = "https://www.gnxp.com/WordPress/2011/05/26/the-power-of-one-nubian-that-is/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/05/26/the-power-of-one-nubian-that-is/).

The power of one (Nubian that is)

[Maju](https://forwhattheywereweare.blogspot.com/2011/05/sudanese-autosomal-genetics.html) pointed me to a new paper on the genetics of Sudanese today. My interest was piqued, then not so much when I looked more closely. [Genetic variation and population structure among Sudanese populations as indicated by the 15 Identifiler STR loci](http://www.investigativegenetics.com/content/2/1/12/abstract):

> **Background**  
> There is substantial ethnic, cultural and linguistic diversity among > the people living in east Africa, Sudan and the Nile Valley. The > region around the Nile Valley has a long history of succession of > different groups, coupled with demographic and migration events, > potentially leading to genetic structure among humans in the region. >
> **Results**  
> We report the genotypes of the **15 Identifiler microsatellite markers > for 498 individuals from 18 Sudanese populations** representing > different ethnic and linguistic groups. The combined power of > exclusion (PE) was 0.9999981, and the combined match probability was 1 > in 7.4 1017. The genotype data from the Sudanese populations was > combined with previously published genotype data from Egypt, Somalia > and the Karamoja population from Uganda. **The Somali population was > found to be genetically distinct from the other northeast African > populations. Individuals from northern Sudan clustered together with > those from Egypt, and individuals from southern Sudan clustered with > those from the Karamoja population.** The similarity of the Nubian and > Egyptian populations suggest that migration, potentially > bidirectional, occurred along the Nile river Valley, which is > consistent with the historical evidence for long-term interactions > between Egypt and Nubia. >
> **Conclusion**  
> We show that despite the levels of population structure in Sudan, > standard forensic summary statistics are robust tools for personal > identification and parentage analysis in Sudan. **Although some > patterns of population structure can be revealed with 15 > microsatellites, a much larger set of genetic markers is needed to > detect fine-scale population structure in east Africa and the Nile > Valley.**

The upside: nearly 500 individuals from a huge range of ethnic groups in Sudan. This is the level of population coverage you’d want. Most of the ethnic groups cover the sample size range from 10 to 50. The downside: only 15 microsatellite markers. About the same number as in the [study which I critiqued earlier this week](http://blogs.discovermagazine.com/gnxp/2011/05/proper-methods-and-false-results/). This is just not a huge number. The authors did try very hard to prune the marker set to be ancestrally informative on this scale, but I think it’s pretty obvious that there are major shortcomings in their analysis. 15 STRs is probably useful for inter-continental genetic variation, but not for intra-continental differences. The paper is open access so you can read the whole thing, but I want to highlight a speculation which they offer based on their results:

> The number of unique alleles (Figure 2B) was greatest in the Somali > population, and and in the population structure analyses (Figure 5), > the Somali population grouped separately from other populations. > Because the Somali population is separated both geographically and > linguistically from the other populations included in our study, it is > not surprising that it is also genetically distinct. **It is possible > that the Bantu expansion from West Africa had a stronger effect on the > region of the Horn of Africa, where Somalia is located, compared with > the region where Sudan is located.** For example, the languages in > Somalia belong to two major linguistic families, the Afro-Asiatic and > Niger-Congo, whereas Nilo-Saharan is absent and the Bantu Swahili > language is one of the major languages in Somalia (Ethnologue \[1\]). > Another explanation could be that the Somali population is of both > Eurasian and sub-Saharan origin, as suggested by a recent study > \[33\], potentially explaining the differentiation of this population > from some east African groups, although many of the Sudanese > populations, such as Arabs and the Beja, may also have mixed Eurasian > and sub-Saharan origin.

I think what is more possible is that as hard as they tried these markers don’t give a insightful picture at the fine scale. By insightful, I mean that there aren’t too many results I’d trust beyond what you’d already intuitively accept. **The genome bloggers have already shown that there’s hardly any Bantu admixture in the Horn of Africa.**

But the main reason I’m talking about this paper is this: **I have one Nubian sample in [the African Ancestry Project](http://africanancestryproject.org/).** Just one. As opposed to 34 in this paper. But my N = 1 makes me really wary of the results from this paper based on 15 STRs. How can my one sample make me wary of the results from 34? Because I have nearly 1 million SNPs from 23andMe’s v3 raw data! So there you have it. The number 1 million isn’t really that big of a deal. I’d be wary if I had 50,000 SNPs (I came up with the number based on running a lot of ADMIXTURE on African populations).

So this is what I did. I took my data set from the African Ancestry Project, pruned a lot of the populations, added Egyptians, and limited AAP members to Ethiopians, Somalis, a Yemeni, and my Nubian. I ran them from K = 2 to K = 12 with \~40,000 SNPs. You can find all of the [results for this run at the African Ancestry Project website](http://africanancestryproject.org/?p=47). But here I want to focus on K = 8. Below is the plot for the reference populations, and then the individual plot for all the Egyptians, and AAP project members who are Ethiopian, Somali, then the Nubian (AF070), and finally the Yemeni (AF091). The Nubian individual is highlighted with a red line, while I’ve placed a blue line underneath the Egyptians. In case you are curious, AF004, AF005, AF006, and AF034 are Somali. AF023 and AF064 are Oromo Ethiopian. AF036 is 7/8 Eritrean and 1/8 Italian, while AF001 is 100% Eritrean.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/k8a.png?resize=600%2C600)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/k8a.png?resize=600%2C600)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/k8a.png)

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/k8i.png?resize=600%2C600)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/k8i.png?resize=600%2C600)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/k8i.png)

**If the Nubian sample I have is representative it seems plausible that Nubians do have a minor component of Egyptian ancestry, but that Nubians are by an large a more conventional East African population**. And contrary to the speculation in the paper, Somalis have surprisingly little ancestry from the Bantu expansion. I’m a lot more confident of this assertion than about the nature of Nubians from my one sample, you see this pattern of Bantu exclusion from Afro-Asiatic groups in Ethiopia and Somalia modulating the parameters every which way. I’d bet \$250 that Sudanese as a whole don’t have less Bantu admixture than the Somalis (both groups have a little affinity, perhaps more through common ancestry with Bantu groups than real Bantu expansion ancestry, despite the existence of a Bantu ex-slave class in Somalia). I’d bet \$100 that my Nubian *is* representative and that Nubians don’t have much as gene flow from Egypt as this paper infers.

The best thing about people releasing genome data is that you can actually go beyond the armchair when it comes to critiquing a paper.

### Related Posts:

- [South seas history through
  genes](https://www.gnxp.com/WordPress/2008/01/18/south-seas-history-through-genes/) - [The population genetic structure of Northeast
  Africa](https://www.gnxp.com/WordPress/2017/08/26/northeast-africa/) - [Back migration into Africa by
  Eurasians](https://www.gnxp.com/WordPress/2021/12/21/back-migration-into-africa-by-eurasians/) - [The genetic palimpsest of the Horn of
  Africa](https://www.gnxp.com/WordPress/2019/01/10/the-genetic-palimpsest-of-the-horn-of-africa/) - [African genetic
  structure](https://www.gnxp.com/WordPress/2009/04/30/african-genetic-structure/) - [The Egyptians
  live](https://www.gnxp.com/WordPress/2016/10/28/the-egyptians-live/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F05%2F26%2Fthe-power-of-one-nubian-that-is%2F&linkname=The%20power%20of%20one%20%28Nubian%20that%20is%29 "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F05%2F26%2Fthe-power-of-one-nubian-that-is%2F&linkname=The%20power%20of%20one%20%28Nubian%20that%20is%29 "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F05%2F26%2Fthe-power-of-one-nubian-that-is%2F&linkname=The%20power%20of%20one%20%28Nubian%20that%20is%29 "Email")[](https://www.addtoany.com/share)
