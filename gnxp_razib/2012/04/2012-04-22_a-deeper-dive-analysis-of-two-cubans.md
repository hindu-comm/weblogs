+++
title = "A deeper dive analysis"
full_title = "A deeper dive analysis of two Cubans"
date = "2012-04-22"
upstream_url = "https://www.gnxp.com/WordPress/2012/04/22/a-deeper-dive-analysis-of-two-cubans/"

+++
Source: [here](https://www.gnxp.com/WordPress/2012/04/22/a-deeper-dive-analysis-of-two-cubans/).

A deeper dive analysis of two Cubans

About a week ago [I put up a post](http://blogs.discovermagazine.com/gnxp/2012/04/the-case-of-the-white-cubans/) put on an analysis of a [paper](http://www.plosgenetics.org/article/info%3Adoi%2F10.1371%2Fjournal.pgen.1002640) which reported on the ancestral make up of 50 Cubans (as well as assorted other Hispanic/Latino groups). One aspect of the paper which was somewhat notable is that 1 out of 3 Cubans were 90 percent or more European in ancestry. The notability of this is that is that 5 out of 6 Cuban Americans identify as white. That is, of European ancestry. The main caveat here is that these Cubans were sampled from New York City, and to a lesser extent the Midwest. The fact of non-European admixture in putatively white European individuals from Latin America is not surprising. Our prior expectation should be that the admixture is non-trivial, though not preponderant. For example, the majority of the white population of [Argentina has Amerindian ancestry](http://blogs.discovermagazine.com/gnxp/2012/04/the-anglosphere-exception/) (or, more precisely \~15 percent of the aggregate ancestry of Argentineans is Amerindian). At least notionally Cuba is a much more racially mixed culture than Argentina, so non-white admixture in even white Cubans is not surprising.

Based on the above paper (and the data which you can find on other Latin American whites), as well as the genotyping of two Cuban American acquaintances, I asserted that on the order of \~10 percent of the ancestry of the average white Cuban was going to be African. Naturally this prompted some objections. Some of the individuals were not too polite. I think the primary issue that I have to be honest about this is this: **I don’t really care too much about the topic on a visceral level**. Now, I’m interested in it. And the specific cases illuminate a greater whole, which comments upon various demographic and population genetic dynamics. But I don’t have a strong investment in the specific instance of the particular ancestral quanta of Cubans, or any other group really.

Second, there was some objection to punctilious attention to scientific methodology, such as representativeness and sample size. This is a serious objection in the abstract, but the reality is that a generation of genomics has been performed with lineages as unrepresentative as “Utah whites.” Science and knowledge seeking is frankly operationally an ad hoc and sloppy process, without great attention to the book of proper scientific methodology. When we don’t have much information, any extra information is often useful, so long as we keep in mind the error that this introduces into the process.

All that being said, one commenter brought to my attention [an interesting paper](http://www.biomedcentral.com/1471-2350/12/43). It reports 6 percent African ancestry in a very large population of white Havana Cubans. The main downside is that they used only 60 SNPs, as opposed to the 60,000 SNPs in the above study. Of course those 60 SNPs would be “ancestrally informative,” but at 6 percent vs. 10 percent (my prior estimate), I’m not sure that I should totally trust the precision and update my values. But I think that nevertheless this study converges upon the same qualitative result: **white Cubans, like white Latin Americans in generally, seem to usually exhibit non-trivial amounts of non-European ancestry.**

But in the interests of moving the discussion forward, the commenter who brought the above paper to my attention supplied two 23andMe genotypes of Cuban Americans: herself and her husband. I will now refer to her as “Cuba 1” and her husband as “Cuba 2.” I created a pooled data set of the following populations:

  
Utah Whites HapMap  
Mandenka HGDP  
Yoruba HapMap & HGDP  
Japanese and Chinese HGDP  
Maya HGDP  
Surui HGDP  
Gujarati HapMap  
French Basque  
Spanish populations

After merging the marker set was reduced to 200,000. This is kind of overkill for inter-continental differences, but that’s fine. I ran ADMIXTURE up to K = 7, and did PCA for 10 dimensions. All the final results can be found [here](https://docs.google.com/open?id=0B_JroKeNrmCBZ1dNUjhsM1JualE).

ADMIXTURE stopped being informative after K = 6 (Yoruba substructure started shaking out at K = 7). Here are the full results:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/04/K6_all.png?resize=579%2C565)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/04/K6_all.png?resize=579%2C565)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/04/K6_all.png)

Cuba 2 has the most African ancestry of any non-African in the sample. Additionally, note his elevated Amerindian ancestry. This is even more notable, since it is not present in the Spanish samples. The patterns are just as clear in the PCA (the two Cubans are circled).

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/04/pca_1_2_all1.png?resize=580%2C528)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/04/pca_1_2_all1.png?resize=580%2C528)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/04/pca_1_2_all1.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/04/PCA_1_2_zoomin.png?resize=573%2C519)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/04/PCA_1_2_zoomin.png?resize=573%2C519)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/04/PCA_1_2_zoomin.png)

