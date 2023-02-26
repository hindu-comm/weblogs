+++
title = "You only go extinct"
full_title = "You only go extinct once…"
date = "2006-10-29"
upstream_url = "https://www.gnxp.com/WordPress/2006/10/29/you-only-go-extinct-once/"

+++
Source: [here](https://www.gnxp.com/WordPress/2006/10/29/you-only-go-extinct-once/).

You only go extinct once….

Assume that you have a new mutation, totally novel. What’s its probability of going extinct in one generation? That is, it doesn’t get passed on….  
Consider, you have a population of *N* individuals. Fix the population size across nonoverlapping generations. So, in generation *t* you have *N* individuals and in *t* + 1 you have *N* individuals. In the first generation of the mutation the proportion in the population is 1/*N*, that is, there is one mutant amongst *N* individuals (ergo, *N* – 1 other copies). The probability that the mutant is never “drawn” (copied) to the next generation in this fixed population is (1 – 1/*N*)^(*N*). 1 – 1/*N* represents the non-mutants, and there are *N* draws since the population across generations is fixed. For example, if there are 100 individuals (haploid) and 99 are non-mutants, and the next generation will also have 100 individuals, there are 100 opportunities for the 99 out of 100 *instead* of the 1 out of 100 to be drawn, i.e., (1 – 0.01)^(*100*).  
This equation converges upon \~ 0.37 as *N* approaches ∞. Here are some values generated for a given *N*:  
10 → 0.34867844  
100 → 0.366032341  
1000 → 0.367695425  
10000 → 0.367861046

  
In other words, **for a neutral allele the probability of extinction in one generation is relatively insensitive to population size**. Also, 0.367861046… is equivalent to 1/*e*. An assumption of the above model is that the mean number of offspring is 1, and that the variance is [Poisson distributed](https://en.wikipedia.org/wiki/Poisson_distribution), in other words the variance and mean are the same. What about selection, which would alter the mean? (i.e., shift up the expectation of offspring for an individual about or below the mean)  
The model then becomes approximately 1/*e* X ( 1 – *s*), where *s* is the selection coefficient (e.g., *s* of 0.10 \~ 10% increased fitness vs. population mean, in this case, 1.1 instead of 1 as expectation). Plugging in….  
0.001 → 0.37  
0.01 → 0.36  
0.10 → 0.33  
0.20 → 0.29  
0.30 → 0.26  
0.40 → 0.22  
0.50 → 0.18  
As you can see, a fitness advantage for a new mutant reduces its probability of extinction in one generation, but it is still non-trivial even if it increases fitness half-again! This is important because empirically we know that a fitness increase of 0.10 is **extremely powerful**. I incremented up to 0.50 simply for illustrative purposes, biologically 0.01 to 0.10 is probably the norm. And, as you can see the risk of extinction does not decrease much with such a selective value. It’s a hard world out there for a new mutant trying to make a go of it, and the fates aren’t kind. The risk of extinction is high, and as you know **the probability of fixation for a new allele in a diploid organism is 2*s***. That is, if it confers a 0.10 fitness advantage its chance of sweeping through the population is only 20%, ergo, its chance of extinction is 80%!  
**Note:** Adapted from chapter 5 of [Evolutionary Genetics: Concepts & Case Studies](https://www.amazon.com/exec/obidos/ASIN/0195168186/geneexpressio-20).

### Related Posts:

- [My
  fixations](https://www.gnxp.com/WordPress/2006/08/06/my-fixations/) - [Hold one hand still, move the
  other](https://www.gnxp.com/WordPress/2006/03/03/hold-one-hand-still-move-the-other/) - [Selection on a quantitative
  trait](https://www.gnxp.com/WordPress/2007/06/25/selection-on-a-quantitative-trait/) - [Misconceptions in evolutionary
  biology](https://www.gnxp.com/WordPress/2006/02/01/misconceptions-in-evolutionary-biology/) - [Can't have genetic drift without the
  other....](https://www.gnxp.com/WordPress/2006/04/17/cant-have-genetic-drift-without-the-other/) - [Will an infection become an epidemic? A simple
  model](https://www.gnxp.com/WordPress/2007/03/28/will-an-infection-become-an-epidemic-a-simple-model/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2006%2F10%2F29%2Fyou-only-go-extinct-once%2F&linkname=You%20only%20go%20extinct%20once%E2%80%A6. "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2006%2F10%2F29%2Fyou-only-go-extinct-once%2F&linkname=You%20only%20go%20extinct%20once%E2%80%A6. "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2006%2F10%2F29%2Fyou-only-go-extinct-once%2F&linkname=You%20only%20go%20extinct%20once%E2%80%A6. "Email")[](https://www.addtoany.com/share)
