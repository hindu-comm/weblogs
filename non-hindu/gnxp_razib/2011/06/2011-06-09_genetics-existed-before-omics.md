+++
title = "Genetics existed before"
full_title = "Genetics existed before omics"
date = "2011-06-09"
upstream_url = "https://www.gnxp.com/WordPress/2011/06/09/genetics-existed-before-omics/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/06/09/genetics-existed-before-omics/).

Genetics existed before -omics

In the post below, [Moderate marginal value to genomics](http://blogs.discovermagazine.com/gnxp/2011/06/moderate-marginal-value-to-genomics/), I left some things implicit. It turns out that this was an ill-considered decision. In reality my comments were simply more cryptic and opaque than implicit. This is pretty obvious because **even those readers who are biologists didn’t seem to catch what I had *assumed* would be obvious in the thrust of my argument.**

The point in the broadest sense is that **DNA and genomics are not magical. Genetics existed before either of them.** Understanding the physical basis of genetics has certainly been incredibly fruitful, and genomics has altered the playing field in many ways. But there was a broad understanding of genetics *before* DNA and genomics, both in a Mendelian sense and in the area of biometrics and quantitative genetics. In the earlier post I indicated that the tools for predictions of adult traits due to the effect of genes have been around for a long time: **our family history.** By this, I mean that a lot of traits of interest are substantially [heritable](https://en.wikipedia.org/wiki/Heritability). A great deal of the variation within the population can be explained by variation of genes in the population, as *inferred* by patterns of correlation between individuals in their traits as a function of genetic relatedness. This is genetics as a branch of applied statistics. It has great “quick & dirty” power, especially in agricultural science.

Let’s look at something simple, height. It’s a continuous trait which is rather concrete. No one argues that “height” is a social construct. In Western societies height is \~80-90% heritable. That means that most of the variation within the population of the trait can be explained by variation in one’s family background. Tall people have tall children, short people have short children, and so forth. Here’s a “toy” scatterplot which shows the relation between mid-parent heights and adult offspring heights (I made up the numbers):

  
[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/gat0.jpg?resize=500%2C478)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/gat0.jpg?resize=500%2C478)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/gat0.jpg)

The correlation isn’t perfect. But it’s pretty good. The more heritable a trait is, the more a scatterplot of this form (offspring regressed on parents) approaches tight linearity with a slope of \~1. These plots are measuring narrow sense heritability, which is the additive genetic variance over the phenotypic variance. Additive genetic variance just means the variants which have additive or subtractive values to the trait value (or, they can be transformed as such).

To make this plot in a fashion which is more than illustrative you need a lot of data on a large number of individuals and their parents. **This would be tedious and require a substantial labor investment in earlier periods, but today with powerful data mining techniques I think it would be much, much, easier**. In a world where the child is the father of the man these methods would have great power.

But they’re not perfect. Siblings vary in height, even though though the trait seems mostly controlled by variation in genes on the population level. What’s going on? Genetically, Mendelian [segregation](https://en.wikipedia.org/wiki/Mendelian_inheritance#Law_of_Segregation_.28The_.22First_Law.22.29) and [genetic recombination](https://en.wikipedia.org/wiki/Genetic_recombination) are going to reshuffle the many alleles which control variation in height from parent to offspring in terms of what the [gamete](https://en.wikipedia.org/wiki/Gamete) contributes. Additionally, the nature of the environmental “noise” may vary from sibling to sibling. Using population wide data you can infer the expected value of the offspring based in heritability and mid-parent value, but there’s going to be variance about the mean of the theoretical distribution. For example, the standard deviation of I.Q. within the population is 15 points, and across full-siblings it is also 15 points.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/gat1.jpg?resize=317%2C330)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/gat1.jpg?resize=317%2C330)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/06/gat1.jpg)This is where genomics comes in. It does make a difference, on the margin. I suspect it would do so by removing some of the uncertainty of [segregation](https://en.wikipedia.org/wiki/Mendelian_inheritance#Law_of_Segregation_.28The_.22First_Law.22.29) and[genetic recombination](https://en.wikipedia.org/wiki/Genetic_recombination). Going back to the height example, imagine that you know of the \~1,000 genes which vary within the population to control variation in height. You sequence two parents, and so know which regions of the genomes they’re enriched for “tall” or “short” alleles. Some of the variance in the offspring is going to be due to the fact that the offspring don’t receive a perfect proportional representation of their parent’s alleles in terms of aggregate effect size. You could then remove some of the uncertainty in outcome because you can check the child’s genome against the parents’ and assess whether they received more or less of the “tall” or “short” alleles.

But there would still be environmental “noise” which you probably couldn’t account for. You can see an illustration of what I have in mind in the two normal distributions I plotted above. Both of them represent the theoretical distribution of possibilities of a child on a quantitative trait which only becomes realized in adulthood. The blue line shows what you can infer from the plain information of parental phenotypes. But what happens when you give them a genomic test? You remove some of the uncertainty from your calculus, and the variance drops. You see that in the red line.

This is what I mean when I say that genomics matters on the margin. It does have an effect. But all the tools to profile and predict are around us now. Even determined amateurs can find out quite a bit about someone’s family if they’re determined. This is no different in deep principle from the sort of techniques which large corporations are utilizing to create a “profile” of your possible future purchases by what you purchased in the past. The parents are past purchases. The adult offspring are future purchases. Knowing a lot of behavior genetic implicated genes might help the profile, but at the end of the day it’s not a deal-breaker or a game-changer.

An analogy to current market research and prediction algorithms is particularly apropos I think. **They creep people out.** So I naturally expect people to be creeped out if the state or insurance company has detailed fleshed out acturial tables based on genetics and genomics. But genetics or genomics don’t make it any more or less scary on a deep level. Nor do they make the techniques qualitatively more effective. **And the policy questions and responses are going to be the same no matter what.**

### Related Posts:

- [The allelomorphs of
  genetics](https://www.gnxp.com/WordPress/2013/09/11/the-allelomorphs-of-genetics/) - [From genomics and evolution to
  medicine](https://www.gnxp.com/WordPress/2006/11/16/from-genomics-and-evolution-to-medicine/) - [Then there was
  bioRxiv...](https://www.gnxp.com/WordPress/2015/04/07/then-there-was-biorxiv/) - [Applied genetics & your
  life](https://www.gnxp.com/WordPress/2006/07/02/applied-genetics-your-life/) - [Machine learning swallowing population genetics
  =…](https://www.gnxp.com/WordPress/2017/10/22/machine-learning-swallowing-population-genetics-understanding-patterns-in-population-genomics/) - [20th century genetics as basic science and 21st
  century…](https://www.gnxp.com/WordPress/2020/08/30/20th-century-genetics-as-basic-science-and-21st-century-genetics-as-basic-and-applied/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F06%2F09%2Fgenetics-existed-before-omics%2F&linkname=Genetics%20existed%20before%20-omics "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F06%2F09%2Fgenetics-existed-before-omics%2F&linkname=Genetics%20existed%20before%20-omics "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F06%2F09%2Fgenetics-existed-before-omics%2F&linkname=Genetics%20existed%20before%20-omics "Email")[](https://www.addtoany.com/share)
