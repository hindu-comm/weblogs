+++
title = "Good Point?"
full_title = "Good Point?"
date = "2007-07-04"
upstream_url = "https://www.gnxp.com/WordPress/2007/07/04/good-point/"

+++
Source: [here](https://www.gnxp.com/WordPress/2007/07/04/good-point/).

Good Point?

Suppose that:

a\) intelligence is partly inherited

and

b\) less intelligent people on average have more children.

Does it follow that:

c\) the average intelligence of the population will decline from one generation to the next?

A simple example, due to the statistician [I. J. Good](https://en.wikipedia.org/wiki/I._J._Good), shows that this is not necessarily the case. \[Note 1\]

Let H stand for High and L for Low intelligence (or any other trait). Let PG stand for the parental generation and O for offspring. (The parental generation should not be confused with parents. Not all individuals in the parental generation are necessarily parents.) Let the numbers of offspring in the categories H and L be as follows, with the numbers of the parental generation in square brackets:

………………OH…….OL……Totals  
\[100 PGH\] 28……..18…….. 46  
\[900 PGL\] 72……882……954  
Totals…….100…..900…..1000

This simple example satisfies assumptions (a) and (b), but not the conclusion (c). The proportions of H and L in the population do not change from one generation to the next. I will call any 2-class system with these properties a ‘Good model’.

I draw attention to Good’s little model because it does not seem to be widely known. For example, Richard Lynn has written an entire book, Dysgenics, on the threat of falling intelligence due to differential fertility, but does not refer to Good’s article. Neither do Murray and Herrnstein in The Bell Curve. I came across it myself [here](http://www.juliansimon.com/writings/Articles/PRESTON3.txt), when I was searching for references to another article on the same theme.

That other article is by Samuel Preston and Cameron Campbell. \[Note 2\] Preston and Campbell present a far more elaborate and mathematically sophisticated model than Good. This is not because they are better mathematicians than Good (few people are!), but because they are aiming to give a realistic model of actual populations. Unfortunately it is so complicated that neither the authors nor their critics seem to understand what is going on. I think that Good’s little model is more useful for analysing the essential issues. There is no advantage (unless the aim is obfuscation) in bringing in Markov chains, primitive matrices, eigenvectors, and the like, if the same points can be made with arithmetic and simple algebra.

Good’s model shows that assumptions (a) and (b) do not imply conclusion (c). It does not follow that conclusion (c) is false. It may be that with additional reasonable assumptions, the conclusion can still be drawn. I discuss this in the continuation.

(Warning: this is a long piece aimed more at people searching for discussions of Preston and Campbell’s theories than at casual browsers.)

\[**Added on 6 July**: I should probably have said here, upfront, that ultimately I reject Preston and Campbell’s model. I should also have emphasised that I. J. Good was only concerned to show that some loose arguments about intelligence are fallacious, whereas Preston and Campbell really believe that their ‘equilibrium’ model of intelligence is usually correct. But I should also have pointed out that there could be other ways of achieving equilibrium, so that rejecting Preston and Campbell does not necessarily mean rejecting equilibrium. Notably, many years ago the geneticist Lionel Penrose outlined a model in which heterozygote advantage maintains an equilibrium distribution of IQ despite greater fertility of the less intelligent. Roughly speaking, in his model the highly intelligent have low fertility, the less intelligent have high fertility, but the really stupid (who are homozygotic for ‘stupidity genes’) have very low fertility, which acts to purge ‘stupidity genes’ from the gene pool. (These are not Penrose’s own terms!) As a twist to this which I have seen suggested somewhere, individuals who are homozygous for a lot of ‘stupid’ genes may have low fetal viability, so the ‘purging’ could be prenatal.)\]

**Good’s Example Discussed More Fully**  
**  
**First, a few more comments on Good’s own example. Good himself emphasises that his example is not biologically realistic, and his aim is only to show that certain loose arguments are invalid.

Good presents his figures in terms of fathers and sons, but this is not essential to the model, so I have referred more generally to parents and offspring. Reproduction within the model could be either sexual or asexual, and mating could be random, assortative, or disassortative. The only special problem arising with biparental inheritance is how to deal with offspring of one H and one L parent. The obvious solution in this case is to assign half of each offspring to the H parent and half to the L parent. It does not matter if this occasionally results in fractional numbers of offspring.

Good himself defines his two classes as ‘Intelligent’ and ‘Unintelligent’. The conclusion that the distribution of intelligence is unchanged assumes either that these are uniform discrete values, or that each class covers a range of values with an unchanging mean.

Of course, a division of intelligence into just two categories, High and Low, is hardly realistic. Good himself describes it as ‘much oversimplified’ , but it would be superficial to reject the model on that account. The same essential features can be shown to apply in a model with any number of categories. (Effectively, this is what is done by Preston and Campbell.) There is no reason to doubt that at the limit it would apply to a continuous distribution.

In Good’s figures the offspring of H parents are on average more intelligent than those of L parents, as required by assumption (a). For example, if we give H the value 1 and L the value 0, the average intelligence of the offspring of H parents is 28/46 = .61, while the intelligence of the offspring of L parents is far lower at 72/954 = .075. These values are based on the particular choice of H = 1, L = 0, but the rank order would be the same with any other values, provided H is greater than L. It is also interesting to see what would be the average intelligence of the offspring if H and L parents reproduced with equal fertility, which I will call the ‘Equal Fertility Variant’. With Good’s figures (assuming that the pattern of inheritance is otherwise the same) this comes out as .128. Setting out in order the mean intelligence of all relevant groups, we have:

High Parents: 1  
Offspring of High Parents: .61  
Equal Fertility Variant: .128\*  
Parental Generation: .1  
All Offspring: .1  
Offspring of Low Parents: .075  
All Parents: .046\*\*  
Low Parents: 0

\*this is the mean intelligence of all offspring on the assumption that H and L parents have equal fertility, and that the ratios of H and L among their offspring are as in Good’s model.  
\*\*this is the mean intelligence of parents counting the parents once for each offspring. There are 46 offspring of H parents, with value 1, and 954 offspring of L parents, with value 0, so the average is 46/1000 = .046.

In Good’s figures the offspring of both H and L parents are therefore more intelligent than the average of all parents, weighted by the number of offspring (not to be confused with the average of the parental generation), but those of H parents are more markedly so. I have calculated the correlation coefficient for intelligence between parents and offspring, and it comes out at the moderate figure of .37. \[Note 3\]

So far as fertility is concerned, L’s in the parental generation are more fertile than H’s, which satisfies assumption (b). Each individual in the PG L class has on average 954/900 = 1.06 offspring, while for PG H’s the number is only 46/100 = .46, less than half that of L’s. It is not possible to calculate a correl  
ation between intelligence and fertility, since we do not know the variance of fertility within groups, but there is clearly a negative correlation; that is, high intelligence tends to go together with low fertility, and vice versa.

It will be noted that the offspring of H’s are on average less intelligent and those of L’s more intelligent than their own parents. This may be regarded as an instance of regression towards the mean. Using Good’s figures I have calculated that the coefficient of regression of offspring on their parents is about .53. (This is higher than the correlation coefficient of .37 because the parents have a lower variance than the offspring.) The extent of regression towards the mean is paradoxically greater the lower the regression coefficient (one of the drawbacks of the established terminology), and a regression coefficient of .53 means that the offspring regress slightly less than halfway towards the mean. This is not an unreasonable figure.

It is more questionable that the average intelligence of all offspring (and even the offspring of L parents) is higher than that of all parents. It is also noteworthy that the average intelligence of offspring in the absence of differential fertility would be higher than either the average for actual parents or for the entire parental generation.

It is evident that if the same patterns of reproduction were to continue, generation after generation, then the proportions of H and L in the population would be unchanged, despite the continued greater fertility of L parents. The crux of the matter is whether it is biologically realistic to expect the same patterns of reproduction to continue indefinitely.

**The General Properties of Good Models**  
  
But first I want to examine in more general terms the properties of Good models. There is nothing sacrosanct about Good’s own figures. Here is a version with nice round numbers:

……………..OH……..OL……..Totals  
\[500 PGH\] 300….100…….400  
\[500 PGL\] 200…..400…..600  
Totals……..500….500… 1000

This has the essential features that it is consistent with assumptions (a) and (b) but is a counterexample to the conclusion (c).

Using the values H = 1 and L = 0, the mean intelligences are as follows:  
High Parents: 1  
Offspring of High Parents: .75  
Equal Fertility Variant: .542  
Parental Generation: .5  
All Offspring: .5  
All Parents: .4  
Offspring of Low Parents: .33  
Low Parents: 0

With these figures the mean intelligence of the offspring of L parents is lower than that of all parents, unlike in Good’s case. This shows that the contrary position is a peculiarity of Good’s figures, not an essential feature of Good models.

It is natural to ask whether there is a systematic procedure for constructing Good models, and whether any general conclusions can be drawn about the range of possible parameters.

The essential structure of a Good model is a 2 x 3 table. There are 4 ‘cells’ for the numbers of offspring and 2 for the numbers in the parental generation. In the absence of any other constraints each of the 6 numbers can be chosen independently of all the others. In technical terms the table therefore has 6 degrees of freedom.

Various other quantities can be derived from the 6 key numbers. Obvious examples are the row and column totals. Two other quantities of particular interest are the proportion of offspring who are in the same class as their parents, which I will call the Continuity Rate; and the ratio between the number of offspring and the number in the parental generation, which I will call the Fertility Rate. To satisfy assumption (b) the Fertility Rate of the L class must be higher than that of the H class. Good’s own model also assumes that the total size of the population is constant. While this is not essential, it is convenient.

To construct a Good model we need to eliminate 6 degrees of freedom (DFs) and thereby fix values for the 6 key numbers. This could be done directly by inserting 6 numbers in the table, but usually we want to impose certain desired constraints, such as a given ratio between H and L. We therefore require 6 independent constraints to eliminate 6 DFs. The requirement of ‘independence’ can be tricky. For example, it might seem that if we insert all 4 row and column totals for the offspring, we have eliminated 4 DFs, which is sufficient to determine the 4 cell entries for the offspring. But in fact the row and column totals have only 3 DFs, since the sum of the row totals must equal the sum of the column totals. We therefore need to impose at least one additional constraint to obtain the cell entries.

Not all possible combinations of parameters have physically possible solutions. For example, if we stipulate that the Fertility Rate of the L class is 1.5, and that the Continuity Rate of L is .7, then the number of L offspring of L parents will be 1.5 x .7 = 1.05 times the total number of L’s in the parental generation. It is therefore impossible to satisfy the equilibrium condition that the number of L’s does not change from one generation to the next, since this could only be achieved if H parents had a negative number of L offspring, which is impossible. We cannot accept a solution in which any of the 6 key numbers in the table are negative.

Subject to these cautions, it is easy and mildly amusing to play around with different parameters. In each case we need to impose constraints in 6 steps to eliminate 6 DF’s. In Note 4 I give four examples to illustrate some general points.

**A Formula for Equilibrium**  
  
For those who do not want to play around with tables, the conditions for equilibrium can be summed up in a formula. I will use the following abbreviations:

N is the total population size, which we assume is constant.  
H1 is the number of H individuals in the parental generation.  
H2 is the number of H individuals in the offspring generation.  
O’H is the number of offspring of H individuals.  
R’H is the fertility rate of H, which we define as equal to O’H/H1.  
A is the Continuity Rate of H (the proportion of the offspring of H individuals who are themselves H).  
B is the proportion of the offspring of L individuals who are H (which equals 1 minus the Continuity Rate of L).

It follows from these definitions that the number of H individuals in the offspring generation is H2 = AR’H.H1 + B(N – R’H.H1). But the condition of equilibrium is that H2 = H1, so we have H1 = AR’H.H1 + B(N – R’H.H1). With a little rearrangement this can be expressed as H1 = BN/\[1 – (A – B)R’H\].

We therefore have a formula for calculating the equilibrium value of H1 for given Fertility Rates and Continuity Rates. From inspection of this formula it will be seen that the equilibrium level of H will generally be higher when the Fertility Rate of H is higher, and when the proportions of H among offspring are higher, though the balance between A and B is also significant.

**General Conclusions about Good Models**

To sum up some general conclusions about Good models:

a\) equilibrium solutions exist for a wide range of parameters, provided they are not so extreme as to lead to negative numbers of offspring in any category.

