+++
title = "Visualization of genetic"
full_title = "Visualization of genetic distances, part n"
date = "2011-04-21"
upstream_url = "https://www.gnxp.com/WordPress/2011/04/21/visualization-genetic-distances-part-n/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/04/21/visualization-genetic-distances-part-n/).

Visualization of genetic distances, part n

Zack Ajmal has been taking his [Reference 3 data set](http://www.harappadna.org/2011/04/introducing-reference-3/) for a stroll over at the [Harappa Ancestry Project](http://www.harappadna.org/). Or, more accurately, he’s been driving his computer to crunch up ADMIXTURE results ascending up a later of K’s. Because it is the *Harappa* Ancestry Project Zack’s populations are overloaded a touch on South Asians. He managed to get a hold of the [data set from Reconstructing Indian History](http://www.nature.com/nature/journal/v461/n7263/abs/nature08365.html). If you will recall this paper showed that the South Asian component which falls out of ancestry structure inference algorithms may actually be a stabilized hybrid of two ancient populations, “Ancestral North Indian” (ANI) and “Ancestral South Indian” (ASI). ANI are a population which can be compared pretty easily to other West Eurasians. There are no “pure” groups of ASI, but the indigenous peoples of the Andaman Islands are the closest, having diverged from the mainland ASI populations tens of thousands of years ago.

At K = 11, that is, 11 inferred ancestral populations, Zack seems to have now stumbled onto the patterns which one would expect from this hybrid model of South Asians. Let me[quote him](http://www.harappadna.org/2011/04/reference-3-admixture-k11/):

> Now let’s take all the reference populations with an Onge component > between 10% to 50% and use the equation above to calculate their ASI > percentage. The results are in a spreadsheet. There are several > populations with an even higher Ancestral South Indian than any of the > Reich et al groups, with Paniya being the highest at 67.4%.

The r-squared between % ASI and % Onge, an Andaman group, is 0.994. That means 99.4% of the variation in the former can be explained by variation of the latter. The % ASI is consistently higher than Onge. Why? The last common ancestors of Andaman Islanders and the ASI diverged on the order of tens of thousands of years ago. [Dienekes](https://dienekes.blogspot.com/) observed ADMIXTURE needs good reference populations, and the Onge have been so long diverged from the last common ancestor with the mainland ASI populations that it’s not a perfect proxy for this ancient group. But it seems that the underestimate is systematically biased in the same direction, so that explains the good fit between the two trends.

Zack naturally generated a pairwise matrix of Fsts between these inferred ancestral populations. Remember, the value within Fst shows the proportion of the genetic variance in the two populations which can be partitioned across them, but not within them. So it’s a rough measure of genetic distance.

Here’s the matrix. I’ve renamed some populations:

------------------------------------------------------------------------

[TABLE]

------------------------------------------------------------------------

The South Asian population above is **very different from the components you’ve seen before.** It seems equivalent to ANI more than anything else. This is a good reminder that the labels we’re giving to these ancestral groups are mnemonics, they’re not to be taken as literal and concretely. Personally I find Fst matrices hard to read, so I’ve generated a number of multidimensional scaling plots illustrating the relationships with the matrix. Clarity can be achieved by mixing & matching the populations, so that’s what I did. Also, I only display dimension 1 and dimension 2. **Remember that dimension 1 is the one with more weight.**

**[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/3.jpg?resize=553%2C552)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/3.jpg?resize=553%2C552)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/3.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/4.jpg?resize=553%2C552)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/4.jpg?resize=553%2C552)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/4.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/5.jpg?resize=553%2C552)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/5.jpg?resize=553%2C552)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/5.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/61.jpg?resize=553%2C552)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/61.jpg?resize=553%2C552)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/61.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/7.jpg?resize=553%2C552)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/7.jpg?resize=553%2C552)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/7.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/8.jpg?resize=553%2C552)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/8.jpg?resize=553%2C552)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/8.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/9.jpg?resize=553%2C552)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/9.jpg?resize=553%2C552)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/9.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/10.jpg?resize=553%2C552)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/10.jpg?resize=553%2C552)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/10.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/11.jpg?resize=553%2C552)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/11.jpg?resize=553%2C552)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/04/11.jpg)**

