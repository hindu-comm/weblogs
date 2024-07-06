+++
title = "Tutsi genetics, ii"
full_title = "Tutsi genetics, ii"
date = "2011-08-31"
upstream_url = "https://www.gnxp.com/WordPress/2011/08/31/tutsi-genetics-ii/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/08/31/tutsi-genetics-ii/).

Tutsi genetics, ii

In my [post below](http://blogs.discovermagazine.com/gnxp/2011/08/tutsi-differ-genetically-from-the-hutu/), [Tutsi probably differ genetically from the Hutu](http://blogs.discovermagazine.com/gnxp/2011/08/tutsi-differ-genetically-from-the-hutu/), there were many [comments](http://blogs.discovermagazine.com/gnxp/2011/08/tutsi-differ-genetically-from-the-hutu/#comments). Some I did not post because they were rude, though they did ask valid questions. I will address those issues, but let me quote one [comment](http://blogs.discovermagazine.com/gnxp/2011/08/tutsi-differ-genetically-from-the-hutu/#comment-83617):

> That’s an interesting possibility, but this admixture run didn’t split > the non-hunter-gatherer Africans that well. In one of your previous > analyses on East Africa you managed to get a pretty accurate > ‘Afro-Asiatic/Cushitic’ and ‘Nilotic’ cluster. Is it possible that you could run this Tutsi sample using the same admixture settings as in the ‘Flavors of Afro-Asiatic’ blog post to see if he carries a significant Nilotic component or is mainly Bantu & Cushitic derived?

So I replicated ADMIXTURE runs for many of the same populations as I did in my post, [Flavors of Afro-Asiatic](http://blogs.discovermagazine.com/gnxp/2011/06/flavors-of-afro-asiatic/). I also pared down the population set and generated a PCA with EIGENSOFT. Before I get to those results, let me tackle the questions.

*1) “Are the Luhya suitable proxies for the Hutus?”*

Probably. The reason is that **Bantu-speaking populations, from the Congo to South Africa, are surprisingly similar.** Not only that, but these populations are very distinctive from groups which are close them geographically, but linguistically different (e.g., Khoe, Sandawe, Masai). The Luhya are not exceptional. I’ve run the [Henn et al.](http://www.pnas.org/content/early/2011/03/01/1017511108.abstract) data sets enough to be convinced that they’re exactly as they should be. They are pretty much what you’d expect from Kenyan Bantu. A predominant element which ties them back to an East-Central African point of origin, with some admixture with other East African elements (similarly, South African Bantu exhibit Khoisan admixture). The Hutu may be peculiar, but we don’t know, and my null is that they’re mostly Bantu with some admixture, as is the case with most Bantu speaking populations (this one Tutsi seems to be an exception in that context, as they are presumably Bantu speaking). If you think that the the Luhya are not suitable, I invite you to download the HapMap Luhya, and merge them with some of the Henn et al. data sets (or HGDP or Behar data sets). I think that should convince you.

  
*2) “The admixture percentages you give are weird for population X.”*

Someone who is more technically fluent than I can correct me, **but I suggest that you be very careful about taking absolute percentages too literally.** If you tell a statistical algorithm to push the genetic variation you’ve input into it into a certain number of boxes, it will do that, even if it has to squeeze them in all sorts of ways. In other words, modulating the parameters is an easy way to generate plenty of weird absolute proportions. Often it’s pretty obvious that deeply admixed populations are showing up as their own distinctive cluster…but that begs the question, when is admixture so distant that it shouldn’t count? Instead of focusing on absolute percentages, **look at the relationships between individuals and populations.** These too can be tweaked and massaged, but my personal experience is that they’re somewhat less volatile.

*3) “The Nilotic cluster doesn’t map well onto Nilotic populations.”*

