+++
title = "Variation in gene"
full_title = "Variation in gene expression between Africans and Europeans"
date = "2007-01-14"
upstream_url = "https://www.gnxp.com/WordPress/2007/01/14/variation-in-gene-expression-between-africans-and-europeans/"

+++
Source: [here](https://www.gnxp.com/WordPress/2007/01/14/variation-in-gene-expression-between-africans-and-europeans/).

Variation in gene expression between Africans and Europeans

Speaking of [race](https://www.gnxp.com/blog/2007/01/race-current-consensus.php), literally on the heels of a [separate study](http://www.nature.com/ng/journal/vaop/ncurrent/abs/ng1955.html) (by a separate lab) on [variation in gene expression](https://www.gnxp.com/blog/2007/01/differences-in-gene-expression-between.php) between European and East Asian populations, a [new study](http://www.journals.uchicago.edu/AJHG/journal/issues/v80n3/44428/brief/44428.abstract.html) in the AJHG quantifies within- and between-population variation in gene expression for Africans and Europeans, an open question at the end of Rik’s post on the Euro vs East Asian differences.

> We find extensive variation in gene-expression levels and estimate > that \~83% of genes are differentially expressed among individuals and > that \~17% of genes are differentially expressed among populations.

The latter percentage is smaller than the corresponding estimate from the Euro vs East Asian study, where it was \~26%. Contrary to proclamations (originally stemming from [Lewontin’s Fallacy](https://www.gnxp.com/MT2/archives/001525.html)) that such fractions are “small,” imagine you observed that, despite most of the employees at the numerous stores of two corporations being mostly identical (there are mail clerks, receptionists, etc.), some of the actions of certain positions varied from one store to another. Suppose 83% of these variations were idiosyncratic: say, the mail clerks in all stores of corporation X tended to wear their hair in ways different from one another, and likewise for the mail clerks in all stores of corporation Y, with no clear split. But then suppose 17% of the variations were mostly X vs Y differences: some might be boring, like X employees wore blue uniforms while those of Y wore red uniforms. Other differences would not be boring, especially differences in “management style” — who gave what orders to whom. You’d have to dig up lots of data to see how large of an effect these between-group differences had on observable characteristics for each corporation (such as gross revenue, market share, and other finance terms I don’t know the meaning of). But the point is simply that it might “only” require the “small” amount of 17% to make a noticeable difference in such characteristics.

Next, the authors looked up the biological pathways that the differentially expressed genes fell into (using [PANTHER](http://www.pantherdb.org/)). Their Table 1 shows that genes in 2 pathways were expressed differently among individuals, while genes in 11 pathways were expressed differently between Africans and Europeans:

Between-individuals  
Inflammation mediated by chemokine and cytokine  
T-cell activation

Between-populations  
Inflammation mediated by chemokine and cytokine  
Histamine H1 receptor-mediated signaling pathway  
Toll-receptor signaling pathway  
Fibroblast growth factor-signaling pathway  
Vascular endothelial growth factor-signaling pathway  
T-cell activation  
EGF receptor-signaling pathway  
B-cell activation  
Notch-signaling pathway  
Enkephalin release  
5HT2 type receptor-mediated signaling pathway

All p-values were less than 0.05, though only the first one listed in “Between-populations” remained significant after a [Bonferroni correction](http://mathworld.wolfram.com/BonferroniCorrection.html). I’m no bioinformaticist, but it seems that “multiple tests” here might not be so multiple if, for example, several differentially expressed genes were all involved in combatting a particular pathogen — then we have 1 hypothesis (different expression to combat a pathogen) which has several facets whose p-values we might add up, on the idea that the facets constitute a partition of the main trait, rather than multiply each p-value by 100 (or however many “tests” we ran). For example, the 4 p-values of the third through sixth entries in the “Between-populations” list add up to 0.0459 — still significant — although here none of their p-values withstands the Bonferroni correction. NB: I don’t claim these 4 pathways are linked to a single purpose; I’m just showing how several typical p-values can add up to less than the standard 0.05 significance level. Obviously, though, the input of professional statisticians is worth more than my wonderings.

Finally, on a molecular bio level (my square brackets:

> To better understand the molecular basis for the observed > \[between-population\] difference in expression \[for > [SH2B3](http://www.ncbi.nlm.nih.gov/entrez/dispomim.cgi?id=605093)\], > we asked whether the expression level of one allele was different from > the other in heterozygous individuals. If so, this provides evidence > of cis-regulatory effects.26 There was a significant difference \[P = > 0.00118\] in expression between alleles in heterozygous cDNA versus > genomic DNA, strongly suggesting cis-regulatory effects (fig. 5b).

And as for signatures of selection (my square brackets):

> Interestingly, these observations coincide with patterns of genetic > variation at SH2B3, since there are 13 SNPs with large > allele-frequency differences \[Fst greater or = 0.45\] between the CEU > and YRI samples (fig. 5c). Five of these highly differentiated SNPs > occur in conserved regions, as determined by alignment of 17 > vertebrate genomes, making them strong candidates for future > functional studies. We calculated the empirical probability of > observing a SNP with a pairwise \[Fst greater or = 0.45\] between the > CEU and YRI samples, on the basis of all autosomal markers contained > in Hap-Map release 21, to be \~0.05, and this magnitude of allele > frequency difference is consistent with a signature of local > adaptation.7,39 SH2B3 also possesses unusually large levels of linkage > disequilibrium compared with the rest of the genome,40 which provides > additional support for the hypothesis that this locus has been subject > to adaptive evolution, although additional studies will be necessary > to make more-definitive inferences about its evolutionary history.

### Related Posts:

- [How different are gene expression levels between
  Europeans…](https://www.gnxp.com/WordPress/2008/12/06/how-different-are-gene-expression-levels-between-europeans-and-africans/) - [Gene expression differences between
  populations](https://www.gnxp.com/WordPress/2008/02/28/gene-expression-differences-between-populations/) - [Differences in gene expression between Asians and
  Europeans](https://www.gnxp.com/WordPress/2007/01/07/differences-in-gene-expression-between-asians-and-europeans/) - [Gene expression, African Americans &
  Europeans](https://www.gnxp.com/WordPress/2008/12/08/gene-expression-african-americans-europeans/) - [Reanalysing gene expression differences between
  populations](https://www.gnxp.com/WordPress/2007/06/28/reanalysing-gene-expression-differences-between-populations/) - [Carbs &
  ancestry](https://www.gnxp.com/WordPress/2009/12/10/carbs-ancestry/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F01%2F14%2Fvariation-in-gene-expression-between-africans-and-europeans%2F&linkname=Variation%20in%20gene%20expression%20between%20Africans%20and%20Europeans "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F01%2F14%2Fvariation-in-gene-expression-between-africans-and-europeans%2F&linkname=Variation%20in%20gene%20expression%20between%20Africans%20and%20Europeans "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F01%2F14%2Fvariation-in-gene-expression-between-africans-and-europeans%2F&linkname=Variation%20in%20gene%20expression%20between%20Africans%20and%20Europeans "Email")[](https://www.addtoany.com/share)
