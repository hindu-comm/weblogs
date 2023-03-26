+++
title = "Flavors of AfroAsiatic"
full_title = "Flavors of AfroAsiatic"
date = "2011-06-10"
upstream_url = "https://www.gnxp.com/WordPress/2011/06/10/flavors-of-afro-asiatic/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/06/10/flavors-of-afro-asiatic/).

Flavors of Afro-Asiatic

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/800px-Afroasiatic-en.svg_.png?resize=250%2C393)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/800px-Afroasiatic-en.svg_.png?resize=250%2C393)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/800px-Afroasiatic-en.svg_.png)In the [post yesterday](http://blogs.discovermagazine.com/gnxp/2011/06/a-genomic-sketch-of-the-horn-of-africa/) I reported what was generally known about the Horn of Africa, that its populations seem to lie between those of Sub-Saharan African and Eurasia genetically. This is totally reasonable as a function of geography, but there are also suggestions that this is not simply a function of [isolation by distance](http://blogs.discovermagazine.com/gnxp/2011/06/man-at-bab-el-mandeb/) (i.e., populations at position 0.5 on the interval 0.0 to 1.0 would presumably exhibit equal affinities in both directions due to gene flow). For example, you observe the almost total lack of “Bantu” genetic influence on the Semitic and Cushitic populations of the Horn of Africa, and the lack of Eurasian influence in groups to the south and west of the Horn *except* to some extent the Masai.

Tacking horizontally in terms of discipline, over the past few generations there has been a veritable cottage industry making the case for the recent origin of many [ethno-linguistic](http://www.harappadna.org/2011/06/caste-is-not-ancestrally-arbitrary/) populations through a processof cultural self-creation. Clearly there are many cases of this, some of them studied in depth by anthropologists (e.g., the shift from Dinka to Nuer identity). **But there has been an unfortunate tendency to over-generalize in this direction.** In some ways this is peculiar insofar as these models presuppose the infinite plasticity of culture without observing the sharp and strong norms which those very same phenomenon can enforce. The [genetic isolation of non-Muslims](http://blogs.discovermagazine.com/gnxp/2011/01/the-assyrians-and-jews-3000-years-of-common-history/) in the Middle East after the rise of Islam seems rather well validated by the evidence from genomics. The norms of both Muslims and non-Muslims strongly biased them toward endogamy, and nature of Islamic hegemony and domination was such that Muslims were the ones who were likely to have cosmopolitan affinities with the “Islamic international.” In contrast, non-Muslim minorities began a long process of involution after the Islamic Arab conquests, only disrupted in the past century by emigration and to a lesser extent emancipation.

So back to the Horn of Africa. The vast majority of the people of the Horn of Africa speak an Afro-Asiatic language. Arabic and Hebrew are the most famous members of this group, but it is a very broad classification, ranging from the dialects of the Berbers in the Maghreb all the way to ancient Akkaddian. There are two large subfamilies of particular note and interest here: **Semitic and Cushitic.** The map above shows the distribution within the Horn of Africa. One can “quick & dirty” summarize the pattern here by observing that Semitic languages in Ethiopia tend to be concentrated in the north-central Christian highlands, while Cushitic is found everywhere else. Additionally, there is the confluence between religion and ethnicity, as there are Cushitic Muslims (Somalis, Afar, etc.) and Cushitic Christians (many Oromo, etc.). From what I can gather many Cushitic social and political elites have had a tendency toward assimilating into an Amhara Semitic identity (Haile Selassie’s mother was a [Muslim Oromo](https://en.wikipedia.org/wiki/Haile_Selassie_I)). We could therefore generate a possible model where Semitic langauges arrived late to Ethiopia and spread through elite emulation, so the difference between Semitic and Cushitic peoples should be marginal in the genomic dimension (such as the marginal differences between Hausa and Yoruba in Nigeria). Or, we could posit that the Semitic element is distinctive from a pre-existent Cushitic substratum.

**To make a long story short by running more ADMIXTURE with a Horn of Africa centered data set I have discerned that one *can* actually differentiate Cushitic and Semitic elements in the Horn and tentatively identify them with different ancestral components.** First, the technical details….

  
I began with the data set I started with in the runs I [posted](http://blogs.discovermagazine.com/gnxp/2011/06/a-genomic-sketch-of-the-horn-of-africa/) yesterday. Strange outliers in the Masai were removed. These are a few sets of individuals who “fix” for minority ancestral components. This is a tell that there’s structure within the Masai being picked up, but more like distantly related individuals, not ethnic level differences. After running this I noticed that a lot of the same then popped up in the non-Jewish Yemeni and Saudi samples. To some extent this is like “whack-a-mole.” If you remove one problem others simply pop out of the woodwork. So I removed all the non-Jewish Yemenis and Saudis. The number of markers remained the same, 210,000 SNPs.

There were still a few issues with outliers, especially with the Bantu Kenya, and to a lesser extent the Levantine samples. But at this point I decided to go with it, since these are marginal to the story of the Horn of Africa in any case. I stated yesterday that in general Horn of Africa populations don’t present their own clusters, but are a composite of others, mostly East African and Arabian. After I removed some of the spurious Masai components and ran ADMIXTURE up to K = 10 I did finally get a Horn of Africa cluster, “HoAc”. Additionally, I also found that you can see systematic differences between Cushitic Oromo and Somalis, and the Semitic Ahmara, Ethopian Jews, and Tigray.

Below are bar plots of K = 7 and K = 9. The lower K’s aren’t too different from what I posted yesterday, while K = 8 and K = 10 has too many minor components. I’ve posted only fine-grained and Horn of Africa focused plots, instead of the more general summary plots which show average ancestral quanta. Also, below these I’ve posted two dimensional representations of genetic distances between inferred ancestral groups for K = 7 and K = 9. I’ve removed several components though, in the case of one because it was clearly a spurious “extended family” cluster, and in some cases to better visualize relationships.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/K7slice.png?resize=600%2C608)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/K7slice.png?resize=600%2C608)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/K7slice.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/K7e.png?resize=600%2C602)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/K7e.png?resize=600%2C602)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/K7e.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/K9slice.png?resize=600%2C600)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/K9slice.png?resize=600%2C600)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/K9slice.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/K9e.png?resize=600%2C600)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/K9e.png?resize=600%2C600)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/K9e.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/FstMDSK7a.png?resize=576%2C640)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/FstMDSK7a.png?resize=576%2C640)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/FstMDSK7a.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/MDSFstK7b.png?resize=567%2C630)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/MDSFstK7b.png?resize=567%2C630)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/MDSFstK7b.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/MDSFst9a.png?resize=568%2C630)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/MDSFst9a.png?resize=568%2C630)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/MDSFst9a.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/MDSFst9b.png?resize=568%2C631)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/MDSFst9b.png?resize=568%2C631)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/MDSFst9b.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/MDSFst9c.png?resize=566%2C625)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/MDSFst9c.png?resize=566%2C625)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/MDSFst9c.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/MDSFst9d1.png?resize=573%2C623)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/MDSFst9d1.png?resize=573%2C623)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/MDSFst9d1.png)

