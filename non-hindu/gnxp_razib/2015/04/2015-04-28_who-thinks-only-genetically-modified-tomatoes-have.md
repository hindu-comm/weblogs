+++
title = "Who thinks only"
full_title = "Who thinks only genetically modified tomatoes have genes?"
date = "2015-04-28"
upstream_url = "https://www.gnxp.com/WordPress/2015/04/28/who-thinks-only-genetically-modified-tomatoes-have-genes/"

+++
Source: [here](https://www.gnxp.com/WordPress/2015/04/28/who-thinks-only-genetically-modified-tomatoes-have-genes/).

Who thinks only genetically modified tomatoes have genes?

[![41rxx-UtsWL.\_SY344_BO1,204,203,200\_](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/04/41rxx-UtsWL._SY344_BO1204203200_-189x300.jpg?resize=189%2C300)![41rxx-UtsWL.\_SY344_BO1,204,203,200\_](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/04/41rxx-UtsWL._SY344_BO1204203200_-189x300.jpg?resize=189%2C300)](https://www.amazon.com/exec/obidos/ASIN/0195393570/geneexpressio-20)Genetically modified organisms (GMO) are a topic I have some interest in, even though I don’t talk about it much. That’s partly because I’m a genetically modified organism; on the order of [8% of my genome was inserted by viruses](http://www.popsci.com/science/article/2010-01/8-percent-human-dna-comes-virus-causes-schizophrenia). More importantly a moral panic about GMO is currently an obstacle to their utilization in full. Yes, GMO are in corn and soybean, but their application is constrained by explicit and implicit bars. Of course these constraints are quite popular. This is why [Chipotle is removing GMO](http://www.usatoday.com/story/money/2015/04/27/chipotle-fast-food-restaurants-gmos-genetically-modified-ingredents/26450061/) from their food. It’s a matter of capitalism, **not** science or health.

Often when you drill down to it fear of GMO come down to two issues. First, there is the “wisdom of repugnance.” People who are not aware of how common horizontal gene transfer in the natural world is are frightened by the idea of “fish genes in tomatoes.” How about [snake genomes in cow](http://phenomena.nationalgeographic.com/2013/01/01/how-a-quarter-of-the-cow-genome-came-from-snakes/)? That is not something man hath wrought. Then there is the issue of corporations and monoculture. **But this is not a necessary function of GMOs.** Organics are very popular with corporations because they can charge a premium through price discrimination (the poor can’t afford organics, while the upper middle class will pay more for them). And monocultures in food production has been an issue which goes back at the latest to the Irish potato famine. Well before transgenics of the scientific sort.

I was curious about opinions about GMO in the [General Social Survey](http://sda.berkeley.edu/sdaweb/analysis/?dataset=gss14). I found the variable TOMATOES. It states: ***“Ordinary tomatoes do not contain genes, while genetically modified tomatoes do. (Is that true or false?)”***

The correct answer is obviously false. But I was curious what proportion of the population would answer “true.” Here are some demographics….

|                                  |                          |        |
|:---------------------------------|:-------------------------|-------:|
| ****                            |                          | True % |
| **Sex**                          | Male                     |   28.3 |
| ****                            | Female                   |   31.9 |
| ****                            |                          |        |
| **Highest level of education**   | Less than HS             |   48.6 |
| ****                            | High School              |   33.4 |
| ****                            | Junior College           |   36.3 |
| ****                            | Bachelor                 |   18.1 |
| ****                            | Graduate                 |   17.6 |
| ****                            |                          |        |
| **Political ideology**           | Liberal                  |   26.8 |
| ****                            | Moderate                 |   33.3 |
| ****                            | Conservative             |   28.3 |
| ****                            |                          |        |
| **Belief about nature of God**   | Atheist                  |   25.2 |
| ****                            | Agnostic                 |   23.2 |
| ****                            | Believe in higher power  |   20.5 |
| ****                            | Believe in God sometimes |   30.1 |
| ****                            | Believe with some doubts |   34.6 |
| ****                            | Know God exists          |   31.8 |
| ****                            |                          |        |
| **Belief about nature of Bible** | Word of God              |     38 |
| ****                            | Inspired word of God     |   31.3 |
| ****                            | Book of fables           |   18.2 |
| ****                            |                          |        |
| **Age**                          | 35 and under             |   34.5 |
| ****                            | 35 to 64                 |   24.7 |
| ****                            | 65 and over              |   40.8 |
| ****                            |                          |        |
| **Correct number on vocab test** | 0 to 4                   |   59.1 |
| ****                            | 5                        |   41.5 |
| ****                            | 6                        |   40.7 |
| ****                            | 7                        |   28.6 |
| ****                            | 8                        |   13.6 |
| ****                            | 9 to 10                  |    7.1 |
| ****                            |                          |        |

I decided to check these variables against a logit regression. The results are as so:

|                                                       |        |           |            |                 |                 |
|:------------------------------------------------------|:-------|:----------|:-----------|:----------------|:----------------|
| **Logit Coefficients Test That Each Coefficient = 0** |        |           |            |                 |                 |
| ****                                                 | **B**  | **SE(B)** | **Exp(B)** | **T-statistic** | **Probability** |
| WORDSUM                                               | 0.413  | 0.099     | 1.511      | 4.173           | 0               |
| DEGREE                                                | 0.226  | 0.15      | 1.254      | 1.504           | 0.134           |
| SEX                                                   | -0.841 | 0.367     | 0.431      | -2.291          | 0.023           |
| POLVIEWS                                              | 0.063  | 0.127     | 1.065      | 0.491           | 0.624           |
| BIBLE                                                 | -0.068 | 0.242     | 0.934      | -0.28           | 0.779           |
| GOD                                                   | -0.076 | 0.145     | 0.926      | -0.525          | 0.6             |
| AGE                                                   | -0.003 | 0.01      | 0.997      | -0.258          | 0.796           |
| Constant                                              | -0.433 | 1.406     | 0.649      | -0.308          | 0.759           |

The big variable here that remains very significant is WORDSUM. The score on a vocabulary test from 0 to 10 which has a correlation with [general intelligence of 0.71](http://blogs.discovermagazine.com/gnxp/2010/05/wordsum-iq/). Perhaps only the intelligent can really comprehend or understand this question? Looking at the descriptive results above it shouldn’t be surprising. The educational gap turns out to mostly be explained by WORDSUM. If your remove WORDSUM then DEGREE becomes a very big deal.

**Note:** the question was asked in 2010, and the sample size was on the order of 1,000 (depends on the crossing variable). Also, I understand some people will claim that the question is priming respondents and confusing people with minimal science understanding. I would suggest you’d get confused if you aren’t very smart or thoughtful. Or, you think “genes” are unnatural and the reason we can’t have nice things.

### Related Posts:

- [80% of public support mandatory labelling of food
  containing…](https://www.gnxp.com/WordPress/2015/01/17/80-of-public-support-mandatory-labelling-of-food-containing-dna/) - [Do liberals oppose genetically modified organisms more
  than…](https://www.gnxp.com/WordPress/2013/06/11/do-liberals-oppose-genetically-modified-organisms-more-than-conservatives/) - [San Francisco supported Proposition
  37!](https://www.gnxp.com/WordPress/2012/11/20/san-francisco-supported-proposition-37/) - [Liberal science denialism at the ballot
  box](https://www.gnxp.com/WordPress/2014/11/17/liberal-science-denialism-at-the-ballot-box/) - [Regulatory barriers to small-scale GMO
  production](https://www.gnxp.com/WordPress/2015/07/19/regulatory-barriers-to-small-scale-gmo-production/) - [Prop 37 and the right to have the government enforce
  your…](https://www.gnxp.com/WordPress/2012/10/30/prop-37-and-the-right-to-have-the-government-enforce-your-right-to-know/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F04%2F28%2Fwho-thinks-only-genetically-modified-tomatoes-have-genes%2F&linkname=Who%20thinks%20only%20genetically%20modified%20tomatoes%20have%20genes%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F04%2F28%2Fwho-thinks-only-genetically-modified-tomatoes-have-genes%2F&linkname=Who%20thinks%20only%20genetically%20modified%20tomatoes%20have%20genes%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F04%2F28%2Fwho-thinks-only-genetically-modified-tomatoes-have-genes%2F&linkname=Who%20thinks%20only%20genetically%20modified%20tomatoes%20have%20genes%3F "Email")[](https://www.addtoany.com/share)