b\) if an equilibrium solution exists, it is unique (as there are no squares or higher powers in the equilibrium formula)

c\) if the system is out of equilibrium, it will move towards equilibrium, provided fertility rates and continuity rates are constant from one generation to another. (See Example 4 in Note 4.)

d\) it is a general feature of Good models that if the fertility rate of L is greater than that of H, then in equilibrium the average intelligence of offspring must be higher than that of their own parents. The reason is simply that if L parents are a higher proportion of parents than  
the proportion of L in the whole parental generation, then the average intelligence of parents is lower than that of the parental generation. But by the equilibrium assumption this is the same as that of all offspring, so the average intelligence of all offspring must be higher than that of their own parents.

e\) If in equilibrium the fertility rate of L is greater than that of H, then the average intelligence of offspring under the Equal Fertility Variant would be higher than that of the parental generation. This is because under the EFV we would be increasing the proportion of H parents, whose offspring on average have higher intelligence. The average intelligence of the offspring will therefore be higher than under the scenario with differential fertility. But by assumption in this scenario the intelligence of the offspring is the same as that of the parental generation. Therefore under the EFV the average intelligence of offspring would be higher than that of the parental generation. The same principle can easily be extended to a system with more than two classes of intelligence.

**Preston and Campbell**  
  
Having discussed Good’s model at such length, I can deal much more quickly with Preston and Campbell’s approach. (I have read their original article, but I will rely here mainly on a more accessible article by Preston \[Note 5\].) P & C’s two main differences from Good are that they use a larger number of classes of intelligence (7 instead of just 2), and they allow explicitly for biparental inheritance. In principle, the father and mother can each come from any of the 7 classes, with a stated probability, so that there are altogether 7 x 7 = 49 possibilities to be dealt with. However, in practice P & C deal mainly with the simple case of assortative mating within the classes.

