+++
title = "Measuring whether a"
full_title = "Measuring whether a painter is under or overvalued"
date = "2009-04-19"
upstream_url = "https://www.gnxp.com/WordPress/2009/04/19/measuring-whether-a-painter-is-under-or-over-valued/"

+++
Source: [here](https://www.gnxp.com/WordPress/2009/04/19/measuring-whether-a-painter-is-under-or-over-valued/).

Measuring whether a painter is under or over-valued

As a follow-up to the previous post on [measuring the price-to-earnings ratio of composers](https://www.gnxp.com/blog/2009/04/measuring-whether-artist-is-under-or.php), I’ve done the same thing for painters. The motivation is the same, and I’m still using the painter’s score in Charles Murray’s Human Accomplishment to measure earnings (the more objective valuation). Here, instead of measuring price (the more fashion-driven valuation) with the number of works available at Amazon.com, I’m using the number of works available at AllPosters.com, the main place that people visit to buy inexpensive high art.

The AllPosters score is simply number of works available, divided by the max for any artist (which happens to be for Monet), multiplied by 100. So, like the HA score, it is a measure of how valued an artist’s works are, using the most highly valued artist of all as a reference point.

A look at the data shows several similarities to the case of composers, suggesting that — for example — we overhype a certain time period in general, even though it could arguably be the peak for one art form and yet be only mediocre for another art form. We are more likely to fall for the whole zeitgeist, rather than ruthlessly discriminate and have a separate “favorite period” for different art forms.

Anyway, let’s get to the results. [I’ve uploaded the dataset here](http://manyeyes.alphaworks.ibm.com/manyeyes/datasets/price-earning-ratio-painters/versions/1), where you can copy & paste the text into an Excel spreadsheet to play around with it yourself. I’m only using painters because the sculptors and architects don’t have much available at AllPosters — people want to buy prints of paintings, not of sculptures. Although I haven’t used them in the analysis, I’ve still included the sculptors and architects in the raw data. This only excludes 12 of 111 artists, and they’re pretty spread out across time periods.

As with composers, the agreement between encyclopedia writers and educated laymen is pretty close. [Spearman’s rank correlation](http://www.wessa.net/rankcorr.wasp) between the HA score and the AllPosters score is rho = +0.58 (p less than 10^-6). As before, a fair amount (about 34%) of the variation in subjective valuations can be accounted for by variation in fundamental worth, but that still leaves plenty of room for hype to influence poster-buyers. Here is a plot of the two scores:

[](http://farm4.static.flickr.com/3408/3452847083_41bc4c45b8.jpg)  
The two biggest outliers are Monet, who dominates the poster market but is considered second-tier in encyclopedias, and Michelangelo, who dominates encyclopedias but doesn’t appear on many people’s walls. This could be due to a lot of his work being sculpture and architecture. (None of the results are affected by counting Michelangelo as a sculptor / architect and removing his data-point from the analysis.) Picasso also gets a lot of coverage in encylopedias, while not attracting much attention from poster-buyers.

As with Schoenberg among composers, this may suggest that Murray’s decision to use 1950 as a cut-off was still a bit too late to fully remove the effects of hype. Still does a very good job, given that only a couple of probably over-rated Moderns have P/E ratios that say they’re actually under-rated (e.g., Picasso, Max Ernst, de Chirico).

The clearest case of a painter who is very eminent is encyclopedias but fairly neglected by the lay public is Raphael — his HA score is 73, while his AllPosters score is 23. Most people my age wouldn’t even recognize him, were it not for the Teenage Mutant Ninja Turtle named after him. For fun, here are the top 10 under-valued and over-valued painters, where hype increases as you go down either list:

Top 10 under-valued painters

Masaccio  
Pol de Limbourg  
Antonio del Pollaiolo  
Max Ernst  
Giorgio de Chirico  
Cimabue  
Piet Mondrian  
Hugo van der Goes  
Martin Schongauer  
Frans Hals

Top 10 over-valued painters

Marc Chagall  
Fra Angelico  
Henri Rousseau  
Edgar Degas  
Camille Pissarro  
Salvador Dali  
Vincent Van Gogh  
Henri de Toulouse-Lautrec  
Pierre-Auguste Renoir  
Claude Monet

And as we saw with composers, the P/E ratios of painters are highly skewed, with most painters being under-rated and a tiny handful who are blown out of proportion. As before, a log-normal (or maybe exponential) distribution probably underlies the pattern. Here is the distribution, where the average is 0.4:

[](http://farm4.static.flickr.com/3108/3453661214_029c591889.jpg)  
Finally, here is a look at how P/E ratios vary based on when the painter flourished:

[](http://farm4.static.flickr.com/3618/3452847111_2f8c526e0a.jpg)  
Just as with composers, those painters who flourished in the second half of the 19th C are the most over-valued. In [a response to my composers post](https://isteve.blogspot.com/2009/04/classical-composers-scholarly-vs.html), Steve Sailer suggested that the time series showed that Western music reached its pinnacle during the Late Romantic period, perhaps because it was more profound than what he considers the daintier Classical-era music. But the painters who are responsible for inflating the hype of late-19th-C painting cannot be said to represent the perfection of technique, the profound rather than the light, and so on. These are the Impressionists and some Post-Impressionists, after all — not their Academic contemporaries like Bouguereau. The only commonality with their musical contemporaries is a preference for expression, emotion, and well, the impressionistic.

So, there are two explanations for the over-valuation of late-19th-C music and painting: 1) there is currently an irrational fashion bubble for that time period — it had to be some period, so why not that one? The bubble would encompass the entire zeitgeist, regardless of whether the different parts of it represented the pinnacle of art in their respective media. Or 2) the art-consuming public is more sentimental than judges of art, so that the public tends to over-value time periods that gave greater emphasis to the emotions per se, independent of their artistic merit or the profundity of emotion expressed.

This second explanation includes all class-based explanations, such as the one that says that academics favor aristocratic art, while the lay public is mostly upper-middle class professionals who have a weak spot for the high point of art consumed by the bourgeoisie. It was the new merchant class, remember, that was responsible for cleaning up the lurid spots left by the aristocratic and lower classes — ending public hangings (and then hangings altogether), campaigning for animal rights, looking upon duels and other fights as barbaric rather than civilized, and so on. So we could just be seeing a class phenomenon, given that the middle class is more sentimental.

### Related Posts:

- [Measuring whether an artist is under- or
  over-valued](https://www.gnxp.com/WordPress/2009/04/07/measuring-whether-an-artist-is-under-or-over-valued/) - [The Two Cultures, and some data on the
  public's…](https://www.gnxp.com/WordPress/2009/05/18/the-two-cultures-and-some-data-on-the-public-s-response/) - [New blog: Black IQ and climate, rethinking the decline
  in…](https://www.gnxp.com/WordPress/2009/08/03/new-blog-black-iq-and-climate-rethinking-the-decline-in-formality-and-changes-in-arts-appreciation/) - [Standardized test score distributions-what are
  they…](https://www.gnxp.com/WordPress/2006/09/08/standardized-test-score-distributions-what-are-they-measuring/) - [How many human genomes have been
  sequenced?](https://www.gnxp.com/WordPress/2011/11/07/how-many-human-genomes-have-been-sequenced/) - [Demystifying Price's
  Equation](https://www.gnxp.com/WordPress/2010/10/03/demystifying-prices-equation/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F04%2F19%2Fmeasuring-whether-a-painter-is-under-or-over-valued%2F&linkname=Measuring%20whether%20a%20painter%20is%20under%20or%20over-valued "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F04%2F19%2Fmeasuring-whether-a-painter-is-under-or-over-valued%2F&linkname=Measuring%20whether%20a%20painter%20is%20under%20or%20over-valued "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F04%2F19%2Fmeasuring-whether-a-painter-is-under-or-over-valued%2F&linkname=Measuring%20whether%20a%20painter%20is%20under%20or%20over-valued "Email")[](https://www.addtoany.com/share)