The labels one gives, formally or informally, to a population cluster are for ease of recollection. **They are not there to transmit to you real concrete information about the deep history of a population and its relationship.** Additionally, there is always going to be a lot of confusion when you leverage geographical or linguistic terminologies which have only approximate relationships to genetic clusters. Don’t get so caught up in semantics that you forget that ADMIXTURE components are abstractions, useful for smoking out genetic variation, not for perfectly mapping onto some idealized set of ur-populations.

Now to my results. I used 200,000 markers. I combined Lithuanians and Belorussians into one pot as “Baltic,” and Syrians and Jordanians into another as “Levantines.” For the PCA I focused on African populations, and used the Yemeni Jews as the outgroup. Additionally, **there is clearly structure due to some family relationships amongst the Masai.** This is a problem in many runs with them. Even when you remove the “problem” individuals other clusters tend to crop up at higher K’s where the Masai are very numerous. In any case, for the purpose of these runs ignore the family clusters, and focus on the more typical individuals amongst the Masai.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/tutsi_k8all.png?resize=500%2C672)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/tutsi_k8all.png?resize=500%2C672)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/tutsi_k8all.png)

Remember that the Tutsi is 3/4 Tutsi, 1/4 Hutu. It is N = 1. So is the Nubian. You see in many of the Horn of Africa populations that the Eurasian component has an affinity with Yemenis, not Europeans. In contrast, the Nubian does have some European-like component. That’s probably simply due to the fact that in this run Levantines themselves have that, and Egyptians who also carry that component are part of the heritage of the Nubian. The Tutsi does have the Southwest Asian component, which the Masai seem to lack.

To get a better sense, let’s look at a slice of individuals. The Tutsi is last. The family relationships of some of the Masai are also clear. Focus on the more typical Masai and the Tutsi:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/tutsi_8_indiv.png?resize=600%2C1148)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/tutsi_8_indiv.png?resize=600%2C1148)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/tutsi_8_indiv.png)

Looking at the individual results it seems that the Tutsi can be placed with the range of combinations of ancestral components of the Masai, though not the Luhya. To get a different vantage point let’s look at some PCAs, which visualize the largest components of genetic variance in the data set.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/tutsi_1_2.png?resize=600%2C600)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/tutsi_1_2.png?resize=600%2C600)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/tutsi_1_2.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/tutsi_1_3.png?resize=640%2C640)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/tutsi_1_3.png?resize=640%2C640)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/tutsi_1_3.png)

The results are not cut & dry. I am less skeptical of some Afro-Asiatic element in the Tutsi heritage, though it still seems that the dominant affinity is with the Masai.

**Note:** I ran K = 7 to K – 10. There wasn’t anything different in the general pattern of the runs I did not show.

### Related Posts:

- [Analysis of a Tutsi
  genotype](https://www.gnxp.com/WordPress/2011/08/30/analysis-of-a-tutsi-genotype/) - [Any Tutsi genotypes
  around?](https://www.gnxp.com/WordPress/2011/07/03/any-tutsi-genotypes-around/) - [Personal genomics & rare populations
  notes](https://www.gnxp.com/WordPress/2011/09/14/personal-genomics-rare-populations-notes/) - [Tutsis are genetically very similar to
  Masai](https://www.gnxp.com/WordPress/2019/04/11/tutsis-are-genetically-very-similar-to-the-masai/) - [Which undersampled groups would you like to
  see?](https://www.gnxp.com/WordPress/2011/09/09/which-undersampled-groups-would-you-like-to-see/) - [Rwanda vs.
  Burundi](https://www.gnxp.com/WordPress/2011/07/02/rwanda-vs-burundi/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F08%2F31%2Ftutsi-genetics-ii%2F&linkname=Tutsi%20genetics%2C%20ii "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F08%2F31%2Ftutsi-genetics-ii%2F&linkname=Tutsi%20genetics%2C%20ii "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F08%2F31%2Ftutsi-genetics-ii%2F&linkname=Tutsi%20genetics%2C%20ii "Email")[](https://www.addtoany.com/share)
