+++
title = "George Price, Group"
full_title = "George Price, Group Selection, and Altruism"
date = "2011-04-10"
upstream_url = "https://www.gnxp.com/WordPress/2011/04/10/george-price-group-selection-and-altruism/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/04/10/george-price-group-selection-and-altruism/).

George Price, Group Selection, and Altruism

This concludes a series of posts on the work of George Price. For the most recent one, with links to the others, see [here](https://www.gnxp.com/wp/2010/11/04/evaluating-prices-equation/)\*. This final post covers the subject of group selection.

**Price and Group Selection**

The application of Price’s Equation to group selection, and the related problem of biological altruism, is largely responsible for the current interest in Price, as shown in Oren Harman’s biography. The controversy over group selection dates from the early 1960s, as discussed [here](https://www.gnxp.com/wp/2011/01/15/the-meaning-of-group-selection/)\*. Price attempted to cut through the controversy with a simple new approach. Using Price’s Equation, the overall change in frequency of a gene in a population between two generations can be broken down into two components, which I call the Covariance and Transmission terms. Price’s simple proposal was to identify the effect of group selection with the Covariance term, while selection on individuals (or genes within individuals) is covered by the Transmission term \[Price, 1972, 488\]. Price’s own work was cut short by his untimely death, but his approach received a boost when it was endorsed (with some qualifications) by W. D. Hamilton \[*Narrow Roads*, vol.1, 333\]. Yet it failed to attract much interest for another decade, and is still not generally accepted.  

The issues raised are partly semantic: what do (or should) we mean by ‘group selection’? Some biologists, like the late John Maynard Smith, think it is important to draw a sharp distinction between group selection and kin selection. Since Price’s approach makes no such distinction, it has little attraction to these biologists. But there is also a more technical problem with the Price-Hamilton approach. As I discovered for myself when working through some numerical examples, the Covariance term (if it is not zero) will be affected by a factor which can only reasonably be described as individual selection, and which may in extreme cases account for most or all of the term. The division between ‘group’ and ‘individual’ selection is therefore not as clear as Price himself seems to have believed. On searching the literature I find that this point has been sporadically recognised at least since 1985, but it still does not seem to be sufficiently emphasised. For the moment, however, I will assume that the blurring of individual and group effects is small enough to be neglected. Making this assumption, how useful is Price’s Equation in clarifying the issues involved in the controversy over group selection?

**Applying Price’s Equation to group selection**

Group selection is explicitly dealt with only in Price’s 1972 paper, where he derives what I have called Price’s Second Equation. Unlike the First Equation, this can be applied to groups that are unequal in size. Against this advantage, it is more complicated than the First Equation, and it involves statistical functions (such as weighted covariances) whose meaning is not intuitively clear. For the purpose of analysing the concept of group selection I will therefore make the simplifying assumption that groups are of equal size. We may then use Price’s First Equation, in the knowledge that via the Second Equation the conclusions can be generalised to groups of unequal size.

Price’s First Equation, as published in 1970, can be expressed as:

\[1\] dQ = cov(z,q)/Z + Sz\[i\]dq\[i\]/NZ.

In the 1970 paper this equation is applied only to populations of individual organisms, but it is valid for any interpretation consistent with the conditions under which it is derived. It can be applied, with only minor modifications, to the case of group selection, provided the groups are of equal size in the first generation. We may interpret the population as being divided into N groups, indexed by the numbers 1, 2…i…N, each containing equal numbers of individuals. There is no migration or interbreeding between groups. The gene frequency of the relevant gene in the i’th group in generation 1 is designated by q\[i\], and the number of offspring of that group’s members is designated by z\[i\]. S indicates summation, and cov(z,q) is the covariance between z and q. The mean number of offspring Z is the average of z\[i\] over all groups (Sz\[i\]/N). dq\[i\] is the change in the frequency of the gene within the i’th group, and dQ the change in the population frequency of the gene, between generations 1 and 2.

When the equation is applied to sub-groups of a population, rather than to individuals, the size of the Covariance term depends on the relationship between the aggregate fitness of each group and the frequency of the relevant gene in that group. If groups with a high frequency of the gene (relative to the population average) also have a higher-than-average number of offspring, while groups with a low frequency have fewer offspring, then the term will be positive. Conversely, if groups with a high frequency of the gene have a lower-than-average number of offspring, while groups with a low frequency have more offspring, then the term will be negative. In contrast, the size of the Transmission term depends on the relative fitness of the gene within groups. If, for whatever reason, the frequency of the gene within groups (averaged over groups) is increasing, then the Transmission term will be positive; while if it is decreasing the term will be negative.

W. D. Hamilton was apparently the first to point out that the equation could be applied hierarchically to groups within groups within groups, etc. In equation \[1\] the second term on the RHS contains the expression dq\[i\] for the change in frequency of the gene within the i’th group. But if the i’th group itself contains sub-groups, the change in frequency within the group can be expressed by means of equation \[1\] itself. (As a special case, a diploid individual can be treated as a ‘group’ with the two genes at the relevant locus as its ‘members’.) In principle there is no limit to the number of ‘levels of selection’ that can be treated in this way. This is a major theoretical attraction of the Price-Hamilton approach, though in practice uses involving more than two levels of selection appear to be rare.

**Advantages of Price’s Equation**

Price’s Equation has several obvious merits for the analysis of group selection. It is simple, mathematically rigorous, and very general in its application. There have been many models of group selection, with a bewildering variety of assumptions and parameters, but in every case we can ask the question: under this model, how does the change of gene frequency between one generation and the next come out under Price’s Equation?

If we accept Price’s view that the Covariance term represents the contribution of group selection, then group selection requires covariance between group fitness and group gene frequency. The Price approach focuses attention on the circumstances that may give rise to covariance.

First, there cannot be covariance between two quantities unless there is variance in both of them. As Price himself noted, ‘the current “group selection” controversy hinges on the question of whether the intergroup variance \[in gene frequency\] is likely to be of significant magnitude under realistic natural conditions’ \[1972, p.489\]. If all groups had the same fitness, or the same gene frequency, or both, then the Covariance term would be zero. For example, if all groups were constrained by a ceiling on resources, such that the number of survivors was always the same in each generation, there would be no variance in group fitness, and the Covariance term would be zero.

The existence of variance in both group fitness and group gene frequency is a necessary but not sufficient condition for covariance between them. What is needed in addition is some connection between gene frequency and group fitness: they need to covary – literally, to vary together. We hypothesise that the groups’ genetic composition has some effect on fitness. This effect, if any, may be statistically measured by the regression of group fitness on group gene frequency. The regression coefficient measures the extent to which the high or low frequency of a given gene, relative to the population average, is associated with high or low fitness. The covariance is proportional to the regression coefficient, and as Price himself pointed out, in considering any model of selection the investigator should ask whether the assumed regression coefficient is plausible in nature. A high regression coefficient would imply that a small difference in group gene frequency has a large effect on group fitness: an assumption that would need to be justified.

**Altruism**

I have so far said little about altruism. Price himself does not use the term at all. (He does refer to ‘group-benefiting’ and ‘individual-benefiting’ genes: 1972, p.489.) The problem of biological altruism was however at the heart of the group selection controversy, and there is little doubt that it motivated Price’s interest in the subject \[see Harman, passim\].

Within the framework of Price’s Equation there is an obvious approach to the definition of altruism. Assuming that the Covariance and Transmission terms are both non-zero, there are four possible combinations:

1\. Both are positive.  
2. Both are negative.  
3. The Covariance term is positive but the Transmission term is negative.  
4. The Covariance term is negative but the Transmission term is positive.

If we assume, with Price, that the Covariance term represents ‘group’ selection, and the Transmission term ‘individual’ selection, then group selection is operating in all four cases, but in cases 1 and 2 it is operating in the same direction as individual selection, so there is no conflict between them. In cases 3 and 4, in contrast, the outcome depends on the balance of opposing forces. Case 3 seems on the face of it to represent group selection in favour of a gene for altruism, while case 4 represents group selection resisting a gene for selfishness.

Price’s Equation has indeed been interpreted in this way to define altruism. If the Covariance term is positive, but the Transmission term is negative, then the frequency of the relevant gene is, on average, declining within groups. A number of investigators have used this as their criterion for the presence of altruism, defining altruism as reducing individual fitness relative to the group average, while increasing the overall fitness of the group. However, this is a criterion for what is often called *weak* altruism. Weak altruism does not necessarily reduce the altruist’s own reproductive fitness relative to the population average, which would constitute *strong* altruism. An important distinction between weak and strong altruism is that the former, but not the latter, can evolve even when individuals are allocated randomly to groups in each generation. The distinction between weak and strong altruism was formulated after Price’s work, and his Equation does not resolve the choice between them. A weak definition of altruism fits neatly into Price’s mathematical treatment, but this is hardly an overriding reason for adopting it. It is noteworthy that Hamilton, despite his words of endorsement for Price’s approach, used a strong definition of altruism in his own work. Alan Grafen is also an advocate of Price’s Equation, but thinks the term ‘weak altruism’ misleading, and prefers to call it ‘a self-interested refusal to be spiteful’ \[Grafen 1984, p83\]. The distinction is discussed more fully [here](https://www.gnxp.com/wp/2011/03/01/defining-biological-altruism/).\*

**The blur between individual and group fitness**

As I mentioned earlier, the Covariance and Transmission terms in Price’s Equation do not mark the division between ‘group’ and ‘individual’ selection as clearly as Price seems to have believed. To introduce this problem, consider an analogy. Ten fat ladies join a Weightwatchers club. At the beginning of the year they have a collective weight of 2000 pounds, and thus an average individual weight of 200 pounds. At the end of the year, nine of them are exactly the same weight as before, but one of them has lost 100 pounds. The collective weight is now 1900 pounds and the average individual weight 190 pounds. We may therefore analyse the weight change of each member into two components: a Group effect (a loss of 10 pounds), and an Individual effect (in one case, a loss of 90 pounds, and in the other nine, a gain of 10 pounds).

The arithmetic is impeccable, but the interpretation is nonsense. There is no ‘Group effect’; or rather, if there is, it cannot be proved in this way. Not every mathematically consistent way of treating a problem makes sense in reality.

Applying this lesson to Price’s Equation, suppose a population is divided into groups. In each group there are two gene types, A and B, differing in frequency in the various groups. Let us suppose that both A and B have a constant fitness, regardless of their frequency within the groups, and that A is fitter than B. The groups in which A has a higher frequency therefore have a higher collective fitness, and the Covariance term will be positive. (For a simple worked example see the Note.) Yet there is nothing that can reasonably be called a group effect, since by assumption the two gene types have a constant fitness regardless of group composition. The change of gene frequency in the population between generations would be exactly the same if the groups were mingled together.

It is evident in this example that the positive Covariance term is just a side-effect of individual fitness differences. It is not quite so obvious what is happening to the Transmission term. Since the Covariance and Transmission terms must still add up to the overall change in population frequency, an increase in the Covariance term (as compared with the position if all groups had the same gene frequency) must be offset by a reduction in the Transmission term, which in Price’s analysis is identified with individual fitness. A little consideration of the example in the Note should clarify what is happening. The Transmission term depends on the average change of frequency within groups. But this is not a reliable indicator of the overall fitness of different gene types in the population. Suppose for example that in one group type A has already reached a very high frequency – say 95%. It cannot possibly grow by more than a further 5 percentage points in that group. Yet that might represent a much larger increase of frequency in the population as a whole. There is no simple way of inferring frequency changes in the whole population from the average change within groups.

In the worked example the Covariance term arising from purely individual selection is relatively small, accounting for only about 10% of the overall frequency change, even though I have deliberately made the difference in initial frequency of the gene between groups moderately large (.5 against .2). In general the Covariance term arising from individual selection will be small unless the difference in initial frequency is very large. At the extreme, if all groups have either 100% or 0% frequency of the gene, then there will be no within-group change in frequency, and the whole of the population change will be attributable to the Covariance term, even though it might be proved from other evidence that the fitness of the gene is independent of group composition.

There will also be cases where the fitness of different gene types is not completely independent of group composition, but where part of the overall fitness of the gene can reasonably be attributed (by experimental controls or otherwise) to purely individual-level effects. Yet these individual effects will still affect the Covariance term. The Covariance and Transmission terms simply do not, as a matter of principle, map precisely onto group and individual effects.

This complication is apparent as soon as one works through a simple numerical example of the kind in the Note, yet it does not seem to have been mentioned in the literature until 1985, when papers by Grafen and Nunney independently drew attention to it. (Grafen believed that an obscure passage in Hamilton’s 1975 paper alluded to the same problem, but Hamilton seems to me to have been making a rather different point.) Even after 1985 it has seldom been given much prominence: for example, in Sober and Wilson’s long book *Unto Others* the main text waxes eloquent on Price’s Equation, while the complications are discreetly buried in a note on page 343.

A partial remedy to the problem is to use what is known as ‘contextual analysis’ (see for example Okasha). The general principle of this is to use partial regression techniques to distinguish the individual fitness of genes when group composition is ‘held constant’, and vice versa. This does indeed eliminate spurious effects like my ‘Weightwatchers’ example, but it gives up the attractive simplicity of the Price approach, and except in special cases it does not entirely separate group and individual effects; it just shows what the individual fitness of a gene type would be in a group of ‘average’ composition so far as the particular population is concerned.

**Conclusions**

My main conclusions from this discussion can be stated briefly. Price’s approach is indeed a useful contribution to the debate on group selection. In considering any particular example or model of (purported) group selection or altruism, it is possible to use Price’s Equation to analyse the change in between-group and within-group frequencies. If the Covariance term is non-zero, it is then important to consider what is giving rise to a positive or negative covariance. As Price himself noted, we also need to look at the intergroup variance in gene frequency, without which there can be no covariance.

On the other hand, Price’s Equation is far from giving an uncontroversial solution to the questions raised in the group selection debate. Even if there were no ‘blur’ between individual and group effects, Price’s approach implicitly adopts a ‘weak’ criterion for altruism, and interprets kin selection as a form of group selection rather than an alternative to it. Many biologists would think that this ignores some of the key questions in the debate: can there be strong altruism without kin selection, and if so what mechanisms are at work?

**Note**

Suppose there are two gene types, A and B, and two groups each containing some A and B members. Suppose in the first and second generations the numbers in the groups are:  
First generation  
Group 1: 50 A, 50 B  
Group 2: 20 A, 80 B

Second generation  
Group 1: 100 A, 50 B  
Group 2: 40 A, 80 B

It can be seen that in both groups the A and B types have a constant fitness: each A member has (on average) 2 offspring (we assume asexual reproduction), and each B member has on average 1 offspring.

The overall increase in the frequency of A in the population is 140/270 – 70/200 = .1685. If we calculate the increase of frequency within each group it is .1666 for Group 1 and .1333 for Group 2. Note that neither of these is as high as the increase in the whole population: the population change is not in any sense a weighted average of the group changes.

If we now calculate the terms of Price’s Equation (I will omit the details), we get .01666 for the Covariance term, and .15185 for the Transmission term, which total to .1685, the overall population increase, as expected.

**References**

G. R. Price, ‘Selection and covariance’, *Nature*, 227, 1970, 520-21.  
G. R. Price, ‘Extension of covariance selection mathematics’, *Annals of Human Genetics*, 35, 1972, 485-90.

Alan Grafen: ‘Natural selection, kin selection and group selection’ in J. Krebs and N. Davies (eds.) *Behavioural Ecology: an evolutionary approach*, 2nd edn., 1984  
Alan Grafen: ‘A geometric view of relatedness’ in *Oxford Surveys in Evolutionary Biology*, 2, 1985.  
W. D. Hamilton: *Narrow Roads of Gene Land*, vol. 1, 1996.  
Oren Harman: *The Price of Altruism: George Price and the Search for the Origins of Kindness*, 2010.  
L. Nunney: ‘Group selection, altruism, and structured-deme models’, *American Naturalist*, 126, 1985, 212-35.  
Samir Okasha: ‘Multi-level selection, covariance, and contextual analysis’, *British Journal for the Philosophy of Science*, 55, 2004, 481-504.  
Elliott Sober and David Sloan Wilson: *Unto Others: the evolution and psychology of unselfish behaviour*, 1998.

### Related Posts:

- [Open Thread - October 30th,
  2010](https://www.gnxp.com/WordPress/2010/10/30/open-thread-october-30th-2010/) - [The Price
  Equation](https://www.gnxp.com/WordPress/2009/11/10/the-price-equation/) - [The Price of
  Altruism](https://www.gnxp.com/WordPress/2010/07/21/the-price-of-altruism/) - [Levels of selection & the full Price
  Equation](https://www.gnxp.com/WordPress/2009/11/11/levels-of-selection-the-full-price-equation/) - [The Fame of
  Price](https://www.gnxp.com/WordPress/2010/08/22/the-fame-of-price/) - [Groups, Price and
  Culture](https://www.gnxp.com/WordPress/2005/09/04/groups-price-and-culture/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F04%2F10%2Fgeorge-price-group-selection-and-altruism%2F&linkname=George%20Price%2C%20Group%20Selection%2C%20and%20Altruism "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F04%2F10%2Fgeorge-price-group-selection-and-altruism%2F&linkname=George%20Price%2C%20Group%20Selection%2C%20and%20Altruism "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F04%2F10%2Fgeorge-price-group-selection-and-altruism%2F&linkname=George%20Price%2C%20Group%20Selection%2C%20and%20Altruism "Email")[](https://www.addtoany.com/share)
