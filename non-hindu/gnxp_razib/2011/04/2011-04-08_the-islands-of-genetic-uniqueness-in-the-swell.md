+++
title = "The islands of genetic"
full_title = "The islands of genetic uniqueness in the swell"
date = "2011-04-08"
upstream_url = "https://www.gnxp.com/WordPress/2011/04/08/the-islands-of-genetic-uniqueness-in-the-swell/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/04/08/the-islands-of-genetic-uniqueness-in-the-swell/).

The islands of genetic uniqueness in the swell

I recall years ago reading [Spencer Wells](https://en.wikipedia.org/wiki/Spencer_Wells) discuss how important it was to sample “indigenous people”\* before they were swallowed up by the cresting [panmixia](https://en.wikipedia.org/wiki/Panmixia). Of course panmixia has to be conditioned on the fact that the vast majority of Han Chinese are stilling reproducing with other Han Chinese, and so forth. But it seems plausible to argue that the great agricultural Diasporas are only today swallowing up the residual of marginalized groups outside of the farming frontier. These populations which expanded from agricultural hearths over the Holocene may only be a shadow of the genetic variation which was once extant after the last Ice Age, as the thinly populated landscape was fractionated into endogamous networks as a matter of necessity rather than preference.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/1cba9c5e7efd0d2a582234e56052bb08.png?resize=120%2C52)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/1cba9c5e7efd0d2a582234e56052bb08.png?resize=120%2C52)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/1cba9c5e7efd0d2a582234e56052bb08.png)First, let’s recall that over the long term “effective population size” is defined by the harmonic mean. Concretely, a population of 1 billion can be far more genetically homogeneous than a population of 1,000, ***if*, those 1 billion only recently expanded from far smaller populations.** Imagine a toy example of two populations, A & B. They both begin in generation 1 with a population size of 1,000. In generation 3 both experience a population drop, A to 750, and B to 85. Now, assume that A bounces back to 1000 and maintains that population for the next 20+ generations. In contrast, B begins to double in population size each generation. Here’s a log-transformed chart illustrating the different population sizes:

  
[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/census1.png?resize=600%2C264)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/census1.png?resize=600%2C264)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/census1.png)

In generation 25 population B is at a census size of 350 million. What’s the **long term effective population of these two groups?**

– Population A = 987

– Population B = 979

As you see **a population bottleneck can have long term consequences in terms of effective population size.** Think about it in terms of evolutionary genetics. Any given population begin with a certain amount of standing genetic variation, but if they crash in size then a lot of that variation is lost through the sampling process of random genetic drift. A small population can be a good representation of the variation of a larger population, but as a practical matter usually there is some information lost in the sampling, with more information lost the smaller the N. If the population rebounds then migration and mutation can eventually replenish the lost variation, but that can take a great deal of time. Even after \~10,000 years as a minimum the populations of the New World seem to exhibit evidence of a population bottleneck.

Coming back to the real world, these are the sorts of dynamics which make me interested in events such as the [Bantu expansion](https://en.wikipedia.org/wiki/Bantu_expansion). If the model outlined in [First Farmers](https://www.amazon.com/exec/obidos/ASIN/0631205667/geneexpressio-20) is correct then the past 10,000 years have witnessed a massive reordering and diminution of genetic variation around the world, as small core populations of agriculturalists radiated and replaced hunter-gathers. This makes Spencer Wells’ argument more persuasive, insofar as the remaining twigs of non-agriculturalists may be reservoirs for the shadow of variation past.

As an amateur prehistorian then my interest in populations such as the Mbuti, Bushmen, and Andaman Islanders has been piqued. Yesterday I ran a set of populations in ADMIXTURE with \~170,000 markers. At K = 11, unsupervised, they partitioned relatively cleanly (and the cross-validation error crept back up at K = 12).

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandK11.png?resize=600%2C606)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandK11.png?resize=600%2C606)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandK11.png)

As you can see most of the populations are dominated by their own unique element here (the Druze and Mandenka are different shades of green). Here are the pairwise genetic distance values:

|            |      |       |      |           |       |       |            |       |        |      |         |
|------------|------|-------|------|-----------|-------|-------|------------|-------|--------|------|---------|
|            | San  | Mbuti | Han  | W African | Druze | Hadza | N European | Masai | Papuan | Maya | Sandawe |
| San        | 0.00 | 0.17  | 0.35 | 0.17      | 0.30  | 0.25  | 0.32       | 0.22  | 0.44   | 0.41 | 0.16    |
| Mbuti      | 0.17 | 0.00  | 0.31 | 0.12      | 0.27  | 0.22  | 0.29       | 0.18  | 0.40   | 0.37 | 0.12    |
| Han        | 0.35 | 0.31  | 0.00 | 0.24      | 0.16  | 0.34  | 0.17       | 0.25  | 0.23   | 0.15 | 0.21    |
| W African  | 0.17 | 0.12  | 0.24 | 0.00      | 0.20  | 0.18  | 0.22       | 0.12  | 0.33   | 0.30 | 0.08    |
| Druze      | 0.30 | 0.27  | 0.16 | 0.20      | 0.00  | 0.29  | 0.09       | 0.19  | 0.25   | 0.19 | 0.16    |
| Hadza      | 0.25 | 0.22  | 0.34 | 0.18      | 0.29  | 0.00  | 0.31       | 0.21  | 0.44   | 0.41 | 0.16    |
| N European | 0.32 | 0.29  | 0.17 | 0.22      | 0.09  | 0.31  | 0.00       | 0.21  | 0.26   | 0.20 | 0.18    |
| Masai      | 0.22 | 0.18  | 0.25 | 0.12      | 0.19  | 0.21  | 0.21       | 0.00  | 0.33   | 0.30 | 0.12    |
| Papuan     | 0.44 | 0.40  | 0.23 | 0.33      | 0.25  | 0.44  | 0.26       | 0.33  | 0.00   | 0.30 | 0.29    |
| Maya       | 0.41 | 0.37  | 0.15 | 0.30      | 0.19  | 0.41  | 0.20       | 0.30  | 0.30   | 0.00 | 0.26    |
| Sandawe    | 0.16 | 0.12  | 0.21 | 0.08      | 0.16  | 0.16  | 0.18       | 0.12  | 0.29   | 0.26 | 0.00    |

My main interest right now is the Sandawe. Who are they? What are their relationships? The Hadza seem a genetic isolate of some sort. The Khoisan and Pygmy seem to be part of a broad hunter-gatherer substrate which was overlain by the Bantu expansion. The Sandawe presumably speak a language related to that of the Khoisan, and most of the stuff in the academic literature is linguistic. But they also are genetically distant from the Hadza, and there is *some* dispute as to their linguistic affinities. I am currently reading [The ecological basis for subsistence change among the Sandawe of Tanzania](https://books.google.com/books?id=si8rAAAAYAAJ&printsec=frontcover&dq=ecological+sandawe&source=bl&ots=1gfiwiKtlG&sig=0jNr-ybibYTWqGMYJPp0D-O3JaY&hl=en&ei=EGifTa2HDOzOiAKJ0bz5Ag&sa=X&oi=book_result&ct=result&resnum=3&ved=0CCYQ6AEwAg#v=onepage&q&f=false) (free on Google Books, so I pulled it to my Kindle). For now, plots and charts using the genetic distance values above. The two dimensional charts are representations of the genetic distances….

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/sanddist.png?resize=480%2C462)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/sanddist.png?resize=480%2C462)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/sanddist.png)

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/sandfst.png?resize=597%2C544)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/sandfst.png?resize=597%2C544)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/sandfst.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandFst1.png?resize=596%2C541)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandFst1.png?resize=596%2C541)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandFst1.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandFst2.png?resize=600%2C541)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandFst2.png?resize=600%2C541)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandFst2.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandFst3.png?resize=596%2C536)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandFst3.png?resize=596%2C536)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandFst3.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandFst4.png?resize=598%2C542)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandFst4.png?resize=598%2C542)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandFst4.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandFst5.png?resize=562%2C539)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandFst5.png?resize=562%2C539)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandFst5.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandFst6.png?resize=592%2C542)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandFst6.png?resize=592%2C542)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/SandFst6.png)\* The quotes because the term “indigenous” seems to be politically loaded and fraught. There’s a fair amount of evidence that many indigenous people replaced other indigenous people, relatively recently in time. The exceptions may be amongst groups who were first settlers on islands, like the Maori, relatively late in history.

### Related Posts:

- [How Chinese relate to each other and the
  Japanese](https://www.gnxp.com/WordPress/2010/01/06/how-chinese-relate-to-each-other-and-the-japanese/) - [How did the Chinese get their genetic
  structure?](https://www.gnxp.com/WordPress/2016/03/10/how-did-the-chinese-get-their-genetic-structure/) - [How the Hui became
  Han(ish)](https://www.gnxp.com/WordPress/2009/09/06/how-the-hui-became-hanish/) - [GWAS, population structure and the Han
  Chinese](https://www.gnxp.com/WordPress/2009/11/25/gwas-population-structure-and-the-han-chinese/) - [The slaves of the First Emperor of
  China](https://www.gnxp.com/WordPress/2008/10/01/the-slaves-of-the-first-emperor-of-china/) - [Round-eyed Chinese, part
  n](https://www.gnxp.com/WordPress/2007/05/25/round-eyed-chinese-part-n/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F04%2F08%2Fthe-islands-of-genetic-uniqueness-in-the-swell%2F&linkname=The%20islands%20of%20genetic%20uniqueness%20in%20the%20swell "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F04%2F08%2Fthe-islands-of-genetic-uniqueness-in-the-swell%2F&linkname=The%20islands%20of%20genetic%20uniqueness%20in%20the%20swell "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F04%2F08%2Fthe-islands-of-genetic-uniqueness-in-the-swell%2F&linkname=The%20islands%20of%20genetic%20uniqueness%20in%20the%20swell "Email")[](https://www.addtoany.com/share)
