+++
title = "Burmese are a bit"
full_title = "Burmese are a bit Bengali"
date = "2018-06-19"
upstream_url = "https://www.gnxp.com/WordPress/2018/06/19/south-asian-ancestry-in-southeast-asians/"

+++
Source: [here](https://www.gnxp.com/WordPress/2018/06/19/south-asian-ancestry-in-southeast-asians/).

Burmese are a bit Bengali

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/06/riversoflostfootsteps.jpeg?resize=176%2C287&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/06/riversoflostfootsteps.jpeg?resize=176%2C287&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/B0010SGQTU/geneexpressio-20/ref=as_at/?imprToken=su9S8lFghrmuhdJf.XHMzQ&slotNum=70&imprToken=y35SghEGEXIWbF1reLx1Gw&slotNum=33&imprToken=LpkHwvjD9DZhnme4GGPFmQ&slotNum=1&creativeASIN=0981519423&linkCode=w61&imprToken=WvNSQCwEIP9qt7KZM0qiUA&slotNum=55)About ten years ago I read the book [The River of Lost Footsteps: Histories of Burma](https://www.amazon.com/exec/obidos/ASIN/B0010SGQTU/geneexpressio-20/ref=as_at/?imprToken=su9S8lFghrmuhdJf.XHMzQ&slotNum=70&imprToken=y35SghEGEXIWbF1reLx1Gw&slotNum=33&imprToken=LpkHwvjD9DZhnme4GGPFmQ&slotNum=1&creativeASIN=0981519423&linkCode=w61&imprToken=WvNSQCwEIP9qt7KZM0qiUA&slotNum=55). Though I have read books where Burma figures prominently (e.g., [Strange Parallels](https://www.amazon.com/exec/obidos/ASIN/0521804965/geneexpressio-20/ref=as_at/?imprToken=su9S8lFghrmuhdJf.XHMzQ&slotNum=70&imprToken=y35SghEGEXIWbF1reLx1Gw&slotNum=33&imprToken=LpkHwvjD9DZhnme4GGPFmQ&slotNum=1&creativeASIN=0981519423&linkCode=w61&imprToken=WvNSQCwEIP9qt7KZM0qiUA&slotNum=55)), this is the only history of Burma I have read. The author is Burmese, and provide something much more than a travelogue, as might have been the case if he was of Western background. By chance over the past month or so I’ve been in contact with the author, who made a few inquiries as to the genetics of his own family (he came with genotypes in hand). But this brought us to the issue of the genetics of the Burmese people, and their position in the historical-genetic landscape.

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/03/strange_parallel.jpeg?resize=183%2C275&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/03/strange_parallel.jpeg?resize=183%2C275&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/0521804965/geneexpressio-20/ref=as_at/?imprToken=Bots5H5CqJLMH73q0KjSzA&slotNum=2&imprToken=su9S8lFghrmuhdJf.XHMzQ&slotNum=70&imprToken=y35SghEGEXIWbF1reLx1Gw&slotNum=33&imprToken=LpkHwvjD9DZhnme4GGPFmQ&slotNum=1&creativeASIN=0981519423&linkCode=w61&imprToken=WvNSQCwEIP9qt7KZM0qiUA&slotNum=55)The author of [The River of Lost Footsteps](https://www.amazon.com/exec/obidos/ASIN/B0010SGQTU/geneexpressio-20/ref=as_at/?imprToken=su9S8lFghrmuhdJf.XHMzQ&slotNum=70&imprToken=y35SghEGEXIWbF1reLx1Gw&slotNum=33&imprToken=LpkHwvjD9DZhnme4GGPFmQ&slotNum=1&creativeASIN=0981519423&linkCode=w61&imprToken=WvNSQCwEIP9qt7KZM0qiUA&slotNum=55)reminded me of something that’s curious about Southeast Asia: **its Indic influences tend to be from the*south*of the subcontinent.** In particular, the native scripts derive from a [South Indian](https://en.wikipedia.org/wiki/Pallava_script) parent. Could genetics confirm this connection as well? Also, could genetics give some insights as to the timing of admixture/gene-flow?

In theory, yes.

I had a lot of Southeast Asian datasets to play with, and did a lot of pruning to remove outliers (e.g., people with obvious recent Chinese ancestry). First, comparing them to Bangladeshis it seems that even without local ancestry tract analysis that Burmese and Malays have more varied, and so likely recent, exogenous ancestry than Bangladeshis. At least this is evidence on the PCA plot, where these two groups exhibit strong admixture clines toward South Asians.

![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/06/burma1.png?resize=625%2C550&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/06/burma1.png?resize=625%2C550&ssl=1)

But what about the question of Southeast Asian affinities? This needs deeper analysis. Three-population tests, which measure admixture with outgroups when compared to a dyad of populations which are modeled as a clade, can be informative.

|              |               |               |              |          | |-------------:|--------------:|--------------:|-------------:|---------:| | **Outgroup** |      **Pop1** |      **Pop2** |       **f3** |    **z** | |  Bangladeshi |        Telugu |    Cambodians |  -0.00183999 | -46.3322 | |  Bangladeshi |        Telugu |           Han |  -0.00220121 |  -46.046 | |        Burma |        Telugu |           Han |  -0.00406071 | -51.0018 | |        Burma |           Han |   Bangladeshi |  -0.00348186 | -49.1398 | |        Burma |           Han | Punjabi_ANI_2 |  -0.00418193 | -47.2351 | |   Cambodians |        Telugu |          Viet |  -0.00126923 |   -16.91 | |   Cambodians | Punjabi_ANI_2 |          Viet |  -0.00129881 | -15.6039 | |   Cambodians |   Bangladeshi |          Viet | -0.000970022 | -14.5642 | |        Malay |        Igorot |        Telugu |  -0.00249795 |  -18.758 | |        Malay |        Igorot |   Bangladeshi |  -0.00223454 | -18.5212 | |        Malay |        Igorot | Punjabi_ANI_2 |  -0.00250732 | -18.3027 | |        Malay |        Igorot |    Cambodians |  -0.00107817 | -16.6214 | |         Viet |           Han |    Cambodians | -0.000569337 | -13.1139 |

Bangladeshis show strong signatures with both Cambodians and Han. This is in accordance with earlier analysis which suggests Austro-Asiatic and Tibeto-Burman contributions to the “East Asian” element of Bengali ancestry. The Burmese always have Han ancestry, with a South Asian donor as well. This aligns with other PCA analysis which shows the Burmese samples skewed toward Han Chinese. Burma is a compound of different ethnic groups. Some are Austro-Asiatic. The Bamar, the core “Burman” group, have some affinities to Tibetans. And the Shan are a Thai people who are relatively late arrivals.

Cambodians have a weaker admixture signature and are paired with a South Asian group and their geographic neighbors the Vietnamese. The Malays are similar to Cambodians but have the Igorot people from the Philippines as one of their donors. And finally, not surprisingly the Vietnamese show some mixture between Han-like and Cambodian-like ancestors.

Further PCA analysis shows that while Cambodians and Malays tend to skew somewhat neutrally to South Asians (the recent Indian migration to Malaysia is mostly Tamil), the Burmese are shifted toward Bangladeshis:

![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/06/BURMA2.png?resize=625%2C550&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/06/BURMA2.png?resize=625%2C550&ssl=1)

![Click to enlarge](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/06/SEASup_htm_2ddabbd4-1.png?resize=300%2C620&ssl=1)

Finally, I ran some admixture analyses.

First, I partitioned the samples with an **unsupervised set of runs** (K = 4 and K = 5). In this way I obtained reified reference groups as follows:

“Austronesians” (Igorot tribesmen from the Philippines)  
“Austro-Asiatic” (a subset of Cambodians with the least exogeneous admixture)  
“North Indians” (Punjabis)  
“South Indians” (A subset of middle-caste Telugus highest on the modal element in South Indians)  
“Han” (a proxy for “northern” East Asian)

The results are mostly as you’d expect. In line with three-population tests, the Vietnamese are Han and Austro-Asiatic. More of the former than latter. There is a minor Austronesian component. Notice there is no South Asian ancestry in this group.

In contrast, Cambodians have low levels of both North and South Indian. These out sample Cambodians are still highly modal for Austro-Asiatic though.

Malays are more Austro-Asiatic than Austronesian, which might surprise. But the Igorot samples are highly drifted and distinct. I think these runs are underestimating Austronesian in the Malays. Notice that some of the Malays have South Asian ancestry, but a substantial number do not. This large range in admixture is what you see in PCA as well. I think this strongly points to the fact that Malays have been receiving gene-flow from India recently, as it is not a well mixed into the population.

The Bangladeshi outgroup is mostly a mix of North and South Indian, with a slight bias toward the latter. No surprise. As I suggested earlier you can see that the Bangladeshi samples are hard to model as just a mix of Burmese with South Asians. The Austro-Asiatic component is higher in them than the Burmese. This could be because Burma had recent waves of northern migration (true), and, eastern India prior to the Indo-Aryan expansion was mostly inhabited by Austro-Asiatic Munda (probably true). That being said, the earlier analysis suggested that the Munda cannot be the sole source of East Asian ancestry in Bengalis.

Finally, every single Burmese sample has South Asian ancestry. Much higher than Cambodians. And, there is variance. I think that leads us to the likely conclusion that Burma has been subject to continuous gene-flow as well as recent pulses of admixture from South Asia. The variation in South Asian ancestry in the Burmese is greater than East Asian ancestry in Bengalis. I believe this is due to more recent admixture in Burmese due to Britishcolonial Indian settlement in that country.

**The cultural and historical context of this discussion is the nature of South Asian, Indic, influence, on Southeast Asia**. One can not deny that there has been some gene-flow between Southeast Asia and South Asia. In prehistoric times it seems that Austro-Asiatic languages moved from mainland Southeast Asia to India. More recently there is historically attested, and genetically confirmed, instances of colonial Indian migration. But, the evidence from Cambodia suggests that this is likely also ancient, as unlike Malaysia or Burma, **Cambodia did not have any major flow of Indian migrants during the colonial period**. One could posit that perhaps the Cambodian Indian affinity is a function of “Ancestral South Indian.” But the Cambodians are not skewed toward ASI-enriched groups in particular. And, I know for a fact that appreciable frequencies of R1a1a exist within the male Khmer population (this lineage is common in South Asia, especially the north and upper castes).

As far as Burma goes, I think an older period of South Indian cultural influence, and some gene-flow seems likely. But, with the expansion of Bengali settlement to the east over the past 2,000 years, more recent South Asian ancestry is probably enriched for that ethnolinguistic group.

I’m going to try and follow-up with some ancestry tract analysis….

### Related Posts:

- [Myanmar/Burma
  links](https://www.gnxp.com/WordPress/2007/09/27/myanmar-burma-links/) - [Democralotry's
  discontents](https://www.gnxp.com/WordPress/2014/07/07/democralotrys-discontents/) - [Rohingya unmasking complexity in a world we want
  simple](https://www.gnxp.com/WordPress/2017/09/03/rohingya-unmasking-complexity-in-a-world-we-want-simple/) - [To know the whole is to know the
  elements](https://www.gnxp.com/WordPress/2015/04/02/to-know-the-whole-is-to-know-the-elements/) - [The confusions of genetic
  relatedness](https://www.gnxp.com/WordPress/2010/09/12/the-confusions-of-genetic-distance/) - [Open Thread,
  11/26/2019](https://www.gnxp.com/WordPress/2019/11/26/open-thread-11-26-2019/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F06%2F19%2Fsouth-asian-ancestry-in-southeast-asians%2F&linkname=Burmese%20are%20a%20bit%20Bengali "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F06%2F19%2Fsouth-asian-ancestry-in-southeast-asians%2F&linkname=Burmese%20are%20a%20bit%20Bengali "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F06%2F19%2Fsouth-asian-ancestry-in-southeast-asians%2F&linkname=Burmese%20are%20a%20bit%20Bengali "Email")[](https://www.addtoany.com/share)
