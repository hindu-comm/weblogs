+++
title = "Breeding the breeder’s"
full_title = "Breeding the breeder’s equation"
date = "2007-05-02"
upstream_url = "https://www.gnxp.com/WordPress/2007/05/02/breeding-the-breeders-equation/"

+++
Source: [here](https://www.gnxp.com/WordPress/2007/05/02/breeding-the-breeders-equation/).

Breeding the breeder’s equation

I’ve talked about “the breeder’s equation,” R = *h²*S, before.  
R = response  
S = selection differential  
*h²* = narrow sense heritability  
For example, if you have a population where the mean phenotypic value is 100, and you select a subpopulation with a mean value of 125 to breed the next generation, and the heritability is 0.50, then:  
R = 0.50 \* (125 – 100) = 12.5  
In other words, the response to selection in this case where the differential is 25 units in the parental generation would be 12.5 units in the offspring with respect to the original population. This is because the “[narrow sense heritability](https://en.wikipedia.org/wiki/Heritability#Definition),” the proportion of phenotypic variation attributable to the variation in the additive effects of genes controls only 1/2 of the variation. In other words, there are other components of phenotypic variance, such as environmental variance, which may not be heritable from parent to offspring, and so there is a regression toward the population mean.  
This is all good & well, just like using [the ideal gas law](https://en.wikipedia.org/wiki/Ideal_gas_law), pV = nRT, is often very useful. But what does this tell us fundamentally about the nature of the phenomenon in question? The breeder’s equation has traditionally been part of the toolkit of the applied geneticist for whom **results matter, and the underlying biological principles are secondary**. On the other hand, an evolutionary biologist would be interested in exactly how the genetical process plays out from first principles, because the processes are simply an ends toward understanding fundamental aspects of nature. The breeder’s equation comes out of applied quantitative genetics, so in a sense it is “gene blind,” it simply describes and projects evolutionary processes without any exploration of a deeper framework. **But, we can obtain the breeder’s equation, and ergo quantitative genetical processes, from population genetic theory**. Nature is one.

  
First, let’s use a simple “counting” example. Imagine two loci, 1 & 2, with alleles in flavors A and a, and B and b, respectively. Let’s assume that the A & B contribute 1 unit of a trait, while a & b contribute 0 units. Additionally, the phenotypic outcomes are additive & independent across and within loci. By example:  
AABB = 4 units  
AaBb = 2 units  
AAbb = 2 units  
aaBB = 2 units  
Aabb = 1 units  
aaBb = 1 units  
aabb = 0 units  
Assume that the frequency of the two alleles are the same, p (since the loci are diallelic, p = 0.5 obviously). Within the population 50% of the alleles are A & B, and another 50% are a & b, at each locus, 1 & 2. We can construct the following table of genotype frequencies that segregate within the population assuming p = 0.5 for A & a and B & b:

|              |               |                          |                           |
|--------------|---------------|--------------------------|---------------------------|
| **Genotype** | **Frequency** | **Phenotype – additive** | **Phenotype – dominance** |
| AABB         | 1/16          | 4                        | 2                         |
| AABb         | 2/16          | 3                        | 2                         |
| AAbb         | 1/16          | 2                        | 1                         |
| AaBB         | 2/16          | 3                        | 2                         |
| AaBb         | 4/16          | 2                        | 2                         |
| Aabb         | 2/16          | 1                        | 1                         |
| aaBB         | 1/16          | 2                        | 1                         |
| aaBb         | 2/16          | 1                        | 1                         |
| aabb         | 1/16          | 0                        | 0                         |

I’ve included dominance because we’ll discuss this in a bit. In any case, intuitively the proportions should make sense. There is only one way you can obtain a genotype of all “upper case” or “lower case” alleles, so you just multiply the expectations across each slot, 1/2⁴, and you get 1/16. In contrast, there are multiple ways that you can obtain an AaBb genotype. AaBb, aABb, aAbB and AabB are equivalent, so you obtain 4 out of the 16 genotypic conformations.  
Now, let’s assume that we are selecting a parental population from a subset of the overall population. Genotypes selected are as follows in the proportions given:  
Aabb = 2/5  
aaBb = 2/5  
aabb = 1/5  
This obviously is not representative of the overall population, and because of what we know about the genetic architecture we should expect that this will result in a different phenotypic mean within the offspring. In the larger population the mean would be 2 (you can confirm this numerically from the table above, or, just note that it is the mean derived from the [binomial distribution](https://en.wikipedia.org/wiki/Binomial_distribution#Mean.2C_variance.2C_and_mode)). In the parent generation the mean is:  
(2/5)(1) + (2/5)(1) + (1/5)(0) = 4/5  
We simply took the proportions, used them as weights for the phenotypic values for the genotypes. Since “lower case” alleles are disproportionately represented in the selected population intuitively we should have expected a value lower than the overall population mean. Let’s stipulate that the trait is totally genetically controlled, then the outcome in the offspring will presumably be the same in regards to the mean phenotype as in the parents (expectation), 4/5. Going back to the breeder’s equation, we substitute:  
(4/5 – 2 ) = *h²*(4/5 – 2) or  
*h²* = 1.0  
The selected parental phenotype & the offspring phenotype both have a mean value of 4/5, so we remove 2, the original population mean. By basic algebra that means that the narrow sense heritability is 1.0. The way I framed the genetic architecture as additive and independent means that all the variation is due to additive genetic variance, so we should expect that the heritability in the narrow sense should account for the full phenotype range.  
So let’s move on to the case of dominance. The frequencies & phenotypic outcomes are in the table above. Note now that though the loci are independent across each other in terms of effect, **they are not additive in the intralocus context**. That is, the “upper case” alleles are dominant so that AA & Aa are phenotypically identical, *ceteris paribus*. The mean value for the distribution of phenotypic values obtained from the genotypes in the case of dominance is 1.5. You can confirm this numerically, or simply derive it from the expression 2p(1 + q), where q = 1 – p, and in this case q = p (both being 0.5). Now let us select from this overall population parents of the proportion:  
AAbb = 1/7  
Aabb = 2/7  
aaBB = 1/7  
aaBb = 2/7  
aabb = 1/7  
As above, we obtain a mean phenotype of the select parents:  
(1/7)(1) + (2/7)(1) + (1/7)(1) + (2/7)(1) + (1/7)(0) = 6/7  
Again, this is expected, we selected from the two lowest phenotypic values. Now, what is the mean of the offspring? Recall that I stated above that 2p(1 + q) = μ, where with a mean value of 110 is the mean value. We substitute the allelic proportions from the above, collecting the A & B as like categories:  
2(2/7)(1 + 5/7) = 48/49  
Now, back into the breeder’s equation:  
(48/49 – 1.5 ) = *h²*(6/7 – 1.5) or  
*h²* = 0.81  
Note: **the trait is totally genetically controlled, but the heritability in the narrow sense is now less than 100%!** Why? We are selecting phenotypic values, not genotypic ones. In the case of the additive inheritance there is a perfect 1:1 linear relation between genotype and phenotype. Not so with dominance, e.g., AaBb & AABB are phenotypically equivalent. Just as in a case where environmental variance can account for some of the exceptional phenotypes selected, dominance results in a imperfect transmission of phenotypes from parent to offspring because of the resegregation of homozygotes in subsequent generations. By example, two populations of pure heterozygotes & homozogyotes where dominance is operative might have the exact same mean phenotypic value in the current generation, but in the subsequent generation the recessive offspring of the heterozygotes will shift the phenotypic distribution even if the attribute is totally genetically controlled.  
![quanttrunc.jpg](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2007/05/quanttrunc.jpg?resize=250%2C145)![quanttrunc.jpg](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2007/05/quanttrunc.jpg?resize=250%2C145)The illustration above was predicated on discrete counting methodology. This being a post about quantitative genetics, I’m now going to throw in a basic definition in regards to the normal distribution and how it relates to truncation selection. The details are pretty irrelevant so I’m going to gloss over it and just define the parameters and throw out an expression which we’ll use later. So to the left you see a normal distribution curve which models a continuous trait which emerges via the [central limit theorem](https://en.wikipedia.org/wiki/Central_Limit_Theorem) from the combined action of innumerable “random variables,” whether they be environmental or genetic (or a combination thereof).  
T = the truncation value, below which all phenotypic values are discarded from the parents of the subsequent generation  
Z = the height of distribution at T  
B = the area under the distribution being selected (i.e., the integral from T to ∞, so if B = 0.35, that means 35% of the population is selected, and that 35% of the population exhibits a phenotypic value above T)  
You should also note deviations from the mean defined by “a,” which indicates the effect of a substitution of one gene, and “d,” which represents the dominance at this locus. If d = 0, there is no dominance, while if d = 1, full dominance is operative (dominance = d/a). To illustrate, if you have a locus, 1, where the effect is additive, then AA = mean + a, Aa = mean + d and aa = mean – a. The important point is that we’re mapping genetic effects upon the normal distribution with these parameters a & d, and they’ll come in handy later. Finally, should also keep in mind the expression:  
(μ_(s) – μ)/σ² = Z/B  
Where:  
μ_(s) = mean of the selected population  
μ = mean of the population  
σ² = [variance](https://en.wikipedia.org/wiki/Variance) of the population  
With that under our belt we shift back to the world of p’s & q’s, population genetics. In a previous post I outlined how changes in allele frequency can be modeled both via population & quantitative genetics, and now we’ll use these formalisms to show how they connect to the breeder’s equation. Here are expressions which represent differences in fitness between the genotypes above:  
(fitness AA – fitness Aa) \~ Z(a – d)  
(fitness Aa – fitness aa) \~ Z(a + d)  
average fitness = B (B is the proportion saved for breeding)  
so,  
Δp = pq(p(fitness AA – fitness Aa) + q(fitness Aa – fitness aa) )/(average fitness)  
substituting from above  
Δp =pq(pZ(a – d) + qZ(a + d))/B  
since p + q = 1  
Δp = (Z/B)pq(a + (q – p)d) or one can substitute 1 – p for q  
Where there is no dominance you note that the formalism above reduces to (Z/B)pqa. With dominance the ratio of p & q is very importance since that determines the proportion of homozygote recessives which will segregate out per the [Hardy-Weinberg](https://en.wikipedia.org/wiki/Hardy-Weinberg) equation. Now, the mean phenotype of a given generation can be obtained:  
μ^(‘) = (p + Δp)²(μ^(\*) + a) + 2(p + Δp)(q – Δp)(μ^(\*) + d) + (q – Δp)²(μ^(\*) – a)  
The change in mean phenotype here is simply assumed to track the change in allele frequencies within a population in Hardy-Weinberg Equilibrium.  
Multiplying and removing Δp² because it is so small  
μ^(‘) = μ + 2(a + (q – p)d)Δp  
Here we have the change in mean phenotype as a function of the change in allele frequencies (presumably being driven by selection) and the additive & dominance effects. If substitution of the allele has a negative additive effect one can see here that the mean phenotype value decreases, while if the effect is positive the phenotypic value also increases. Similarly, we see again that if dominance is operative the proportion of p & q is highly significant as the recessive phenotype is a squared function of the proportion of one of the alleles (i.e., by convention generally q²). The expression above can now bring us to the breeder’s equation. I’ll jump through the steps briefly  
Move the mean value to the left side  
μ^(‘) – μ = 2(a + (q – p)d)Δp  
Substitute Δp for the expression with Z & B  
μ^(‘) – μ = (Z/B)2pq(a + (q – p)d)²  
Recall that (μ_(s) – μ)/σ² = Z/B, so  
μ^(‘) – μ = (μ_(s) – μ)2pq(a + (q – p)d)²/σ²  
Now, what are the definitions for R & S?  
R = μ^(‘) – μ (response to selection)  
S = μ_(s) – μ (selection differential)  
Substitute  
R = S2pq(a + (q – p)d)²/σ²  
So now you have R, S and 2pq(a + (q – p)d)²/σ². The original breeder’s equation is R = *h²*S, so  
*h²* = 2pq(a + (q – p)d)²/σ²  
Bingo, **we’ve defined *h²* with concrete genetic parameters, p & q (the proportions of the alleles) and a & d (additive and dominance effects)!** Finally, since *h²* is used in the context of continuous quantitative traits which vary because of the combined effects of loci of small effect, we need to add a summation:  
(Σ 2pq(a + (q – p)d)²)/σ²  
And, since we know that *h²* = (additive genetic variance)/(total variance)  
additive genetic variance = Σ 2pq(a + (q – p)d)²  
Take a breath. If you’ve made it this far you might wonder why I posted this in the first place. Two reasons:  
a) putting this post together meant I had to go over this topic in more detail  
b) we see now that population and quantitative genetics are intimately connected, that Mendelian principles can be bridged with the utilitarian methods of applied quantitative genetics  
The breeder’s equation is a simple formalism. All you need is a heritability and a selection differential and you can generate a prediction of response. But being able to use an algorithm does not imply that one **understands the underpinning of that algorithm.** A [normal distribution](https://en.wikipedia.org/wiki/Normal_distribution) is an abstraction which only roughly maps onto continuous quantitative traits which emerge from the combined effects of discrete loci. Analyzing the continuous probability distributions gets us only so far in understanding genetics, because genetics is predicated on biological realities. The breeder’s equation is proximately useful, but to explore its boundaries and limitations we need to comprehend how it relates to Mendelian genetics. To understand the nature of evolutionary dynamics we need to understand how quantitative traits are shaped by selection and how they respond to selection. To understand the variation which selection must utilize we must understand the nature of Mendelian genetics. And so on. Science is a contingent system, but that contingency is not based on faith, it is based on induction and deep tedious analysis. In the future I plan to explore evolutionary quantitative genetics, and some comprehension of this post is a necessary precondition.  
**Note:** This post **closely** follows the treatment in [Principles of Population Genetics](https://www.amazon.com/exec/obidos/ASIN/0878933069/geneexpressio-20).

### Related Posts:

- [A smarter
  population?](https://www.gnxp.com/WordPress/2006/09/07/a-smarter-population/) - [More from less, increased variance from
  bottlenecks](https://www.gnxp.com/WordPress/2007/05/07/more-from-less-increased-variance-from-bottlenecks/) - [You only go extinct
  once....](https://www.gnxp.com/WordPress/2006/10/29/you-only-go-extinct-once/) - [Human driven elephant
  evolution?](https://www.gnxp.com/WordPress/2008/01/22/human-driven-elephant-evolution/) - [Longer term effective
  population](https://www.gnxp.com/WordPress/2006/09/02/longer-term-effective-population/) - [The Dutch are tall because evolution (in
  part)](https://www.gnxp.com/WordPress/2015/04/08/the-dutch-are-tall-because-evolution-in-part/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F05%2F02%2Fbreeding-the-breeders-equation%2F&linkname=Breeding%20the%20breeder%E2%80%99s%20equation "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F05%2F02%2Fbreeding-the-breeders-equation%2F&linkname=Breeding%20the%20breeder%E2%80%99s%20equation "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F05%2F02%2Fbreeding-the-breeders-equation%2F&linkname=Breeding%20the%20breeder%E2%80%99s%20equation "Email")[](https://www.addtoany.com/share)
