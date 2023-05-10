+++
title = "Bygone brunette beauty"
full_title = "Bygone brunette beauty Fashion in hair color"
date = "2008-06-29"
upstream_url = "https://www.gnxp.com/WordPress/2008/06/29/bygone-brunette-beauty-fashion-in-hair-color/"

+++
Source: [here](https://www.gnxp.com/WordPress/2008/06/29/bygone-brunette-beauty-fashion-in-hair-color/).

Bygone brunette beauty: Fashion in hair color

[](https://www.gnxp.com/blog/uploaded_images/February1964-776024.jpg)Long-time readers know that one of my beliefs that I’ll stop at nothing to prove is that blond women are not sexier than brunettes, whatever other appeal they obviously have for many men. Point-estimates of the current popularity of blond hair neglect the fact that standards of beauty can change over time — within boundaries, to be sure, but still. Perhaps we only live in a blond-obsessed world today, while brunettes may have ruled in the past. Indeed, I will show just that. Furthermore, the shift toward blonds parallels several other shifts toward a more masculine ideal of female beauty since the early / mid-1960s.

The data come from Playboy Playmates of the Month (“Playmates”) from 1954 to 2007. We need to look at sources that pander to popular demand in sexual tastes, which excludes runway fashion magazines (not used by males for fantasy purposes) as well as data on high-ranking Hollywood actresses (who are esteemed only in part based on their looks). We also need comparable data that stretch over decades, and that provide us with many data-points for each year — in a worst case scenario, we might look at something like Miss Universe winners, but estimating the value of blond-obsession for a given year with only a single data-point is hardly ideal. Playmates, though, yield 12 data-points per year.

In the name of scientific discovery, I looked at pictures of every Playmate \[1\], and coded her hair color as either 1 for blond or 0 for non-blond. Dark blonds counted as blond, light browns as non-blond. Redheads counted as blond if they had very fair, strawberry blond hair, and as non-blond otherwise. The point is not to measure the popularity of the full spectrum of hair colors — just blondness. A small handful of Playmates had several hair colors within the single issue they appeared in. I coded these as 0.5 because their pictures were split pretty evenly between blond and non-blond hair — maybe due to wigs, I don’t know.

I then took the fraction of blonds in a given year and plotted these over time. Here is the raw scatter-plot, together with 3-year and 7-year moving averages that smooth it out:

[](https://www.gnxp.com/blog/uploaded_images/PercentBlondPlaymates-711491.JPG)

The scatter-plot suggests an increasing trend, and this is true: Kendall’s tau for the correlation between year and percent blond is +0.27 (p = 0.01, two-tailed). \[2\] However, because each year’s value can only take on roughly 12 values (1 / 12, 2 / 12, etc.), there are a lot of tied years, which may underestimate the true correlation. Kendall’s tau for the correlation between year and the 3-year moving average of percent blond is +0.47 (p = 2 x 10^(-6), two-tailed), and is +0.64 (p = 2 x 10^(-10), two-tailed) when the 7-year moving averages are used. Using a moving average gives us a better idea since they can take on far many more values, and so produce fewer ties.

Whichever one we choose, it is clear that blonds have increased quite a bit in popularity over the decades. At the same time, the trend is clearly not linear: there is a decrease in blond-obsession at least from the mid-1950s, when the data begin, to the early / mid-1960s. There follows an increase, and an apparent reversal since the turn of the millennium — please god, let it be so. This looks periodic, like a fashion cycle.

In trying to account for this trend, we should try to be as general as possible. What other trends in female beauty show an increase after the early 1960s? I didn’t look at other aspects of the Playmates, but someone else has tabulated [data on Playmates of the Year from 1960 to 2006](http://www.swivel.com/data_sets/show/1003187) — again, estimating the popularity of some trait in a given year based on a single data-point is worst-case, but I’m relying on it here because I’ve already spent enough time collecting hair color data. The links in footnote 1 provide all the anthropometric data, though, so if you want to collect an analyze it, we will link to your analysis.

I calculated the Waist-to-Hip Ratio and BMI of Playmates of the Year from the above data, and Kendall’s tau for the correlation between year and WHR is +0.53 (p = 4 x 10^(-7), two-tailed), while between year and BMI it is -0.24 (p = 0.02, two-tailed). So, these sex symbols are increasingly losing their feminine hourglass shape and fatty softness — nearly all BMI points are below 20, so it’s not like they used to be fat but are now healthy. They are also getting taller: Kendall’s tau is +0.31 (p = 0.004); and smaller in the chest: Kendall’s tau is -0.35 (p = 0.001).

Someone else has also done [an analysis of Miss America winners](http://www.seductionlabs.org/2008/02/06/87-years-of-beauty/), and the exact same trends emerge there as well (see his graphs).

The common factor of all these trends is that the ideal of female beauty has become increasingly masculinized. Recall that [males are more likely to be blond](https://www.gnxp.com/blog/2007/11/brown-eyed-girl.php), so the hair color trend is part of the larger masculinizing trend. I didn’t look at eye color, but if it’s part of the overall trend, the earlier Playmates should be less blue-eyed than later ones, as blue eyes are also more typical of males. Skin color would be tougher to analyze; if it’s part of the same trend, it should get darker over time. Anecdotally, these two guesses seem to be true, but someone should look at the data to check.

It therefore appears that a preference for blonds should also correlate with a preference for taller and less curvy women. Again, someone else can look that up in the psychology literature and post in the comments. But the words “tall,” “thin,” and “blond” usually co-occur, don’t they? Whatever appeal such women have, raw sex appeal is unlikely to be among the top reasons. Blond hair correlates with something like introversion, and that makes sense since men on average are more introverted than women. So, maybe guys start digging blonds when they become more marriage-minded, or if they are inveterate monogamists. A blond will be less likely to be bouncing off the walls and being constantly out and about in search of social stimulation.

Bang a brunette, bank on a blond? It would fit with the [trend toward lower sluttiness](https://www.gnxp.com/blog/2008/06/your-generation-was-sluttier.php) in recent times, which we expect to weed out the sex kitten types from popular culture. This suggests that dark hair is part of that highly sexualized image — something that was always obvious to everyone but the blond-lovers.

\[1\] For years 1954 to 1992, I used [this source](http://www.thecoincorner.net/playboy/Index1.htm) that contains the full shoot for each Playmate, and for 1993 to 2007, [Playboy’s official website](http://www.playboy.com/girls/playmates/directory/index.html) (if the single picture available on the Playboy site was ambiguous, I did a Google image search to get a better idea).

\[2\] You can easily calculate Kendall’s tau [with this website](http://www.wessa.net/rwasp_kendall.wasp), which I used here.

### Related Posts:

- [Maxim's audience prefers brunettes; distribution
  is…](https://www.gnxp.com/WordPress/2008/07/06/maxim-s-audience-prefers-brunettes-distribution-is-bimodal/) - [Do women lighten their hair to compensate for
  aging?](https://www.gnxp.com/WordPress/2008/12/15/do-women-lighten-their-hair-to-compensate-for-aging/) - [How swarthy are the
  Sami?](https://www.gnxp.com/WordPress/2007/07/10/how-swarthy-are-the-sami/) - [Hair thickness,
  update](https://www.gnxp.com/WordPress/2007/11/06/hair-thickness-update/) - [NLSY blogging: Eye and hair color of
  Americans](https://www.gnxp.com/WordPress/2008/12/13/nlsy-blogging-eye-and-hair-color-of-americans/) - [Golden-haired
  Neandertals?](https://www.gnxp.com/WordPress/2007/11/09/golden-haired-neandertals/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F06%2F29%2Fbygone-brunette-beauty-fashion-in-hair-color%2F&linkname=Bygone%20brunette%20beauty%3A%20Fashion%20in%20hair%20color "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F06%2F29%2Fbygone-brunette-beauty-fashion-in-hair-color%2F&linkname=Bygone%20brunette%20beauty%3A%20Fashion%20in%20hair%20color "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F06%2F29%2Fbygone-brunette-beauty-fashion-in-hair-color%2F&linkname=Bygone%20brunette%20beauty%3A%20Fashion%20in%20hair%20color "Email")[](https://www.addtoany.com/share)
