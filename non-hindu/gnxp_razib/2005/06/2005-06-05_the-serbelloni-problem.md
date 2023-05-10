+++
title = "The Serbelloni Problem"
full_title = "The Serbelloni Problem"
date = "2005-06-05"
upstream_url = "https://www.gnxp.com/WordPress/2005/06/05/the-serbelloni-problem/"

+++
Source: [here](https://www.gnxp.com/WordPress/2005/06/05/the-serbelloni-problem/).

The Serbelloni Problem

Having once fallen for the notorious Monty Hall puzzle, I was interested to find a similar-looking problem in John Maynard Smith’s Mathematical Ideas in Biology (1968):

Of three prisoners, Matthew, Mark and Luke, two are to be executed, but Matthew does not know which. He therefore asks the jailer ‘Since either Mark or Luke are certainly going to be executed, you will give me no information about my own chances if you give me the name of one man, either Mark or Luke, who is going to be executed’. Accepting this argument, the jailer truthfully replied ‘Mark will be executed’. Thereupon, Matthew felt happier, because before the jailer replied his own chances of execution were 2/3, but afterwards there were only two people, himself and Luke, who could be the one not to be executed, and so his chance of execution is only 1/2. Is Matthew right to feel happier?

JMS says ‘This should be called the Serbelloni problem since it nearly wrecked a conference on theoretical biology at the Villa Serbelloni in the summer of 1966’.

So: is Matthew right to feel happier?

At the end of the book JMS simply gives the answer to the problem as ‘No.’ But in the text (page 70) he says that the problem ‘yields at once to common sense or to Bayes’ theorem’.

Common sense is sadly unreliable in such cases, but let us take the hint about Bayes’ theorem. This provides a means of calculating the probability that a hypothesis is true in the light of a piece of evidence. In this case the hypothesis is ‘Matthew will be executed’, and the evidence is the jailer’s statement that ‘Mark will be executed’.

Bayes’ theorem can be expressed as h\|e = (h x e\|h)/e, where h\|e is the probability that the hypothesis is true in the light of the evidence, h is the antecedent probability that the hypothesis is true, e\|h is the conditional probability that the evidence will be observed if the hypothesis is true, and e is the probability that the evidence will be observed whether or not the hypothesis is true.

The name of Bayes is often associated with subjectivist interpretations of probability, but the terms in Bayes’ theorem can be given frequentist interpretations. The expression (h x e\|h)/e can then be interpreted as the long-term frequency with which both the hypothesis is true and the evidence is observed as a proportion of all cases in which the evidence is observed, in a large number of similar cases.

To calculate h\|e in the Serbelloni case we therefore need to know the antecedent probability that Matthew will be executed, the conditional probability that the jailer will say Mark is to be executed if Matthew is to be executed, and the unconditional probability that the jailer will say Mark is to be executed, whether or not Matthew is to be executed.

Unfortunately in the problem as stated these probabilities are not explicit, but we may reasonably assume from the wording that:

a\. initially each combination of possible outcomes is equally probable. There are three combinations: Matthew and Mark to be executed; Matthew and Luke to be executed; and Mark and Luke to be executed. Each prisoner therefore has a 2/3 chance of being executed and a 1/3 chance of surviving. Therefore h = 2/3

b\. If Mark and Luke are both to be executed, the jailer will give Matthew the name of one of them at random, with probability 1/2

c\. the jailer will not lie.

With these assumptions, e\|h is 1/2. The condition h is fulfilled if Matthew and Luke are to be executed, or if Matthew and Mark are to be executed. By assumption these events are equally probable. If Matthew and Luke are to be executed, the jailer cannot tell Matthew that Mark is to be executed (since the jailer does not lie). If Matthew and Mark are to be executed, the jailer is bound to say that Mark is to be executed. The conditional probability e\|h is therefore (1/2 x 0) + (1/2 x 1) = 1/2.

The unconditional probability of e is also (coincidentally) 1/2. There are two circumstances in which the jailer will say that Mark is to be executed: either, with probability 1/3, Matthew and Mark are to be executed, in which case e has a probability of 1, or, also with probability 1/3, Mark and Luke are to be executed, in which case there is a probability of 1/2 that the jailer will choose to give Mark’s name. The total probability of e is therefore (1/3 x 1) + (1/3 x 1/2) = 1/2.

Putting the various components together, we get h\|e = (2/3 x 1/2)/1/2 = 2/3. The antecedent probability of 2/3 that Matthew will be executed therefore is not changed by the information he is given, and he is wrong to feel happier.

This may seem at first sight inconsistent with the Monty Hall puzzle, where the probabilities do change when Monty opens one of the doors. But the two cases can be reconciled if we consider the probability that Luke will be executed. Suppose for example that Matthew wants to place a bet on who will survive, with the proceeds to go to his widow if he does not survive himself. Initially there is an equal 1/3 probability that each of the prisoners will survive. But if Matthew persuades the jailer into giving him Mark’s name as described in the Serbelloni problem, then the probability that Luke will survive increases to 2/3, and Matthew (or rather his widow) will stand to gain by betting on Luke’s survival rather than his own (given the same betting odds), since Matthew himself still only has a 1/3 chance of survival. This can also be shown using Bayes’ theorem, but I leave that as an exercise for the reader!

Added on June 7:

I have a suggestion for visualising the problem:

– draw three lines of equal length (say, 2 inches) in pencil. These can represent the number of times each of the three outcomes (Matt/Mark, Matt/Luke, Mark/Luke) will occur in a large number of similar cases

– now rub out parts of the lines representing those cases where the jailer does not say that Mark is to be executed. This means you have to rub out the whole of the Matt/Luke line and half of the Mark/Luke line.

– you are left with the whole of the Matt/Mark line (2 inches) and half of the Mark/Luke line (1 inch), totalling 3 inches. These represent the posibilities remaining after the jailer’s announcement. Mark is executed in all of these cases, Matt in 2/3 of them, and Luke in 1/3, which is consistent with the Bayesian conclusion.

As a matter of historical interest, the Serbelloni problem seems to pre-date the Monty Hall puzzle. The latter became notorious around 1990, though I have found a reference to it in the 1980s. But the Serbelloni problem goes back at least to 1966, the date of the conference. However, in a slightly different form it is also to be found in a puzzle by Martin Gardner in 1959. In Gardner’s version the prisoner and the jailer have an argument about whether he should give him the information.

Posted by David B at [03:05 AM](https://www.gnxp.com/MT2/archives/004048.html) [](http://js-kit.com/api/static/pop_comments?ref=http://gnxp.com&path=/4048?url=http://www.gnxp.com/MT2/archives/004048.html&thetime=%20060505&MT=true)

### Related Posts:

- [Mirror neurons not all
  that?](https://www.gnxp.com/WordPress/2009/06/02/mirror-neurons-not-all-that/) - [More Financial
  Morons](https://www.gnxp.com/WordPress/2009/02/25/more-financial-morons/) - [Conformity scorned, the dangers of within
  group…](https://www.gnxp.com/WordPress/2009/05/26/conformity-scorned-the-dangers-of-within-group-criticism/) - [Skewing my
  winnings](https://www.gnxp.com/WordPress/2012/09/29/skewing-my-winnings/) - [What does Mark Thoma
  mean?](https://www.gnxp.com/WordPress/2007/06/06/what-does-mark-thoma-mean/) - [10 Questions gets you interviewed
  elsewhere!](https://www.gnxp.com/WordPress/2006/09/14/10-questions-gets-you-interviewed-elsewhere/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2005%2F06%2F05%2Fthe-serbelloni-problem%2F&linkname=The%20Serbelloni%20Problem "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2005%2F06%2F05%2Fthe-serbelloni-problem%2F&linkname=The%20Serbelloni%20Problem "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2005%2F06%2F05%2Fthe-serbelloni-problem%2F&linkname=The%20Serbelloni%20Problem "Email")[](https://www.addtoany.com/share)