P & C appear to be unaware of Good’s model, but Preston’s article begins with a 2-class example which can easily be put into a Good-type table as follows (rounded to whole numbers):

…………OH…….OL…..Totals  
\[40 PGH\] 22…..6…….28  
\[60 PGL\] 18…. 54……72  
Totals…..40…. 60….100

It will be seen that this has all the essential features of a Good model. I note in particular that, as in a Good model, the offspring under the EFV would have average intelligence higher than that of the parental generation.

In the more elaborate 7-class model P & C use the methods of matrix theory to reach some general theorems about the behaviour of the system over an indefinite number of generations. Their key assumptions are that fertility rates are fixed; that the probabilities of offspring falling into a given intelligence class depend only on the intelligence of their parents; and that these probabilities are the same in any generation. With these assumptions, they prove that the system will always result eventually in a constant equilibrium distribution. After our consideration of Good models, there should be nothing surprising in this conclusion.

**Biological Objections**  
  
I now move on at last to consider whether a Good (or P-C) model is biologically plausible or even possible.

First, I deal briefly with a possible objection to such models based on a theorem of quantitative genetics known as the [Breeders’ Equation](https://www.gnxp.com/blog/2005/11/response-heritability-and-selection-r.php).

This can be expressed as:  
R = h²S  
where R is the response to selection, measured by the difference between the mean of the offspring of selected parents and the mean of the parental generation, h² is ‘narrow heritability’, as measured by the regression of offspring on parents, and S is the average deviation of the selected parents from the mean of the parental generation. \[Note 6\] If h² and S are both non-zero, then R cannot be zero. In a Good model it seems that h² and S are both non-zero, but that R is zero, since there is no difference between the mean of the offspring of selected parents and the mean of the parental generation. How can this be?

The short answer is that the derivation of the Breeders’ Equation in its usual form makes various assumptions which are not satisfied in Good models. Notably, it assumes that the mean and variance of the offspring of unselected parents are the same as those of the parental generation. But in Good models this is not the case. If we want to use the Breeders’ Equation for a Good model the response to selection needs to be measured in relation to what the mean of the offspring would have been in the absence of selection (in my terms, the EFV).

There remain several respects in which Good or Preston-Campbell models seem biologically implausible or problematic. I distinguish these as follows:

a\) in equilibrium the intelligence of offspring is on average higher than that of their own parents;

