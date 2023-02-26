+++
title = "Skin color and IQ in"
full_title = "Skin color and IQ in the GSS"
date = "2006-09-29"
upstream_url = "https://www.gnxp.com/WordPress/2006/09/29/skin-color-and-iq-in-the-gss/"

+++
Source: [here](https://www.gnxp.com/WordPress/2006/09/29/skin-color-and-iq-in-the-gss/).

Skin color and IQ in the GSS

A question from Jason Malloy prompted [a quick search of the GSS for data](https://www.gnxp.com/blog/2006/09/data-access-to-gss.php) on the cause of the Black-White IQ gap. In 1982, the GSS characterized the skin color of Black participants on a 5-point scale (1:very dark brown to 5:very light brown). The very dark/light categories consist of only 50 and 14 individuals, respectively, and so in the following analysis I merged them with the dark/light brown categories, to give three COLOR levels: dark, medium, and light. In the web application, use COLOR(r:1-2;3;4-5) instead of COLOR. The WORDSUM variable is a 10 question vocabulary test, which I’m treating as a proxy for IQ. It is correlated with educational attainment (\~.4), and also correlates (\~.4-.5) with tests of reasoning and basic knowledge that were given in some years. These other tests are not available for 1982. In the all-subject all-year GSS data set, WORDSUM varies by SEX, and in 1982 COLOR also varies by SEX. Thus, SEX is controlled for in each analysis. WORDSUM is lower in the youngest and oldest age groups, so an AGE(25-65) filter was used.

Table 1. Mean WORDSUM score by COLOR and SEX with ANOVA

**Main Statistics**

SEX

ROW  
TOTAL

COLOR

COL TOTAL

[TABLE]

color indicates T-statistic, and thus p-value

|                        |                      |        |       |                     |       |       |       | |:-----------------------|:--------------------:|:------:|:-----:|:-------------------:|:-----:|:-----:|-------| | **Color coding:**      |        \<-2.0        | \<-1.0 | \<0.0 |        \>0.0        | \>1.0 | \>2.0 | **T** | | **Mean in each cell:** | Smaller than average |        |       | Larger than average |       |       |       |

**Analysis of Variance**

|                  |           |        |     |        |        |       | |------------------|-----------|--------|-----|--------|--------|-------| |                  |           |        |     |        |        |       | |                  | SSQ       | Eta_sq | df  | MSQ    | F      | P     | | **Main effects** | 89.443    | .061   | 3   | 29.814 | 6.956  | .0002 | | **COLOR**        | 89.099    | .061   | 2   | 44.549 | 10.394 | .0000 | | **SEX**          | .691      | .000   | 1   | .691   | .161   | .6884 | | **Interaction**  | 2.569     | .002   | 2   | 1.285  | .300   | .7412 | | Residual         | 1,375.884 | .937   | 321 | 4.286  |        |       | | Total            | 1,467.896 | 1.000  | 326 |        |        |       |

We can quantify the effect size of each skin color class using Cohen’s d statistic, which measures the mean difference in standard deviation units. In the 1982 dataset, the overall d for the Black-White gap on WORDSUM is -0.63 (among males d=-0.51, among d=-0.74). For comparison, the 1982 male-female gap among Whites is d=-.12, favoring females.

Table 2. Effect size (d) of COLOR on WORDSUM using “light” as a control group

|        |       |        |       | |--------|-------|--------|-------| | Color  | Male  | Female | Total | | Dark   | -0.99 | -0.53  | -0.68 | | Medium | -0.31 | -0.20  | -0.22 | | Light  | 0.00  | 0.00   | 0.00  |

We can also use Whites as the control group.

Table 3. Effect size (d) of COLOR on WORDSUM using Whites as a control group

|        |       |        |       | |--------|-------|--------|-------| | Color  | Male  | Female | Total | | Dark   | -0.99 | -1.10  | -1.04 | | Medium | -0.35 | -0.69  | -0.54 | | Light  | -0.07 | -0.46  | -0.33 |

Thus, there are substantial (moderate to large effect size) differences in WORDSUM scores between the darkest and lightest Blacks in 1982.

As reported by [Rushton and Jensen (2005)](http://taxa.epi.umn.edu/~mbmiller/journals/pppl/200504/2/235-2.html), Shuey (1966) reviewed 18 studies which used skin color as a measure of racial admixture to compare with IQ. Of those 18, 16 found a significant effect of the kind found here, but the overall correlation with IQ was low (r=.1). In this data, the COLOR WORDSUM correlation is r=.31 among males and r=.18 among females, with an overall correlation of r=.23. Off the top of my head, I’m not certain what the expected correlation would be between IQ and skin color among Blacks for a given measure of “between-group heritability” (BGH) as described by Jensen (1998). I’ll leave it as an exercise for our mathematically skilled commentators to derive a formula for this relationship and to evaluate the signficance of this finding in explaining the cause of the Black-White IQ gap.

### Related Posts:

- [Question the "experts"
  sometimes....](https://www.gnxp.com/WordPress/2006/10/17/question-the-experts-sometimes/) - [How swarthy are the
  Sami?](https://www.gnxp.com/WordPress/2007/07/10/how-swarthy-are-the-sami/) - [Genetics of hair
  color](https://www.gnxp.com/WordPress/2006/10/26/genetics-of-hair-color/) - [Bah bah black sheep and balancing
  selection?](https://www.gnxp.com/WordPress/2008/01/17/bah-bah-black-sheep-and-balancing-selection/) - [Skin deep, why I'm brown and you wish you
  were](https://www.gnxp.com/WordPress/2006/09/25/skin-deep-why-im-brown-and-you-wish-you-were/) - [New Paper from the Journal of Bogus
  Sociology](https://www.gnxp.com/WordPress/2006/06/05/new-paper-from-the-journal-of-bogus-sociology/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2006%2F09%2F29%2Fskin-color-and-iq-in-the-gss%2F&linkname=Skin%20color%20and%20IQ%20in%20the%20GSS "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2006%2F09%2F29%2Fskin-color-and-iq-in-the-gss%2F&linkname=Skin%20color%20and%20IQ%20in%20the%20GSS "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2006%2F09%2F29%2Fskin-color-and-iq-in-the-gss%2F&linkname=Skin%20color%20and%20IQ%20in%20the%20GSS "Email")[](https://www.addtoany.com/share)
