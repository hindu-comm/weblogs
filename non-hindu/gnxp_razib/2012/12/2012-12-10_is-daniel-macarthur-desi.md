+++
title = "Is Daniel MacArthur"
full_title = "Is Daniel MacArthur 'desi'?"
date = "2012-12-10"
upstream_url = "https://www.gnxp.com/WordPress/2012/12/10/is-daniel-macarthur-desi/"

+++
Source: [here](https://www.gnxp.com/WordPress/2012/12/10/is-daniel-macarthur-desi/).

Is Daniel MacArthur 'desi'?

My initial inclination in this post was to discuss a recent ordering snafu which resulted in many of my friends being quite peeved at 23andMe. But browsing through their new ‘ancestry composition’ feature I thought I had to discuss it first, because of some nerd-level intrigue. Though I agree with many of [Dienekes](https://dienekes.blogspot.com/2012/12/23andme-ancestry-composition.html) concerns about this new feature, I have to admit that at least this method doesn’t give out positively misleading results. For example, I had complained earlier that ‘ancestry painting’ gave literally crazy results when they weren’t trivial. It said I was \~60 percent European, which makes some coherent sense in their non-optimal reference population set, but then stated that my daughter was \>90 percent European. Since 23andMe did confirm she was 50% identical by descent with me these results didn’t make sense; some readers suggested that there was a strong bias in their algorithms to assign ambiguous genomic segments to ‘European’ heritage (this was a problem for East Africans too).

Here’s my daughter’s new chromosome painting:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/daugpaint.png?resize=600%2C425)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/daugpaint.png?resize=600%2C425)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/daugpaint.png)

One aspect of 23andMe’s **new ancestry composition feature is that it is very Eurocentric**. But, most of the customers are white, and presumably the reference populations they used (which are from customers) are also white. Though there are plenty of public domain non-white data sets they could have used, I assume they’d prefer to eat their own data dog-food in this case. But that’s really a minor gripe in the grand scheme of things. This is a huge upgrade from what came before. Now, it’s not telling me, as a South Asian, very much. But, it’s not telling me ludicrous things anymore either!

But in regards to omission I am curious to know why this new feature rates my family as only \~3% East Asian, when other analyses put us in the 10-15% range. The problem with*very*high values is that South Asians often have some residual ‘eastern’ signal, which I suspect is not real admixture, but is an artifact. Nevertheless, northeast Indians, including Bengalis, often have genuine East Asia admixture. On PCA plots my family is shifted considerably toward East Asians. The signal they are picking up probably isn’t noise. Almost every apportionment of East Asian ancestry I’ve seen for my family yields a greater value for my mother, and that holds here. It’s just that the values are implausibly low.

In any case, that’s not the strangest thing I saw. I was clicking around people who I had “shared” genomes with, and I stumbled upon this:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/dgm.png?resize=600%2C465)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/dgm.png?resize=600%2C465)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/dgm.png)

As you can guess from the screenshot **this is [Daniel MacArthur’s](https://twitter.com/dgmacarthur) profile.** And according to this \~25% of chromosome 10 is South Asian! On first blush this seemed totally nonsensical to me, so I clicked around other profiles of people of similar Northern European background…and I didn’t see anything equivalent.

What to do? It’s going to take more evidence than this to shake my prior assumptions, so I downloaded [Dr. MacArthur’s genotype](http://www.genomesunzipped.org/data). Then I merged it with three HapMap populations, the Utah whites (CEU), the Gujaratis (GIH), and the Chinese from Denver (CHD). The last was basically a control. I pulled out chromosome 10. I also added Dan’s wife Ilana to the data set, since I believe she got typed with the same Illumina chip, and is of similar ethnic background (i.e., very white). It is important to note that only 28,000 SNPs remained in the data set. But usually 10,000 is more than sufficient on SNP data for model-based clustering with inter-continental scale variation.

I did two things:

1\) I ran ADMIXTURE at K = 3, unsupervised

2\) I ran an MDS, which visualized the genetic variation in multiple dimensions

Before I go on, I will state what I found: **these methods supported the inference from 23andMe, on chromosome 10 Dr. MacArthur seems to have an affinity with South Asians**(i.e., this is his ‘curry chromosome’). Here are the average (median) values in tabular format, with MacArthur and his wife presented for comparison.