b\) the average intelligence of offspring under the EFV is higher than that of the entire parental generation;

c\) the assumption, built into any model with a fixed number of values, that there are upper and lower limits to intelligence;

d\) the assumption that the intelligence of offspring is influenced only by that of their parents, and not their more remote ancestry;

e\) the assumption that the same patterns of inheritance can continue in equilibrium indefinitely.

I consider these aspects in turn.

a\) As noted earlier, the offspring of H’s are on average less intelligent and those of L’s more intelligent than their own parents. This is not in itself unreasonable, as a result of regression towards the mean. In combination with the higher fertility of L parents, regression may well have the consequence that the average intelligence of offspring is higher than that of parents. For example, let us suppose that the offspring of L and H parents show the same average amount of regression towards the mean. It can be shown that if L parents are more fertile, the mean intelligence of the offspring will be higher than that of their parents, weighted by their number of offspring. To illustrate the process, suppose the population is divided equally into people 6 feet tall and 5 feet tall. Suppose that the offspring of the 6-footers are on average 5’10” tall, while those of the 5-footers are 5’2″ tall. The extent of regression towards the mean, in units of height, is therefore 2 inches in both cases. Now suppose that the 5-footers have twice as many offspring as the 6-footers. For example, suppose there are 600 potential parents, of whom the 300 short individuals have 400 offspring, while the 300 tall individuals have 200 offspring. The mean height of the parents (weighted by the number of offspring) is \[(400 x 5′) + (200 x 6′)\]/600 = 3200’/600 = 5’4″, while the mean height of the offspring is \[(400 x 5’2″) + (200 x 5’10”)\]/600 = 3233’/600 = 5’4.7″. The average height of the offspring is therefore about three-quarters of an inch greater than that of the parents (counting each parent once for each child). Given the phenomenon of regression towards the mean, combined with differential fertility, it is therefore quite possible for point (a) to be satisfied. Of course, not every pattern of regression that is mathematically possible would be biologically realistic. However, I do not see anything biologically unreasonable about the patterns of regression required to satisfy point (a).

