+++
title = "The vines around the"
full_title = "The vines around the tree trunks"
date = "2019-07-01"
upstream_url = "https://www.gnxp.com/WordPress/2019/07/01/the-vines-around-the-tree-trunks/"

+++
Source: [here](https://www.gnxp.com/WordPress/2019/07/01/the-vines-around-the-tree-trunks/).

The vines around the tree trunks

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2019/07/arg.jpg?resize=600%2C486&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2019/07/arg.jpg?resize=600%2C486&ssl=1)](https://www.biorxiv.org/content/10.1101/687368v1)  
[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/01/lone_survivor.jpeg?resize=183%2C275&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/01/lone_survivor.jpeg?resize=183%2C275&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/B005XMK898/geneexpressio-20/ref=as_at?imprToken=3SzvErsqk0uegISbc6B6.g&slotNum=0&imprToken=T99HvL7y.cNmVg.TW4Q7EQ&slotNum=0&imprToken=67TxncJrNOO11LKRkLbXog&slotNum=23&creativeASIN=0878933085&linkCode=w61&imprToken=QiG2bf7fc5-czG6VLZ9cSg&slotNum=164)A lot of the understanding of scientific theories and models in the public domain is communicated by evocative metaphors and turns of phrase. For example, Charles Darwin famously wrote:

> **It is interesting to contemplate a tangled bank**, clothed with many > plants of many kinds, with birds singing on the bushes, with various > insects flitting about, and with worms crawling through the damp > earth, and to reflect that these elaborately constructed forms, so > different from each other, and dependent upon each other in so complex > a manner, have all been produced by laws acting around us….

When it comes to understanding the origin of our own species and the broader human lineage over the past two million years, **I’ve started to come to a mental model of a weighted-graph with edges**. Some of the edges traverse time and have strong weights. These are analogous to the normal phylogenetic tree model, representing phyletic gradualism and anagenesis along each branch before some bifurcation event. But, some of the edges move horizontally between others. These represent migration and/or gene flow between the primary lineages.

I’m not sure though that a graph theory derived mental model helps many people, so I’ll use another one: **imagine large trunks defining the primary lineages, and vines tying them together representing gene flow events**. The above figure is from a new preprint, [Mapping gene flow between ancient hominins through demography-aware inference of the ancestral recombination graph](https://www.biorxiv.org/content/10.1101/687368v1). This is a methods-heavy preprint. It utilizes an “ancestral recombination graph” (so a model of the genealogy of genes in the genome) and [MCMC](https://en.wikipedia.org/wiki/Markov_chain_Monte_Carlo) generate Bayesian probabilities of particular events (e.g., introgression of a lineage that diverged *x* years ago at fraction *y*).

The abstract presents some specific findings:

> …While much attention has been paid to the relatively recent gene flow > from Neanderthals and Denisovans into modern humans, other instances > of introgression leave more subtle genomic evidence and have received > less attention. Here, we present an extended version of the ARGweaver > algorithm, ARGweaver-D, which can infer local genetic relationships > under a user-defined demographic model that includes population splits > and migration events. This Bayesian algorithm probabilistically > samples ancestral recombination graphs (ARGs) that specify not only > tree topology and branch lengths along the genome, but also indicate > migrant lineages…We show that this method is well powered to detect > the archaic migration into modern humans, even with only a few > samples…We apply it to human, Neanderthal, and Denisovan genomes, > looking for signatures of older proposed migration events, including > ancient humans into Neanderthal, and unknown archaic hominins into > Denisovans. **We identify 3% of the Neanderthal genome that is > putatively introgressed from ancient humans, and estimate that the > gene flow occurred between 200-300kya.** We find no convincing > evidence that negative selection acted against these regions. **We > also identify 1% of the Denisovan genome which was likely introgressed > from an unsequenced hominin ancestor, and note that 15% of these > regions have been passed on to modern humans through subsequent gene > flow.**

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/01/whoweare.png?resize=183%2C276&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/01/whoweare.png?resize=183%2C276&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/B073NP8WT3/geneexpressio-20/ref=as_at?imprToken=3SzvErsqk0uegISbc6B6.g&slotNum=0&imprToken=T99HvL7y.cNmVg.TW4Q7EQ&slotNum=0&imprToken=67TxncJrNOO11LKRkLbXog&slotNum=23&creativeASIN=0878933085&linkCode=w61&imprToken=QiG2bf7fc5-czG6VLZ9cSg&slotNum=164)ARGweaver-D is gnarly. Not in a bad way. But you should never really trust computational wizard of this sort unless you’ve taken it for a test drive, or it’s been around decades and people have validated it. A “play with the parameters” phase is necessary for these packages to become more than magic.

That being said, for about half a decade people have been detecting evidence of a “super-archaic” lineage within Denisovans. This is just another confirmation with another method. The super-archaic hypothesis seems plausible as an explanation of the patterns in the data (there may be other explanations). Second, there’s a lot of circumstantial evidence for gene flow into Neanderthals from moderns. E.g., [mtDNA replacement](https://www.nature.com/articles/ncomms16046) in Neanderthals. Though not in the abstract, the preprint mentions the likelihood of “super-archaic” introgression into Neanderthals as well. From a recent ancient DNA paper on [Nuclear DNA from two early Neandertals reveals 80,000 years of genetic continuity in Europe](https://advances.sciencemag.org/content/5/6/eaaw5873):

> We find that population split times between HST and other Neandertals > of less than 150 ka ago make the occurrence of a mitochondrial time to > the most recent common ancestor (TMRCA) of 270 ka ago unlikely (1.2% > of all simulated loci have such a deep TMRCA; note S11). We note that > this result is robust to uncertainties in the estimates of the > Neandertal population size and of the mitochondrial TMRCA (note S11). > **The presence of this deeply divergent mtDNA in HST thus suggests a > more complex scenario in which HST carries some ancestry from a > genetically distant population.**

It seems entirely likely that we’re going to see “shadows of forgotten ancestors” in our genomes. But wait, there’s more!

> …ARGweaver-D only detected a small amount of Sup→Afr introgression, > which was somewhat lower than our estimated false positive rate. One > aspect to note here is that the power to identify introgression from > an unsequenced population is highly dependent on the population size > of the recipient population. The larger the population, the deeper the > coalescences are within that population, making it more difficult to > discern which long branches might be explained by super-archaic > introgression…If we had used a smaller population size, ARGweaver-D > would have produced more Sup→Afr predictions, but most of these would > be false positives unless that smaller population size is closer to > the truth. **Overall, we caution that the problem of detecting > super-archaic introgression into a large and structured population > such as Africas is very difficult and that claims of such > introgression need to be robust to the demographic model used in > analysis.** It may not be possible to address the question of ancient > introgression into Africans without directly sequencing fossils from > the introgressing population.

In northern Eurasia, in particular, one might imagine a scenario with large fluctuations in population size, and patchy landscapes. This would reduce gene flow between populations, and also foster drift to produce distinct lineages. Simple stylized models of gene flow at particular times across disparate lineages makes a great deal of sense in this context. But if Africa had larger populations of humans, with more interconnected networks with continuous, if variable, levels of gene flow then the stylized models will mislead in important features.

This preprint is likely reporting some true robust results that will hold up. But I think the bigger picture is that it will lead us toward moving beyond the extremely simple models in vogue a generation ago, to a more subtle understanding of complex emergence and collapse of human population structure over the last two million years.

### Related Posts:

- [Tangled Bank
  \#88](https://www.gnxp.com/WordPress/2007/09/12/tangled-bank-88/) - [Tangled Bank
  \#88](https://www.gnxp.com/WordPress/2007/09/11/tangled-bank-88/) - [Tangled Bank
  \#79](https://www.gnxp.com/WordPress/2007/05/09/tangled-bank-79/) - [Tangled Bank & Four Stone
  Hearth](https://www.gnxp.com/WordPress/2006/11/22/tangled-bank-four-stone-hearth/) - [The New Yorker has fact-checkers, they should use
  them](https://www.gnxp.com/WordPress/2016/04/28/the-new-yorker-has-fact-checkers-they-should-use-them/) - [Darwin
  Texts](https://www.gnxp.com/WordPress/2006/01/06/darwin-texts/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2019%2F07%2F01%2Fthe-vines-around-the-tree-trunks%2F&linkname=The%20vines%20around%20the%20tree%20trunks "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2019%2F07%2F01%2Fthe-vines-around-the-tree-trunks%2F&linkname=The%20vines%20around%20the%20tree%20trunks "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2019%2F07%2F01%2Fthe-vines-around-the-tree-trunks%2F&linkname=The%20vines%20around%20the%20tree%20trunks "Email")[](https://www.addtoany.com/share)
