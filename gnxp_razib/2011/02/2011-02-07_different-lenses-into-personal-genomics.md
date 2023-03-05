+++
title = "Personal genomics in two"
full_title = "Personal genomics in two dimensions"
date = "2011-02-07"
upstream_url = "https://www.gnxp.com/WordPress/2011/02/07/different-lenses-into-personal-genomics/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/02/07/different-lenses-into-personal-genomics/).

Personal genomics in two dimensions

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/ADMIXRAZIB.png?resize=300%2C292)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/ADMIXRAZIB.png?resize=300%2C292)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/ADMIXRAZIB.png)***The Pith:** In this post I take a different tack at genetic data visualization. Instead of bar plots, I show how genetic relationships can be explored using two dimensional spaces.*

Last week [I suggested](https://www.gnxp.com/wp/2011/02/02/diminishing-returns-of-ancestry-analysis-for-me/) that in some ways I had hit a wall of sharply reduced diminishing returns when it came to understanding my family’s ancestry. It seems rather clear that we’re basically South Asians with a minority East Asian component of ancestry. That being said, I’m still [happy to be involved with the Harappa Ancestry Project](http://www.harappadna.org/). I might have a good sense of my own family’s background, but **Bengal remains extremely undersampled.** An N = 2 is better than none. And, there is still something to be said for understanding how your own lineage is distinctive, or not, in its local geographic context. More specifically I am still curious as to the exact nature of the genetic origins of the Bengali people, especially those on the eastern “marches” (where my family comes from).

But there are still interesting things you can do with the genetic material which I have access to. I converted the autosomal SNPs of the raw 23andMe files with [PLINK](http://pngu.mgh.harvard.edu/~purcell/plink/), and then ran ADMIXTURE with the HapMap Gujaratis, Tuscans, and American Chinese (so probably disproportionately Cantonese). I included my parents, and, two white American friends of western European heritage. My mother is RM, my father is RF, and I will refer to my friends as Euro 1 and Euro 2 . With K = 3, so three putative ancestral populations, you see that the Chinese and Tuscans are disjoint, while the South Asians form a more mixed picture. Euro 1 shows East Asian, and has more than 1% in 23andMe. I assume that the “South Asian” for Euro 2 is just an artifact of the fact that the categories only roughly corresponded to ancestral groups, and South Asians share enough with Europeans genetically to produce this sort of spurious overlap. If [Reconstructing Indian population history](http://www.nature.com/nature/journal/v461/n7263/abs/nature08365.html) is correct, then the “South Asian” component is really an ancient admixture of a European-like population, and a South Eurasian group which has distant, but closer, affinities with East Asians.

But when it comes to personal family history until we get some samples from Burma I think I might be near the end of the line using a program like ADMIXTURE. But **how about PCA?** [EIGENSOFT](http://genepath.med.harvard.edu/~reich/Software.htm) takes pedigree formats, which I had for ADMIXTURE. Remember, PCA is pulling out the largest independent components of variance in the data sequentially rank ordered by the proportion of variance explained by each dimension. So generally you focus on dimensions 1 and 2, since these are the most significant. Positions in each dimensions can nicely be translated into a two dimensional plot.

First, let’s look at Gujaratis, Tuscans, and American Chinese, along with my parents and my two friends. Keep in mind that the x axis is has a magnitude greater than the y axis by a factor of 3.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/allPCA.png?resize=500%2C409)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/allPCA.png?resize=500%2C409)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/allPCA.png)

Isn’t it interesting how well these PCA’s often correspond to geography? The x axis spans Eurasian west-east, while the y-axis spans it north-south. Euro 1 *is* shifted further toward the Asians, just as ADMIXTURE (and 23andMe’s ancestry painting) would imply. While Euro 2 is shifted toward South Asians a bit (the results might have been different if I used the Utah white sample, but I think the Tuscans need a bit of love at this point). Notice that my parents are outside of the main South Asian cluster of Gujaratis. Additionally, you can see two clusters of Gujaratis. One tight cluster, and another which is more diffuse and whose linear topology is suggestive of differential admixture with the European-like element.