b\) The fact that average intelligence of offspring under the EFV is higher than that of the entire parental generation seems to me a more serious difficulty with Good models (and the more elaborate Preston-Campbell versions). It is equivalent to saying that if everything else (all environmental and genetic conditions) were the same, but that each individual had one offspring (or each couple two offspring), then the average intelligence of the population would rise. This is surprising. Of course, if environmental conditions were to change,  
for example through improvements in nutrition or education, then a rise in average intelligence would be plausible, but the whole point of Good models is to show that the distribution of intelligence can be in equilibrium without such changes. It is remarkable that neither Good, Preston and Campbell, nor Preston and Campbell’s various critics, seem to have noticed this paradoxical situation. In Preston and Campbell’s case this is partly due to the complexity of their model, which obscures its underlying features, but also to the fact that they make use of empirical data derived from a study carried out in the 1960s. A ‘Flynn Effect’ increase in IQ is built into these figures, which makes them useless for exploring the general case where no such increase is in progress. I do not assert that point (b) is biologically impossible. There may be some scenarios in which, following cessation of selection, the average intelligence of the population would increase, for one or a few generations, until a new equilibrium is reached. The effects of genetic dominance and epistasis depend on the frequency of the relevant genes in the population, and on the systems of mating, so it is possible that a change in the frequency of certain genes or mating types, due to the ending of differential fertility, would raise average intelligence beyond that of the parental generation. But neither Good not Preston and Campbell appeal to any such phenomena, and I think the burden of proof is on the exponents of their models to come up with plausible genetic scenarios.

