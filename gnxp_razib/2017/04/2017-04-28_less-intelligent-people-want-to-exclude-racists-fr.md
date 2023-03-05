+++
title = "Less intelligent people"
full_title = "Less intelligent people want to exclude racists from the public square"
date = "2017-04-28"
upstream_url = "https://www.gnxp.com/WordPress/2017/04/28/less-intelligent-people-want-to-exclude-racists-from-the-public-square/"

+++
Source: [here](https://www.gnxp.com/WordPress/2017/04/28/less-intelligent-people-want-to-exclude-racists-from-the-public-square/).

Less intelligent people want to exclude racists from the public square

|                    |            |             |                   | |--------------------|------------|-------------|-------------------| | ***Coefficients*** |            |             | ******           | | ******            | ***B***    | ***SE(B)*** | ***Probability*** | | **SEX**            | **0.739**  | **0.217**   | **0.001**         | | **DEGREE**         | **-0.302** | **0.092**   | **0.001**         | | **WORDSUM**        | **-0.338** | **0.068**   | **0**             | | POLVIEWS           | -0.078     | 0.078       | 0.317             | | INCOME             | -0.026     | 0.06        | 0.671             | | AGE                | 0.007      | 0.007       | 0.283             | | **ATTEND**         | **0.09**   | **0.046**   | **0.05**          | | GOD                | -0.018     | 0.077       | 0.819             | | Constant           | 3.341      | 0.937       | 0                 |

![](https://i0.wp.com/gnxp.com/WordPress/wp-content/uploads/2017/04/41mS3TGKdXL._SX280_BO1204203200_.jpg?resize=282%2C498)![](https://i0.wp.com/gnxp.com/WordPress/wp-content/uploads/2017/04/41mS3TGKdXL._SX280_BO1204203200_.jpg?resize=282%2C498)It’s been a while since I’ve done much [GSS](http://sda.berkeley.edu/sdaweb/analysis/?dataset=gss14) blogging. Part of it is that I’ve got only so much attention I can devote to things, and most of my focus has been on the area of science that I’m interested in, and one or two non-scientific topics. The second variable is that I started blogging about GSS data a long time ago (\~2008), and there’s only so much interesting stuff you can talk about.

But over the past few years there have been some controversies related to speech in public spaces, and what is and isn’t acceptable. There has also been some chatter that young people today in particular are intolerant of freedom of speech. I’ve wanted to address this, so here I go.

The toleration of racists is in today’s America is like testing a boundary condition. **If you are willing to tolerate racist speech if you are not a racist, then you are pretty likely to be a free speech absolutist**. I am not interested in rehashing arguments, I support free speech in an absolutist sense personally. Rather, let’s look at some data.

The General Social Survey has a question up from 2014 for the variable **RACEMEET** that asks:

> Should people prejudiced against any racial or ethnic group be allowed > to hold public meetings?

The question was asked in 2010 and 2014, and 2,651 individuals answered this. The answer was converted to ordinal, so I decided to probe relationships between variables and the score of toleration through regression. Some independent variables, such as political viewpoint (POLVIEWS), were recoded in an ordinal fashion (so that “extremely liberal” = 1, “liberal” = 2, and so forth, to “extremely conservative” = 7). Others, such as age, do not require any recoding. RACEMEET itself was converted to an ordinal.

The above results suggest that political ideology does not predict your response to this question much once you account for other variables. In fact, I did a query on ideological views first, and the results indicated to me what was really going on.

|                                     |           |      |               |              |                  |          |               | |-------------------------------------|-----------|------|---------------|--------------|------------------|----------|---------------| |                                    | EXT. LIB. | LIB. | SLIGHTLY LIB. | **MODERATE** | SLGHTLY CONSERV. | CONSERV. | EXT. CONSERV. | | 1: Should definitely be allowed     | 39        | 24   | 17            | **15**       | 22               | 17       | 20            | | 2: Should probably be allowed       | 12        | 24   | 24            | **21**       | 22               | 22       | 15            | | 3: Should probably not be allowed   | 26        | 20   | 19            | **22**       | 19               | 24       | 22            | | 4: Should definitely not be allowed | 23        | 32   | 40            | **43**       | 37               | 38       | 43            |

As you can see **moderates are relatively skeptical of allowing racists to have a public meeting.** All of my analysis of the GSS indicates that [moderates are not as smart as more liberal or conservative](http://blogs.discovermagazine.com/gnxp/2012/10/political-moderates-and-independents-are-not-as-smart-on-average/) people.

Let’s go through the variables which were significant predictors above. First, sex.

|                                     |      |        | |-------------------------------------|------|--------| |                                     | Male | Female | | 1: Should definitely be allowed     | 21   | 13     | | 2: Should probably be allowed       | 22   | 21     | | 3: Should probably not be allowed   | 20   | 23     | | 4: Should definitely not be allowed | 36   | 43     |

These results were expected. On the whole women tend to be more skeptical of absolutist free speech positions which allow offensive material to be promoted (women are more skeptical of allowing Communists to speak too in comparison to men, so it’s not because of the ideology of the speaker or viewpoint).

Then church attendance frequency:

|                                     |                      |     |     |     |     |                       |     |     |     | |-------------------------------------|----------------------|-----|-----|-----|-----|-----------------------|-----|-----|-----| |                                     | Never attends church |     |     |     |     | More than once a week |     |     |     | | 1: Should definitely be allowed     | 20                   | 23  | 19  | 14  | 21  | 15                    | 13  | 14  | 13  | | 2: Should probably be allowed       | 21                   | 21  | 27  | 24  | 13  | 16                    | 26  | 22  | 20  | | 3: Should probably not be allowed   | 21                   | 17  | 20  | 18  | 28  | 24                    | 18  | 24  | 23  | | 4: Should definitely not be allowed | 37                   | 39  | 34  | 44  | 37  | 45                    | 43  | 40  | 44  |

A modest difference.

Next, highest educational attainment:

|                                     |       |     |              |         |          | |-------------------------------------|-------|-----|--------------|---------|----------| |                                     | No HS | HS  | Some college | College | Graduate | | 1: Should definitely be allowed     | 7     | 14  | 11           | 26      | 32       | | 2: Should probably be allowed       | 14    | 20  | 23           | 29      | 27       | | 3: Should probably not be allowed   | 20    | 23  | 21           | 19      | 20       | | 4: Should definitely not be allowed | 59    | 43  | 45           | 26      | 21       |

The big gap here is between those with college and those without college educations.

Finally, we look at WORDSUM, [which is a proxy for intelligence](http://blogs.discovermagazine.com/gnxp/2010/05/wordsum-iq/#.WQQqW1PyvBI). It’s a tenword vocabulary test. Below in the columns are the number of answers a respondent got correct:

|                                     |     |     |     |     |     |     |     | |-------------------------------------|-----|-----|-----|-----|-----|-----|-----| |                                     | \<5 | 5   | 6   | 7   | 8   | 9   | 10  | | 1: Should definitely be allowed     | 8   | 10  | 12  | 16  | 24  | 30  | 36  | | 2: Should probably be allowed       | 13  | 22  | 18  | 24  | 26  | 34  | 33  | | 3: Should probably not be allowed   | 27  | 20  | 23  | 22  | 21  | 18  | 18  | | 4: Should definitely not be allowed | 52  | 48  | 47  | 38  | 29  | 18  | 12  |

I combined those who scored below 5 out of 10 (0-4) into one class. **You can see that as score on this vocabulary test goes up, the viewthat racists should be allowed to meet in public goes up**. It’s almost monotonic. The smartest people are more tolerant than the next smartest people who are more tolerant than the next smartest people, with the dumb being the least tolerant.

I made the below chart to illustrate this:

![](https://i0.wp.com/gnxp.com/WordPress/wp-content/uploads/2017/04/racists_allowed_to_meet.png?resize=640%2C587)![](https://i0.wp.com/gnxp.com/WordPress/wp-content/uploads/2017/04/racists_allowed_to_meet.png?resize=640%2C587)

Often when it comes to views associated with “smart” people when you put it into some regression eduction accounts for all of the difference. In other words, the less intelligent educated have the same views as the intelligent educated, and the more intelligent but less educated have the same views as the less intelligent less educated. There are more older people who are intelligent but not educated, so it could be generational too (though in this case age does not seem to matter). A plausible hypothesis is that in many cases it is social milieu. Even if you are not bright, being in college inculcates certain values.

And college is a predictor. **But these data show that even if you account for college education the brighter you are, the more likely you favor allowing tolerance for views that most people find intolerable**.

### Related Posts:

- [Data access to the
  GSS](https://www.gnxp.com/WordPress/2006/09/26/data-access-to-the-gss/) - [Turks: Greek or
  Armenian?](https://www.gnxp.com/WordPress/2021/08/24/turks-greek-or-armenian/) - [Most people understand independence
  (probability)](https://www.gnxp.com/WordPress/2009/03/22/most-people-understand-independence-probability/) - [WORDSUM & IQ & the
  correlation](https://www.gnxp.com/WordPress/2010/05/04/wordsum-iq/) - [GSS
  blogging](https://www.gnxp.com/WordPress/2008/12/09/gss-blogging/) - [Men trust people more than women
  do](https://www.gnxp.com/WordPress/2011/05/09/men-trust-people-more-than-women/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F04%2F28%2Fless-intelligent-people-want-to-exclude-racists-from-the-public-square%2F&linkname=Less%20intelligent%20people%20want%20to%20exclude%20racists%20from%20the%20public%20square "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F04%2F28%2Fless-intelligent-people-want-to-exclude-racists-from-the-public-square%2F&linkname=Less%20intelligent%20people%20want%20to%20exclude%20racists%20from%20the%20public%20square "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F04%2F28%2Fless-intelligent-people-want-to-exclude-racists-from-the-public-square%2F&linkname=Less%20intelligent%20people%20want%20to%20exclude%20racists%20from%20the%20public%20square "Email")[](https://www.addtoany.com/share)
