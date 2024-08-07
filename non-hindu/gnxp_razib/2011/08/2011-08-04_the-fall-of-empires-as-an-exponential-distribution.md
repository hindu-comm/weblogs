+++
title = "The fall of empires as"
full_title = "The fall of empires as an exponential distribution"
date = "2011-08-04"
upstream_url = "https://www.gnxp.com/WordPress/2011/08/04/the-fall-of-empires-as-an-exponential-distribution/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/08/04/the-fall-of-empires-as-an-exponential-distribution/).

The fall of empires as an exponential distribution

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/expo.png?resize=296%2C268)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/expo.png?resize=296%2C268)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/expo.png)I was alerted to Samuel’s Arbesman’s new paper, [The Life-Spans of Empires](https://dx.doi.org/10.1080/01615440.2011.577733), by the fact that he pointed to his research [on his weblog](http://arbesman.net/blog/2011/08/02/the-life-spans-of-empires/). Interestingly I’m not the only one who was interested, as after I pointed to it on my link round up a few people asked if they could get a copy of the paper (yes, I almost always send papers if I have access). Luckily it’s a nicely elegant piece of work, basically quantifying what we’ve already probably known qualitatively. There isn’t that great of a value-add to quantification as such, **but with a mathematical understanding of a topic one can engage in an algebra of mental manipulations so as to construct models with which one can project other facts.** Quantitative information is often an excellent way to generate “free information” from theoretical models. The figure above is the primary result of the paper. Basically Arbesman took a data set which was laying around which measured the lengths of various empires (N = 41), and showed that the rise and fall of these political entities tends to follow an exponential distribution: e^(−λt) . This is an incredibly elegant summation of what we know qualitatively: **some empires last a long time, but most do not.**

  
[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/expo2.png?resize=298%2C285)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/expo2.png?resize=298%2C285)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/expo2.png)Interestingly the mean length of an empire is 220 years. That’s basically what you’d probably expect from intuition, especially if you knew Chinese history. To the left is a density plot I generated with the data provided in the paper. You can see that the mode and mean are a bit different because of the skewness. One of the interesting points about the exponential distribution is that it implies that the the duration of an empire at any given moment can’t tell you the probability that it’s going to collapse in the near future. The distribution is “memoryless.” In other words, the likelihood of doom striking isn’t greater as time passes. This seems somewhat counterintuitive. After all doesn’t the cohesion and elan of the a ruling caste of a given empire wane as the society slowly lose its vital force? Hasn’t the author read Spengler! Arbesman admits that there are more complex equations which can describe the distribution more precisely, but the exponential formula has only one parameter, so it’s quite parsimonious. But even if we have a first approximation we don’t have a total description.

Like evolutionary process as a whole I’m not convinced that the nature of the current data set is sufficient to deny the shifting background parameters which are operative over time. As I’ve noted before, there are two counteracting tendencies over time in human history when it comes to social & political entities:

– A greater rate of cultural change over time

– A greater cohesion and integrative power of social and political systems (more rapid bounce-backs from collapse, and greater civilizational continuity)

One thing I wanted to do is check to see what the correlation between age of the polity and its duration was. My intuition was that older polities will have greater recorded duration. Obviously there’s just more time for them, but some societies, such as Egypt, were very stable for longer periods of time in far antiquity. When I ran the correlate it was pretty weak, -0.23. Below is a chart which shows the scatter plot and the r-squared (correlation squared):

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/empires_htm_m5862ed6e.jpg?resize=485%2C478)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/empires_htm_m5862ed6e.jpg?resize=485%2C478)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2011/08/empires_htm_m5862ed6e.jpg)

Here’s the original data:

------------------------------------------------------------------------