c\) Julian Simon, in the note which draws attention to Good’s little example, has stressed the role of a lower limit to intelligence in producing equilibrium. He points out that if there is such a lower limit, and if there is a non-zero probability that the offspring of low intelligence parents will have higher intelligence, then there will be an equilibrium level somewhat higher than the lower limit. I would agree that this is one way of producing an equilibrium, but I do not think it is the only way. While I have not worked out the details, I think it would be possible to have an equilibrium system, incorporating differential fertility, in which the intelligence of offspring is normally distributed (and therefore in principle with no upper or lower limits) around an appropriately regressing mean for each class of parents.

d\) The assumption that the intelligence of offspring is influenced only by that of their parents, and not their more remote ancestry, cannot be strictly true in the case of dominant and recessive gene effects. Preston and Campbell recognise this as a weakness of their model but do not see it as a major problem. I am inclined to agree. While I don’t have a proof, I think that the essential features of Good or P-C models could be found in a more complicated model where the intelligence of offspring is affected by more than two ancestors (i.e. the parents).

e\) The most serious problem is the assumption that the same patterns of inheritance can continue unchanged indefinitely, despite continued differential fertility. If high and low intelligence were determined purely by environmental factors, this would be less surprising. It would be reasonable to suppose that the average quality of environments encountered by offspring is not affected by selection in previous generations. (I say ‘reasonable’, not certain, because one could imagine that environments deteriorate cumulatively as a consequence of declining parental intelligence.) In contrast, if high and low intelligence are determined partly by genetic factors, then they will be affected by the genetic composition of the population. This will change cumulatively as a result of selection. These changes will be permanent, in the absence of reversed selection (neglecting the small effects of mutation and genetic drift). If less intelligent parents are more fertile, then the frequency of genes associated with low intelligence will increase. Each such gene will contribute to a certain average expected value of intelligence (under constant environmental conditions). The effect of an increase in the frequency of genes for low intelligence should be to reduce the average expected intelligence of offspring to a lower level than would otherwise have been the case. One would therefore usually expect the average intelligence of the population to fall as a result of differential fertility, even if, as a result of regression towards the mean, the average intelligence of the offspring after selection is higher than that of their own parents. As discussed under point (b) it is conceivable \[**added**: actually, I am not sure it is conceivable, but I concede the point for the sake of argument\] that, due to some unusual genetic scenario, the average intelligence of the population may be sustained at its original level for a few generations, but this can hardly continue indefinitely if differential fertility also continues. There is an analogy with the heating of a liquid: as it reaches boiling point the temperature may remain constant for a certain period as heat is absorbed (so-called ‘latent’ heat), but if the heating continues the liquid will eventually begin to boil. Similarly, as the proportion of genes associated with low intelligence rises, individuals will be carrying an increasing number of genes with latent negative effects on intelligence. To take an example from eye colour, if parents with blue eyes (a recessive trait) have persistently higher fertility than parents with brown eyes, then the proportion of ‘blue eye’ genes in the population will steadily increase. Even though the offspring of blue-eyed parents will often have brown eyes (assuming random mating between blue and brown eyed parents), the probability of homozygosity for ‘blue’ genes will increase, and the probability that parents (whether blue or brown eyed) will have blue-eyed offspring will also rise. Initially the effect may be slight (if ‘blue’ genes are initially rare), but ultimately blue eyes would still drive out brown. The same principle would apply in the case of epistatic effects. The objection to Preston and Campbell’s model is ultimately quite simple: by assuming constant patterns of inheritance, they are implicitly excluding the effect of changes in gene frequencies. They are therefore prejudging one of the main points at issue.

