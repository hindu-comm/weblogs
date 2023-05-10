+++
title = "Population vs"
full_title = "Population vs quantitative genetics?"
date = "2007-03-23"
upstream_url = "https://www.gnxp.com/WordPress/2007/03/23/population-vs-quantitative-genetics/"

+++
Source: [here](https://www.gnxp.com/WordPress/2007/03/23/population-vs-quantitative-genetics/).

Population vs. quantitative genetics?

One issue that has cropped up in the comments a few times here is a conflation between quantitative & population genetics. Though people seem to think they’re interchangeable terms, they’re distinct fields. That’s why population genetics [text books](https://www.amazon.com/exec/obidos/ASIN/0878933069/geneexpressio-20) have chapters devoted specifically to quantitative genetics, and showing how the latter can be bridged with the former.  
Roughly, [population genetics](https://en.wikipedia.org/wiki/Population_genetics) is a “bottom up” field which deals with the dynamics of allele frequencies under the influence of evolutionary forces such as mutation, drift, selection and migration. In some ways it can be thought of as a formalization of the Mendelian revolution of the early 20th century, which reconceptualized inheritance as a discrete process.¹ [Quantitative genetics](https://en.wikipedia.org/wiki/Quantitative_genetics) is a more “top down” discipline. Though it crystallized during the same period as population genetics via the work of R.A. Fisher, Sewall Wright and J.B.S. Haldane, its roots are pre-Mendelian, and can be traced to the biometrical school founded by Francis Galton and promoted by Karl Pearson. It many ways quantitative genetics is a branch of statistics. Population genetics starts from first principles, assuming a set number of loci and an arrangement of alleles, first and foremost the [Hardy-Weinberg Equilibrium](https://en.wikipedia.org/wiki/Hardy-Weinberg_principle) (HWE), *p² + 2pq + q²*, where *p* & *q* represent two alleles on one locus and the three terms represent respective homozygotes and the heterozygote frequeny within a population. In contrast, quantitative genetics focuses on continuous traits which exhibit an normal distribution, and by its nature begins from the characteristics of realized phenotypes, as opposed to an abstract genetic model. But, **the two are fundamentally connected because quantitative genetics simply represents one extreme in regards to genetic architecture** (i.e., many loci which may be modeled by the [Central Limit Theorem](https://en.wikipedia.org/wiki/Central_Limit_Theorem) as random variables).

  
To illustrate the differences between population and quantitative genetics I thought it would be helpful to review some of the material in chapter 4 of [Evolutionary Genetics: Concepts and Case Studies](https://www.amazon.com/exec/obidos/ASIN/0195168186/geneexpressio-20), where Michael Wade tackles natural selection. In this chapter Wade illustrates how selection can be conceptualized from both a population & quantitative genetic perspective, and how the two are fundamentally equivalent formally.  
First, Wade begins with the classic diallelic single locus model. In sum:  
Genotype 1 homozygote = *AA*  
Genotype heterozygote = *Aa*  
Genotype 2 homozyogte = *aa*  
Here we are starting from first principles, one gene with two alleles, *A* and *a*. A randomly mating diploid organismic population without mutation, migration, drift or selection it is defined by the HWE like so:  
*p² + 2pq + q² = 1*  
*p²* = the frequency of the *AA* genotype (homozygote)  
*2pq* = the frequency of the heterozygote genotype, the sum of *Aa* & *aA*, which are genetically equivalent  
*q²* = the frequency of the *aa* genotype (homozygote)  
Because this is a diallelic system, by definition *q* = *(1 – p)*, so one could substitue and obtain the equation:  
*p² + 2p(1 – p) + (1 – p)² = 1*  
Since this chapter deals with selection Wade is interested in the **change of allele frequencies**, specifically, the different between *p^(‘)* and *p*, or *Δp*, where *p^(‘)* represents the frequency of *p* in the subsequent generation (the ^(‘) notation will be assumed as such subsequently). The change in the allele frequency is driven by the fitness associated with the allele in relation to the mean population fitness.  
For an additive allele the fitness of the genotypes can be defined as follows:  
*AA → 1 + 2*s**  
*Aa → 1 + *s**  
*aa → 1*  
1 is the baseline fitness. Substituting one *A* for an *a* increases the fitness by the selection coefficient, *s* (e.g., 0.01 would be a 1% increase in fitness), another *A* increase the fitness proportionally. In other words, the effect is additive & independent (independence here is less important as we are speaking only one of one locus). *W* or *w* will be used to represent fitness on occassion (the former being population mean and the latter an individual genotypic value). For the diallelic single locus model the equation is as follows:  
*Δp = ((1 + 2*s*)p²+ 1/2(1 + *s*)2pq)/(1 + 2p*s*) – p*  
The first term is a collection of variables and parameters which predict frequency of *p* in the generation after the initial one and after selection via differential fitness has altered the frequency. After a little algebra you get:  
*Δp = *spq/W**  
Where *W* is the mean population fitness, *s* is the selection coefficient, and *p* and *q* are the allele frequencies.  
For a scenario where heterozygote advantage is operative the fitness of the genotypes can be defined as follows:  
*AA → 1 + *s**  
*Aa → 1*  
*aa → 1 + *t**  
In this case *s* and *t* are the negative selection coefficients for the alleles when they are in homozygote genotypes. The initial formula is similar to the additive model:  
*Δp = ((1 + 2*s*)p²+ 1/2(1 + *s*)2pq)/(1 + p²*s* + q²*s*) – p*  
Which reduces to:  
*Δp = *pq(sp – tq)/W**  
In this case the sign of *Δp* depends upon the frequencies of the two alleles and their respective selection coefficients. Heterozygote advantange maintains genetic variation and attains an equilibrium of allelic proportions as a function of the selection coefficients defined by:  
*p^(\*) = t/(s + t)*  
Consider a situation where the *s* = – 0.01 and *t* = -0.1. This means that *AA* has a fitness of 0.99 vs. *Aa*, while aa has a fitness of 0.90 vs. *Aa*. Because the heterozygote exhibits advantage *a* will not be driven to extinction, but, 91% of the alleles in the population will be *A*. So that  
*AA* = 82.6%  
*Aa* = 16.5%  
*aa* = 8.26%  
All this illustrates the hallmarks of foundational population genetics: simple algebraic operations, difference equations, and prior assumptions about the parameters. Reality of course is quite a bit more complex than this toy model.  
Now let’s look at selection a bit from a quantitative genetic perspective. While above there was no talk of phenotypes, simply genes and their putative selective values vis-a-vis the mean, here we need to think in terms of phenotypes. Because phenotypes often exhibit continuity (e.g., height) we’ll make some recourse to calculus, though ultimately the integration won’t be so hairy that you need to follow the details. Rather, keep in mind that the integration is occuring over a function which describes the frequency distribution of traits. Assume that:  
*z* is a phenotypic value  
*W(z)* is the fitness function. That is, the fitness for a given *z*  
Though z is normally conceived of as a continuous trait which exhibits a wide range, one could map it onto the above population genetic model where *AA* = 1, *Aa* = 0.5 and *aa* = 0, assuming additivity.  
The mean phenotype in the population is described by the distribution:  
*Z = ∫ z p(z) dz*  
*z* is the phenotypic value, while *p(z)* represents the frequency of that value. Intregrating over the range over *z* gives the mean value. One could reach a good approximation by extracting proportions across very small phenotypic intervals (e.g., the proportion from 0 to 0.01 and 0.01 to 0.02….) and adding up the products, but with non-discrete traits this can get to be more of a headache then it’s worth. In studies of traits in wild populations it may be best not to discard any element of precision, ergo, the recourse to calclus (*dz* is of course just over an infinitemsimal range of *z*).  
Using the analogy with the population genetic model, we’re looking for the change in phenotype (as opposed to allele frequency):  
*ΔZ = Z^(‘) – Z*  
Here we see the formal equivalence between *Δp* and *ΔZ*. Ultimately we’re looking at the same issue, only from different sides of the coin. In a population genetic model we assume the nature of the reproductive process and the phenotypic outcome is posterior. In a quantitative genetic model the phenotype is in the picture from the beginning, and genes can be inferred or assumed later. In fact, the biometrical school, which was the precursor of quantitative genetics, rejected a Mendelian genetic model explicitly.  
Now let’s look at the above equation with the parameters:  
*ΔZ = ∫ z w(z) p(z) dz* – Z  
Here we’ve introduced *w(z)*. This is the appropriate fitness weight for each phenotypic value. The effect of these on the change in phenotype is further modulated by *p(z)*, the frequency of the phenotype. The fitness was not in the earlier expression because we were not assuming selection in the initial generation.  
The various parameters in the expression above are equivalent to:  
*ΔZ = Cov(z, w(z))*  
This implies that the change in the phenotype due to natural selection is the covariance of the phenotype and fitness.Recall that **natural selection works through differential fitness correlated with heritable traits**. Selection only “sees” the phenotype, its affect on the genotype is proportional to the amount of phenotypic variation that is controlled by genotypic variation, the *heritability*. In practice quantitative traits tend to exhibit heritabilities significantly below 1. Even human height exhibits a heritability of 0.80 in the industrialized world. That is, 80% of the phenotypic variation is due to genotypic variation, but 20% can not be attribute to genotype. This means that the offspring of parents whose values were selected to be above the population mean will not reflect in the whole the parental value, but will regress somewhat because the phenotypic value is not totally heritable (due to genes). In quantitative genetics there is a “breeder’s equation”:  
*R = h²S*  
This predicts the “response” (*R*) to a given selection differential between the parental population and the general population (*S*) assumping a particular heritability (*h²*). So, if you had a population with the phenotypic value 100, and selected a parental population with the value 200, and heritability was 0.5, then the offspring would have an average value of 150. This is because the parental average value of 200 was only half attributable to genetic qualities, and it is the genetic qualities which are presumably transmitted to the offspring. Using the notation above, we can rewrite the expression like so:  
*R = h²ΔZ*  
As you can see, **quantitative** genetics is quite mathematical. But so is population genetics as it becomes far more complex than the simple models above, and proceeds to enter into the domain of diffusion equations to model the flow of alleles through a population. Both are fundamentally simply models and descriptions of biological reality which emerge from the nature of our genetic architecture. In the early 20th century R.A. Fisher showed how discrete Mendelian genetics could simulate continuous phenotypic values. Discrete probability distributions converge upon the normal, and the discrete inheritance model easily generates continous phenotypes. Obviously the relationship between parental and offspring genotypes is clear, and is easily deducible a priori using a Mendelian paradigm, but Fisher also showed that the degrees of relatedness could be analyzed using the statistical concept of variance ([The Correlation Between Relatives on the Supposition of Mendelian Inheritance](https://en.wikipedia.org/wiki/The_Correlation_Between_Relatives_on_the_Supposition_of_Mendelian_Inheritance)). In the Post-Genomic Era single locus diallelic models really aren’t going to cut it, we’re going to have to grapple with enormous genomic scale data sets. A quantitative sense of large numbers and ranges needs to come back into play.  
**Note:** Adapted from chapter 4 of [Evolutionary Genetics: Concepts and Case Studies](https://www.amazon.com/exec/obidos/ASIN/0195168186/geneexpressio-20).  
**Related:** Some historical background.  
1 – Charles Darwin had no theory of inheritance so he postulated an intuitive “blending” model. The problem with this model is that this eliminates the variation which natural selection needs to operate. Mendelianism is ideal because the variation is perfectly preserved from generation to generation (though rearranged) in the form of discrete genes.

### Related Posts:

- [Types of
  genetics](https://www.gnxp.com/WordPress/2012/04/25/types-of-genetics/) - [Doing evolution's
  sums](https://www.gnxp.com/WordPress/2010/05/27/doing-evolutions-sums/) - [Creationism in
  Poland](https://www.gnxp.com/WordPress/2006/10/16/creationism-in-poland/) - [D. S. Falconer,
  1913-2004](https://www.gnxp.com/WordPress/2011/12/24/d-s-falconer-1913-2004/) - [Shout out for a good textual smackdown on the
  molecules](https://www.gnxp.com/WordPress/2006/04/06/shout-out-for-a-good-textual-smackdown-on-the-molecules/) - [Population Genetics and Microevolutionary
  Theory](https://www.gnxp.com/WordPress/2007/11/10/population-genetics-and-microevolutionary-theory/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F03%2F23%2Fpopulation-vs-quantitative-genetics%2F&linkname=Population%20vs.%20quantitative%20genetics%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F03%2F23%2Fpopulation-vs-quantitative-genetics%2F&linkname=Population%20vs.%20quantitative%20genetics%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F03%2F23%2Fpopulation-vs-quantitative-genetics%2F&linkname=Population%20vs.%20quantitative%20genetics%3F "Email")[](https://www.addtoany.com/share)
