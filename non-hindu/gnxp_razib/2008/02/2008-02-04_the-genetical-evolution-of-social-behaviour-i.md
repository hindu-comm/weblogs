+++
title = "The genetical evolution"
full_title = "The genetical evolution of social behaviour – I"
date = "2008-02-04"
upstream_url = "https://www.gnxp.com/WordPress/2008/02/04/the-genetical-evolution-of-social-behaviour-i/"

+++
Source: [here](https://www.gnxp.com/WordPress/2008/02/04/the-genetical-evolution-of-social-behaviour-i/).

The genetical evolution of social behaviour – I

[![ResearchBlogging.org](https://i0.wp.com/www.researchblogging.org/images/rbicons/ResearchBlogging-Medium-White.png?resize=80%2C50)![ResearchBlogging.org](https://i0.wp.com/www.researchblogging.org/images/rbicons/ResearchBlogging-Medium-White.png?resize=80%2C50)](http://www.researchblogging.org)[Inclusive fitness](https://en.wikipedia.org/wiki/Inclusive_fitness) is something you’ve heard of before no doubt. [J. B. S. Haldane](https://en.wikipedia.org/wiki/JBS_Haldane), one of the greatest evolutionary geneticists of the 20th century, once quipped that he would "…lay down \[his\] life for two brothers or eight cousins," a succinct expression of the subset of this framework which is bracketed under [kin selection](https://en.wikipedia.org/wiki/Kin_selection). The logic is pretty self-evident, but in the 1960s a lonely graduate student in England, William D. Hamilton, toiled away attempting to formally explain the mystery of altruism. The fruit of his labors were two papers, [The genetical evolution of social behaviour – I](http://www.ncbi.nlm.nih.gov/pubmed/5875341?dopt=Abstract) and [The genetical evolution of social behaviour – II](http://www.ncbi.nlm.nih.gov/pubmed/5875340), published in 1964 in the *The Journal of Theoretical Biology*. In [Narrow Roads of Gene Land, Volume 1: Evolution of Social Behaviour](https://www.amazon.com/exec/obidos/ASIN/0716745305/geneexpressio-20) he bemoans in a biographical preface to these papers his incredible self-doubts about the worth of the questions he was asking, the ubiquitous hostility or incomprehension that Hamilton was subject to from all his potentional mentors. During this period the explanation of altruism was self-evident to most, and the biologist [V. C. Wynne-Edwards](https://en.wikipedia.org/wiki/V._C._Wynne-Edwards) expressed the reigning consensus about the power of group level effects in shaping social dynamics. In short, it was "for the good of the species." Like Charles Darwin and his hero R. A. Fisher Hamilton thought there was more there than met the eye, and that a genetic explanation from first principles was necessary. In the prologue to his preface to [The genetical evolution of social behaviour – I](http://www.ncbi.nlm.nih.gov/pubmed/5875341?dopt=Abstract) he asks rhetorically why after all are there amicable relations between organisms which are not mates or the parent-offspring dyad? In this paper he attempts to mathematically "prove" why a gene selectionist viewpoint is sufficient as an explanation for altruism. Hamilton admits that his formalism was clumsy, he would later enthusiastically admit the elegance and greater generality of George Price’s [solution](https://en.wikipedia.org/wiki/Price_equation) toward the problem of altruism. But until then these two papers were essential as markers of an inflection point in a new direction in evolutionary biology and social theory. [The genetical evolution of social behaviour – I](http://www.ncbi.nlm.nih.gov/pubmed/5875341?dopt=Abstract) is not a hallmark of clear exposition; rather, [The genetical evolution of social behaviour – II](http://www.ncbi.nlm.nih.gov/pubmed/5875340) performs the task of illustrating the biological relevance of the somewhat opaque formalisms which Hamilton introduces. In reality it is actually one argument, but the presentation and level of abstraction differs to such a great extent that one may imagine many simply dove into the second with barely a glance at the first. My aim in his post is to go over the major points in homage to Hamilton, who ruefully admitted that though the first part of the paper had copious citations it seemed likely that very few actually read it (1,700+ citations according to [Google Scholar](https://scholar.google.com/scholar?q=The+genetical+evolution+of+social+behaviour&ie=UTF-8&oe=utf-8&rls=org.mozilla:en-US:official&client=firefox-a&um=1&sa=N&tab=ws) right now). The notation used is somewhat peculiar, and I’m going to make a few compromises because of the difficulties of rendering mathematical equations in HMTL (for purposes of accessibility I’m not going to make recourse to a specialty markup language).

The fitness of an individual is the sum of his basic unit of his personal genotype and the total of effects on due to neighbors which will depend on their genotypes:

*a*^(•) = 1 + δ*a* + *e*°, where sybmol ^(•) the personal effect of δ*a* into any aggregate, and ° will represent its exclusion. (1)

Hamilton then asks you to imagine two individuals, A & B, and their relation on a locus with represent to [their identity by descent](http://www.biochem.northwestern.edu/holmgren/Glossary/Definitions/Def-I/identity_by_descent.html). The sum of the probabilities of state is represented like so:

*c*₂ + *c*₁ + *c*₀ = 1

Where the subscript indicate the number of copies with match across the two individuals, and the probabilities must sum up to 1. From these relations Hamilton surmises that one can derive *r*, the [coefficient of relationship](https://en.wikipedia.org/wiki/Coefficient_of_relationship), and this value is essential in understanding the distribution of effects when an actor operates upon another individual. From a genetic viewpoint when fitness is at issue *r* is of the essence. From this Hamilton constructs a vector,

{ δ*a*_(*r*) }_(A) , which sums up the affect of A upon a range of individuals whose genetic relationship is measured by the *r* between A and the said individual.

Next Hamilton wants you to consider a set of genes at the locus, *p*₁, *p*₂, *p*₃…*p*_(*n*), so that the array may now be thought of as:

{ δ*a*_(*r*) }_(*ij*), where *ij* are now to represent genotypic values of A. Now, the total effect on fitness due to A can be considered:

Σ (evaluate across all *r*) (δ*a*_(*r*))_(A)= Σ (evaluate across all *r*) *r* (δ*a*_(*r*))_(A) + Σ (evaluate across all *r*) (1 – *r*) (δ*a*_(*r*))_(A)

This equation is decomposing the effect of A upon genes which are identical by descent and those which are not identical by descent using the coefficient of relationship. Hamilton, in another flurry of opaque formal transitions then rewrites the above as:

*δT*^(•)_(A) = *δR*^(•)_(A) + *δS*_(A)

This sums up the total effect of genes by A upon those identical by descent (that is, related), *δR*^(•)_(A), and those not identifical by descent, *δS*_(A). Now I’m going to skip some algebraic manipulation, and translate these into the affect upon an allele frequency, *p*_(*i*), over time:

Δ*p*_(*i*) = { *p*_(*i*) / ( *R*^(•)_(..) + *δS*_(..) ) } ( *R*^(•)_(*i*.) – *R*^(•)_(..) )

At this point, it is important to note that *R*^(•)_(..)represents the *inclusive fitness* as such, while Hamilton terms *δS*_(..) as the *dilution effect*. Remember, the latter are genes which are not identical by descent. Hamilton states that the sign of the inclusive fitness determines the direction of the change in gene frequencies, while *δS*_(..) influences the magnitude. The periods are placeholders for *i* & *j*, note that in this case one of the inclusive fitness variables does have *i*, indicating identity with the allele which we are tracking over time. After some algebraic manipulation Hamilton "proves" that the inclusive fitness is always maximized over time. I place quotations marks because Hamilton himself acknowledges "artificialities" in the model, for example, he uses weak selection to approximate zero selection because he isn’t changing the coefficients of relatedness over the generations through the iterations. His apologia is that selection as such *should be* weak, and that large effect mutations are ludicrous by definition. History is not on his side in this case! In any case, Hamilton makes it clear in the text that his goal is emulate the "classical model" of his time, which focused upon the spread of an allele via individual selection without an assumption of inclusive fitness, and that constrained and shaped his exposition and ends. In the next section, after a little algebra Hamilton constructs another equation where *r* is included more explicitly:

Δ*p*_(*i*) = *( p*_(*i*) *r*^(•) ) ( *δT*_(^(•)*i*.) – *δT*_(^(•)*.*.) ) / ( 1 + – *δT*_(^(•)*.*.) )

Remember that *r* manifests like so:

*0.500* parent-offspring  
*0.250* grandparent-grandchild  
*0.125* great grandparent-great grandchild  
*1.000* identical twins  
*0.500* full siblings  
*0.250* half siblings  
*0.125* first cousins

In short, the rate of change of an allele in this case may be modulated by the relationship across which the allele operates. Hamilton says that "the advantages conferred by the ‘classical’ gene to its carriers are such that the gene spreads at a certain rate the present result tells us that in exactly similar circumstances another gene **which conferred similar advantages to the sibs of the carriers would progress at exactly half this rate**." Does this sound familiar? Recall the idea that the "gay gene" could spread because aid given to nieces and nephews at the expense of individual fitness; the implausibility of this sort of evolutionary action is simply due to the fact that with an *r* of 1/4 between aunts & uncles and nieces & nephews the fitness enough would have to be incredibly large on the order of multiples.

There are some further details I’ve left out of this "exposition," as it is. But I think I provided a taste of the general line of thinking that Hamilton is proceeding along. If you’re curious I highly recommend that you obtain a copy of [The genetical evolution of social behaviour – I](http://www.ncbi.nlm.nih.gov/pubmed/5875341?dopt=Abstract). The biographical introduction to these two chapters are extremely informative and illuminating; and give you a heads up on the weak points in the papers.

HAMILTON, W. (1964). The genetical evolution of social behaviour. I. Journal of Theoretical Biology, 7(1), 1-16. DOI: [10.1016/0022-5193(64)90038-4](https://dx.doi.org/10.1016/0022-5193(64)90038-4)

### Related Posts:

- [Just Science, William D. Hamilton
  week](https://www.gnxp.com/WordPress/2008/02/03/just-science-william-d-hamilton-week/) - [William D. Hamilton & Narrow Roads of Gene Land
  week](https://www.gnxp.com/WordPress/2008/02/09/william-d-hamilton-narrow-roads-of-gene-land-week/) - [The West
  Group](https://www.gnxp.com/WordPress/2008/03/02/the-west-group/) - [R. A. Fisher and Inclusive
  Fitness](https://www.gnxp.com/WordPress/2008/09/23/r-a-fisher-and-inclusive-fitness/) - [Fisher on Inclusive Fitness, Again
  (again)](https://www.gnxp.com/WordPress/2010/12/19/fisher-on-inclusive-fitness-again-again/) - [E. O. Wilson has not changed his position on
  altruism](https://www.gnxp.com/WordPress/2008/11/10/e-o-wilson-has-not-changed-his-position-on-altruism/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F02%2F04%2Fthe-genetical-evolution-of-social-behaviour-i%2F&linkname=The%20genetical%20evolution%20of%20social%20behaviour%20%E2%80%93%20I "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F02%2F04%2Fthe-genetical-evolution-of-social-behaviour-i%2F&linkname=The%20genetical%20evolution%20of%20social%20behaviour%20%E2%80%93%20I "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F02%2F04%2Fthe-genetical-evolution-of-social-behaviour-i%2F&linkname=The%20genetical%20evolution%20of%20social%20behaviour%20%E2%80%93%20I "Email")[](https://www.addtoany.com/share)
