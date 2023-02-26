+++
title = "Speaking of…"
full_title = "Speaking of…"
date = "2006-09-24"
upstream_url = "https://www.gnxp.com/WordPress/2006/09/24/speaking-of/"

+++
Source: [here](https://www.gnxp.com/WordPress/2006/09/24/speaking-of/).

Speaking of…

…[epigenetics](https://www.gnxp.com/blog/2006/09/epigenetics-is-new-genetics.php)\[1\] and [non-coding RNAs](https://www.gnxp.com/blog/2006/09/is-intergenic-expression-functional.php). I encourage everyone to check out [the new Cell](http://www.cell.com/content/issue?volume=126&issue=6) and find “[the first genome-wide high-resolution mapping of DNA methylation and the first systematic analysis of the role of DNA methylation in regulating gene expression for any organism](http://www.cell.com/content/article/fulltext?uid=PIIS009286740601018X)” and a new [microRNA target prediction](http://www.sciencedirect.com/science?_ob=ArticleURL&_udi=B6WSN-4KY2PG7-N&_coverDate=09%2F22%2F2006&amp;_alid=455080545&_rdoc=1&_fmt=&_orig=search&amp;_qd=1&_cdi=7051&_sort=d&view=c&_acct=C000047944&_version=1&_urlVersion=0&_userid=918210&md5=9a034bcf1a4ae94cf6a59161266c4e72) method ([rna22](http://cbcsrv.watson.ibm.com/rna22.html)) that makes big (perhaps too radical?) predictions about the percentage of mRNAs regulated by this pathway.

I haven’t even had time to read the methylation paper yet, it looks like tiling arrays are used and this will be the third instance of that technique I’ve come across in the past week. Basically, this is an array that contains little chunks of sequence making up all of the non-repetitive parts of the genome. You can then wash some sample over it and see which chunks of sequence on the array get sample stuck to them through hybridization. Looks like in this paper they pulled out all the methylated vs. unmethylated DNA and hybridized that to the tiling array. Scanning the paper I note that when methylation occurs within the coding portion of a gene it is likely to be expressed whereas when methylation occurs in the promoter region it is likely to be controlled in a tissue-specific manner. Also, they present some evidence downplaying the role of microRNAs in transcriptional regulation through guided methylation, which was getting some buzz a couple or three months ago. BTW, this study was performed in a plant genome; Arabidopsis thaliana to be exact.

On the other hand, microRNAs in translational regulation are still getting played up as a major force. I won’t pretend to understand all of the pros and cons of rna22’s algorithm, but they do some false positive and sensitivity analysis and predict that it will find 1 false-positive binding site per 10,000 nucleotides and will discover 83% of real binding sites. With those rates in mind, consider the number of binding sites their algorithm predicts in the human genome. Conventional wisdom is that microRNAs are most likely to bind to the 3′ untranslated region of mRNAs, so that is where you should look for binding sites. 92.3% of 3′ UTRs in the human genome contain one or more “target islands” according to rna22. Even better, 99% of coding sequences are in the human genome do the same. That result almost seems outlandish to me, but I really have no expertise to evaluate it from.

Whenever the [Schratt et al. paper](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?db=pubmed&cmd=Retrieve&dopt=AbstractPlus&list_uids=16421561&query_hl=1&itool=pubmed_docsum) came out earlier this year I was totally hyped on it. One microRNA (miR-134) was found to control LIMK-1 expression and thus dendritic spine morphogenesis. The translational repression of LIMK-1 was released in response to brain-derived neurotrophic factor (BDNF, associated with LTP and memory and all that jazz). I thought, “Maybe miR-134 has multiple synapse-related targets that are co-upregulated by release from microRNA inhibition in the face of synaptic activity.” I was thinking in the 50-100 range. This paper predicts 2318 targets for miR-134. There are not that many dendritically localized RNAs, so my little theory is at best incomplete.

Finally, everything you knew about microRNA-target hybridization is wrong. Many heuristic-based approaches have focused on the “seed region” of miRNAs for target recognition. The idea is that it is particularly important for the first 7 or so nucleotides of a miRNA to match its target sequence and bind effectively. This paper says good seed-binding can still lead to crappy translational repression, and poor seed-binding (weird base-pairs or nucleotides with no binding partner at all) can still lead to strong repression. So everything right is wrong again and we can all go back to the drawing board, but at least now we have IBM on our side.

\[1\]I’m a little concerned that people won’t understand the connection between epigenetics and DNA methylation. It seems like lately when I see the term it refers to any sort of heritability that can’t be directly attributed to DNA sequence. When I first learned the term it was primarily in relation to the molecular modifications that can occur around the DNA. For instance, DNA can be methylated and histones (the proteins that DNA wraps around to condense) can be acetylated or methylated or phosphorylated. People were very concerned with the methylation states of chromosomes and how they were modified by paternal and maternal imprinting. Of late, it seems that there is increasing focus on potential environmental effects on germline genome which are epigenetic in the broad sense, but may or may not be in the DNA methylation sense. Maybe I’m the only one who finds this distinction necessary/troublesome.

### Related Posts:

- [Copying Gene Expression
  Patterns](https://www.gnxp.com/WordPress/2005/04/22/copying-gene-expression-patterns/) - [Epigenetics in
  memory](https://www.gnxp.com/WordPress/2007/03/16/epigenetics-in-memory/) - [Exhaling
  genes](https://www.gnxp.com/WordPress/2006/11/16/exhaling-genes/) - [Wait, does this mean genetics isn't
  everything?](https://www.gnxp.com/WordPress/2006/05/11/wait-does-this-mean-genetics-isn-t-everything/) - [Psychometrics, epigenetics and
  economics](https://www.gnxp.com/WordPress/2010/06/27/psychometrics-epigenetics-and-ecnomics/) - [Nature Reviews Epigenetics
  Focus](https://www.gnxp.com/WordPress/2007/03/25/nature-reviews-epigenetics-focus/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2006%2F09%2F24%2Fspeaking-of%2F&linkname=Speaking%20of%E2%80%A6 "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2006%2F09%2F24%2Fspeaking-of%2F&linkname=Speaking%20of%E2%80%A6 "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2006%2F09%2F24%2Fspeaking-of%2F&linkname=Speaking%20of%E2%80%A6 "Email")[](https://www.addtoany.com/share)
