+++
title = "Sequencing is hard"
full_title = "Sequencing is hard"
date = "2006-10-05"
upstream_url = "https://www.gnxp.com/WordPress/2006/10/05/sequencing-is-hard/"

+++
Source: [here](https://www.gnxp.com/WordPress/2006/10/05/sequencing-is-hard/).

Sequencing is hard

Both the [Wall Street Journal](http://online.wsj.com/public/article/SB115993034340082110-CKyzf6mJyNzGTtTINo0V0UgWon8_20061011.html?mod=blogs) and the [NY Times](http://www.nytimes.com/2006/10/04/science/04cnd-genome.html?_r=1&oref=slogin) report on the new X Prize Challenge:

> The X Prize Foundation, sponsor of a widely noted 2004 award for > developing a reusable rocket suitable for private space travel, says > it is now teaming with a wealthy Canadian geologist to offer \$10 > million to any team that can completely decode the genes of 100 people > in 10 days. >
> And that’s not all. As an encore, the winning team will be paid \$1 > million more to decode another 100 people’s genes, including a bevy of > wealthy donors and celebrities. Already accepted for future decoding: > Google Inc. co-founder Larry Page, Microsoft Corp. co-founder Paul G. > Allen and former junk-bond king Michael Milken.

[John Hawks](http://johnhawks.net/weblog/) has a little commentary, including the ever important question: how does anyone actually know the winners get it right (as opposed to generating random variations on the current reference sequence, for example)?

One broader question overall is: why do we need a new method for sequencing? [Sanger sequencing](https://en.wikipedia.org/wiki/Sanger_sequencing) has gotten us this far, shouldn’t a little more miniaturization and automation get us where we need to be? The answer, in a word, is no.

As I see it, the problem with both [454 sequencing](https://evolgen.blogspot.com/2005/04/bead-based-resequencing.html) (one of the top candidates to be the next major sequencing technology) and Sanger sequencing is their ability (or lack thereof) to handle large repeats. Here’s what I mean:

First, note that sequencing is not the same as looking at a DNA molecule and reading on down. Sanger sequencing gets you about 600 bases at a time, so you first need to break the genome up into pieces of that size, sequence them all, then put them back in order. In 454 sequencing, you break the genome up into piece of about 1000 bp, but you only can read about 200 of them. Note that the human genome is composed of somewhere around 3.3 billion bases.

Now imagine you have a stretch of 3000 bases on chromosome 5, and another *identical* stretch on chromosome 11. If you’re sequencing 600 bases, you have no idea that there are two copies of that sequence in the genome– all you see is a bunch of identical sequence. The only thing you can do is sequence the same genome over and over again and hope that one of your 600 bp reads overlaps both some unique sequence from one chromosome and some of your repeat, allowing you to anchor it down. Of course, there are computational methods for resolving repeats that have gotten much better in the past few years, but the larger the repeat, the harder it is, and you still have to generate a lot of sequence– off the top of my head, I’d guess you need something like 10X coverage (meaning for a 3.3 billion bp genome, you have to sequence 33.3 billion bases) to successfully resolve most repeats. That’s a lot.

And this is not just a theoretical problem– **the reference genome is still not complete due to the [presence of large repeats](http://www.nature.com/nature/journal/v431/n7011/abs/nature03062.html)**! And these things are important– one, their architecture predisposes to [pathogenic rearrangements](http://www.nature.com/ng/journal/v38/n9/abs/ng1862.html) and two, [normal copy number differences](http://www.journals.uchicago.edu/cgi-bin/resolve?id=doi:10.1086/431652&erFrom=-7346741497855838108Guest) in humans is a relatively unexplored source of natural variation.

In the short term (ie. in the next 2-3 years), no sequencing technology will be able to get around this problem reliably enough to win this prize. What we will see, however, is the use of [array-based methods](http://www.sciencemag.org/cgi/content/abstract/311/5769/1932) to type almost all polymorphism in the genome, which will give an approximation of a genome sequence. These technologies are cheap and fairly computationally tractable, meaning they can be widely used, but they’re still subject to problems like the ones described above, so they’re not as good as a full sequence.

In the long run, however, sequencing will indeed be routine. How long? I’m guessing no more than 10 years. And what technology will do it? My money is on technologies that work with a single DNA molecule. If they get good enough (and they will), it should be possible to simply read down a DNA molecule as if it were an open book. No problem with repeats there. [Here’s a paper](http://www.sciencemag.org/cgi/content/abstract/313/5788/801) that follows an enzyme down DNA and uses the movement of the enzyme to call the base. [Nanopore sequencing](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=Retrieve&db=PubMed&list_uids=10740260&dopt=Citation) has also gotten a lot of press in the last few years; I wouldn’t be surprised if a company using that technology throws their hat into the ring.

It’s worth noting that the vast majority of DNA variants in the world are singletons– that is, they only appear in one individual. Once sequencing is routine, there will be a revolution in how we understand the genetic basis of phenotypes– whether pathological or not.

### Related Posts:

- [In defense of the celebrity
  genome](https://www.gnxp.com/WordPress/2007/05/24/in-defense-of-the-celebrity-genome/) - [Another Nobel for the New Germ Theory of
  disease](https://www.gnxp.com/WordPress/2008/10/07/another-nobel-for-the-new-germ-theory-of-disease/) - [The shuttle as a flop (in
  numbers)](https://www.gnxp.com/WordPress/2011/07/22/the-shuttle-as-a-flop-in-numbers/) - [Singularity Institute Research
  Challenge](https://www.gnxp.com/WordPress/2010/02/28/singularity-institute-research-challenge-2/) - [Singularity Institute Research
  Challenge](https://www.gnxp.com/WordPress/2010/02/28/singularity-institute-research-challenge-2/) - [\$99 for 1 million
  markers](https://www.gnxp.com/WordPress/2012/12/11/99-for-1-million-markers/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2006%2F10%2F05%2Fsequencing-is-hard%2F&linkname=Sequencing%20is%20hard "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2006%2F10%2F05%2Fsequencing-is-hard%2F&linkname=Sequencing%20is%20hard "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2006%2F10%2F05%2Fsequencing-is-hard%2F&linkname=Sequencing%20is%20hard "Email")[](https://www.addtoany.com/share)
