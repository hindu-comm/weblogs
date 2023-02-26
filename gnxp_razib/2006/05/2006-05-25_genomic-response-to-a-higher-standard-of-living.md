+++
title = "Genomic response to a"
full_title = "Genomic response to a higher standard of living"
date = "2006-05-25"
upstream_url = "https://www.gnxp.com/WordPress/2006/05/25/genomic-response-to-a-higher-standard-of-living/"

+++
Source: [here](https://www.gnxp.com/WordPress/2006/05/25/genomic-response-to-a-higher-standard-of-living/).

Genomic response to a higher standard of living

[Deadsmith](https://www.gnxp.com/blog/2006/05/noise-in-gene-expression.php) dropped me another gem about a transcriptional profiling study in yeast getting a little more sugar. I will continue to share these with you until somebody tells me to stop. As before, any ire or accolades should be directed to him, as much as you can direct either one at a floating handle in cyberspace:

I really like the idea of studying things like cancer and Alzheimer’s in things like yeast. Yeast are just so easy to do genetics on. I like things that are reliable and easy to work on (I also like 20 year old Toyotas).

Okay, just file the following away… I may not even come back to it today:

Despite the canonized pathways of metabolism in eukaryotes, notably yeast, there is still quite a bit about metabolism that is unknown. Metabolism is important for lots of things in biology, since biological organisms have energy requirements, but one particularly interesting aspect of metabolism for humans is how it changes in cancerous tissue. One of the hallmarks of tumor cells is the excessive metabolism of glucose, often the result of mutations that have left the glycolysis machinery running unattended.

There. Now onto another topic: transcriptional response to environmental changes in yeast.

Organisms, even unicellular ones, have to respond to their environment. They can do this in the short term by leveraging the proteins that comprise the cell against the problem (think heat shock proteins refolding proteins, for example). But if the stimulus is long-lasting, then the cell too needs a long-lasting response, and we generally start thinking about transcription of genes to make new RNA to, in turn, make new proteins to come to the aid of the cell in its hour(s) of need.

But the details of these responses have not been particularly well-studied, so today I review an [attempt to perturb yeast cultures while monitoring their transcriptional and metabolic responses](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=pubmed&dopt=Abstract&list_uids=16381818&query_hl=3&itool=pubmed_docsum) ([pdf](http://f5.grp.yahoofs.com/v1/YJl2ROEVvBa3qGKmG_X_859eC9bknvSdZRFOPrpwvCKYVYte8CW3z0TN0TpoN4Gfw8o5dPRgy25tw1dNU1ONzZ14hsacOtN1UgU/ronenandbotstein2006.pdf)) that was published by the Botstein lab at Princeton University’s Lewis-Sigler Institute for Integrative Genomics in collaboration with Michal Ronen, a graduate student-turned post-doc at Stanford. Botstein has long been tangled in the development of microarray technology and interpretation, so it’s no surprise that this study teams the microarray with an old microbiology tool, the chemostat, to profile the transcriptional response of yeast to small doses of glucose.

The [chemostat](http://www.rpi.edu/dept/chem-eng/Biotech-Environ/Contin/chemosta.htm), for those unfamiliar, is a device that allows the steady-state growth of a microbial culture by continually adding nutrients and removing excess culture and byproduct. On a side note, the chemostat was invented by nuclear physicist [Leo Szilard](https://en.wikipedia.org/wiki/Leo_Szilard), Einstein’s coauthor of the letter that kicked off the [Manhattan Project](https://en.wikipedia.org/wiki/Manhattan_project) (man, those guys all had night jobs!).

Anyway, the idea here is to grow yeast in a chemostat, and then give them a tiny little glob of glucose to metabolize, and see how they respond transcriptionally and metabolically. The transcriptional measurement was done by microarray, and the metabolic assay was as simple as looking at how long it took for the glucose to “go away” and the ethanol to show up. I say “go away” because there are two obvious ways for it to do so: 1) glucose could be dissipating through the chemostat, or 2) it could be metabolized by the yeast. Since it “goes away” much faster if there are yeast in the chemostat, and since ethanol shows up on the chemostat if yeast are there, it’s safe to assume that the yeast are metabolizing the glucose to ethanol, as yeast are wont to do.

The interesting data, of course, is in the transcriptional response. The glucose doses came in one of two sizes: really small, and small. Both doses were too small to allow the cells to change in number (division) or size (growth without division), yet over the course of the next 3 hours (about one yeast cell cycle), 25% of genes changed expression at least 2 fold. Within minutes, there were dramatic expression differences, exhibiting the transcriptional response to the new carbon source, and over the remainder of the 3 hours measured, the RNA levels returned to their initial state in different modes.

Most of the genes behaved in a “burst response,” meaning that their transcripts dropped dramatically, then climbed back to initial state levels. These included the galactose metabolism genes, TCA cycle genes, and interestingly, ribosomal genes.

The glucose metabolism genes, including both glycolysis and gluconeogenesis, both showed a “lasting response,” though in opposite directions (glycolysis goes up and falls off slowly, gluconeogeneis goes down and comes up slowly).

A couple of genes, including the hexokinase genes, exhibited a bidirectional response, first dipping quickly, and then peaking well above baseline. These guys are known to work in a cross-regulatory circuit with MIG1 and RGT1. MIG1 is responsible for repressing the expression of gluconeogenesis and galactose genes, and is upregulated by glucose presence in the cell (all this is outlined in the diagram Iâ€™ve taken from pg. 391 of the article and posted below). RGT1, meanwhile, represses the hexokinase transporter, which is responsible for importing glucose into the cell. The point is, these genes are in a repression-oscillator circuit, and thus have a bidirectional response that generates a smooth combined effect for regulating the switch from glucose to alternative carbon sources.  
[](https://www.gnxp.com/blog/uploaded_images/glucosepathways-769484.jpg)  
They also quantified the iron chelators, but I don’t really see the significance, and the signal was much shakier, so I’ll say only that about them.

It’s interesting to think about the transcript levels that fell quickly, as I went into this paper thinking that it was going to be about transcription, not degradation. The authors mention in the discussion that the half-life of a glycolysis RNA 3 times longer in a glucose-rich culture, and that begs for more investigation (since we also don’t know jack about RNA degradation)\[Coffee Mug note: [we know a little about RNA degradation](http://thegenius.typepad.com/the_genius/2006/03/the_decapping_c.html)\].

Using all this data on the levels of the RNA rise and fall of each group of genes, and knowing a bit about how each gene in the system regulates the system, the authors then construct a couple of basic differential equations to model the transcription factor activity (TFA) of some of the genes. It’s important to realize that TFA is hard to measure directly, so if you can construct a good model of how you think it’s working from the expression data, then you can create predictive groups of TFA by functionality. They did such grouping by functional annotations from the [Gene Ontology](http://www.geneontology.org/) database, and thus the end result was a set of mathematical classifiers for the types of transcription factor activity.

As with all things yeast, this looks like a model study for something bigger. There are tons of other ways to perturb yeast, but it might be possible to look at these basic sugar metabolism circuits and their regulatory profiles (and predictive transcription factor activity models) and look at other cell lines. Maybe human cell lines? Maybe human cell lines with ab  
normal TFA profiles? Gee, what kinda human cells have abnormal transcription factor activity? Any with abnormal TFA that involve glucose metabolism that we care about?

Hrmmm… It turns out that Botstein is interested in human disease, and I doubt this has escaped his attention, since I’ve seen him lecture on other ideas that involve studying cancer in yeast.

### Related Posts:

- [The randomness of model
  organisms](https://www.gnxp.com/WordPress/2009/09/19/the-randomness-of-model-organisms/) - [Daily Data Dump
  (Thursday)](https://www.gnxp.com/WordPress/2010/04/22/daily-data-dump-11/) - [Against contingency (in yeast
  traits)](https://www.gnxp.com/WordPress/2014/09/23/against-contingency-in-yeast-traits/) - [Pope on
  evolution](https://www.gnxp.com/WordPress/2007/04/11/pope-on-evolution/) - [Thinking about
  heritability](https://www.gnxp.com/WordPress/2012/10/03/thinking-about-heritability/) - [Does your twin have "rights" on your
  genomes?](https://www.gnxp.com/WordPress/2011/02/03/does-your-twin-have-rights-on-your-genomes/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2006%2F05%2F25%2Fgenomic-response-to-a-higher-standard-of-living%2F&linkname=Genomic%20response%20to%20a%20higher%20standard%20of%20living "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2006%2F05%2F25%2Fgenomic-response-to-a-higher-standard-of-living%2F&linkname=Genomic%20response%20to%20a%20higher%20standard%20of%20living "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2006%2F05%2F25%2Fgenomic-response-to-a-higher-standard-of-living%2F&linkname=Genomic%20response%20to%20a%20higher%20standard%20of%20living "Email")[](https://www.addtoany.com/share)
