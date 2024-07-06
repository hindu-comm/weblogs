+++
title = "Beyond the Punnett"
full_title = "Beyond the Punnett Square, part n"
date = "2005-10-09"
upstream_url = "https://www.gnxp.com/WordPress/2005/10/09/beyond-the-punnett-square-part-n/"

+++
Source: [here](https://www.gnxp.com/WordPress/2005/10/09/beyond-the-punnett-square-part-n/).

Beyond the Punnett Square, part n

This post is really just a short addendum to [David’s post](https://www.gnxp.com/blog/2005/10/genetics-in-movies.php). He offered that perhaps there are 5 loci that control skin color in humans. Well, it’s [more complicated than that](https://www.google.com/search?ie=UTF-8&oe=UTF-8&q=skin+color&btnG=Search&domains=gnxp.com&sitesearch=gnxp.com) I suspect, but let’s assume there are 6 loci. I’m going to present a super simple model to illustrate what I think is part of the reason that the inheritance of this trait contradicts some of the high school biology most people learn, which tends to emphasize simple Mendelian traits which are explained in the [dominant-recessive paradigm](https://www.gnxp.com/MT2/archives/003868.html).1

OK, so, as I said, we have 6 loci which control the expression of the skin color phenotype (basically a proxy for the density of melanocytes). Now, to make things simple, assume there are two alleles, or flavors, at each locus. At all the loci the alleles are either “on” or “off,” so you can have a profile at a locus of AA (both on), aa (both off), or Aa (one of each). Though the details of the sequence of each allele at each locus is no doubt different, assume they all have the same phenotypic effect of equivalent “dosage,” let’s call it “one dosage unit” (1 d.u.). In other words, someone who has all 12 alleles “on” would have 12 d.u. of melanin expression, someone with them all “off” would have 0 d.u. of expression. We are neglecting any interactional effects, so assume pure [additivity](http://www.medterms.com/script/main/art.asp?articlekey=25508) and independence.

Now, assume you have two parents with the genetic profiles as follows:

Parent 1 (P1) Aa, Bb, Cc, Dd, Ee, Ff.  
Parent 2 (P2) Aa, Bb, Cc, Dd, Ee, Ff.

In other words, they have the exact same profiles, and they are expression 6 d.u. of melanin, since at each locus they have an “on” and “off” allele. On visual inspection both would be “brown.” A parent with 0 du expression would be “white,” and 12 d.u. expression would be “black.”

Long time readers know where I’m going with this, but bear with me. What kind of children would they have? Each of the children would have 6 loci, with 2 alleles, one from each parent. So, you would have:

Child P1P2, P1P2, P1P2, P1P2, P1P2, P1P2.

Each slot would be filled by one of the two alleles at the equivalent locus from the parent. Note that I rigged it so that the expectation would follow a [binomial distribution](http://mathworld.wolfram.com/BinomialDistribution.html) like a coin flip, each slot has a 50:50 shot as being filled up by an “on” or “off” allele, because the parents are heterozygous at each locus.

The expectation is that the child would have a profile just like the parents, but, the number of loci being sampled during [random assortment](http://biology.about.com/library/glossary/bldefmenlawia.htm) and [segregation](http://biology.about.com/library/glossary/bldefmenlawseg.htm) is pretty small.

Expectation (X) = np, where n \~ trials (the total number of slots on all 6 loci, 12) and p \~ 0.5 (the chance of either an “on” or an “off” result in this case). So, expectation (X) = 12\*0.5, or 6, ergo, 6 d.u.s expectation of expression, just like the parents. This fits our intuition well.

But what about the variance? Variance (X) = np(1 – p), or, variance (X) = 12\*0.5(1 – 0.5) = 3. Since a standard deviation is the square root of the variance (let’s keep it in intelligible units), you get an expected deviation of 1.73 d.u.s during each round of successful reproduction. There is only about a 1 out of 4 chance that a child will be exactly at exactly 6 d.u.s. There is a 1 out of 14 chance that the child will express 3 or fewer d.u.s, and an equivalent probability that the child will express 9 or more d.u.s. If one assumes that these extremes verge toward the “white” and “black” phenotypes, one could say that there is a 1 out of 7 chance that each time these “brown” parents have a child, it will not be brown. This neglects the variation between 4 and 8 d.u.s, which would likely be discernable to visual inspection (quick back-of-excel, I figure that if the parents above have 6 children, there will be a 60% chance that at least 1 will not be brown as defined by a 4-8 d.u. range of phenotype).

As I stipulated above, I rigged the scenario for ease of exposition. The parents could both be brown, but be homozygous on all the same loci (P1 = AA, BB, CC, ee, dd, ff, P2 = AA, BB, CC, ee, dd, ff) which would result in no variation in the children if the trait was totally heritable in a conventional genetic sense (i.e.; no epigenetic factors, developmental randomness, environmental component of variation, etc.). Or, the parents could exhibit different genetic profiles, in which case the simplicity of expectation and variance wouldn’t be so easy to determine. This neglects the almost sure reality that 1) loci will have different dosage effects, 2) there will be some interactional aspect 3) some of the loci will be wide-ranging in their regulatory functions (like [MC1R](https://www.google.com/search?hl=en&lr=&safe=off&c2coff=1&domains=gnxp.com&q=MC1R&btnG=Search&sitesearch=gnxp.com)).

The only moral is one should go beyond the Punnett Square abstraction where phenotypes have simple (monogenic) causes.

Update: This applies to eye color as well, as I talked to an individual who claimed that their father had brown eyes, and mother green eyes, while they have blue eyes (and seemed sure of paternity based on other resemblences). One could imagine a scenario where the sampling process resulted in this individual getting a disproportionate number of “fair” alleles from both parents, which resulted in the expression of a phenotype that looks “blue” to the naked eye. Imagine, for example, that the 50% of the father’s alleles are “blue,” and 75% of the mother’s, one could selectively sample out of that (since 1/2 of the alleles come from each parent) fraction to generate a frequency of blue alleles greater than 75% (the mother’s phenotype being determined by the 3 to 1 blue to brown ratio, so a ‘true blue’ phenotype would need to be greater than that).

1 – I think terms like [incomplete dominance](https://en.wikipedia.org/wiki/Incomplete_dominance) and [codominance](https://en.wikipedia.org/wiki/Codominance) are pretty confusing, because they take the dominance-recessive dichotomy as an important reference that makes the rest of genetics intelligible. In reality, I think it just adds a conceptual overhead which isn’t justifiable in the post-genomic age. I also think [penetrance](https://en.wikipedia.org/wiki/Penetrance) is not really worth it as a term, not to mention that it sounds kind of dirty in our sexualized age.

### Related Posts:

- [Skin color loci
- older
  work](https://www.gnxp.com/WordPress/2005/12/02/skin-color-loci-older-work/) - [Skin deep, why I'm brown and you wish you
  were](https://www.gnxp.com/WordPress/2006/09/25/skin-deep-why-im-brown-and-you-wish-you-were/) - [More complex than simple
  addition](https://www.gnxp.com/WordPress/2006/12/26/more-complex-than-simple-addition/) - [But it still
  adapts!](https://www.gnxp.com/WordPress/2011/12/04/but-it-still-adapts/) - [The science of
  blindness](https://www.gnxp.com/WordPress/2006/03/09/the-science-of-blindness/) - [Gene expression, overdominance and skin
  color](https://www.gnxp.com/WordPress/2008/03/06/gene-expression-overdominance-and-skin-color/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2005%2F10%2F09%2Fbeyond-the-punnett-square-part-n%2F&linkname=Beyond%20the%20Punnett%20Square%2C%20part%20n "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2005%2F10%2F09%2Fbeyond-the-punnett-square-part-n%2F&linkname=Beyond%20the%20Punnett%20Square%2C%20part%20n "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2005%2F10%2F09%2Fbeyond-the-punnett-square-part-n%2F&linkname=Beyond%20the%20Punnett%20Square%2C%20part%20n "Email")[](https://www.addtoany.com/share)
