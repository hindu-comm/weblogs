+++
title = "The silent majority"
full_title = "The silent majority liberals who support free speech"
date = "2015-11-11"
upstream_url = "https://www.gnxp.com/WordPress/2015/11/11/the-silent-majority-liberals-who-support-free-speech/"

+++
Source: [here](https://www.gnxp.com/WordPress/2015/11/11/the-silent-majority-liberals-who-support-free-speech/).

The silent majority: liberals who support free speech

[![onliberty](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/11/onliberty-193x300.jpg?resize=193%2C300)![onliberty](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/11/onliberty-193x300.jpg?resize=193%2C300)](https://www.amazon.com/exec/obidos/ASIN/B004UJ8LVM/geneexpressio-20)At this point you have heard about the controversies at Yale and Missouri. If you haven’t, just Google it. Among liberals there has been some debate and soul searching about the value of free speech, and its diminishing status as inviolate among youth. Jon Chait has a pretty thorough take over at [New York Magazine](http://nymag.com/daily/intelligencer/2015/11/can-we-take-political-correctness-seriously-now.html). You can follow links to the arguments of those who contextualize and apologize for the more Maoist of the protesters to “get the other side.”

Since I support free speech, offensive speech, and engage in a fair amount of offensive speech, obviously I have a reflex to side with Chait on principle. Additionally, I’m a conservative who finds intra-Left/liberal conflicts pretty interesting and delicious. Finally, I don’t think that America is horribly racist, nor do I think institutionalized racism is a huge problem on campus (and perhaps not so much outside of campus, at least insofar as policy can and should address it), and, I don’t think that much consideration should be given to “marginalized populations” in terms of being particularly sensitive or apologizing for them (there is a whole lexicon which has cropped upon the Left which has a lot of meaning within-group, but is useless when attempting to communicate out-group; I reject the legitimacy of the terms of the debate as it is presented by many on the Left and liberals).

[![711zuJb66HL](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/11/711zuJb66HL-184x300.jpg?resize=184%2C300)![711zuJb66HL](https://i0.wp.com/www.unz.com/wp-content/uploads/2015/11/711zuJb66HL-184x300.jpg?resize=184%2C300)](https://www.amazon.com/exec/obidos/ASIN/B00MLFBDBM/geneexpressio-20)In my more cynical moments I’ve stated that we need to stick a fork in John Stuart Mill, and the idea of a free exchange of ideas. The Left has started to go [full Marcuse](http://www.marcuse.org/herbert/pubs/60spubs/65repressivetolerance.htm), to the point where even the language used by conservatives is deemed illegitimate. Yes, there are liberals who attempt to enforce the old rules of tolerance of vigorous dissent, but at the end of the day there’s not much broader policy daylight between the two campus, so will they stand up for unpopular views when push comes to shove? The best bet then would be to join in the animal-battle for the authoritarian state of yore as it comes back to life. Kill or be killed, while the libertarians keep shouting “can’t we just get along?!?!?!”

But my old standby is **what do the data say?** Back when “trigger warnings” were in the news I noticed that there was a question in the [general social survey](http://sda.berkeley.edu/sdaweb/analysis/?dataset=gss14) about the removal of library books. There is a variable LIBMSLM which asks about an “anti-American Muslim clergymen’s book”:

> If some people in your community suggested that a book he wrote which > preaches hatred of the United States should be taken out of your > public library, would you favor removing this book, or not.

There are also similar questions about anti-religious books, militarist books, a book promoting homosexuality, and a book promoting racism. My question is simple: **what demographic groups support the removal of these books?** The detailed methods are at the end of this post (you should be able to replicate), but what I basically did is used a [logistic regression](https://en.wikipedia.org/wiki/Logistic_regression) to compare the effects of several variables at once in terms of predicting attitude toward book removal. The samples were limited to the year 2000 and later.

What did I find?

\* Liberals support free speech more than conservatives. Even in cases, such as racist books, where ideologically you would suppose they would oppose it (and there is a modest trend if you look at the period between 1990 to 2014 for liberals to be more supportive of removing the racist book).

\* The more educated and more intelligent support free speech more than the less educated and less intelligent (the effects hold independently of each other).

\* Whites are more supportive of free speech than non-whites, except in the case of a book promoting homosexuality, where there is no difference.

\* Atheists and agnostics are moderately more in favor of free speech than the very religious. They are not very differentiated when it comes to the anti-American Muslim clergymen, confirming secular discomfort with fundamentalist Islam.

If one follows Twitter of the elite media one might be surprised that liberals are more supportive of free speech than conservatives. A different set of [similar variables](http://www.unz.com/gnxp/liberals-and-the-intelligent-stand-by-free-speech/) support the same conclusion. So what’s going on here?

First, I do think that the hot-house of the campus environment results in distortion and extremism which has minimal support more broadly. My Twitter following is very diverse, and many liberals have been direct messaging me expressing worry and anger at the anti-free speech antics of the protesters. But please observe: **the have been *direct messaging*, rather than putting up their objections in my *public* timeline.** Though the majority of liberals still support free speech, the loudest and most organized element seem to be much more “nuanced” on the issue of freedom of thought.

Second, the modern Left is a coalition of very different groups. The majority of the non-white sample above was black, and it is clear that in regards to speech non-whites are less supportive of tolerance of taboo or unpopular ideas than whites. White liberals may be very strong supporters of free speech, but their political allies may not be. And, the reality is that in terms of intra-coalition dynamics white liberals have to be very careful in how they talk to non-whites, lest they be accused of racism (I’ve been told by my wife to curtail my trolling on Twitter, but pretending to be an SJW of color is pretty fun when engaging with white liberals, since they let you slice off their balls at will, and don’t even object when you’re totally incoherent in your argumentation). This probably explains some of the private expression of support for free speech, but the subdued public sentiments. Liberals who support free speech also still want to eliminate institutional racism and oppression toward marginalized groups, so they have to balance their values when they seem at tension, and don’t want to be supporting those who oppose their policies even if they support the right of those people to disagree.

Finally, the robust support for free speech by the intellectual and social elites is heartening, and suggests that the courts are going to consistently serve as a legal bulwark against attempts to curtail dangerous ideas and sentiments. But obviously that’s not going to always translate into social norms.

Ultimately the question comes down to will. The broad sentiment of liberals does remain in the corner of liberty of thought, right or wrong. But will they stand up for unpopular views, as they have in the past, because in this country you can? That’s an open question I guess.  
  
**Methods:**

The dependent variable names are below in the table.

The independent variables were: sex, age, realinc (income adjusted for inflation), god(r:1-2″atheist/agnostic”;6″very religious”), polviews(r:1-3″Liberal”;5-7″Conservative”), race(r:1″white”;2-\*”non-white”), degree(r:0-2″No College”;3-4″College”), wordsum

Wordsum is a vocabulary test, with a [0.71](http://blogs.discovermagazine.com/gnxp/2010/05/wordsum-iq/) correlation with IQ.

Removing books was always coded as 1, and not removing as 2. Sex is 1 = male, 2 = female. For the god variable, 6 = those who “know god exists.” I did not look at moderates, but aggregated liberals and conservatives (extremely to slightly). For education I just divided between college and non-college.

To get an intuition for the direction of effect, for the anti-American preacher being a male, liberal, younger, more educated, more intelligent, and white, are statistically significantly contributing to greater odds of tolerating the book in the library.

|                   |             |        |             |            |        |             |             |        |             |
|:------------------|:------------|:-------|:------------|:-----------|:-------|:------------|:------------|:-------|:------------|
|                   | **LIBMSLM** |        |             | **LIBMIL** |        |             | **LIBHOMO** |        |             |
|                   | B           | Exp(B) | Probability | B          | Exp(B) | Probability | B           | Exp(B) | Probability |
| SEX               | -0.40       | 0.67   | 0.01        | 0.06       | 1.06   | 0.63        | 0.08        | 1.09   | 0.52        |
| POLVIEWS(Recoded) | -0.88       | 0.41   | 0.00        | -0.50      | 0.61   | 0.00        | -0.71       | 0.49   | 0.00        |
| AGE               | -0.01       | 0.99   | 0.00        | -0.03      | 0.97   | 0.00        | -0.02       | 0.98   | 0.00        |
| DEGREE(Recoded)   | 0.46        | 1.59   | 0.01        | 0.58       | 1.78   | 0.00        | 0.61        | 1.84   | 0.00        |
| WORDSUM           | 0.32        | 1.37   | 0.00        | 0.18       | 1.20   | 0.00        | 0.20        | 1.23   | 0.00        |
| REALINC           | 0.00        | 1.00   | 0.08        | 0.00       | 1.00   | 0.22        | 0.00        | 1.00   | 0.00        |
| RACE(Recoded)     | -0.49       | 0.61   | 0.01        | -0.77      | 0.46   | 0.00        | -0.17       | 0.85   | 0.27        |
| GOD(Recoded)      | -0.17       | 0.84   | 0.47        | -0.57      | 0.57   | 0.01        | -0.75       | 0.48   | 0.01        |
| Constant          | 0.90        | 2.46   | 0.17        | 2.92       | 18.61  | 0.00        | 2.66        | 14.33  | 0.00        |
|                   |             |        |             |            |        |             |             |        |             |
| ****             | **LIBATH**  |        |             | **LIBRAC** |        |             | ****       | ****  | ****       |
|                   | B           | Exp(B) | Probability | B          | Exp(B) | Probability |             |        |             |
| SEX               | -0.21       | 0.81   | 0.09        | -0.09      | 0.92   | 0.43        |             |        |             |
| POLVIEWS(Recoded) | -0.56       | 0.57   | 0.00        | -0.29      | 0.75   | 0.02        |             |        |             |
| AGE               | -0.02       | 0.98   | 0.00        | -0.01      | 0.99   | 0.05        |             |        |             |
| DEGREE(Recoded)   | 0.51        | 1.66   | 0.00        | 0.45       | 1.57   | 0.00        |             |        |             |
| WORDSUM           | 0.22        | 1.25   | 0.00        | 0.15       | 1.17   | 0.00        |             |        |             |
| REALINC           | 0.00        | 1.00   | 0.22        | 0.00       | 1.00   | 0.75        |             |        |             |
| RACE(Recoded)     | -0.62       | 0.54   | 0.00        | -0.55      | 0.58   | 0.00        |             |        |             |
| GOD(Recoded)      | -0.75       | 0.47   | 0.00        | -0.32      | 0.73   | 0.09        |             |        |             |
| Constant          | 3.31        | 27.37  | 0.00        | 1.20       | 3.30   | 0.02        |             |        |             |

### Related Posts:

- [Free speech not as important in Eastern
  Europe](https://www.gnxp.com/WordPress/2009/05/06/free-speech-not-as-important-in-eastern-europe/) - [Young, agnostic, moderately liberal & smart support
  free…](https://www.gnxp.com/WordPress/2009/03/10/young-agnostic-moderately-liberal-smart-support-free-speech/) - [Clash of
  freedoms](https://www.gnxp.com/WordPress/2006/04/18/clash-of-freedoms/) - [Free speech Über
  Alles!](https://www.gnxp.com/WordPress/2012/09/29/free-speech-uber-alles/) - [Insulting religions and races; should it be
  allowed?](https://www.gnxp.com/WordPress/2008/08/16/insulting-religions-and-races-should-it-be-allowed/) - [The New York Times posts stupid
  stuff](https://www.gnxp.com/WordPress/2007/04/09/the-new-york-times-posts-stupid-stuff/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F11%2F11%2Fthe-silent-majority-liberals-who-support-free-speech%2F&linkname=The%20silent%20majority%3A%20liberals%20who%20support%20free%20speech "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F11%2F11%2Fthe-silent-majority-liberals-who-support-free-speech%2F&linkname=The%20silent%20majority%3A%20liberals%20who%20support%20free%20speech "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F11%2F11%2Fthe-silent-majority-liberals-who-support-free-speech%2F&linkname=The%20silent%20majority%3A%20liberals%20who%20support%20free%20speech "Email")[](https://www.addtoany.com/share)
