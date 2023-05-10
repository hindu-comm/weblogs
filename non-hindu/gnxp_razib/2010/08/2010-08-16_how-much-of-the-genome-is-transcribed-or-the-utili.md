+++
title = "How much of the genome"
full_title = "How much of the genome is transcribed? Or, the utility of a good genome browser"
date = "2010-08-16"
upstream_url = "https://www.gnxp.com/WordPress/2010/08/16/how-much-of-the-genome-is-transcribed-or-the-utility-of-a-good-genome-browser/"

+++
Source: [here](https://www.gnxp.com/WordPress/2010/08/16/how-much-of-the-genome-is-transcribed-or-the-utility-of-a-good-genome-browser/).

How much of the genome is transcribed? Or, the utility of a good genome browser

Recent genome-wide association studies have identified a large number of [non-genic regions associated with disease risk](https://www.gnxp.com/wp/uncategorized/how-do-non-genic-polymorphisms-influence-disease-risk); the standard interpretation of this observation is that these are regions involved in gene regulation. A few years back, though, another possibility was raised: what if there are simply a large number of genes in the human genome that we don’t know about yet? This hypothesis came from the observation, using gene expression microarrays, that there appeared to be much more transcription in the human genome than currently annotated (for example, \[1\]).

A [new study](http://www.plosbiology.org/article/info:doi/10.1371/journal.pbio.1000371#pbio.1000371.s016), however, throws a bit of cold water on this possibility \[2\]. Using RNA sequencing, the authors show that 1) there doesn’t appear to be *that* much unannotated transcription, and 2) most of the unannotated transcription that does exist is connected in some way to previously known genes. I don’t want to focus too much on these observations; however, I do want to spend a bit of time on the new transcription that they *do* find. In particular, they identify \~8,000 novel, short, unspliced transcripts, some of which show evidence of evolutionary conservation. This seems like quite a few! However, **my feeling is that many of these are not true transcripts, but rather experimental artifacts**. Let me explain why.  

Let’s take the example of such a transcript that the authors give us in their Figure 8, reproduced below. On the x-axis is the position along the genome, the top track shows a measure of evolutionary conservation, and the tracks below show measures of gene expression from RNA sequencing in various tissues. Notice the discrete peaks of mapped sequencing reads, consistently positioned in the different tissues.

[![](https://i0.wp.com/www.gnxp.com/wp/wp-content/uploads/2010/08/hughes_fig11.png?resize=600%2C420 "hughes_fig1")![](https://i0.wp.com/www.gnxp.com/wp/wp-content/uploads/2010/08/hughes_fig11.png?resize=600%2C420 "hughes_fig1")](https://i0.wp.com/www.gnxp.com/wp/wp-content/uploads/2010/08/hughes_fig11.png)

Now, let’s take a look at this region in the UCSC genome browser—the centralized resource for all annotations of the human genome. If we consider the conservation track, we see the picture below. Like the authors of the paper, we see relatively high levels of sequence conservation in the region. However, if we look more closely at the multiple genome alignment that leads to this high sequence conservation, we notice a strange pattern—there are gaps in the alignment in the mouse and the dog (which both have high quality genome assemblies), but the sequence is present in human and much more distantly related species with lower quality genomes (like sticklebacks). This should give you pause—how could a DNA sequence be present in humans and sticklebacks, but absent from dogs and mice? There are some possibilities, but the most likely one is that this sequence is not conserved at all, but instead the alignment algorithm is aligning non-homologous, but similar, sequences in humans and the distantly related species.

[![](https://i0.wp.com/www.gnxp.com/wp/wp-content/uploads/2010/08/hughes_fig21.png?resize=600%2C304 "hughes_fig2")![](https://i0.wp.com/www.gnxp.com/wp/wp-content/uploads/2010/08/hughes_fig21.png?resize=600%2C304 "hughes_fig2")](https://i0.wp.com/www.gnxp.com/wp/wp-content/uploads/2010/08/hughes_fig21.png)

What could lead to this phenomenon? One possibility is processed pseudogenes (a phenomenon where a transcribed–and, importantly, intronless–copy of a gene is re-inserted elsewhere in the genome): if processed pseudogenes arose independently in two lineages, the two copies could look pretty similar and might get aligned. Indeed, if we take the sequence in question and look to see if it matches anywhere else in the genome, we find it’s an excellent match to a gene on a different chromosome (see figure below).

[![](https://i0.wp.com/www.gnxp.com/wp/wp-content/uploads/2010/08/hughes_fig31.png?resize=600%2C200 "hughes_fig3")![](https://i0.wp.com/www.gnxp.com/wp/wp-content/uploads/2010/08/hughes_fig31.png?resize=600%2C200 "hughes_fig3")](https://i0.wp.com/www.gnxp.com/wp/wp-content/uploads/2010/08/hughes_fig31.png)

This fact explains a number of observations about this region—the apparent sequence conservation is due to misalignment of the genomes in the region, and the apparent expression is due to RNA-Seq reads that cover exon-exon junctions \[3\]. In reality, **the most likely situation is that there is neither conservation nor expression of the region**. It’s unclear how many of the 8,000 putative new regions match this sort of profile, but my guess is that there are quite a few. I hasten to add that this actually supports the main conclusions made by the authors—there’s less unannotated transcription than previously reported, and even less than they themselves report \[4\]!

As a final aside, why is there no annotation of processed pseudogenes on the UCSC browser? With a bit of searching, I found pseudogene.org \[5\], which maintains a database of pseudogene locations in humans (the region discussed is indeed annoatated in this database). Unfortunately, these annotation are not found in the UCSC browser; my guess is the authors of this paper took a look at their region in the browser and saw nothing out of the ordinary. If the pseudogene annotation had been in this centralized database, it might have raised a red flag. In any case, a good genome browser can make life a lot easier, and the more information the better.

—–

\[1\] Cheng, Kapranov et al. (2005) Transcriptional Maps of 10 Human Chromosomes at 5-Nucleotide Resolution. Science. DOI: 10.1126/science.1108625

\[2\] van Bakel et al. (2010) Most “Dark Matter” Transcripts Are Associated With Known Genes. PLoS Biology. DOI:10.1371/journal.pbio.1000371

\[3\] Exon-exon junction sequences are separated by introns in the gene itself, but are together in the processed pseudogene. Thus any RNA-Seq read from the gene that spans the junction will match the pseudogene, but not the gene from which it came. Note that there are 11 exon-exon junctions in the gene, and about 11 peaks of gene expression in the pseduogene.

\[4\] It’s possible, of course, that some processed pseudogenes are actually expressed. However, this is probably a small fraction of all such pseudogenes, and would require more evidence than presented to prove.

\[5\] Zhang et al. (2003) Millions of Years of Evolution Preserved: A Comprehensive Catalog of the Processed Pseudogenes in the Human Genome. Genome Research. DOI: 10.1101/gr.1429003

### Related Posts:

- [Extensive transcription in the
  fly](https://www.gnxp.com/WordPress/2006/10/01/extensive-transcription-in-the-fly/) - [EGHM I: the slow death of the "one
  gene-one…](https://www.gnxp.com/WordPress/2006/05/10/eghm-i-the-slow-death-of-the-one-gene-one-enzyme-hypothesis/) - [Is intergenic expression
  functional?](https://www.gnxp.com/WordPress/2006/09/21/is-intergenic-expression-functional/) - [How do non-genic polymorphisms influence disease
  risk?](https://www.gnxp.com/WordPress/2010/04/25/how-do-non-genic-polymorphisms-influence-disease-risk/) - [Asia finally getting in on the genome-wide association
  game?](https://www.gnxp.com/WordPress/2008/08/18/asia-finally-getting-in-on-the-genome-wide-association-game/) - [Evolutionary forces in the (human)
  genome](https://www.gnxp.com/WordPress/2006/10/13/evolutionary-forces-in-the-human-genome/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F08%2F16%2Fhow-much-of-the-genome-is-transcribed-or-the-utility-of-a-good-genome-browser%2F&linkname=How%20much%20of%20the%20genome%20is%20transcribed%3F%20Or%2C%20the%20utility%20of%20a%20good%20genome%20browser "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F08%2F16%2Fhow-much-of-the-genome-is-transcribed-or-the-utility-of-a-good-genome-browser%2F&linkname=How%20much%20of%20the%20genome%20is%20transcribed%3F%20Or%2C%20the%20utility%20of%20a%20good%20genome%20browser "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F08%2F16%2Fhow-much-of-the-genome-is-transcribed-or-the-utility-of-a-good-genome-browser%2F&linkname=How%20much%20of%20the%20genome%20is%20transcribed%3F%20Or%2C%20the%20utility%20of%20a%20good%20genome%20browser "Email")[](https://www.addtoany.com/share)