To cut to the chase, it looks like all Horn of Africa populations share a HoAc base, which one might term “Cushitic,” though that is not totally accurate. On top of that base you see differences based on language family. The Semitic speaking groups have an ancestral component which is identical to the one fixed in Yemeni Jews, while the Cushitic speaking ones tend to lack this. But observe that the Semitic speaking populations generally have the component found in the Cushitic speaking groups, and especially the Somalis in which it often fixes. This is why I put the sequence of language-population expansions so that the Semitic is overlain upon a Cushitic base. Additionally, there does seem to be admixture from Nilotic groups into Ethiopian, but not Somali, populations. This is most consistent and evident in the Oromo, and where an isolation by distance model seems plausible, as the Oromo are geographically the most likely to have interacted with Nilo-Saharan populations and the Somali the least.

Finally, please keep in mind that if the Somalis are 100% cluster X, that does not mean that the Somalis are derived from some real homogeneous ancestral cluster X. These ADMIXTURE components are very interesting in helping to flesh out relationships horizontally across populations today, but we should be cautious about what they can tell us about relationships vertically in terms of how populations emerged over time. A thoroughly admixed group can break out into its own distinctive cluster if it exhibits a level of internal homogeneity and the ancestral “reference” populations themselves no longer exist. This seems to be what has occurred in South Asia, where certain groups shake out as “100% South Asian,” but themselves on the deeper genomic level seem to be stabilized admixtures of ancient fusions between two ancestral groups which were very diverged. A South Asian analogy to the Horn of Africa might lead us to infer that Somalis are the equivalent of these populations, where they lack admixture with more recent arrivals to the region after the initial admixture event between “Ancestral East Africans” (AEA) the Arabians of yore. This may simply be a function of geography and historical contingency, as the position of Somalis is more “sheltered” because of the quasi-peninsular nature of their region of the Horn. Additionally, Somalia is relatively dry and unsuitable for agriculture, making it perhaps less ecologically friendly than the highlands of Ethiopia to Semitic populations bringing a new agricultural toolkit.

