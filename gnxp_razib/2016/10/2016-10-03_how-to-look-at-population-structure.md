+++
title = "How to look at"
full_title = "How to look at population structure"
date = "2016-10-03"
upstream_url = "https://www.gnxp.com/WordPress/2016/10/03/how-to-look-at-population-structure/"

+++
Source: [here](https://www.gnxp.com/WordPress/2016/10/03/how-to-look-at-population-structure/).

How to look at population structure

[![700px-Neighbor-joining_Tree-2](https://i0.wp.com/www.unz.com/wp-content/uploads/2016/10/700px-Neighbor-joining_Tree-2.png?resize=600%2C380)![700px-Neighbor-joining_Tree-2](https://i0.wp.com/www.unz.com/wp-content/uploads/2016/10/700px-Neighbor-joining_Tree-2.png?resize=600%2C380)](https://en.wikipedia.org/wiki/Neighbor_joining)

[![51qciM4cBhL.\_SX258_BO1,204,203,200\_](https://i0.wp.com/www.unz.com/wp-content/uploads/2016/10/51qciM4cBhL._SX258_BO1204203200_.jpg?resize=260%2C344)![51qciM4cBhL.\_SX258_BO1,204,203,200\_](https://i0.wp.com/www.unz.com/wp-content/uploads/2016/10/51qciM4cBhL._SX258_BO1204203200_.jpg?resize=260%2C344)](https://www.amazon.com/exec/obidos/ASIN/0691029059/geneexpressio-20)A friend asked me about population structure, and methods to ferret it out and classify it. So here is a quick survey on the major methods I’m familiar with/utilize now and then. I’ll go roughly in chronological order.

First, you have **trees.** These are pretty popular from macroevolutionary relationships, but on the population genetic scale (intraspecific, microevolutionary) you’re mostly talking about representing distances between groups in a tree format. You saw this in [History and Geography of Genes](https://www.amazon.com/exec/obidos/ASIN/0691029059/geneexpressio-20), where genetic distances in the form of Fst values (proportion of genetic variation unique to between two groups) were used as distance inputs.

A problem with trees is that they don’t model gene flow, a major dynamic on a microevolutionary scale. Also, complex relationships can get elided in tree frameworks, and as you add more and more populations you often end up with an incomprehensible fan-like topology.

[![journal.pgen.0020190.g005](https://i0.wp.com/www.unz.com/wp-content/uploads/2016/10/journal.pgen_.0020190.g005-300x211.png?resize=300%2C211)![journal.pgen.0020190.g005](https://i0.wp.com/www.unz.com/wp-content/uploads/2016/10/journal.pgen_.0020190.g005-300x211.png?resize=300%2C211)](http://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.0020190)Then you have principle component analyses (**PCA**) and related methods (e.g., multidimensional scaling, which is very different in the sausage-making but generates a similar output). Like trees, this is a visualization of the variation, in this case on a two dimensional plot (please don’t bring up three dimensional PCA, there’s no such thing until holograms show up).

The problem with PCA is that different types of dynamics can lead to the same result. For example, someone who is an F1 of two distinct groups occupies the same position as a population which happens to occupy a genetic position between two groups. Additionally, by constraining the variation into two dimensions, one can mislead in terms of relationships. There are many dimensions, but operationally you focus on on two at a time.

A paper of interest, [Population Structure and Eigenanalysis](http://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.0020190).

[![Rosenberg4](https://i0.wp.com/www.unz.com/wp-content/uploads/2016/10/Rosenberg4-300x16.jpg?resize=300%2C16)![Rosenberg4](https://i0.wp.com/www.unz.com/wp-content/uploads/2016/10/Rosenberg4-300x16.jpg?resize=300%2C16)](http://pritchardlab.stanford.edu/publications/pdfs/PritchardEtAl00.pdf)Next you have **model-based clustering** introduced in Jonathan Pritchard’s [Inference of Population Structure Using Multilocus Genotype Data](http://pritchardlab.stanford.edu/publications/pdfs/PritchardEtAl00.pdf). There are many flavors of this, but they operate under the same framework. You have a model of population dynamics, and see how the genotype data can be explained by parameters of the model. Of particular interest is assignment to one of K populations, which can be combined to explain the variation in the data.

Unlike PCA these model-based methods are rather good at identifying people who are first generation mixes, as opposed to those from stabilized groups along a cline. But, they also produce artifacts, because they are quite sensitive to the input data, and lend themselves to cherry-picking.

![journal.pgen.1002967.g003 (1)](https://i0.wp.com/www.unz.com/wp-content/uploads/2016/10/journal.pgen_.1002967.g003-1-151x300.png?resize=151%2C300)![journal.pgen.1002967.g003 (1)](https://i0.wp.com/www.unz.com/wp-content/uploads/2016/10/journal.pgen_.1002967.g003-1-151x300.png?resize=151%2C300)Earlier I said that one problem with the tree methods is that they don’t model gene flow. Joe Pickrell’s **[TreeMix](http://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1002967)** does so. Like the original tree methods, and unlike PCA or unsupervised model-based clustering, you specify a set of populations. Then you compare the populations in terms of their genetic distance, and fit them to a tree, but add migration parameters to that tree where the fit between the tree and the data is the most tenuous fit.

All visualizations are deformations of reality. TreeMix attempts to mitigate this somewhat by introducing another representation, that of migration.

![Screenshot 2016-10-02 22.38.02](https://i0.wp.com/www.unz.com/wp-content/uploads/2016/10/Screenshot-2016-10-02-22.38.02-300x238.png?resize=300%2C238)![Screenshot 2016-10-02 22.38.02](https://i0.wp.com/www.unz.com/wp-content/uploads/2016/10/Screenshot-2016-10-02-22.38.02-300x238.png?resize=300%2C238)Next we have **local ancestry methods**. By local ancestry, basically we mean methods which can assign ancestry to particular regions of the genome. While tree methods measure differences across pooled populations, PCA and model-based methods compare genotypes between individuals (this is a simplification, but bear with me). Local ancestry methods, like [RFMix](http://www.cell.com/ajhg/abstract/S0002-9297(13)00289-9), compare regions of the genome with each other.

Related to, but not exactly the same, as local ancestry methods are **haplotype based methods**. In particular, I’m thinking of the [FineStructure](https://paintmychromosomes.blogspot.com/) and its related methods. These leverage variation across the genome in terms of haplotypes, rather than just looking at genotypes. They also tend to benefit from phasing, for obvious methods. FineStructure and its relatives tend to need more marker density than model-based methods, which require more marker density than PCA, which requires more marker density that tree based methods. These haplotype based methods allow for correction of and accounting for forces such as genetic drift, which tend to skew results in other methods.

Finally, there is the [AdmixTools](http://www.genetics.org/content/early/2012/09/06/genetics.112.145037)framework which is good for testing very explicit hypotheses. While many of the above methods, such as TreeMix and unsupervised model-based clustering, explore an almost open-ended space of structure possibilities, the methods in AdmixTools exists in large part to test narrow delimited models. This goes to the fact that many of these methods are complementary, and you should use them together to arrive at a robust result. For example, if you are assigning populations for TreeMix, you should use PCA and model-based clustering to make sure that the populations are clear and distinct, and outliers are removed.

There’s a lot I left out, but many of the other methods are just twists on the ones above.

### Related Posts:

- [PCA remains the swiss-army-knife to explore
  population…](https://www.gnxp.com/WordPress/2017/11/16/pca-remains-the-swiss-army-knife-to-explore-population-structure/) - [Visualizing intra-European phylogenetic
  distances](https://www.gnxp.com/WordPress/2017/12/10/visualizing-intra-european-phylogenetic-distances/) - [Ashkenazi Jews are more European in
  ancestry](https://www.gnxp.com/WordPress/2009/09/04/ashkenazi-jews-are-more-european-in-ancestry/) - [How Chinese relate to each other and the
  Japanese](https://www.gnxp.com/WordPress/2010/01/06/how-chinese-relate-to-each-other-and-the-japanese/) - [More genetic structure of human
  populations](https://www.gnxp.com/WordPress/2009/05/16/more-genetic-structure-of-human-populations/) - [SpaceMix](https://www.gnxp.com/WordPress/2015/01/09/spacemix/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2016%2F10%2F03%2Fhow-to-look-at-population-structure%2F&linkname=How%20to%20look%20at%20population%20structure "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2016%2F10%2F03%2Fhow-to-look-at-population-structure%2F&linkname=How%20to%20look%20at%20population%20structure "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2016%2F10%2F03%2Fhow-to-look-at-population-structure%2F&linkname=How%20to%20look%20at%20population%20structure "Email")[](https://www.addtoany.com/share)
