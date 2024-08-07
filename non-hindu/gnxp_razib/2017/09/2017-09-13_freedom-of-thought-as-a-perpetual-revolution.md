+++
title = "Freedom of thought as a"
full_title = "Freedom of thought as a perpetual revolution"
date = "2017-09-13"
upstream_url = "https://www.gnxp.com/WordPress/2017/09/13/freedom-of-thought-as-a-perpetual-revolution/"

+++
Source: [here](https://www.gnxp.com/WordPress/2017/09/13/freedom-of-thought-as-a-perpetual-revolution/).

Freedom of thought as a perpetual revolution

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/onLiberty.jpeg?resize=182%2C277)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/onLiberty.jpeg?resize=182%2C277)](https://www.amazon.com/exec/obidos/ASIN/B00A735PTG/geneexpressio-20)I mentioned offhand on Twitter today that I am skeptical of the tendency to brand the classically liberal emphasis on freedom of thought and speech as “centrist.” The implicit idea is that those on the Right and Left for whom liberalism is conditional, and a means at best, are radical and outside the mainstream.

**This misleads us in relation to the fact that classical liberalism is the aberration both historically and culturally.** Liberty of thought and speech have existed for time immemorial, but they were the luxury goods of the elite salons. Frederick the Great of Prussia had no use for religion personally, and famously patronized heretical philosophers, but he did not disturb the conservative social order of the polity which he inherited. For the masses, the discourse was delimited and regulated to maintain order and reinforce social norms.

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/system_of_liberty.jpeg?resize=183%2C275)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/system_of_liberty.jpeg?resize=183%2C275)](https://www.amazon.com/exec/obidos/ASIN/0521182093/geneexpressio-20)The attempt to position the liberal stance as a centrist one is clearly historically and culturallycontingent. It reflects the ascendancy of a particular strand of Anglo-American elite culture worldwide. But it is not universal. In the Islamic world and South Asia free expression of skepticism of religious ideas in **public** are subject to limits explicitly to maintain public order. The Islamic punishments for apostasy have less to do with the sin of individual disbelief and more to do with disruption to public norms and sedition against the state. Similarly, both China and Russia tap deeply into cultural preferences for state and elite paternalism in regards to public freedom of thought.

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/therighteousmind.jpeg?resize=150%2C231)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/therighteousmind.jpeg?resize=150%2C231)](https://www.amazon.com/exec/obidos/ASIN/B0052FF7YM/geneexpressio-20)In fact, the classical liberal perspective on prioritizing freedom of conscience and the ability to explore the full range of ideas is probably counter to the “lowest energy state” of human cognitive intuitions. It reflects only a slice of the “moral foundations” which Jonathan Haidt explores in [The Righteous Mind](https://www.amazon.com/exec/obidos/ASIN/B0052FF7YM/geneexpressio-20).

To explore some of the demographic correlates of classical liberalism I utilized the [General Social Survey](http://sda.berkeley.edu/sdaweb/analysis/?dataset=gss16). As instruments to assess liberal attitudes toward free speech and thought I focused on two variables,SPKMSLM and SPKLRAC. For the first variable respondents were asked:

> Now consider a Muslim clergyman who preaches hatred of the United States. If such a person wanted to make a speech in your community preaching hatred of the United States, should he be allowed to speak, or not?

For the second:

> Or consider a person who believes that Blacks are genetically inferior. a. If such a person wanted to make a speech in your community claiming that Blacks are inferior, should he be allowed to speak, or not?

I assess the pro-free speech position by inspecting the **subset who accept that *both* groups should be allowed to speak, and those who reject that *either* group should be allowed to speak.** That is, these are people consistent in their attitudes when it comes to speech which conflicts with community norms.

For demographic variables, I looked at educational attainment (DEGREE), verbal intelligence (WORDSUM), and political ideology (POLVIEWS). For verbal intelligence scoring 0-4 out of 10 was below average, 5-7 was average, and 8-10 above average.

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/offensive_speech1.jpg?resize=625%2C426)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/offensive_speech1.jpg?resize=625%2C426)](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/offensive_speech1.jpg)[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/offensive_speech2.jpg?resize=625%2C404)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/offensive_speech2.jpg?resize=625%2C404)](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/offensive_speech2.jpg)[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/offensive_ideology.jpg?resize=625%2C407)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/offensive_ideology.jpg?resize=625%2C407)](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/offensive_ideology.jpg)

What is clear above is that **those with more education and those who are more intelligent tend to support free speech more than those who lack education or are less intelligent**. But it is also notable that moderates, in particular, are overrepresented among those who reject freedom of speech. ~~Though t~~The proportion of liberals goes up appreciably, the proportion of conservatives also goes up a bit!.

**I ran a quick logistic regression model** which attempts to predict the odds of two outcomes (support or reject free speech here) across a range of variables simultaneously. Statistically significant***B***coefficients are bolded. You can see that the demographics which support speech across the two are consistent:

|              |                      |                      |                               |
|--------------|----------------------|----------------------|-------------------------------|
|              | **B – Allow Muslim** | **B – Allow racist** | **Who supports free speech?** |
| **AGE**      | **0.01**             | **0.006**            | Younger people                |
| **SEI**      | -0.008               | **-0.007**           | Higher SES people             |
| **POLVIEWS** | 0.061                | **0.072**            | Liberals                      |
| **WORDSUM**  | **-0.306**           | **-0.145**           | Smart people                  |
| **DEGREE**   | **-0.274**           | **-0.153**           | More education                |
| **INCOME**   | -0.026               | -0.026               | Richer                        |
| **SEX**      | **0.45**             | **0.24**             | Men                           |
| **GOD**      | **0.151**            | **0.159**            | Less religious                |

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/theEnlightenedEconomy.jpeg?resize=184%2C275)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/theEnlightenedEconomy.jpeg?resize=184%2C275)](https://www.amazon.com/exec/obidos/ASIN/0300189516/geneexpressio-20)From looking at the GSS data moderates are the less interested in politics overall, and also less educated and intelligent. **In general, when they respond to a political issue they’re going with their gut**. Humans are social animals and tend to not look favorably upon public disruption. The rationales for why one should discourage offensive and taboo speech are rather coherent. The liberal instrumental argument for freedom of thought as a social good tends to take a longer view that the proliferation of ideas will lead to greater prosperity and moral advancement.

This is a very [Whig](https://en.wikipedia.org/wiki/Whig_history) model of history. Whether the model is correct or not, it captures a particular moment in the Zeitgeist of the early modern West. The reason that *classical* liberalism is classical is that it in minimal terms it has never gone beyond its roots in the late 18th and early 19th century in relation to its preoccupations. Within the West many conservatives and reactionaries have argued against the presuppositions of classical liberal thought, which have tacitly been ascendant for the past two centuries (the fascists being the inchoate apotheosis of these reactive strands). Marxists and other radicals have gone*beyond*the liberal fixation on liberty narrowly defined, while modern Left-liberals tend to put as much emphasis on economic liberty through redistribution as upon civil liberty.

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/watsonideas.jpeg?resize=200%2C252)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/watsonideas.jpeg?resize=200%2C252)](https://www.amazon.com/exec/obidos/ASIN/B000FCKC5G/geneexpressio-20)But I also want to suggest here that perhaps the classical liberal fixation on freedom of thought reflects the interests and preoccupations of a particular segment of society: **those for whom ideas are fascinating and give sustenance and meaning to life**. The Enlightenment can be thought of as the revolt of the middle class, broadly construed, from the mercantile high bourgeoisie down to the broad professional class. These are people for whom “post-materialist” considerations loom large because material considerations have faded into the background. For the poor and those in material want freedom of thought is less important by necessity. Similarly, the large segment of the population which is not interested in novel ideas may not care much about the importance of intellectual novelty. Finally, there are those with post-materialist values which may emphasize the importance of taboos and social conformity of the collective.

Though the majority of the population (at least in the West) seems inclined to go along with liberalism as part of the broader suite of post-Enlightenment Western culture, there is no guarantee that they will always hew to such a position. Classical liberalism understood to be fundamentally radical would be useful insofar as the elites for whom it is an ends, and not a means, **would be less complacent and more motivated toward maintaining the primacy of the values which give meaning to their lives**.

### Related Posts:

- [Off to the
  catacombs?](https://www.gnxp.com/WordPress/2005/01/22/off-to-the-catacombs-2/) - [Free speech not as important in Eastern
  Europe](https://www.gnxp.com/WordPress/2009/05/06/free-speech-not-as-important-in-eastern-europe/) - [Liberals and the intelligent stand by free
  speech](https://www.gnxp.com/WordPress/2015/05/05/liberals-and-the-intelligent-stand-by-free-speech/) - [Open Thread,
  1/11/2015](https://www.gnxp.com/WordPress/2015/01/11/open-thread-1112015/) - [Off to the
  catacombs?](https://www.gnxp.com/WordPress/2005/01/22/off-to-the-catacombs/) - [Clash of
  freedoms](https://www.gnxp.com/WordPress/2006/04/18/clash-of-freedoms/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F09%2F13%2Ffreedom-of-thought-as-a-perpetual-revolution%2F&linkname=Freedom%20of%20thought%20as%20a%20perpetual%20revolution "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F09%2F13%2Ffreedom-of-thought-as-a-perpetual-revolution%2F&linkname=Freedom%20of%20thought%20as%20a%20perpetual%20revolution "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F09%2F13%2Ffreedom-of-thought-as-a-perpetual-revolution%2F&linkname=Freedom%20of%20thought%20as%20a%20perpetual%20revolution "Email")[](https://www.addtoany.com/share)
