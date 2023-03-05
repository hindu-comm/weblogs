+++
title = "Natural selection in"
full_title = "Natural selection in humans"
date = "2017-12-20"
upstream_url = "https://www.gnxp.com/WordPress/2017/12/20/natural-selection-in-humans-ok-375000-british-people/"

+++
Source: [here](https://www.gnxp.com/WordPress/2017/12/20/natural-selection-in-humans-ok-375000-british-people/).

Natural selection in humans (OK, 375,000 British people)

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/12/select1.png?resize=625%2C289&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/12/select1.png?resize=625%2C289&ssl=1)](http://www.pnas.org/content/early/2017/12/12/1707227114.abstract)

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/12/selec2.jpg?resize=300%2C265&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/12/selec2.jpg?resize=300%2C265&ssl=1)](http://www.pnas.org/content/early/2017/12/12/1707227114.abstract)  
The above figure is from [Evidence of directional and stabilizing selection in contemporary humans](http://www.pnas.org/content/early/2017/12/12/1707227114.abstract). I’ll be entirely honest with you: **I don’t read every UK Biobank paper, but I do read those where Peter Visscher is a co-author.** It’s in *PNAS*, and a draft which is [not open access](https://en.wikipedia.org/wiki/Sci-Hub). But it’s a pretty interesting read. Nothing too revolutionary, but confirms some intuitions one might have.

The abstract:

> Modern molecular genetic datasets, primarily collected to study the > biology of human health and disease, can be used to directly measure > the action of natural selection and reveal important features of > contemporary human evolution. Here we leverage the UK Biobank data to > test for the presence of linear and nonlinear natural selection in a > contemporary population of the United Kingdom. We obtain phenotypic > and genetic evidence consistent with the action of linear/directional > selection. **Phenotypic evidence suggests that stabilizing selection, > which acts to reduce variance in the population without necessarily > modifying the population mean, is widespread and relatively weak in > comparison with estimates from other species**.

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/11/principlesofpopgen-1.jpeg?resize=198%2C255&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/11/principlesofpopgen-1.jpeg?resize=198%2C255&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/0878933085/geneexpressio-20)The stabilizing selection part is probably the most interesting part for me. But let’s hold up for a moment, and review some of the major findings. The authors focused on \~375,000 samples which matched their criteria (white British individuals old enough that they are well past their reproductive peak), and the genotyping platforms had 500,000 markers. The dependent variable they’re looking at is reproductive fitness. In this case specifically, “rRLS”, or relative reproductive lifetime success.

With these huge data sets and the large number of measured phenotypes they first used the classical [Lande and Arnold](http://people.oregonstate.edu/~arnoldst/pdf_files/Lande%20&%20Arnold%201983.pdf) method to detect selection gradients, which leveraged regression to measure directional and stabilizing dynamics. Basically, how does change in the phenotype impact reproductive fitness? So, it is notable that shorter women have higher reproductive fitness than taller women (shorter than the median). This seems like a robust result. We’ve seen it before on much smaller sample sizes.

The results using phenotypic correlations for direction (*β*) and stabilizing (*γ*) selection are shown below separated by sex. The abbreviations are the same as above.

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/12/bothergreek.jpg?resize=625%2C241&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/12/bothergreek.jpg?resize=625%2C241&ssl=1)](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/12/bothergreek.jpg?ssl=1)

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/introquantgenetics.jpeg?resize=177%2C285&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/introquantgenetics.jpeg?resize=177%2C285&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/0582243025/geneexpressio-20)There are many cases where directional selection seems to operate in females, but not in males. But they note that that is often due to near zero non-significant results in males, not because there were opposing directions in selection. Height was the exception, with regression coefficients in opposite directions. For stabilizing selection there was no antagonistic trait.

**A major finding was that compared to other organisms stabilizing selection was very weak in humans**. There’s just not that that much pressure against extreme phenotypes. This isn’t entirely surprising. First, you have the issue of the weirdness of a lot of studies in animal models, with inbred lines, or wild populations selected for their salience. Second, prior theory suggests that a trait with lots of heritable quantitative variation, like height, shouldn’t be subject to that much selection. If it had, the genetic variation which was the raw material of the trait’s distribution wouldn’t be there.

Using more complex regression methods that take into account confounds, they pruned the list of significant hits. But, it is important to note that even at \~375,000, this sample size might be underpowered to detect really subtle dynamics. Additionally, **the beauty of this study is that it added modern genomic analysis to the mix**. Detecting selection through phenotypic analysis goes back decades, but interrogating the genetic basis of complex traits and their evolutionary dynamics is new.

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/11/lynch.jpeg?resize=195%2C258&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/11/lynch.jpeg?resize=195%2C258&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/0878934812/geneexpressio-20)To a first approximation, the results were broadly consonant across the two methods. But, there are interesting details where they differ. There is selection on height in females, but not in males. This implies that though empirically you see taller males with higher rLSR, the genetic variance that is affecting height isn’t correlated with rLSR, so selection isn’t occurring in this sex.

\~375,000 may seem like a lot, but from talking to people who work in polygenic selection there is still statistical power to be gained by going into the millions (perhaps tens of millions?). These sorts of results are very preliminary but show the power of synthesizing classical quantitative genetic models and ways of thinking with modern genomics. And, it does have me wondering about how these methods will align with the sort of stuff I wrote about last year which [detects recent selection on time depths of a few thousand years](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5182071/). The SDS method, for example, seems to be detecting selection for increasing height the world over…which I wonder is some artifact, because there’s a robust pattern of shorter women having higher fertility in studies going back decades.

### Related Posts:

- [More detecting natural
  selection](https://www.gnxp.com/WordPress/2007/06/18/more-detecting-natural-selection/) - [Humans still evolving,
  etc.](https://www.gnxp.com/WordPress/2009/10/19/humans-still-evolving-etc/) - [More skepticism of natural
  selection](https://www.gnxp.com/WordPress/2009/03/30/more-skepticism-of-natural-selection/) - [Natural selection and cultural rates of
  change](https://www.gnxp.com/WordPress/2008/02/19/natural-selection-and-cultural-rates-of-change/) - [And you shall be as gods, knowing additive
  and…](https://www.gnxp.com/WordPress/2016/02/12/and-you-shall-be-as-gods-knowing-additive-and-independent/) - [Evolution of Primate
  Regulation](https://www.gnxp.com/WordPress/2008/11/21/evolution-of-primate-regulation/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F12%2F20%2Fnatural-selection-in-humans-ok-375000-british-people%2F&linkname=Natural%20selection%20in%20humans%20%28OK%2C%20375%2C000%20British%20people%29 "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F12%2F20%2Fnatural-selection-in-humans-ok-375000-british-people%2F&linkname=Natural%20selection%20in%20humans%20%28OK%2C%20375%2C000%20British%20people%29 "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F12%2F20%2Fnatural-selection-in-humans-ok-375000-british-people%2F&linkname=Natural%20selection%20in%20humans%20%28OK%2C%20375%2C000%20British%20people%29 "Email")[](https://www.addtoany.com/share)