The surprising thing is not that Preston and Campbell’s argument is flawed, but that the existence of some flaw was not obvious to the authors themselves. As Richard Lynn tersely commented, ‘it \[Preston and Campbell’s article\] attempts to prove mathematically that Darwin’s theory of evolution does not work’. \[Note 7\] Why then did Preston and Campbell not themselves see that something must be wrong? I can only speculate about this. It may be partly due to an misplaced respect for mathematics: having shown by sophisticated methods that something is mathematically possible, Preston and Campbell gave too little attention to their underlying assumptions. But I suspect the main reason is in their disciplinary background, which is apparently in demography. Demographers have developed methods for analysing the transition between social or occupational classes. For example, the offspring of farmers are themselves often, but not always, farmers, and demographers have devised methods to analyse how occupational classes like farmers can be stable in size despite differences in fertility. Preston and Campbell have applied these methods to the case of intelligence. The assumptions they adopt may well be quite appropriate to demographic problems, where genetic inheritance is often either irrelevant or negligible. The same assumptions are misconceived when applied to traits where genetic heritability is (or may be) substantial.

Note 1: I. J. Good, “Fallacies, Statistical” in Encyclopedia of the Social Sciences, Vol. 5, p.292-300.

Note 2: Samuel H. Preston and Cameron Campbell, ‘Differential Fertility and the Distribution of Traits: the case of IQ’, American Journal of Sociology, 98  
, 1993, 997-1019, with comments by James S. Coleman and David Lam and reply by Preston and Campbell, pp.1020-43.

Note 3: to calculate a Pearson product-moment correlation coefficient, we may assign arbitrary values to H and L. It will be found that these cancel out in the final calculation, so the correlation is not affected by the choice of values. Some parents will have more than one offspring, in which case each parent-offspring pair should be counted in the covariance, and in the standard deviation of parents they should be counted once for each offspring.

Note 4:

Example 1

The key assumptions in this example are (a) equilibrium in intelligence levels (b) unequal numbers of H and L, and (c) the offspring of H and L have an equal probability of being in the same class as their parents. The main point of interest is to see what fertility rates arise from these assumptions.

Step 1: The total in the parental generation is 1000.  
Step 2: The total of offspring is also 1000.  
Step 3: There are 400 H’s in the PG. Therefore there are 600 L’s.  
Step 4: As we are assuming equilibrium, there are 400 H’s among the offspring. Therefore there are 600 L’s.  
Step 5: Among the offspring of H, H and L are in the ratio 7:3.  
Step 6: Among the offspring of L, H and L are in the ratio 3:7. We can then calculate the row totals for the offspring. If we set the row total for H as X, the row total for L is (1000 – X). To obtain the value of X we can use the ratios stipulated in steps 5 and 6. These imply that .7X + .3(1000 – X) = 400, so we have X = 250. The rest of the table then follows easily, and we get:

……………..OH……….OL…….Totals  
\[400 PGH\] 175…… 75…….250  
\[600 PGL\] 225…..525……750  
Totals…….400…..600…..1000

The fertility rates come out as .625 for H and 1.25 for L.

Example 2

In this example we assume equal fertility for H and L, and explore what this implies for the proportion of offspring who are in the same class as their parents.

Steps 1 to 4: as in Example 1.  
Step 5: With equal fertility, and a constant population size, the total number of offspring of H parents must be the same as the number of H parents, i.e. 400. Therefore the total number of offspring of L parents is 600. (Note that we are only losing one DF, not two.)  
Step 6: It still remains to eliminate one DF. I choose to fix the proportion of offspring of H who are also H at .7.

This gives us the following table:

