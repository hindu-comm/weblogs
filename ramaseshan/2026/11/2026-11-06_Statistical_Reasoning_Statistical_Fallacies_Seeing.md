+++
title = "Statistical Reasoning,"
full_title = "Statistical Reasoning, Statistical Fallacies & Seeing Through the Noise Part 1 Correlation"
upstream_url = "https://ramaseshanchandrasekaran.substack.com/p/statistical-reasoning-statistical"
date = "2026-11-06"
+++
Source: [here](https://ramaseshanchandrasekaran.substack.com/p/statistical-reasoning-statistical).

Statistical Reasoning, Statistical Fallacies & Seeing Through the Noise : Part 1 - Correlation

# Statistical Reasoning, Statistical Fallacies & Seeing Through the Noise : Part 1 - Correlation

### This series of three articles gives an accessible introduction to the tools of statistical reasoning, common statistical fallacies, and related philosophical problems without much math

[](https://substack.com/@ramaseshanc)

![Rama Seshan Chandrasekaran's avatar](https://substackcdn.com/image/fetch/$s_!ZHOm!,w_36,h_36,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11e50d60-b811-4831-8bbc-4d320762e60b_96x96.png)

[Rama Seshan Chandrasekaran](https://substack.com/@ramaseshanc)

Nov 06, 2026



20





5

Share

Learning to reason clearly with data is all the more important in this data-driven age, even as LLMs are becoming more and more effective at reasoning. Large language models might reason through and find patterns in vast and complex data sets much more easily than any single human, but still remember that : what we get from these models is as good as the kind of questions that we ask. From the same data, depending on the questions you ask, you might get different answers for a given situation. How much ever AI advances in medical diagnosis, it is ultimately us who have to describe the symptoms of our disease to either the doctor or the machine, and it is us who have the final hand to choose what tests to take or what to eat, among a lot of options. Similarly, the more we know how to handle and reason with data, we can get a more informative answer from these AI models.

No chatbot will work for us in the best way if we do not ask the right questions that are grounded in correct assumptions and feed the appropriate data and the context required. This is where I think basic statistical literacy is needed for everyone now even to use LLM models, in the same way a basic computer literacy is needed for everyone to even use these LLM models and consume what they give.

I firmly believe that basic statistical reasoning is important for a human to possess, irrespective of whether he is going to do it in a professional capacity or whether chatbots become more and more capable in technical skills. We become more sophisticated consumers or producers of information with a clear dose of statistical thinking. Unfortunately, most statistics and data analytics courses focus on the messy technical details; and students end up learning and memorising a ton of formulae, proofs, and algorithms, and start crunching numbers immediately, without focusing on the concepts and intuitions, that guide what is to be used in what situation. This is why I have decided to write a series of three articles to serve as a friendly guide to get comfortable in the broad strokes of thinking and reasoning involving in statistical analysis. This first article deals with correlation that is about discovering relationships from data ; while the next article is about establishing causal links between features based on their relationships ; while the third article will be about decision making with statistics.

------------------------------------------------------------------------

# Correlation & Measurement



At its most basic level, correlation is an empirical concept that tells us how much two features of the world tend to occur together. If the increase of one feature tends to increase the other feature as well, then the two features are called **positively correlated**. If the increase of one feature tends to decrease the other feature, then the two features are called **negatively correlated**. If the increase of one feature has no bearing on the other feature, then the two features are called **uncorrelated**. You might have also heard the famous technical adage that “***correlation does not imply causation***”. We will come back to discuss this in depth a little later ; for now, let us just understand what correlation means and entails (without bothering about causation).

For example, [here](https://edm-developers.github.io/fastEDM-r/articles/chicago.html) is a scatter plot between two features recorded in a given area (Chicago) in a given time period : the number of crimes in a day and the average temperature of the day. What is a scatter plot? Each red dot here is a point that gives the details about a particular day. The horizontal coordinate of each red point denotes the average temperature of the day and the vertical coordinate of each red point denotes the number of crime incidents on that particular day.

[](https://substackcdn.com/image/fetch/$s_!Z3LL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F86f34be8-c8fc-412b-92ea-96b9d5ef0560_1076x664.png)

![](https://substackcdn.com/image/fetch/$s_!Z3LL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F86f34be8-c8fc-412b-92ea-96b9d5ef0560_1076x664.png)





$`Point_{i} = (x_{i},y_{i})`$

$`x_{i}:\text{temperature at~}i^{th}\text{~day}`$

$`y_{i}:\text{number of crimes at~}i^{th}\text{~day}`$

By looking at this figure, one can see that there is a positive correlation between temperature and crime. That is, as the temperature increases, the crime increases on average. But, how can we numerically quantify the strength of correlation between these two features? There are two options possible. One is to draw a line of best fit that describes the relationship between temperature and crime. We will get more precise about this in a later section; but for now, the blue line in the below picture best describes the relation between these two variables as it cuts through the middle of these scatter points.

[](https://substackcdn.com/image/fetch/$s_!FTJ4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4035b7a7-0abc-445a-a4dd-eccbad51a74f_2624x1620.png)

![](https://substackcdn.com/image/fetch/$s_!FTJ4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4035b7a7-0abc-445a-a4dd-eccbad51a74f_2624x1620.png)





The slope of the blue line segment tells us about how strongly they are correlated. The slope of the blue line above is 6.25. This means that for every additional degree of temperature rise, the crime observed in Chicago increased on average by 6.25 in that time period of observation.

If the slope of the line of best fit is zero, it means that the two variables are **uncorrelated**.

If the slope of the line of best fit is positive, it means that the two variables are **positively correlated**.

If the slope of the line of best fit is negative, it means that the two variables are **negatively correlated**.

There is a simple formula to calculate the slope of the line of best fit about which we will see a little later. There is also another measure of correlation that is unit agnostic and can be used comparatively. Let us say that you observe a positive correlation between the number of crimes on a given day and the daily average temperature, while your friend observes a positive correlation between oil-wealth of nations and autocracy of their governments. A third person now asks which is a stronger positive correlation. This cannot be answered by the slope of the best fit because they have different units of measurement and it would be like comparing apples with oranges. In this case, we need a unit-less number that summarises the amount of correlation between the variables. The variable that does this is called the **correlation coefficient** which has no units and hence can be compared between different pairs of variables across various scenarios. An important feature of the correlation coefficient is that it strictly lies between
-1 and +1 and has no units at all. When the correlation coefficient is 0, it means that there is no correlation between the two features. When the correlation coefficient is at its maximum value +1, it denotes full positive correlation between the two variables and when it is at its minimum value -1, it denotes full negative correlation between the two variables. There are formulae for both the **slope of the best fit line** and the **correlation coefficient**. If you are not mathematically minded however, feel free to just browse quickly through the formulae. But if you can tolerate some Class 10 level mathematics, continue reading with focus.

Let (x_1, y_1), (x_2, y_2), (x_3, y_3), … , (x_i, y_i), … , (x_N, y_N) be the coordinates of the N scatter points. First, their **average**, denoted by the Greek letter μ are defined as follows where the big Σ denotes addition over all the samples :

$`\mu_{X}:=\frac{1}{N}\sum\limits_{i = 1}^{N}x_{i}`$

$`\mu_{Y}:=\frac{1}{N}\sum\limits_{i = 1}^{N}y_{i}`$

Now, the average tells us the centre value of the bunch of data corresponding to a variable, but cannot tell us the spread of the variable. For example, consider two countries A and B with just four people each. The following are the annual incomes in USD of the four people of A and B along with their averages.

[](https://substackcdn.com/image/fetch/$s_!yB9m!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9ccf0a9-2669-4bbc-b6ae-095c05472587_1298x648.png)

![](https://substackcdn.com/image/fetch/$s_!yB9m!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9ccf0a9-2669-4bbc-b6ae-095c05472587_1298x648.png)





In both of these countries, the average annual income of the citizens is 10,000 USD. But, we see that in the country A, the incomes of the citizens are narrowly distributed about the mean and are almost equal; whereas in the country B, the incomes of the citizens are unequally distributed around the same mean. We need another number that summarises this inequality or spread of the data about the mean. For that, let us first define a quantity called the **standard deviation** which is denoted by the symbol sigma given below.

$`\sigma_{X}:=\sqrt{\frac{1}{N}\sum\limits_{i = 1}^{N}(x_{i} - \mu_{X})^{2}}`$

$`\sigma_{Y}:=\sqrt{\frac{1}{N}\sum\limits_{i = 1}^{N}(y_{i} - \mu_{Y})^{2}}`$

Note that the standard deviation of X is always non-negative and will be equal to zero if and only if all the samples are equal to the average. If even one sample point x_i is different from the average, the standard deviation begins to rise. We square the difference because we want deviation to the right of the average to be equally penalised as deviation to the left of the average. We divide by N because we want the average of these square deviations of each sample. We take the square root finally to get a quantity whose units is same as that of the variable of interest.

Now, let us define another quantity called **co-variance** between two variables which is :

$`cov(X,Y):=\frac{1}{N}\sum\limits_{i = 1}^{N}(x_{i} - \mu_{X})(y_{i} - \mu_{Y})`$

This measure gives a sign of the correlation between the two variables. If X and Y are positively correlated, then whenever x_i is above its average, y_i also will tend to be above its average. Thus, the products inside the summation of the above equation will have the same sign and hence will be positive. If X and Y are negatively correlated, then whenever x_i is above its average, y_i will tend to be below its average. Thus, the products inside the summation of the above equation will have the opposite sign and hence will be negative. If they are uncorrelated, then whenever x_i is above its average, y_i is equally likely to be above or below its average and hence the products are equally likely to be both positive and negative and hence will add up to zero.

We now present the formulae for the correlation coefficient and the slope of the best fit line.

$`\text{Correlation Coefficient~}r(X,Y):=\frac{cov(X,Y)}{\sigma_{X}\sigma_{Y}}`$

$`\text{Slope of best fit line~}m(X,Y):=\frac{cov(X,Y)}{\sigma_{X}^{2}}`$

Having seen what correlation entails and how to measure it and compare it, we will now see some common fallacies involved when we try to reason using correlation.

------------------------------------------------------------------------

# Correlation Needs Variation



In order to establish a correlation between two variables, one has to collect data that vary both the variables. For example, if we want to establish a correlation between temperature and crime (as we saw in the previous section), we need to collect data for both hot days and cold days; and also collect data for high-crime days and low-crime days. If we collect data only for hot days (or only for cold days), that does not prove any correlation, and it may actually mislead us into believing a wrong correlation. Consider the following statement about US politics

> Most politicians facing a scandal tend to win re-elections

There are two features of interest here : the first is whether a politician is facing a scandal ; the second is whether the politician successfully wins the re-election. The statement seems to establish a (seemingly unintuitive) positive correlation between politicians facing scandals and politicians winning re-elections. The fact quoted above may be true in the sense that among politicians facing scandals, many of them do win re-elections. But, this does not establish a positive correlation between politicians facing scandals and winning re-elections because the data (that the quote talks about) concerns only those politicians who faced scandals. It does not tell us about anything regarding what happens to those politicians who did not face scandals. Without getting to know that other half of the picture, we cannot conclude anything about the nature of the correlation between these two phenomena. Let us now look at the complete data and see what it has to offer.

Scott Basinger has systematically collected data on congressional scandals between 2006 and 2012. The first part of this data is given as follows :

[](https://substackcdn.com/image/fetch/$s_!1HMq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F74a4fa8d-39ef-40f3-ae3c-c3ac66ffa934_1324x434.png)

![](https://substackcdn.com/image/fetch/$s_!1HMq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F74a4fa8d-39ef-40f3-ae3c-c3ac66ffa934_1324x434.png)





Observing this partial data, we do see that among the total 70 politicians facing scandals, 62 of them do get re-elected which is about 89% of them. So, the quoted news item that “*Most politicians facing a scandal tend to win re-elections*” is indeed correct. But, does that mean that facing scandals is positively correlated to winning re-elections? For this, let us observe the complete data which is as follows.

[](https://substackcdn.com/image/fetch/$s_!yVR0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd305fc6f-3064-406b-b22e-a1462060b1eb_1308x446.png)

![](https://substackcdn.com/image/fetch/$s_!yVR0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd305fc6f-3064-406b-b22e-a1462060b1eb_1308x446.png)





Let us now find the correlation coefficient between scandals and winning re-elections using the complete data in all the four cells. Here, both x_i and y_i are restricted to either 0 or 1. Consider the following conventions regarding each politician numbered “i” in the data:

> x_i = 0 : politician does not face a scandal  
> x_i = 1 : politician does face a scandal
>
> y_i = 0 : politician does not win the re-election  
> y_i = 1 : politician wins the re-election

Now, we can say the following for the data (x_i , y_i) from the table above :

> Number of (0,0) : 101  
> Number of (0,1) : 1,192  
> Number of (1,0) : 8  
> Number of (1,1) : 62

Let us now plot the scatter plot for the above case. Since all the data points only take four values of (0,0), (0,1), (1,0), and (1,1), I give the width around these points to convey the number of data points in those values.

[](https://substackcdn.com/image/fetch/$s_!3KAu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7010b6a6-3a2c-49ee-8846-e01ab89eab49_1948x1196.png)

![](https://substackcdn.com/image/fetch/$s_!3KAu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7010b6a6-3a2c-49ee-8846-e01ab89eab49_1948x1196.png)





After seeing the scatter plots in blue and the line of best fit in red, one sees that there is actually a slightly negative correlation between facing a scandal and winning a re-election!! This is the opposite of what the initial statement “*Most politicians facing a scandal tend to win re-elections*” conveys!! Why is this the case?

The initial statement “*Most politicians facing a scandal tend to win re-elections*” is made based on the fact that 89% of politicians facing scandals end up winning re-elections. But, this does not tell anything about how facing a scandal affects the prospects of winning the re-election until we look at how many percentage of politicians not facing scandals end up winning re-elections. If we look at this side of the picture, we see from the data that there are 1,293 politicians who did not face scandals and 1,192 of them too end up winning re-elections which turns out to be 93% of them, which is higher than the 89% in the scandal facing side!! So, we see from both sides of the data that facing a scandal reduces the chances of winning the re-election from 93% to 89% which results in the slightly negative correlation that we obtained. Had the percentage of non-scandal facing politicians winning re-elections been much less than 89%, then we can say that facing a scandal is positively correlated to (and hence increases the odds of) winning a re-election.

This may seem like something obvious to you now but it is an extremely and embarrassingly common mistake made by many people across the board who may be experts in their own field but do not possess statistical literacy. You might nod your head in agreement now, but now let me show you tons of examples of extremely smart people making this mistake in high-stakes environments. All these mistakes are made because only one side of the picture is painstakingly collected and analysed while the other side is completely neglected.

------------------------------------------------------------------------

# Selecting on the Dependent Variable



Intuitively, we all would think that, to explain a phenomenon Y, one should start by examining previous instances where that phenomenon Y occurred, and see if they share some feature, say X, in common. For example, if you want to explain a disease Y, observe as many instances of the disease occurring, and see what features, say X, recurrently occur in them. But, as I said just now, when you are trying to find correlations between X and Y, you also have to look at instances where the phenomenon Y did not occur. When you do not do that, you end up making a huge mistake. The name “***dependent variable***” is normally used to refer to the variable that you are trying to explain and is denoted by the symbol Y (like crime or disease or winning elections). The name “***independent variable***” is normally denoted by the symbol X and refers to the variable that one is trying to use in order to explain the dependent variable Y. The mistake in this sub-section is called as “*Selecting the Dependent Variable*” because you are looking only at those data for particular values of the dependent variable, without looking at other values. If you are trying to explain a disease Y, you would collect and examine only those data where the disease occurred while ignoring to collect those data for the cases when the disease did not occur.

As natural as it may seem, looking for patterns and commonalities in past instances of **only** **occurrences** of the event of interest (that you want to explain), is really a huge mistake. Since correlation requires variation, it is **also** necessary to look at those past of **non-occurrences** of the event of interest (that you want to explain).

I will now give lots of examples of this fallacy being used by many people who are otherwise experts (or faux experts) in their own fields. There is a very important reason why I avoid reading self-help books in general. Consider the following book below :

[](https://substackcdn.com/image/fetch/$s_!kVvq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0fedca63-6bb1-479d-a88a-404a4fa2e761_978x1500.jpeg)

![](https://substackcdn.com/image/fetch/$s_!kVvq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0fedca63-6bb1-479d-a88a-404a4fa2e761_978x1500.jpeg)





Here, the journalist **Malcolm Gladwell** tries explaining the success of high-achieving people based on a particular habit they follow which is the 10,000-Hour Rule. The central claim of this book is that there is a causal link between 10,000 hours of serious practice in a field and becoming a great success in that field. We have not discussed what causality is in detail, but correlation between the habit and success is anyway necessary to establish causality. So, let us first see whether even if this correlation claim holds water. Gladwell argues that behind many great achievers across various domains (from computer science to music), there is overwhelming evidence that they put 10,000 hours of intense practice. Assuming even that the data he has sampled is enough, still he has established only the following :

[](https://substackcdn.com/image/fetch/$s_!lBd4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe384db90-2d29-44d6-ab69-6b830fbc902a_1286x418.png)

![](https://substackcdn.com/image/fetch/$s_!lBd4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe384db90-2d29-44d6-ab69-6b830fbc902a_1286x418.png)





We see that he has given data only for achievers and has found that many put 10,000 hours of practice. But, to establish correlation between that habit and success (let alone causality), it is also necessary to undertake a detailed study on the habits of those non-achievers too. If you are a person who has spent five years on something full time but not a high achiever, you are one of those people in the two empty cells in the above picture. Many bestsellers like this book have made millions by selectively studying some iconic, highly successful people or companies or institutions to extract the supposed "secrets" of enduring corporate greatness, without bothering to look at the many examples of failures. Sometimes, due to the way in which the world is organised and expects things, and the way institutions are built, we are forced to look for correlation without having access to variation. There are many ways in which it can happen and some popular among them in various fields are enumerated here.

One of the reasons why I hate taking and giving advices from people is again exactly this problem. It is an expected practice for an aspiring person to ask successful people in his field what they did to make it and figure out the key decisions they made or stuff they did that ensured their success. But, those successful people (leaving aside their expertise and talent) have absolutely no idea about whether non-successful people also took those key decisions or did stuff they did. So, data on successful people alone can’t be the sole basis for determining correlates of their success. Hence, beware of life advice ; a lot of it is a scam anyways. We do realise it sometimes ourselves. Whenever we read articles like highly successful people tend to drop out of college or get low grades, we do feel that it is a scam because such analyses ignore the bulk of people who did drop out of college or get low grades but are stuck up in minimum wage jobs.

**Professional Constraints** : Consider the case of medical diagnosis. Doctors only see and examine sick people most of the time. Let us assume you have an intense back pain and go to a doctor and he orders an MRI and finds out that some discs in your spine are bulged or herniated. An experienced doctor who has seen lots of such back-pain cases knows that two-thirds of back pain sufferers had disc bulge or herniation (also confirmed in various studies). Does that mean that bulged/herniated discs are correlated to back pains? If you are a doctor who is an expert only in medicine, you might conclude affirmatively because two-thirds of back-pain cases do have it. But, since you know statistics, this is a bad idea because it is premature conclusion without examining the MRIs of those people who do not have back pains and checking how much of them have bulged/herniated discs. In fact, a study published in 1994 did find that two-thirds of people who do not have back pain, also have a disc bulge or herniation! So, we conclude that there is no correlation between bulging and herniation in discs and back pain. But, it is indeed obvious to see why even highly experienced doctors can fall into this trap easily; because a doctor is forced by his profession, to look only at cases of those people who have complaints, and healthy people do not come to hospitals for getting their bodies scanned.

**Post-Mortem Dissection** : After a great crisis or a catastrophic disaster (or success), everyone wants to know what went wrong (or what was done right), to avoid future disasters (or replicate future successes). Looking at instances of past failures (or successes) is indeed a good starting point but you now know that this is not sufficient to establish any correlations (let alone causations). For example, after the financial crisis of 2008, two famous economists Carmen M. Reinhart and Kenneth S. Rogoff collected and analysed data on every major financial crisis across the world for the past eight hundred years to look for early warning signals that preceded such crises.

[](https://substackcdn.com/image/fetch/$s_!EXh8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F38719e82-0746-4113-9d02-83841ccc2d4e_969x1500.jpeg)

![](https://substackcdn.com/image/fetch/$s_!EXh8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F38719e82-0746-4113-9d02-83841ccc2d4e_969x1500.jpeg)





The early warning indicators that they came up with include large current account deficits, asset price bubbles, and excessive borrowing. The issue here is again the same as in our earlier examples. Because establishing correlation requires variation, we should not just look at data when financial crises occur, but also at their prevalence at times when there are no crises. Again, they dealt with only one side of the picture and ignored collecting and analysing the complete data. Their meticulous studies of all financial crises while commendable are not sufficient.

[](https://substackcdn.com/image/fetch/$s_!oIVt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F397f05fe-39a7-4132-833e-bcce43c79d83_1298x434.png)

![](https://substackcdn.com/image/fetch/$s_!oIVt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F397f05fe-39a7-4132-833e-bcce43c79d83_1298x434.png)





**Survivor Bias** : After the British military forces introduced better Brodie steel helmets in World War I, the high command panicked because they noticed an alarming trend: the number of soldiers arriving with head injuries at field hospitals began increasing rapidly**.** Some officers initially panicked, arguing that the new helmets were somehow causing more head injuries or were making soldiers more reckless. In other words, they thought that steel helmets negatively correlated with solider safety, which actually is wrong (we know that more protection causes more safety). We now easily know where these commanders went wrong in their reasoning again; because they were looking at only the data from survivors who made it to the hospital. Before the helmets, a shrapnel hit to the head was almost always mortally fatal and those soldiers went straight dead to the morgue, never impacting the hospital registry. The helmets didn't cause injuries; they turned what used to be mortally fatal head wounds into survivable injuries that could be treated in the hospital. Again, the people who panicked looked at only one side of the data. This is called survivor bias because one typically looks at only survivors of a process (literal or metaphorical) and ignore the dead because they perish and become invisible.

[](https://substackcdn.com/image/fetch/$s_!B1B8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F264fa016-2d79-4154-839a-a6e29c873e8a_1306x506.png)

![](https://substackcdn.com/image/fetch/$s_!B1B8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F264fa016-2d79-4154-839a-a6e29c873e8a_1306x506.png)





**Important Statistical Fallacy Lesson** : Establishing correlation requires variation. Unclear thinking, organisational protocols, survivor bias, social expectations, impulsive intuitions, and other kinds of biases, often lead even experts to select the dependent variable and to collect and look at only one half of the data. Whenever you are doing any kind of causal reasoning or evidence-based thinking, force yourself to think whether you could fill in all the four cells of the two-by-two correlation table and have the complete picture.

[](https://substackcdn.com/image/fetch/$s_!yz0_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbaf93f5e-4c76-4ece-8622-7dac170714f7_1286x410.png)

![](https://substackcdn.com/image/fetch/$s_!yz0_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbaf93f5e-4c76-4ece-8622-7dac170714f7_1286x410.png)





To test your learning, here are a bunch of statements. Tell which of them are sufficient grounds to establish a correlation and which of them are not because dependent variable selection is involved.

1.  People who live more than 100 years old do so-and-so things.

2.  Older people tend to vote more than younger people.

3.  Most criminals are men (we also know that men and women are half of
    the total population).

4.  Most IITJEE national rank holders used a particular book X.

5.  Cities with higher crime rates have more police force.

6.  Most people who suddenly got sick in a city had a particular
    beverage

Once you realise this, you will see that this statistical fallacy abounds everywhere in all walks of life.

------------------------------------------------------------------------

# Using Correlation



In the last section, we saw a very important fallacy that leads one to erroneously conclude about correlations. Given that we indeed have the entire complete data, how can we go about describing a correlation and what can we use them for? They are used for three kinds of tasks :

#### Description of the data : Regression



Describing the data that we have collected is probably the safest use of correlation analysis. For example, looking at the demographics of the voter turnout in a particular election in a given area in a given year, let us assume that we find a positive correlation between age and voting turnout (i.e. older people participated more in voting). Let us assume that the slope of the regression line between age and voter-percentage is 0.006 for the 2014 mid-term American elections. This means that every additional year a person had in his age increased his percentage chance of going out to vote by 0.6% on average. This kind of description may be useful in making you think differently about the election results. There are lots of problems that one face in even this kind of descriptive analysis and these are dealt with in standard courses on statistics and data science. These include non-linear relationships between the feature variables and the associated problem of **under-fitting** and **over-fitting** (we will see more on this in the future). The broad area of statistics that involves finding out the relationship describing variables is known as **regression**. But, on the whole, regression is still the most straightforward and the least risky application of correlative analysis. Hence, we do not elaborate on this in much detail in this article further. I will write a stand-alone independent article on the technicalities and subtleties of regression, but it will not be a part of this article. But, to push the boundaries of correlative analysis any further, we need to make strong additional assumptions about the world and about the data about which the next two sub-sections elaborate.

#### Prediction from the data : Statistical Inference



Another reason why we are interested in correlation analysis involves using the information from the sample population we surveyed in our data to make predictions or forecasts about a different population that is not a part of the data set. For this, one needs to determine whether the relationship that you have found in your data is indicative of a broader relation across the larger population (for which you want to predict), or whether this relationship in your data is merely the result of chance variation and particular peculiarities (or eccentricities) specific to the samples which are represented in your dataset. In the case of the former, we can make bold predictions for the broader population based on analysing the data that we have sampled ; otherwise, we cannot reliably conclude anything. The broad area of statistics that involves using data analysis from a random sample to make conclusions, estimates, or generalisations about a larger population (of which the sample is a part of) is called **statistical inference**. For example, given the age-wise voter turn out data, you might ask if this same relation between age and voter turnout in the 2014 midterm election will hold true for the next 2016 presidential election as well. Or you might have collected the data only from 25 states in 2014 and you might be interested in knowing if the relation concluded from them holds for the remaining 25 states as well in the same election. The rest of this article is all about statistical inference.

#### Prescription based on the data : Causal Inference



Another reason why we are finding out relationships is to learn about causal relationships that will help us to decide on strategies to change some feature of the world. It is here where we have to be careful with the famous adage that “***correlation does not imply causation***”. Erroneously concluding a causal link between two variables when there is only a correlation between them can lead to policy disasters. Again, this sort of mistake is easy to understand but you can see all sorts of experts making this at all levels, ranging from peer-reviewed journals to policy making. To illustrate this, consider an example of the positive correlation that American students who take tough mathematics courses in high school (like Algebra 2, Trigonometry, Calculus) tend to complete their college education. Does this mean that taking tough mathematics courses causes students to complete college? It may not be the case, and something else may be at play here. People who take tough math courses in high school do so because they are academically well-motivated and self-driven. It is this same motivation that is also making them complete college. So, instead of taking tough mathematics courses directly causing students to complete college, it can also be possible that there is a third variable (which is self-motivation) that is causing both of these variables - taking tough mathematics courses and completing college.

Soon, we will prove that if two variables X and Y are positively correlated, it is always because of one of the four below scenarios :

1.  **Direct Causation** : X causes Y

2.  **Reverse Causation** : Y causes X

3.  **Mutual Causation** : X causes Y , Y causes X (feedback coupling)

4.  **Confounding Causation** : A third variable Z causes both X and Y

X = taking tough math courses in high school  
Y = completing college

When X is taking tough mathematics courses in school and Y is completing college, we know that it has to be either 1 or 4 (completing college definitely cannot cause someone taking tough math courses in high school). So, it has to be that either tough math courses in high school directly cause a student to prepare him for completing college; or that there is another common confounding cause Z (like self-motivation and self-drive) that causes both of them. Which one of the two it is, and what are the stakes involved?

The stakes involved are very high here. If X (taking tough math course in high school) directly causes Y (completing college), then compelling students to take tough mathematics courses in high school will lead to an increase in students completing college. But, if the confounding cause by a third variable Z (self-motivation) is right, then taking tough math courses in high school is just another indicator of motivation like completing college is. Requiring a student to compulsorily take tough mathematics courses will not magically make him more motivated and won’t have any effect on the students completing college. The exact mistake we just described was made in a peer-reviewed scientific article (click [here](https://www.jstor.org/stable/42732549)). The researchers here compared the college performance of people who did and did not take a variety of intensive high-school math courses. On the basis of the positive correlation they observed, they suggested that high school counsellors “*use the results of this study to inform students and their parents and guardians of the important role that high school math courses play with regard to subsequent bachelor’s degree completion*”. That is, they mistook correlation for causation. On the basis of these correlations, they recommended that students who were not otherwise planning to do so, should also enrol in intensive math courses to increase their chances of graduating from college. As we saw in the previous section, even people who are otherwise knowledgable and expert in their own fields, can make statistical mistakes which involve high stakes. The broad area of statistics that involves figuring out whether a specific action or event (the cause) directly leads to a particular result (the effect) within a system is called **causal inference**. We will deal with causation and causal inference in detail not in this article, but in the next article in this series. The next section and the remainder of this article will deal with mainly only the second application which is prediction, and also somewhat on the first application which is regression.

------------------------------------------------------------------------

# Statistical Inference : Bias & Noise



In this section, we enter the art of prediction using statistical patterns observed in samples of data. To start this subject, I am going to give a very simple equation that I will repeatedly refer you to. So, I am going to call it hereafter as the “important” equation.

![](https://substackcdn.com/image/fetch/$s_!B3iZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4b4d60e2-e46c-4fc2-bc88-5750d2cf88d0_1026x126.png)

The estimate is the number we get as the prediction for a variable based on our analysis of data. The true value refers to the actual value for the variable that we are interested in predicting. Ideally, we expect that the estimate is equal to the true value. But, in reality, there is an error between these two values which is made up of two terms : **bias** and **noise**. **Bias** refers to the errors that occur because of systemic reasons due to limitations in our regression methods. **Noise** refers to the errors that occur because of chance and noise from the idiosyncrasies of the data we sampled. Bias tells us how accurately the estimate is hitting the target on average. Noise tells us how much the estimate varies about the average across different samples for each dataset. If you think of estimation as shooting a target with an arrow, bias tells us how much your aim is drifted away from the target. Noise tells you how much your hits vary about your aim because of unforeseen factors.

**Noise** is a measure of ***inconsistency*** while **bias** is a measure of ***inaccuracy***. A completely noiseless but heavily biased estimator gives wrong answers consistently all the time ; whereas a completely unbiased estimator with heavy noise is inconsistent but gives the correct answer on average across different sets of samples.

Noise results from the idiosyncracies of the samples we chose from the population. Bias results from the limitations of the regression algorithm in capturing the exact relationship between variables in a population.

[](https://substackcdn.com/image/fetch/$s_!1RKi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1de74e60-9bd4-41f5-a644-a075e69ee9f4_748x830.png)

![File:Statistical bias and statistical noise illustration.png - Wikimedia Commons](https://substackcdn.com/image/fetch/$s_!1RKi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1de74e60-9bd4-41f5-a644-a075e69ee9f4_748x830.png "File:Statistical bias and statistical noise illustration.png - Wikimedia  Commons")





Let us give a concrete example to solidify these two concepts. Assume it is the beginning of the year 2028 and we want to predict the fraction of Americans who will vote Republican at the elections to be held at the end of that year. Let q be the fraction of Americans that will vote Republican in the 2028 elections. In mathematics, it is conventional to denote the estimate of a variable by putting a hat above the variable.

$`\begin{matrix} q & {= \text{fraction of Americans voting Republican in 2028}} \\ \hat{q} & {= \text{fraction of Americans estimated to be voting Republican in the 2028 election}} \end{matrix}`$

Let us assume that we use the following method to estimate q. We choose a hundred people from the country and ask them whom they are going to vote and then find out how much fraction in them tell that they will vote Republican, and give that as our estimate. By the important equation, we have :

$`\hat{q} = q + \text{bias} + \text{noise}`$

What would be the sources of bias and noise in this estimation algorithm?

**Sources of Noise** : When you ask only a hundred people out of a population of millions, if the sample you chose is not well mixed, then it might contain a more than actual share of Republican or Democrat voters. So, even without any bias, this sampling introduces noise in the estimation. If you choose a different hundred people, you will get a different answer to the estimate. But, if we apply this estimator many many times across many sample of many hundreds that run through all of the population (that is not feasible but assume hypothetically), you would on average, estimate correctly (assuming no bias) because you have covered the entire population by sampling many many times. You expect that the noise will reduce when we increase the sample size or when we randomise the samples more. Asking a ten thousand people random people instead of a carelessly chosen set of hundred people will give a better estimate of q with much less noise.

**Sources of bias** : Even if you sampled the entire population of the United States (which ensures zero noise) to estimate the percentage of Republican voters, there are still biases that prevent you from estimating q accurately. There are many sources of these biases. For example, some people might tell they are voting Republican in June 2028 but might change their mind and vote Democrat because of what the Republican candidate said in the gap. People also routinely lie about whom they will vote for depending on whom they believe would be the winner. Perhaps voters believe that pollsters are themselves likely to be Democrats and the voters want to please the pollsters. Hence, Republican voters report supporting the Democrat which leads the estimation to be biased in favour of the Democrats. Or maybe more of Democrat supporters who end up saying Republican on the poll end up not voting on the election day which also makes the poll to be biased towards Democrats.

How we can reduce bias and noise will be the focus of the rest of this article.

------------------------------------------------------------------------

# Sampling & Dealing with Noise



Assume for a moment that we have no bias in our estimator which means that on average across infinitely many samples, the estimator is accurate. But, we cannot average across many samples and want to be content with only the particular sample we have chosen for inference. In this case, we saw that due to noise induced by sampling, the estimate that we get is not consistent and may go this way or that way from the true value. If that is the case, we might have to give the range in which the actual values lie rather than giving a single value to quantify how bad the sampling induced noise is. For instance, in case of the exercise in the previous of estimating the fraction of Republican voters, instead of saying that the estimated value is 0.34, we can say that there is a 95% chance that the true value lies between 0.30 and 0.38. What measure can we use in order to build such confidence intervals?

![](https://substackcdn.com/image/fetch/$s_!ZrR0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F23cf8a8b-ed0a-42c0-80ec-4b3011d61990_2760x592.png)

Let us understand what noise is actually doing. What noise is doing is that as you select different samples from the population, it gives you different estimates. So, if we plot the values of the estimate across various samples, we will get a spread of values, as shown in the picture above. This distribution of estimated values is approximately centred about the average value (which is also the true value, if there is no bias). The problem is that we do not know where exactly our estimate with our sample has landed in this distribution of values. You never know if your particular sample is to the left or the right of the true value and by how much; although you can say that you are equally likely to be to the left as to the right.

In a previous section, we saw that the standard deviation of a set of values measures the spread of the distribution about its average. So, if we can somehow calculate the standard deviation of this spread, then we can say something about the average spread of the values. Turns out that it is possible to estimate (and many times, even give a formula for) this standard deviation without running across various samples. The exact details depend on the problem, but here let us try to do it only for this particular problem of estimating the fraction of Republican voters in the 2028 elections. I don’t want to give boring and technical derivations here, but in this polling example, if N is the number of individuals we have sampled, if q is the true value of the fraction of Republican voters, and if there are infinite individuals in the total population (this is a reasonable assumption actually; because the actual population is in practice much much larger compared to our sample size), the standard deviation of our estimates (assuming no bias) is given by the following expression

$`\sigma = \sqrt{\frac{q(1 - q)}{N}}`$

Although the actual formula for the standard deviation varies with each problem, we can learn some generic trends from this formula that holds for all situations. Let us first look at the denominator of the expression which is square root of N. The presence of square root of N in the denominator tells us that as our sample size N increases, the standard deviation goes down. Which means that as we sample more people, the spread in our estimate of q becomes lower and lower. The problem of noise comes from the fact that our sample might not accurately reflect the trends of the whole population; and hence if we sample more, it will more closely approximate the whole population. The formula here actually tells us something even more that holds across all estimation scenarios. It tells us that the standard error shrinks in proportion to the square root of the sample size N. Suppose the true proportion of Republican voters is q = 0.5 which makes the numerator 0.5. If we sample a 1,000 people, the standard error is approximately 0.016. When we sample 10,000 people, our standard error is 0.005. So, increasing the sample size tenfold from 1,000 to 10,000 has reduced the standard deviation to only threefold (0.016/0.005 = 3.2). If we increase the sample size another ten-fold to 100,000, we will only get another threefold improvement in standard deviation which is 0.0016. In other words, there are diminishing returns to bigger sample sizes. These generic trends hold true for any estimation problem in general.

Now, let us look at the numerator term where we have the square root of the product q(1-q). When q=0 and q=1, the term is zero and the standard deviation is zero. What does this mean? When the entire population votes fully Democrat (q= 0) or fully Republican (q = 1), then no matter how much ever people you sample and poll, you will find only entirely Democrat or entirely Republican samples and hence any sample will be perfectly reflective of the entire population. It is common sense that samples drawn from completely homogeneous population are perfectly representative of them because every person is the same as every other person, and hence even by analysing just one person, we can generalise it to the entire population. The product q(1-q) is zero when q = 0 or q = 1, and reaches its peak at q = 0.5. In this scenario, you have half of the population voting Democrat and half of the population voting Republican (50-50). This means that there are lots of both Democrats and Republicans and this provides more room for sampling error. You can easily find samples from this population that have all sorts of eccentricities ranging from 55-45 to 99-1. The closer the value of q is to one-half, more is the room for variation in sampling, and hence more is the standard deviation.

But, wait a minute; in order to calculate this standard deviation, I need to know the true value “q”. But, I do not know this “q” value beforehand and that is what I am trying to estimate (the sample size N is known beforehand). In practice, when the estimated value is close to the true value of q, one puts only the estimated value in the formula to quote standard deviations.

$`q \approx \hat{q}\operatorname{=>}\sigma \approx \sqrt{\frac{\hat{q}(1 - \hat{q})}{N}}`$

Note that this is only an approximation and carelessly applying this formula for very low sample sizes (when q is very far from q hat) can give us absurd answers. Suppose we sample only five people and found out all of them were voting Republican, then we would have a zero standard deviation from this approximate formula, and hence we will erroneously say that the entire population is fully Republican with a hundred percent confidence.

$`\hat{q} = 1\Rightarrow\sigma \approx 0`$

  
Although we saw formulae for this particular case, there are two generic results that hold across all estimation problems. Let us state them one by one without proof (the proof of these results are so technical that even undergraduate courses in mathematics and engineering skip it, so do not feel bad that you are not smart enough to understand it ! ).

> **Law of Large Numbers** : (Even if the total population is
> effectively infinite), as our sample size N increases, the noise
> essentially disappears (i.e. the sample based estimate hits the true
> value almost surely when there is no bias)!

We saw this in the poll example where the standard deviation drops to zero as N becomes large and the shrinkage is proportional to the square root of the sample size. Another important result upholds this trend in general and gives the shape of the distribution of the estimates and quantifies how fast the noise disappears with sampling size.

> **Central Limit Theorem** : For most populations, as the sample size N
> increases in an effectively infinite population (practically : N \> 30
> or so is a good range), the **sample average** (which here is the
> estimated value) is distributed symmetrically about the **true
> average** (which here is the true value of the average of the entire
> population, if there is no bias) in the following bell-shapes
> distribution curve below (called the **Gaussian distribution**) with a
> standard deviation that shrinks proportionally to the square root of
> N.
>
> $`\sigma_{N} \propto \frac{1}{\sqrt{N}}`$
>
> And more precisely,
>
> $`\sigma_{N} = \frac{\sigma}{\sqrt{N}}`$
>
> where σ is the proportionality constant and is related to the natural
> variation about the average that is present in the full population,
> which in the case of our poll example was √q(1-q).

The bell-shape of the Gaussian distribution is shown below.

[](https://substackcdn.com/image/fetch/$s_!8qPz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc16c433-0676-476b-bebb-da74dd933736_855x369.png)

![](https://substackcdn.com/image/fetch/$s_!8qPz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc16c433-0676-476b-bebb-da74dd933736_855x369.png)





What this shape tells us is as follows :

[](https://substackcdn.com/image/fetch/$s_!tmDS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9f5d308-df26-46f3-abb1-ebc97849531f_1288x620.png)

![](https://substackcdn.com/image/fetch/$s_!tmDS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9f5d308-df26-46f3-abb1-ebc97849531f_1288x620.png)





Statisticians call these probabilities as confidence intervals and this is a source of some confusion. Often, many casually say that we’re 95% confident that the true value lies within the 95% confidence interval, which is two standard deviations from either side of the average. But that’s not quite right and the correct statement is a lot more unaesthetic. Technically, we should say that :

> If there is no bias and if we repeated our estimator an infinite
> number of times across a variety of samples, the true value would be
> inside the 95% confidence interval 95 percent of the time.

------------------------------------------------------------------------

# Statistical Hypothesis Testing



Often, we believe that a certain hypothesis is true based on the data we have, and then want to be confident enough to reject as unlikely, the possibility of our data being generated under our hypothesis being false. In other words, we want to be confident enough to eliminate the possibility that the data supporting our hypothesis was generated by chance because we got lucky, despite the hypothesis being false. To do this, we enter into this area of statistics called **statistical** **hypothesis testing (SHT)**. In our poll example, assume that in the US elections, whoever crosses q = 0.5 wins the elections (it does not work that way at all, but just for simplicity). In that case, we would be interested in the hypothesis q \> 0.5 (the Republican party gets more than half of the votes and then wins). Assume that we took a poll surveying 1000 people and estimated that

$`\hat{q} = 0.532`$

We now would want to know how confident we can be in expecting that the Republicans will win the election. In hypothesis testing, we always start by setting up a **Null Hypothesis (H0)** that represents the "skeptical baseline" or the status quo we want to test against, and an **Alternative Hypothesis (H1)** that represents our expectations. In our case, we have :

H0 : The Republicans actually do not win the election (q \<= 0.5)  
H1 : The Republicans actually do win the election (q \> 0.5)

We want to see if our particular estimate from the data that we sampled is giving us enough evidence to confidently reject the skeptical null hypothesis in favour of the affirmative alternative.

Consider the borderline case when q = 0.5 that sits at the threshold between the null hypothesis and the alternate hypothesis. In this case, what are the chances that we observe a data with the sample fraction of Republicans being

$`\hat{q} = 0.532\text{~?}`$

In the case of q = 0.5, the standard deviation of the distribution of the estimates is

$`\sigma = \sqrt{\frac{q(1 - q)}{N}} = \frac{0.5}{\sqrt{1000}} \approx 0.016`$

Thanks to the Central Limit Theorem, we know that, 95 percent of the estimates lie within two standard deviations of the true value. Thus, we have that

$`\begin{array}{r} {\text{~95\% of the time :~}q - 2\sigma < \hat{q} < q + 2\sigma} \end{array}`$

Substituting q = 0.5 and sigma = 0.016, we have

$`\text{~95\% of the time :~}0.468 < \hat{q} < 0.532`$

Or in other words, 95% of the time, the estimates fall in the interval \[0.468, 0.532\]. In the remaining 5% of the time, the estimates fall beyond this interval range. But, even in this remaining 5% of the cases, the estimates will fall below 0.468 in half of the times. So, the chances that the estimate falls above 0.532 is actually only 2.5%. We did get an estimate of q^ = 0.532 which is in this 2.5% range of two standard deviations to the right of the mean 0.5. So, what do we have here now?

At the case of q = 0.5 when the Republicans will just begin to lose, the odds of getting our estimate q^ = 0.532 by sampling 1000 people is just 2.5% or 1 in 40 which is very slim (the odds are approximately as good as tossing a coin 5 times and getting all heads). So, we can be sure with 97.5% confidence that the Republicans will win the election if there are no biases. Because, in the case when the Republican voters are at a fraction 0.5, it is highly unlikely (just 2.5% chance) that we ended up with a sample of candidates with fraction of Republicans being 0.532 or higher. In the case when the Republican voters are at a fraction less than 0.5, it is even highly unlikely (less than 2.5%) that we ended up with a sample of candidates with fraction of Republicans being 0.532 or higher. What we have done above is a special case of a very popular and generic process called **statistical hypothesis testing**, whose generic scope and the steps involved are summarised below. Read the steps in the box below if you are more interested in how statistical hypothesis testing works in the generic scenario.

Suppose we want to investigate some unknown **parameter** called “**q**” of a large population using the information contained in a limited sample drawn from it. This parameter “q” may be the proportion of people supporting a political party (as in our example), the average income of a population, the effectiveness of a medicine, or the relationship between two variables, or even a collection of multiple numbers like the two coordinates of a point in a plane. We hypothesise that the parameter of a population satisfies some property. The following are the steps to be followed in statistical hypothesis testing to test if our hypothesised property regarding the parameter holds true for the actual population (e.g. in our poll scenario, we have to estimate the parameter q, and we hypothesise that q \> 0.5).

1.  Preparation of the two complementary hypothesis :  
    (i) The **Null** Hypothesis **H0** : Skeptical scenario which
    rejects the claimed hypothesis.  
    *In our poll scenario, the null hypothesis is q \< 0.5 which means
    the case that less than half of the population are Republican
    voters.*  
    (ii) The **Alternate** Hypothesis **Ha** : Expected Scenario that
    accepts that the claimed hypothesis   
    *In our poll scenario, the alternate hypothesis is q \> 0.5 which
    means the case that more than half of the population are Republican
    voters.*

    Note that these two hypotheses are constructed such that they are
    mutually exclusive and together exhaust all the possibilities for
    the parameters under consideration.

2.  Calculating the Test Statistic from Sample Data :   
    A **test statistic T(X_1, X_2, X_3, .. X_N)** is an expression that
    constructs a number based on the observations of the sample data
    X_1, X_2, X_3, … , X_N, that measures how incompatible the observed
    data is with the null hypothesis. That is, an increasing value of
    the test statistic T should mean that our hypothesis more likely to
    be true.  
    *In case of the poll example, the test statistic is the fraction of
    the voters in the sample of size N who say they would vote for the
    Republican party. That is :*

    $`T(X) = \frac{1}{N}\sum\limits_{i = 1}^{N}X_{i}`$

    *where*

    $`X_{i} = \left\{ \begin{matrix}
    0 & \text{if candidate i says he votes Democrat} \\
    1 & \text{if candidate i says he votes Republican}
    \end{matrix} \right.`$

    *This is a valid test statistic because higher the fraction of
    Republican voters in the sample, the more incompatible it is with
    the null hypothesis that there are lower Republican voters in the
    population.*

3.  Determining the Null Distribution(s) :   
    Under each value of the parameter in the null parameter space H0,
    the test statistic has a probability distribution. We want to know
    whether the observed value of the test statistic is unusually
    extreme under these distributions so that we can reject the null
    hypothesis confidently. If H0 has only one point, then determining
    the null distribution is easy ; simply substitute the one parameter
    of the null hypothesis in the probability expression. If it has many
    points, we have to account for all possible distributions allowed by
    all of these points.   
    *In case of the poll example,* *the null parameter space H0 is q \<=
    0.5 which does have infinitely many points.*

4.  Compute the p-value :   
    Among all possible distributions permitted by all the parameters in
    the null hypothesis H0, find the one under which obtaining a test
    statistic that is at least as extreme as the observed one, is the
    most probable. This maximum probability is called the **p-value**.
    Why the maximum? Because we want to determine how plausible our
    observations could be, even under the most favourable condition of
    parameters permitted by the null hypothesis.

    $`p:=\max\limits_{q \in H_{0}}P_{q}(T \geq T^{OBS}))`$

    Let us dissect this formula step by step. T ≥ T^{OBS} corresponds to
    the favourable event where the test statistic has a value that is
    greater than or equal to the observed test statistic (from the
    sample we actually observed). P_q (T≥ T^{OBS}) denotes the
    probability of this favourable event happening for a given value of
    the null parameter q. The test demands us to compute this
    probability of the favourable event for all possible values of the
    parameter q and take the maximum possible probability out of it.   
    *In case of the poll example, the null parameter space H0 is q \<=
    0.5 indeed has infinitely many points. But, we avoided working
    around with infinitely many distributions and computing a maximum
    over infinitely many values by an intelligent trick. The boundary is
    the point in H0 that is closest to our expected alternative
    hypothesis (e.g : q \> 0.5).   *

    $`p = \max\limits_{q \geq 0.5}P_{q}(\hat{q} \geq {\hat{q}}^{OBS}) = P_{q = 0.5}(\hat{q} \geq {\hat{q}}^{OBS} = 0.532)`$

    *where  *

    $`P_{q}\rightarrow\text{~Gaussian with mean q and s.d}\sqrt{\frac{q(1 - q)}{N}}`$

    *  
    By assuming the true value of q to be right at this tipping point
    (e.g. q = 0.5) at the boundary, we are holding our test to the
    toughest possible standard of skepticism. If we can prove that the
    fraction of Republican voters in our observed sample data (the
    observed T-statistic) is statistically too extreme to have come from
    the boundary (e.g. q = 0.5), then it is even more unlikely for it to
    have come from further inside of the null hypothesis (q \< 0.5)
    where more fraction of the actual population is made of Democrat
    voters. Therefore, rejecting the boundary confidently automatically
    also means that you are rejecting the entire set of values in the
    null hypothesis H0 even more confidently, as if q \< 0.5, it will
    throw out with even less chances, a sample with more fraction of
    Republican voters. This p value for the example turns out to be
    0.025 which is 2.5% by observing that when q = 0.5, the event q^ \>
    0.532 in the Gaussian curve is two standard deviations away from the
    mean to the right.*

5.  Make your decision using the significance level :   
    Compare the probability in the p-value (e.g. here 2.5%) for getting
    your data to a pre-chosen **significance level α**. If this p-value
    (even the maximum possible probability of observing a T-score that
    is at least as high as the observed one under the null hypothesis)
    is less than the significance level, then it means that your
    observed T-score is sufficiently improbable to occur under the null
    hypothesis.   
    *In our poll example, if you believe 2.5% is low enough a
    probability to reject as unlikely, then your data is rare enough to
    happen and hence you can confidently reject the null hypothesis to
    accept your alternative.*

Thus, hypothesis testing provides a way of concluding quantitatively that the pattern or result you have detected in your data set (from which you have made a conclusion) is sufficiently unlikely to have happened even under the best conditions of the null hypothesis. So, you can rule out confidently the null hypothesis and hence the data you have is likely to reflect a genuine case of your assumed hypothesis rather than getting fortunate with a lucky sample under the null hypothesis.

Now, what about the case when we have q^=0.52 (instead of the 0.532 that we already had). In this case, when we apply hypothesis testing, we find that 0.52 is approximately just one standard deviation away from 0.5 and hence the probability of observing value greater than it is 32% which is not low at all (compared to the 5% we had for two standard deviations). What do we do in this case? We are not confident to reject the skeptical null hypothesis, but that does not mean that our alternate is false either. In this case, statistical hypothesis testing enters into a sort of limbo where we are neither confident enough to reject the null hypothesis nor confident enough to accept our alternate hypothesis.

Now obviously, I have picked up the numbers in this example so that these computations can be easily done by hand but your laptop can run a simple program to compute these things for generic examples using the exact shape of the Gaussian curve. More technical details on this topic can be found in any basic statistics textbook. One common error that people make is to assume that the p-value tells you the probability that the null hypothesis is true. It doesn’t. It tells you the probability of getting a data as extreme as the one you got if the null were beginning to be true. Those two numbers are typically different.

Also, note that statistical hypothesis testing is all about probabilities. In our example, we have just a 2.5% chance of getting our kind of data that is favourable to us when our assumed hypothesis is false. While it is small enough for practical purposes to reject the null hypothesis, it is not absolutely zero. There is still a 2.5% chance that your assumed hypothesis is actually false, and luckily you just got data that is sufficiently favourable to your hypothesis, by ending up with a favourable sample. This scenario is called by many names in the statistics community that include **Type I Error**, **False Positive** (you conclude your hypothesis to be true even if it is actually false), or **Innocent Found Guilty** (in the legal parlance). On the other hand, if you decide that 2.5% chances (1 in 40) are not strong enough to be confident to reject the null hypothesis and if you hence reject your hypothesis, what this leads to is the opposite scenario which is that your original hypothesis that you assumed is actually true, but just that your sample data is not making you sufficiently confident enough to bravely accept the truth of your assumed hypothesis. So, you might end up unnecessarily rejecting the belief in the truth of your hypothesis in many legit cases when it is actually true. This type of error is called by many names in the statistics community that include **Type II Error**, **False Negative** (you reject your hypothesis to be false even if it is actually true), or **Guilty Declared Innocent** (in the legal parlance). We can see that there is a tradeoff to be made here between both the scenarios. If you are extremely skeptic and make the hypothesis testing so stringent that you demand a very low p-score to be confident (e.g. 2.5% is not enough, I need 0.000001%), then you will commit a lot of Type-II errors and end up increasing rejection of true cases, because you are not confident enough in your sample test. On the other hand, if you are extremely over-confident and make the hypothesis testing so lenient that you are confident with with high p-scores (e.g. 2.5% is not needed, 10% is enough), then you will commit a lot of Type-I errors by increasing the acceptance of false cases, because you trust your data too easily even when they are crappy. Being very stringent on SHT enables more of Type-II errors and being lenient on SHT enables more of Type-I errors. Balancing these cases depends entirely on the stakes at hand in your problem. For instance, in medical diagnosis, for some kind of diseases, a Type II error of missing the disease when there is actually disease, may be considered much worse; while in other kinds of diseases, a Type I error of falsely diagnosing a healthy patient may be considered much worse.

**Type I Error** : The hypothesis is actually false and our supporting data is a result of sampling chance but it is still accepted in the testing because we had a lenient test for statistical significance

**Type II Error** : The hypothesis is actually true but we have rejected it because testing from our data cannot eliminate the null hypothesis with a confidence margin that we expect

**Exercise** : If you are feeling very enthusiastic, solve this problem. You suspect that a coin used by your friend is unfair (i.e. it is biased towards giving more heads or tails). So, you toss it a hundred times and then observe that it shows heads 60 times (or the fraction of heads is 0.6). Use statistical hypothesis testing to determine whether you can confidently conclude that the coin is unfair, based on this data, and use an insignificance level of 1%. Let “q” be the true probability of your friend’s coin giving heads. The alternate hypothesis that you suspect here is that the coin is unfair (q ≠ 0.5) while the null hypothesis is that the coin is fair (q = 0.5). The test-statistic should measure how unfair the coin is based on the samples of tosses. So, since fair coins are expected to give half heads on tossing, you can use \|q - 0.5\| ; i.e. the magnitude of the deviation from 0.5) as a test statistic ; to suspect if a coin is unfair or not. The Central Limit Theorem implies that the distribution of the fraction of heads after tossing a fair coin “N” times (here N = 100) is Gaussian with mean “1/2” and variance “0.5/√N”. Note that this is almost the same as the polling problem ; the only difference here is that instead of Republican people, we are dealing with heady coins; and also here, deviations to the left and the right of 0.5 are both favourable for our alternate hypothesis under the null hypothesis (unlike in the poll case where only deviation to the right was favourable to our hypothesis of there being more Republicans). The situation is even simpler because the null hypothesis (the coin is fair) has only one value in the parameter space (q = 0.5).

------------------------------------------------------------------------

# Hypothesis Testing & Concluding Correlation



There are lot more important applications of hypothesis testing that cannot be covered here due to paucity of space, but there is one more application that I cannot leave out here, as it is central to the topics that we have discussed in the beginning. Consider the problem of correlation of two variables X and Y. We gave a formula to find the slope of the line of best fit from the data. Let us say that we did observe 100 data and found the slope of the line of best fit, and say it is some non-zero number called “c”. I told you that a non-zero value of the slope of the line of best fit means that the two variables are positively or negatively correlated in the data set. But, let us say that I now want to generalise and conclude that the two variables are indeed correlated for the whole population from which the data is sampled. How confident can I be in making this claim? We saw that when we sample some data from a huge population, the parameter that we end up concluding for the data need not be representative of the larger population. You might observe a positive or negative correlation in your data; but thay may be because of the eccentricities of the particular sample. In reality, there may be no correlation between the variables, and just that your limited sample size has some peculiarities. When can we be confident enough to confidently reject this possibility that your correlated sample was just a lucky draw from an actually uncorrelated population? This is again where hypothesis testing comes in.

Consider an application of the correlation between number of years in education (X) and income in USD (Y) of the population of the United States. We have sampled some people and have asked their years of education and incomes (x_i, y_i) and have found a positive correlation in the data; but, we want to know if there is an actually positive correlation between education and income for the entire population; not just for the data we sampled. This is very important in policy making because if there is indeed a positive correlation for sure, and later is also established to be causal, we would want to invest more on subsidising education to improve income. But, we do not want to waste government money on subsidising education if there is actually no correlation on the larger population. If our sampled data were (x_1, y_1), (x_2, y_2), (x_3, y_3), … , (x_N, y_N). Then, we saw in the beginning that the slope of the best-fit line (or regression line) is given by

$`\text{Slope of best fit line~}\hat{m}(X,Y):=\frac{cov(X,Y)}{\sigma_{X}^{2}} = \frac{\sum\limits_{i = 1}^{N}(x_{i} - \mu_{X})(y_{i} - \mu_{Y})}{\sum\limits_{i = 1}^{N}(x_{i} - \mu_{X})(x_{i} - \mu_{X})}`$

where

$`\begin{matrix} \mu_{X} & {:=\frac{1}{N}\sum\limits_{i = 1}^{N}x_{i}} \\ {\mu_{Y}:} & {= \frac{1}{N}\sum\limits_{i = 1}^{N}y_{i}} \end{matrix}`$

Note that I have put a hat for the “m” because this is the slope of the correlation that we estimated from the data that we have, and not the real slope of correlation for the entire population. Hence,

$`\begin{matrix} \hat{m} & {= \text{~estimated correlation slope from the sample}} \\ m & {= \text{~the actual correlation slope of the entire population}} \end{matrix}`$

Turns out that m^ that we computed in the above formula is indeed an unbiased estimate of the true slope m if the sampling is random (trust me on this) ; that is, as we estimate through many samples, it estimates correctly on average. But, sampling noise can corrupt it to drift here or there from the true m. That is, **even if the true slope were zero and income had no correlation with education, could the randomness of sampling have produced the positive slope in the data that we observed? Statistical hypothesis testing is designed to compute the probability of this event and eliminate this scenario if the chances are low enough.**

In hypothesis testing, we start by assuming the null hypothesis here that there is no actual correlation between education and income ; or numerically m = 0. We now want to know the distribution of the variable m^ when m = 0 and also its standard deviation. In the previous example, we wanted the distribution of q^ when q = 0.5. Since q^ was a sample average, the Central Limit Theorem helped us by telling that the distribution of any sample average is Gaussian, and we also gave without proof that the standard deviation is √q(1-q)/√N. I rationalised this formula although I did not derive it. Now, you similarly have to trust me on this that when the sample size is large, the distribution of the sample slopes can be computed, and hence the probability of obtaining a sample slope as extreme as the one that we have obtained for a data of size N can also be computed. If you obtain a small enough p-value and reject the null hypothesis, then you have statistically significant evidence that there is a relationship between income and education in the population.

**Important Statistical Fallacy Lesson** : Statistical hypothesis testing is so useful because we are bound to find patterns in our data that either do or do not reflect genuine relationships in the larger population. This is the nature of noise induced due to limited sampling from a very large population. So we need to check whether we have good reason to believe our findings aren’t just the result of accidents from our particular sample.

An interesting case ensues when we do have the samples for the entire population. Assume that we want to know the correlation between participating in sports and CGPA for students in a particular university. The number of students in a university are not that high and it is easy to convince the university to give data for this without affecting the privacy of the students involved. After doing so, let us say that we do find a correlation between student CGPA and participation in sports. Now the question is this : does statistical hypothesis testing still make sense? You might think no way at all, as we have data from the entire population, and there was no sampling involved. But, it turns out we can still ask the question as to whether this correlation between CGPA and sports activities is because of coincidence! Suppose that we cannot come up with any good reason to think there should be an on-average, some difference between the CGPAs of sports players and non-players in a university (maybe the admissions standards are the same for all students). But, there can be personal idiosyncratic differences between these particular set of sports and non-sports students in the university that makes their CGPAs different. To assess whether this observed correlation arose by coincidence or for a reason, we cant to collect more data. But, we already have all the data there is to have because we have information about all students of the university. But, statistics can still provide a useful way to think about whether an observed pattern was a coincidence or not, even if we have observed everything about the system. We can say that although we have data on all the actual students at the university, these actual students are just a small sample of a much larger **hypothetical population** of students that could have been at the university. If we make this assumption, we can start with the null hypothesis that the true correlation in that larger, hypothetical population is zero, and we can ask how likely it is that we would have observed a correlation at least as large as the one we observed among the actual students we have now, by chance. Of course, doing this requires a philosophical leap from actual populations to hypothetical populations. But, it is not that unreasonable to think that we are interested in the pattern that pertains to all sorts of students that can study at this university now (which is potentially infinite) rather than the small number that the university has admitted because of obvious constraints. If that is the case, taking this metaphysical leap to such hypothetical populations is actually useful because it can tell us if a pattern is truly generic enough even when it is stretched to this degree of generality.

------------------------------------------------------------------------

# Statistical Significance vs Importance



Is hypothesis testing then the gold standard of statistics? Is it enough to tackle everything? If yes, this article would end here, but unfortunately we have more to go. Although statistical significance is useful and informative, it is often misused and misunderstood. Often, we want to know two things about the relationships we discover from our data. They are :

1.  Is the relationship statistically significant? i.e. unlikely to have
    arisen by chance

2.  Is the relationship important ? i.e. if it matters or if it is
    valuable

These two questions are different actually. The former question is about statistical significance which is answered by hypothesis testing. The latter question actually is something about its importance that is based on the nature of the field and the context. A relation can be statistically very significant but not that important ; conversely, a relation can be very important but statistically not significant. For example, let us say that a cereal company has found a statistically significant relationship between TV advertisement budget and product sales. But, it does not automatically mean that the relationship is significant enough that the company invest a lot of money in TV advertisement rather than say newspaper advertisement or something entirely different like flavour enhancements. Just because a company has found from experiment that there is a negative correlation between the intake of the drug they discovered and blood pressure, does not mean that the medicine is a hit for high blood pressure. If it turns out for example that the allowable dosage of their drug can lower blood pressure only by 0.8 mmHg, it is useless as doctors know. The company can hype up the statistical significance of this drug and market it and push it with a deceptive headline like "*statistically well proven to lower blood pressure*" even though doctors wouldn't care about such a tiny decrease in pressure. When your sample size N is large enough (as it often is the case in digital tech, big data, and large clinical trials), your sampling error shrinks to almost nothing and hence hypothesis testing is extremely confident. This means that statistical hypothesis testings can detect microscopic differences that have zero practical uses. **The importance of a statistically significant relationship can only be answered with context and field knowledge in which the relationship is posed.**

Similarly, a relationship can be true and also be really significant and important, but it can happen that hypothesis testing cannot give us sufficient grounds to reject its null based on the given data. This happens when a real-world relationship or pattern is indeed massively important (and also turns out to be true), but because your data is limited (due to reasons like small sample size, high noise, or prohibitive costs for scaling the testing), your statistical test fails to clear the confidence threshold that you would like to have (like 1% or 2.5% or 5%). Statisticians then fail to reject the null hypothesis, not because the hypothesis is false, but because the data is not of sufficient quality or the confidence standards required are very high to entertain any risk of accepting a false hypothesis. This leads people to falsely conclude that “*there is no effect*” or “*there is no significant effect*” where statistical significance is again conflated with importance. Consider the case when a pharmaceutical company develops a breakthrough drug for an ultra-rare paediatric disorder that affects only some hundred children worldwide. The drug testing sees that it cures 12 out of the 15 children in the test group completely, while the untreated control group of 15 sees zero recovery. Because the total sample size is only N = 15, it is small and hence hypothesis testing yields a p-value that does not pass the p \< 0.05 test. Statistically, researchers must fail to reject the null hypothesis, and might even claim that the drug is still unproven to the standard of statistical significance required. But, in reality, the drug is most likely a miraculous, life-saving cure for a fatal disease. Relying strictly on the p-value would mean abandoning a monumental medical breakthrough simply because there aren’t enough patients in the world to satisfy the sample size requirements of a traditional hypothesis test. In this case, what we have is indeed a discovery of a very significant pattern of treatment with the new drug ; the problem is that its statistical significance is not yet to the standard we want. Strict statistical purists look at the results and declare "*the drug’s effect is not statistically significant; it could just be random economic fluctuation*". The drug then gets rejected, even though a it has proven to be life-saving on the trial patients, simply because the study lacked the statistical power (the number of affected patients to be sampled is too low) to prove it cleanly.

**Important Statistical Fallacy Lesson** : Thus, statistical hypothesis testing is not a holy grail ; not all discoveries that pass hypothesis testings are important breakthroughs ; not all discoveries that fail hypothesis testings are unimportant or false.

Many problems and ambiguities arise due to conflating statistical significance of a pattern vis-à-vis its importance. Again, this is like selecting the dependent variable problem. It is easy to understand that it is a mistake but occurs so common even among experts. In the remainder of this article, we will see more and more misuses of hypothesis testing.

------------------------------------------------------------------------

# Statistical Hacking : Over-Repeating & Under-Reporting



[](https://substackcdn.com/image/fetch/$s_!z9E-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6ffc29cb-efa1-4677-87c6-a4d7c79688fc_1000x960.png)

![](https://substackcdn.com/image/fetch/$s_!z9E-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6ffc29cb-efa1-4677-87c6-a4d7c79688fc_1000x960.png)





Paul, the Octopus choosing Spain over Germany for his 2010 semi-final prediction

Between 2008 and 2010, an octopus named Paul made sensational news for his apparent foresight in predicting the outcome of football matches. Before each match between nations, Paul’s caretakers would present him with two boxes of food, which were marked with the flags of each nation about to play the football match. Paul would eat first from one of the boxes, which apparently was his prediction for who would win the match. This octopus became a sensation in the media and predicted the outcomes of over 14 games in his career, out of which 12 turned out to be correct. Now, if you are like me and most other people, you would not believe that octopuses have special predictive powers, and would hypothesise that Paul was just predicting randomly and got lucky. Given that he predicted 12 out of 14 matches correctly, let us use statistical hypothesis testing to get the p-value of this data assuming the null hypothesis that Paul was choosing randomly. Assuming that Paul was choosing at random 14 times, we need to get the probability that he could get at least 12 of them correct. It is equivalent to tossing a fair coin 14 times and getting at least 12 heads because if Paul is choosing a winner randomly every time, and each team has an equally likely chance of winning, the probability of getting correct every time is half which is basically the probability of getting a head after tossing a fair coin (heads = predicting winner, tails = predicting loser). We can calculate the p-value of getting at least 12 heads in tossing a coin 14 times, and the answer turns out to be approximately 1 in 155. This is a very low chance and hence hypothesis testing says that we should be able to confidently reject the null hypothesis that Paul is guessing at random. But, does it mean that Paul has foresight of who will win football matches? Or have we made a mistake in formulating the test?

Let us now look at more information to see if we have been too generous to Paul. Paul lived in Germany, and 13 out of the 14 games which Paul predicted involved Germany as one of the national teams competing. Also, out of the 13 matches involving Germany, Paul chose Germany 11 times (means he had a tendency to pick Germany), and also Germany was very good at football (it won 9 out of those 13 matches). So, let us modify our null hypothesis somewhat in the light of this information. Paul is still assumed to be choosing randomly in the new null hypothesis, but in matches involving Germany, we now assume that he is biased to pick Germany with a probability 11/13, which indeed was the frequency with which Paul picked Germany (maybe Paul liked the German flag better for some reason because of the colours or the exposure). What is the new p-score now with these modified assumptions? The probability that Paul gets 11 or more games right out of the 13 times Germany played is now 0.03 which is approximately 1 in 33, which is still very unlikely (albeit being much more likely than the previous p-score of 1 in 155).

If you are still a skeptic like me and many other reasonable people, you will still not surrender and conclude that Paul indeed had magical powers. Consider this scenario that Paul is not the only octopus out there in Germany who could do this exercise. Maybe, there are 10 octopuses in Germany, and we hear only about Paul because he is the most successful one. Then, assuming we have ten octopuses doing this, what are the odds that at least one of them would get this lucky (and hence become famous like Paul). The odds that one octopus could make predictions that are at least as extreme as that of Paul’s is 0.03 ; but if there are ten octopuses predicting independently, the probability that at least one of them gets this much lucky in its prediction would be easy to calculate ; let me give an easy and intuitive derivation to calculate the expression.

We know that 0.03 as the chance of each octopus becoming successful like Paul. When an octopus is not able to have the success rate at least as much as Paul, we say that it has failed. This means that the probability of each octopus failing is (1-0.03). The probability of all octopuses failing when they are acting independently is simply the product of the probabilities of each of them failing which is hence :

$`(1 - 0.03)(1 - 0.03)\ldots(1 - 0.03) = (1 - 0.03)^{10}`$

Now, the event that we are interested here is the case when at least one octopus succeeds. But, the only way this event can be prevented to happen is by all octopuses failing. So, the two events

1.  E1 : All octopuses fail

2.  E2 : At least one octopus succeeds

are complementary. That is, together they exhaust all possible scenarios (either all fail OR at least one works) and they cannot be true simultaneously (we cannot have that all are failing if at least one of them is succeeding). For such complementary events, their probabilities add up to 1.

$`P(E_{1}) + P(E_{2}) = 1\Longrightarrow P(E_{2}) = 1 - P(E_{1})`$

So, the probability of the second event is 1 minus the probability of the first event. But, the probability of all the octopuses failing was already computed as :

$`P(E_{1}) = (1 - 0.03)^{10}`$

Hence, the probability of at least one octopus being successful like Paul is given by :

$`(1 - (1 - 0.03)^{10}) \approx 0.26`$

In other words, if there are 10 German octopuses that went through the same ridiculous exercise like Paul, the odds that at least one of them would have a record of predictive accuracy at least like that of Paul’s is approximately 1 in 4, which is very much plausible by chance. If we increase the number of octopuses to 20 instead of 100, we would have an even more success rate of getting at least one success which is

$`(1 - (1 - 0.03)^{20}) \approx 0.4562`$

basically 1 in 2 odds. As the number of octopuses becomes very large, what happens? Since (1-0.03) is less than 1, when powered with a very large number, rapidly falls to zero. Hence (1-0.03)^N falls to a very small value for even a moderately large N. Thus, the probability of getting at least one octopus that is at least as successful like Paul approaches 1 as the number of octopuses becomes even moderately large. Mathematically, we say

$`\lim\limits_{N\rightarrow\infty}(1 - (1 - 0.03)^{N}) = 1`$

This holds true for not just 0.03 but for any number that is strictly between 0 and 1.

$`\lim\limits_{N\rightarrow\infty}(1 - (1 - p)^{N}) = 1\mspace{1895mu}\forall\mspace{1263mu} 0 < p \leq 1`$

We do not know exactly how many other German octopuses were in this football forecasting business. But, we do know for sure that lot more animals like Leon the Porcupine, Petty the Hippopotamus, Anton the Tamarin, and Mani the Parakeet made it to the news; and hence we can be sure that there were many other unnamed animals who were tested for this business, but eventually lost out because they turned out unsuccessful. What this says is that if enough people repeat the same action, one of them is bound to get something statistically improbable. Viewed in isolation, it might seem like he has superpowers or he got very lucky or he is particularly skilled ; but when viewed in the larger context of repetitions, such rare events are bound to happen to someone or the other once in a while. **When we focus only on those rare instances of success and neglect all the many other instances where their same actions were repeated in vain, statistical hypothesis testing leads to extremely ridiculous beliefs and conclusions** like Paul the Octopus can predict the outcomes of football matches,

What then should we make of statistical hypothesis testing? It is indeed genuinely useful to evaluate the odds of the patters observed in data being produced by chance. But, the case of Paul the Octopus clearly shows that when we repeat an experiment many times and select only one statistically significant result from those trials for publication or attention or evaluation, it is highly misleading ; that one extreme result, when viewed in isolation, seems to be extremely unlikely and hence statistically very significant; but in the larger context of multiple repetitions, it is actually very plausible to have happened by chance.

**Important Statistical Fallacy Lesson** : If we base our beliefs purely on what gets reported or published or made available to be known, then we will end up with extremely misguided beliefs. Making a lot of trials (**over-repeating**), while selectively reporting only the few interesting or statistically significant ones (**under-reporting**) is a dangerous combination and a serious statistical fallacy. But, like all other fallacies we have seen so far, it is also extremely widespread. And because of it, when we hear about a new, exciting result or phenomenon or even a claimed scientific discovery, it is much harder to know how likely it is to reflect a genuine phenomenon than the naive logic of hypothesis testing in isolation suggests. So, whenever we see claims of a statistically significant result, we should not hurry until we replicate it a lot of times and are confident that it is not a one-off event.

This happens more than we think in the scientific community ; either intentionally or unintentionally. A scientist conducts an experiment hoping to collect statistically significant data that verifies his hypothesis. But, let us say that he does not get the desired result the first time he conducts the experiment. Instead of giving up on his hypothesis, he might think that something was wrong in his experiment and hence slightly tweaks it and performs it again. Upto this point, it looks very innocent and a genuine quest for the truth. But, when the scientist repeats the experiment many times after repeated tweaks and suddenly gets a statistically significant result once, he can never be sure if that statistically significant result was because of the tweaks he performed, or because of chance; as happened with Paul the Octopus. Instead of repeating it further and checking, the scientist, may either due to haste, or intentionally, choose to publish about that statistically significant result (which was actually because of chance) without bothering to repeat and replicate it further to confirm it. The scientific community calls the behaviour of playing around with the data or tests, until a p-value below a particular threshold emerges by chance with the term **p-hacking**. Another way it can happen is in the medical field which can be visualised by considering the case when a new pill for curing a disease has been prescribed for trial to verify its efficacy. You may test it on a large group and see if the pill has a statistically significant effect on a variety of outcomes - mortality, heart attacks, strokes, cholestrol, days of hospitalisation. But, if you have a list of outcomes that is too large, you will end up getting a statistically significant result on just one or a few of them simply due to noise. If you are not statistically literate or lack proper ethics, you would report the statistical significance on only that one particular outcome and aggressively use that for marketing and convincing doctors.

Sometimes, p-hacking can happen even when all the parties are acting ethically. Assume that there are thirty labs across the world that are operating independently and testing the efficacy of a particular drug for curing cancer. In reality, the drug is a sham and it does not work at all. Twenty-nine of the labs find no statistically significant evidence for the efficacy of the drug for cancer, and hence conclude that the drug does not work. They do not publish it because obviously news like “*another drug XXX cannot cure cancer*” neither make for papers in journals nor make catchy headlines. These labs do not even bother to write about this negative finding anywhere and move on to another area of research, and hence no one knows about these twenty-nine failed trials. But, let us say that one lucky lab out of those thirty find a statistically significant evidence regarding the drug’s efficacy. We now know that it is due to sheer chance for reasons having nothing to do with the drug, but everything to do with brutal repetition that forces rare events to happen. So, as far as this group of scientists in this lab is concerned, they are the only people who thought of testing this drug for cancer ; and hence all available evidence points to the fact that it does work. So everyone believes this result even though it is in fact completely wrong, and if we had access to all the data (from the twenty-nine other failed experiments from the other labs), we would see that the bulk of evidence actually points in exactly the opposite direction. There was no p-hacking and every party acted ethically. It is just that publication mechanisms we have today screens out studies that are unsuccessful while favouring only those that are statistically significant. This phenomenon is called as p-screening where the bulk of statistically insignificant results are not made known at all.

So, like Satan, **statistical hacking** can take many different forms, and one has to work hard to avoid it either unintentionally or intentionally, whether one is as an expert or one is an ordinary consumer of data. Because of p-screening, the scientific record itself can be unreliable even when everyone behaves just as they should. Once you start looking out for this phenomenon, you again see it everywhere. There are lots of ways to mitigate statistical hacking, some of which are :

1.  **Reducing the insignificance threshold** : We can be more stringent
    and say that we will accept only those studies that pass an
    extremely low threshold of significance (say p \< 0.005). It would
    certainly make it harder for p-hacking or p-screening, but it comes
    at the cost of creating two problems. First, because it ends up
    making statistically significant results much rarer, it ends up
    making them more valuable when they do happen (one can always
    increase N large enough). Also, it ends up rejecting many genuine
    cases of actually significant discoveries (type II errors).

2.  **Adjusting for multiple testing** : We can make it mandatory that
    when multiple tests or experiments are conducted, the p-value should
    be adjusted. If “p” is the p-score of a single trial and there are N
    trails, the new p-score should be   

    $`(1 - (1 - p)^{N})`$

    But, this only works if the tests are independent and this also will
    not prevent unintentional trials that happen due to screening.

3.  **Integration** : We should realise that statistical hypothesis
    testing can always be abused. It is not the only way of assessing
    the believability of a finding ; statistics is a tool and cannot be
    a substitute for clear thinking ; and we have to incorporate
    evidence with field knowledge and context, in order to think clearly
    about what our beliefs should be after seeing some new evidence.

4.  **Pre-Registration of tests** : To avoid the problem of
    under-reporting, the practice of pre-registering one’s experiment
    before performing it and gathering data can be followed, and this is
    especially used in drug trials, where a company that has invested a
    lot in a new drug might be tempted to search over lots of
    specifications, subgroups of people or diseases, or outcomes, until
    they find something that suggests the drug is efficacious for a
    particular outcome on a particular group of people.

5.  **Replication of tests** : Since repeating an experiment lot of
    times can result in a statistically significant result occurring
    once by fluke, one way to ensure that a result is not by chance
    would be to replicate it a lot of times and see if we get the same
    result every time. This is a standard practice in the hard sciences;
    and there are lots of cases of papers getting rejected because its
    results can’t be replicated by others. But, sometimes replication is
    not feasible as the data and study would pertain to a one-off event.

6.  **Fields without this problem** : If you come to know about a study
    that would have never been published, if the researchers had found
    the opposite of what they found (because then it would be something
    ordinary), you should be worried about p-hacking. But if a study
    answers a question for which both an affirmative and negative answer
    to the concerned hypothesis are novel, these problems disappear.
    Many problems in the hard sciences fall in this category ; for e.g.,
    testing whether a newly discovered particle has mass, or whether
    ratio is a constant independent of a certain other variables,
    whether a fossil specimen belongs to a known or a brand-new hominid
    species - in all of these problems, either scenario is a very
    informative answer that points to discovery of something new and
    hence would get published. Hence, in such fields, there is neither
    an incentive for researchers to engage in p-hacking nor is
    p-screening possible because tests that give both answers would be
    published as significant findings.

As pointed out, statistics is just a tool, and is not a substitute for clear thinking and reasoning. No wonder quotes like “***There are three kinds of lies: lies, damned lies, and statistics***” (Mark Twain), ***“It is easy to lie with statistics, but it is easier to lie without them***” (Frederick Mosteller), “**If you torture the data long enough, it will confess to anything**” (Ronald Coase), and “**Statistics like bikinis: what they reveal is suggestive, but what they conceal is vital**” (Aaron Levenstein) abound. Now, you also might have gotten why there are book titles like “**How to Lie with Statistics**” by Darrell Huff.

------------------------------------------------------------------------

The link to the second article in this series is below where I will be focusing on causation.

[](https://ramaseshanchandrasekaran.substack.com/p/statistical-reasoning-statistical-778)

## Statistical Reasoning, Statistical Fallacies & Seeing Through the Noise : Part 2 - Causation

[Rama Seshan Chandrasekaran](https://substack.com/profile/195425058-rama-seshan-chandrasekaran)

·

Nov 9

![Statistical Reasoning, Statistical Fallacies & Seeing Through the Noise : Part 2 - Causation](https://substackcdn.com/image/fetch/$s_!12i_!,w_1300,h_650,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb4fe9cac-acd0-4a23-a3fa-7b140193446e_500x670.jpeg)

In the previous article in this series, we saw about establishing the relationship between two features of the world and finding it when it is known to exist. We also saw how noise affects our estimate of the relationship, and also how to use (and not misuse) statistical hypothesis testing to determine the statistical significance of a relationship disc…

[](https://ramaseshanchandrasekaran.substack.com/p/statistical-reasoning-statistical-778)

Read full story

Meanwhile. if you are interested in knowing about more articles I write, refer here. I write on both STEM and the humanities topics that interest me.

[](https://ramaseshanchandrasekaran.substack.com/p/master-post-post-of-posts)

## Master Post - Post of posts

[Rama Seshan Chandrasekaran](https://substack.com/profile/195425058-rama-seshan-chandrasekaran)

·

September 25, 2025

Here, I update the list of all my posts on Substack topicwise

[](https://ramaseshanchandrasekaran.substack.com/p/master-post-post-of-posts)

Read full story

------------------------------------------------------------------------

#### Subscribe to Rama’s Substack

By Rama Seshan Chandrasekaran · Launched a year ago

My personal Substack

Subscribe

By subscribing, you agree to Substack's [Terms of Use](https://substack.com/tos), and acknowledge its [Information Collection Notice](https://substack.com/ccpa#personal-data-collected) and [Privacy Policy](https://substack.com/privacy).

[](https://substack.com/profile/195425058-rama-seshan-chandrasekaran)

![Rama Seshan Chandrasekaran's avatar](https://substackcdn.com/image/fetch/$s_!ZHOm!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11e50d60-b811-4831-8bbc-4d320762e60b_96x96.png)

[](https://substack.com/profile/373290025-malayali-hindutva-vicharak)

![Malayali Hindutva Vicharak's avatar](https://substackcdn.com/image/fetch/$s_!l_nH!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F42504e9e-0ebd-4f41-a376-2cc1baff5729_509x509.png)

[](https://substack.com/profile/284920280-ravinder-reddy)

![Ravinder Reddy's avatar](https://substackcdn.com/image/fetch/$s_!2Tvm!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F77da9531-28fb-41f8-b757-599e5b73f4c6_1202x1204.png)

[](https://substack.com/profile/514546062-m-siddhartha)

![M Siddhartha's avatar](https://substackcdn.com/image/fetch/$s_!H3lT!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb79c52b9-8e31-438c-bcb7-b498e9a6819b_96x96.png)

[](https://substack.com/profile/4344917-jablonski)

![Jablonski's avatar](https://substackcdn.com/image/fetch/$s_!y9nh!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdfd6293f-e320-4c36-afd9-2bb35b18d1bc_144x144.png)

20 Likes∙

[5 Restacks](https://substack.com/note/p-223430402/restacks?utm_source=substack&utm_content=facepile-restacks)



20





5

Share
