+++
title = "Inferring and"
full_title = "Inferring and visualizing patterns in genomic data"
date = "2011-02-09"
upstream_url = "https://www.gnxp.com/WordPress/2011/02/09/inferring-and-visualizing-patterns-in-genomic-data/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/02/09/inferring-and-visualizing-patterns-in-genomic-data/).

Inferring and visualizing patterns in genomic data

I’ve been playing around with [ADMIXTURE](http://www.genetics.ucla.edu/software/admixture/) and [EIGENSOFT](http://genepath.med.harvard.edu/~reich/Software.htm) with the the HapMap data set along with a few friends & family merged into it. It is interesting to see how the intuitive inferences you make from ADMIXTURE bar plots differ somewhat from PCA scatter plots. In any case, I’ve been posting some of the preliminary results on Facebook (in part because one of my friends is on Facebook and is curious about his own genetic background), and a friend who is a grad student pointed me to [Structurama](http://fisher.berkeley.edu/structurama/download.html), which infers the best number of categories\* (one can do cross-vaidation in ADMIXTURE). I’ve avoided [STRUCTURE](http://pritch.bsd.uchicago.edu/software.html) because it’s computationally more intensive. Any other recommendations? Specifically, something *not* mentioned by [Dienekes](https://dienekes.blogspot.com/) or [David](https://bga101.blogspot.com/).

Below the fold is a taste of the games my computer has been up to overnight. K = 5 ancestral populations in ADMIXTURE. HapMap Utah whites, Tuscans, Mexicans, Beijing Chinese, in that order. The last 6 bars are: my father, my mother, and then four individuals of European ancestry, Euro 1, Euro 2, Euro 3, and Euro 4. After merging files and pruning founders and thinning the markers to reduce linkage disequilibrium I was left with 120,000 SNPs. Just a note, I’ve played around with different numbers of SNPs at various K’s, and some very small differences are surprising consistent. My mother is always just a bit more “Asian” than my father.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/K5.png?resize=600%2C1106)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/K5.png?resize=600%2C1106)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/K5.png)

\* Some of the download links on the Structurama site do not seem to work right now, but you can download the source code. Didn’t try the Mac links.

### Related Posts:

- [Peak
  Facebook?](https://www.gnxp.com/WordPress/2011/06/13/peak-facebook/) - [Another perspective on
  Facebook](https://www.gnxp.com/WordPress/2010/06/19/another-perspective-on-facebook/) - [D.I.Y. population structure
  analysis](https://www.gnxp.com/WordPress/2011/12/26/d-i-y-population-structure-analysis/) - [Lots and lots of genotype
  data!](https://www.gnxp.com/WordPress/2013/01/09/lots-and-lots-of-genotype-data/) - [D.I.Y. population structure inference, part 1 of
  many](https://www.gnxp.com/WordPress/2011/02/13/d-i-y-population-structure-inference-part-1-of-many/) - [Death of email = death of
  Facebook](https://www.gnxp.com/WordPress/2010/06/17/death-of-email-death-of-facebook/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F02%2F09%2Finferring-and-visualizing-patterns-in-genomic-data%2F&linkname=Inferring%20and%20visualizing%20patterns%20in%20genomic%20data "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F02%2F09%2Finferring-and-visualizing-patterns-in-genomic-data%2F&linkname=Inferring%20and%20visualizing%20patterns%20in%20genomic%20data "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F02%2F09%2Finferring-and-visualizing-patterns-in-genomic-data%2F&linkname=Inferring%20and%20visualizing%20patterns%20in%20genomic%20data "Email")[](https://www.addtoany.com/share)
