+++
title = "Genomic ancestry tests"
full_title = "Genomic ancestry tests are not cons, part 1"
date = "2017-12-04"
upstream_url = "https://www.gnxp.com/WordPress/2017/12/04/genomic-ancestry-tests-are-not-cons-part-1/"

+++
Source: [here](https://www.gnxp.com/WordPress/2017/12/04/genomic-ancestry-tests-are-not-cons-part-1/).

Genomic ancestry tests are not cons, part 1

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/12/konradbook.jpeg?resize=196%2C257)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/12/konradbook.jpeg?resize=196%2C257)](https://www.amazon.com/exec/obidos/ASIN/0199644497/geneexpressio-20)As someone [who is part](https://www.helix.com/shop/insitome-regional-ancestry) of the personal genomics sector, I keep track of media representations of the industry very closely. There is the good and the bad, some justified and some not.

But there is one aspect which I need to weigh in on because it is close to my interests and professional focus, and it is one where I have a lot of experience: **ancestry inference on human data.**

Periodically I see in my Twitter timeline an article shared by a biologist which is filled with either misrepresentation, confusions, and even falsehoods. Of course, some of the criticisms **are correct**. The problem is that when you mix truth and falsehood or sober analysis and critique with sensationalism the whole product is debased.

I’m going to address some of the most basic errors and misimpressions. This post is “part 1” because I might have follow-ups, as I feel like this is a situation where I have to put out fires periodically, as people write about things they don’t know about, and then those articles get widely shared to a credulous public.

First, if an article mentions**STRs or microsatellites** or a test with fewer than 1,000 markers in a direct to consumer genomic context, **ignore the article**. This is like an piece where the author dismisses air travel because it’s noisy due to propeller-driven planes. Propeller-driven planes are a very small niche. Similarly, the major direct to consumer firms which have sold close to \~10 million kits do not use STRs or microsatellites, very much a technology for the 1990s and 2000s. Any mention of STRs or microsatellites or low-density analyses indicate the journalist didn’t do their homework, or simply don’t care to be accurate.

Second, **there is constant harping on the fact that different companies give different results**. This is because tests don’t really give results as much is **interpretations**. The raw results consist of your genotype. On the major SNP-chip platforms this will be a file on the order of 20 MBs. The companies could provide this as the product, but most humans have difficulty grokking over 100,000 variables.

So what’s the solution? The same that scientists have been using for decades: reduce the variation into a much smaller set of elements which are human digestible, often through tables or visualization.

For example, consider a raw data set consisting of my three genotypes from 23andMe, Ancestry, and Family Tree DNA. Merged with public data these are \~201,000 single nucleotide markers. You can [download the plink formatted data](https://www.dropbox.com/s/ynz29p3j2jvdcem/RazibAncestry.zip?dl=0) yourself and look at it. The PCA below shows where my three genotypes are positioned, by the Tamil South Asians. **Observe that my genotypes are basically at the same point**:

![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/12/razibPCA.jpg?resize=625%2C550)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/12/razibPCA.jpg?resize=625%2C550)

The differences between the different companies have nothing to do with the raw data, because with hundreds of thousands of markers they capture enough of the relevant between population differences in my genome (do you need to flip a coin 1 million times after you’ve flipped it 100,000 times to get a sense of whether it is fair?). The [law of large numbers](https://en.wikipedia.org/wiki/Law_of_large_numbers) is kicking in at this point, with genotyping errors on the order of 0.5% not being sufficient to differentiate the files.

Sure enough raw genotype files of the three services match pretty closely. 99.99% for Family Tree DNA and 23andMe, 99.7% for Family Tree DNA and Ancestry, and 99.6% for Ancestry and 23andMe. For whatever reason Ancestry is the outlier here. My personal experience looking at genotype data from Illumina chips is that most are pretty high quality, but it’s not shocking to see instances with 0.5% no call or bad call rates. For phylogenetic purposes if the errors **are not systematic** it’s not a big deal.

The identity to other populations is consistent. About 74% to Tamils. 72-73% for other Eurasians. 71% for the Surui, an isolated Amazonian group. And 69% to Yoruba. **Observe that this recapitulates the phylogenetic history of what we know for the population which I am from, Bengalis**. The greater the genetic distance between two populations due to distinct evolutionary histories the greater the genetic divergence. This is not rocket science. This gets to the point that the raw results make a lot more sense when you integrate and synthesize them with other information you have. Most customers are not going into the process of getting a personal genomic ancestry test blind…but that causes pitfalls as well as opportunities.

But most people do not receive statistics of the form:

|     |          |                  |
|-----|----------|------------------|
|     |          | **SNP Identity** |
| You | Yoruba   | 0.69             |
| You | German   | 0.72             |
| You | Japanese | 0.73             |
| You | Tamil    | 0.74             |

Mind you, this is informative. It’s basically saying I am most genetically distant from Yoruba and closer in sequence to Tamils. But this is somewhat thin gruel for most people. Consider the below which is a zoom in of PC 2 vs. PC 4. I am blue and the purple/pink are Tamils, and the population at the bottom left are East Asians.

![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/12/narrowPCA.jpg?resize=600%2C550)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/12/narrowPCA.jpg?resize=600%2C550)

If you looked at enough PCA plots it will become rather clear **I am shifted toward East Asians in comparison to most other South Asians**. The high identity that I have with Japanese and Dai is due in part to the fact that I have relatively recent admixture from an East Asian population, above and beyond what is typical in South Asians. Remember, **all three of my genotypes are basically on the same spot on PCA plots**. That’s because they’re basically the same. Genotyping error is rather low.

How do we summarize this sort of information for a regular person? **The standard method today is giving people a set of proportions with specific population labels**. Why? People seem to understand population labels and proportions, but can be confused by PCA plots. Additionally, the methods that give out populations and proportions are often better at capturing pulse admixture events relatively recent in time than PCA, and for most consumers of ancestry services, this is an area that they are particularly focused on (i.e., Americans).

An easy way to make one’s genetic variation comprehensible to the general public is to model them as a mixture of various populations that they already know of. So consider the ones above in the plink file. I ran ADMIXTURE in supervised model progressively removing populations for my three genotypes. The results are below.

|               |         |              |              |              |            |               |           |           |            |
|---------------|---------|--------------|--------------|--------------|------------|---------------|-----------|-----------|------------|
| ****         | **Dai** | **Druze**    | **German**   | **Japanese** | **Papuan** | **Sardinian** | **Surui** | **Tamil** | **Yoruba** |
| Razib23andMe  | 11%     | 3%           | 8%           | 4%           | 1%         | 0%            | 1%        | 73%       | 1%         |
| RazibAncestry | 10%     | 2%           | 8%           | 4%           | 1%         | 0%            | 1%        | 73%       | 1%         |
| RazibFTDNA    | 11%     | 2%           | 8%           | 3%           | 1%         | 0%            | 1%        | 72%       | 1%         |
|              |        |             |             |             |           |              |          |          |           |
|              | **Dai** | **Druze**    | **German**   | **Japanese** | **Papuan** | **Sardinian** | **Surui** | **Tamil** |           |
| Razib23andMe  | 11%     | 3%           | 8%           | 4%           | 1%         | 0%            | 1%        | 73%       |           |
| RazibAncestry | 10%     | 3%           | 8%           | 4%           | 1%         | 0%            | 1%        | 74%       |           |
| RazibFTDNA    | 11%     | 3%           | 8%           | 3%           | 1%         | 0%            | 1%        | 73%       |           |
|              |        |             |             |             |           |              |          |          |           |
|              | **Dai** | **Druze**    | **Japanese** | **Papuan**   | **Surui**  | **Tamil**     |          |          |           |
| Razib23andMe  | 10%     | 9%           | 4%           | 1%           | 1%         | 74%           |          |          |           |
| RazibAncestry | 10%     | 9%           | 4%           | 1%           | 1%         | 75%           |          |          |           |
| RazibFTDNA    | 11%     | 9%           | 4%           | 1%           | 1%         | 74%           |          |          |           |
|              |        |             |             |             |           |              |          |          |           |
|              | **Dai** | **Japanese** | **Surui**    | **Tamil**    |           |              |          |          |           |
| Razib23andMe  | 11%     | 4%           | 1%           | 84%          |           |              |          |          |           |
| RazibAncestry | 10%     | 4%           | 1%           | 85%          |           |              |          |          |           |
| RazibFTDNA    | 11%     | 3%           | 1%           | 84%          |           |              |          |          |            |

Please observe again that they are broadly congruent. These methods exhibit a stochastic element, so there is some noise baked into the cake, but with 200,000+ markers and a robust number of reference populations the results come out the same across all methods (also, 23andMe and Family Tree DNA seem to correlate a bit more, which makes sense since these two genotypes are more similar to each other than they are to Ancestry).

Observe that until I remove all other West Eurasian populations the Tamil fraction in my putative ancestry is rather consistent. Why? Because my ancestry is mostly Tamil-like, but social and historical evidence would point to the likelihood of some exogenous Indo-Aryan component. Additionally, seeing as how very little of my ancestry could be modeled as West African removing that population had almost no impact.

When there were three West Eurasian populations, Germans, Druze, and Sardinians, the rank order was in that sequence. Removing Germans and Sardinians and the Druze picked up most of that ancestral component. This a supervised method, so I’m assigning the empirical populations as reified clusters which can be used to reconstitute the variation you see in my own genotype. **No matter what I put into the reference data, the method tries its best to assign proportions to populations**.

The question then comes into the stage of subtle choices one makes to obtain the most informative inferences for the customer. These are not always matters of different results in terms of accuracy or precision, **but often of presentation**. If West Eurasian populations are removed entirely, my Tamil fraction inflates. That’s the closest to the West Eurasian populations left in the data. In contrast, the East Asian fraction remains the same because I’ve left the two proxy populations in the data (I rigged the die here because I know I have Tibeto-Burman admixture which is a combination of Northeast and Southeast Asian).

Let’s do something different. I’m going to swap out the West Eurasian populations with equivalents.

|               |                   |            |                   |              |              |           |            |           |
|---------------|-------------------|------------|-------------------|--------------|--------------|-----------|------------|-----------|
|              | **Armenians**     | **Dai**    | **French_Basque** | **Japanese** | **Mandenka** | **Surui** | **Sweden** | **Tamil** |
| Razib23andMe  | 6%                | 11%        | 0%                | 4%           | 1%           | 1%        | 5%         | 72%       |
| RazibAncestry | 5%                | 11%        | 0%                | 4%           | 1%           | 1%        | 5%         | 73%       |
| RazibFTDNA    | 6%                | 11%        | 0%                | 4%           | 1%           | 1%        | 5%         | 72%       |
|              |                  |           |                  |             |             |          |           |          |
|               | **German**        | **Papuan** | **Yoruba**        |             |             |          |           |          |
| Razib23andMe  | 68%               | 20%        | 13%               |             |             |          |           |          |
| RazibAncestry | 68%               | 20%        | 13%               |             |             |          |           |          |
| RazibFTDNA    | 68%               | 20%        | 13%               |             |             |          |           |          |
|              |                  |           |                  |             |             |          |           |          |
|               | **French_Basque** | **Tamil**  |                  |             |             |          |           |          |
| Razib23andMe  | 8%                | 92%        |                  |             |             |          |           |          |
| RazibAncestry | 7%                | 93%        |                  |             |             |          |           |          |
| RazibFTDNA    | 8%                | 92%        |                  |             |             |          |           |          |
|              |                  |           |                  |             |             |          |           |          |
|               | **Tamil**         | **Yoruba** |                  |             |             |          |           |          |
| Razib23andMe  | 97%               | 3%         |                  |             |             |          |           |          |
| RazibAncestry | 97%               | 3%         |                  |             |             |          |           |          |
| RazibFTDNA    | 97%               | 3%         |                  |             |             |          |           |           |

I have no ancestry from French Basque, but I do have ancestry from Armenians and Swedes in this model. Why? If you keep track of the most recent population genomic ancestry this all makes sense. But if you don’t, well, it’s harder to unpack. This is part of the problem with these sorts of tests: **how to make it comprehensible to the public while maintaining fidelity to the latest research.**

This is not always easy, and differences between companies in terms of interpretation are not invidious as some of the press reports would have you think, but a matter of difficult choices and trade-offs one needs to make to give value to customers. True, this could all be ironed out if there was a ministry of genetic interpretation and a rectification of names in relation to population clusters, but right now there isn’t. This allows for both brand differentiation and engenders confusion.

In most of the models with a good number of populations, my Tamil ancestry is in the low 70s. Notice then that some of these results are relatively robust to the populations one specifies. Some of the patterns are so striking and clear that one would have to work really hard to iron them out and mask them in interpretation. But what happens when I remove Tamils and include populations I’m only distantly related to? This is a ridiculous model, but the algorithm tries its best. My affinity is greatest to Germans, both because of shared ancestry, and in the case of Papuans, their relatively high drift from other East Eurasians and Denisovan ancestry. But both Papuan and Yoruba ancestry are assigned because I’m clearly not 100% German, and I share alleles with both these populations. In models where there are not enough populations to “soak up” an individual’s variation, but you include Africans, it is not uncommon for African ancestry to show up at low fractions. If you take Europeans, Africans, and East Asians, and force two populations out of this mix, then Europeans are invariably modeled as a mix of Africans and East Asians, with greater affinity to the latter.

Even when you model my ancestry as Tamil or Yoruba, you see that there is a Yoruba residual. I have too much genetic variation that comes from groups not closely related to the variation you find in Tamils to eliminate this residual.

Just adding a few populations fixes this problem:

|               |         |            |            |            |
|---------------|---------|------------|------------|------------|
|              | **Dai** | **Tamil**  | **Yoruba** |           |
| Razib23andMe  | 14%     | 83%        | 2%         |           |
| RazibAncestry | 14%     | 84%        | 2%         |           |
| RazibFTDNA    | 14%     | 83%        | 2%         |           |
|              |        |           |           |           |
|              | **Dai** | **German** | **Tamil**  | **Yoruba** |
| Razib23andMe  | 15%     | 10%        | 74%        | 1%         |
| RazibAncestry | 14%     | 9%         | 75%        | 1%         |
| RazibFTDNA    | 15%     | 10%        | 74%        | 1%         |

Notice how my Tamil fraction is almost the same as when I had included in many more reference populations. Why? My ancestral history is complex, like most humans, **but it’s not that complex**. The goal for public comprehensibility is to reduce the complexity into digestible units which give insight.

Of course, I could just say read [Inference of Population Structure Using Multilocus Genotype Data](http://www.genetics.org/content/155/2/945). The basic framework was laid out in that paper 17 years ago for model-based clustering of the sort that is very common in direct to consumer services (some use machine learning and do local ancestry decomposition across the chromosome, but really the frameworks are an extension of the original logic). But that’s not feasible for most people, **including journalists.**

Consider this piece at Gizmodo,[Why a DNA Test Is Actually a Really Bad Gift](https://gizmodo.com/why-a-dna-test-is-actually-a-really-bad-gift-1820934113). I pretty much disagree with a lot of the privacy concerns, seeing as how I’ve had my public genotype downloadable for seven years. But this portion jumped out at me: “Ancestry tests are based on sound science, **but variables in data sets and algorithms mean results are probabilities, not facts, as many people expect**.”

Yes, there are probabilities involved. But if a DNA test using the number of markers above tells you you are 20% Sub-Saharan African and 80% European in ancestry, that probability is of the same sort of confidence of you determining that a coin flip is fair after 100,000 flips. True, you can’t be **totally sure** after 100,000 flips that you have a fair coin, but you can be pretty confident. With hundreds of thousands of markers, a quantum of 20% Sub-Saharan African in a person of predominantly European heritage is an inference made with a degree of confidence that verges upon certitude within a percentage or so.

As for the idea that they are not “facts.” I don’t even know what that means in this context. And I doubt the journalist does either. Which is one of my main gripes with these sorts of stories: **unless they talk to a small subset of scientists the journalists just don’t know what they are talking about when it comes to the statistical genetics.**

Finally, there is the issue about **what does it even mean to be % percent of population X, Y, or Z?** Even many biologists routinely reify and confuse the population clusters with something real and concrete in a Platonic sense. But deep down when you think about it we all need to recall we’re collapsing genealogies of many different segments of DNA into broad coarse summaries when we say “population.” And populations themselves are by their nature often somewhat open and subject to blending and flow with others. **A population genomic understanding of structure does not bring into clarity Platonic facts, but it gives one instruments and tools to smoke out historical insight.**

The truth, in this case, is not a thing in and of itself, but a dynamic which refines our intuitions of a fundamentally alien process of Mendelian assortment and segregation.

### Related Posts:

- [The abuse of ancestry testing is bad for personal
  genomics](https://www.gnxp.com/WordPress/2013/02/25/the-abuse-of-ancestry-testing-is-bad-for-personal-genomics/) - [Personal genomics & the
  state](https://www.gnxp.com/WordPress/2010/07/23/personal-genomics-the-state/) - [The oracle of personal
  genomics](https://www.gnxp.com/WordPress/2012/05/01/the-oracle-of-personal-genomics/) - [At least today we can explore personal
  genomics](https://www.gnxp.com/WordPress/2018/07/02/at-least-today-we-can-explore-personal-genomics/) - [The impact of genetic ancestry
  testing](https://www.gnxp.com/WordPress/2011/06/27/the-impact-of-genetic-ancestry-testing/) - [Personal genomics, beyond the
  hype](https://www.gnxp.com/WordPress/2009/09/15/personal-genomics-beyond-the-hype/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F12%2F04%2Fgenomic-ancestry-tests-are-not-cons-part-1%2F&linkname=Genomic%20ancestry%20tests%20are%20not%20cons%2C%20part%201 "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F12%2F04%2Fgenomic-ancestry-tests-are-not-cons-part-1%2F&linkname=Genomic%20ancestry%20tests%20are%20not%20cons%2C%20part%201 "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F12%2F04%2Fgenomic-ancestry-tests-are-not-cons-part-1%2F&linkname=Genomic%20ancestry%20tests%20are%20not%20cons%2C%20part%201 "Email")[](https://www.addtoany.com/share)
