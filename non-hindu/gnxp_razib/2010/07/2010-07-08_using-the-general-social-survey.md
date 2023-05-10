+++
title = "Using the General Social"
full_title = "Using the General Social Survey"
date = "2010-07-08"
upstream_url = "https://www.gnxp.com/WordPress/2010/07/08/using-the-general-social-survey/"

+++
Source: [here](https://www.gnxp.com/WordPress/2010/07/08/using-the-general-social-survey/).

Using the General Social Survey

I’ve mentioned this before, but I thought it would be useful to repeat again. Many of my social science related posts use Berkeley’s web interface with the [General Social Survey](http://sda.berkeley.edu/cgi-bin/hsda?harcsda+gss08). Regularly people ask me in the comments details as to the variables, or a more explicit elaboration of the methods. First, this is a weblog, not a venue for me to publish scholarly papers. Most of the GSS related posts are meant to be “quick & dirty,” and stimulate further exploration by readers. Unfortunately follow ups rarely happen. One can speculate why, but that’s how it is. Nevertheless, I thought I would repeat really quickly how to use the GSS in a basic fashion.

First, here’s the URL:  
<http://sda.berkeley.edu/cgi-bin/hsda?harcsda+gss08>

This is the database from 1972 to 2008. You’ll meet a screen like this:

  
![gss1](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2010/07/gss1.png?resize=600%2C403)![gss1](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2010/07/gss1.png?resize=600%2C403)

The page is cluttered, but basically the right side is where you enter in your row and column variables which you want to cross or compare together. The left side allows you to explore the variables. Search and selected are pretty straightforward, while you can browse the list of variables in the menu to the bottom left. The easiest thing to do is just look at frequencies of X, Y, and Z against particular categories A, B and C (e.g., educational attainments vs. sex). But you can do more, at the top left if you select “analysis” you have more options:

![gss2](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2010/07/gss2.png?resize=600%2C375)![gss2](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2010/07/gss2.png?resize=600%2C375)

I’ve been looking at mean values a lot. Sometimes the mean is obvious because the variables are quantitative. But if you’re talking about a dichotomous response it is “recoded” numerically (e.g., 0 vs. 1), so you have to keep in mind that the mean is just a representation of the underlying data. There are correlations and regressions too. You can do a lot with the GSS, but the more complicated or detailed you get in your analysis, the less appropriate for a “quick & dirty” they are. I’ve been shying away from presenting regressions because to do it right you have to be careful, and if you just throw out a bunch of betas people aren’t going to replicate your analysis and might put more stock in the model than they should (and it’s not hard to massage the betas you get with your variables my just manipulating the set of variables).

Here’s a quick example of a query:

![gss3](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2010/07/gss31.png?resize=552%2C190)![gss3](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2010/07/gss31.png?resize=552%2C190)

WORDSUM will output the % in the sample who score 0, 1, 2, etc. out of 10 on the WORDSUM vocabuary test. I wanted to check it against highest education attained, DEGREE. I decided to combine those without high school diplomas, those with high school diplomas, and some college, into one category, and label it “No College.” Next I combined those with bachelors and graduate degrees into one category. Then I controlled for males and females, so it will output the row and column variables twice for each control. Finally I constrained the data set to non-hispanic whites who were surveyed after 1999 to the present (2008 in this survey).

Here’s the outcome for males:

![gss4](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2010/07/gss4.png?resize=527%2C598)![gss4](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2010/07/gss4.png?resize=527%2C598)

### Related Posts:

- [General Social Survey on the
  desktop](https://www.gnxp.com/WordPress/2012/10/23/general-social-survey-the-desktop/) - [How to use the General Social
  Survey](https://www.gnxp.com/WordPress/2011/08/06/how-to-use-the-general-social-survey/) - [Data access to the
  GSS](https://www.gnxp.com/WordPress/2006/09/26/data-access-to-the-gss/) - [Reader
  survey](https://www.gnxp.com/WordPress/2007/11/10/reader-survey/) - [Google Wave is
  dead](https://www.gnxp.com/WordPress/2010/08/07/google-wave-is-dead/) - [Survey on genetics
  knowledge](https://www.gnxp.com/WordPress/2012/01/24/survey-on-genetics-knowledge/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F07%2F08%2Fusing-the-general-social-survey%2F&linkname=Using%20the%20General%20Social%20Survey "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F07%2F08%2Fusing-the-general-social-survey%2F&linkname=Using%20the%20General%20Social%20Survey "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F07%2F08%2Fusing-the-general-social-survey%2F&linkname=Using%20the%20General%20Social%20Survey "Email")[](https://www.addtoany.com/share)
