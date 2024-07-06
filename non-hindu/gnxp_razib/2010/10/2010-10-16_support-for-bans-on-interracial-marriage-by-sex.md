+++
title = "Support for bans on"
full_title = "Support for bans on interracial marriage by sex"
date = "2010-10-16"
upstream_url = "https://www.gnxp.com/WordPress/2010/10/16/support-for-bans-on-interracial-marriage-by-sex/"

+++
Source: [here](https://www.gnxp.com/WordPress/2010/10/16/support-for-bans-on-interracial-marriage-by-sex/).

Support for bans on interracial marriage by sex

A quick follow-up to [my previous post](http://blogs.discovermagazine.com/gnxp/2010/10/female-race-consciousness-as-prudence/) which points to the data that women tend to be more race-conscious in dating than men. There’s a variable in the [GSS](http://sda.berkeley.edu/cgi-bin/hsda?harcsda+gss08) which asks if you support a ban on interracial marriage, RACMAR. Here’s the question itself:

> Do you think there should be laws against marriages between (Negroes/Blacks/African-Americans) and whites?

There isn’t much surprising in the results for this variable. It was asked between 1972 and 2002, and support for a ban on interracial marriages dropped over time. Whites, old people, conservatives, and less educated people, tended to support these bans, as well as Southerners. But what about men vs. women? I’ve never actually looked at that. I limited the sample to whites; the number of blacks in the sample is small and wouldn’t alter the result, but I figured I’d control for race anyway. Support for such laws is in the 35-40% range for whites in 1972, before dropping off to 5-15% in 2002.

Here’s the trendline broken down by sex:

  
![antimisclaw](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2010/10/antimisclaw.png?resize=546%2C470)![antimisclaw](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2010/10/antimisclaw.png?resize=546%2C470)

There is a small but consistent difference until the last year. The difference is within 95% intervals within a given year of course. But the consistency of the greater female support for interracial marriage bans made me want to perform a [logistic regression](https://en.wikipedia.org/wiki/Logistic_regression). I decided to look at the total sample, and also limit it to the 1970s. The pseudo r-square for both is \~0.20. Italics means lack of statistical significance. The other values were all p = 0.000 in the GSS interface.

[TABLE]

These results confirm that being female predicts a greater likelihood of supporting laws against interracial marriage. Having more education and being intelligent reduced the probability. Surprisingly year and age don’t matter much when you’re taking other variables into account.

As a final note, let’s compare sex differences on another issue: homosexuality. The HOMOSEX variable asks about “sexual relations between adults of the same sex.” There are four responses:

1 = Always wrong

2 = Almost always wrong

3 = Sometimes wrong

4 = Not wrong at all

Using the GSS I computed the *mean* value year by year. So if in 1974 50% said homosexual sex was always wrong, and 50% not wrong at all, you’d have a mean value of 2.5. Here is the trendline by year by sex:

![homsexsex](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2010/10/homsexsex.png?resize=541%2C466)![homsexsex](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2010/10/homsexsex.png?resize=541%2C466)

As with interracial marriage, there is a small, but consistent, sex difference. On the margins the sex difference will disappear, so one can think of it as one sex “lagging” the other on social change.

### Related Posts:

- [Whites favor law against interracial marriage
  where?](https://www.gnxp.com/WordPress/2009/04/18/whites-favor-law-against-interracial-marriage-where/) - [Can 46% of Mississippi Republicans favor banning
  interracial…](https://www.gnxp.com/WordPress/2011/04/07/can-46-of-mississippi-republicans-favor-banning-interracial-marriage/) - [Gap in attitudes toward interracial marriage
  gone](https://www.gnxp.com/WordPress/2010/02/01/gap-in-attitudes-toward-interracial-marriage-gone/) - [Who are the cultural
  integrators?](https://www.gnxp.com/WordPress/2009/06/02/who-are-the-cultural-integrators/) - [Interracial marriage and Asian
  Americans](https://www.gnxp.com/WordPress/2008/02/18/interracial-marriage-and-asian-americans/) - [Guess who's coming to dinner: the
  stranger](https://www.gnxp.com/WordPress/2017/10/10/guess-whos-coming-to-dinner-the-stranger/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F10%2F16%2Fsupport-for-bans-on-interracial-marriage-by-sex%2F&linkname=Support%20for%20bans%20on%20interracial%20marriage%20by%20sex "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F10%2F16%2Fsupport-for-bans-on-interracial-marriage-by-sex%2F&linkname=Support%20for%20bans%20on%20interracial%20marriage%20by%20sex "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F10%2F16%2Fsupport-for-bans-on-interracial-marriage-by-sex%2F&linkname=Support%20for%20bans%20on%20interracial%20marriage%20by%20sex "Email")[](https://www.addtoany.com/share)
