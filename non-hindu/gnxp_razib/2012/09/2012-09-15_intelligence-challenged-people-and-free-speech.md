+++
title = "Intelligence challenged"
full_title = "Intelligence challenged people and free speech"
date = "2012-09-15"
upstream_url = "https://www.gnxp.com/WordPress/2012/09/15/intelligence-challenged-people-and-free-speech/"

+++
Source: [here](https://www.gnxp.com/WordPress/2012/09/15/intelligence-challenged-people-and-free-speech/).

Intelligence challenged people and free speech



In the [post below](http://blogs.discovermagazine.com/gnxp/2012/09/who-tolerates-anti-american-preaching-from-muslims/) I took the time out to link to the [GSS](http://sda.berkeley.edu/cgi-bin/hsda?harcsda+gss10), **as well as posting my exact queries.** As payment for this consideration the first comment was [absolute drivel](http://blogs.discovermagazine.com/gnxp/2012/09/who-tolerates-anti-american-preaching-from-muslims/comment-page-1/#comment-161100). I understand people have political opinions, **but I’m not too interested in your opinions.** You may be interested in your *opinions*, but I’d rather have more data. Most people don’t know enough for me to have interest in their opinions (most != all, many readers do have opinions in their specialties which I seek out).

I was trying to make a point that **anger and even violence in reaction to actions which offend are actually comprehensible as the modal human response.** The community reacts to punish those who violate taboos. The taboos may differ, but the response to the action of violation is normal and natural. A primary issue that needs to be considered is that taboos differ from society to society, so one is often not conscious of the act of violation (e.g., if you show the bottom of your shoes to people when you sit down, that’s an offensive act in some societies).

An implication here is that American norms of free speech near absolutism, enforced through the fiat of the courts because of their interpretation of the applicability of the Bill of Rights, are radically non-intuitive to most people. The only reason that they are intuitive to many Americans is that we are acculturated over time. This is clear when you look at differences of intelligence and education. In short, **less intelligent and educated Americans are much more skeptical of allowing social deviants to speak.** This is true even in cases where they are more likely to agree with the deviant in question (e.g., these groups have a more pro-military bent, and yet are more accepting of the concept of censure of pro-military opinions).

I have limited all the results to the year 2000 and later. Additionally, I classify those who score 0-4 on the WORDSUM vocab test as stupid, those who score 5-8 as average, and those who score 9-10 as smart. WORDSUM has been [reported to have a 0.7 correlation](http://blogs.discovermagazine.com/gnxp/2010/05/wordsum-iq/) with general intelligence. In this data set 20% of individuals scored 0-4, 69% 5-8, and 12% 9-10.

|                                          |            |             |           |
|------------------------------------------|------------|-------------|-----------|
|                                          | **Stupid** | **Average** | **Smart** |
| Allow racist to speak                    | 52         | 60          | 84        |
| Allow homosexual to speak                | 74         | 86          | 98        |
| Allow militarist to speak                | 51         | 67          | 93        |
| Allow communist to speak                 | 51         | 68          | 95        |
| Allow atheist to speak                   | 64         | 79          | 97        |
| Allow Muslim to preach hatred of America | 25         | 41          | 74        |

I wanted to repeat the logistic regression I did earlier, this time with more variables. If you care, they are: SPKRAC, SPKHOMO, SPKMIL, SPKCOM, SPKATH

|                          |           |      |        |      |        |      |            |      |         |      |
|--------------------------|-----------|------|--------|------|--------|------|------------|------|---------|------|
| **Allow group to speak** |           |      |        |      |        |      |            |      |         |      |
|                          | Communist |      | Racist |      | Homo   |      | Militarist |      | Atheist |      |
|                          | B         | Prob | B      | Prob | B      | Prob | B          | Prob | B       | Prob |
| SEX                      | 0.279     | 0.01 | 0.331  | 0.00 | -0.209 | 0.11 | -0.062     | 0.53 | 0.282   | 0.01 |
| AGE                      | 0.012     | 0.00 | 0.008  | 0.00 | 0.019  | 0.00 | 0.021      | 0.00 | 0.017   | 0.00 |
| SEI                      | -0.004    | 0.18 | -0.003 | 0.29 | -0.009 | 0.05 | -0.013     | 0.00 | -0.011  | 0.00 |
| DEGREE                   | -0.366    | 0.00 | -0.119 | 0.02 | -0.267 | 0.00 | -0.108     | 0.06 | -0.138  | 0.04 |
| WORDSUM                  | -0.229    | 0.00 | -0.139 | 0.00 | -0.276 | 0.00 | -0.204     | 0.00 | -0.228  | 0.00 |
| RACE(Recoded)            | 0.068     | 0.58 | 0.021  | 0.86 | -0.096 | 0.54 | 0.29       | 0.02 | 0.078   | 0.55 |
| HISPANIC(Recoded)        | 0.419     | 0.01 | 0.876  | 0.00 | 0.173  | 0.36 | 0.49       | 0.00 | 0.463   | 0.00 |
| GOD                      | 0.194     | 0.00 | 0.176  | 0.00 | 0.233  | 0.00 | 0.149      | 0.00 | 0.228   | 0.00 |
| POLVIEWS                 | 0.025     | 0.50 | 0.07   | 0.04 | 0.227  | 0.00 | 0.079      | 0.03 | 0.103   | 0.01 |

Most of you may not know the GSS codes for variables, but I do, so I will tell you what the above means. For sex 1 = male and 2 = female. And 1 = allow speech, and 2 = disallow. Therefore, you see that women are more skeptical of free speech for communists, racists, and atheists. Additionally, this skepticism is statistically significant. In contrast, they more supportive of free speech for homosexuals and militarists than men. These results are on the border of significance, but in general women support gay rights more robustly than men, so I think we can accept that.

For age the values are straightforward. Older people have higher values. There isn’t a strong trend. Similarly with socieconomic index. The magnitudes for the beta are not high because intelligence and education probably is what is really driving the socioeconomic differences. And as you can see in every case people with more education or a higher intelligence are more supportive of free speech. **These are the people who run American society**. I’m intrigued that when accounting for background variables non-whites don’t seem particularly supportive of restraints on the speech of racists. In contrast, Hispanics seem definitely much more skeptical of free speech. Finally, being more religious and more conservative also tends to result in more support for censorship. Note that this is the case even in the situation where the very religious and conservative are more likely to support the outlined deviant position, militarism.

On a deep philosophical level what this is asking is whether the community has the right to restrain the speech of individuals. Historically, and to a great extent internationally, the answer is yes. Particular universal ideals of individual liberty which have expanded in scope since the 18th century have started to challenge this assumption, but even within Western societies there are substantial minorities who hew with the older ways.

### Related Posts:

- [More GSS, less
  speculation!](https://www.gnxp.com/WordPress/2012/08/20/more-gss-less-speculation/) - [Ross Douthat talks
  porn](https://www.gnxp.com/WordPress/2008/09/17/ross-douthat-talks-porn/) - [What do you think about group
  selection?](https://www.gnxp.com/WordPress/2012/04/08/what-do-you-think-about-group-selection/) - [Is Free Speech part of the White Power
  Structure?](https://www.gnxp.com/WordPress/2009/03/13/is-free-speech-part-of-the-white-power-structure/) - [Open Thread,
  1/11/2015](https://www.gnxp.com/WordPress/2015/01/11/open-thread-1112015/) - [The Telegraph poll of British
  Muslims](https://www.gnxp.com/WordPress/2005/07/22/the-telegraph-poll-of-british-muslims/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F09%2F15%2Fintelligence-challenged-people-and-free-speech%2F&linkname=Intelligence%20challenged%20people%20and%20free%20speech "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F09%2F15%2Fintelligence-challenged-people-and-free-speech%2F&linkname=Intelligence%20challenged%20people%20and%20free%20speech "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F09%2F15%2Fintelligence-challenged-people-and-free-speech%2F&linkname=Intelligence%20challenged%20people%20and%20free%20speech "Email")[](https://www.addtoany.com/share)
