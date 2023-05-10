+++
title = "Structure in 1000"
full_title = "Structure in 1000 Genomes South Asian data"
date = "2015-07-12"
upstream_url = "https://www.gnxp.com/WordPress/2015/07/12/structure-in-1000-genomes-south-asian-data/"

+++
Source: [here](https://www.gnxp.com/WordPress/2015/07/12/structure-in-1000-genomes-south-asian-data/).

Structure in 1000 Genomes South Asian data

![Est100_1](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/07/Est100_1.png?resize=640%2C492)![Est100_1](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/07/Est100_1.png?resize=640%2C492)

I’m currently trying to figure out how best to integrate [1000 Genomes data](http://www.1000genomes.org/data), along with [Estonian Biocentre](http://www.ebc.ee/), and HGDP. First, I converted the VCF files from the 1000 Genomes into pedigree format. I’ll put that up on GitHub in the next few days. Then I filtered the results for SNPs which are found in the HGDP. Finally, I intersected the results with the Estonian Biocentre data sets. I was left with \~250,000 markers after quality control (e.g., removing markers which are missing in more than 0.1% of the 5000+ samples).

In particular I’m curious about the **population structure of the South Asian data**. When you sample Chinese or Japanese or the English you need to be geographically diverse, but you don’t have to worry about social stratification too much.\* Not so with South Asia. You have to be careful who and where you sample, because the variation doesn’t cleanly follow geography. In the Diaspora for example wealthier and higher status groups tend to be represented. In the mid-2000s Noah Rosenberg’s lab published [Low Levels of Genetic Divergence across Geographically and Linguistically Diverse Populations from India](http://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.0020215). In the paper itself the authors cautioned their samples were from the United States, so one should be careful about accepting the idea that they might represent the geographic variation in South Asia well. In hindsight it seems likely that their selection bias was too great for them to overcome to make robust conclusions, even with over 700 microsatellites.

Above is a PCA plot I generated for South Asians. I’m not quite sure of the coding of some of the Estonian Biocentre populations, so don’t take that as gospel. I was more curious about the distribution of the 1000 Genomes samples, since they are likely to be widely used in the near future.

First, let’s focuson the Bengalis from Bangladesh:

![Parents](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/07/Parents.png?resize=640%2C492)![Parents](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/07/Parents.png?resize=640%2C492)

**I was frankly surprise how genetically homogeneous this group is**. The two overlapping black dots are my parents. It seems clear that my family comes from a region of Bangladesh which likely has more East Asian ancestry than is the norm. This makes geographic sense, my family’s roots are in the [eastern part](https://en.wikipedia.org/wiki/Comilla_District) of eastern Bengal. Though it is hard to see on this plot a small group of Bengali individuals, specifically six, reside in a tight cluster amidst samples from Tamil Nadu.The fact that they aren’t randomly scattered indicates to me that there’s some genuine structure here. I suspect that there is evidence here of a group which has been assimilated, but retained its separate caste-community identity.

But overall there is a major contrast between the Bengali samples from Bangladesh, and the previous Gujarati samples, now also in the 1000 Genomes (ou can see the Patel cluster on the other side of the Bengalis, as it bulges out). The non-Patel Gujaratis were genetically varied, some very similar to individuals from Pakistan. In contrast there isn’t that sort of cline among the Bengali samples (it doesn’t look like they sampled any Bengali Brahmins in this data set, at least those of full heritage). The Punjabi samples were collected from Lahore, and they range from many individuals who are little different from Pathans to some whose genetic background resembles those from middle castes in Southern India. I don’t know what’s going on here, but there has been some back migration of laborers into the Punjab historically. I believe this is the origin of some low caste groups who are now Christian. Both the Telegu and Tamil samples have a few Brahmins in them. This is clearin the following plot:

![SIndia](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/07/SIndia.png?resize=640%2C492)![SIndia](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/07/SIndia.png?resize=640%2C492)

The two Brahmins are from Tamil Nadu. You notice that several of the 1000 Genomes Tamil and Telegu samples are rather close to them. South Indian Brahmins tend to be genetically very similar, so almost certainly that’s what these individuals are if they are placed here on the PCA. Though the Tamil samples are relatively tightly clustered, the Telegu break out into several groups. One of the major 1000 Genomes groups overlaps perfectly with Velamas, a middle caste from Andhra Pradesh. The individuals who are Telegu speakers between the Velamas and Brahmins may be of mixed heritage. I don’t know.

Ultimately I’d like to do some TreeMix and pairwise comparisons between these populations. But to do that I’m going to have to clean them up a bit so that they make sense as…populations.

\* The [outcaste](https://en.wikipedia.org/wiki/Burakumin) group in Japan only crystallized during the Tokugawa period. Not long enough to be genetically that distinct from the broader Japanese population.

### Related Posts:

- [1000 Genomes data, 290,000
  SNPs](https://www.gnxp.com/WordPress/2015/09/30/1000-genomes-data-290000-snps/) - [South Asians in the 1000
  Genomes](https://www.gnxp.com/WordPress/2016/02/19/south-asians-in-the-1000-genomes/) - [Lots and lots of genotype
  data!](https://www.gnxp.com/WordPress/2013/01/09/lots-and-lots-of-genotype-data/) - [Batch effects in the 1000 Genomes
  data?](https://www.gnxp.com/WordPress/2019/05/04/batch-effects-in-the-1000-genomes-data/) - [Punjabi genetic variation in 1000 Genomes: Hindu caste
  in…](https://www.gnxp.com/WordPress/2018/01/28/punjabi-genetic-variation-in-1000-genomes-hindu-caste-in-the-land-of-the-pure/) - [South Asian gene flow into Burmese and
  Malays?](https://www.gnxp.com/WordPress/2017/09/07/189219/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F07%2F12%2Fstructure-in-1000-genomes-south-asian-data%2F&linkname=Structure%20in%201000%20Genomes%20South%20Asian%20data "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F07%2F12%2Fstructure-in-1000-genomes-south-asian-data%2F&linkname=Structure%20in%201000%20Genomes%20South%20Asian%20data "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F07%2F12%2Fstructure-in-1000-genomes-south-asian-data%2F&linkname=Structure%20in%201000%20Genomes%20South%20Asian%20data "Email")[](https://www.addtoany.com/share)
