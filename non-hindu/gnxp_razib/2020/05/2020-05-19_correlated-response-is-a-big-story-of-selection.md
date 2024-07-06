+++
title = "Correlated response is a"
full_title = "Correlated response is a big story of selection"
date = "2020-05-19"
upstream_url = "https://www.gnxp.com/WordPress/2020/05/19/correlated-response-is-a-big-story-of-selection/"

+++
Source: [here](https://www.gnxp.com/WordPress/2020/05/19/correlated-response-is-a-big-story-of-selection/).

Correlated response is a big story of selection

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/04/principlespopulationgenetics.jpg?resize=234%2C284&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/04/principlespopulationgenetics.jpg?resize=234%2C284&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/0878933085/geneexpressio-20)Adaptation is clearly one of the most important processes in understanding how evolution occurs. In a classical sense, it’s easy to understand. Parallel adaptations in body plans make dolphins and swordfish shaped the same. It’s physics.

But with the emergence of DNA, a lot of the focus on adaptation has been displaced to the signatures of natural selection on the molecular level. Phenotypes are controlled by variation in genotypes, and instead of description and hypothesizing, researchers can actually **infer from the genetic patterns the history and arc of adaptation.**

At least that’s the theory.

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/11/lynch.jpeg?resize=195%2C258&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/11/lynch.jpeg?resize=195%2C258&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/B07GYTZ92L/geneexpressio-20)The initial tests for signatures of natural selection focused on adaptation **between** species. For example, Tajima’s D. Usually this took the form of comparing variation across two lineages of *Drosophila*. In the 2000s with genome-wide data new methods predicated on looking at ‘haplotype structure’ (variation across sequences of genes) emerged. Instead of between species, these methods focused on the selection within species (e.g., why are some humans adapted to malaria?). These methods were good at picking up strong signals at a few genes where the selective sweeps were recent.

But as datasets and genomics got bigger and better researchers focused on more fundamental patterns and analyses, such as looking at ‘site frequency spectra.’ Ultimately the goal was to go beyond selection at a single locus (e.g., lactase persistence), and understand polygenic characteristics (e.g., height). Obviously, this is much harder because polygenic characters are distributed across many genetic loci, and issues of statistical power are always going to loom large (and there is the soft vs hard sweep issue too!).

A new preprint is an excellent introduction to this wild world, [Disentangling selection on genetically correlated polygenic traits using whole-genome genealogies](https://www.biorxiv.org/content/10.1101/2020.05.07.083402v1):

> We present a full-likelihood method to estimate and quantify polygenic > adaptation from contemporary DNA sequence data. The method combines > population genetic DNA sequence data and GWAS summary statistics from > up to thousands of nucleotide sites in a joint likelihood function to > estimate the strength of transient directional selection acting on a > polygenic trait. Through population genetic simulations of polygenic > trait architectures and GWAS, we show that the method substantially > improves power over current methods. We examine the robustness of the > method under uncorrected GWAS stratification, uncertainty and > ascertainment bias in the GWAS estimates of SNP effects, uncertainty > in the identification of causal SNPs, allelic heterogeneity, negative > selection, and low GWAS sample size. The method can quantify selection > acting on correlated traits, fully controlling for pleiotropy even > among traits with strong genetic correlation (\|rg\| = 80%; c.f. > schizophrenia and bipolar disorder) while retaining high power to > attribute selection to the causal trait. We apply the method to study > 56 human polygenic traits for signs of recent adaptation. We find > signals of directional selection on pigmentation (tanning, sunburn, > hair, P=5.5e-15, 1.1e-11, 2.2e-6, respectively), life history traits > (age at first birth, EduYears, P=2.5e-4, 2.6e-4, respectively), > glycated hemoglobin (HbA1c, P=1.2e-3), bone mineral density > (P=1.1e-3), and neuroticism (P=5.5e-3). We also conduct joint testing > of 137 pairs of genetically correlated traits. We find evidence of > widespread correlated response acting on these traits (2.6-fold > enrichment over the null expectation, P=1.5e-7). We find that for > several traits previously reported as adaptive, such as educational > attainment and hair color, a significant proportion of the signal of > selection on these traits can be attributed to correlated response, vs direct selection (P=2.9e-6, 1.7e-4, respectively). Lastly, our joint test uncovers antagonistic selection that has acted to increase type 2 diabetes (T2D) risk and decrease HbA1c (P=1.5e-5).

There’s a lot going on here. This is my favorite passage:

> To address these issues, we recently developed a full-likelihood > method, CLUES, to test for selection and estimate allele frequency > trajectories. 21 The method works by stochastically integrating over > both the latent ARG using Markov Chain Monte Carlo, and the latent > allele frequency trajectory using a dynamic programming algorithm, and then using importance sampling to estimate the likelihood function of a focal SNP’s selection coefficient, correcting for biases in the ARG due to sampling under a neutral model.

Alrighty then! Someone’s a major-league nerd.

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/06/evolutionary_quantitative_genetics.jpeg?resize=183%2C276&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/06/evolutionary_quantitative_genetics.jpeg?resize=183%2C276&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/041212971X/geneexpressio-20)The preprint is fine, but ultimately this is something you get a “feel” for by working with models, data, and general analyses in the field. And I don’t have a strong feel since I don’t work with these sorts of data and questions myself. So what do I know? That being said, I like the preprint because it satisfies an intuition I’ve long had: **correlated response is a big part of the story of polygenic selection.**

