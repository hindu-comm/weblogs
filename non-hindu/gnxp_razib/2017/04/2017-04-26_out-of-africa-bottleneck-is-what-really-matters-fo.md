+++
title = "“Out of Africa”"
full_title = "“Out of Africa” bottleneck is what really matters for mutations"
date = "2017-04-26"
upstream_url = "https://www.gnxp.com/WordPress/2017/04/26/out-of-africa-bottleneck-is-what-really-matters-for-mutations/"

+++
Source: [here](https://www.gnxp.com/WordPress/2017/04/26/out-of-africa-bottleneck-is-what-really-matters-for-mutations/).

“Out of Africa” bottleneck is what really matters for mutations

[![](https://i0.wp.com/gnxp.com/WordPress/wp-content/uploads/2017/04/pygmy1.jpg?resize=600%2C300)![](https://i0.wp.com/gnxp.com/WordPress/wp-content/uploads/2017/04/pygmy1.jpg?resize=600%2C300)](http://biorxiv.org/content/early/2017/04/26/131219)  
At least in relation to mutational load, if you read a new preprint in biorxiv, [The demographic history and mutational load of African hunter-gatherers and farmers](http://biorxiv.org/content/early/2017/04/26/131219):

> The distribution of deleterious genetic variation across human > populations is a key issue in evolutionary biology and medical > genetics. However, the impact of different modes of subsistence on > recent changes in **population size, patterns of gene flow**, and > deleterious mutational load remains to be fully characterized. We > addressed this question, by generating **300 high-coverage exome > sequences** from various populations of rainforest hunter-gatherers > and neighboring farmers from the western and eastern parts of the > central African equatorial rainforest. We show here, by model-based > demographic inference, that the effective population size of African > populations remained fairly constant until recent millennia, **during > which the populations of rainforest hunter-gatherers have experienced > a \~75% collapse and those of farmers a mild expansion, accompanied by > a marked increase in gene flow between them.** Despite these > contrasting demographic patterns, African populations display > **limited differences** in the estimated distribution of fitness > effects of new nonsynonymous mutations, consistent with purifying > selection against deleterious alleles of similar efficiency in the > different populations. This situation contrasts with that we detect in > Europeans, **which are subject to weaker purifying selection than > African populations.** Furthermore, the per-individual mutation load > of rainforest hunter-gatherers was found to be similar to that of > farmers, under both additive and recessive modes of inheritance. > Together, our results indicate that differences in the subsistence > patterns and demographic regimes of African populations have not resulted in large differences in mutational burden, and highlight the role of gene flow in reshaping the distribution of deleterious genetic variation across human populations.

There’s two major moving parts in this preprint. First, they using **phylogenomic methods to explicitly model population history**. Second, they integrated their demographic results in generation and interpreting the **distribution of mutations within the exomes of these populations.** That is, they combined phylogenomics to gain insight into population genomics, as the latter focuses more on the parameters which define variation with a population.

[![](https://i0.wp.com/gnxp.com/WordPress/wp-content/uploads/2017/04/Screenshot-2017-04-27-00.22.29.png?resize=200%2C591)![](https://i0.wp.com/gnxp.com/WordPress/wp-content/uploads/2017/04/Screenshot-2017-04-27-00.22.29.png?resize=200%2C591)](http://biorxiv.org/content/early/2017/04/26/131219)The data they worked with was from the exome. The regions of the genome which translate into genes. That’s \~30 million bases. They get really good precision due to high coverage, hitting site about 70 times. Their sample was about 300 Africans and 100 Europeans, and they got \~500,000 polymorphisms or variants for their trouble.

The populations were labeled by subsistence and provenance. The Europeans were Belgians. For the Africans they had two groups of hunter-gatherer Pymgies, and two groups of Bantu agriculturalists, sampled from western and eastern locations as you see on the map above.

The admixture plots, which separate out individuals into*K* numbers of populations break out in a way that makes sense. First, Europeans separate, and the eastern agriculturalist populations have a little bit of evidence of European-like ancestry. This is almost certainly Middle Eastern farmer, which has been found in many East African populations, and those populations which have mixed with them. Then the hunter-gathers separate from the agriculturalists. This is in line with expectation and earlier research; the hunter-gatherers of Africa seem very different from the agriculturalists, and are actually more closely related to each other than the agriculturalists in their neighboring regions.

The exception to this pattern is caused by recent gene flow, which is clearly evident above. Due to population size differences it looks like there is more agricultural ancestry in the Pygmies than vice versa. I wish that they had sampled Mbuti Pygmies. I’m told that this group has the least agricultural admixture.

But then they decided to get fancy and explicitly model demographic histories with*fastsimcoal2*. What does this do? From the [website](http://cmpg.unibe.ch/software/fastsimcoal2/) for the software:

> While preserving all the simulation flexibility of *simcoal2*, > *fastsimcoal* is now implemented under a faster continous-time > sequential Markovian coalescent approximation, allowing it to > **efficiently generate genetic diversity for different types of markers along large genomic regions**, for both present or ancient samples. It includes a parameter sampler allowing its integration into Bayesian or likelihood parameter estimation procedure. >
> *fastsimcoal* **can handle very complex evolutionary scenarios** > including an arbitrary migration matrix between samples, historical > events allowing for population resize, population fusion and fission, > admixture events, changes in migration matrix, or changes in population growth rates. The time of sampling can be specified independently for each sample, allowing for serial sampling in the same or in different populations.

The models you see that were tested are pretty simple, and they all seem plausible I suppose. Their simulations suggested that the three above scenarios, with alternative branching patterns and various gene flows, were all of equal likelihood. That is, given the models and the data that they had (4-fold synonymous sites which are likely to be neutral) you can’t distinguish which is right.

[![](https://i0.wp.com/gnxp.com/WordPress/wp-content/uploads/2017/04/phylo2.jpg?resize=175%2C230)![](https://i0.wp.com/gnxp.com/WordPress/wp-content/uploads/2017/04/phylo2.jpg?resize=175%2C230)](https://www.amazon.com/exec/obidos/ASIN/081534211X/geneexpressio-20)In all the models hunter-gatherers diverged relatively recently and so did the agriculturalists. Europeans, who are stand-ins for*all*non-Africans in this scenario, diverged pretty early from the Africans. But how the Africans relate to each other and Europeans is not totally clear. Why? **Because ancient population structure.**It is becoming rather obvious now that \~100,000 years ago, and earlier, there were many different modern human lineages which had already diversified. The Khoisan seem to have diverged from other human lineages closer to 200,000 thousand than 100,000 years ago. What this means is that for most of the history of anatomically modern humans populationstructure
existed between distinct lineages. And some of that persists down to today within Africa.

I’ll bullet point some of their inferences from these models (verbatim quotes below):

1.  Our results suggest that the ancestors of the contemporary RHG, AGR
    and EUR populations diverged between 85 and 140 thousand years ago
    (kya), from an ancestral population that underwent demographic
    expansion between 173 and 191 kya 2.  After the initial population splits, the Ne of AGR and RHG (NaAGR
    and NaRHG) remained within a range extending from 0.55 to 2.2 times
    the ancestral African Ne (NHUM), whereas EUR (NaEUR) experienced a
    decrease in Ne by a factor of three to seven. 3.  The ancestors of the wRHG and eRHG populations diverged 18 to 20 kya
    (TRHG), and underwent a decreased in Ne by a factor of 3.8 to 5.7
    for the wRHG (NwRHG) and 7.1 to 11 for the eRHG (NeRHG), regardless
    of the branching model considered. 4.  The ancestors of the AGR (NaAGR) split into western and eastern
    populations 6.7 to 11 kya (TAGR), and underwent a mild expansion, by
    a factor of 2.3 to 3.1 for the wAGR (NwAGR) and 1.2 to 2.2 for the
    eAGR (NeAGR). 5.  The EUR population experienced a 7.1- to 8.3-fold expansion (NEUR)
    12 to 22 kya (TEUR).

No results are perfect. **But some of these dates do not make sense**. There’s a lot of circumstantial evidence that the ancestors of European populations began to expand over the last 10,000 years. The dates above suggest there was a Pleistocene expansion. Basically you can divide that value by half, and then you get a reasonable range.

[![](https://i0.wp.com/gnxp.com/WordPress/wp-content/uploads/2017/04/Screenshot-2017-04-27-01.47.11.png?resize=175%2C250)![](https://i0.wp.com/gnxp.com/WordPress/wp-content/uploads/2017/04/Screenshot-2017-04-27-01.47.11.png?resize=175%2C250)](https://www.amazon.com/exec/obidos/ASIN/3319540629/geneexpressio-20)Second, both the agriculturalists sampled here are Bantu speaking, and there’s a good amount of cultural and genetic data for recent shared ancestry of the Bantu [over the last 3,000 years](https://en.wikipedia.org/wiki/Bantu_expansion#Expansion). I understand that admixture with a very diverged lineage (e.g., eastern Bantu agriculturalist samples mixing with Nilotic populations, which is how they got some non-African ancestry, as well as local Pygmy groups) can inflate these divergence dates. If that’s the case, they should note that in the text.

We don’t have much historical or archaeological clarity from what I know about divergences between Pygmy groups. This particular group has studied the topic and published on it before, so I’m inclined to trust them more than anyone else. But, the above dates for groups we do know make me a bit more skeptical of a simple divergence around the Last Glacial Maximum.

Then there are the earliest divergences. And 85 to 140,000 year interval is huge for when non-Africans split off from Africans. If closer to 140 than 85, then that means that non-African divergence from Africans preserves ancient African diversity. That is, non-Africans descend from an African group that no longer exists (or has not been sampled in this study at least!). I’ve poked around this question, and when you take into account recent gene flow, it is hard to find the specific African group that non-Africans descend from, though there is some consensusthat they branched off from the non-Khoisan Africans later than from the Khoisan.

But there is also a lot of archaeological and some ancient genetic DNA now that indicates that the vast majority of non-African ancestry began to expand rapidly around 50-60,000 years ago. This is tens of thousands of years after the lowest value given above. Therefore, again we have to make recourse to a long period of separation before the expansion. This is not implausible on the face of it, but we could do something else: **just assume there’s an artifact with their methods and the inferred date of divergence is too old**. That would solve many of the issues.

I really don’t know if the above quibbles have any ramification for the site frequency spectrum of deleterious mutations. My own hunch is that no, it doesn’t impact the qualitative results at all.

[![](https://i0.wp.com/gnxp.com/WordPress/wp-content/uploads/2017/04/Screenshot-2017-04-27-01.21.17.png?resize=300%2C275)![](https://i0.wp.com/gnxp.com/WordPress/wp-content/uploads/2017/04/Screenshot-2017-04-27-01.21.17.png?resize=300%2C275)](http://biorxiv.org/content/biorxiv/early/2017/04/26/131219.full.pdf)Figure 3 clearly shows that **Europeans are enriched for weak and moderately deleterious mutations** (the last category produces weird results, and I wish they’d talked about this more, but they observe that strong deleterious mutations have issues getting detected). *N_(e)* is just the effective population size and *s* is the selection coefficient (bigger number, stronger selection).

Why are the middle two values enriched? Presumably it’s the non-African bottleneck. This is where another non-African population would have been a nice check to make sure that it was the “Out of Africa” bottleneck…but it’s probably asking a bit much to sequence more individuals to 70x coverage.

The lack of difference between the African populations is an **indication that recent demography is not shaping the distribution much.** Additionally, they note that gene flow between the African groups probably increased diversity in some ways, so that as long as a group is connected with other populations it will probably be rescued (note that none of these in their data were particular inbred as judging by runs of homozygosity).

Finally, they found that the number of homozygote mutations that were deleterious is higher in their model results for Europeans than the African groups. This is not surprising, and what one expects. But, **they found that this is a function likely of continuous gene flow between the African groups.** Without gene flow homozygosity would have been much higher. This gets back to the fact that gene flow is a powerful homogenizing tool, and the lack of gene flow has to be pretty extreme for divergence to occur.

Which brings us back to the “Out of Africa” event. The next ten years are going to see a lot of investigation of African phyologenomics and population genomics. Basically, the relationships, and selection pressures. It is totally implausible that Bantu groups in Kenya and Tanzania did not absorb local non-Nilotic populations. We’ll figure that out. Additionally, selection pressures are probably different between different groups. We’ll know more about that. **But, ancient DNA will probably give us some understanding of why non-Africans went through such a massive demographic sieve.** We know in broad sketches. But most people want to fill in the details.

**Citation:** The demographic history and mutational load of African hunter-gatherers and farmers, Marie Lopez, Athanasios Kousathanas, Helene Quach, Christine Harmant, Patrick Mouguiama-Daouda, Jean-Marie Hombert, Alain Froment, George H Perry, Luis B Barreiro, Paul Verdu, Etienne Patin, Lluis Quintana-Murci, doi: https://doi.org/10.1101/131219

### Related Posts:

- [Selection and load (through the
  bottleneck)](https://www.gnxp.com/WordPress/2014/11/03/selection-and-load-through-the-bottleneck/) - [Fitness is still a
  bugger!](https://www.gnxp.com/WordPress/2015/02/01/fitness-is-still-a-bugger/) - [Jolie + Pitt = baby with low mutational
  load?](https://www.gnxp.com/WordPress/2006/05/21/jolie-pitt-baby-with-low-mutational-load/) - [The introduction of farming & new genes to
  Europe](https://www.gnxp.com/WordPress/2009/09/03/the-introduction-of-farming-new-genes-to-europe/) - [Whole genomes of ancient farmers and
  hunter-gatherers](https://www.gnxp.com/WordPress/2020/11/24/whole-genomes-of-ancient-farmers-and-hunter-gatherers/) - [Genetic load is higher outside of
  Africa](https://www.gnxp.com/WordPress/2015/05/24/genetic-load-is-higher-outside-of-africa/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F04%2F26%2Fout-of-africa-bottleneck-is-what-really-matters-for-mutations%2F&linkname=%E2%80%9COut%20of%20Africa%E2%80%9D%20bottleneck%20is%20what%20really%20matters%20for%20mutations "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F04%2F26%2Fout-of-africa-bottleneck-is-what-really-matters-for-mutations%2F&linkname=%E2%80%9COut%20of%20Africa%E2%80%9D%20bottleneck%20is%20what%20really%20matters%20for%20mutations "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F04%2F26%2Fout-of-africa-bottleneck-is-what-really-matters-for-mutations%2F&linkname=%E2%80%9COut%20of%20Africa%E2%80%9D%20bottleneck%20is%20what%20really%20matters%20for%20mutations "Email")[](https://www.addtoany.com/share)
