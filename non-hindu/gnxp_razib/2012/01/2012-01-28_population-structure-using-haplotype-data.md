+++
title = "Population structure"
full_title = "Population structure using haplotype data"
date = "2012-01-28"
upstream_url = "https://www.gnxp.com/WordPress/2012/01/28/population-structure-using-haplotype-data/"

+++
Source: [here](https://www.gnxp.com/WordPress/2012/01/28/population-structure-using-haplotype-data/).

Population structure using haplotype data

***The Pith:* New software which gives you a more fine-grained understanding of relationships between populations and individuals.**

According to the [reader survey](https://www.surveymonkey.com/sr.aspx?sm=Jg07zaWxoEQH40vO5ToXuQaEoi6Un9Nz_2fB_2bh8pw_2bAYI_3d) \>50 percent of you don’t know how to interpret PCA or model-based (e.g., ADMIXTURE) genetic plots, so I am a little hesitant to point to this new paper in *PLoS Genetics*, [Inference of Population Structure using Dense Haplotype Data](http://www.plosgenetics.org/article/info:doi/10.1371/journal.pgen.1002453), as it extends the results of those earlier methods. But it’s an important paper, and at some point I’ll starting using their [software](http://www.paintmychromosomes.com/). The “big picture” is that earlier methods left “some information on the table.” That’s partly due to the fact that they were developed (or in the case of PCA leveraged, as it’s a very general technique) in an era where very dense marker data sets were not available (today we’re shifting to full genome sequences in many cases!). The information left on the table would be haplotype structure. Genetic variation in a concrete form manifests as sequences along a line, many of them physically connected. These correlations of nearby variant markers represent haplotypes of great interest, because they are excellent clues to admixture or divergence events across populations. In contrast the older methods, were looking at variation from marker to marker, each in turn independently, which collapses some of the important genomic structure that we can now inspect (in fact, linkage disequilibrium due to these correlations can distort some of the results in the older methods, so you want to “thin” your marker set).

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/01/pcamislead.jpg?resize=267%2C255)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/01/pcamislead.jpg?resize=267%2C255)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/01/pcamislead.jpg)Let me make this concrete for you. On [23andMe](https://www.23andme.com/) you can see where your friends shake out on a PCA plot using the HGDP data set as a reference. What this means is that the HGDP data set is used to generate independent dimensions of genetic variation. As is the usual case in these analyses the largest dimension separates Africans from everyone else, and the second largest dimension separates Asians from Europeans and Africans. 23andMe customers are then projected upon this variation, so you can get a sense where you are positioned in the clusters. To the left is a zoom in on the section for Central/South Asians. You can see that one of my friends, highlighted with a green color, falls almost perfectly in the Uygur cluster. According to ancestry estimates my friend is 50 percent Asian and 50 percent European. The “representative” Uygur in the 23andMe chromosome painting gives about the same results. But these are total genome estimates. The historical nature of my friend’s admixture and that of the Uygur woman is very different, as one can see in the below figure.



[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/01/eurasian.jpg?resize=600%2C441)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/01/eurasian.jpg?resize=600%2C441)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/01/eurasian.jpg)

My friend is to the right, and the Uygur woman is to the left. Why the big difference? My friend has an East Asian parent an a European parent. The Uygur woman is the product of a marriage between Uygurs, a population which is due to admixture betwen East Asians and Europeans one to two thousand years ago. Recombination has broken apart the perfect linkage between European and East Asian regions among the Uygurs. Obviously this isn’t the case with my friend, as recombination has had no time to generate alternative sequences of ancestry. This is critical information which genome-wide estimates displayed on PCA or ADMIXTURE will miss out on.

As for this particular paper and method, I want to point you to [figure 5](http://www.plosgenetics.org/article/slideshow.action?uri=info:doi/10.1371/journal.pgen.1002453&imageURI=info:doi/10.1371/journal.pgen.1002453.g005). The darker/bluish colors indicate higher conancestry estimates, and yellower colors lower ones. Red is in the middle. The diagonal tends to be blue/red because that represents populations’ correlations with themselves, which one would expect to be high. You can’t really read the labels, but I wanted to highlight the Italian and Sardinian blocks. Explanation below.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/01/SARDI.jpg?resize=600%2C580)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/01/SARDI.jpg?resize=600%2C580)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/01/SARDI.jpg)

You can see an ADMIXTURE plot underneath the heat-map. What’s going on? Sardinians exhibit the hallmarks of an isolated population with smaller effective population which has undergone more genetic drift than Italians over the same amount of time. This is naturally one reason that they “break out” rather quickly in ADMIXTURE and PCA. You see this in South Asia with the Kalash, who often emerge as their own cluster rather quickly, and separate out in a PCA as well. This is simply a function of their isolation and lower effective population size. Most of the people who use ADMIXTURE and PCA know this, but those reading these plots do not. Without that knowledge one can make incorrect inferences. The methods outlined here in the paper allow one to visually observe immediately these trends, while keeping in place broader wold-wide correlations across populations in mind. This is a big step forward not only in data analysis, but result visualization.

If you are more interested in this topic, the [first author has a comparison of the various tools up](http://www.maths.bris.ac.uk/~madjl/finestructure/comparisons.html). Both [Dienekes](https://dienekes.blogspot.com) and [Eurogenes](https://bga101.blogspot.com/) are using the new software. Get the software at [PaintMyChromosomes.com](http://www.paintmychromosomes.com/)!

**Citation:** Lawson DJ, Hellenthal G, Myers S, Falush D (2012) Inference of Population Structure using Dense Haplotype Data. PLoS Genet 8(1): e1002453. doi:10.1371/journal.pgen.1002453

### Related Posts:

- [PCA remains the swiss-army-knife to explore
  population…](https://www.gnxp.com/WordPress/2017/11/16/pca-remains-the-swiss-army-knife-to-explore-population-structure/) - [Clusters where they "shouldn't
  be"....](https://www.gnxp.com/WordPress/2012/02/13/clusters-where-they-shouldnt-be/) - [How to look at population
  structure](https://www.gnxp.com/WordPress/2016/10/03/how-to-look-at-population-structure/) - [What is a
  population?](https://www.gnxp.com/WordPress/2013/06/10/what-is-a-population/) - [One K to rule them
  all?](https://www.gnxp.com/WordPress/2016/08/14/one-k-to-rule-them-all/) - [D.I.Y. population structure inference, part 1 of
  many](https://www.gnxp.com/WordPress/2011/02/13/d-i-y-population-structure-inference-part-1-of-many/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F01%2F28%2Fpopulation-structure-using-haplotype-data%2F&linkname=Population%20structure%20using%20haplotype%20data "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F01%2F28%2Fpopulation-structure-using-haplotype-data%2F&linkname=Population%20structure%20using%20haplotype%20data "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F01%2F28%2Fpopulation-structure-using-haplotype-data%2F&linkname=Population%20structure%20using%20haplotype%20data "Email")[](https://www.addtoany.com/share)
