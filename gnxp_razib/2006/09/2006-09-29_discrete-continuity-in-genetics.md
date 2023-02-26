+++
title = "Discrete continuity in"
full_title = "Discrete continuity in genetics"
date = "2006-09-29"
upstream_url = "https://www.gnxp.com/WordPress/2006/09/29/discrete-continuity-in-genetics/"

+++
Source: [here](https://www.gnxp.com/WordPress/2006/09/29/discrete-continuity-in-genetics/).

Discrete continuity in genetics

In the post below on skin color within a multiracial family I made the point that **genetics is inherited in a discrete fashion**. In the post-genomic era, or even the post-DNA era, this seems intuitively clear. Our genetic sequence, our genome, is a string of precisely four base pairs, A, G, T and C. The genome is digital, not analog. Case closed, right?  
Not really. One of the main reasons I wrote the post below is the consistent misconception that **genetics is blending**, that children are a mix of the essences of their parents. This captures the expectation, but the variance. A natural inference of this model is that variation is diminished over the generations as it is homogenized through a process of mixture. Because Charles Darwin held to a system of blending inheritance he had to come up with ingenious ways to perpetuate and replenish variation. R.A. Fisher saw that Mendelianism was a way out, that discrete inheritance preserved information and genetic variation from generation to generation in full, mitigating the need for high mutational rates to battle homogenization, or to conceive of artificial barriers to breeding between demes.  
Though it is easy to assert that Mendelianism “naturally” leads to the perpetuation of extant variation, it was harder to come to this consensus. One of the early posts on this weblog dealt with the early 20th century battle between the Mendelians and Biometricians. A large number of the former conceived of themselves as rebels overthrowing the outmoded Darwinian model, while the Biometricians fancied themselves the heirs of Charles Darwin. Under the leadership of Karl Pearson the Biometricians held that the Mendelian model could not account for continuous variation in phenotype, such as the famous [bell curve](https://en.wikipedia.org/wiki/Normal_distribution) which describes the nature of traits such as height or intelligence. This was nonsense, as some early Mendelians saw, and Will Provine in his book *The Origins of Theoretical Population Genetics* seems to suggest that one of the main blocks was simply a conflict of personality. Though Karl Pearson was no Fisher, he was a genius in his own right, and the basic reality that discrete processes can approximate continuous ones should have been clear to him.  
Get it? If not, click below the fold for some graphs which I believe elucidate the issue pretty clearly.

  
Imagine a gene, locus “A,” which comes in two flavors, *A* and *a*. The latter is a loss of function, while the former codes for 1 bristle on a flie. The alleles on the locus are additive and independent, so that the genotype *Aa* is between the values of *AA* and *aa*.  
![image001.jpg](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2006/09/image001.jpg?resize=400%2C272)![image001.jpg](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2006/09/image001.jpg?resize=400%2C272)  
One could interpret *A* as dominant if you frame it as a dyad, “Bristled” vs. “unbristled.” But in any case, this is a standard Mendelian single locus trait. But what if we add a **second locus**, “B,” with the alleles *B* and *b* which are functionally cognate with *A* and *a*? That is, *B* contributes 1 bristle unit, while *b* contributes 0. This is now a two locus biallelic trait, and since we assume additivity and independence, the range of bristles can go from 4 to 0, all the way from *AABB* to *aabb*.  
![image004.jpg](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2006/09/image004.jpg?resize=400%2C272)![image004.jpg](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2006/09/image004.jpg?resize=400%2C272)  
The graph illustrates the combinations. But it tells you nothing of expected frequencies. Going back to our first example, we can imagine it as a Hardy-Weinberg Equilibrium system, where the frequency of allele *A* is 0.5 and *a* is 0.5. From p² + 2*pq* + q² we get:  
AA = 0.25  
Aa = 0.5  
aa = 0.25  
Or, to be clearer in terms of realized combinations,  
AA = 0.25  
Aa = 0.25  
aA = 0.25  
aa = 0.25  
In other words, **not all combinations are created equal, there are multiple ways to get a unit of 1 bristle, but only one way to get 2 or 0 is in the first case**. The same applies to the two locus biallelic case, assume that *p* and *q* are 0.5 again, you can generate a binomial probability mass distribution like so:  
![image002.jpg](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2006/09/image002.jpg?resize=400%2C269)![image002.jpg](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2006/09/image002.jpg?resize=400%2C269)  
2 bristles is the modal unit, dropping off to 4 and 0 at the tails. There are many combinations that will give you 2 bristle units, only 1 will give you 0 or 4. This is clearly a discrete stepwise distribution, but it more than a simple “dominant/recessive” dyad. Now, let’s crank this baby up, lets scale up to a 50 locus biallelic. Again, assume (extremely artificial) that all loci have frequences of 0.5 for a 1 bristle functional allele and a 0 bristle loss of function allele:  
![image006.jpg](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2006/09/image006.jpg?resize=400%2C273)![image006.jpg](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2006/09/image006.jpg?resize=400%2C273)  
That’s actually **not a smoothed out graph in excel**, the rather continuous form is simply an artifact of the human eye’s perception. And so it is continuous variation on polygenic traits: **as the number of loci increase, and their contribution to the sum totality of a trait decrease in average effect, they simulate the [Central Limit Theorm](https://en.wikipedia.org/wiki/Central_limit_theorem)**, and approach a [normal distribution](https://en.wikipedia.org/wiki/Normal_distribution). I like using the binomial distribution not only for its simplicity, but also because it too can approach the normal distribution as the *n* approaches ∞.  
We perceive genetic variation as continuous, but its fundamental nature is discrete. Similarly, our everyday life is governed by the continuous motion of Newtonian Mechanics which is so well approximated by the calculus, but at its basic core the physical universe consists of discrete packets.

### Related Posts:

- [Personal Genome
  Project](https://www.gnxp.com/WordPress/2007/12/03/personal-genome-project/) - [Fisher web](https://www.gnxp.com/WordPress/2006/02/27/fisher-web/) - [Brown + Brown = Black &
  White](https://www.gnxp.com/WordPress/2009/01/05/brown-brown-black-white/) - [Skin deep, why I'm brown and you wish you
  were](https://www.gnxp.com/WordPress/2006/09/25/skin-deep-why-im-brown-and-you-wish-you-were/) - [Applied genetics & your
  life](https://www.gnxp.com/WordPress/2006/07/02/applied-genetics-your-life/) - [Can you tell if you're black or
  white?](https://www.gnxp.com/WordPress/2006/09/27/can-you-tell-if-youre-black-or-white/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2006%2F09%2F29%2Fdiscrete-continuity-in-genetics%2F&linkname=Discrete%20continuity%20in%20genetics "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2006%2F09%2F29%2Fdiscrete-continuity-in-genetics%2F&linkname=Discrete%20continuity%20in%20genetics "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2006%2F09%2F29%2Fdiscrete-continuity-in-genetics%2F&linkname=Discrete%20continuity%20in%20genetics "Email")[](https://www.addtoany.com/share)
