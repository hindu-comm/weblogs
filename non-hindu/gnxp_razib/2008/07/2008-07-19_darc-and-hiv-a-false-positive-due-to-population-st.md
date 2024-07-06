+++
title = "DARC and HIV a false"
full_title = "DARC and HIV a false positive due to population structure?"
date = "2008-07-19"
upstream_url = "https://www.gnxp.com/WordPress/2008/07/19/darc-and-hiv-a-false-positive-due-to-population-structure/"

+++
Source: [here](https://www.gnxp.com/WordPress/2008/07/19/darc-and-hiv-a-false-positive-due-to-population-structure/).

DARC and HIV: a false positive due to population structure?

The [recent report](https://dx.doi.org/10.1016/j.chom.2008.06.002) that the Duffy null allele is associated with increased risk of HIV infection recieved a lot of press (see Razib’s comments on it [here](http://scienceblogs.com/gnxp/2008/07/evolution_a_reason_for_the_afr.php)), mostly positive. In Nick Wade’s New York Times [article](http://www.nytimes.com/2008/07/17/science/17hiv.html?_r=1&ref=science&oref=slogin) on the paper, however, some smart people publicly express some doubts. It’s a tribute to Wade that he actually tries to summarize those doubts in the limited space allotted to him:

> Dr. Goldstein said that in parts of the United States, > African-Americans have a higher infection rate than > European-Americans, and that patients with a higher proportion of > African genes may be more vulnerable to H.I.V. for reasons unconnected > to the SNP. Nonetheless, the SNP would show up in a greater proportion of infected people simply because of their African heritage. If so, the gene’s apparent association with H.I.V. infection could be just coincidental, not causal.

In somewhat more technical terms, the issue referred to here is the potential for false positives in an association study due to population structure\[1\]. The issues involved in accounting for structure in an admixture mapping study are somewhat more subtle than in a classic case-control study, but are generally similar. In particular, it’s important to take individual levels of admixture into account\[2\]; this is generally done by including an estimate of individual admixture as a covariate in any regression model.

The authors are aware of this potential confounder, and develop a measure of admixture based on 11 SNPs to include as a covariate in their regression. However, this measure is kind of weak, which I imagine in the sticking point for the skeptics in the *Times* article. If you have access to the supplemental information, take a look at it–several of these 11 SNPs are in the same gene, which means they’re not independent, and several don’t even have big frequency differences between African and European samples (if you’re trying to judge via SNPs whether someone is more African or European, those SNPs better have a big frequency difference between Africa and Europe). This is probably not a precise measure of ancestry. In fact, **the Duffy null allele they claim as associated is a better predictor of ancestry than any of these SNPs**.

So it’s quite possible that the authors have simply shown a correlation between level of African ancestry and susceptibility to HIV (which could be due to any number of sociological, demographic, or genetic factors), rather than an association between Duffy null and susceptibility to HIV. Here’s a relatively simple test of this possibility: genotype rs1426654 (the nonsynonymous SNP in [SLC24A5](https://www.google.com/search?ie=UTF-8&oe=UTF-8&q=slc24a5&btnG=With+Google&domains=gnxp.com&sitesearch=gnxp.com)) in their sample and perform exactly the same test as performed with Duffy. The motivation for this is that this SNP shares the property of Duffy null of being highly informative about ancestry, while being in a gene that presumably plays no role in HIV infection. If you get an association there, it seriously calls the Duffy result into question; if not, you feel a bit more comfortable.

\[1\] For the classic extreme example of how population structure leads to false positive associations, consider a case-control association study on, say, diabetes, where the cases are all from Nigeria and the controls from France. Clearly, the cases are all going to have a high frequency of the Duffy null allele, and the controls are all going to have a low frequency (as Duffy null is essentially fixed in Africa and absent elsewhere), and one might naively conclude that Duffy null causes diabetes. But of course, the Duffy blood group has absolutely nothing to do diabetes (I don’t think!), and the researchers have simply been confused by not matching their cases and controls. Obviously, this example is extreme, but more subtle population structure can also confound an association study (and methods for correcting for it are an active area of research; see [here](http://www.nature.com/ng/journal/v38/n8/abs/ng1847.html), for example)

\[2\] It’s well-known that African-Americans are an admixed population, with about 15-20% European ancestry on average. But there’s great variability in this–a single sample of self-defined “African-Americans” can contain individuals with essentially no European ancestry and individuals who look genetically to be completely European. And on a larger scale, within the United States there’s heterogeneity in admixture proportions as well (see [Parra et al.](http://www.ajhg.org/AJHG/abstract/S0002-9297%2807%2961628-0)). How could this create false positives? Essentially, **if risk for a disease is correlated with ancestry *for any reason*, there’s the potential for getting false positives**. In this particular example, if HIV rates are higher in metropolitan areas where there’s been more admixture, or if there are other genetic factors that make Europeans more resistant to HIV, etc., any “African allele” (like Duffy null) will show up as associated with HIV despite playing absolutely no role in the disease.

### Related Posts:

- [HIV susceptibility, a "black" thing, not a Duffy
  thing?](https://www.gnxp.com/WordPress/2008/07/19/hiv-susceptibility-a-black-thing-not-a-duffy-thing/) - [Genetic background & medicine, HIV &
  differences…](https://www.gnxp.com/WordPress/2009/07/21/genetic-background-medicine-hiv-differences-between-blacks-whites/) - [Evolution, a reason for the African HIV
  epidemic?](https://www.gnxp.com/WordPress/2008/07/16/evolution-a-reason-for-the-african-hiv-epidemic/) - [Circumcision to prevent HIV infection in
  America](https://www.gnxp.com/WordPress/2009/08/25/circumcision-to-prevent-hiv-infection-in-america/) - [Circumcision - HIV vs.
  pleasure?](https://www.gnxp.com/WordPress/2007/06/15/circumcision-hiv-vs-pleasure/) - [HIV may not be associated to
  Duffy!?!?!](https://www.gnxp.com/WordPress/2008/07/20/hiv-may-not-be-associated-to-duffy/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F07%2F19%2Fdarc-and-hiv-a-false-positive-due-to-population-structure%2F&linkname=DARC%20and%20HIV%3A%20a%20false%20positive%20due%20to%20population%20structure%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F07%2F19%2Fdarc-and-hiv-a-false-positive-due-to-population-structure%2F&linkname=DARC%20and%20HIV%3A%20a%20false%20positive%20due%20to%20population%20structure%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F07%2F19%2Fdarc-and-hiv-a-false-positive-due-to-population-structure%2F&linkname=DARC%20and%20HIV%3A%20a%20false%20positive%20due%20to%20population%20structure%3F "Email")[](https://www.addtoany.com/share)
