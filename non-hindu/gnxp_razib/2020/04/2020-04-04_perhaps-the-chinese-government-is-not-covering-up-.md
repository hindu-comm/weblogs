+++
title = "Perhaps the Chinese"
full_title = "Perhaps the Chinese government is not covering up the number of Covid19 cases?"
date = "2020-04-04"
upstream_url = "https://www.gnxp.com/WordPress/2020/04/04/perhaps-the-chinese-government-is-not-covering-up-the-number-of-covid-19-cases/"

+++
Source: [here](https://www.gnxp.com/WordPress/2020/04/04/perhaps-the-chinese-government-is-not-covering-up-the-number-of-covid-19-cases/).

Perhaps the Chinese government is not covering up the number of Covid-19 cases?

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2020/03/greatinfluenza.jpeg?resize=180%2C279&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2020/03/greatinfluenza.jpeg?resize=180%2C279&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/B000OCXFWE/geneexpressio-20)A big debate on the internet is whether China is covering up the number of cases of Covid-19 in Hubei, and more specifically Wuhan. Right now [JHU](https://gisanddata.maps.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6) says that China has 82,000 confirmed cases, as opposed to 300,000 in the USA. Both are underestimates, but there are those who believe that the Chinese death toll is not 3,000, but in the millions! I think a more sober take is that they could be underreporting by an order of magnitude. That being said, many epidemiologists believe that China’s numbers [are roughly correct](https://www.thelancet.com/journals/laninf/article/PIIS1473-3099(20)30243-7/fulltext). And certainly, some demographic patterns to be robust and holding up (e.g., the proportion of the aged that die).

But there’s another way to estimate how many people were infected: [look at the variation in the genome sequences of SARS-coV-2 itself](https://bedford.io/projects/ncov-phylodynamics/). The genetic variation patterns in viruses that underwent massive rapid demographic expansion will be different from those that are subject to constant population size.

From what I can see Trevor Bedford and his group at UW have done the best and most thorough estimate of the number infected from the SARS-coV-2 genomes, [Phylodynamic estimation of incidence and prevalence of novel coronavirus (nCoV) infections through time](https://bedford.io/projects/ncov-phylodynamics/).

Here is a part of the abstract and methods:

> Here, we use a phylodynamic approach incorporating 53 publicly > available novel coronavirus (nCoV) genomes to the estimate underlying > incidence and prevalence of the epidemic. This approach uses estimates > of the rate of coalescence through time to infer underlying viral > population size and then uses assumptions of serial interval and > heterogeneity of transmission to provide estimates of incidence and > prevalence. We estimate an exponential doubling time of 7.2 (95% CI > 5.0-12.9) days. We arrive at a median estimate of the total cumulative > number of worldwide infections as of Feb 8, 2020, of **55,800 with a 95% uncertainty interval of 17,500 to 194,400.** Importantly, this approach uses genome data from local and international cases and does not rely on case reporting within China. >
> … >
> …. We began by running the Nextstrain nCov pipeline to align sequences and mask spurious SNPs. We took the output file masked.fasta as the starting point for this analysis. We loaded this alignment into BEAST and specified an evolutionary model to estimate: >
> \* strict molecular clock (CTMC rate reference prior)  
> \* exponential growth rate (Laplace prior with scale 100)  
> \* effective population size at time of most recent sampled tip (uniform prior between 0 and 10) >
> We followed Andrew in using a **gamma distributed HKY nucleotide substitution model**. MCMC was run for 50M steps, discarding the first 10M as burnin and sampling every 30,000 steps after this to give a dataset of 1335 MCMC samples. >
> The file ncov.xml contains the entire BEAST model specification. To > run it will require filling in sequence data; **we are not allowed to reshare this data according to GISAID Terms and Conditions**. The Mathematica notebook ncov-phylodynamics.nb contains code to analyze resulting BEAST output in ncov.log and plot figures.

It’s been many years since I used BEAST but it’s a complicated piece of software and has a lot of options and parameters. I’m very curious about how robust the estimate is when considering sentences such as “assume that variance of secondary cases is at most like SARS with superspreading dynamics with k=0.15.” Bedford and his colleagues know 1,000 times more about this than I do, but I am really curious about other groups looking at the data and running their models.

If all of the results are in the range of the order of magnitude of above, I think some of us really have to update our priors about how much misreporting the Chinese are engaging in…

**Update:** Lots of [sequences](https://www.ncbi.nlm.nih.gov/genbank/sars-cov-2-seqs/) here. I may try to brush up on my BEAST skills…

### Related Posts:

- [Has China won by beating
  coronavirus?](https://www.gnxp.com/WordPress/2020/10/14/has-china-won-by-beating-coronavirus/) - [Internet usage by
  country](https://www.gnxp.com/WordPress/2010/11/28/internet-usage-by-country/) - [Not too many young are dying from
  COVID-19](https://www.gnxp.com/WordPress/2020/04/28/not-too-many-young-are-dying-from-covid-19/) - [COVID-19, another
  panic?](https://www.gnxp.com/WordPress/2020/04/07/covid-19-another-panic/) - [COVID-19, the springtime of
  2020](https://www.gnxp.com/WordPress/2020/04/06/covid-19-the-springtime-of-2020/) - [Alina Chan is
  credible](https://www.gnxp.com/WordPress/2020/11/11/alina-chang-is-credible/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2020%2F04%2F04%2Fperhaps-the-chinese-government-is-not-covering-up-the-number-of-covid-19-cases%2F&linkname=Perhaps%20the%20Chinese%20government%20is%20not%20covering%20up%20the%20number%20of%20Covid-19%20cases%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2020%2F04%2F04%2Fperhaps-the-chinese-government-is-not-covering-up-the-number-of-covid-19-cases%2F&linkname=Perhaps%20the%20Chinese%20government%20is%20not%20covering%20up%20the%20number%20of%20Covid-19%20cases%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2020%2F04%2F04%2Fperhaps-the-chinese-government-is-not-covering-up-the-number-of-covid-19-cases%2F&linkname=Perhaps%20the%20Chinese%20government%20is%20not%20covering%20up%20the%20number%20of%20Covid-19%20cases%3F "Email")[](https://www.addtoany.com/share)
