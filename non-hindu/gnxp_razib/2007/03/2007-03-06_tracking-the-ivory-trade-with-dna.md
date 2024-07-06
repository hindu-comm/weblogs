+++
title = "Tracking the ivory trade"
full_title = "Tracking the ivory trade with DNA"
date = "2007-03-06"
upstream_url = "https://www.gnxp.com/WordPress/2007/03/06/tracking-the-ivory-trade-with-dna/"

+++
Source: [here](https://www.gnxp.com/WordPress/2007/03/06/tracking-the-ivory-trade-with-dna/).

Tracking the ivory trade with DNA

[](https://www.gnxp.com/blog/uploaded_images/elephant-723949.gif)A [new paper in PNAS](http://www.pnas.org/cgi/content/full/104/10/4228) (open access) uses DNA isolated from seized ivory to investigate where elephant poaching is occurring. It’s an interesting idea, but for me the idea itself takes a back seat to the clever statistical framework in which it’s implemented. The analysis of DNA data is getting more and more sophisticated; this is an excellent example of that phenomenon.

The paper starts with very little data– 37 tusks from this ivory seizure along with a database of DNA samples of elephants from all over Africa. Traditional methods would treat each of the 37 tusks independently, but the authors want to consider the possibliity that all came from a single area as well as the possiblity that all are from disparate parts of the continent (the two possiblities have different implications for law enforcement). So they create a grid on all of Africa (actually, just the subset containing the elephant range) and [randomly split the grid into polygons](https://en.wikipedia.org/wiki/Voronoi), considering each polygon as equally likely to be part of area where elephants were poached. This gives them a [prior distribution](https://en.wikipedia.org/wiki/Prior_probability) for the origin of the poached elephants.

They then use their data and the existing database to estimate the [posterior distribution](https://en.wikipedia.org/wiki/Posterior_probability) for that origin using [Markov chain Monte Carlo](https://en.wikipedia.org/wiki/Markov_Chain_Monte_Carlo). They provide evidence that this method works very well at distinguishing the two possiblities (a single origin of the elephants or a disparate collection), an advertisement for [Bayseian methods](https://en.wikipedia.org/wiki/Bayesian_statistics) and their ability to get as much information as possible from limited data. As can be seen in the figure, all the elephants seem to come from an area centered around Zambia. This has had some consequences:

> The seizure immediately followed Zambia’s application to CITES for a > one-off sale of their ivory stockpiles at COP12 (Conference of the > Parties). That application maintained that only 135 elephants were > known to have been illegally killed in Zambia during the previous 10 > years, woefully shy of the 3,000-6,500 elephants we estimate to have > been killed in Zambia surrounding the seizure, let alone during that > entire 10-year period. Subsequent to being informed of our findings, the Zambian government replaced its director of wildlife and began imposing significantly harsher sentences for convicted ivory traffickers in its courts.

### Related Posts:

- [Elephants without
  tusks?](https://www.gnxp.com/WordPress/2013/03/31/elephants-without-tusk/) - [Human driven elephant
  evolution?](https://www.gnxp.com/WordPress/2008/01/22/human-driven-elephant-evolution/) - [DNA databases -
  revisited](https://www.gnxp.com/WordPress/2006/05/24/dna-databases-revisited/) - [A DNA database
  nation?](https://www.gnxp.com/WordPress/2006/05/20/a-dna-database-nation/) - [130,000 year old Mastodon
  DNA?](https://www.gnxp.com/WordPress/2007/07/22/130000-year-old-mastodon-dna/) - [DNA databases and DNA
  profiling](https://www.gnxp.com/WordPress/2007/03/12/dna-databases-and-dna-profiling/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F03%2F06%2Ftracking-the-ivory-trade-with-dna%2F&linkname=Tracking%20the%20ivory%20trade%20with%20DNA "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F03%2F06%2Ftracking-the-ivory-trade-with-dna%2F&linkname=Tracking%20the%20ivory%20trade%20with%20DNA "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F03%2F06%2Ftracking-the-ivory-trade-with-dna%2F&linkname=Tracking%20the%20ivory%20trade%20with%20DNA "Email")[](https://www.addtoany.com/share)