**Do not think of these as real concrete populations from which all modern populations emerged.** These eleven populations are abstractions which fulfill the dictates of the algorithm. But, I do think that with that caveat in mind, there are suggestive patterns.

First, the “SW Asian” component isn’t that much closer to “W Africans” than the other West Eurasian groups. Yet we know in reality that Southwest Asian populations *are* closer to Africans. What’s going on? **Southwest African populations have African admixture.** And, that admixture is recent enough that it shakes out rather easily. This is in contrast to the normal South Asian modal components, which are indicative of a greater time since admixture, which was thorough enough that it is not trivial to tease out the two ancestral groups from each other’s genetic background. Fission and fusion are normal parts of the history of any geographically expansive species. ADMIXTURE will capture the earlier parts of fusion. But after a long enough period of time that fusion becomes its own distinctive element.

There is the conventional east-west division you see in Eurasia on PCA, but you see evidence of the north-south secondary component on these plots too. The Andaman populations are closer to East Eurasians than West Eurasians, but, they also occupy their own position which highlights a north-south axis.

Finally, **the S. Asian/ANI population seems somewhat closer to “Europeans” than “SW Asians.** That is interesting. But this where you have to very careful and remember that these “pure” ancestral components can themselves fractionate into substituent elements at higher K’s or when you constrain the data set appropriately (Africans and inbred groups tend to hog clusters in ADMIXTURE). If you’ve read all the genome bloggers you will be aware that “European” and “SW Asian” components themselves break apart upon closer inspection. The “SW Asian” component usually divides into a northern and southern branch. The northern branch is often positioned closer to the other “European” groups than it is to the southern branch in terms of genetic distance. Here are a selection of West Eurasian groups sorted by their “S Asian” proportion:

|                       |                   |
|-----------------------|-------------------|
|                       | **South Asian %** |
| Iranians              | 30%               |
| Lezgins (Caucasian)   | 29%               |
| Georgians (Caucasian) | 26%               |
| Adygei (Caucasian)    | 24%               |
| Armenians             | 22%               |
| Turks                 | 21%               |
| Syrians               | 19%               |
| Druze                 | 18%               |
| Lebanese              | 17%               |
| Samaritians           | 16%               |
| Palestinian           | 15%               |
| Cypriots              | 14%               |
| Saudis                | 14%               |
| Yemenese              | 14%               |
| Russian               | 8%                |
| Tuscans               | 7%                |
| Hungarians            | 7%                |
| Utah whites           | 7%                |
| Orcadian              | 5%                |
| British               | 5%                |
| French                | 5%                |
| Italian               | 5%                |
| Finnish               | 4%                |

Also observe that the distance between SW Asians and Europeans is smaller than bertween Europeans and S Asians. Crunching up the K’s, or limited the data set to West Eurasian groups, would probably show more fine-grained relationships.

### Related Posts:

- [Genome bloggers & Indian
  genomics](https://www.gnxp.com/WordPress/2011/03/22/genome-bloggers-indian-genomics/) - [Harappa Ancestry Project, before the first
  wave](https://www.gnxp.com/WordPress/2011/01/28/harappa-ancestry-project-before-the-first-wave/) - [Zack Ajmal's public domain
  genotype](https://www.gnxp.com/WordPress/2011/07/26/zack-ajmals-public-domain-genotype/) - [Introducing the Harappa Ancestry
  Project](https://www.gnxp.com/WordPress/2011/01/17/introducing-the-harappa-ancestry-project/) - [Introducing the Harappa Ancestry
  Project](https://www.gnxp.com/WordPress/2011/01/18/introducing-the-harappa-ancestry-project/) - [Harappa Ancestry Project,
  update](https://www.gnxp.com/WordPress/2011/01/24/harappa-ancestry-project-update/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F04%2F21%2Fvisualization-genetic-distances-part-n%2F&linkname=Visualization%20of%20genetic%20distances%2C%20part%20n "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F04%2F21%2Fvisualization-genetic-distances-part-n%2F&linkname=Visualization%20of%20genetic%20distances%2C%20part%20n "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F04%2F21%2Fvisualization-genetic-distances-part-n%2F&linkname=Visualization%20of%20genetic%20distances%2C%20part%20n "Email")[](https://www.addtoany.com/share)