|                                 |               |              |
|---------------------------------|---------------|--------------|
| **Empire**                      | **Adulthood** | **Duration** |
| Western Turk (C. Asia)          | 582           | 0.7          |
| Avar (Europe)                   | 580           | 2            |
| T’u Chueh Turk (C. Asia)        | 550           | 0.9          |
| Visigoth (Europe)               | 470           | 2.4          |
| White Hun (Indo-Iran)           | 460           | 1            |
| Toba (China)                    | 440           | 1.3          |
| Yuen-Yuen (C. Asia)             | 400           | 0.3          |
| Byzantine (Europe)              | 395           | 3.5          |
| Hun (Europe)                    | 380           | 0.8          |
| Gupta (India)                   | 370           | 0.9          |
| Liu-Sung (China)                | 330           | 2.1          |
| Ptolemaic (Africa)              | 323           | 2.9          |
| Bactria (Indo-Iran)             | 200           | 0.6          |
| Kushan (Indo-Iran)              | 75            | 2            |
| Rome (Europe)                   | 0             | 4            |
| Saka (Indo-Iran)                | -50           | 1.2          |
| Parthia (Iran)                  | -60           | 7            |
| Ch’in (China)                   | -90           | 2.9          |
| Andhra (India)                  | -170          | 3.7          |
| Hsiung Nu Hun (C. Asia)         | -190          | 1            |
| Maghada-Maurya (India)          | -300          | 0.9          |
| Achaemenid (Iran)               | -540          | 3.2          |
| Lydia (Anatolia)                | -610          | 0.6          |
| New Babylon (Mesopotamia)       | -610          | 0.7          |
| New Assyrian (Mesopotamia)      | -700          | 0.8          |
| Late Period (Egypt)             | -715          | 1.9          |
| Phrygia (Anatolia)              | -760          | 0.6          |
| Urartu (Mesopotamia)            | -810          | 0.9          |
| Babylon (Mesopotamia)           | -1000         | 2.5          |
| Middle Assyrian (Mesopotamia)   | -1090         | 0.5          |
| Hittite (Anatolia)              | -1320         | 1.3          |
| Hsia-Shang (China)              | -1350         | 4            |
| New Empire (Egypt)              | -1500         | 5            |
| Mitanni (Mesopotamia)           | -1500         | 1.4          |
| Elam (Mesopotamia)              | -1600         | 10           |
| Hykso (Syria)                   | -1650         | 0.8          |
| Babylon—Hammurabi (Mesopotamia) | -1700         | 2            |
| Old Assyria (Mesopotamia)       | -1800         | 1            |
| Middle Empire (Egypt)           | -2000         | 3            |
| Akadia (Mesopotamia)            | -2310         | 1            |
| Old Empire (Egypt)              | -2800         | 5            |

### Related Posts:

- [On getting gated
  papers](https://www.gnxp.com/WordPress/2012/12/03/on-getting-gated-papers/) - [Two posts on history and
  dynamics](https://www.gnxp.com/WordPress/2008/08/06/two-posts-on-history-and-dynamics/) - [Haldane
  Papers](https://www.gnxp.com/WordPress/2006/11/21/haldane-papers/) - [What is going on with plant
  domestication?](https://www.gnxp.com/WordPress/2012/10/03/what-is-going-on-with-plant-domestication/) - [Eurasian
  books](https://www.gnxp.com/WordPress/2009/09/13/eurasian-books/) - [Did you pass a paper to me last
  december?](https://www.gnxp.com/WordPress/2009/10/20/did-you-pass-a-paper-to-me-last-december/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F08%2F04%2Fthe-fall-of-empires-as-an-exponential-distribution%2F&linkname=The%20fall%20of%20empires%20as%20an%20exponential%20distribution "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F08%2F04%2Fthe-fall-of-empires-as-an-exponential-distribution%2F&linkname=The%20fall%20of%20empires%20as%20an%20exponential%20distribution "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F08%2F04%2Fthe-fall-of-empires-as-an-exponential-distribution%2F&linkname=The%20fall%20of%20empires%20as%20an%20exponential%20distribution "Email")[](https://www.addtoany.com/share)
