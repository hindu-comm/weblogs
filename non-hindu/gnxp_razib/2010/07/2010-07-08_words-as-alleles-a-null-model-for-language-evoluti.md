+++
title = "Words as alleles A"
full_title = "Words as alleles A nullmodel for language evolution?"
date = "2010-07-08"
upstream_url = "https://www.gnxp.com/WordPress/2010/07/08/words-as-alleles-a-null-model-for-language-evolution/"

+++
Source: [here](https://www.gnxp.com/WordPress/2010/07/08/words-as-alleles-a-null-model-for-language-evolution/).

Words as alleles: A null-model for language evolution?

For me, recent computational accounts of language evolution provide a compelling rationale that cultural, as opposed to biological, evolution is fundamental in understanding the design features of language. The basis for this rests on the simple notion of language being not only a conveyor of cultural information, but also a socially learned and culturally transmitted system: that is, an individual’s linguistic knowledge is the result of observing the linguistic behaviour of others. Here, this well-attested process of language acquisition, often termed [*Iterated Learning*](http://replicatedtypo.wordpress.com/2009/08/31/iterated-learning-and-language-evolution/), emphasises the effects of differential learnability on competing linguistic variants. Sounds, words and grammatical structures are therefore seen to be the products of selection and directed mutation. As you can see from the use of terms such as *selection* and *mutation* it’s clear we can draw many parallels between the literature on language evolution and analogous processes in biology. Indeed, [Darwin himself noted such similarities in the Descent of Man](https://www.google.co.uk/search?q=A+struggle+for+life+is+constantly+going+on+amongst+the+words+and+grammatical+forms+in+each+language.+The+better%2C+the+shorter%2C+the+easier+forms+are+constantly+gaining+the+upper+hand%2C+and+they+own+their+success+to+their+own+inherent+virtue&ie=utf-8&oe=utf-8&aq=t&rls=org.mozilla:en-GB:official&client=firefox-a). However, one aspect evolutionary linguists don’t seem to borrow is that of a null model. Is it possible that the changes we see in languages over time are just the products of processes analogous to genetic drift?

Such questions are asked in a paper by Reali & Griffiths (2009) that also takes some steps to remedying the situation, by defining a neutral model at the level of linguistic variants. Specifically, they apply this neutral model to three linguistic phenomena: the [*s-shaped curve of language change*](https://en.wikipedia.org/wiki/Logistic_function#cite_note-probabilistic_linguistics-4); [the *distribution of word frequencies*](https://en.wikipedia.org/wiki/Zipf%27s_law); and, the *relationship between word frequencies and extinction rates*. But before getting into these three phenomena, a quick overview of the model is needed (for reasons you’ll see later on):

> Defining a model of language evolution that is neutral at the level of > linguistic variants requires an account of learning that is explicit > about the inductive biases of learners–those factors that make some > variants easier to learn than others–so that it is clear that these > biases do not favour particular variants. We model learning as > statistical inference, with learners using Bayes’ rule to combine the > clues provided by a set of utterances with inductive biases expressed > through a prior distribution over languages. We define a neutral model > by using a prior that assigns equal probability to different variants > of a linguistic form. While it is neutral at the level of variants, > this approach allows for the possibility that learners have more > general expectations about the structure of a language–such as the amount of probabilistic variation in the language, and the tendency for new variants to arise–that can result in forces analogous to directed mutation at the level of entire languages.

So, if this is the case, we can instead appeal to high-level inductive biases as explanatory mechanisms for the structure of languages, without necessarily appealing to selective forces at the level of linguistic variants. By combining the Iterated Learning Model (ILM) with Bayesian learners, the authors arrive at two surprising conclusions: (1) the model is equivalent to [the Wright-Fisher model](http://www.genetics.wustl.edu/bio5488/lecture_notes_2004/popgen_1.pdf) of allele transmission; and, (2) the model is able to reproduce basic regularities in the structure and evolution of languages without the need for the selection or directed mutation of linguistic variants. To reach this equivalence with the Wright-Fisher model linguistic variants are treated as different alleles of a gene, with the Markov chain produced by Iterated Learning matching the model of genetic drift. Essentially, they are proposing the results from population genetics can help define the dynamics and stationary distribution of the [Markov chain](https://en.wikipedia.org/wiki/Markov_chain): this will give a good indication of what kind languages will emerge.

By using Bayesian learners, the authors are able to explicitly relate language change to individual inductive biases: by manipulating the parameters of the prior and seeing the consequences produced via Iterated Learning. Also, their mathematical formulation allows them to generalize the biological-linguistic equivalence to the case of an unbounded number of variants:

> Following an argument similar to that for the finite case, iterated > learning with Bayesian learners considering distributions over an unbounded vocabulary can be show to be equivalent to the Wright-Fisher model for infinitely many alleles (see the electronic supplementary material for a detailed proof).

Just to reiterate:

- Their model is *neutral* in regards to both selection and directed
  mutation at the level of linguistic variants, assuming a symmetric
  mutation between competing variants. - The goal is to provide a *null hypothesis* to evaluate certain claims
  about the importance of selective pressures, which are often used to
  explain the “statistical regularities found in the form and evolution
  of languages”. - The authors also note that the model “allows for a kind of directed
  mutation at the level of entire languages, with expectations about the
  amount of probabilistic variation in a language shaping the structure
  of that language over time. These expectations play a role analogous
  to setting the mutation rate in the Wright-Fisher model.”

Frequency effects in lexical replacement rates

As you’ve probably guessed, the authors find that their null model can account for three linguistic phenomena previously mentioned. I’m going to focus on lexical replacement rates because it’s what I’m most familiar with. Anyway, two recent studies show how the frequency of use predicts: (1) the rates at which verbs change from irregular to regular forms ([Lieberman *et al.*, 2007](http://www.nature.com/nature/journal/v449/n7163/abs/nature06137.html)); and, (2) the word replacement rates in Indo-European languages ([Pagel *et al.*, 2007](http://www.nature.com/nature/journal/v449/n7163/abs/nature06176.html)). So, if a word is used frequently, then it is replaced much more slowly than a less frequently used one. For instance, Pagel *et al* found that over a 10,000 year time scale, some words show a minimal amount of cognate replacement (zero to one) for words used frequently, while less-frequently used words might have up to nine cognate replacements. Furthermore, certain classes of words evolve at different rates, with prepositions and conjunctions changing more quickly than pronouns and numbers. When plotted, this shows an inverse relationship between the frequency of use and replacement rates.

One suggestion is that some form of linguistic, frequency-dependent, purifying selection is a central factor in determining the slow rate of evolution in highly expressed words. However, as Reali & Griffiths show, their neutral model alone is sufficient to account for the frequency effect:

> In the infinite case, mutation occurs only to new variants, thus, all > variants are eventually lost from the population. A new cognate is > represented by a new variant. Replacement happens when the variant > corresponding to the old cognate becomes extinct. The case of verb > regularization is modelled by assuming that irregular and regular verbs coexist as two variants among other words in the vocabulary. Extinction of the irregular verb happens when the regular form replaces completely the irregular one.

Importantly, their analytic results and simulations indicate the replacement rate follows an inverse power-law relationship with frequency (see figure below):

[![](http://replicatedtypo.files.wordpress.com/2010/07/lexical-frequency.jpg?resize=512%2C483 "lexical frequency")![](http://replicatedtypo.files.wordpress.com/2010/07/lexical-frequency.jpg?resize=512%2C483 "lexical frequency")](http://replicatedtypo.files.wordpress.com/2010/07/lexical-frequency.jpg?resize=512%2C483)

Now, for me, I think this paper is quite important for the field of language evolution: all too often we assume some sort of purifying selection is shaping the trajectory of language. However, one of the apparent problems with their model is the use of a single chain of Bayesian learners. Recent studies (see [Ferdinand & Zuidema, 2009](http://www.isrl.illinois.edu/~amag/langev/paper/ferdinand09CogSci.html)) show that the outcome of iterated learning is sensitive to more factors than are explicitly encoded in the prior, including population size. This is true even when a small modification is made: e.g. expanding the population size to two individuals at each generation. I’m not entirely sure whether or not this has a profound impact on the current results, but it does stress the need for more work on developing null models for language evolution. As the authors themselves note:

> While this analysis of one of the most basic aspects of language–the > frequencies of different variants–emphasizes the connections between > biological and cultural evolution, it also illustrates that the models > developed in population genetics cover only one small part of the > process of cultural evolution. We anticipate that developing neutral models that apply to the transmission of more richly structured aspects of language will require a deeper understanding of the mechanisms of cultural transmission–in this case, language learning.

**Citation:** Florencia Reali and Thomas L. Griffiths. Words as alleles: connecting language evolution with Bayesian learners to models of genetic drift. *Proc R Soc B* (2010). 277: 429-436. DOI: [10.1098/rspb.2009.1513](http://rspb.royalsocietypublishing.org/content/277/1680/429.full).

N.B. You can currently download this article, and the whole backlog of Royal Society articles, for free until the end of July.

### Related Posts:

- [Podcasts about language as a complex adaptive
  system](https://www.gnxp.com/WordPress/2010/04/11/podcasts-about-language-as-a-complex-adaptive-system/) - [The Cultural Evolution of
  Language](https://www.gnxp.com/WordPress/2010/03/10/the-cultural-evolution-of-language/) - [Evolution of
  language](https://www.gnxp.com/WordPress/2007/10/10/evolution-of-language/) - [Social Networks and Linguistic
  Research](https://www.gnxp.com/WordPress/2010/04/02/social-networks-and-linguistic-research/) - [...and twins](https://www.gnxp.com/WordPress/2006/07/06/and-twins/) - [Complex societies = simple
  languages](https://www.gnxp.com/WordPress/2010/01/20/complex-societies-simple-languages/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F07%2F08%2Fwords-as-alleles-a-null-model-for-language-evolution%2F&linkname=Words%20as%20alleles%3A%20A%20null-model%20for%20language%20evolution%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F07%2F08%2Fwords-as-alleles-a-null-model-for-language-evolution%2F&linkname=Words%20as%20alleles%3A%20A%20null-model%20for%20language%20evolution%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F07%2F08%2Fwords-as-alleles-a-null-model-for-language-evolution%2F&linkname=Words%20as%20alleles%3A%20A%20null-model%20for%20language%20evolution%3F "Email")[](https://www.addtoany.com/share)
