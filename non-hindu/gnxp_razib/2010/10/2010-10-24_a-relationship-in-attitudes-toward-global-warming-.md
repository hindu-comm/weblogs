+++
title = "A relationship in"
full_title = "A relationship in attitudes toward Global Warming & evolution?"
date = "2010-10-24"
upstream_url = "https://www.gnxp.com/WordPress/2010/10/24/a-relationship-in-attitudes-toward-global-warming-evolution/"

+++
Source: [here](https://www.gnxp.com/WordPress/2010/10/24/a-relationship-in-attitudes-toward-global-warming-evolution/).

A relationship in attitudes toward Global Warming & evolution?

In my [post earlier in the week](http://blogs.discovermagazine.com/gnxp/2010/10/glenn-beck-evolution-global-warming-tea-parties/) I mentioned the possible relationship between attitudes toward evolution and the causes and likelihood of Global Warming. I haven’t seen any survey data myself relating the two, so naturally I wanted to poke into the [General Social Survey](http://sda.berkeley.edu/cgi-bin/hsda?harcsda+gss08). Two variables of interest showed up, both from 2006:

1\) GWSCI, “Understanding of causes of Global Warming by environmental scientists.” A five-point scale, from understanding “Very well” (1) to “Not at all” (5).

2\) SCIAGRGW, “Extent of agreement among environmental scientists.” A five-point scale, from “Near complete agreement” (1) to “No agreement at all” (5).

I paired these up against EVOLVED, which is a simple True vs. False answer in relation the question as to whether “Human beings developed from animals.”

Tables below.

Each *row* in the following set of tables adds up to 100%. In other words in the first row 55% of Democrats think that environmental scientists understand the cause of global warming “Very well.”

[TABLE]

Now we’ll switch the columns, but again, the rows add up to 100%. So of those who think that environmental scientists understand the cause of global warming “Very well,” 55% accept that humans developed from animals.

|                                                                        |                  |           | |------------------------------------------------------------------------|------------------|-----------| |                                                                        | **Evolution is** |           | |                                                                        | **TRUE**         | **FALSE** | | *Environmental scientists understand cause of global warming*          |                  |           | | Very well                                                              | 55               | 45        | | 2                                                                      | 58               | 42        | | 3                                                                      | 36               | 64        | | 4                                                                      | 28               | 72        | | Not at all                                                             | 38               | 62        | |                                                                        |                  |           | |                                                                        | **Evolution is** |           | |                                                                        | **TRUE**         | **FALSE** | | *Extent of agreement on global warming among environmental scientists* |                  |           | | Near complete agreement                                                | 50               | 48        | | 2                                                                      | 56               | 44        | | 3                                                                      | 46               | 54        | | 4                                                                      | 52               | 48        | | No agreement at all                                                    | 47               | 54        |

Finally, a set of regressions. Since the ones for Global Warming have a 1 to 5 scale I just used a linear regression, while for evolution I used logistic regression (since it’s a dichotomous response).

|                          |        |       | |--------------------------|--------|-------| | **GWSCI**                |        |       | |                          | Beta   | p     | | POLVIEWS                 | 0.158  | 0.01  | | PARTYID                  | 0.087  | 0.144 | | AGE                      | 0.053  | 0.293 | | GOD                      | 0.114  | 0.058 | | BIBLE                    | -0.028 | 0.654 | | WORDSUM                  | -0.082 | 0.152 | | DEGREE                   | -0.021 | 0.748 | | SEI                      | -0.116 | 0.069 | |                          |        |       | | R-squared = 0.118        |        |       | |                          |        |       | |                          |        |       | | **SCIAGRGW**             |        |       | |                          | Beta   | p     | | POLVIEWS                 | 0.085  | 0.185 | | PARTYID                  | 0.062  | 0.325 | | AGE                      | 0.032  | 0.557 | | GOD                      | 0.035  | 0.558 | | BIBLE                    | 0.095  | 0.156 | | WORDSUM                  | 0.031  | 0.609 | | DEGREE                   | -0.103 | 0.132 | | SEI                      | -0.138 | 0.043 | |                          |        |       | | R-squared = 0.053        |        |       | |                          |        |       | | **EVOLVED**              |        |       | |                          | B      | p     | | POLVIEWS                 | 0.158  | 0.003 | | PARTYID                  | 0.075  | 0.03  | | AGE                      | 0.016  | 0     | | GOD                      | 0.549  | 0     | | BIBLE                    | -1.144 | 0     | | WORDSUM                  | -0.03  | 0.402 | | DEGREE                   | -0.091 | 0.174 | | SEI                      | -0.008 | 0.04  | |                          |        |       | | Pseudo R-squared = 0.255 |        |       |

Weird things happen when I try and relate the Global Warming variables to evolution. Since I gave you the names of the variables I invite you to replicate. I see some relationship in the 2006 GSS, but not a strong one. The dependence of attitudes toward evolution on religious views is pretty direct as expected. Not as clear with the Global Warming issues.

### Related Posts:

- [Global Warming: Cool
  It!](https://www.gnxp.com/WordPress/2006/05/27/global-warming-cool-it/) - [In defense of science and its relevance to
  policy](https://www.gnxp.com/WordPress/2009/10/09/in-defense-of-science-and-its-relevance-to-policy/) - [Anti-science mad
  libs](https://www.gnxp.com/WordPress/2007/01/19/anti-science-mad-libs/) - [How to use the General Social
  Survey](https://www.gnxp.com/WordPress/2011/08/06/how-to-use-the-general-social-survey/) - [Friday Fluff - October 22nd,
  2010](https://www.gnxp.com/WordPress/2010/10/22/friday-fluff-october-22nd-2010/) - [Sizzle: not even
  bad?](https://www.gnxp.com/WordPress/2008/07/15/sizzle-not-even-bad/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F10%2F24%2Fa-relationship-in-attitudes-toward-global-warming-evolution%2F&linkname=A%20relationship%20in%20attitudes%20toward%20Global%20Warming%20%26%20evolution%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F10%2F24%2Fa-relationship-in-attitudes-toward-global-warming-evolution%2F&linkname=A%20relationship%20in%20attitudes%20toward%20Global%20Warming%20%26%20evolution%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F10%2F24%2Fa-relationship-in-attitudes-toward-global-warming-evolution%2F&linkname=A%20relationship%20in%20attitudes%20toward%20Global%20Warming%20%26%20evolution%3F "Email")[](https://www.addtoany.com/share)
