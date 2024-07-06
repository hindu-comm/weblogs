+++
title = "Looking for relatedness"
full_title = "Looking for relatedness in the HapMap Gujaratis"
date = "2011-03-17"
upstream_url = "https://www.gnxp.com/WordPress/2011/03/17/looking-for-relatedness-in-the-hapmap-gujaratis/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/03/17/looking-for-relatedness-in-the-hapmap-gujaratis/).

Looking for relatedness in the HapMap Gujaratis

Recently I was looking at a 3-D PCA animation which [Zack generated](http://www.harappadna.org/2011/03/ref-1-south-asians-harappa-pca/) from the [Harappa Ancestry Project](http://www.harappadna.org/2011/03/ref-1-south-asians-harappa-pca/) data set. Click the link and come back. Notice the outlier clusters?The Burusho are straightforward, they seem to have low levels of Tibetan admixture. **But what about the Gujarati cluster?** Again, we see what we’ve seen before, the fractioning out of the Gujaratis in PCA into two groups, one a tight cluster, and the other relatively widely distributed. This prompted me to look more closely at the HapMap Gujarati sample. Today I was exploring the question with [Plink’s identity-by-descent](http://pngu.mgh.harvard.edu/~purcell/plink/ibdibs.shtml) feature. First I’ll start out with a smaller data set, my family (father, mother, sibling 1, sibling 2, and myself), and an Indian (from Uttar Pradesh) and Pakistani as unrelated individuals. I merged out 23andMe derived genotypes, and with \~900,000 markers calculated pairwise IBD:

    ./plink --bfile IBDControl --genome

Here are the relevant results:

|                  |                  |        |        |        |            |         |         |           |
|------------------|------------------|--------|--------|--------|------------|---------|---------|-----------|
| **Individual 1** | **Individual 2** | **Z0** | **Z1** | **Z2** | **PI_HAT** | **DST** | **PPC** | **RATIO** |
| Indian           | Father           | 0.768  | 0.027  | 0.205  | 0.218      | *0.760* | 0.160   | 1.940     |
| Indian           | Mother           | 0.782  | 0.010  | 0.209  | 0.214      | *0.759* | 0.026   | 1.886     |
| Indian           | Razib            | 0.767  | 0.032  | 0.202  | 0.218      | *0.759* | 0.500   | 2.000     |
| Indian           | Sibling1         | 0.769  | 0.025  | 0.206  | 0.219      | *0.760* | 0.198   | 1.949     |
| Indian           | Sibling2         | 0.766  | 0.032  | 0.203  | 0.219      | *0.760* | 0.685   | 2.030     |
| Indian           | Pakistani        | 0.781  | 0.017  | 0.203  | 0.211      | *0.758* | 0.533   | 2.005     |
| Father           | Mother           | 0.776  | 0.018  | 0.207  | 0.215      | *0.759* | 0.284   | 1.965     |
| Father           | Razib            | 0.002  | 0.777  | 0.221  | 0.610      | *0.851* | 1.000   | 450.800   |
| Father           | Sibling1         | 0.001  | 0.785  | 0.214  | 0.606      | *0.850* | 1.000   | 898.800   |
| Father           | Sibling2         | 0.002  | 0.779  | 0.220  | 0.609      | *0.851* | 1.000   | 643.143   |
| Father           | Pakistani        | 0.778  | 0.019  | 0.203  | 0.213      | *0.758* | 0.201   | 1.950     |
| Mother           | Razib            | 0.002  | 0.788  | 0.211  | 0.605      | *0.849* | 1.000   | 639.429   |
| Mother           | Sibling1         | 0.002  | 0.781  | 0.218  | 0.608      | *0.850* | 1.000   | 639.857   |
| Mother           | Sibling2         | 0.002  | 0.782  | 0.216  | 0.607      | *0.850* | 1.000   | 447.900   |
| Mother           | Pakistani        | 0.779  | 0.020  | 0.201  | 0.211      | *0.758* | 0.052   | 1.904     |
| Razib            | Sibling1         | 0.183  | 0.408  | 0.409  | 0.613      | *0.866* | 1.000   | 11.386    |
| Razib            | Sibling2         | 0.194  | 0.432  | 0.374  | 0.590      | *0.858* | 1.000   | 11.491    |
| Razib            | Pakistani        | 0.781  | 0.016  | 0.203  | 0.211      | *0.758* | 0.933   | 2.095     |
| Sibling1         | Sibling2         | 0.236  | 0.412  | 0.351  | 0.557      | *0.849* | 1.000   | 9.413     |
| Sibling1         | Pakistani        | 0.777  | 0.024  | 0.199  | 0.211      | *0.758* | 0.327   | 1.973     |
| Sibling2         | Pakistani        | 0.774  | 0.024  | 0.202  | 0.214      | *0.758* | 0.443   | 1.991     |

You can infer some things without even knowing what the columns mean. Notice that there are differences between parent-child, sibling-sibling, and unrelated comparisons. The distance measure, DST, is basically exactly the same as the genome-wide comparison in 23andMe. Either the web app is running Plink, or, it’s using the exact same algorithm. Z0 = IBD 0, Z1 = IBD 1, and Z2 = IBD 2. Notice that with my siblings I have a fair amount of IBD 2, but far less with my parents. That’s because parents give you one copy, but you can share zero, one, or two, of a gene with your siblings. In contrast, with our parents there is hardly any IBD = 0, since they’re guaranteed to give you one copy. I assume that the IBD = 2 in that case is population wide fixation of a variant. Notice in the last column that there are different values for unrelated individuals (\~2), siblings (\~10), and parent-children (\~500).

I ran a similar test among the Gujaratis. Remember that I’ve labeled them Gujarat_A and Gujarati_B based on PCA clusters, where the latter form a tight population cluster, and the former do not. Here are the mean pairwise DST values with the groups of pairs:

Mean of all: 0.746

Mean of Gujarati_A only: 0.744

Mean of Gujarati_B only: 0.749

Mean of Gujarati_A and Gujarati_B pairs only: 0.745

Gujarati_B are marginally closer to each other than Gujarati_A. I’m not sure these DST values are totally comparable to the ones from the 23andMe files. I’ll show you why. I constrained the pairs to those where the RATIO was \> 2.5. Here’s what I found:

|                  |                  |        |        |        |            |         |         |           |            |            |
|------------------|------------------|--------|--------|--------|------------|---------|---------|-----------|------------|------------|
| **Individual 1** | **Individual 2** | **Z0** | **Z1** | **Z2** | **PI_HAT** | **DST** | **PPC** | **RATIO** | **PopX**   | **PopY**   |
| NA20900          | NA20891          | 0.003  | 0.974  | 0.023  | 0.510      | 0.842   | 1.000   | 188.250   | Gujarati_A | Gujarati_A |
| NA20909          | NA20910          | 0.003  | 0.970  | 0.027  | 0.512      | 0.842   | 1.000   | 140.438   | Gujarati_A | Gujarati_A |
| NA20891          | NA20907          | 0.412  | 0.557  | 0.032  | 0.310      | 0.803   | 1.000   | 5.730     | Gujarati_A | Gujarati_A |
| NA20900          | NA20907          | 0.684  | 0.292  | 0.024  | 0.170      | 0.775   | 1.000   | 3.251     | Gujarati_A | Gujarati_A |

Notice that Z2 \~ 0, in contrast to the calculations above. I assume someone reading this knows that there’s a simple reason for this, so do tell. The IBD estimates for 23andMe always struck me as too high. In any case, to my surprise **the definitely related individuals seem to be in the Gujarati_A cluster!** What’s going on there? My first thought is that I messed up the data, or, I coded something incorrectly. I assume that this was double-checked before it got into the HapMap data set. Has anyone else seen this weird result? If not, I assume I made an error (that’s kind of my working model right now actually).

### Related Posts:

- [Who are those Houston
  Gujus?](https://www.gnxp.com/WordPress/2011/02/14/who-are-those-houston-gujus/) - [Personal genomics in two
  dimensions](https://www.gnxp.com/WordPress/2011/02/07/different-lenses-into-personal-genomics/) - [The three poles of South Asian genetic
  variation](https://www.gnxp.com/WordPress/2011/04/28/the-three-poles-of-south-asian-genetic-variation/) - [ADMIXTURE vs. MDS, visualization is just
  visualization](https://www.gnxp.com/WordPress/2011/01/18/admixture-vs-mds-visualization-is-just-visualization/) - [Introducing the Harappa Ancestry
  Project](https://www.gnxp.com/WordPress/2011/01/17/introducing-the-harappa-ancestry-project/) - [Introducing the Harappa Ancestry
  Project](https://www.gnxp.com/WordPress/2011/01/18/introducing-the-harappa-ancestry-project/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F03%2F17%2Flooking-for-relatedness-in-the-hapmap-gujaratis%2F&linkname=Looking%20for%20relatedness%20in%20the%20HapMap%20Gujaratis "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F03%2F17%2Flooking-for-relatedness-in-the-hapmap-gujaratis%2F&linkname=Looking%20for%20relatedness%20in%20the%20HapMap%20Gujaratis "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F03%2F17%2Flooking-for-relatedness-in-the-hapmap-gujaratis%2F&linkname=Looking%20for%20relatedness%20in%20the%20HapMap%20Gujaratis "Email")[](https://www.addtoany.com/share)
