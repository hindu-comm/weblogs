+++
title = "Do women lighten their"
full_title = "Do women lighten their hair to compensate for aging?"
date = "2008-12-15"
upstream_url = "https://www.gnxp.com/WordPress/2008/12/15/do-women-lighten-their-hair-to-compensate-for-aging/"

+++
Source: [here](https://www.gnxp.com/WordPress/2008/12/15/do-women-lighten-their-hair-to-compensate-for-aging/).

Do women lighten their hair to compensate for aging?

[](http://farm4.static.flickr.com/3231/3110371004_4618270763.jpg?v=0)In Jason’s post on [the distributions of hair and eye color](https://www.gnxp.com/blog/2008/12/nlsy-blogging-eye-and-hair-color-of.php), it looks like women are claiming their hair is lighter than it is. The sex differences are the opposite of what is found when the hair is rated by others. Women are lying because they think it makes them look better.

If they’re going to misrepresent their hair color, they’re likely to dye it for the same reason. Whether it is to participate in the [fashion for blonds in their age cohort](https://www.gnxp.com/blog/2008/06/bygone-brunette-beauty-fashion-in-hair.php) or to cater to men in their cohort (there’s evidence that [younger audiences aren’t as captivated by light hair](https://www.gnxp.com/blog/2008/07/maxims-audience-prefers-brunettes.php)), older women should lighten their hair more. It’s like a boob job.

I compared age and hair color data from Playboy Playmates of the Month. I only distinguish between blonds and non-blonds (though there are a few tough calls who I label intermediate). I can’t look at age by year since some years have few points. I’ve grouped the playmates into three ranges: 16 – 20 (n = 210), 21 – 24 (n = 329), and 25 – 35 (n = 105). I chose these groups since each has lots of points. I had to include everyone 25+ in one group, or statistical tests could not have been done.

In any case, these groups also correspond pretty nicely to three phases of a female’s reproductive career: 1) the high school or college girl who doesn’t have to try at all to look presentable; 2) the early-mid 20-something whose waistline has begun expanding; and 3) the 25+ woman who should have had a child. Here is [how the female body shape changes across the lifespan](https://akinokure.blogspot.com/2008/12/you-were-cuter-in-high-school-data.html).

So here is a plot of the proportion of each age group that is blond, along with 1 standard error on either side:

[](http://farm4.static.flickr.com/3250/3110356492_ce8b4e411c.jpg?v=0)

The youngest group (where blonds are 42.1%) is statistically significantly different from the oldest group (where blonds are 53.7%), and marginally significantly different from the middle group (where blonds are 48.3%). The middle and oldest groups are not significantly different. (See Appendix for the gory details.)

I conclude that the 16 – 20 year-old playmates had such flawless and tight skin, clear large eyes, gravity-defying breasts and buttocks, etc., that blond hair wouldn’t add much. Already by their mid-20s, women’s looks have just passed their peak, so that they’re probably more likely to dye their hair, although the difference may be illusory. But certainly by 25, the rest of their face and body couldn’t compete with those of younger girls, so they begin dying their hair blond to distract the audience from that. (Getting fake boobs would probably show a similar age-related trend.) It’s like how restaurants scam the elites by making shitty chicken sandwiches but then tossing on a bit of pesto to make it seem exotic and totally worth \$15.

There’s another prediction of this idea: if playmates were to be drawn increasingly from older women, they should become blonder too. I’ve shown that [the average playmate has gotten older](https://www.gnxp.com/blog/2008/06/your-generation-was-more-into.php) since a low during most of the 1960s, and in the second link in this post I show that they’ve also gotten blonder. Indeed, the [Spearman rank correlation](http://www.wessa.net/rankcorr.wasp) between a year’s average age and average blondness of playmates is +0.35, two-tailed p = 0.006. Taken as a whole, these differences suggest that, even if it isn’t as strongly related to aging as is buying moisturizers and skin-firming lotions, lightening the hair is one way that aging women cope with their declining attractiveness.

But if blond hair enhanced attractiveness to the same degree across all ages, then age would not predict the percent of women who dye their hair — younger girls would do so just as eagerly, as with washing and styling their hair in the morning (a huge boost over a rat’s nest). It seems, then, that blondness yields diminishing returns in attractiveness — I mean, you can’t really picture teen star Selena Gomez having to dye her hair. Or for that matter Audrey Hepburn, Jean Shrimpton, Penelope Cruz, or Monica Bellucci bleaching their hair at any age!

Appendix

I ran an F-test for equality of variances between two samples, one test for each pairwise comparison. None of the three groups had significantly different variances. I then ran a two-proportion z-test (equal variances), one test for each pairwise comparison. The p-values for the tests are: 0.080 (youngest vs. middle), 0.025 (youngest vs. oldest), and 0.164 (middle vs. oldest). These are one-tailed because the prediction was that increasing age should increase the percent who dye their hair or need blond hair to make up for having less attractive skin, breasts, etc. It’s like expecting the percent of women with fake boobs and facelift surgery to increase as age increases.

But I made three comparisons, and the more comparisons you make, the more likely you are to find apparently low p-values just by chance. No one really knows how to deal with adjusting the critical p-value (alpha) when you’re making multiple comparisons. So rather than futz around with the many theoretical corrections to alpha, I decided to take an empirical attack.

I wrote a program in Python that took all the playmates and separated them into three groups, each one having the same size as the three groups I created based on age. But instead of deterministically using age to sort them, I sampled them at random without replacement to fill the first group, then the second group, with the rest going into the third. Because “group 1,” “group 2,” and “group 3” were formed randomly, the proportion of blonds shouldn’t be too different between them. I performed the same two-proportion z-test (equal variances) as before, one for each pairwise comparison.

I simulated this process 10,000 times, and then took the fraction across all runs that the z-statistic was at least as large as the observed z-statistic, doing so for each of the three group comparisons. These empirical p-values are: 0.0813 (youngest vs. middle), 0.0226 (youngest vs. oldest), and 0.1564 (middle vs. oldest). Therefore, in this case, correcting alpha for multiple comparisons would have been pointless, perhaps because I only made three rather than three thousand comparisons.

### Related Posts:

- [NLSY blogging: Eye and hair color of
  Americans](https://www.gnxp.com/WordPress/2008/12/13/nlsy-blogging-eye-and-hair-color-of-americans/) - [How swarthy are the
  Sami?](https://www.gnxp.com/WordPress/2007/07/10/how-swarthy-are-the-sami/) - [Brown eyed
  girl?](https://www.gnxp.com/WordPress/2007/11/20/brown-eyed-girl/) - [Hair, eye and skin color in
  Europeans](https://www.gnxp.com/WordPress/2007/11/01/hair-eye-and-skin-color-in-europeans/) - [Genetics of hair
  color](https://www.gnxp.com/WordPress/2006/10/26/genetics-of-hair-color/) - [Hair Color and Skin Pigmentation in
  Europeans](https://www.gnxp.com/WordPress/2008/05/17/hair-color-and-skin-pigmentation-in-europeans/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F12%2F15%2Fdo-women-lighten-their-hair-to-compensate-for-aging%2F&linkname=Do%20women%20lighten%20their%20hair%20to%20compensate%20for%20aging%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F12%2F15%2Fdo-women-lighten-their-hair-to-compensate-for-aging%2F&linkname=Do%20women%20lighten%20their%20hair%20to%20compensate%20for%20aging%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F12%2F15%2Fdo-women-lighten-their-hair-to-compensate-for-aging%2F&linkname=Do%20women%20lighten%20their%20hair%20to%20compensate%20for%20aging%3F "Email")[](https://www.addtoany.com/share)
