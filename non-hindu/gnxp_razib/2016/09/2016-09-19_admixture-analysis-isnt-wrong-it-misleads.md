+++
title = "Admixture analysis isn’t"
full_title = "Admixture analysis isn’t wrong, it misleads"
date = "2016-09-19"
upstream_url = "https://www.gnxp.com/WordPress/2016/09/19/admixture-analysis-isnt-wrong-it-misleads/"

+++
Source: [here](https://www.gnxp.com/WordPress/2016/09/19/admixture-analysis-isnt-wrong-it-misleads/).

Admixture analysis isn’t wrong, it misleads

[![Screenshot 2016-09-18 20.57.52](https://i0.wp.com/www.unz.com/wp-content/uploads/2016/09/Screenshot-2016-09-18-20.57.52.png?resize=599%2C283)![Screenshot 2016-09-18 20.57.52](https://i0.wp.com/www.unz.com/wp-content/uploads/2016/09/Screenshot-2016-09-18-20.57.52.png?resize=599%2C283)](http://dna.ancestry.com/public/ethnicity/ad010207-d500-4f63-b5af-74014f0dd550/ee749e40-16eb-4f83-bfc7-39b811e4cca0)

The above results are from [Ancestry](http://dna.ancestry.com/ethnicity/61D86CB3-B5ED-4389-8063-A9B7D253D79F). You can see here 4% Melanesian. This is common in South Asians. And it’s not an error in the method. Rather, it is a natural outcome of the methods uses to generate admixture profiles.

Basically what’s going on is this:

1\) You have data. In this case, the data are your own genotypes, as well as that of a set of individuals which represent world genetic variation, and are categorized into discrete populations.

2\) You have a model or set of models. These models have different parameters.

3\) You look at the data you have, and pick the parameters which best explain the data given the model.

If you have 100,000 or more markers that’s more than enough genotype data for individuals. The models themselves are quite stylized (e.g., HWE random mating sets of populations), but close enough to reality to give good results in many cases. For example, Ashkenazi Jews are often assigned to be \~100% Ashkenazi Jewish through these methods.

Then again, Ashkenazi Jews are a good test case. This is a population which went through a bottleneck about 500 to 1,000 years ago, and has been reasonably endogamous most of this time. Additionally, it’s not extremely structured due to inbreeding in different clan lineages. Though cousin marriage and uncle-niece marriage has been practiced by Ashkenazi Jews, the runs of homozygosity you see in Jewish genomes is not such that indicates a highly inbred population, as is common in the Middle East or South Asia. Rather, there are lots of medium length segments identical by descent across individuals.

Ashkenazi Jewish population is rather simple, and it is actually a rather clear and distinct population cluster. It stands to reason that when you create an Ashkenazi Jewish reference panel in your training data set it’s a pretty good match to the individuals you are testing.

The problems occur when you are to generate clusters and ancestry assignments for populations which are not so clear and distinct. Why do South Asians routinely come out as part Melanesian or Polynesian? This post was prompted by a Facebook thread where a South Asian customer of Ancestry was interested to see she had Polynesian ancestry. **The reality is she almost certainly does not have Polynesian ancestry.**

What’s going on is that the reference panel for South Asians used by many of the DTC genomics companies is not diverse enough to capture South Asian genetic diversity. There is an element of South Asian ancestry, “Ancestral South Indian” or ASI, which has deep shared ancestry with populations across Southern Eurasia and out toward Oceania. The admixture analysis method is searching through the reference panels for combinations of genotypes which can explain individual genetic variation. Since the South Asian training set is insufficient to explain all the South Asian variation **the algorithms are filling in the balance of the variation with the closest available proxies to the “ghost clusters.”**

The method is constrained and conditioned on two things:

1\) The data being put in, which is often insufficient.

2\) The set of populations that it is forced to work with to generate the combinations in individuals (the parameter values in the model to explain the data) are often insufficient or artificial.

What I mean by the last is that **many of the genetic clusters are not taxonomically equivalent.** “South Asian” ancestry is much more diverse and diffuse than “Melanesian” ancestry. This why Melanesian ancestry can explain South Asian ancestry, but generally not the reverse.

### Related Posts:

- [How much informative "structure" is in the HGDP data
  set?](https://www.gnxp.com/WordPress/2014/06/06/how-much-informative-structure-is-in-the-hgdp-data-set/) - [The Dodecad ancestry
  project](https://www.gnxp.com/WordPress/2010/10/25/the-dodecad-ancestry-project/) - [PCA remains the swiss-army-knife to explore
  population…](https://www.gnxp.com/WordPress/2017/11/16/pca-remains-the-swiss-army-knife-to-explore-population-structure/) - [Complex history of archaic
  ancestry](https://www.gnxp.com/WordPress/2021/07/19/complex-history-of-archaic-ancestry/) - [More markers, or more
  populations?](https://www.gnxp.com/WordPress/2010/07/02/more-markers-or-more-populations/) - [Input determining output in
  ADMIXTURE](https://www.gnxp.com/WordPress/2011/03/21/input-determining-output-in-admixture/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2016%2F09%2F19%2Fadmixture-analysis-isnt-wrong-it-misleads%2F&linkname=Admixture%20analysis%20isn%E2%80%99t%20wrong%2C%20it%20misleads "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2016%2F09%2F19%2Fadmixture-analysis-isnt-wrong-it-misleads%2F&linkname=Admixture%20analysis%20isn%E2%80%99t%20wrong%2C%20it%20misleads "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2016%2F09%2F19%2Fadmixture-analysis-isnt-wrong-it-misleads%2F&linkname=Admixture%20analysis%20isn%E2%80%99t%20wrong%2C%20it%20misleads "Email")[](https://www.addtoany.com/share)
