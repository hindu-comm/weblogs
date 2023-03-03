+++
title = "Maxim's audience prefers"
full_title = "Maxim's audience prefers brunettes; distribution is bimodal"
date = "2008-07-06"
upstream_url = "https://www.gnxp.com/WordPress/2008/07/06/maxim-s-audience-prefers-brunettes-distribution-is-bimodal/"

+++
Source: [here](https://www.gnxp.com/WordPress/2008/07/06/maxim-s-audience-prefers-brunettes-distribution-is-bimodal/).

Maxim's audience prefers brunettes; distribution is bimodal

While showing that [the super-popularity of blonds is recent](https://www.gnxp.com/blog/2008/06/bygone-brunette-beauty-fashion-in-hair.php), I saw an apparent reversal of the upward trend around 2000, suggesting that perhaps Playboy readers are becoming fatigued by blonds. To get a better feel for what the younger generations prefer, let’s look at Maxim magazine (US edition), whose [average reader is 27.5 years old](http://media.www.nineronline.com/media/storage/paper971/news/2003/12/08/TheDailyExtra/Playboy.Makeover.Aims.To.Lure.Younger.Readers-2006655.shtml) (by contrast, the average Playboy reader is 32.5). Maxim is the contemporary counterpart to Playboy — it’s widespread on college campuses, and is what horny dudes are likely to leaf through to ogle hot babes. They also have roughly the same circulation — about 2.5 million. For those in a rush, I’ve boldfaced all key results.

Audacious Epigone and I have both done analyses on the Maxim Hot 100 lists for recent years (see [here](https://www.gnxp.com/blog/2006/12/western-ideals-of-beauty-look-to-south.php) and [here](https://anepigone.blogspot.com/2008/05/demographic-profile-of-maxims-hottest.html)). But these smell of “lists just for the fun of making lists” or “lists to get people arguing,” and the fact that A.E.’s results and mine varied so much despite analyzing consecutive years supports that idea. However, there are at least two datasets that are surely more shaped by audience demand than the editors’ whims: the girls who appear on the cover to lure the reader into purchasing it (they are featured prominently inside as well), and the girls who readers vote as being the hottest out of a pool of “Hometown Hotties” nominees.

First, I looked at [all covers of Maxim](http://www.maximcovers.com/index.aspx?imgCollectId=48&SlideGroup=1) from 1997 to present, excluding only two issues that did not show people, which yielded 126 covers. To be more fine-grained than before, I coded hair color as 1 = light blond, 2 = dark blond, 3 = light brown, 4 = dark brown, and set aside 0 for redheads. If there were multiple girls on a cover, or if an issue had multiple covers available, I took the average of all girls for that issue. For a few, it was too close to call, so I coded the girl halfway between two categories. If the cover was ambiguous, I looked at the full photo shoot through a Google Images search. There was no significant trend in blondness over the past 11 years.

To determine the average hair color, I re-coded redheads as 2.5 (there were only 2 of 126, so this choice doesn’t really make a difference). The average Maxim cover girl scores 2.8 — light brown. To determine the frequency distribution, I binned girls into light blond, dark blond, light brown, and dark brown, with redheads going into the light brown bin. Some data-points were not integers, so I used both conventions for rounding the numbers with .5 (“up” and “down”). It turned out to make almost no difference. Here is the distribution using “rounding up”:

[](https://www.gnxp.com/blog/uploaded_images/MaximCovers-739839.JPG)

Light blonds and dark browns are overrepresented, while the intermediate colors are underrepresented. To test this, I used [published data on hair color frequencies](https://www.gnxp.com/blog/2007/11/brown-eyed-girl.php) and took the Dutch values instead of the Icelandic ones, since Americans must resemble the former more than the latter. Because the published estimates have only one intermediate category, I had to merge the dark blond and light brown categories together. I put redheads in the intermediate category since otherwise I wouldn’t be able to do a chi-squared test (an expected number would be too small). For rounding up, chi-squared = 24.1 (p less than 0.0001, df = 2); and for rounding down, chi-squared = 27.4 (p less than 0.0001, df = 2). So, the discrepancy between Maxim cover girls and the general population is no fluke.

But are light blonds and dark browns equally overrepresented? No: depending on the rounding convention, light blonds are 25-29% more common than we’d expect, whereas dark browns are 63-66% more common than we’d expect. Together with the average cover girl being light brown, I conclude that Maxim readers respond more to women with dark hair, although there is a sizable minority that prefers light hair.

Second, I did a similar analysis on the [finalists in Maxim’s Hometown Hotties](http://www.maximonline.com/hotties/winners.aspx) contest from 2003 to 2007. For 10 weeks each year, Maxim staffers scour the country to photograph 100 local hotties per week. Of these 100, Maxim readers vote online to determine 10 semi-finalists and 1 finalist for that week. There is no way I’m looking through 5000 pictures to see what all the contestants look like, and the 5 winners are too small of a sample. The 50 finalists seem like enough data to get a good picture. (Someone else can analyze all 500 semi-finalists.) Indeed, the results are virtually identical to the cover girl results, which shows that both datasets are reliably measuring the same thing. The methods are as before. Here is the distribution of hair types among Hometown Hotties finalists:

[](https://www.gnxp.com/blog/uploaded_images/MaximHometown-767326.JPG)

Once more, light blonds and dark browns are overrepresented, while intermediate colors are underrepresented. For rounding up, chi-squared = 10.3 (p = 0.0058, df = 2); for rounding down, chi-squared = 13.1 (p = 0.0014, df = 2). These results are no fluke. As before, though, dark browns are more overrepresented than light blonds: by 57-64% compared to 22-52%, respectively, depending on the rounding convention. (The convention for rounding didn’t make much of a difference overall in these data either, but since the sample size is less than half that of the cover girl data, it introduces more uncertainty.) Replicating the cover girl results, the average Hometown Hotties finalist scores 2.8 — light brown. I conclude what I did in the cover girl case.

To see how closely the two datasets agree with each other, I did a chi-squared test for the observed values in one, using the other’s frequencies as the expected ones. Taking the cover girl frequencies as expected, the hometown hotties data are no different (chi-squared = 0.025, p = 0.9875, df = 2). The same holds for the other way around (chi-squared = 0.068, p = 0.9666, df = 2). That is for rounding up, but rounding down produced p-values above 0.5 as well. I conclude that both datasets measure the same thing — audience preferences.

As a final anecdote in support of the bigger picture, consider the [Miss Maxim](http://www.maximonline.com/miss_maxim/) girls. Although about 1/2 of the 24 countries could have easily supplied a blond, only 1/6 actually did. The girls from Belgium, England, and so on, look quite different from the average Belgian, Englishwoman, etc. Clearly, among Maxim’s horndog audience, dark hair rules.

What is causing these two key results — that Maxim readers prefer brunettes, and that the distribution is bimodal? I think brunettes are just more exciting on the level of physiological arousal, so the younger — and therefore the randier  
— the audience is, the more they will prefer dark hair. When Playboy’s circulation was growing exponentially in the 1960s, it featured hardly any blonds and mostly brunettes. As its average reader has become older, its Playmates have become blonder.

Lighter hair is correlated with behavioral inhibition ([see here](http://www.ncbi.nlm.nih.gov/pubmed/16414174)), so it could also be that dark-haired girls get the blood pumping more because they appear more flirtatious.

Or it may be a pure fashion trend — digging blonds is what your father’s generation did, so you set yourselves apart by tacking up pictures of Mila Kunis and Vanessa Minnillo on your wall.

As for the bimodal nature of the distribution, this probably reflects supply meeting demand: the audience’s preferences are likely bimodal, with a majority preferring brunettes and a minority preferring blonds. Guys respond better to the exaggerated version of their tastes, and that drives up the fraction of light blonds and dark browns, in the same way that among porn stars you see an inflated fraction of women with large breasts or large rumps.

### Related Posts:

- [Bygone brunette beauty: Fashion in hair
  color](https://www.gnxp.com/WordPress/2008/06/29/bygone-brunette-beauty-fashion-in-hair-color/) - [Has porn become mainstream? Not
  really](https://www.gnxp.com/WordPress/2008/08/14/has-porn-become-mainstream-not-really/) - [Do women lighten their hair to compensate for
  aging?](https://www.gnxp.com/WordPress/2008/12/15/do-women-lighten-their-hair-to-compensate-for-aging/) - [Decency on the internet, 20 years
  on](https://www.gnxp.com/WordPress/2014/07/31/decency-on-the-internet-20-years-on/) - [Your generation was more into sexualizing young
  girls](https://www.gnxp.com/WordPress/2008/06/30/your-generation-was-more-into-sexualizing-young-girls/) - [Straight porn makes you
  gay](https://www.gnxp.com/WordPress/2009/09/24/straight-porn-makes-you-gay/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F07%2F06%2Fmaxim-s-audience-prefers-brunettes-distribution-is-bimodal%2F&linkname=Maxim%27s%20audience%20prefers%20brunettes%3B%20distribution%20is%20bimodal "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F07%2F06%2Fmaxim-s-audience-prefers-brunettes-distribution-is-bimodal%2F&linkname=Maxim%27s%20audience%20prefers%20brunettes%3B%20distribution%20is%20bimodal "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F07%2F06%2Fmaxim-s-audience-prefers-brunettes-distribution-is-bimodal%2F&linkname=Maxim%27s%20audience%20prefers%20brunettes%3B%20distribution%20is%20bimodal "Email")[](https://www.addtoany.com/share)
