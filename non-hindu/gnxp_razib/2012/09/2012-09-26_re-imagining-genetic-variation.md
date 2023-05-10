+++
title = "Reimagining genetic"
full_title = "Reimagining genetic variation"
date = "2012-09-26"
upstream_url = "https://www.gnxp.com/WordPress/2012/09/26/re-imagining-genetic-variation/"

+++
Source: [here](https://www.gnxp.com/WordPress/2012/09/26/re-imagining-genetic-variation/).

Re-imagining genetic variation

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/genetic00-300x241.jpg?resize=300%2C241)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/genetic00-300x241.jpg?resize=300%2C241)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/genetic00.jpg)To the left is a PCA from [The History and Geography of Human Genes](https://www.amazon.com/exec/obidos/ASIN/0691029059/geneexpressio-20). If you click it you will see a two dimensional plot with population labels. How were these plots generated? In short what these really are are visual representations of a matrix of genetic distances (those distances being general F_(ST)), which L. L. Cavalli-Sforza and colleagues computed from classical autosomal markers. Basically what the distances measure are the differences across populations in regards to their genetics. The unwieldy matrix tables can be visualized as a neighbor-joining tree, or a two dimensional plot as you see here. But that’s not the end of the story.

In the past ten years with high density SNP-chip arrays instead of just representing the relationship of populations, these plots often can now illustrate the position of an individual (the methods differ, from components analysis or coordinate analysis, to multi-dimensional scaling, but the outcomes are the same).



![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/genmap1-300x234.jpg?resize=300%2C234)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/genmap1-300x234.jpg?resize=300%2C234)For example, the famous [genetic map of Europe](http://www.nature.com/nature/journal/v456/n7218/abs/nature07331.html). Here you see the colors representing nationalities, and centroid positions of the populations as well as individuals. In this manner you can take into population genetic variation in a *gestalt* fashion. Nevertheless, these still leave something to be desired. They are precise and powerful, but they lack a certain elegance due to their scatter. When you have over a dozen color schemes, and overlapping populations, these are not minor matters. Additionally, the human eye is often not well tuned to note the finer gradients of density difference.

This is clear when you move from a manageable number of populations (e.g., Europeans), to the world. In these cases you have to color in specific *regions*, else you’d get lost rather quickly.I can illustrate this easy enough. I’ve a data set I’m running right now with \~3,000 individuals and 250,000 SNPs. It’s a merge of HGDP, Behar et al., HapMap, etc. I decided to use [PLINK](http://pngu.mgh.harvard.edu/~purcell/plink/) to generate an MDS plot.



[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/printA-300x144.png?resize=300%2C144)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/printA-300x144.png?resize=300%2C144)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/printA.png)Here you see the unadorned scatter. To the top of the plot are Asian populations, and to the right African ones. Europeans are at the vertex to the bottom left. This should be familiar to you, though you may have to [rotate it](http://blogs.discovermagazine.com/gnxp/files/2012/04/23me1.jpg). One way to extract some clarity out of this picture is to color code the regions, and give different symbols to the lowest level category. Yes, this helps, but there are still limitations (and to be frank I often have a hard time making out triangles on these plots). First and foremost, I think we need to be unable to ascertain the variation in density of the scatter. A further plot will illustrate this (click to enlarge):

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/printB.png?resize=580%2C280)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/printB.png?resize=580%2C280)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/printB.png)

Most of the text is basically illegible. This is where a centroid method would do well; in lieu of a scatter of individuals you just label a population. Or, you could do something like allow points in various colors to represent populations, but put the labels at centroids only. This still runs into the problem that populations are not equidistant, so therefore you can have crowding.

Recently to address these issues I decided to use a ‘utilization distribution’ method which I saw in one of the ‘genetic map of Europe’ papers. The logic here is simple.

1\) First, take the density distribution of the points on the plot by category and ‘smooth’ them. Basically this creates a continuous distribution where there was a discontinuous ones.

2\) Then demarcate the central \~90% area as the bounds of the population distribution. Color these bounding lines differently.

Below you see the results:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/pcatest1.png?resize=622%2C356)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/pcatest1.png?resize=622%2C356)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/pcatest1.png)

Obviously there are some kinks to be worked out. But you see two things. First, **some groups are clearly subsets of other groups in their distribution**. This is very hard to discern in the other visualization methods above. Second, these plots are taking density into account, so you aren’t distracted by outliers (which may be mislabeling by the analyst or the original collector of the samples).

My ultimate aim is to develop a script which will place the text near the suitable distribution zone, without crowding out other text. I have some ideas of how to do this “on the fly,” but it will take time to implement. Until then some of you may want to know a bit about the packages used for the above.

First, download the*adehabitat* package from R. Actually, you may want to download various *tcl* development packages first, because the former won’t install without the latter. Once you have that you need data. I assume you can generate the results from PLINK above. Once you have that you need to have three colums

1\) x

2\) y

3\) the identification

Here’s some R that might help:

    #MDSData is the data frame with MDS data
    attach(MDSData)
    library(adehabitat)
    cexValue=0
    par(mar=c(0,0,0,0))
    plot(C1,C2,cex=cexValue,xlab="Coordinate 1",ylab="Coordinate 2")

    # process the data, remove more than 5 individuals in group
    loc=subset(MDSData,Group %in% names(which(table(Group) >= 5)))
    loc$X = loc$C1
    loc$Y = loc$C3
    #load ids
    id = factor(loc$Group)
    #create first parameter, two columns
    loc=subset(loc,select=c(X,Y))

    vud=kernelUD(loc,id)
    #90% utilization
    kVert=getverticeshr(vud, 9);
    #I'm removing one of the populations
    kVert[21]=NULL
    kVertLength=length(attr(kVert,"names"))
    plot(kVert, add=TRUE, lwd=2,colpol=NA,colborder=rainbow(kVertLength) )
    groups=attr(kVert,"names")
    legend('topright',groups,cex=.55,lty=1,lwd=3,col=rainbow(kVertLength) )

### Related Posts:

- [Visualizing intra-European phylogenetic
  distances](https://www.gnxp.com/WordPress/2017/12/10/visualizing-intra-european-phylogenetic-distances/) - [Genetic distances across
  Eurasia](https://www.gnxp.com/WordPress/2018/01/27/genetic-distances-across-eurasia/) - [A picture is worth a thousand words, part
  n](https://www.gnxp.com/WordPress/2008/04/21/a-picture-is-worth-a-thousand-words-part-n/) - [Genes and facial
  features](https://www.gnxp.com/WordPress/2008/09/25/genes-and-facial-features/) - [How South Asian populations relate to each
  other](https://www.gnxp.com/WordPress/2018/01/25/how-south-asian-populations-relate-to-each-other/) - [What L. L. Cavalli-Sforza got
  wrong?](https://www.gnxp.com/WordPress/2008/04/21/what-l-l-cavalli-sforza-got-wrong/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F09%2F26%2Fre-imagining-genetic-variation%2F&linkname=Re-imagining%20genetic%20variation "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F09%2F26%2Fre-imagining-genetic-variation%2F&linkname=Re-imagining%20genetic%20variation "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F09%2F26%2Fre-imagining-genetic-variation%2F&linkname=Re-imagining%20genetic%20variation "Email")[](https://www.addtoany.com/share)
