+++
title = "Why do percentage"
full_title = "Why do percentage estimates of “ancestry” vary so much?"
date = "2017-08-29"
upstream_url = "https://www.gnxp.com/WordPress/2017/08/29/why-do-percentage-estimates-of-ancestry-vary-so-much/"

+++
Source: [here](https://www.gnxp.com/WordPress/2017/08/29/why-do-percentage-estimates-of-ancestry-vary-so-much/).

Why do percentage estimates of “ancestry” vary so much?

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/08/dnatest.jpg?resize=600%2C651)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/08/dnatest.jpg?resize=600%2C651)](https://www.amazon.com/exec/obidos/ASIN/B00TRLVKW0/geneexpressio-20)

When looking at the results in [Ancestry DNA](https://www.amazon.com/exec/obidos/ASIN/B00TRLVKW0/geneexpressio-20), [23andMe](https://www.amazon.com/exec/obidos/ASIN/B01LZ5K87Z/geneexpressio-20), and [Family Tree DNA](https://www.amazon.com/exec/obidos/ASIN/B01NAQ1UCW/geneexpressio-20) my “East Asian” percentage is:

– 19%  
– 13%  
– 6%

What’s going on here? In science we often make a distinction between precision and accuracy. Precision is how much your results vary when you re-run an experiment or measurement. Basically, can you reproduce your result? Accuracy refers to how close your measurement is to the true value. A measurement can be quite precise, but consistently off. Similarly, a measurement may be imprecise, but it bounces around the true value…so it is reasonably accurate if you get enough measurements just cancel out the errors (which are random).

**[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/08/blaineftdna.jpeg?resize=197%2C256)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/08/blaineftdna.jpeg?resize=197%2C256)](https://www.amazon.com/exec/obidos/ASIN/B01M0S7C6U/geneexpressio-20)The values above are precise**. That is, if you got re-tested on a different chip, the results aren’t going to be much different. The tests are using as input variation on 100,000 to 1 million markers, so a small proportion will give different calls than in the earlier test. But that’s not going to change the end result in most instances, even though these methods often have a stochastic element.

But what about accuracy? I am not sure that old chestnuts about accuracy apply in this case, **because the percentages that these services provide are summaries and distillations of the underlying variation**. The model of precision and accuracy that I learned would be more applicable to the DNA SNP array which returns calls on the variants; that is, how close are the calls of the variant to the true value (last I checked these are arrays are around 99.5% accurate in terms of matching the true state).

What you see when these services pop out a percentage for a given ancestry is the outcome of a series of conscious choices that designers of these tests made keeping in mind what they wanted to get out of these tests. At a high level here’s what’s going on:

1.  You have a model of human population history and dynamics with
    various parameters 2.  You have data that that varies that you put into that model 3.  You have results which come back with values which are the best fit
    of that data to the model you specificed

**Basically you are asking the computational framework a question, and it is returning its best answer to the question posed**. To ask whether the answer is accurate or not is almost not even wrong. The frameworks vary because they are constructed by humans with difference preferences and goals.

Almost, but not totally wrong. You can for example simulate populations whose histories you know, and then test the models on the data you generated. Since you already know the “truth” about the simulated data’s population structure and history, you can see how well your framework can infer what you already know from the patterns of variation in the generated data.

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/08/Est100_1.jpg?resize=300%2C231)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/08/Est100_1.jpg?resize=300%2C231)](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/08/Est100_1.jpg)Going back to my results, **why do my East Asian percentages vary so much**? The short answer is that one of the major variables in the model alluded to above is the nature of the reference population set and the labels you give them.

Looking at Bengalis, the ethnic group I’m from, **it is clear that in *comparison* to other South Asian populations they are East Asian shifted**. That is, it seems clear I do have some East Asian ancestry. But how much?

The “simple” answer is to model my ancestry is a mix of two populations, an Indian one and an East Asian one, and then see what the values are for my ancestry across the two components. But here is where semantics becomes important: **what is Indian and East Asian**? Remember, these are just labels we give to groups of people who share genetic affinities. The labels aren’t “real”, the reality is in the raw read of the sequence. But humans are not capable of really getting anything from millions of raw SNPs assigned to individuals. We have to summarize and re-digest the data.

The simplest explanation for what’s going on here is that the different companies have different populations put into the boxes which are “Indian/South Asian” and “East Asian.” If you are using fundamentally different measuring sticks, then there are going to be problems with doing apples to apples comparisons.

**My personal experience is that 23andMe tends to give very high percentages of South Asian ancestry for all South Asians**. Because “South Asian” is a very diverse category when tests come back that someone is 95-99% South Asian…it’s not really telling you much. In contrast, some of the other services may be using a small subset of South Asians, who they define as “more typical”, and so giving lower percentages to people from Pakistan and Bengal, who have admixture from neighboring regions to the west and east respectively.\*

Something similar can occur with East Asian ancestry. If the “donor” ancestral groups are South Asian and East Asian for me, then the proportions of each is going to vary by how close the donor groups selected by the company is to the true ancestral group. If, for example,[Family Tree DNA](https://www.amazon.com/exec/obidos/ASIN/B01NAQ1UCW/geneexpressio-20)chose a more Northeastern Asian population than[Ancestry DNA](https://www.amazon.com/exec/obidos/ASIN/B00TRLVKW0/geneexpressio-20), then my East Asian population would vary between the two services because I know my East Asian ancestry is more Southeast Asian.

**The moral of the story is that the values you obtain are conditional on the choices you make**, and those choices emerge from the process of reducing and distilling the raw genetic variation into a manner which is human interpretable. If the companies decided to use the same model, the would come out with the same results.

\* I helped develop an earlier version of MyOrigins, and so can attest to this firsthand.

### Related Posts:

- [On being a
  pundit](https://www.gnxp.com/WordPress/2012/09/05/on-being-a-pundit/) - [Why I avoid processed
  foods](https://www.gnxp.com/WordPress/2010/01/06/why-i-avoid-processed-foods/) - [Race, TNR
  debate](https://www.gnxp.com/WordPress/2007/06/15/race-tnr-debate/) - [Notes on Sewall Wright: Wright's
  F-statistics](https://www.gnxp.com/WordPress/2008/05/20/notes-on-sewall-wright-wrights-f-statistics/) - [Our family's pedigree in
  23andMe](https://www.gnxp.com/WordPress/2018/04/05/our-familys-pedigree-in-23andme/) - [Three admixture recipes for Razib
  Khan](https://www.gnxp.com/WordPress/2016/02/12/three-admixture-recipes-for-razib-khan/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F08%2F29%2Fwhy-do-percentage-estimates-of-ancestry-vary-so-much%2F&linkname=Why%20do%20percentage%20estimates%20of%20%E2%80%9Cancestry%E2%80%9D%20vary%20so%20much%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F08%2F29%2Fwhy-do-percentage-estimates-of-ancestry-vary-so-much%2F&linkname=Why%20do%20percentage%20estimates%20of%20%E2%80%9Cancestry%E2%80%9D%20vary%20so%20much%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F08%2F29%2Fwhy-do-percentage-estimates-of-ancestry-vary-so-much%2F&linkname=Why%20do%20percentage%20estimates%20of%20%E2%80%9Cancestry%E2%80%9D%20vary%20so%20much%3F "Email")[](https://www.addtoany.com/share)
