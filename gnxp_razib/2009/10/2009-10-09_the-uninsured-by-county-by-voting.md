+++
title = "The uninsured, by"
full_title = "The uninsured, by county, by voting"
date = "2009-10-09"
upstream_url = "https://www.gnxp.com/WordPress/2009/10/09/the-uninsured-by-county-by-voting/"

+++
Source: [here](https://www.gnxp.com/WordPress/2009/10/09/the-uninsured-by-county-by-voting/).

The uninsured, by county, by voting

*The New York Times* has a piece, [The Divided States of Health Care](http://www.nytimes.com/2009/10/10/business/economy/10charts.html?ref=business):

> Those who lack health insurance now are far more likely to live in > states that usually vote Republican â€” the states whose senators and > representatives are least likely to support a law to extend coverage. >
> That would seem to indicate that Republican constituents are the ones > who would most benefit from passage of universal health insurance > coverage. But an analysis of Congressional districts within those > states indicates that those without health insurance are much more > likely to live in strongly Democratic Congressional districts. Many of > those contain large minority populations with relatively low incomes.

[](https://www.gnxp.com/blog/uploaded_images/healthinsurancecounties-762032.png)This is not a surprising finding. Some of the most Democratic districts due to variables of race & income are in “Red States.” The text alludes to more granular analysis, but it doesn’t show up in the graphics, which is focused on the state level. But the county level data is freely available from the Census. To the left is a map of uninsured (those 18-64) by county. It does seem to me that state regulations or policies have some influence, look at the Pennsylvania-Ohio border with Kentucky and West Virginia, and Pennsylvania’s border with New York. Culturally the Appalachian areas of Pennsylvania are extensions of West Virginia. Or look at the Missouri-Iowa border. But we can do more than just look at maps. Let’s compare the county-by-county variation against other metrics. For example, how about voting for this year’s Nobel Peace Prize recipient in the fall of 2008. What’s the correlation?

I was a little surprised when I got a correlation of -0.33. That is, a **negative** correlation for voting for Barack Obama and proportion of uninsured on the county level. This assumes a level of linearity which really isn’t there when you look more closely. You can see in the scatterplots at the bottom of this post, but let’s just go with the linear for the moment so I can stick to correlations; you can correct by looking at the loess curves later on. Here are some other correlations with the proportion uninsured in each county (most of the dta are from the American Community Survey 2005-2007 of the Census, the “Foreign Born Males” data are for males over the age of 18):

-.36 – White (not Latino)  
0.07 – Black (not Latino)  
0.48 – Latino  
0.43 – Foreign Born Males  
-.29 – Age  
-.24 – Median Household Income (2006)  
-.15 – Median Home Value (2006)

I was a little curious about the lack of correlation with health insurance for blacks, but this from the Census clears it up:

> At 89.4 percent, non-Hispanic Whites were more likely to have health > insurance coverage than any other racial group. Those reporting ‘some > other race’ were the least likely to have coverage, 66.0 percent > \[most of ‘some other race’ are probably Latino -Razib\]. The health > insurance coverage rates for the remaining single-race groups fell in > that range – 85.5 percent for Asians, 83.8 percent for Native > Hawaiians and Other Pacific Islanders, 82.0 for Blacks, and 68.4 > percent for American Indians and Alaska Natives. The health insurance > coverage rate for Hispanics was 68.5 percent.

This includes **both** private health insurance and public health insurance (Medicaid) for those under 65. Look at the [map for those at or below 200% of the poverty rate](http://www.census.gov/did/www/sahie/data/2006/files/Age064_Pct_UI_below200IPR_2006.pdf). It looks like Medicaid is covering many people in the [Black Belt](https://en.wikipedia.org/wiki/Black_Belt_(U.S._region)), while regions in Appalachia which aren’t quite as destitute in northern Alabama and Mississippi are relatively underinsured. The Census also reports that those ages 18-24, and 25-34, have coverage rates of 71.4 and 73.3 respectively, before jumping up to nearly 81% in the 35-44 range. For non-citizens the rate is around 50%.

How about limiting the data set to those counties where 90% of the population is white, not hispanic. That leaves 1477 counties in the data set.

-.48 – Obama  
-.30 – Income  
-.12 – Home Value

As you can see, in **very white counties the inverse relationship between proportion uninsured and proportion voting for Barack Obama holds.** I played around with limiting geographically. In New England and Tennessee there’s no correlation between voting for Obama and insurance rates. But New England had really uniform voting. Tennessee might be a special case where lower insurance coverage rates among blacks are at play. In California and Texas the lack of insurance among Latinos positive correlations between voting for Obama and underinsurance, but only on the order of \~0.10.

I’m a little confused by these results. You can get the original data [as a csv](http://scienceblogs.com/gnxp/upload/2009/10/insurance.csv) and see if I switched the sign or did something wrong. I wouldn’t be surprised. My general model though is that this is a case of:

1\) The Dems tending to get high and low socioeconomic status groups (not necessarily the super-rich, but the middle and upper-middle class college-educated).

2\) The poor get insurance through Medicaid. And public sector workers and small business people of approximately same incomes are likely to differ in their insurance rates (public sector workers are overwhelmingly insured from what I know).

3\) Democratic leaning states have more robust insurance systems for the poor. Take a close look at some of the inter-state differences on the borders; rather stark. In a lot of data county level variation doesn’t give you a sense of state borders, especially those dictated by latitude or longitude. Not so here.

Here are the some plots.

[](https://www.gnxp.com/blog/uploaded_images/inallcounties-763879.png)

[](https://www.gnxp.com/blog/uploaded_images/in90whitecounties-780907.png)

[](https://www.gnxp.com/blog/uploaded_images/inincome-700064.png)

[](https://www.gnxp.com/blog/uploaded_images/inblack-729584.png)

[](https://www.gnxp.com/blog/uploaded_images/inforeign-774094.png)

[](https://www.gnxp.com/blog/uploaded_images/inlatino-748401.png)

### Related Posts:

- [Post-genomic era = socialized
  medicine?](https://www.gnxp.com/WordPress/2006/11/15/post-genomic-era-socialized-medicine/) - [The end of insurance (some if
  it)](https://www.gnxp.com/WordPress/2017/05/15/the-end-of-insurance-some-if-it/) - [Genomics &
  insurance](https://www.gnxp.com/WordPress/2007/08/27/genomics-insurance/) - [Why the Democratic wave may be bigger because
  of…](https://www.gnxp.com/WordPress/2017/12/26/why-the-democratic-wave-may-be-bigger-because-of-gerrymandering/) - [Map of Health in
  America](https://www.gnxp.com/WordPress/2009/03/11/map-of-health-in-america/) - [Health insurance remains (and will remain)
  relevant](https://www.gnxp.com/WordPress/2012/03/09/health-insurance-remains-and-will-remain-relevant/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F10%2F09%2Fthe-uninsured-by-county-by-voting%2F&linkname=The%20uninsured%2C%20by%20county%2C%20by%20voting "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F10%2F09%2Fthe-uninsured-by-county-by-voting%2F&linkname=The%20uninsured%2C%20by%20county%2C%20by%20voting "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F10%2F09%2Fthe-uninsured-by-county-by-voting%2F&linkname=The%20uninsured%2C%20by%20county%2C%20by%20voting "Email")[](https://www.addtoany.com/share)