……………….OH…….OL……..Totals  
\[400 PGH\] 280….120……400  
\[600 PGL\] 120…..480……600  
Totals…….400….600…..1000

The proportion of offspring of L who are also L is now 480/600 = .8, instead of .7 as previously.

Example 3

In this example I treat the numbers of H and L in the parental generation as unknowns, and derive them from the other parameters.

Steps 1 and 2: As in Example 1.  
Step 3: The number of offspring who are H is to be the same as the number of H in the parental generation. Designate this number as X. The corresponding numbers of L are therefore 1000 – X  
Step 4: I assume a fertility rate of 1.1 for L.  
Step 5: I assume a fertility rate of .8 for H. With these fertility rates, and a total offspring number of 1000, X = 333.  
Step 6: I assume that among the offspring of H, H and L are in the ratio 6:4.

These assumptions give the following table:

……………….OH……OL…….Totals  
\[333 PGH\] 160…..106…..266  
\[667 PGL\] 173……561…..734  
Totals…… 333…..667… 1000

Example 4

Examples 1-3 all assume that the system is in equilibrium, with the numbers of L and H among the offspring equalling those in the parental generation. In Example 4 we explore what happens when the system is out of equilibrium. To do this I will take the figures of Example 1 and vary one of the parameters so that the system is no longer in equilibrium.

Steps 1 to 3: as in Example 1.  
Step 4: We could vary any of the other parameters of Example 1. I choose to vary the fertility rates, and take the fertility rate for L as 1 instead of 1.25. It follows that the fertility rate for H is also 1.  
Steps 5 – 6: As in Example 1.

The resulting table is as follows:

……………….OH……..OL……Totals  
\[400 PGH\] 280…..120……..400  
\[600 PGL\] 180……420…….600  
Totals…….460…….540……1000

It will be seen that the numbers of H and L offspring no longer equal the numbers in the PG. If we insert the offspring numbers as the PG numbers in the next generation, and apply the same constraints as before, we get the following:

…………………OH……..OL……Totals  
\[460 PGH\] 322……..138…..460  
\[540 PGL\] 162……..420……540  
Totals…….484……..516…..1000

It will be seen that the offspring numbers are still out of equilibrium, but they appear to be converging on 500 for both H and L. Given the symmetry of the fertility rates and proportions of H and L among the offspring, it is easy to see that the system will be in equilibrium if a 500:500 ratio is reached.

Note 5: Samuel H. Preston, ‘Differential Fertility IQ and the IQ Distribution of a Population’ in The Rising Curve, ed. Ulric Neisser, 1998, p.377-89.

Note 6: For details see D. S. Falconer, Introduction to Quantitative Genetics, 3rd edn., p.188-92.

Note 7: Richard Lynn, Dysgenics: Genetic Deterioration in Modern Populations, 1996, p200. Unfortunately Lynn, while seeing that something must be wrong with P & C’s model, does not engage with it in detail.

### Related Posts:

- [Fisher web](https://www.gnxp.com/WordPress/2006/02/27/fisher-web/) - [A smarter
  population?](https://www.gnxp.com/WordPress/2006/09/07/a-smarter-population/) - [New Paper from the Journal of Bogus
  Sociology](https://www.gnxp.com/WordPress/2006/06/05/new-paper-from-the-journal-of-bogus-sociology/) - [IQ and Higher
  Education](https://www.gnxp.com/WordPress/2008/06/08/iq-and-higher-education/) - [R. A. Fisher on Inclusive Fitness
  (again)](https://www.gnxp.com/WordPress/2008/11/23/r-a-fisher-on-inclusive-fitness-again/) - [You only go extinct
  once....](https://www.gnxp.com/WordPress/2006/10/29/you-only-go-extinct-once/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F07%2F04%2Fgood-point%2F&linkname=Good%20Point%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F07%2F04%2Fgood-point%2F&linkname=Good%20Point%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F07%2F04%2Fgood-point%2F&linkname=Good%20Point%3F "Email")[](https://www.addtoany.com/share)
