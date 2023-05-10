+++
title = "DIY population structure"
full_title = "DIY population structure inference, part 1 of many"
date = "2011-02-13"
upstream_url = "https://www.gnxp.com/WordPress/2011/02/13/d-i-y-population-structure-inference-part-1-of-many/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/02/13/d-i-y-population-structure-inference-part-1-of-many/).

D.I.Y. population structure inference, part 1 of many

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/F1.large_.jpg?resize=600%2C193)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/F1.large_.jpg?resize=600%2C193)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/02/F1.large_.jpg)

If you’ve been reading this weblog for a while you’ve seen many images like the one above. It comes from the 2008 paper [Worldwide Human Relationships Inferred from Genome-Wide Patterns of Variation](http://www.sciencemag.org/content/319/5866/1100.full). The data set is from the [Human Genome Diversity Project](https://en.wikipedia.org/wiki/Human_Genome_Diversity_Project). It consists 52 groups from around the world, curated for representativeness, but also ethnic distinctiveness. They utilized the FRAPPE program, which like STRUCTURE and ADMIXTURE estimates the ancestry of individuals (and in the aggregate populations) from a a combination of components, the number of which you specify with the parameter K. In other words, this is model based. It works out really well when you have an intuition of the model you’re looking for. Imagine African Americans, who you can presume are a two-way admixture between two distinct ancestral populations. It works less well in other cases. For example, South Asians are modeled by 23andMe as a two-way admixture between Europeans and East Asians. *Why* this occurs is totally comprehensible; they have three (Chinese + Japanese = one) reference populations which are very different from South Asians. So the computer, being dumb but fast, simply slaps together the best inference possible from the weird constraints placed upon it. Garbage in, garbage out.

But along with PCA these sorts of algorithms which allow one to visualize variance across hundreds of thousands of markers across hundreds of individuals are very useful (though perhaps there are [mentats](https://en.wikipedia.org/wiki/Mentat) amongst us who have no need of such techniques). You just have to use them with caution. Information may be free, but it can be misinterpreted!

Over the years of my blogging people have regularly asked questions of the form “are East Africans more closely related to West or South Africans?” They are easily answered, **I would just look in the literature.** But, it did take time, and I’d have to pick the right figure, look for [Fst](https://en.wikipedia.org/wiki/Fixation_index), and so forth. But that is changing.

The *Nature* piece [“The rise of the genome bloggers”](http://www.nature.com/news/2010/101215/full/468880a.html) covered the change. Since last fall [BGA](https://bga101.blogspot.com/) and [Dodecad](dodecad.blogspot.com) have been dumping lot bar plots and PCAs on the web. Instead of looking for a paper, I have now begun to use those sites as my resource of first choice (since they’re well indexed by Google). Now with [HAP](http://www.harappadna.org/) you have another source of information. It’s gotten to the point that technically capable [commenters are now submitting their own](http://www.harappadna.org/2011/02/south-asian-pca/#comment-340) results!

We’ve come a long way. Academics are not miserly with information, and some of my best friends have been the gatekeepers of the data and results. But now you can find the [data](http://hagsc.org/hgdp/files.html) [on the](http://hapmap.ncbi.nlm.nih.gov/downloads/index.html.en) [web](http://jorde-lab.genetics.utah.edu/?page_id=23) easily. You can [reprocess](http://pngu.mgh.harvard.edu/~purcell/plink/) the data by yourself. And, you can do the [analysis](http://www.genetics.ucla.edu/software/admixture/) [yourself](http://genepath.med.harvard.edu/~reich/Software.htm).

I’ve been sitting back for a while, letting Dienekes, Zack, etc., do their thing. There are so many technically fluent people out there, I’ve enjoyed just consuming the raw information yield. **But that ends today.** Over the past week I’ve been slapping together some R functions to make it easier for me to generate bar plots at various K’s, as well as PCA’s. My goal is this: **a reader asks a question, and I quickly constrain my data set appropriately and do the analyses, take the screenshots, and upload them to the servers here, and point them to the images in the comments.** The main constrain should be the computational resources (ADMIXTURE can take hours). Yes, that’s where we’re at.

Every now and then I’m going to put up a post of ADMIXTURE bar plots or MDS/PCA’s. Part of the reason is that it will be useful for my later reference. Second, I think the slide show display view is probably pretty useful to get a *gestalt* sense of what’s going on. That’s what we’re going for: human comprehension. Below is my first slide show, from K = 2 to K = 16. That is, the models assumed two to sixteen ancestral populations. I also excluded Sub-Saharan Africans from the data set since they’re so varied. Here are the details:

  
– \~55,000 markers  
– All non-African HGDP populations  
– HapMap Tuscans + Gujaratis (as well some some white Americans from 23andMe)  
– Bengali = my parents, N = 2

I removed some bar plots because they seemed redundant:

-Makrani  
-Melanesian  
-White American (these are half a dozen friends whose data I received from 23andMe)  
-North Italian  
-Colombians  
-Karitiana

Note, these populations are simply not displayed. Their variance still was used to generate the results!

In regards to the bar plot, I did not output the legend. There’s plenty of labeling the ancestral fractions elsewhere, and it’s useful, but I think it is also important for people to take the colors in without any bias of what they mean. I have added text to some of the slides though, which you can see at the bottom if you are so inclined. I apologize for the garishness of some of the colors…I have some element of colorblindness in the purple-violent range for what it’s worth.

\[zenphotopress album=263 sort=sort_order number=15\]

### Related Posts:

- [NPR on human
  variation](https://www.gnxp.com/WordPress/2008/02/22/npr-on-human-variation/) - [More genetic structure of human
  populations](https://www.gnxp.com/WordPress/2009/05/16/more-genetic-structure-of-human-populations/) - [PCA remains the swiss-army-knife to explore
  population…](https://www.gnxp.com/WordPress/2017/11/16/pca-remains-the-swiss-army-knife-to-explore-population-structure/) - [85% of genetic variation is within
  groups...](https://www.gnxp.com/WordPress/2008/02/23/85-of-genetic-variation-is-within-groups/) - [Peeling the population genetic Indian
  onion](https://www.gnxp.com/WordPress/2011/12/08/peeling-the-population-genetic-indian-onion/) - [Input determining output in
  ADMIXTURE](https://www.gnxp.com/WordPress/2011/03/21/input-determining-output-in-admixture/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F02%2F13%2Fd-i-y-population-structure-inference-part-1-of-many%2F&linkname=D.I.Y.%20population%20structure%20inference%2C%20part%201%20of%20many "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F02%2F13%2Fd-i-y-population-structure-inference-part-1-of-many%2F&linkname=D.I.Y.%20population%20structure%20inference%2C%20part%201%20of%20many "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F02%2F13%2Fd-i-y-population-structure-inference-part-1-of-many%2F&linkname=D.I.Y.%20population%20structure%20inference%2C%20part%201%20of%20many "Email")[](https://www.addtoany.com/share)
