+++
title = "Measuring whether an"
full_title = "Measuring whether an artist is under or overvalued"
date = "2009-04-07"
upstream_url = "https://www.gnxp.com/WordPress/2009/04/07/measuring-whether-an-artist-is-under-or-over-valued/"

+++
Source: [here](https://www.gnxp.com/WordPress/2009/04/07/measuring-whether-an-artist-is-under-or-over-valued/).

Measuring whether an artist is under- or over-valued

The concept of [price-to-earnings ratio](https://en.wikipedia.org/wiki/Price-to-earnings_ratio) can be extended to anything that has an objective, fundamental value and a subjective value that people give to the thing — assuming these can be measured, however crudely. The ratio gets bigger when the price goes up while the thing is still generating the same amount of earnings, or when it generates less earnings while being priced the same. So, larger values of this ratio mean that the thing is overhyped, while smaller values mean it’s overlooked.

When lots of instances of the same thing are over-hyped, and when this over-hyping steadily increases for a stretch of time, we have a bubble. When people wake up to reality and the P/E ratio plummets, the bubble bursts. See the first graph in the Wikipedia link above for stock market data that show this relationship. These bubbles are counter-examples to the [efficient-market hypothesis](https://en.wikipedia.org/wiki/Efficient-market_hypothesis), which holds that prices already contain all known information about the stock — or, say, the house. Under the hypothesis, a smarty-pants could not predictably outperform the stock (or housing) market, since they can’t know anything that everyone else does not already know. But in reality, people who didn’t believe the hype about houses, such as hedge fund manager Steve Eisman, [got rich by betting that everyone else was nuts](http://www.portfolio.com/news-markets/national-news/portfolio/2008/11/11/The-End-of-Wall-Streets-Boom).

Below the fold, I develop a rough P/E ratio for Western composers, calculate it for 69 eminent ones, and discuss some applications.

For the measurement of the composer’s fundamental value, I use his score in Charles Murray’s [Human Accomplishment](https://www.amazon.com/Human-Accomplishment-Pursuit-Excellence-Sciences/dp/006019247X), which measures how much space he is given across a wide variety of music encyclopedias — how deserving he is. It’s true that article writers could be in the midst of an irrational bubble for Beethoven and devote more space to him than he merits, but by using encyclopedias across many different languages and time periods, Murray protected as much as possible against this bias. He also excluded figures who flourished in the second half of the 20th C, just in case article writers were still affected by a recent bubble.

For the measurement of the public’s subjective valuation of the composer, I use the number of results returned from a search of his name in the “classical” section of Amazon’s music section. (This is the name listed under “composer” in the work’s webpage.) Unlike the number of Google results, the number of works offered for sale is a good measure of how much hype the composer enjoys among real consumers of classical music. I normalize these results by dividing by the maximum number of results (which happens to be for Mozart) and multiplying by 100, to put it on a 0 – 100 scale, as with the HA scores.

The measurement of how under- or over-valued a composer is, the P/E ratio, is just the scaled Amazon score divided by the HA score. Higher P/E scores suggest he is over-hyped — if two composers have the same amount of space devoted to them by those in the best position to objective judge the composers’ excellence, the one with many more works being offered enjoys the influence of hype. And so does the composer who has the same number of works being offered as another, but who has much less space devoted to him in encyclopedias.

One drawback here is that, unlike the P/E ratio for stocks or houses, the two parts of the ratio aren’t measured in the same units, or even close — they are a scaled measure of column inches and a scaled measure of works being offered. So the ratio here doesn’t have an intuitive interpretation. But if we just want to see who’s over- and under-valued, that doesn’t matter.

I calculated this P/E ratio for anyone in Murray’s list of Western composers who scored 10 or above on his 0 to 100 scale, which yielded 69 data-points. To see all composers’ data, [you can download the spreadsheet here](http://manyeyes.alphaworks.ibm.com/manyeyes/datasets/price-earning-ratios-for-composers/versions/1) by clicking on view data and copying & pasting (as text) into an Excel file. Briefly, though, for fun here are the 10 most under- and over-valued composers, where the P/E ratio increases as you go down each list. (Thus, Willaert suffers the least from hype, and Puccini the most.) Bear in mind that “over-valued” does not mean “junk,” and “under-valued” does not mean “awesome” — only that the composer is given too much attention, or too little.

10 most under-valued composers

Adrian Willaert  
Jean-Baptiste Lully  
Anton Webern  
Guillaume de Machaut  
Guillaume Dufay  
Arnold Schoenberg  
Josquin des Prez  
Giovanni Pierluigi da Palestrina  
Jean-Philippe Rameau  
Orlande de Lassus

10 most over-valued composers

Johannes Brahms  
Camille Saint-Saens  
Charles Gounod  
Giuseppe Verdi  
Edvard Grieg  
Antonio Vivaldi  
Antonin Dvorak  
Pyotr Tchaikovsky  
Georges Bizet  
Giacomo Puccini

Despite the presence of hype, though, the Amazon score and HA score agree pretty well with each other, as you see here:

[](http://farm4.static.flickr.com/3356/3416930347_7cc08beabb.jpg)  
The [Spearman rank correlation](http://www.wessa.net/rankcorr.wasp) between the two scores is +0.53 (p less than 10^-6). So, to some degree, the greater the esteem from encyclopedists, the more works are offered for sale. Still, differences in HA scores only account for under 30% of the variation in Amazon popularity, leaving plenty of room for the influence of hype.

And do the P/E scores form a bell-shaped normal distribution? No. The average is 0.73 — about what Domenico Scarlatti scores — but most of the data are below this, and less above it. The graph below shows this skewed distribution, where most composers are actually rather under-valued and a handful are fairly over-hyped.

[](http://farm4.static.flickr.com/3355/3419900305_c9d1a07a5c.jpg)  
I don’t have Amazon scores going back years — or even one year — so I can’t make a series similar to the one that shows rising P/E ratios as the stock market enters a bubble, and declining values when the bubble bursts. I could find how many articles JSTOR contains that mention the composer, and measure this for all 69 composers across the years, and re-scale them by dividing by the maximum score in each year. But I’m not that interested in this topic, so I’ve done something a little different to detect bubbles.

Murray also includes the year that each composer flourished — i.e., when he turned 40 — and I’ve plotted each composer’s P/E score for the year he flourished. This allows us to see if composers from one time period are more or less over-hyped compared to those of another:

[](http://farm4.static.flickr.com/3623/3417737824_72116c97ba.jpg)  
The composers of the pre-Classical periods (Medieval, Renaissance, and Baroque) are below-average in hype. Classical composers are average or a bit below, and the early Romantics are also about average. However, the late Romantics are vastly over-hyped. The Moderns are all over the place, although none is very over-hyped. It could be, though, that for the Moderns, an “overlooked” composer could have an unjustifiably high HA score, if Murray’s article writers were not yet distanced enough to avoid the effects of recent manias  
for Modern composers.

As a non-music buff, I feel my pedestrian tastes have been vindicated, as I’ve never gotten into the late Romantic period, but have always loved the Baroque most, then Classical, and even some early Romantic stuff. I have some catching up to do with Medieval and Renaissance composers, though. Culture mavens tell me that Baroque music is considered too nerdy and mostly suited for guy consumption, while the Romantics appeal more to normal people and women. So, music that appeals to more emotional people is over-valued, while music that appeals to more cerebral people is under-valued. This confirms that over-hyping something and an irrational, emotional mindset go hand-in-hand.

On the topic of bubbles, Murray mentions that you do see fashion cycles, or booms and busts, in the percentage of an orchestra’s output that comes from a particular composer — e.g., that Bach might be very popular one year and decline for the next, say, 10 years. This is despite the fact that the aesthetic value of his work — however we measure it — hasn’t changed.

I think this argues against the cultural version of the efficient-market hypothesis. The public valuation of a composer may capture plenty of information about his fundamental worth, but there’s a lot that’s left out, such as the strong chance that a composer with a high P/E ratio owes some of his popularity to a bubble mindset among consumers.

There are plenty of other cases you can apply this approach to, not to mention further refinements in looking at composers. What I’d really like to see is an objective measure of female celebrities’ attractiveness — say, by plugging measurements of their face, body, etc., into a regression equation — and compare this against the number of results returned in a Google Image search for their name. I predict Angelina Jolie would score in the far-over-hyped range, Monica Bellucci in the average range of hype, and Jean Shrimpton in the over-looked range.

### Related Posts:

- [Measuring whether a painter is under or
  over-valued](https://www.gnxp.com/WordPress/2009/04/19/measuring-whether-a-painter-is-under-or-over-valued/) - [The economic
  correction](https://www.gnxp.com/WordPress/2012/08/18/the-economic-correction/) - [Earnings and skin color among
  immigrants](https://www.gnxp.com/WordPress/2007/02/01/earnings-and-skin-color-among-immigrants/) - [Mice & digit
  ratio](https://www.gnxp.com/WordPress/2008/09/17/mice-digit-ratio/) - [The Inheritance of Inequality: Big Insight, Small
  Error](https://www.gnxp.com/WordPress/2008/07/18/the-inheritance-of-inequality-big-insight-small-error/) - [Bias toward the
  beautiful](https://www.gnxp.com/WordPress/2008/08/24/bias-toward-the-beautiful/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F04%2F07%2Fmeasuring-whether-an-artist-is-under-or-over-valued%2F&linkname=Measuring%20whether%20an%20artist%20is%20under-%20or%20over-valued "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F04%2F07%2Fmeasuring-whether-an-artist-is-under-or-over-valued%2F&linkname=Measuring%20whether%20an%20artist%20is%20under-%20or%20over-valued "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F04%2F07%2Fmeasuring-whether-an-artist-is-under-or-over-valued%2F&linkname=Measuring%20whether%20an%20artist%20is%20under-%20or%20over-valued "Email")[](https://www.addtoany.com/share)
