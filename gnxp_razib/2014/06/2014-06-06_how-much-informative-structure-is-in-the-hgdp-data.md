+++
title = "How much informative"
full_title = "How much informative “structure” is in the HGDP data set?"
date = "2014-06-06"
upstream_url = "https://www.gnxp.com/WordPress/2014/06/06/how-much-informative-structure-is-in-the-hgdp-data-set/"

+++
Source: [here](https://www.gnxp.com/WordPress/2014/06/06/how-much-informative-structure-is-in-the-hgdp-data-set/).

How much informative “structure” is in the HGDP data set?

A few weeks ago people were arguing about the utility of the model based clustering packages which produce intuitive bar plots which break down individual and population percentages. To understand the fundamental basis of these packages I’ll refer you to the original [Pritchard et al.](http://www.genetics.org/content/155/2/945.full) paper. As you probably know at this point one of the major parameters of the packages is the K value, which refers to the number of populations which are going to be assumed as the constituents of the genetic variation. **A key point is that those who use the packages are forcing the variation to fit a particular model.** You can take the data for Icelanders, to pick an example, and find K = 100. It will be produce results, but I suspect you’ll intuit that this really isn’t the best model in terms of fitting reality. Similarly, you can take a population of Northern Europeans, West Africans, and East Asians, and set K = 2. This will likely separate the Eurasians from the Africans, as that’s the natural phylogenetic affinity. But K = 3 is probably a better fit to the data. By this, I mean that Northern Europeans and East Asians are not, and have not been for a*long time*, random mating populations. K = 3 reflects this reality.

So far this is intuitive. Is there a formal way to check this? Yes. A variety. Structure outputs log likelihoods for each K. Admixture gives you cross-validation errors. For a full treatment of how Admixture estimates cross-validation error see [Alexander et al.](http://www.biomedcentral.com/1471-2105/12/246)An intuitive way to think about how you should interpret these values is that **they are giving you a sense of where you are trying to squeeze too many K’s out of the data set**. Admixture’s cross-validation value has a simple interpretation, look for the lowest point on the graph.

Going to back to the HGDP data set I wanted to know where that point on the scale of K’s was. Looking over [the populations](https://en.wikipedia.org/wiki/Human_Genome_Diversity_Project) I assumed more than 5, but likely less than 20. That wide range tells you that I don’t honestly have a good intuition (some distinct populations are going to be hard to separate in pooled data sets because there hasn’t been much time since divergence, or they are not really genetically separate populations).

  
The first thing I did was prep the HGDP data bit in terms of quality with [Plink](https://www.cog-genomics.org/plink2/). I filtered to SNPs with minor allele frequencies greater than 0.05, to get variants which might be informative on the interpopulation scale. Then I removed SNPs which were missing in more than 1% of individuals. Finally, I also LD pruned the SNPs (basically thinning the markers so that I got rid of variants which weren’t adding more information because they were near other SNPs). Additionally I also removed individuals which were very closely related to others in the data set. This resulted in a data set of 1,024 individuals and 116,840 SNPs.

Then I ran Admixture 20 times with default five-fold cross-validation from K = 2 to K = 20. Here’s the result in a scatterplot:

![cverrorbig](https://i0.wp.com/www.unz.com/wp-content/uploads/2014/06/cverrorbig.png?resize=600%2C527)![cverrorbig](https://i0.wp.com/www.unz.com/wp-content/uploads/2014/06/cverrorbig.png?resize=600%2C527)

You can’t see some of the points because the variation in error was so small at the lower K’s. It is clear that a few K’s do not accurately capture the variation in the HGDP data set. To put it different there aren’t four distinct randomly mating populations in the HGDP data set (K = 4).

Here’s a zoom in.

![cverrorZoom](https://i0.wp.com/www.unz.com/wp-content/uploads/2014/06/cverrorZoom.png?resize=600%2C527)![cverrorZoom](https://i0.wp.com/www.unz.com/wp-content/uploads/2014/06/cverrorZoom.png?resize=600%2C527)

These results make it clear there’s a ‘valley’ across the interval K = 11 to K = 16, with the lowest mean cross-validation error at K = 16. Not only does K = 16 have the lowest cross-validation error, but below K = 4 it has the lowest variation in cross-validation error as well. **This does not mean that there are 16 natural populations which best defines the world’s genetic variation.** For why this is not so I’ll point you to Daniel Falush’s post [What did we learn from Rosenberg et al. 2002, actually?](https://paintmychromosomes.blogspot.com/2014/06/what-did-we-learn-from-rosenberg-et-al.html), which highlights some other major dependencies of Structure-like model based clustering.

But, a complementary point is that **the number of K’s within the data are *not* arbitrary and subjective.** And that’s because human genetic variation exhibits geographic structure consistently across many forms of vizualization and inference. A second more tendentious point I would also like to add is that the new generation of population structure inference methodologies are pointing to the likelihood that **human genetic variation did not emerge through isolation by distance dynamics across clinal gradients.**

**Addendum:** I’m merging my 20 runs, starting with K = 16. But that’s going to take time. I’m also running K = 2 to K = 20 with a different data set, which expands beyond the HGDP, with 20 replicates.

### Related Posts:

- [Population structure, concrete and
  ineffable](https://www.gnxp.com/WordPress/2013/08/05/population-structure-concrete-and-ineffable/) - [What is a
  population?](https://www.gnxp.com/WordPress/2013/06/10/what-is-a-population/) - [Carving nature at its joints more
  realistically](https://www.gnxp.com/WordPress/2017/09/16/carving-nature-at-its-joints-more-realistically/) - [Geography of Genetic Variants
  Browser](https://www.gnxp.com/WordPress/2014/07/25/geography-of-genetic-variants-browser/) - [More genetic structure of human
  populations](https://www.gnxp.com/WordPress/2009/05/16/more-genetic-structure-of-human-populations/) - [Assessing the utility of models in ancient DNA
  admixture…](https://www.gnxp.com/WordPress/2020/04/13/assessing-the-utility-of-models-in-ancient-dna-admixture-analyses/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2014%2F06%2F06%2Fhow-much-informative-structure-is-in-the-hgdp-data-set%2F&linkname=How%20much%20informative%20%E2%80%9Cstructure%E2%80%9D%20is%20in%20the%20HGDP%20data%20set%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2014%2F06%2F06%2Fhow-much-informative-structure-is-in-the-hgdp-data-set%2F&linkname=How%20much%20informative%20%E2%80%9Cstructure%E2%80%9D%20is%20in%20the%20HGDP%20data%20set%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2014%2F06%2F06%2Fhow-much-informative-structure-is-in-the-hgdp-data-set%2F&linkname=How%20much%20informative%20%E2%80%9Cstructure%E2%80%9D%20is%20in%20the%20HGDP%20data%20set%3F "Email")[](https://www.addtoany.com/share)
