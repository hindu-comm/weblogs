+++
title = "Birth Months of World"
full_title = "Birth Months of World Cup Players"
date = "2010-07-09"
upstream_url = "https://www.gnxp.com/WordPress/2010/07/09/birth-months-of-world-cup-players/"

+++
Source: [here](https://www.gnxp.com/WordPress/2010/07/09/birth-months-of-world-cup-players/).

Birth Months of World Cup Players

Four years ago I (and [others](https://isteve.blogspot.com/2006/05/levitt-maybe-world-cup-wasnt-best.html)) [got in a dispute](http://freakonomics.blogs.nytimes.com/2006/05/11/maybe-the-world-cup-wasnt-the-best-example/) with Stephen Dubner and Steven Levitt (DL) about [their claim](http://www.nytimes.com/2006/05/07/magazine/07wwln_freak.html) that birth month had a meaningful impact on later success in professional sports because kids born in January were “old” for their age group and were, therefore, more likely to make elite travel, national teams for U-17 tournaments and the like. These athletes benefited from the better coaching and competition that they faced relative to the kids who were born later in the same calendar year but with the same natural ability. DL predicted that

> If you were to examine the birth certificates of every soccer player > in next month’s \[2006\] World Cup tournament, you would most likely > find a noteworthy quirk: elite soccer players are more likely to have > been born in the earlier months of the year than in the later months.

  
But this turned out [not to be true](http://freakonomics.blogs.nytimes.com/2006/06/13/are-stars-born-or-made-heres-what-world-cup-2006-has-to-say-on-the-issue/?scp=2-b&sq=freakonomics+world+cup+birth+month&st=nyt#comment-15023). Yet the worst part was that Levitt, through some peculiar post-hoc reasoning, [tried to claim](http://freakonomics.blogs.nytimes.com/2006/06/13/are-stars-born-or-made-heres-what-world-cup-2006-has-to-say-on-the-issue/) that it was, in fact, true, that birth month mattered.

The larger debate here goes back to nature-versus-nurture. DL (and/or their readers) and [Malcolm Gladwell](http://sports.espn.go.com/espn/page2/story?page=merron/081208) (and/or his readers) want to believe that stars are made not born. Spend enough on your kids coaching and he too can play in the World Cup or the NHL! The GNXP perspective would probably be that, while training obviously matters, the more incentives there are for high performance and the more open/democratic the pipeline, the more that genetics matter.

Luge stars are made but not born because so few kids have access to a luge track. Soccer stars are born but not made because millions of children around the world have extensive exposure to soccer. If they have the genetics to star, the system will find them and cultivate their talents. Without the genetics, they have no chance. The more equal the opportunities, the more that genetics matter. This is not the story that your typical American soccer parent wants to read about in the *New York Times* or *The New Yorker*.

But enough random speculation! Let’s look at the data ([text file](https://www.gnxp.com/wp/wp-content/uploads/2010/07/players.txt) hand-collected by me from the [FIFA site](http://www.fifa.com/worldcup/teams/index.html)) for the current World Cup. I will add some code later in the comments, but here is the key chart.

[![](https://i0.wp.com/www.gnxp.com/wp/wp-content/uploads/2010/07/Rplot001.jpg?resize=480%2C480 "Rplot001")![](https://i0.wp.com/www.gnxp.com/wp/wp-content/uploads/2010/07/Rplot001.jpg?resize=480%2C480 "Rplot001")](https://i0.wp.com/www.gnxp.com/wp/wp-content/uploads/2010/07/Rplot001.jpg)

If you squint, you can try to claim that players are less likely to be born later in the year than earlier. But a chi-square test of randomness gives a p-value of 16% and a binomial test of the 72 players born in January versus the expected value of about 61 (given a total player population of 736) yields a p-value of 10%. In other words, there is no/little evidence that birth month matters to your chances of playing in the World Cup.

And, to the extent that you think it does (and looking at the first three months of the year does pop up as statistically significant), the much more likely explanation (exercise left for the reader) is not age cut-offs in wealthy countries with extensive junior soccer programs but birth date fraud in poor countries seeking an advantage in international U-17 and U-20 competitions.

### Related Posts:

- [Sunshine and SEC
  Football](https://www.gnxp.com/WordPress/2009/11/02/sunshine-and-sec-football/) - [This is reproductive
  fitness!](https://www.gnxp.com/WordPress/2009/03/11/this-is-reproductive-fitness/) - [Why Dukies underachieve as
  pros](https://www.gnxp.com/WordPress/2010/04/02/why-dukies-underachieve-at-the-pros/) - [SI on the White
  Athlete](https://www.gnxp.com/WordPress/2010/02/23/si-on-the-white-athlete/) - [Version 2.0 of Montana &
  Gretzky](https://www.gnxp.com/WordPress/2009/10/14/version-2-0-of-montana-gretzky/) - [Individual differences don't
  lie](https://www.gnxp.com/WordPress/2011/10/16/individual-differences-dont-lie/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F07%2F09%2Fbirth-months-of-world-cup-players%2F&linkname=Birth%20Months%20of%20World%20Cup%20Players "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F07%2F09%2Fbirth-months-of-world-cup-players%2F&linkname=Birth%20Months%20of%20World%20Cup%20Players "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F07%2F09%2Fbirth-months-of-world-cup-players%2F&linkname=Birth%20Months%20of%20World%20Cup%20Players "Email")[](https://www.addtoany.com/share)
