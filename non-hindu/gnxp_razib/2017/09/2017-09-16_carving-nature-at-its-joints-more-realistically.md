+++
title = "Carving nature at its"
full_title = "Carving nature at its joints more realistically"
date = "2017-09-16"
upstream_url = "https://www.gnxp.com/WordPress/2017/09/16/carving-nature-at-its-joints-more-realistically/"

+++
Source: [here](https://www.gnxp.com/WordPress/2017/09/16/carving-nature-at-its-joints-more-realistically/).

Carving nature at its joints more realistically

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/inferring_phylogenies.jpeg?resize=198%2C254)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/inferring_phylogenies.jpeg?resize=198%2C254)](https://www.amazon.com/exec/obidos/ASIN/0878931775/geneexpressio-20)If you are working on phylogenetic questions on a coarse evolutionary scale (that is, “macroevolutionary,” though I know some evolutionary geneticists will shoot me the evil eye for using that word) generating a tree of relationships is quite informative and relatively straightforward, since it has a comprehensible mapping onto to what really occurred in nature. When your samples are different enough that the [biological species concept](https://simple.wikipedia.org/wiki/Biological_species_concept) works well and gene flow doesn’t occur between node, then a tree is a tree (one reason Y and mtDNA results are so easy to communicate to the general public in personal genomics).

**Everything becomes more *problematic* when you are working on a finer phylogenetic scale** (or in taxa where inter-species gene flow is common, as is often the case with plants). And I’m using problematic here in the way that denotes a genuine substantive analytic issue, as opposed to connoting something that one has moral or ethical objections to.

It is intuitively clear that there is often **genetic population structure within species**, but how to summarize and represent that variant is not a straightforward task.

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/neighstruc.jpg?resize=200%2C236)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/neighstruc.jpg?resize=200%2C236)](http://www.genetics.org/content/155/2/945)In 2000 the paper [Inference of Population Structure Using Multilocus Genotype Data](http://www.genetics.org/content/155/2/945) in *Genetics* introduced the sort of model-based clustering most famously implemented with [Structure](https://web.stanford.edu/group/pritchardlab/structure.html). The paper illustrates limitations with the neighbor-joining tree methods which were in vogue at the time, and contrasts them with a method which defines a finite set of populations and assigns proportions of each putative group to various individuals.

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/structill.jpg?resize=150%2C133)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/structill.jpg?resize=150%2C133)](http://www.genetics.org/content/155/2/945)The model-based methods were implemented in numerous packages over the 2000s, and today they’re pretty standard parts of the phylogenetic and population genetic toolkits. The reason for their popularity is obvious: **they are quite often clear and unambiguous in their results.** This may be one reason that they emerged to complement more visualization methods like PCA and MDS with fewer *a priori* assumptions.

**But of course, crisp clarity is not always reality**. Sometimes nature is fuzzy and messy. The model-based methods take inputs and will produce crisp results, even if those results are not biologically realistic. They can’t be utilized in a robotic manner without attention to the assumptions and limitations (see [A tutorial on how (not) to over-interpret STRUCTURE/ADMIXTURE bar plots](http://www.biorxiv.org/content/early/2016/07/28/066431)).

This is why it is exciting to see a new preprint which addresses many of these issues, [Inferring Continuous and Discrete Population Genetic Structure Across Space](http://www.biorxiv.org/content/early/2017/09/15/189688)\*:

> A classic problem in population genetics is the characterization of > discrete population structure in the presence of continuous patterns > of genetic differentiation. Especially when sampling is discontinuous, > **the use of clustering or assignment methods may incorrectly ascribe > differentiation due to continuous processes** (e.g., geographic > isolation by distance) to discrete processes, such as geographic, > ecological, or reproductive barriers between populations. This > reflects a shortcoming of current methods for inferring and > visualizing population structure when applied to genetic data deriving > from geographically distributed populations. Here, we present a > statistical framework for the simultaneous inference of continuous and > discrete patterns of population structure….

The whole preprint should be read for anyone interested in phylogenomic inference, as there is extensive discussion and attention to many problems and missteps that occur when researchers attempt to analyze variation and relationships across a species’ range. Basically, the sort of thing that might be mentioned in peer review feedback, but isn’t likely to be included in any final write-ups.

As noted in the abstract the major issue being addressed here is the problem that **many clustering methods do not include within their model the reality that genetic variation within a species may be present due to continuous gene flow defined by isolation by distance dynamics.** This goes back to the old “clines vs. clusters” debates. Many of the model-based methods assume pulse admixtures between population clusters which are random mating. This is not a terrible assumption when you consider perhaps what occurred in the New World when Europeans came in contact with the native populations and introduced Africans. But it is not so realistic when it comes to the North European plain, which seems to have become genetically differentiated only within the last \~5,000 years, and likely seen extensive gene flow.

The figure below shows the results from the [conStruct](https://github.com/gbradburd/conStruct) method (left), and the more traditional fastStructure(right):  
[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/spatial_dist.jpg?resize=600%2C329)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/spatial_dist.jpg?resize=600%2C329)](http://www.biorxiv.org/content/early/2017/09/15/189688)

There are limitations to the spatial model they use (e.g., ring species), but that’s true of any model. The key is that it’s a good first step to account for continuous gene flow, and not shoehorning all variation into pulse admixtures.

Though in beta, the R package is already available on [github](https://github.com/gbradburd/conStruct)(easy enough to download and install). I’ll probably have more comment when I test drive it myself….

\* I am friendly with the authors of this paper, so I am also aware of their long-held concerns about the limitations and/or abuses of some phylogenetic methods. These concerns are broadly shared within the field.

### Related Posts:

- [The end of phylogenetic
  controversies](https://www.gnxp.com/WordPress/2012/10/07/the-end-of-phylogenetic-controversies/) - [Between the tree &
  ring](https://www.gnxp.com/WordPress/2015/01/01/between-the-tree-ring/) - [Haplogroups in the post-genomic
  era](https://www.gnxp.com/WordPress/2014/12/11/haplogroups-in-the-post-genomic-era/) - [Whales and complex
  speciation](https://www.gnxp.com/WordPress/2018/04/25/whales-and-complex-speciation/) - [Unveiling the genealogical
  lattice](https://www.gnxp.com/WordPress/2012/12/18/unveiling-the-genealogical-lattice/) - [If these bones could
  talk](https://www.gnxp.com/WordPress/2013/10/19/bones-talk/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F09%2F16%2Fcarving-nature-at-its-joints-more-realistically%2F&linkname=Carving%20nature%20at%20its%20joints%20more%20realistically "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F09%2F16%2Fcarving-nature-at-its-joints-more-realistically%2F&linkname=Carving%20nature%20at%20its%20joints%20more%20realistically "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F09%2F16%2Fcarving-nature-at-its-joints-more-realistically%2F&linkname=Carving%20nature%20at%20its%20joints%20more%20realistically "Email")[](https://www.addtoany.com/share)
