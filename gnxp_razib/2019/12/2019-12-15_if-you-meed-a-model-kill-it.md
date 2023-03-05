+++
title = "If you meet a model,"
full_title = "If you meet a model, kill it!"
date = "2019-12-15"
upstream_url = "https://www.gnxp.com/WordPress/2019/12/15/if-you-meed-a-model-kill-it/"

+++
Source: [here](https://www.gnxp.com/WordPress/2019/12/15/if-you-meed-a-model-kill-it/).

If you meet a model, kill it!

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2019/12/pythonmacinelearning.jpeg?resize=202%2C249&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2019/12/pythonmacinelearning.jpeg?resize=202%2C249&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/B07VBLX2W7/geneexpressio-20)If you are awake in the year 2019 you have heard of “machine learning.” And, if you listened to my podcast [The Insight](https://www.stitcher.com/podcast/insitome/the-insight) [you know that](https://blog.insito.me/the-insight-show-notes-season-2-episode-29-deep-learning-and-population-genetics-ffebb7278bc8) [Andy Kern’s lab at University of Oregon](http://kernlab.org/) is leveraging machine learning (and “deep learning” and “neural networks”) for population genetics.

Now, obviously in population genetics, you know that models are a big deal. The Hardy-Weinberg model. The coalescent. Various models of selection against which you can test data. This is not a coincidence. In the 20th-century population genetics was a data-poor field and a lot of work was done in the theoretical space since that’s where the work could be done (here’s to you two-locus models of selection from the 1970s!).

In the 2000s genomics transformed the landscape. All of a sudden there was a surfeit of data. On the one hand, this meant that there was a lot of material for models to work on. On the other hand, it turns out that some models aren’t too scalable to big data, nor do they turn out to be very robust (one reason for the persistence of single-locus phylogenetic models around mtDNA and Y is their elegant tractability).

This is where a “bottom-up” machine learning approach comes into the picture. Kern’s group just came out with new a preprint I’ve been hearing about for a while, [Predicting Geographic Location from Genetic Variation with Deep Neural Networks](https://www.biorxiv.org/content/10.1101/2019.12.11.872051v1.full):

> Most organisms are more closely related to nearby than distant members > of their species, creating spatial autocorrelations in genetic data. > This allows us to predict the location of origin of a genetic sample > by comparing it to a set of samples of known geographic origin. Here > we describe a deep learning method, which we call Locator, to > accomplish this task faster and more accurately than existing > approaches. In simulations, Locator infers sample location to within > 4.1 generations of dispersal and runs at least **an order of magnitude > faster than a recent model-based approach**. We leverage Locator’s > computational efficiency to predict locations separately in windows > across the genome, which allows us to both quantify uncertainty and > describe the mosaic ancestry and patterns of geographic mixing that > characterize many populations. Applied to whole-genome sequence data > from Plasmodium parasites, Anopheles mosquitoes, and global human > populations, this approach yields median test errors of 16.9km, 5.7km, > and 85km, respectively.

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2019/07/gillespie.jpeg?resize=190%2C265&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2019/07/gillespie.jpeg?resize=190%2C265&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/B004M1905O/geneexpressio-20)Reads of this weblog can jump to the empirical examples of the HGDP. They make sense, and I especially liked the local ancestry deconvolution analysis and variation in predictive power conditional on recombination.

Sometimes quantity has a quality all its own, and the eye-opening aspect of [locator](https://github.com/kern-lab/locator) is how it can test a lot of propositions quickly (this is more important in the era of WGS datasets). It’s no joke that dispensing with a model can speed things up.

One minor element I’ll note is that getting [locator](https://github.com/kern-lab/locator) installed is not trivial from what I have seen. Especially the [tensorFlow](https://www.tensorflow.org/) dependency. So I’ll probably have more updates once I get it up and running myself.

### Related Posts:

- [Machine learning swallowing population genetics
  =…](https://www.gnxp.com/WordPress/2017/10/22/machine-learning-swallowing-population-genetics-understanding-patterns-in-population-genomics/) - [On theoretical evolutionary
  genetics](https://www.gnxp.com/WordPress/2012/07/01/on-theoretical-evolutionary-genetics/) - [Raging against the population genetics
  machine](https://www.gnxp.com/WordPress/2010/09/20/raging-against-the-population-genetics-machine/) - [Evolutionary biology in the 21st-century: from big
  theories…](https://www.gnxp.com/WordPress/2019/08/27/evolutionary-biology-in-the-21st-century-from-big-theories-to-big-facts/) - [Back to Africa migration & Deep
  Learning](https://www.gnxp.com/WordPress/2020/12/12/back-to-africa-migration-deep-learning/) - [Recollections of Mel
  Green](https://www.gnxp.com/WordPress/2017/10/25/recollections-of-mel-green/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2019%2F12%2F15%2Fif-you-meed-a-model-kill-it%2F&linkname=If%20you%20meet%20a%20model%2C%20kill%20it%21 "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2019%2F12%2F15%2Fif-you-meed-a-model-kill-it%2F&linkname=If%20you%20meet%20a%20model%2C%20kill%20it%21 "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2019%2F12%2F15%2Fif-you-meed-a-model-kill-it%2F&linkname=If%20you%20meet%20a%20model%2C%20kill%20it%21 "Email")[](https://www.addtoany.com/share)
