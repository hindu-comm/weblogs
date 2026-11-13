+++
title = "Statistical Reasoning,"
full_title = "Statistical Reasoning, Statistical Fallacies & Seeing Through the Noise Part 2 Causation"
upstream_url = "https://ramaseshanchandrasekaran.substack.com/p/statistical-reasoning-statistical-778"
date = "2026-11-09"
+++
Source: [here](https://ramaseshanchandrasekaran.substack.com/p/statistical-reasoning-statistical-778).

Statistical Reasoning, Statistical Fallacies & Seeing Through the Noise : Part 2 - Causation



![User's avatar](https://substackcdn.com/image/fetch/$s_!ZHOm!,w_64,h_64,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11e50d60-b811-4831-8bbc-4d320762e60b_96x96.png)

Discover more from Rama’s Substack

My personal Substack

Over 2,000 subscribers

Subscribe

By subscribing, you agree to Substack's [Terms of Use](https://substack.com/tos), and acknowledge its [Information Collection Notice](https://substack.com/ccpa#personal-data-collected) and [Privacy Policy](https://substack.com/privacy).

Already have an account? Sign in

# Statistical Reasoning, Statistical Fallacies & Seeing Through the Noise : Part 2 - Causation

### This series of three articles gives an accessible introduction to the tools of statistical reasoning, common statistical fallacies, and related philosophical problems without much math

[](https://substack.com/@ramaseshanc)

![Rama Seshan Chandrasekaran's avatar](https://substackcdn.com/image/fetch/$s_!ZHOm!,w_36,h_36,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11e50d60-b811-4831-8bbc-4d320762e60b_96x96.png)

[Rama Seshan Chandrasekaran](https://substack.com/@ramaseshanc)

Nov 09, 2026



6





3

Share

In the previous article in this series, we saw about establishing the relationship between two features of the world and finding it when it is known to exist. We also saw how noise affects our estimate of the relationship, and also how to use (and not misuse) statistical hypothesis testing to determine the statistical significance of a relationship discovered from data. If you want to read that first article, click below; but this article can also be read as a standalone piece.

[](https://ramaseshanchandrasekaran.substack.com/p/statistical-reasoning-statistical)

![Statistical Reasoning, Statistical Fallacies & Seeing Through the Noise : Part 1 - Correlation](https://substackcdn.com/image/fetch/$s_!Z3LL!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F86f34be8-c8fc-412b-92ea-96b9d5ef0560_1076x664.png)

#### Statistical Reasoning, Statistical Fallacies & Seeing Through the Noise : Part 1 - Correlation

[Rama Seshan Chandrasekaran](https://substack.com/profile/195425058-rama-seshan-chandrasekaran)

·

Nov 6

[](https://ramaseshanchandrasekaran.substack.com/p/statistical-reasoning-statistical)

Read full story

------------------------------------------------------------------------

# Defining Causation : The Philosophical Problem



[](https://substackcdn.com/image/fetch/$s_!12i_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb4fe9cac-acd0-4a23-a3fa-7b140193446e_500x670.jpeg)

![dominoes](https://substackcdn.com/image/fetch/$s_!12i_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb4fe9cac-acd0-4a23-a3fa-7b140193446e_500x670.jpeg "dominoes")





Although this is an article about statistics and mathematics, it is essential to get acquainted into the basics of the philosophical issues behind defining causation, because that will impact the mathematics through which we establish it. We use the word “cause” very abundantly in our daily course as though we understand it precisely. We make statements like “*smoking causes cancer*”, “*burning fossil fuels cause global warming*”, “*increasing taxes would cause reduction in GDP*”, and “*industrialisation caused the population movement from villages to citie*s”. But, behind this word lies a metaphysical leap that we hardly think about. Let us say that you ate some pasta at a restaurant and your stomach started aching afterwards. You suspect that the restaurant pasta that you ate caused your stomach ache. What do you exactly mean when you claim that the restaurant pasta caused the stomach ache? Turns out, what you mean is something like this : Imagine a hypothetical scenario where everything about the world remains the same except that : at the point you were about to eat the pasta, you changed your mind in the hypothetical world, and did not consume it. Then, your causal claim means that in this counterfactual scenario, you would not have got the stomach ache later. The comparison of outcomes in such a thought experiment is called a counterfactual comparison. Whenever you make a causal claim, you are comparing between the outcome in the actual world and another outcome that would have happened in a hypothetical world. You claim that the outcomes in the actual world and the counterfactual world are different in the scenario where everything is identical between those two worlds, up until the point where the feature that is claimed to have caused the event is made different between these two worlds . This idea of counterfactuals is actually philosophically deep and subtle, and hence to ensure that we are on the same page, I am going to introduce some notation for the rest of this article.

Assume that an event X causes another event Y to happen. For simplicity, let us begin with the assumption that X is a discrete event which means that there are only two possibilities : it either happened or did not happen. Hence, the causal factor variable can take only two values which are denoted by 0 (the event X did not happen) and 1 (the event X did happen). Then, we have :

> Y₁ = outcome with X = 1 (X happened)  
> Y₀ = outcome with X = 0 (X did not happen)
>
> Causal effect   
> = **Y₁** - Y₀   
> = Y₁ - **Y₀**

The causal claim is the claim that there is a significant difference between Y₁ and Y₀. But, note that in the actual world out there, you only observe one of these two things, while the other remains hypothetical and strictly unobservable. In reality, you either ate the pasta or did not eat the pasta. So, you either observe only Y₁ or only Y₀. The observed variable is shaded in green and the hypothetical variable is shaded in red. So, strictly speaking, causation, which is the difference between one observable variable and another unobservable variable, is hence unobservable no matter what. This is called by many names by philosophers, and here I use the term “***the fundamental problem of causal inference**”*. So, given this seemingly hopeless situation, how do we make progress on answering causal questions, if we can never access the counterfactual variable required for establishing causation? Before we proceed to answer this question in the next section, let us explore more philosophical problems that plague us once we start thinking about hypothetical worlds.

Often, we ask innocent questions like “*what caused this particular event*?” and expect an answer. For example, it is a common historical claim that the assassination of Archduke Ferdinand (the heir to the throne of Austro-Hungarian empire) in 1914 by Serbian assassins caused the First World War. This seems to make sense in a simplistic scenario ; because it is easy to imagine that had he not been assassinated, then the chain of events leading to the war would not have happened. But, just because of this reasoning, can we say that this assassination was “**the**” cause of the war? Surely, we can see that there are many other factors which would have prevented the war if they had been different in the counterfactual world. If the Austro-Hungarian empire had not annexed Bosnia and Herzegovina in 1908, then the Serbian assassins would have never killed Ferdinand. If the Serbian government had accepted the demands placed by Austria-Hungary after the assassination, then also the war could have been prevented despite the assassination. There are lots of hypothetical worlds in which World War I would not have happened ; imagine a world where the meteorite that caused the extinction of dinosaurs was bigger and made the entire earth bereft of any human life. Then, in such a world as well, the war would not have happened because there would be no humans in the first place. Once we are obsessed with counterfactuals, it looks like an event can have and typically has several causes, and hence we are interested in “the” cause(s) of it. Of course, it is obvious that some causes are more proximate and immediate than others ; for instance, it is obvious that the Big Bang and the meteorites that caused the extinction of dinosaurs are hardly proximate causes for the world wars. But, how exactly to determine proximity in a universal and principled manner, when we compare hypothetical worlds? Many historians have argued that early twentieth century military doctrines and national alliances were “the” causes of the First World War, and because of them, the war would have happened, even if Ferdinand was not assassinated (these historians argue that his assassination was just one of the mechanisms through which the war was triggered, and it was inevitable to happen via some means or the other, simply as a consequence of early 20th century military doctrines and national alliances). In this case, what is (are) the most proximal set of caus(es)? The assassination of Ferdinand or the combination of military doctrines plus national alliances at the beginning of the 20th century? Another problem is that events can have two or more equally proximal causes. Let us say that two people take guns and simultaneously shoot a guy dead. The two people can argue that they did not cause the death of that guy because each person can argue that whether he took the gun and shot or not, the guy would have been dead anyways, because the other guy was shooting. Of course, this would not fly in court, because the two people both caused the death of the guy they shot with equal proximity. The philosophical problems implied by these thought experiments tell us that causation is much more complex than we think in everyday life.

There are also other philosophical issues while thinking about causation. We always believe that causation runs forward in time. If an event X causes another event Y, then Y should always happen after X happens. In fact, one way to prove (at least in the court of law) that an event X did not cause event Y, is by establishing that X happened after Y happened. But, let us think of some scenario where this intuition also is not exactly valid. Assume that it is going to be your fiftieth birthday this year, and you will have your friends sending you birthday cards or wishes. All these cards tend to arrive in the few days before your birthday (there are more birthday cards mailed to you in the week leading up to your birthday than in any other days of the year). Assuming that this correlation is causation (for now intuitively), it looks like your birthday cards are coming before your birthday. So, it looks like the arrival of your birthday cards is causing your birthday, if we strictly assume that causes precede effects. But, this does not make any sense here, because your birthday is bound to occur on that day whether you get cards or not, and it is your birthday that causes the cards to arrive before it. Does this mean that causation can work backward in time? You might argue in many ways against a backward-in-time causation. You might say that it is not your upcoming birthday that is causing the arrival of cards, but the belief in the people’s minds that your birthday is upcoming. If your friends believe that your birthday is occurring on some other day for some reason, then they will send cards before that day. But again, what causes the belief of your friends about your correct birthday? Turns out the answer is that because you were born in so and so date fifty years ago. So, it looks like your birth fifty years ago is the most proximal cause of the this arrival of cards, if you have to preserve causation as strictly forward in time. These philosophical issues regarding causation are still deep and many remain still debated. but I just wanted to slightly whet your appetite in this so that it will motivate you when we proceed to the mathematical side of things in the next section. To read more on these philosophical issues, I highly recommend this book to you, which is very compact and also lead you to many more resources.

[](https://substackcdn.com/image/fetch/$s_!fGPu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa63d59e2-89fd-4b26-b573-9f656a70193c_967x1500.jpeg)

![](https://substackcdn.com/image/fetch/$s_!fGPu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa63d59e2-89fd-4b26-b573-9f656a70193c_967x1500.jpeg)





------------------------------------------------------------------------

# When Correlation = Causation : Randomised Control Trials



You must have heard the famous adage that “***correlation does not imply causation***”. What you might not have heard is also the equally true but less well-known fact that “***causation does not imply correlation***” (we will see about this in a future section of this article). In this section, we will see how correlation and causation are related, and how one does not always lead to another, after establishing a mathematical framework to talk about causation. We will also see about one particular situation where correlation and causation are identical ; which is the case of randomised controlled trials that are important in drug testing.

[](https://substackcdn.com/image/fetch/$s_!IiQR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fefd3d828-82e7-4afe-8b09-51669325afcc_1920x1118.jpeg)

![Randomized Control Trial (RCT) - Simply Psychology](https://substackcdn.com/image/fetch/$s_!IiQR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fefd3d828-82e7-4afe-8b09-51669325afcc_1920x1118.jpeg "Randomized Control Trial (RCT) - Simply Psychology")





Let us first start with the classic case of a drug trial in medical research. As seen in the previous section, one can never observe or determine or establish causation on an individual basis because one of the terms in the causal claim is hypothetical and always unobservable. So, one can never prove that you eating pasta at that restaurant caused your stomach ache, or that you taking this drug will cause recovery from a particular disease. But, drug testers and pharmaceutical researchers are not interested in causal efficacies of drugs on an individual basis, but on the average causal efficacies on drugs for a large group of population. So, let us shift the discourse from the individual scenario to the group scenario to put causation on an empirical footing.

In reality, an individual person or case study or agent either had the event or did not have the event. So, let us assume that we want to determine the average effect of an event X on event Y on a group of people or agents. In reality, some people experience the event X and others do not experience X. So, let us split the population into two categories :

1.  **Treated** **Group** (for whom X = 1) : denoted by the subscript
    **T**

2.  **Untreated** **Group** (for whom X = 0) : denoted by the subscript
    **U**

The terminology is inspired from the case of a drug trial and related health scenarios, where the people in the treated group get the drug or food that is being tested, while the people in the untreated group do not get the drug or food that is being tested. But, it can hold true for any scenario. The untreated group is also called the **control** group in medical terminology who are given a placebo of the drug being tested. Assume that the number of individuals is the same in both the groups, just for mathematical simplicity (we will tell what happens when this is not the case ; it is just a minor adjustment). Let Y denote the outcome for each group - treated vs untreated. Now, we have four scenarios that are described below.

![](https://substackcdn.com/image/fetch/$s_!JHzN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe55c1d38-79ca-470b-be05-fa2f3ceba63d_1472x326.png)

> **Y^(U)₀** : average outcome for the untreated group without
> treatment  
> **Y^(T)₀** : average outcome for the treated group without treatment  
> **Y^(U)₁** : average outcome for the untreated group with treatment  
> **Y^(T)₁** : average outcome for the treated group with treatment

In reality, we observe only two of the four variables. The average outcome for the treated group with treatment, and the average outcome for the untreated group without treatment (shaded green). We never observe the hypothetical scenarios of what would have happened if the treated group were not treated and if the untreated group were treated (shaded red).

What we observe is this correlation :

> **Observed Correlation = Y^(T)₁** - **Y^(U)₀** = average difference in
> outcomes due to treatment between treated group and untreated group

But, this is not equal to the causal efficacy that we want to find. The causal efficacies that we are interested in are :

> **Y^(T)₁** - **Y^(T)₀** = average effect of the treatment on the
> treated group = **AT**  
> **Y^(U)₁** - **Y^(U)₀** = average effect of the treatment on the
> untreated group = **AU**
>
> The average of these two effects would be the causal difference in
> outcomes in the entire population, half of which is treated and half
> of which is untreated.
>
> **Average causal effect of treatment** of the entire group = 1/2
> (**Y^(T)₁** - **Y^(T)₀** ) + 1/2 (**Y^(U)₁** - **Y^(U)₀**) = 1/2 AT +
> 1/2 AU
>
> **Note** : The average effect of treatment on the entire population
> (treated + untreated) is the average of AT and AU assuming they are
> equal in number (otherwise the two 1/2 would be replaced by their
> appropriate proportions in the population and this is called a
> weighted average).

But, we cannot measure this average causal efficacy of treatment on the population, because they involve hypothetical and unobserved variables. For observing the average effect of the treatment on the treated group (AT), we have to compare the difference in outcomes in the same treated group with treatment and without treatment ; this is impossible as the same person in the same group can either have treatment or not have treatment, and not both. Similarly, for observing the average effect of the treatment on the untreated group (AU), we have to compare the difference in outcomes in the same untreated group with treatment and without treatment which is impossible as the same person can either have treatment or not have treatment. The average effect of treatment on the entire population (treated + untreated) is the average of AT and AU assuming they are equal in number (otherwise the two 1/2 would be replaced by their appropriate proportions in the population).

Ideally, we would like to see how the event X affects the same group of people. But, the same group cannot both have the treatment and not have the treatment. Let us see how the observed correlation between treated group with treatment and the untreated group without treatment is related to the causal efficacies AT and AU that we want to compute.

> Observed Correlation = (**Y^(T)₁** - **Y^(U)₀**) = (**Y^(T)₁**
> -**Y^(T)₀**) + (**Y^(T)₀** - **Y^(U)₀**)

The latter term is obtained by adding and subtracting the number **Y^(T)₀** in the expression. But, the first difference term in the expression in the right hand side is nothing but the causal AT term (average effect of the treatment on the treated). So, we get

> Observed Correlation = (**Y^(T)₁** -**Y^(T)₀**) + (**Y^(T)₀** -
> **Y^(U)₀**) = Causal AT term + Bias^(AT) term

We see that the observed correlation is made up of two terms : the first term is the causal AT term that we want, and the other term is a bias term that comes after the AT expression and hence I have called it Bias^(AT). We can also write the observed correlation in another way as :

> Observed Correlation = (**Y^(T)₁** - **Y^(U)₀**) = (**Y^(U)₁** -
> **Y^(U)₀**) + (**Y^(T)₁** - **Y^(U)₁**)

The latter term now here is obtained by adding and subtracting the number **Y^(U)₁** in the expression. And now, the first difference term in the expression in the right hand side is nothing but the causal AU term (average effect of the treatment on the untreated). So, we get

> Observed Correlation = (**Y^(U)₁** - **Y^(U)₀**) + (**Y^(T)₁** -
> **Y^(U)₁**) = Casual AU term + Bias^(AU) term

Taking average of both the observed correlation equations, we get

> Observed Correlation = (Average of AT and AU) + (Average of bias^(AT)
> and bias^(AU))

So, we finally have

> Observed Correlation
>
> = Average causal effect of treatment in entire population + Average
> biases of AT and AU terms

So, we have that the observed correlation is made up of two terms. One is the unobservable causal effect (AT and AU) that we want to determine but we also have the bias terms that distort this causal effect. Even though we can’t directly observe this bias term (there are red coloured variables there), let us examine what is the physical significance of these bias terms and think about what could be the reason they occur.

> **Bias^(AT)** = (**Y^(T)₀** - **Y^(U)₀**) = difference in output when
> both T & U groups are not treated  
> **Bias^(AU)** = (**Y^(T)₁** - **Y^(U)₁**) = difference in output when
> both T & U groups are treated

If we are trying to estimate the effect of the treatment or input X on the performance Y, the bias^(AT) term tells us the difference in the performance of these two groups even when both groups are not treated. Similarly, the bias^(AU) term tells us the difference in the performance of these two groups even when both groups are treated.

But, in the specific case of drug trials, if we assume that the trial is randomised, then we have that everyone has an equal chance of getting the drug. So, since the trial group T and the placebo group U are chosen at random, we have that both the T groups and the U groups are statistically homogeneous. When the number of people in the groups are large enough, noise averages out, and hence we need to be worried only about bias. But, since the T and U groups are randomly split and hence are both statistically the same (made of random mixtures of people), the bias terms (**Y^(T)₀** - **Y^(U)₀**) and (**Y^(T)₁** - **Y^(U)₁**) vanish. Because, if T and U groups both get the drug (or both do not), their homogeneity due to randomness make them on average perform equally w.r.t Y when the input condition X is the same (both get drugs or both do not). Hence, in this special case, any correlation term we physically observe in (**Y^(T)₁** - **Y^(U)₀**) is mostly due to a causal effect of the drug X on the sample population made up of T and U groups. Thus, we can empirically determine the average causal effect of a drug X on the recovery Y by simply observing the observed correlation (**Y^(T)₁** - **Y^(U)₀**) since the biases vanish. The same holds for the food example where you observed that the pasta that you ate on the restaurant caused stomach ache. You can never ever prove that the particular pasta that you ate in the restaurant that you ate, caused a stomach ache. But, if you assume that the chef who cooked the pasta cooked it similarly for everyone who ate around the time you ate, then you can determine the average causal effect of the chef’s pasta on the eaters of the restaurant who ate at that time. Since it is fair to assume that the population visiting the restaurant at any particular hour is random, and people randomly choose to order pasta from the restaurant or not, if you can verify that many people who ate the same pasta that you also ate got stomach ache like you, while most of the people who did not order that pasta at that hour are fine, you can sue the restaurant by claiming that the pasta that the chef cooked during that hour you ate caused health issues to you, as a member of a larger sample population being subjected to the provable average causal effect. If you are the only person in the restaurant at that time who got a stomach ache after eating that pasta, you never know if that food poisoning is due to the restaurant pasta or because of some other health issues unique to you. This method of establishing average causation is called a **Randomised Controlled Trial** (**RCT**) and is due to the 20th century statistician **Donald Rubin**, and is also called the **Rubin Causal Model**.

------------------------------------------------------------------------

# Overcoming Selection Bias : The Case Study of Charter Schools



[](https://substackcdn.com/image/fetch/$s_!X0j_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2bb5387b-1366-48d2-bae6-b5b696a2b0c8_660x495.jpeg)

![The Case Against Charter Schools \| YIP Institute](https://substackcdn.com/image/fetch/$s_!X0j_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2bb5387b-1366-48d2-bae6-b5b696a2b0c8_660x495.jpeg "The Case Against Charter Schools | YIP Institute")





Looks like randomised control trials are the universal solution for the causation problem. Whenever you want to establish causation through correlation, simply use them. Wherever possible, randomised controlled trials are indeed used for establishing average causal effects in a large population. This is true in areas like testing drugs, short-term training programmes, computer softwares, and marketing. But, unfortunately, in most cases, we do not get to control who is in the trial group and who is in the control group ; that has already been pre-decided without us, and we have only the final data of the observed correlation, that contains both the causal effect term and the bias terms (AT and AU). In other cases, performing randomised controlled trials might infringe on personal liberties or come at a very high cost. In these cases, what should we do? There are many strategies about which we will see in this section.

Consider the example in the United States where one wants to study the causal effects of a student going to a charter school on his later educational performance. There are two kinds of tuition-free publicly-funded schools in the USA : **public** **schools** and **charter** **schools**. But, they differ significantly in how they are run, how students are admitted, and the rules they must follow. Public Schools are run directly by local school districts, and overseen by an elected local school board, adhere strictly to a district-mandated curriculum, and follow a top-down bureaucratic structure from the district superintendent to individual principals. Charter schools, on the other hand, are sparser (not every school district has one), and are independently operated by non-profit or private boards under a fixed-term contract (or "charter") granted by a state or local authority. They answer to their specific charter contract, rather than district-wide policies and enjoy greater autonomy in designing their own curricula, scheduling, and teaching methods. Another important difference is that while public schools are obligated to admit anyone from their district who applies, charter schools admit students from anywhere in the country (both local and non-local), and use a lottery system to decide who gets admitted and who does not, if the number of students applying exceeds their capacity. Given all these differences, what we know for sure is that there is a huge correlation between going to charter school and academic performance. But, does that mean that going to charter schools cause students to perform better academically in standardised tests and exams? If that is the case, opening more charter schools could benefit the education system in that country. If that is not the case and it is simply a correlation without causation, then it will have absolutely no effect.

If it were entirely up to us, we would love to perform an RCT on students where we randomly select which students study in a public school and which students study in a charter school. But, that is impossible, as that would infringe tremendously on personal freedoms of parents and students. All that we have is the data on academic performance of a large bunch of students along with whether they went to public schools or charter schools. We would love to control the choice of which student gets to go to which school ourselves through an RCT, but that is not an option. The choice of which student goes to what kind of school has already been made, and we have only the correlation data that is available to us (which does have a large positive correlation). But, using some intelligent technique, can we somehow use this available data only, and tease out the causal influence and separate it from the bias terms?

Let us again look at the two equations we saw in the last section. If the students who go to charter schools is the treated group (X = 1) and if the students who go to public schools is the untreated group (X = 0) and if Y is the academic performance of the group of students with respect to some metric, we have so far :

> **Bias^(AT)** = (**Y^(T)₀** - **Y^(U)₀**) = difference in output when
> both T & U groups are not treated  
> **Bias^(AU)** = (**Y^(T)₁** - **Y^(U)₁**) = difference in output when
> both T & U groups are untreated

Let us ask the physical significances of these biases for this particular example ; and remember that it is these biases that make the observed correlation deviate from the causal influence that we are trying to measure.

> **Bias^(AT)** = (**Y^(T)₀** - **Y^(U)₀**) = baseline difference in
> average academic performance between charter school students (T) and
> public school students (U) under the identical circumstance of both
> groups going to *public* schools  
> **Bias^(AU)** = (**Y^(T)₁** - **Y^(U)₁**) = baseline difference in
> average academic performance between charter school students (T) and
> public school students (U) under the identical circumstance of both
> groups going to *charter* schools

Let us ask what exactly the bias is telling us. There are now two types of students in the population under study : those who study in charter schools (T) and those who study in public schools (U). The AT bias term tells if there would be an inherent baseline difference in academic scores between the people who get into charter schools (T) and the people who get into public schools (U), even if both of them are identically put in public schools hypothetically. The AU bias term tells if there would be an inherent difference in academic scores between the people who get into charter schools (T) and the people who get into public schools (U), even if both of them are identically put in charter schools hypothetically. If the students who are selected to go to charter schools are on average inherently academically better performing than students who are selected to go to public schools, then there will be a difference in the average academic performance of these two groups (T and U) even if both of them are given the identical kind of school education. The AT bias and the AU bias precisely measure the extent of this phenomenon. If the choice of who gets to go to a public school and who gets to go to a charter school are random, then there would be no such inherent differences in average academic performances between the two groups, if both are given identical education (both in charter school / both public school). But, if suppose the choices are not random, we see from above that there could be some **selection bias** at play, so that students who perform better tend to get selected to go to charter schools and students who perform worse tend to get selected to go to public schools, so that there is already a baseline difference in academic performance between the T and U groups, even if both were to be subjected to identical treatment.

Is there a reason to think that there could be some selection bias at work (these biases again cannot be measured empirically as they involve hypothetical scenarios), so that the demographics of the two groups already have a baseline difference in performance, even if both of them would be hypothetically given identical treatments? If that is the case, then charter school students perform better than public school students, not so much because going to a charter school causes better academic performance, but simply because students who get selected to go to charter schools, are already academically better than the students who get selected to go to public schools. Here is one situation how such a selection bias can be at play. Imagine you are a poor parent who cannot afford any tuition fees of the private schools, and hence your only option is going for publicly funded schools. When would you try to get your child admitted into a charter school with a novel and autonomous education system at a far-off place that involves the risk of making it through a lottery, rather than a public school in your local district with a standard curriculum that is obligated to accept your child ? You would take such a risk only when you believe that your child is already academically better, and hence deserves a novel education system; right? So, we see that, by the time parents apply their kids to charter schools, there is a selection bias at play. A parent of a gifted child will try his best to apply for charter schools and try to get his child admitted there. A parent of an academically normal or dull child would be less likely to take such a risk, and instead get his/her kid admitted into a local public school in his district instead. So, there is already a difference in academic capabilities of students who study in charter schools vis-a-vis public schools, even if all other circumstances would be identical for them. So, it could be that the higher scores of charter school kids is simply due to this selection bias at play, and not due to causal effects of charter schools doing something to make the kids better. How do we isolate the causal part from the selection bias here? In this particular case, there is a very elegant way to isolate these two effects. It is not so tough to think about it given that the charter schools admit students with a lottery if their application numbers exceed their capacity. So, take some time to think about this problem, and if you still cannot figure out, continue reading the next paragraph.

We need to ensure that the people in the treatment group (T) and the control group (U) are identical and chosen randomly. But, we already have a random selection at work here. Charter schools have a lottery system to determine who gets accepted and who gets rejected, if the number of applicants exceed their capacity (and they frequently do). So far, our groups are :

> T = those who get admitted into charter schools  
> U = those who get admitted into public schools

But, now we observe that among those people who go to public schools (U), there are two groups of people. They are :

> People who study in public school = People who applied to charter
> schools and got rejected by the lottery + People who never applied to
> charter schools at all

What if we restrict as our control group, only those students who applied for charter schools but got rejected by the lottery, and hence are forced to study in public schools. That is :

> T = those who applied to charter schools and got admitted   
> U = those who applied to charter schools but did not get admitted (and
> hence are forced to study in public schools)

If we restrict our U to this set, we are restricting ourselves only to those people in public schools who applied to charter schools. And we saw that charter schools determine who gets in and who gets rejected based on a random lottery, as we would want in an RCT. There cannot be any selection bias in this new smaller population of T and U ; because it is a random lottery that decides who is in the T group and who is in the U group. So, we now see if there is still a correlation between higher academic performance and attending charter schools, only in the restricted data set of those students who applied to charter schools in the first place. It turns out that there is no significant correlation between people who study in charter schools and higher academic performance in this restricted data set (at least that is what this study [here](https://econweb.ucsd.edu/~jbetts/Pub/A51%20Report%2008%2006%20Betts%20et%20al%20Choice%20Report%20PPIC.pdf) claims). Thus, if this is the case, building more charter schools at the expense of public schools, will not magically increase the number of academically well-performing children, as the opening cartoon in this section shows. Thus, when you compare all charter school students to all public school students, charter schools look like magic. But when you restrict the control group only to the kids who applied to the charter-school lottery and lost (so that both groups had parents motivated enough to apply, meaning the selection bias is neutralised), the massive performance gap often shrinks dramatically or vanishes entirely. The lottery losers form the ideal control group (U) because they share the exact same desire/motivation to attend a charter school, thus wiping out the baseline bias. In the next section, we will examine deeper into the sources of selection biases.

Differences in performance between two groups subject to different treatments, need not always be because of the causal effect of the treatment on the performance. It can also arise due to selection bias where in some other mechanism tends to influence well-performing individuals to be more likely or less likely to be in the group receiving the treatment. Only if we are sure that the two groups (treated vs untreated) are made of randomly chosen individuals, does a difference in average performance between the two groups is solely explained by causality of the treatment on the performance.

------------------------------------------------------------------------

# Controlling for Confounders : The Case Study of Congress Voting Patterns



In the last section, we saw about how selection biases at play lead to a correlation between performance of two groups subjected to different treatments, even when there is no causal effect of the treatment on the performance. In this section, we will see about one main source that gives rise to selection bias. Understanding this will be a gigantic leap ahead in your understanding of when you can conclude about an unobserved causality from an observed correlation. The other important source of selection bias will be introduced in the end of this article and will be covered in detail in the next article of this series.

One main source of bias is what is called a **confounding variable**. In the study of the relation between a treatment X and outcome Y, another variable Z is called a confounder if it satisfies two conditions :

1.  Z has a causal effect on the treatment status X (causes X to
    increase)

2.  Z has an independent causal effect on the outcome Y (causes Y to
    increase)

[](https://substackcdn.com/image/fetch/$s_!i2HM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F06774185-e092-4bcb-bfdc-648afd505d4b_1487x877.png)

![](https://substackcdn.com/image/fetch/$s_!i2HM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F06774185-e092-4bcb-bfdc-648afd505d4b_1487x877.png)





Confounders create baseline bias. Suppose in the population, an increased Z causes people to have increased odds of receiving the treatment (Z → X) and also an increased causes people to have increased outcomes (Z → Y). This creates a correlation between X and Y through the common influence by Z rather than the direct influence of X on Y.

In other words, presence of a confounder Z causes a difference in outcome between the treated group (X = 1) and the untreated group (X = 0) not because the treatment X causes increased outcomes directly, but because being in the treated group (X = 1) and having an increased outcome (more Y) are both common symptoms caused by an increased Z.

> In the case of the school example,
>
> Z = academic abilities of the student  
> X = admission into a charter school  
> Y = academic performance
>
> There is a positive correlation between studying in charter schools
> and increased academic performance not because charter schools train
> for better performance, but because both admission into a charter
> school and high academic performance are symptoms of the academic
> abilities of a student. That is, students with more academic abilities
> both tend to apply more to charter schools and also tend to perform
> better.

Confounders are a big problem when we are trying to learn about causal relationships from data on correlation. In this section, we will see an important technique used to mitigate against confounders which is called **controlling**. Let us demonstrate how it is done using a case study from the US Congress. A very unsurprising thing about the US Congress is that Republicans tend to vote more conservatively than Democrats. A metric of measuring the degree of conservatism of a Congressman is that the American Conservative Union (ACU) gives scores to a Congressman from 0 to 100 based on how they voted in some collection of bills at that year. A higher ACU score here means a right leaning conservative voting pattern and a left leaning score means a left leaning liberal voting pattern. Data collected in 1997 from the House of Representatives shows that Republican Congressmen have a much higher average score by the ACU (around 83) than Democrats who have a much lower score (around 19).

This correlation between being a Republican and a conservative voting pattern is an undeniable and significant one. But, does this automatically mean that being a Republican in the Congress causes one to vote more conservatively? Is the Republican party causing its Congressmen to vote conservatively, and vis-a-vis the Democrats progressively? Not at all, if we remember the last section. Here, we can see an obvious confounder at play here which is the personal ideology of the candidate. Republican Congressmen may tend to vote more conservatively because the party pressure causes them to vote so (direct causation), but also may be because a person with a conservative ideology would be more likely to be both in the Republican party and also be more likely to vote more conservatively (an obvious case of selection bias where personal ideology influences both party membership as well as voting pattern).

[](https://substackcdn.com/image/fetch/$s_!dDcl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff1ece479-4dea-426c-bb42-0dd42b1334f4_1458x864.png)

![](https://substackcdn.com/image/fetch/$s_!dDcl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff1ece479-4dea-426c-bb42-0dd42b1334f4_1458x864.png)





So, can we isolate and see how much of this correlation is explained by the confounding variable, and how much of it is caused by direct causation? How much of the voting pattern of US Congressmen is influenced by party pressure and how much by personal ideology? In this case, we clearly have a known candidate for the confounding variable Z which is personal ideology. We can also quantitatively measure the degree of conservatism in personal ideology by another score from 0 to 100 that is generated by an organisation called Project Vote Smart, based on the responses of candidates to several questions.

So, in the case where there is a known candidate for a confounding variable Z, the technique of controlling is used to isolate the causal component from the selection bias in the correlation data. What we do is basically observe if there is any correlation among those data points where Z is constant. The data for some Congressmen from 1997 is shown below. To control for personal ideology Z, we compare the voting patterns of Democrats and Republicans with similar NPAT ideological scores. Note first that the average difference in the ACU conservative voting scores between Republicans and Democrats is 83 - 19 = 64, which is massive. In the table below, controlling for personal ideology Z based on NPAT percentile, we see that in no column, is the difference in ACUs anywhere close to the 64. This itself says that personal ideology plays a huge role as a confounding variable - so, a large part of the difference is due to conservative people being more likely to serve in the Republican party; and not the direct pressure from the party.

[](https://substackcdn.com/image/fetch/$s_!HRZe!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd7f92f05-c302-4e75-9c06-9ab6b6b3117e_1634x616.png)

![](https://substackcdn.com/image/fetch/$s_!HRZe!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd7f92f05-c302-4e75-9c06-9ab6b6b3117e_1634x616.png)





Next, we see that the number of ideologically conservative Democrats (NPAT scores in the ranges 61-80 and 81-100) is just two, and hence any statistics from that end is very unreliable and corrupted with noise. Similarly, the number of ideologically liberal Republicans (NPAT scores in the ranges 0-20 and 21-40) is also small and just are four in number, hence the same. So, no information in the difference in voting patterns from those sides are any informative at all. Hence, the only reliable place to estimate Z-controlled correlation is in NPAT range 41-60 column which is in the mid-range of the progressive vs conservative ideological score. Intuitively this makes sense too, because a score from 41-60 indicates that the candidate is at the middle in the progressive-conservative scale without a firm and strong personal inclination towards either conservatism or progressivism. Hence, such a type of candidate is equally likely to belong to either the Democrat Party or the Republican party ; and random chance is the only thing that decides which party he is (like in RCTs). Thus, the mid-range in NPAT serves as a natural RCT experiment that we would love to have for estimating only the causal effect between party membership and voting pattern. Looking at the difference in ACU voting scores only here in this NPAT score range gives a value of 27. If the data in the other NPAT score ranges are good, then one would take a weighted average of the voting differences across all the ideological spectrum which are 26, 27,
-10, 10. We hence see a difference of 27 in the conservative voting score between Republicans and Democrats in this range ; and comparing it to the total average difference 64, we see that, roughly 40% of the correlation between conservative voting patterns in the Congress and being in the Republican party, is explained by a direct causal link from party membership (party pressure) ; whereas the remaining 60% of the correlation is explained by the confounding variable which causes ideologically conservative candidates to vote conservatively and also simultaneously causes them to be more likely in the Republican party than the Democrat party.

This overall strategy of choosing a small range of the control variable and then looking at the correlations between treated and untreated cases at just those range of the controls, and then taking weighted averages of those correlations for all ranges to report the final unbiased correlation; is called technically as **nearest neighbour matching**.

There is also another way to quantify these aspects would be via **regression** (which we saw in the previous article). Assume for a moment that we simply try to predict the voting ACU score based on just party membership without controlling for the personal ideology Z. Then, we do another linear regression (as we saw in the previous article in this series) as follows :

$`\text{ACU score} = \alpha^{S} + \beta^{S}T`$

where

> T : this variable is 0 if the candidate is Democrat and 1 if
> Republican

With techniques in the previous article of this series, we can find the slope of the best fit line for this relationship β^(S) from the available data without controlling for any personal ideology. This β^(S) tells us the raw correlation between party membership and conservative voting score which also has bias. To control for bias, now assume that the ACU score of a candidate can be predicted based on a formula not only based on party membership but also based on what the NPAT score of the candidate is. The structure of this formula is shown below.

$`\text{ACU score} = \alpha + \beta\text{~T} + \gamma Z`$

The independent variables are :

> T : this variable is 0 if the candidate is Democrat and 1 if
> Republican  
> Z : the NPAT of the candidate which is in range 0-100

The parameters have the following interpretations :

$`\begin{matrix} \alpha & {:\text{constant term}} \\ \beta & {:\text{influence of the party X}} \\ \gamma & {:\text{influence of personal ideology Z}} \end{matrix}`$

Like we found the slope of the best-fit line using the data points for data with two variables (one dependent variable and one independent variable), we can similarly find the coefficients of the best-fit relationship from the data that gives these details. The formulae are more complicated and hence I won’t give it. But, the general method to do it is called **weighted least squares regression**, just in case you want to dig up the math details. The presence of a non-zero value of the first beta coefficient β tells us the party influence which corresponds to direct causal influence between party membership and voting pattern score. The gamma coefficient γ tells us the influence of the confounding variable Z. So, now we have three parameters computed so far :

> β^(S) : correlation between party membership and voting pattern  
> β : correlation between party membership and voting pattern when
> controlled for personal ideology (which is the direct causal influence
> of party on voting)  
> γ : correlation between personal ideology and voting pattern in the
> controlled study

When there is no influence of personal ideology Z on party membership, then we must have that β^(S) = β and γ = 0. Thus, the difference between these two quantities should give the measure of the bias induced by personal ideology on both party membership and the voting pattern.

> β^(S) - β : bias of the simultaneous influence of the confounding
> personal ideology on the party membership and the voting pattern

It turns out that there are more interesting things to say about this number β^(S) - β. For this, consider a regression that tries to determine the correlation between the confounding variable Z (here, personal ideology) and the treatment variable T (here, party membership) that is structured as follows :

$`Z = \tau + \pi T`$

This regression tries to predict the ideological leaning of a person Z based on his party membership, and hence the slope of the best-fit line π ogives the measure of correlation between party membership and ideological leanings.

Thus, we have computed three quantities so far :

> β^(S) - β : bias of the simultaneous influence of the confounding
> personal ideology (Z) on the party membership (T) and the voting
> pattern (Y)  
> π : correlation between personal ideological leaning (Z) and party
> membership (T)   
> γ : correlation between personal ideology (Z) and voting pattern in
> the controlled study (Y)

It turns out that there is a neat mathematical relationship between these four numbers which is

$`\text{Bias} = \beta^{S} - \beta = \pi \times \gamma`$

This formula is called in the statistics community as the **omitted variable bias formula**. What this tells us is that there are two sources whose product contribute to the bias. One is the influence of the confounding variable (here, personal ideology) on the treatment (here, party membership) which is π. Another is the influence of the confounding variable (here, personal ideology) on the output (here, voting pattern) which is γ. The formula tells us that the bias is caused by the confounding variable (here, personal ideology) simultaneously influencing both the treatment (here, party membership) and the output (here, voting pattern). This fact is nothing new ; we already said that confounding variables produce a correlation between input and output simply due to bias, by independently influencing both the treatment and the output, even if there is no direct influence of the treatment on the output. The things that we have learnt so far are summarised below.

[](https://substackcdn.com/image/fetch/$s_!b91j!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffa57fc23-96a2-4e7b-a145-ee0fd6e0a582_1512x940.png)

![](https://substackcdn.com/image/fetch/$s_!b91j!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffa57fc23-96a2-4e7b-a145-ee0fd6e0a582_1512x940.png)





The direct causal influences of each variable on the other

[](https://substackcdn.com/image/fetch/$s_!8Sct!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcbf0020d-c2b5-4b28-9d77-e670bb921992_1530x638.png)

![](https://substackcdn.com/image/fetch/$s_!8Sct!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcbf0020d-c2b5-4b28-9d77-e670bb921992_1530x638.png)





The observed correlation between treatment and output without considering the influence of confounding variables is made up of two terms : the direct causal influence and the confounding influences from the confounder

We can also use statistical hypothesis testing (learnt in the previous article) to determine the probability of getting the data that you have gotten assuming the null that there is no causal influence, for confidently postulating that there is a direct causal influence between party membership and voting pattern that is established by regression.

Although the above was a very specific example involving only one confounding variable, it should be very clear by now that : **As long as all the possible confounding variables are known and measurable, one can isolate the causal influence from the selection bias (caused by confounding influence) in a correlation, by controlling for those confounding variables**. The computations are lengthier if there are more variables and more data, but a simple program can churn out these numbers very easily in that case.

But, **if there are unknown confounders or known but unmeasurable confounders, we have to remember that there is always a danger of wrongly estimating the causal effect of one phenomenon on the another using their observed correlation data**.

------------------------------------------------------------------------

# Causation Leading to No / Opposite Correlation : The Remedial Tutoring Paradox



Now, we are prepared to answer another question that we saw in the beginning of this article. While everyone is familiar with the famous statistical adage that “***correlation does not imply causation***”, and in the last section we see how to isolate for confounding variables to eliminate selection bias from the observed correlation in order to extract the causal effect, now we are prepared to understand the equally true but less well-known fact that “***causation does not imply correlation***”. How can there be no correlation observed between two variables even if one is directly causing some effect on the other variable? It is here once again that the bias from the confounding variable comes in. Recollect from the previous section that :

$`\begin{matrix} {\text{Observed correlation~}\beta^{S}} & {= \beta + \text{Bias}} \\ \text{Bias from the confounder} & {= \pi \times \gamma} \end{matrix}`$

We saw that if there is a direct causal influence 𝝱, the bias from the confounder adds to it to produce an increased observed correlation. In other words, the bias from the confounder typically boosts the causal effect 𝝱 to produce an even increased observed correlation. But, what if the sign of the bias term is negative? Then, the bias will suppress and diminish the causal influence to produce a reduced observed correlation between the treatment and the effect. If the bias is just about right, then it will exactly cancel the causal effect and will result in a zero observed correlation between the treatment and the output, even if there is a direct causal effect of the treatment on the output. If the negative bias exceeds the causal influence, one sees even a negative correlation between the treatment and effect, despite a positive causal influence from the treatment to the effect. Let us now investigate when the sign of the bias is typically negative.

The bias is given by the product of two terms 𝝿 and 𝛄. It is positive if both of these terms are of the same sign, and is negative, if both of these terms are of different sign. Again, let me illustrate this with an example that is popularly called as the **remedial tutoring paradox**. Here, we want to study how tutoring affects the performance of the students. Remedial tutoring is when weak students are made to stay at school after class hours where a tutor makes them complete their homework, help them as they struggle through it, and also make them prepare for an upcoming test. Some school districts offer remedial tutoring in their public schools whereas others do not; and hence we need to determine if remedial tutoring is causing an improvement in overall school performance. The diagram is as follows.

![](https://substackcdn.com/image/fetch/$s_!bQS_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3467af9c-b783-43b5-bf52-4bffcd9d4fa6_1476x264.png)

Intuitively, we are certain that tutoring will improve the overall academic performance in the student population. If the causal influence is the only thing at play, remedial tutoring in schools should correlate to better student average marks for the school.

But, there is a selection bias at play here. The decision of which school gets chosen to be funded for remedial tutoring, or which school will prioritise utilising its funds for offering remedial tutoring, is not made randomly. Only schools that have a weak average student performance anyways, are more likely to offer remedial tutoring for its students. But, such schools with weak students on average, also typically perform poorer than others anyways. So, there is a confounding variable Z which is average academic ability of the school student population, that simultaneously influences (first:) which school gets chosen for offering remedial tutoring and (second:) also influences the kind of performance that schools will have. Let us see the signs of their influences and the selection bias induced by it, by reasoning through below.

> π : correlation between confounding variable (average academic ability
> of student population) and treatment (offering remedial tutoring)

What is the sign of this π term? We know that schools with higher average academic ability of its students, are less likely to offer remedial tutoring, while schools with lower average academic ability of its students, are more likely to be chosen for tutoring. So, we see that higher average student academic abilities lower the odds of getting the treatment (here, tutoring) and hence there is a negative influence between the confounding academic ability and the treatment of tutoring. So, we now have π \< 0. Now, let us look at the next parameter.

> γ : correlation between personal confounding variable (average
> academic ability of student population) and output (average school
> academic performance)

What is the sign of this γ term? We know that schools with students of higher academic ability perform better than others independently of whether there is tutoring for everyone or not. So, we see that there is a positive influence between the confounding feature of academic ability and the output of academic performance. So, we now have γ \> 0.

From the equation we saw in the previous section, we have

> Bias = γ.π \< 0

Thus, the observed correlation between tutoring and academic performance in the population would be

$`\beta^{S} = \beta + \text{bias} = \beta + \pi \times \gamma`$

And hence, we have

$`\beta_{S} < \beta`$

If the bias effect is of enough magnitude, we can even have

> 𝝱^(S) \< 0

That is, there is negative observed correlation between tutoring and the average school performance!! That is, schools that have remedial tutoring tend to perform worse than students that do not have it!! If you pull the raw data across the country or a large state, you will routinely find that **schools offering extensive remedial programs, after-school tutoring interventions, or special academic support packages have lower average test scores and graduation rates** ! A very stupid policy maker might see this and conclude that tutoring is having no effect or a worsening effect on school performance, when it in fact is working very good as expected on the ground ! The reason why schools with tutoring perform worse than schools that have tutoring here, is not because the tutoring is not having the expected causal effect, but simply because : **the very fact that the school is already performing poorly is what made it more likely to offer tutoring.** In this case, controlling for the confounding variable is mandatory to even get the correct effect, and even the correct sign, of the causation. One simple way to do this would be to compare the performance between schools that offer tutoring and schools that do not, taking into account only schools in similar socio-economic neighbourhoods, or within the same district. This failure to account for and control the confounding variable is one of the most common pitfalls in policy evaluation.

Thus, not only does correlation not imply causation ; it can also be that the sign of the observed correlation might mislead on the actual causal influence. Thus, one should be extremely careful jumping from the observed correlation or non-correlation to any causal claims.

When programmes are targeted towards the demographics that need them the most, one should be very careful about their performance assessment, and isolate this negative confounding bias to see only the causal influence ! This is why correct why causal inference is mandatory in public policy. Otherwise, governments would defund successful programs just because they happen they are selectively targeted towards the demographics who need them most !

------------------------------------------------------------------------

# Policy Design & Evaluation : Regression Discontinuity



In the previous section, we saw how we can isolate true causal effects by simply controlling for all confounding variables using either nearest neighbourhood matching or regression. However, in many complex real-world scenarios, the most critical confounders are either entirely unobservable or impossible to be measured even if observable (psychological features like innate motivation, hidden talent, or unrecorded background factor). When these unknown and unmeasured confounders lurk in the shadows, standard controlling techniques fail, leaving our regression models hopelessly biased even after controlling for all the known and measured confounders. But, there is a workaround in some of these situations that allows us to bypass unobserved confounding to produce a locally accurate causal estimate of a binary policy (some action is either done or not done) which is the subject of this section.

Again, a motivating example is a great way to explain how the technique works. Suppose we are running a merit scholarship programme for financially underprivileged students in a college and we want to estimate its effect on the student performance. We cannot simply compare the performances of students those who receive the scholarship with those who do not, because the students eligible for scholarship is not randomly selected. But there are so many confounding variables to account for that makes students who receive the scholarship perform differently from the students who do not. We cannot measure and control for all these variables (like intelligence, ability, motivation, talent, work ethic, ambition, taste). But still we want to evaluate if the scholarship is making a difference for students receiving it. Assume that the students are scored transparently from 0 to 100 on a numerical scale that involves a weighted sum of a lot of parameters (GPA, income of parents, test scores, community service, extracurriculars etc..). Let us say that those students who score 95 or above in this score are chosen for scholarship while the others are rejected. Many policies relevant of interest in social sciences are designed based on a threshold in a certain numerical score. Again, the students who are above 95 in this score and receive the scholarship and the students who are below 95 in this score and do not receive the scholarship are very different in many ways, and hence this is not a random selection. The score that is used to award scholarships is also correlated to the output of the students (colleges would give scholarships only to those people whom they believe will perform well). So, a raw correlation analysis again will not at all work here. But, since there is an abrupt discontinuity in who gets the scholarship based on a threshold (here, it is 95), we can ask another question. The people with scores like 94.5, 94.9, 94.7 are not that different from people with scores like 95.0, 95.3, 95.4. Had the people with 94.5 score worked a little harder on an exam day, they would have crossed to 95; and if the people who had 95.3 score got a fever in one of their exams, they could have easily gotten to below 95. So, it seems reasonable to conclude that at least the students who are little below the threshold (94.8, 94.7, 94.55 etc) are not that different from the students who are little above the threshold (95.0, 95.3, 95.12 etc). But still, the people who got a litte below 95 are rejected for the scholarship, while the people who got a little above 95 are awarded scholarship. Thus, we can conclude that at least in the restricted population of students with scores very near threshold 95, where some students get the scholarship and some do not, the reasons are essentially random in that small group. So, since it is a random trial for that small group of population with scores close to that threshold, we can estimate accurately the causal effect of winning a scholarship simply by observing the correlation.

How exactly do we estimate the causal effect of the scholarship just around that threshold? One can plot the data of the students with their score on the x-axis and their outcomes on the y-axis keeping in mind that students with scores above the threshold are treated (T = 1) and students with scores below the threshold are untreated (T = 0). Notice that there will be correlation between the score and the performance because that is how scores are typically designed so as to award scholarships to potentially more deserving students. Let us assume that the plot looks like this below. The score is rescaled between -0.3 to +0.3 so that the people above score 0 get scholarship and people below 0 do not. Such a normalised representation of the score is called the **running variable** (here denoted by R) in statistics literature. The blue dots represent the performance of those who get the scholarship and the red dots represent the performance of those who do not get the scholarship.

[](https://substackcdn.com/image/fetch/$s_!_7kv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F72c0f78e-bae4-4bbe-b62e-472fc07277d2_2564x1632.png)

![](https://substackcdn.com/image/fetch/$s_!_7kv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F72c0f78e-bae4-4bbe-b62e-472fc07277d2_2564x1632.png)





We can run two regressions and compute two lines of best fit : one for the right side of the threshold, and another for the left side of the threshold. We can then see what both regressions predict at the threshold. The abrupt jump or discontinuity in these two predictions at the threshold is due to the causal effect of the treatment since nothing else abruptly changes about the population just around the threshold, except for their treatment status. The jump or discontinuity due to treatment is shown below. It is technically called as **regression discontinuity** in the statistics literature.

[](https://substackcdn.com/image/fetch/$s_!y5Rc!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fec98c94d-ab9d-4307-a1c4-b87a18e1d0ba_2574x1664.png)

![](https://substackcdn.com/image/fetch/$s_!y5Rc!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fec98c94d-ab9d-4307-a1c4-b87a18e1d0ba_2574x1664.png)





There is something very important worth repeating a lot of times here. The treatment effect which is observed in the vertical gap is not for the entire population. It is just for those small population who have the value of their running variable just around a small neighbourhood of its threshold. In this particular example of scholarship, the treatment effect is only for those students whose score is around 95. If the threshold for awarding the scholarship were different (say 70), then the treatment effect could be very different because the population who share a score around 70 are different from those that share a threshold score around 95. So, this treatment effect estimated for the population at the threshold is technically called as the **local average treatment effect** (abbreviated **LATE**). The word “local” in LATE emphasises that this treatment effect holds only for the threshold population, and not for the entire group. So, you must not use this LATE estimate if you want to know the treatment effect for the entire group. But, there are many times where you would want to estimate only the LATE value. Many policies and treatment programs in this world are based on a threshold of a certain score. In these cases, LATE estimate using regression discontinuity determine the effects of the program for the kind of people we care about the most : the people who are around the margin, and are barely eligible or ineligible. If the LATE is very large for the threshold chosen, one might want to increase the threshold further to bring those people inside the program. So, LATE is indeed a very reliable estimate of the treatment effect for people who are at thresholds of a discontinuous threshold based treatment mechanism.

There is one important point to note though. The regression discontinuity mechanism and LATE estimation assumes two things :

1.  Agents do not have access to the scoring system or the threshold so
    that they can change their natural behaviour to hack the threshold;
    which enables selection bias as to who gets to be just above the
    threshold and who gets to be just below the threshold

&nbsp;

2.  Everything else that has got to do with the performance of the
    population change continuously, except the treatment status which
    alone changes discontinuously.

There are two main situations where these hypotheses fails. The first thing is that there could be biased manipulation happening either by the students or the scholarship committee to deliberately around the threshold. For example, well to do candidates with connections to the committee can figure out the scoring system and can do the least possible to get their scores just above the threshold. Or the committee can boost or reduce the final scores of certain candidates so that people of a certain demographic are not over-represented or under-represented. In both of these cases, the individuals just above the threshold will not be comparable to the individuals just below the threshold because the selection of who belongs where is no longer random but deliberately manipulated based on certain demographic criteria that may correlate with the output. The second thing that could screw up the estimation of LATE is when there are other things correlated to the output that also change discontinuously at the given threshold. For example, in some European nations like France, salaries of city mayors jump abruptly at certain population threshold in their respective cities. If we want to determine the effect of such mayor salaries on the city performance or standards at thresholds, we might be tempted to just use LATE by using salary of the mayor as the running variable. But, the salary is not the only thing that changes at this population threshold as per law. There are many other policies that change when the population just crosses this threshold which include the size of the city council, the electoral rules, the budget, taxation rules, and so on. In this case, discontinuities in the city performance at this threshold are not necessarily due to the abrupt salary change but can also be due to the other factors mentioned above that also change discontinuously at this threshold an have an effect on the output. Clearly in that case, LATE estimation using regression discontinuity will be a very biased and unreliable estimate.

When we know that a treatment of interest was determined by a threshold or cutoff in a certain numerical variable, an RD design might allow us to obtain credible estimates of the effect of that treatment at that cutoff point. In LATE estimation using regression discontinuity, the fundamental assumption is that the agents just below the threshold who barely miss the treatment), and the agents just above the threshold who barely get the treatment, have it so for essentially random reasons; and the treatment is the only factor that changes discontinuously at the threshold. Sorting at the threshold which involves manipulation of agents or cheating at the threshold and other discontinuities at the same threshold upset this situation, thus rendering regression discontinuity to be a poor estimate of LATE. Thus, regression discontinuity is powerful, but not a magic wand if other policies change at the exact same boundary and if there is biased cheating to hack the threshold.

------------------------------------------------------------------------

# Difference-in-Difference Mechanism



Threshold based mechanisms are not the only mechanisms out there where the causal effect of treatment can be locally estimated by an easy process (like regression discontinuity). There are other mechanisms that motivate other estimation strategies too. In this section, we will study another such mechanism, called the **difference-in-difference mechanism**, before proceeding to discuss mechanism design generically in the next section.

Consider a policy where we want to evaluate the impact of the introduction of a binary policy like a mid-day meal scheme on the student performance. Let us say that some schools in a district adopted that policy and some did not. The choice of what schools adopted that policy and what did not was neither made randomly (hence not an RCT) nor was it made by any threshold of a score (hence LATE is not possible) but for arbitrary yet non-random reasons. We cannot simply compare the performance of the states that adopted that policy to states that did not adopt that policy because of selection bias. But, we can here compare the performances of schools that adopted that policy with their own performances before they adopted that policy. But, this is not a reliable estimate either because there could be a change in the performance with time in an adopted school even if it had not adopted the policy. So, we never know if the post versus pre treatment changes in the effect for treated schools is due to the adoption of that policy or this generic time change that would have happened even if they had not adopted treatment. But, assume that we are interested to know only the effect of the treatment on just the treated population which adopted the policy (this solves the first problem) and that the average time variation of performance without treatment is same between treated and untreated units (this solves the second problem).

Let UU be the group whose members never adopted the treatment and hence did not change their treatment status (T = 0 → T = 0 : remain untreated : U → U). Let us first observe the average change in outcome of this untreated group with time, by noting the difference between their average output performance after treatment introduction period (A) and the same before treatment introduction period (B). That is, even though the UU group did not receive treatment, their output performance can still change with time during the period when the treatment was adopted by other groups. This is what the below quantity observes and is denoted by :

$`DIFF_{UU}:=Y_{0,UU}^{A} - Y_{0,UU}^{B}`$

Let UT be the group whose members adopted the treatment and hence changed their treatment status (T = 0 → T = 1 : U → T). Let us now observe the average change in outcome of this treated group with time after treatment introduction period (A) compared to the before treatment introduction period (B). This quantity directly denotes the average observable difference in the performances of the treated group with time during the time period between after their adoption of the treatment and before. This is denoted by :

$`DIFF_{UT}:=Y_{1,UT}^{A} - Y_{0,UT}^{B}`$

Let us now rewrite the above expression by adding and subtracting a term Y^A\_{0,UT} which is the hypothetical performance of the treated group after treatment if there were no treatment. We now have :

$`\begin{matrix}
 & {DIFF_{UT} = Y_{1,UT}^{A} - Y_{0,UT}^{B}} \\
 & {= \underset{\text{effect of getting treatment for the treated UT group}}{\underbrace{(Y_{I,UT}^{A} - Y_{0,UT}^{A})}} + \underset{\text{average time trend for treated UT group without treatment}}{\underbrace{(Y_{0,UT}^{A} - Y_{0,UT}^{B})}}} \end{matrix}`$

So, the overall change in performance after the treatment for the group that adopted that treatment is made up of the addition of two components :

1.  the first is the average causal effect of getting the treatment on
    performance of the treated group who adopted the treatment (ATT like
    term) → we would love to calculate this

2.  the bias that signifies the trend in performance of the treated
    group over the time the treatment got introduced, even if there was
    no treatment (bias ATT like term)

If we subtract these two differences (that is why the name difference-in-differences), we get three terms :

$`\begin{matrix}
 & {\text{Difference in differences} = DIFF_{UT} - DIFF_{UU} = \underset{\text{effect of getting treatment for the treated UT group}}{\underbrace{(Y_{I,UT}^{A} - Y_{0,UT}^{A})}}} \\
 + & {\underset{\text{average time trend for treated UT group without treatment}}{\underbrace{(Y_{0,UT}^{A} - Y_{0,UT}^{B})}} - \underset{\text{average time trend for untreated UU group without treatment}}{\underbrace{(Y_{0,UU}^{A} - Y_{0,UU}^{B})}}} \end{matrix}`$

Now, we make the assumption that the second and third terms in the above equations are equal so that they cancel and become zero. That is, we assume that the time variation of both the treated and untreated groups would have been the same on average if both the groups were left untreated. This assumption is called in statistics literature as the **parallel trend assumption**. The change in average outcome with time should have been the same for both the groups without treatment. Note that this does not mean that both the groups are statistically the same and this allows for the possibility that the members of the two groups can have different characteristics. But, it is required that time affects both the groups equally if there would be no treatment for both the groups. If that is the case, we have that the observable difference-in-differences can estimate the causal effect on the treated group successfully.

$`\text{Difference in differences} = DIFF_{UT} - DIFF_{UU} = \underset{\text{effect of getting treatment for the treated UT group}}{\underbrace{(Y_{I,UT}^{A} - Y_{0,UT}^{A})}}`$

Also note again that this measures the causal effect of the treatment only on the subgroup that adopted that treatment, and not on the entire population. But, in many cases, the former might be the quantity of interest.

The Difference-in-Differences mechanism offers a pragmatic and powerful strategy for the evaluation of the time effects of a policy by comparing the over-time trajectories of a treated group and subtracting it against that of an untreated control group. Its greatest strength lies in its ability to eliminate unobservable, time-invariant selection biases, allowing researchers to isolate the causal effects of their policy that has been introduced. However, its primary limitation hinges entirely on the parallel trends assumption which is the premise that : both groups would have changed with time identically on average without the policy. If unobserved external trends affect the treated and control groups differently, the parallel trends break down, rendering this estimate heavily biased. Like all tools in causal inference, there is no free lunch here either. DiD breaks down if there are time-trends that affect the two groups differently.

------------------------------------------------------------------------

# Negative & Positive Feedback : Reverse Causation



If there is a correlation between a treatment variable T and an output variable Y, then it is possible that either there is a causal relationship of the treatment T directly causing the output Y, or there is at least one third confounding variable Z that is causing both the treatment T and the output Y. These are the two options we have seen so far :

1.  T → Y

2.  Z → T , Z → Y

[](https://substackcdn.com/image/fetch/$s_!1RCr!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb96d45f0-bfb6-4bb8-99b3-28afbec90434_1516x970.png)

![](https://substackcdn.com/image/fetch/$s_!1RCr!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb96d45f0-bfb6-4bb8-99b3-28afbec90434_1516x970.png)





Wherever we are pretty sure about what the confounders are and can measure them, we saw that we can isolate their influence to get the direct causal effect. If identifying, measuring, and accounting for all confounders is not possible, we saw how to estimate the direct causal influence between a treatment and an output performance by exploiting the design of the treatment mechanism, and restricting the subgroup on which the effects of the treatment is to be evaluated. But, in all the analysis so far, we have missed one other possibility which we have not at all addressed.

This third possibility which is called **reverse causation** whose analysis will be the focus of the next article in this series. Reverse causation happens when the output itself is influencing the treatment. In some sense, the output itself is independently influencing the input treatment T. This phenomenon is called **feedback** in systems theory and in statistics where the output itself influences agents to change their treatment status.

[](https://substackcdn.com/image/fetch/$s_!ntHD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c5dccd6-56da-458e-a034-6c60974cd2f2_1492x680.png)

![](https://substackcdn.com/image/fetch/$s_!ntHD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c5dccd6-56da-458e-a034-6c60974cd2f2_1492x680.png)





Feedback happens when an outcome loops backward (as in the above diagram) to influence and alter the treatment status itself, creating a dynamic two-way loop rather than a simple one-way causal influence. Recognising this phenomenon is vital because many real-world systems are constantly evolving, where what we measure as an effect of a cause quickly turns around to influence the cause itself. This circular entanglement introduces severe simultaneity bias, breaking all models that we have seen far and masking true causal pathways unless specialised identification strategies are deployed. We will cover more advanced topics (more mechanisms and applications) in the next third article in this series among which feedback also will be one of them.

------------------------------------------------------------------------

Meanwhile, if you are interested in knowing about more articles I write, refer here. I write on both STEM and the humanities topics that interest me.

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

[](https://substack.com/profile/360871361-tusar-kar)

![Tuṣār Kar's avatar](https://substackcdn.com/image/fetch/$s_!TI95!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fefff33b6-31c6-4a95-8dc4-5678984e18d5_4080x3060.jpeg)

[](https://substack.com/profile/39655793-nahusha-acharya)

![Nahusha Acharya's avatar](https://substackcdn.com/image/fetch/$s_!V4mH!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F060d9b8c-aa8e-484f-9e37-837b84014b74_96x96.png)

[](https://substack.com/profile/367402-vijay)

![Vijay's avatar](https://substackcdn.com/image/fetch/$s_!nbNq!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc590aa5-6970-4789-a21d-04b3a53e9ae6_144x144.png)

6 Likes∙

[3 Restacks](https://substack.com/note/p-223978080/restacks?utm_source=substack&utm_content=facepile-restacks)



6





3

Share