Now let’s constrain the sample to TSI + South Asians. **This is not just a zoom-in on that segment of the chart, rather, the dimensions are re-generated using the narrower data set.** Please note that the x axis has a magnitude 6 times greater than the y axis.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/TSI_SouthAsian.png?resize=500%2C403)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/TSI_SouthAsian.png?resize=500%2C403)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/TSI_SouthAsian.png)

The distinctiveness of two Gujarati clusters in the HapMap data set has been found by others, so it’s not some error. I do find it interesting that my mother is in the tighter cluster, \#1, while my father is in cluster \#2.

Now let’s swap the TSI for the CHD, the American Chinese sample from Denver. The x axis is about an 10 times greater in magnitude.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/CHD_SouthAsian21.png?resize=500%2C430)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/CHD_SouthAsian21.png?resize=500%2C430)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/CHD_SouthAsian21.png)

Remember how I always say not to assume that the clusters on PCA plots have some concrete and invariant reality? You see that here. On the world wide plot my parents’ clearly are shifted toward the Chinese, but you can’t see it here, when Tuscans are removed. What’s going on? First, remember that these are the two largest dimensions. Only a small proportion of the total variance. Additionally, yanking the Tuscans may have shifted the rank order of the dimensions too. So let’s run this again and plot the top three dimensions.

It turns out that dimensions 2 and 3, axes y and z, are very close in magnitude (both 10% of dimension 1). I added labels so you can see where my parents are, with G = Gujarati, and C = Chinese.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/CHD_SouthAsian1_2.png?resize=500%2C407)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/CHD_SouthAsian1_2.png?resize=500%2C407)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/CHD_SouthAsian1_2.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/CHD_SouthAsian_1_3.png?resize=500%2C410)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/CHD_SouthAsian_1_3.png?resize=500%2C410)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/CHD_SouthAsian_1_3.png)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/CHD_SouthAsian2_3.png?resize=500%2C411)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/CHD_SouthAsian2_3.png?resize=500%2C411)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/CHD_SouthAsian2_3.png)

And now, three dimensions:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/CHD_SouthAsian3D.png?resize=500%2C429)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/CHD_SouthAsian3D.png?resize=500%2C429)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/CHD_SouthAsian3D.png)

As you can see, the Chinese simply do not vary much, and are a tight cluster. **But, there is a somewhat equivalent Gujarati cluster too!** The HapMap sample was collected from Gujaratis in Houston. To me, it looks like that Houston population can be divided into two groups: one of the tight cluster, and the rest of the population, which is all over the place. Despite my parents’ obvious East Asian affinities, their South Asian variance seems to put them into two different Gujarati clusters. I don’t put much stock in this. Remember these are two dimensions of variation. What’s more interesting is to try and understanding what’s going on with Houston Gujaratis. Anyone in the audience know?

**Note:** I’ll go into more detail about how I did this later. But, do know that PCA goes much quicker than ADMIXTURE. I had some issues with getting the plotting functions working, so I just took the output and did everything in Open Office aside from the last plot, which I obviously did in R.

### Related Posts:

- [Harappa Ancestry Project,
  update](https://www.gnxp.com/WordPress/2011/01/24/harappa-ancestry-project-update/) - [ADMIXTURE vs. MDS, visualization is just
  visualization](https://www.gnxp.com/WordPress/2011/01/18/admixture-vs-mds-visualization-is-just-visualization/) - [ChromoPainter & fineSTRUCTURE on a South Asian data
  set](https://www.gnxp.com/WordPress/2012/02/01/chromopainter-finestructure-on-a-south-asian-data-set/) - [The genetic world in
  3-D](https://www.gnxp.com/WordPress/2011/03/24/the-genetic-world-in-3-d/) - [Visualizing variation, input →
  output](https://www.gnxp.com/WordPress/2011/01/26/visualizing-variation-input-output/) - [South Asian Genotype
  Project](https://www.gnxp.com/WordPress/2017/12/02/south-asian-genotype-project/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F02%2F07%2Fdifferent-lenses-into-personal-genomics%2F&linkname=Personal%20genomics%20in%20two%20dimensions "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F02%2F07%2Fdifferent-lenses-into-personal-genomics%2F&linkname=Personal%20genomics%20in%20two%20dimensions "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F02%2F07%2Fdifferent-lenses-into-personal-genomics%2F&linkname=Personal%20genomics%20in%20two%20dimensions "Email")[](https://www.addtoany.com/share)
