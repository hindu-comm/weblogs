+++
title = "Direct measurement of"
full_title = "Direct measurement of the genetic contribution to the BW IQ gap"
date = "2007-01-29"
upstream_url = "https://www.gnxp.com/WordPress/2007/01/29/direct-measurement-of-the-genetic-contribution-to-the-bw-iq-gap/"

+++
Source: [here](https://www.gnxp.com/WordPress/2007/01/29/direct-measurement-of-the-genetic-contribution-to-the-bw-iq-gap/).

Direct measurement of the genetic contribution to the BW IQ gap

To follow-up on two older posts, here is a comment on the direct tests of the genetic contribution to the Black-White IQ gap that were proposed by [David Rowe](https://www.gnxp.com/blog/2006/11/david-rowes-final-paper.php) and [Charles Murray](https://www.gnxp.com/blog/2006/11/black-white-iq-gap-is-it-closing-will.php). Each appears to be describing the same set of experiments. The aim of these experiments is to ascertain the relative contribution of genes versus environment to the Black-White IQ gap, or put another way they aim to measure the [between-group heritability (BGH)](https://www.google.com/search?q=between-group+heritability) of IQ.

The easiest way to explain what they are proposing is to steal a bit of text from a paper describing the analogous experiments for a different phenotype (lung cancer):

> The explanation for the observed racial or ethnic variation remains to > be determined. Unmeasured environmental variations, genetic > differences, or both may be involved. Dissection of disparities among > racial and ethnic groups is complicated by the strong correlation > between the socioenvironmental and genetic factors that differentiate > these groups, with few persons differentially classified.2,8 However, > a number of approaches can be taken. One approach is based on the > recognition of mixed continental ancestry among persons > self-identified as African American or Latino. … Despite being > genetically separable from whites, African Americans show a range of > European ancestry that extends from nearly 0 percent to greater than > 50 percent.9 Other studies have shown similar trends, with an average > of about 20 percent European ancestry.10 Latinos are even more > complex, comprising variable proportions of indigenous ancestry from > three continental regions (Europe, the Americas, and Africa).11 Within > these populations, individual ancestry can be estimated with the use > of numerous ancestry-informative genetic markers; once established, > this information can be used to examine correlations between the > ancestry estimates and the trait of interest. > [\[source\]](http://content.nejm.org/cgi/content/full/354/4/408)

Rowe and Murray each suggest examining the correlation between ancestry estimates (individual ancestry, or IA) and IQ. These experiments have not been done using the techniques of modern DNA genotyping, but they have been proposed for some time. Here’s my question: what would be the expected correlation between IA and IQ for a given BGH? A naive answer is that r = BGH. However, this is quite unlikely to be the case.

This question has been asked in a related context, so I’ll have to introduce more background to get us closer to an answer. While direct DNA genotyping has not been used to examine the IA-IQ correlation, other (less reliable) measures of IA have been used. Skin color is a prominent and notable example. Most recently, using data from the GSS, Lynn found a correlation of r=.17 between verbal IQ and skin color.\[1\] (I unknowingly [replicated this finding in a previous post.](https://www.gnxp.com/blog/2006/09/skin-color-and-iq-in-gss.php)) What is the implication of a correlation of skin-color and IQ of this magnitude to BGH? Jensen had previously considered this question.\[2\] In that context, Jensen estimates that the IA-IQ correlation should be around 0.5 and that the IQ-skin color correlation should be no more than about 0.2. Jensen’s 0.2 figure is based on an under-estimate of the IA-skin color correlation that is found using DNA markers and electronic measurement of skin color (decades later). (However, Lynn’s skin color data comes from self-estimates on a 5-point scale, and so Jensen’s numbers may be appropriate.) However, Jensen does not offer an explanation for how he arrives at a value of 0.5 for the IA-IQ correlation, and so it’s not clear what factors Jensen is taking into account. Jensen offers other reasons to downplay the importance of the IQ-skin color correlation as being informative about BGH. I’ll again steal text from the lung cancer review to explain the point:

> Such analyses are not without caveats, however. Even within an > apparently homogeneous admixed group, individual ancestry may remain > correlated with environmental risk factors.8 This is most likely to be > the case when ancestry is apparent or known, but less likely when it > is cryptic. For example, in African Americans, skin pigment is > correlated with the degree of European ancestry12 and may therefore > lead to residual confounding. > [\[source\]](http://content.nejm.org/cgi/content/full/354/4/408)

Getting back to the question: what would be the expected correlation between IA and IQ for a given BGH? I don’t know how to derive a formula to compute this directly, but it is easy enough to run simulations of the data. Jensen’s estimate of 0.5 is at the upper end of the values that I computed for BGH=100%. Why not r=1? The predominant reason is that IQ varies in the African American population for reasons in addition to variation in IA. It is difficult to know how much variation in IQ occurs at a given level of IA, but a lower bound estimate comes from the variation in IQ of siblings. Full siblings share the same level of IA (more than that, they are \~50% identical by descent), but show a substantial amount of variation in IQ. A common estimate I’ve seen is an average difference of 12 points among white siblings. Unrelated individuals with identical IA will vary at least this much (further correction for the lower overall variance in the Black population is needed). Factors of study design will also attenuate the IA-IQ correlation. While “Black” individuals may be found at all levels of IA, the actual population distribution of IA is clustered around 20% European / 80% West African ancestry; thus the range of IA measured will probably be restricted. Also, IQ scores have excellent but imperfect reliability, further attenuating the correlation. My attempts at simulating the IA-IQ correlation suggest that even if BGH=100%, the IA-IQ correlation might be as low as r=0.25. Jensen estimates BGH in the range of 50-75%, further reducing the IA-IQ correlation.There are other caveats, and possible way around these problems (MALD). From the lung-cancer review:

> Another caveat is that an estimate of individual ancestry from the > entire genome may be misleading if the racial or ethnic difference is > due to one or a small number of genes.13 However, this is also an > attractive scenario, since the same collection of markers could be > used to pinpoint specific genetic locations involved in the difference > (admixture mapping).10 In this case, the likelihood of residual > confounding is reduced.13 > [\[source\]](http://content.nejm.org/cgi/content/full/354/4/408)

MALD may be the best hope of circumventing the confounding of skin color with ancestry — the problem identified by Jensen, and later directed as criticism of Lynn’s conclusions\[3\]. If black-white skin color differences are mapped to a few loci of large effect (e.g. SLC24A5) then it should be possible to examine their effects in the MALD analysis. However, this all seems far from simple.

References:  
\[1\] Lynn, R. (2002). Skin color and intelligence in African Americans. [Population and Environment, 23, 365-375.](https://dx.doi.org/10.1023/A:1014572602343)  
\[2\] Jensen, A. R. (1973). Educability and Group Differences. London: Methuen.  
\[3\] Hill, M. E. (2004). Skin Color and Intelligence in African Americans: A Reanalysis of Lynn’s Data. [Population and Environment, 24, 209-214.](https://dx.doi.org/10.1023/A:1020704322510)

Update:

Here’s a figure that explains MALD in a case-control context:

[](https://www.gnxp.com/blog/uploaded_images/nrg1657-f1-710638.gif)

> Figure 1 \| Detecting disease-associated gen  
> omic regions using mapping by admixture linkage disequilibrium. a \| > The strategy that is used to assess the ancestral origin of > chromosomal segments in mapping by admixture linkage disequilibrium > (MALD)7, 13, 15 . Genotyping MALD markers is used to assess parental > ancestry across a single chromosome in multiple cases (individuals > with the disease of interest) versus matched healthy controls. The > region indicated by the star is derived more often from one of the > parental populations only in the disease cases, indicating that this > region contains a disease-susceptibility locus. In the controls, the > same region has an equal probability of originating from either > parental population. b \| A theoretical example of how an admixture > signal can be detected using the MALD method for a disease with a > higher incidence in one parental population (population A). The > proportion of ancestry from population A in multiple individuals (both > with the disease (cases) and without the disease (controls)) is shown > schematically for different positions on a single chromosome. An > elevated ancestry proportion from population A in cases is evident at > the peak (marked by an arrow), which indicates the involvement of the > corresponding genomic region in the disease. The peak can be > identified by the higher (or lower; not shown) level of ancestry that > is seen in cases relative to the same region in controls, and/or > relative to the remainder of the genome in cases (only the > neighbouring chromosomal region is shown here). Part b is modified, > with permission, from Ref. 13 Â© (2004) The University of Chicago > Press.  
> Â© 2005 Nature Publishing Group

[\[source\]](http://www.nature.com/nrg/journal/v6/n8/abs/nrg1657_fs.html)

### Related Posts:

- [Narrowing of the white-black IQ
  gap?](https://www.gnxp.com/WordPress/2006/08/13/narrowing-of-the-white-black-iq-gap/) - [Charles Murray's latest paper on changes in
  the…](https://www.gnxp.com/WordPress/2007/03/25/charles-murray-s-latest-paper-on-changes-in-the-black-white-iq-gap-over-time/) - [Stereotype
  Fret](https://www.gnxp.com/WordPress/2006/09/04/stereotype-fret/) - [The Black-White IQ Gap: Is It Closing? Will It Ever Go
  Away?](https://www.gnxp.com/WordPress/2006/11/29/the-black-white-iq-gap-is-it-closing-will-it-ever-go-away/) - [Skin color and IQ in the
  GSS](https://www.gnxp.com/WordPress/2006/09/29/skin-color-and-iq-in-the-gss/) - [History and Geography of Genes on a
  Desktop](https://www.gnxp.com/WordPress/2010/10/25/history-and-geography-of-genes-on-a-desktop/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F01%2F29%2Fdirect-measurement-of-the-genetic-contribution-to-the-bw-iq-gap%2F&linkname=Direct%20measurement%20of%20the%20genetic%20contribution%20to%20the%20BW%20IQ%20gap "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F01%2F29%2Fdirect-measurement-of-the-genetic-contribution-to-the-bw-iq-gap%2F&linkname=Direct%20measurement%20of%20the%20genetic%20contribution%20to%20the%20BW%20IQ%20gap "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F01%2F29%2Fdirect-measurement-of-the-genetic-contribution-to-the-bw-iq-gap%2F&linkname=Direct%20measurement%20of%20the%20genetic%20contribution%20to%20the%20BW%20IQ%20gap "Email")[](https://www.addtoany.com/share)