I’ve only labeled the Spanish individuals for the second plot, which is a zoom in. The African and Amerindian ancestry of Cuba 2 is clear in the PCA and ADMIXTURE. Cuba 1 does seem to have some African ancestry…but she could just as well be a Spaniard with African ancestry via the Moorish period. I do believe that the Moors did introduce African ancestry into Spain. Why? Below are individual plots, for Basque vs. non-Basque Spaniards (with Cuba 1 and Cuba 2):

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/04/K6_individual_Spain1.png?resize=590%2C1093)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/04/K6_individual_Spain1.png?resize=590%2C1093)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/04/K6_individual_Spain1.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/04/K6_individual_Basque.png?resize=583%2C1093)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/04/K6_individual_Basque.png?resize=583%2C1093)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/04/K6_individual_Basque.png)

Overall, it looks to be that Cuba 2 is 5-10 percent non-white. Cuba 1 definitely has more non-white ancestry than the typical white American, but can arguably simply be on one range of the distribution within Spain. Further analysis of the admixture pattern on the chromosomal level would answer this question (post-Columbian admixture would not have recombined against the European genetic background as much). Neither Cuba 1 or Cuba 2 seems to have Chinese ancestry. Rather, their “Asian” in 23andMe is almost certainly Amerindian. This is definitely the case for Cuba 2. Cuba 1 looks to be the “noise” level for that component (this increases my estimate of the probability that the African admixture is old, and Moorish era, because post-Columbian admixture probably manifested in tri-raciality).

If you are a white Latin American, I invite you to send me your genotype at contactgnxp -at- gmail -dot- com. Especially if you have been told you are “pure Spanish.”

### Related Posts:

- [An algorithm is just an
  algorithm](https://www.gnxp.com/WordPress/2012/04/23/an-algorithm-is-just-an-algorithm/) - [The case of the white
  Cubans](https://www.gnxp.com/WordPress/2012/04/15/the-case-of-the-white-cubans/) - [The Anglosphere American exception
  (?)](https://www.gnxp.com/WordPress/2012/04/10/the-anglosphere-exception/) - [Three continents come together in
  Cuba](https://www.gnxp.com/WordPress/2014/07/27/three-continents-come-together-in-cuba/) - [Sex differences in ancestry in the New
  World](https://www.gnxp.com/WordPress/2009/11/25/sex-differences-in-ancestry-in-the-new-world/) - [The coincidental intersection of sociology &
  genetics](https://www.gnxp.com/WordPress/2011/04/20/the-coincidental-intersection-of-sociology-and-genetics/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F04%2F22%2Fa-deeper-dive-analysis-of-two-cubans%2F&linkname=A%20deeper%20dive%20analysis%20of%20two%20Cubans "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F04%2F22%2Fa-deeper-dive-analysis-of-two-cubans%2F&linkname=A%20deeper%20dive%20analysis%20of%20two%20Cubans "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F04%2F22%2Fa-deeper-dive-analysis-of-two-cubans%2F&linkname=A%20deeper%20dive%20analysis%20of%20two%20Cubans "Email")[](https://www.addtoany.com/share)