Basically, you have to remember that complex traits are subject to variation at a host of genetic positions. And genetic variants rarely have singular effects. That is, one locus usually exhibits pleiotropy. The genetic effect shapes a lot of characteristics. Therefore, if there is a strong selection on a gene, more traits than simply the target of selection will be impacted. In animal breeding making huge, meaty, fast-growing lineages can render them infertile if selection is taken too far. That’s a bad correlated response.

After correcting for the genetic correlation the authors **note that some traits, such as EDU and hair color, are not really selected directly at all.** This is like the fact that we know *EDAR* is associated with hair thickness and is a strong target of selection. We have no idea what the trait of interest is. But it’s a pretty big deal. All these quantitative traits controlled by variation across the genome are being reshaped by adaptation on other traits. What are those traits? This preprint doesn’t answer that really.

Hopefully, we’ll make some headway in the 2020s because we’re definitely looking through the mirror darkly.

### Related Posts:

- [Quantitative genetics strikes back!
  (?)](https://www.gnxp.com/WordPress/2010/02/27/quantitative-genetics-strikes-back/) - [Loss of Function is
  Adaptation](https://www.gnxp.com/WordPress/2007/07/08/loss-of-function-is-adaptation/) - [Human evolutionary
  genomics](https://www.gnxp.com/WordPress/2007/10/09/human-evolutionary-genomics/) - [Selection "vs."
  drift](https://www.gnxp.com/WordPress/2007/07/06/selection-vs-drift/) - [Humans have adapted on genome-wide
  level?](https://www.gnxp.com/WordPress/2009/01/16/humans-have-adapted-on-genome-wide-level/) - [The genetics of adaptation in
  Arabidopsis](https://www.gnxp.com/WordPress/2008/04/24/the-genetics-of-adaptation-in-arabidopsis/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2020%2F05%2F19%2Fcorrelated-response-is-a-big-story-of-selection%2F&linkname=Correlated%20response%20is%20a%20big%20story%20of%20selection "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2020%2F05%2F19%2Fcorrelated-response-is-a-big-story-of-selection%2F&linkname=Correlated%20response%20is%20a%20big%20story%20of%20selection "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2020%2F05%2F19%2Fcorrelated-response-is-a-big-story-of-selection%2F&linkname=Correlated%20response%20is%20a%20big%20story%20of%20selection "Email")[](https://www.addtoany.com/share)
