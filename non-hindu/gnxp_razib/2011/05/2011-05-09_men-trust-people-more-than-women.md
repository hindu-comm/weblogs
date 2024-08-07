+++
title = "Men trust people more"
full_title = "Men trust people more than women do"
date = "2011-05-09"
upstream_url = "https://www.gnxp.com/WordPress/2011/05/09/men-trust-people-more-than-women/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/05/09/men-trust-people-more-than-women/).

Men trust people more than women do

One of the weird things I randomly noticed when querying the “TRUST” variable in the [GSS](http://sda.berkeley.edu/cgi-bin/hsda?harcsda+gss10) was that men were more trusting than women. I didn’t think much of that, but take a look at this logistic regression:

|                                                      |                         |             |                         |             |
|------------------------------------------------------|-------------------------|-------------|-------------------------|-------------|
| **Trust in people, sample from after the year 2000** |                         |             |                         |             |
|                                                      |                         |             |                         |             |
| **Logistic regression**                              |                         |             |                         |             |
| **Variable**                                         | **All**                 |             | **Non-Hispanic white**  |             |
|                                                      | B                       | Probability | B                       | Probability |
| SEX                                                  | -0.340                  | 0.000       | -0.485                  | 0.000       |
| WORDSUM                                              | 0.176                   | 0.000       | 0.201                   | 0.000       |
| DEGREE                                               | 0.343                   | 0.000       | 0.274                   | 0.000       |
| COHORT                                               | -0.018                  | 0.000       | -0.013                  | 0.001       |
| SEI                                                  | 0.002                   | 0.393       | 0.003                   | 0.394       |
| POLVIEWS                                             | -0.105                  | 0.011       | -0.121                  | 0.018       |
| PARTYID                                              | 0.073                   | 0.019       | 0.011                   | 0.777       |
| GOD                                                  | -0.035                  | 0.438       | 0.015                   | 0.765       |
| ATTEND                                               | 0.023                   | 0.261       | 0.038                   | 0.105       |
|                                                      |                         |             |                         |             |
|                                                      | Pseduo R-square = 0.096 |             | Pseduo R-square = 0.083 |             |

The outcomes are “can trust people = 1” and “cannot trust people = 0.” I removed “depends” (which is never more than 5-10% in a class anyway). For sex 1 = male and 2 = female, so you can immediately see that being a woman will reduce the odds of being trusting. WORDSUM, vocabulary score, and educational attainment go in the direction you’d expect. Interestingly controlling for education doesn’t remove the vocabulary effect. COHORT is the year you were born. Lower values indicate older individuals in the data set. Younger people are less trusting, so this makes sense. To my surprise on the individual level religion doesn’t seem that important.

Since the sample sizes for sex are huge I thought I’d compare sex differences in trust over the years by demographic variable.

  
[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust1.jpg?resize=566%2C475)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust1.jpg?resize=566%2C475)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust1.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust2.jpg?resize=568%2C478)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust2.jpg?resize=568%2C478)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust2.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust3.jpg?resize=567%2C478)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust3.jpg?resize=567%2C478)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust3.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust4.jpg?resize=566%2C479)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust4.jpg?resize=566%2C479)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust4.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust5.jpg?resize=567%2C484)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust5.jpg?resize=567%2C484)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust5.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust6.jpg?resize=567%2C485)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust6.jpg?resize=567%2C485)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust6.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust7.jpg?resize=567%2C485)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust7.jpg?resize=567%2C485)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust7.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust8.jpg?resize=565%2C478)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust8.jpg?resize=565%2C478)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust8.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust9.jpg?resize=566%2C480)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust9.jpg?resize=566%2C480)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust9.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust10.jpg?resize=569%2C477)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust10.jpg?resize=569%2C477)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust10.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust11.jpg?resize=594%2C479)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust11.jpg?resize=594%2C479)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust11.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust12.jpg?resize=595%2C478)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust12.jpg?resize=595%2C478)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust12.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust14.jpg?resize=596%2C479)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust14.jpg?resize=596%2C479)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust14.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust15.jpg?resize=567%2C479)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust15.jpg?resize=567%2C479)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust15.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust16.jpg?resize=565%2C476)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust16.jpg?resize=565%2C476)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust16.jpg)[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust17.jpg?resize=569%2C478)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust17.jpg?resize=569%2C478)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/05/sextrust17.jpg)

### Related Posts:

- [Another genetic map of
  Europe](https://www.gnxp.com/WordPress/2008/11/21/another-genetic-map-of-europe/) - [Support for bans on interracial marriage by
  sex](https://www.gnxp.com/WordPress/2010/10/16/support-for-bans-on-interracial-marriage-by-sex/) - [A relationship in attitudes toward Global Warming
  &…](https://www.gnxp.com/WordPress/2010/10/24/a-relationship-in-attitudes-toward-global-warming-evolution/) - [The Indo-European
  Völkerwanderung](https://www.gnxp.com/WordPress/2015/02/11/the-indo-european-volkswanderung/) - [40 year old
  virgins!!!](https://www.gnxp.com/WordPress/2009/06/11/40-year-old-virgins/) - [Data access to the
  GSS](https://www.gnxp.com/WordPress/2006/09/26/data-access-to-the-gss/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F05%2F09%2Fmen-trust-people-more-than-women%2F&linkname=Men%20trust%20people%20more%20than%20women%20do "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F05%2F09%2Fmen-trust-people-more-than-women%2F&linkname=Men%20trust%20people%20more%20than%20women%20do "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F05%2F09%2Fmen-trust-people-more-than-women%2F&linkname=Men%20trust%20people%20more%20than%20women%20do "Email")[](https://www.addtoany.com/share)
