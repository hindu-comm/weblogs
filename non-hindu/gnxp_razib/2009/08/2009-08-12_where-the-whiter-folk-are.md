+++
title = "Where the Whiter Folk"
full_title = "Where the Whiter Folk Are"
date = "2009-08-12"
upstream_url = "https://www.gnxp.com/WordPress/2009/08/12/where-the-whiter-folk-are/"

+++
Source: [here](https://www.gnxp.com/WordPress/2009/08/12/where-the-whiter-folk-are/).

Where the Whiter Folk Are

Today I combined some Census data with 2008 election results (thanks [Cosma](http://www-personal.umich.edu/~mejn/election/2008/)). Though Barack Obama won the vote last fall, he lost the Non-Hispanic white vote. It stands to reason then that the whiter and less Hispanic a county is, the more likely it would be to tilt McCain. I was curious as to geographic variation within this general rule-of-thumb. So I plotted the % who voted for Obama in a county vs. the % who were Non-Hispanic whites (according to the 2000 Census\*). I then generated a line of best fit via [loess](https://en.wikipedia.org/wiki/Local_regression), and used the deviations from the trend to generate a map shaded proportionately. In other words, the bluer a county is the more it voted for Obama above expectation based on the overall relationship of the % white Non-Hispanic within a county and vote for Obama (the converse for red naturally). Again, **click the map for the larger image.**

[](http://scienceblogs.com/gnxp/upload/2009/08/SWPLplot2.png)

[](http://scienceblogs.com/gnxp/upload/2009/08/trendnamp1b.png)

I also decided to constrain the data set to those counties which were at minimum 80% Non-Hispanic white. Mostly because the [“Black Belt”](https://en.wikipedia.org/wiki/Black_Belt_(U.S._region)) counties are showing up on the above map.

[](http://scienceblogs.com/gnxp/upload/2009/08/trendnamp2.png)

Finally, a shaded map of the results.

[](http://scienceblogs.com/gnxp/upload/2009/08/ElectionMapPurpleCounty.jpg)

1\) Don’t mess with Texas Obama. Despite Obama winning the Hispanic counties in the South, those counties are always underperforming relative to other majority-minority districts. Since some of those counties are 90% Hispanic it probably isn’t just Non-Hispanic white swing in the other direction.

2\) Though Obama lost much of the rural North and East, he overperformed when you use the whole nation as a reference point, in particular rural areas in the West and South.

3\) Pennsylvania kind of does look like Pittsburgh + Philadelphia, with Alabama in the middle.

4\) Obama did well in [Greater New England](http://www.prospect.org/cs/articles?articleId=8954). Less well in the [Butternut Region](http://wiki.answers.com/Q/Where_is_the_butternut_region) of the southern Midwest settled from the South.

Here are a list of the 200 counties furthest from the trendlines. The first 100 are the most pro-Obama above expectation when the predictor is Non-Hispanic white %. The last 100 the most pro-McCain.

[TABLE]

\* This is 8 years out of date, but by far the most complete and precise data set until the 2010 Census.

### Related Posts:

- ["Americans" don't like Barack Hussein
  Obama](https://www.gnxp.com/WordPress/2009/12/08/americans-dont-like-barack-hussein-obama/) - [The white vote for Obama, by county &
  correlates](https://www.gnxp.com/WordPress/2009/11/28/the-white-vote-for-obama-by-county-correlates/) - [What's not the matter with
  Appalachia](https://www.gnxp.com/WordPress/2009/08/16/what-s-not-the-matter-with-appalachia/) - [Tracing the tribes of American
  politics](https://www.gnxp.com/WordPress/2009/11/14/tracing-the-tribes-of-american-politics/) - [American data by
  counties](https://www.gnxp.com/WordPress/2009/11/29/american-data-by-counties/) - [The uninsured, by county, by
  voting](https://www.gnxp.com/WordPress/2009/10/09/the-uninsured-by-county-by-voting/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F08%2F12%2Fwhere-the-whiter-folk-are%2F&linkname=Where%20the%20Whiter%20Folk%20Are "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F08%2F12%2Fwhere-the-whiter-folk-are%2F&linkname=Where%20the%20Whiter%20Folk%20Are "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F08%2F12%2Fwhere-the-whiter-folk-are%2F&linkname=Where%20the%20Whiter%20Folk%20Are "Email")[](https://www.addtoany.com/share)
