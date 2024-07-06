+++
title = "Who tolerates"
full_title = "Who tolerates antiAmerican preaching from Muslims?"
date = "2012-09-15"
upstream_url = "https://www.gnxp.com/WordPress/2012/09/15/who-tolerates-anti-american-preaching-from-muslims/"

+++
Source: [here](https://www.gnxp.com/WordPress/2012/09/15/who-tolerates-anti-american-preaching-from-muslims/).

Who tolerates anti-American preaching from Muslims?

Obviously the news over the past week has been filled with the events in the Middle East, and the broader Muslim world, in reaction to an anti-Muslim film. I think the most eloquent commentary is from *The Onion* (**NSFW!!!**), [No One Murdered Because Of This Image](https://www.theonion.com/articles/no-one-murdered-because-of-this-image,29553/). That being said, there are some serious broader issues here. A friend of mine who lives in India (he is Indian American, though raised for several years in India, so not totally unfamiliar with the culture) has expressed to me his frustration with having to defend American liberalism in a society where American liberalism is an abstraction, rather than concrete. The frustration has to do with the **fundamental divergence in *basic values*.** For example, his interlocutors have argued to him (he is a practicing Christian of libertarian political orientation) that if someone committed an act of blasphemy against his faith *of course* he would react in anger **and** violence. And yet of course the clause “and” is false, though he is greeted with skepticism when he asserts he wouldn’t react violently. As a matter of fact I can attest to the reality that he wouldn’t react angrily necessarily, because in interactions where I’ve made casually blasphemous comments he’s only rolled his eyes. Just as Americans have a vague, even misleading, understanding of the broader historical forces which engender resentment of American hegemony in the broader world, so many non-Americans lack a proper awareness of the broader historical forces, and cultural reality, of the particular American radicalism and extremism in the domain of free expression.

I say radicalism and extremism because that is exactly what free speech near absolutism is. Over the course of human history blasphemy has been understood to be unacceptable in most human societies, and often entails extreme sanction. The American, and to a lesser extent Western, elevation of liberty of speech over the sacred values of the community is a peculiar counter-cultural trend which has become normative. But that doesn’t mean that it’s normal or natural. I stipulate here the term “sacred values of the community,” because though blasphemy connotes violations of religious norms, obviously outrage can be triggered by violations of sacred communal norms more generally. Imagine, for example, if someone violated Lenin’s Tomb during the 1950s in the Soviet Union. [Jonathan Haidt](https://en.wikipedia.org/wiki/Jonathan_Haidt) has alluded to this issue. Someone who reacts calmly to [“Piss Christ”](https://en.wikipedia.org/wiki/Piss_Christ)might not react so calmly to “Piss Martin Luther King.”

This points to the second issue. Not only is there is a human universal of offense at violation of sacred norms, **but those sacred norms vary from culture to culture**. So, for example, I have pointed out to followers of the Abrahamic religions that the core documents of their own faiths and the dominant interpretations are often gravely offensive and hostile toward those of other religious traditions. There is a certain [incommensurability](https://en.wikipedia.org/wiki/Commensurability_(philosophy_of_science)) of offense across cultures. What may be sacred to one culture may be offensive and blasphemous to another. To give an example, the institutions of sacred prostitution has cropped up repeatedly over human history. Many religious people would consider prostitution in the service of gods or God blasphemous, whereas others might consider it an exalted act. Similarly, blood sacrifice, whether of humans or animals, has been central to many religions, and taboo and blasphemy in the context of others. In contrast to this there are acts and violations which seem relatively universal in interpretation. This is clear when offended people make analogies to insulting one’s mother; this is generally communicable across societies, because emotional family ties are fundamental. And the collective paroxysms of rage, anger, and violence, due to violations of communal honor probably draw from the same cognitive reflexes as those which are triggered by violations of family honor.

But let’s put the shoe on the other foot here. Would Americans tolerate anti-American preaching from Muslim clerics in this country? We can explore this with the [General Social Survey](http://sda.berkeley.edu/cgi-bin/hsda?harcsda+gss10) with the SPKMSLM variable. It asks:

> Now consider a Muslim clergyman who preaches hatred of the United States. >
> If such a person wanted to make a speech in your community preaching hatred of the United States, should he be allowed to speak, or not?

The question was asked in 2008 and 2010. Since the sample sizes are large I’ll limit to non-Hispanic whites first.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/webpreview_htm_7f8a03fb.jpg?resize=564%2C714)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/webpreview_htm_7f8a03fb.jpg?resize=564%2C714)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/webpreview_htm_7f8a03fb.jpg)

Now in tabular format.

|                                        |                                                   |
|----------------------------------------|---------------------------------------------------|
| ***Non-Hispanic whites, 2008 & 2010*** |                                                   |
| **Demographic**                        | **Allow Muslim clergymen to preach hatred of US** |
| Male                                   | 52.6                                              |
| Female                                 | 39.7                                              |
| \< HS                                  | 19                                                |
| High School                            | 38.2                                              |
| Junior College                         | 45.3                                              |
| Bachelor                               | 62.5                                              |
| Graduate                               | 71.6                                              |
| Stupid                                 | 28                                                |
| Average                                | 43.7                                              |
| Smart                                  | 73.6                                              |
| Liberal                                | 59.9                                              |
| Moderate                               | 40.6                                              |
| Conservative                           | 43.6                                              |
| 18-34 years old                        | 49.3                                              |
| 35-64 years old                        | 48.5                                              |
| 65-\* years old                        | 33.4                                              |
| Protestant                             | 40.7                                              |
| Catholic                               | 43.6                                              |
| Jewish                                 | 45.7                                              |
| No religion                            | 61.1                                              |
| Word of God                            | 26.6                                              |
| Inspired Word of God                   | 48                                                |
| Book of Fables                         | 66.1                                              |

The exact row variables in the GSS:

SEX DEGREE WORDSUM(r:0-4″Stupid”;5-8″Average”;9-10″Smart”) POLVIEWS(r:1-3″Liberal”;4″Moderate”;5-7″Conservative”) AGE(r:18-34;35-64;65-\*) RELIG BIBLE

I then decided to run a [logistic regression](https://en.wikipedia.org/wiki/Logistic_regression). I wanted to see which variables predict attitudes toward speech on this issue. I expanded the data set to include Hispanics and non-whites.

Below **positive values in the “B” column include opposition to allowing a Muslim cleric preach.** Therefore, a negative value favors freedom of speech in this case.

[TABLE]

What’s striking to me is that once you account for education and intelligence, income and socioeconomic status don’t matter. That makes sense since the former are related causally to the latter. The sex difference here is pretty robust. Once you account for other variables race is not so important, but Hispanic identity is. I would suggest here that assimilation to American values is the determining factor, but nativity (BORN variable) doesn’t seem to matter when I checked. It is not surprising to me that political ideology (very liberal to very conservative) doesn’t matter when you account for other variables, especially religion. Well educated conservatives who are not religious tend toward social libertarianism. So once you account for religion and education, ideology isn’t as predictive, similar to race.

There are other similar variables in related to free speech. One pattern is clear. American cultural elites are particularly protective of free speech, while the lower orders tend to have attitudes which are more “relaxed,” and would be more in keeping with other parts of the world. Why? One can imagine many reasons, but this republic was founded by prominent and powerful men who were traitors, and who valued their own personal individual liberty. This is not an uncommon tendency; liberty of thought has been one of the privileges of aristocracy throughout human history. One aspect of ancient Greek democratic populism which rankled aristocrats was that the community might censor and restrain the freedoms of those who traditionally had more license to violate communal norms.

### Related Posts:

- [FAQ](https://www.gnxp.com/WordPress/faq/)
- [The God Delusion in The
  Economist](https://www.gnxp.com/WordPress/2006/10/08/the-god-delusion-in-the-economist/) - [The vast majority of Muslims believe that being gay is
  not…](https://www.gnxp.com/WordPress/2017/04/02/the-vast-majority-of-muslims-believe-that-being-gay-is-not-morally-acceptable/) - [Numbers,
  numbers](https://www.gnxp.com/WordPress/2007/03/17/numbers-numbers/) - [No
  compulsion?](https://www.gnxp.com/WordPress/2006/08/29/no-compulsion/) - [Decade in race, all brown people are the
  same](https://www.gnxp.com/WordPress/2009/12/31/decade-in-race-all-brown-people-are-the-same/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F09%2F15%2Fwho-tolerates-anti-american-preaching-from-muslims%2F&linkname=Who%20tolerates%20anti-American%20preaching%20from%20Muslims%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F09%2F15%2Fwho-tolerates-anti-american-preaching-from-muslims%2F&linkname=Who%20tolerates%20anti-American%20preaching%20from%20Muslims%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F09%2F15%2Fwho-tolerates-anti-american-preaching-from-muslims%2F&linkname=Who%20tolerates%20anti-American%20preaching%20from%20Muslims%3F "Email")[](https://www.addtoany.com/share)