There’s plenty more you can say, but I’ll hold off, and add a word of caution: **it is very possible that I was looking for these specific clusters and arrived at them via confirmation bias.** As I’ve noted before, if you tune ADMIXTURE’s parameters in the proper fashion you can “arrive” at the answers you want. How to protect against this? If I keep performing ad hoc runs and going by intuition, lots of repetition often helps. You naturally arrive at a sense of the underlying distribution of possibilities, can guard against anchoring upon an outlier result, because you know that it is atypical (this is though on reason that ground-breaking results are ignored, as they don’t fit the paradigm, so there’s a flip-side to this bias). I also run [cross-validation](https://en.wikipedia.org/wiki/Cross-validation_(statistics)) now and then to find the optimal number of K’s, but that *really* slows down the program, so I this is a matter of trade offs for me. I’m rather sure that the differences between Ethiopian and Somali groups are robust, because the same pattern of relationships (e.g., the Amhara tendency to resemble the Tigray more than the Somali) reoccurs over and over. But I’m not so confident about the inference I’ve drawn here about the Afro-Asiatic language families and the partitioning of the Cushitic and Semitic groups.

You can find some more files [here](https://docs.google.com/leaf?id=0B8Tdg8RZEWOOMTViOGY3NzgtNWEzNy00YzY5LWFjZjItMjlmNjA0OWQ4NzIz&hl=en_US&authkey=CJm56u4F).

*Image credit: [Wikipedia](https://en.wikipedia.org/wiki/File:Afroasiatic-en.svg)*

### Related Posts:

- [The genetic affinities of
  Ethiopians](https://www.gnxp.com/WordPress/2011/01/10/the-genetic-affinities-of-ethiopians/) - [The genetic palimpsest of the Horn of
  Africa](https://www.gnxp.com/WordPress/2019/01/10/the-genetic-palimpsest-of-the-horn-of-africa/) - [Tutsi genetics,
  ii](https://www.gnxp.com/WordPress/2011/08/31/tutsi-genetics-ii/) - [Ancient human population
  sizes](https://www.gnxp.com/WordPress/2007/12/12/ancient-human-population-sizes/) - [The sons of Ham and
  Shem](https://www.gnxp.com/WordPress/2017/07/10/the-sons-of-ham-and-shem/) - [The Fulani have an old "Berber" (?)
  element](https://www.gnxp.com/WordPress/2012/01/16/the-fulani-have-an-old-berber-element/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F06%2F10%2Fflavors-of-afro-asiatic%2F&linkname=Flavors%20of%20Afro-Asiatic "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F06%2F10%2Fflavors-of-afro-asiatic%2F&linkname=Flavors%20of%20Afro-Asiatic "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F06%2F10%2Fflavors-of-afro-asiatic%2F&linkname=Flavors%20of%20Afro-Asiatic "Email")[](https://www.addtoany.com/share)