|                                         |            |      |      |
|-----------------------------------------|------------|------|------|
| **ADMIXTURE results for chromosome 10** |            |      |      |
|                                         |            |      |      |
|                                         | K 1        | K 2  | K 3  |
| CEU                                     | 0.04       | 0.02 | 0.93 |
| GIH                                     | 0.87       | 0.05 | 0.08 |
| CHD                                     | 0.01       | 0.97 | 0.01 |
| Daniel MacArthur                        | ***0.29*** | 0.07 | 0.64 |
| Ilana Fisher                            | 0.01       | 0.06 | 0.94 |
|                                         |            |      |      |

You probably want a distribution. Out of the non-founder CEU sample none went above 20% South Asian. Though it did surprise me that a few were that high, making it more plausible to me that MacArthur’s results on chromosome 10 were a fluke:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/dis.png?resize=586%2C572)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/dis.png?resize=586%2C572)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/dis.png)

And here’s the MDS with the two largest dimensions:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/Screenshot-from-2012-12-10-003824.png?resize=573%2C540)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/Screenshot-from-2012-12-10-003824.png?resize=573%2C540)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/Screenshot-from-2012-12-10-003824.png)

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/inter.png?resize=202%2C399)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/inter.png?resize=202%2C399)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/inter.png)Again, it’s evident that this chromosome 10 is shifted toward South Asians. If I had more time right now what I’d do is probably get that specific chromosomal segment, phase it, and then compare it to various South Asian populations. But I don’t have time now, so I went and checked out the results from the [Interpretome](http://esquilax.stanford.edu/#painting). I cranked up the settings to reduce the noise, and so that it would only spit out the most robust and significant results. As you can see, again chromosome 10 comes up as the one which isn’t quite like the others.

Is there is a plausible explanation for this? Perhaps Dr. MacArthur [can call up a helpful relative](http://www.genomesunzipped.org/2010/11/am-i-partly-jewish-an-unexpected-turn-of-events.php)? From what recall his parents are immigrants from the United Kingdom, and it isn’t unheard of that white Britons do have South Asian ancestry which dates back to the 19th century. **Though to be totally honest I’m rather agnostic about all this right now.** This genotype has been “out” for years now, so how is it that no one has noticed this peculiarity??? Perhaps the issue is that everyone was looking at the genome wide average, and it just doesn’t rise to the level of notice? What I really want to do is look at the distribution ofallchromosomes and see how Daniel MacArthur’s chromosome 10 then stacks up. It might be a random act of nature yet.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/browndan.png?resize=116%2C127)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/browndan.png?resize=116%2C127)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/12/browndan.png)Also, I guess I should add that at \~1.5% South Asian that would be consistent with one of MacArthur’s great-great-great-great grandparents being Indian. Assuming 25 year generation times that puts them in the mid-19th century. Of course, at such a low proportion the variance is going to be high, so it is quite possible that you need to push the real date of admixture one generation back, or one generation forward.

### Related Posts:

- [The importance of open data in genomics (and in
  everything!)](https://www.gnxp.com/WordPress/2013/01/27/the-importance-of-open-data-in-genomics-and-in-everything/) - [Peculiarities in 23andMe's ancestry
  assignments](https://www.gnxp.com/WordPress/2014/01/26/peculiarities-in-23andmes-ancestry-assignments/) - [Are you a
  caveman?](https://www.gnxp.com/WordPress/2011/12/15/are-you-a-caveman/) - [Ancestry painting: true but trivial, or interesting
  but…](https://www.gnxp.com/WordPress/2012/04/17/ancestry-painting-true-but-trivial-or-interesting-but-inaccurate/) - [Behold, the
  Interpretome!](https://www.gnxp.com/WordPress/2011/06/14/behold-the-interpretome/) - [Ancestry.com's AncestryDNA won't give you your
  raw…](https://www.gnxp.com/WordPress/2012/09/16/ancestry-coms-ancestrydna-wont-give-you-your-raw-data/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F12%2F10%2Fis-daniel-macarthur-desi%2F&linkname=Is%20Daniel%20MacArthur%20%27desi%27%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F12%2F10%2Fis-daniel-macarthur-desi%2F&linkname=Is%20Daniel%20MacArthur%20%27desi%27%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F12%2F10%2Fis-daniel-macarthur-desi%2F&linkname=Is%20Daniel%20MacArthur%20%27desi%27%3F "Email")[](https://www.addtoany.com/share)
