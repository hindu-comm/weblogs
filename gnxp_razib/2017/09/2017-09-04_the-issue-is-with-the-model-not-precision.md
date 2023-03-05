+++
title = "The issue is with the"
full_title = "The issue is with the model, not precision!"
date = "2017-09-04"
upstream_url = "https://www.gnxp.com/WordPress/2017/09/04/the-issue-is-with-the-model-not-precision/"

+++
Source: [here](https://www.gnxp.com/WordPress/2017/09/04/the-issue-is-with-the-model-not-precision/).

The issue is with the model, not precision!

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/exploringpersonalgenomics.jpeg?resize=196%2C257)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/exploringpersonalgenomics.jpeg?resize=196%2C257)](https://www.amazon.com/exec/obidos/ASIN/0199644497/geneexpressio-20)[The Wirecutter](http://thewirecutter.com/reviews/best-dna-ancestry-testing-kit/) has a [thorough review](http://thewirecutter.com/reviews/best-dna-ancestry-testing-kit/) of direct-to-consumer ancestry testing services. Since I now work at a human personal genomics company I’m not going to comment on the merits of any given service. But, **I do want to clarify something in regards to the precision of these tests.** Before the author quotes Jonathan Marks, he says:

> For Jonathan Marks, anthropology professor at University of North > Carolina at Charlotte, the big unknown for users is the **margin for > error with these estimates….**

The issue I have with this quote is that **the margin of error on these tests is really not that high**. [Margin of error](https://en.wikipedia.org/wiki/Margin_of_error#Basic_concept) itself is a precise concept. If you sample 1,000 individuals you’ll have a lower margin of error than if you sample 100 individuals. That’s common sense.

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/phylogenomicsprimer.jpeg?resize=198%2C255)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/phylogenomicsprimer.jpeg?resize=198%2C255)](https://www.amazon.com/exec/obidos/ASIN/081534211X/geneexpressio-20)But for direction-to-consumer genomic tests you are sampling 100,000 to 1 million markers on SNP arrays (the exact number used for ancestry inference is often lower than the total number on the array). For ancestry testing you are really interested in the 10 million or so (order of magnitude) markers which vary between population, and a random sampling of 100,000 to 1 million is going to be pretty representative (consider that election year polling usually surveys a few thousand people to represent an electorate of tens of millions).

If you run a package like [Admixture](https://www.genetics.ucla.edu/software/admixture/) you can repeat the calculation for a given individual multiple times. In most cases there is very little variation between replicates in relation to the percentage breakdowns, even though you do a random seed to initialize the process as it begins to stochastically explore the parameter space (the variance is going to be higher if you try to resolve clusters which are extremely phylogenetically close of course).

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/treethinking.jpeg?resize=198%2C255)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/treethinking.jpeg?resize=198%2C255)](https://www.amazon.com/exec/obidos/ASIN/1936221160/geneexpressio-20)As I have stated before, **the reason these different companies offer varied results is that they start out with different models**. When I learned the basic theory around phylogenetics in graduate school the philosophy was definitely Bayesian; vary the model parameters **and** the model and see what happens. But you can’t really vary the model all the time between customers, can you? It starts to become a nightmare in relation to customer service.

There are certain population clusters that customers are interested in. To provide a service to the public a company has to develop a model that answers those questions which are in demand. If you are designing a model for purely scientific purposes then you’d want to highlight the maximal amount of phylogenetic history. That isn’t always the same though as the history that customers want to know about it. This means that direct-to-consumer ethnicity tests in terms of the specification of their models deviate from pure scientific questions, **and result in a log of judgment calls based on company evaluations of their client base**.

**Addendum:** There is a lot of talk about the reference population sets. The main issue is representativeness, not sample size. You don’t really need more than 10-100 individuals from a given population in most cases. But you want to sample the real population diversity that is out there.

### Related Posts:

- [If you are not too stupid you can be in
  Mensa](https://www.gnxp.com/WordPress/2012/04/17/if-you-are-not-too-stupid-you-can-be-in-mensa/) - [Direct-to-consumer genomics, it's back
  on!](https://www.gnxp.com/WordPress/2017/04/07/direct-to-consumer-genomes-its-back-on/) - [Two opinions on D.T.C. personal genomic
  testing](https://www.gnxp.com/WordPress/2011/04/17/two-opinions-on-d-t-c-personal-genomic-testing/) - [My personal
  DNA](https://www.gnxp.com/WordPress/2006/04/17/my-personal-dna/) - [Ban them! (including ancestry
  analysis)](https://www.gnxp.com/WordPress/2011/05/31/ban-them-including-ancestry-analysis/) - [Genetic testing comment period, last
  day](https://www.gnxp.com/WordPress/2011/05/02/genetic-testing-comment-period-last-day/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F09%2F04%2Fthe-issue-is-with-the-model-not-precision%2F&linkname=The%20issue%20is%20with%20the%20model%2C%20not%20precision%21 "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F09%2F04%2Fthe-issue-is-with-the-model-not-precision%2F&linkname=The%20issue%20is%20with%20the%20model%2C%20not%20precision%21 "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F09%2F04%2Fthe-issue-is-with-the-model-not-precision%2F&linkname=The%20issue%20is%20with%20the%20model%2C%20not%20precision%21 "Email")[](https://www.addtoany.com/share)
