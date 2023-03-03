+++
title = "Why are most genetic"
full_title = "Why are most genetic associations found through candidate gene studies wrong?"
date = "2009-06-21"
upstream_url = "https://www.gnxp.com/WordPress/2009/06/21/why-are-most-genetic-associations-found-through-candidate-gene-studies-wrong/"

+++
Source: [here](https://www.gnxp.com/WordPress/2009/06/21/why-are-most-genetic-associations-found-through-candidate-gene-studies-wrong/).

Why are most genetic associations found through candidate gene studies wrong?

In [a recent post](https://www.gnxp.com/blog/2009/06/another-candidate-gene-association.php), I made a blanket statement that the vast majority of candidate gene association studies published in psychiatric genetics (actually, in nearly all fields of genetics) are wrong. I’m not just being offhandedly dismissive–below, I outline the statistical argument behind that claim. This discussion is cribbed almost verbatim from [a discussion of the issue by statisticians at the Welcome Trust](http://www.nature.com/nature/journal/v447/n7145/box/nature05911_BX1.html).

Let’s assume that there are a finite number of loci in genome, and we test some number of those (in a genome-wide association study, this is on the order of 500K-1M; in a candidate gene study it’s more likely in the tens. But the actual marker density is irrelevant for what follows) for association with some phenotype of interest. In general, the criterion used to decide if one has discovered a true association is the [p-value](https://en.wikipedia.org/wiki/P-value), or the probability of seeing the data that you have given that there is no association. But that’s not really the quantity you’re interested in. The real quantity of interest is the probability that there’s a true association given the data you see–the inverse of what’s being reported.

By [Bayes’ Law](https://en.wikipedia.org/wiki/Bayes%27_theorem), this probability depends on the prior probability of an association at that marker, the p-value threshold you’ve chosen to call a finding “significant”, and crucially, the [power](https://en.wikipedia.org/wiki/Statistical_power) you had to detect the association \[1\]\[[2](http://jnci.oxfordjournals.org/cgi/content/full/96/6/434#FD1)\]. **Thus, the interpretation of a given p-value depends on the power to detect an association, such that the lower your power, the lower the probability that a “significant” association is true** \[3\].

That’s where recent evidence from large genome-wide association studies comes into play. For nearly all diseases, reproducible associations have small effect size and are only detectable when one has sample sizes in the thousands or tens of thousands (for many psychiatric phenotypes, even studies with these sample sizes don’t seem to find much). The vast majority of candidate gene association studies had sample sizes in the low hundreds, and thus had essentially zero power to detect the true associations. By the argument above, in this situation the probability that a “significant” association is real approaches zero. **The problem with candidate gene association studies is not that they were only targeting candidate genes, *per se*, but rather that they tended to have small sample sizes and were woefully underpowered to detect true associations.**

\[1\] Let D be the data, T be the event that an association is true, t, be the event that an association is not true, and P(T) be the prior probability that an association is true.

P(T\|D) = P(D\|T)P(T) / \[ P(D\|T) P(T) + P(D\|t) (1-P(T) \]

P(D\|T) is the power, and P(D\|t) is the p-value. Clearly, both are relevant here.

\[2\] http://jnci.oxfordjournals.org/cgi/content/full/96/6/434#FD1

\[3\] As the authors note,

> A key point from both perspectives is that interpreting the strength > of evidence in an association study depends on the likely number of > true associations, and the power to detect them which, in turn, > depends on effect sizes and sample size. In a less-well-powered study > it would be necessary to adopt more stringent thresholds to control > the false-positive rate. Thus, when comparing two studies for a > particular disease, with a hit with the same MAF and P value for > association, the likelihood that this is a true positive will in > general be greater for the study that is better powered, typically the > larger study. **In practice, smaller studies often employ less > stringent P-value thresholds, which is precisely the opposite of what > should occur**.

### Related Posts:

- [Interpreting genetic association
  studies](https://www.gnxp.com/WordPress/2009/09/19/interpreting-genetic-association-studies/) - [Following up association
  studies](https://www.gnxp.com/WordPress/2008/10/06/following-up-association-studies/) - [Duffy and malaria in
  baboons?](https://www.gnxp.com/WordPress/2009/06/24/duffy-and-malaria-in-baboons/) - [Another candidate gene association bites the
  dust](https://www.gnxp.com/WordPress/2009/06/16/another-candidate-gene-association-bites-the-dust/) - [Asia finally getting in on the genome-wide association
  game?](https://www.gnxp.com/WordPress/2008/08/18/asia-finally-getting-in-on-the-genome-wide-association-game/) - [A success for genome-wide assciation
  studies?](https://www.gnxp.com/WordPress/2008/07/02/a-success-for-genome-wide-assciation-studies/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F06%2F21%2Fwhy-are-most-genetic-associations-found-through-candidate-gene-studies-wrong%2F&linkname=Why%20are%20most%20genetic%20associations%20found%20through%20candidate%20gene%20studies%20wrong%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F06%2F21%2Fwhy-are-most-genetic-associations-found-through-candidate-gene-studies-wrong%2F&linkname=Why%20are%20most%20genetic%20associations%20found%20through%20candidate%20gene%20studies%20wrong%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F06%2F21%2Fwhy-are-most-genetic-associations-found-through-candidate-gene-studies-wrong%2F&linkname=Why%20are%20most%20genetic%20associations%20found%20through%20candidate%20gene%20studies%20wrong%3F "Email")[](https://www.addtoany.com/share)
