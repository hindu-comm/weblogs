+++
title = "Harappa Ancestry Project"
full_title = "Harappa Ancestry Project at 10 months"
date = "2011-10-16"
upstream_url = "https://www.gnxp.com/WordPress/2011/10/16/harappa-ancestry-project-at-10-months/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/10/16/harappa-ancestry-project-at-10-months/).

Harappa Ancestry Project at 10 months

It’s been 10 months since Zack Ajmal first contacted me about the possibility of the [Harappa Ancestry Project](http://www.harappadna.org/). I was of two minds. On the one hand I did think there was a major problem with undersampling some regions of South Asia. But, it seemed that the 1000 Genomes would fix that soon enough. As it turns out the [1000 Genomes](http://www.1000genomes.org/about) has been a bit slower than I had anticipated (and I assume that the nixing of the Indian samples was a matter of politics not science). So I’m glad Zack started the project when he did.

At this point he’s hit the [zone of diminishing marginal returns](http://www.harappadna.org/2011/10/participation-rate/) when it comes to participants. Looking through his samples he has a little over 100 non-founders of unadmixed South Asian ancestry (I’m not a founder because both my parents are in the database). I decided to prune the individuals down to this selection, and tack on a lot of his reference populations, with a bias toward South Asians, and see what I could find. I used his K = 11 ADMIXTURE run, since this seems maximally informative for South Asians. You can find the file [here](https://www.gnxp.com/wp/wp-content/uploads/2011/10/harappa1.csv).

  
One interesting aspect of Zack’s project is that he began to collect Y and mtDNA haplogroups at a certain point. Not too surprising there was a preponderance of [R1a1a](https://en.wikipedia.org/wiki/Haplogroup_R1a_(Y-DNA)). For many years now this paternal marker has been suggested to have some association with [Indo-Iranians](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC56946/), though more recently researchers have suggested that in fact it’s a very old haplogroup sharply differentiated between a European branch and a South Asian one. Zack has 56 individuals with Y and mtDNA information in his database. These have to be males. He has 14 individuals with mtDNA information and no Y information. These are probably females (obviously there could be males who are only entering their mtDNA information, but this seems unlikely given that most of the results come from 23andMe). 27 of the males are R1a1a. 29 are not. The mean “Onge” proportion of those with R1a1a is 24%. Without? 24%. The respective values for “South Asian” is 56 and 55 percent respectively. In this likely skewed sample R1a1a doesn’t seem to predict the ancestral variation much.

How about we look at mtDNA. Haplogroup M is localized to South Asia. Dividing the population into M and not M you get the following values:

Not M, South Asian = 55%  
Not M, Onge = 23%  
M, South Asian = 56%  
M, Onge = 23%

There doesn’t seem to be that much in uniparental markers, which aligns with my intuition. At least to this scale of analysis. So let’s look at the autosomal genome. The total genetic variation. If you’ve been following HAP the following won’t be news, for those who haven’t, I thought I’d generate some plots.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap2-e1318796099213.png?resize=600%2C600)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap2-e1318796099213.png?resize=600%2C600)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap2.png)

The two-way admixture aspect of South Asian populations is evident in the HAP data. “Onge” refers to an element affinal to those of Andaman Islanders. “S.Asian” seems to be some sort of compound, but with strong West Eurasian affinities. The axis is NW-SE, upper caste to lower caste, just as you’d expect.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap31-e1318796261973.png?resize=600%2C552)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap31-e1318796261973.png?resize=600%2C552)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap31.png)

There are two West Eurasian components which aren’t collapsed into “S.Asian,” “SW.Asian” and “European.” The names are rather self-evident. The interesting thing here is that “SW.Asian” tends to be elevated among South Indians, especially non-Brahmin upper castes. In contrast, there is far less “SW.Asian” amongst Northeast Indians, and proportionally more “European.” This is more evident when you look at populations in the reference set.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap4-e1318796423762.png?resize=600%2C543)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap4-e1318796423762.png?resize=600%2C543)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap4.png)

There are also some interesting caste/region patterns.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap5-e1318796495212.png?resize=600%2C600)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap5-e1318796495212.png?resize=600%2C600)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap5.png)

When you remove region from consideration it is interesting that Brahmins are somewhat “central” among South Asian populations.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap6-e1318796566983.png?resize=600%2C600)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap6-e1318796566983.png?resize=600%2C600)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap6.png)

In contrast, Punjabis are where you’d expect geography to predict. That’s one reason it was somewhat problematic that the HGDP had only Pakistani groups for South Asians. They’re not too representative of South Asians.

Differences along the axis of caste become more clear when you correct for region, at least mostly.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap7-e1318796659946.png?resize=600%2C600)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap7-e1318796659946.png?resize=600%2C600)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap7.png)

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap8-e1318796722130.png?resize=600%2C600)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap8-e1318796722130.png?resize=600%2C600)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap8.png)

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap9-e1318796756130.png?resize=600%2C600)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap9-e1318796756130.png?resize=600%2C600)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/10/harap9.png)

Punjab is somewhat atypical here. I am now much more willing to credit migrations within the last 2,000 years accounting for the distinctiveness of groups like Jatts.

On a somewhat less exciting note, **it looks like a lot of the genome blogging projects are losing steam.** I’m pretty busy right now, so I haven’t been able to maintain AAP, though we’ll have another Merina soon. But I suspect it goes to show **just how important collection of new data is to these endeavors.** There’s only so much juice you can get out of the same data set. Right now we depend on research groups and the 1000 Genomes, as well as enthusiasts. At some point in the near future the genotypes won’t be the limiting factor. I think then you’ll see a renaissance of amateur ancestral genomics.

### Related Posts:

- [Zack Ajmal's public domain
  genotype](https://www.gnxp.com/WordPress/2011/07/26/zack-ajmals-public-domain-genotype/) - [Harappa Ancestry Project,
  update](https://www.gnxp.com/WordPress/2011/01/24/harappa-ancestry-project-update/) - [The ethnic breakdown of 23andMe
  customers](https://www.gnxp.com/WordPress/2011/06/13/the-ethnic-breakdown-of-23andme-customers/) - [Harappa Ancestry Project, before the first
  wave](https://www.gnxp.com/WordPress/2011/01/28/harappa-ancestry-project-before-the-first-wave/) - [Introducing the Harappa Ancestry
  Project](https://www.gnxp.com/WordPress/2011/01/17/introducing-the-harappa-ancestry-project/) - [Introducing the Harappa Ancestry
  Project](https://www.gnxp.com/WordPress/2011/01/18/introducing-the-harappa-ancestry-project/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F10%2F16%2Fharappa-ancestry-project-at-10-months%2F&linkname=Harappa%20Ancestry%20Project%20at%2010%20months "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F10%2F16%2Fharappa-ancestry-project-at-10-months%2F&linkname=Harappa%20Ancestry%20Project%20at%2010%20months "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F10%2F16%2Fharappa-ancestry-project-at-10-months%2F&linkname=Harappa%20Ancestry%20Project%20at%2010%20months "Email")[](https://www.addtoany.com/share)
