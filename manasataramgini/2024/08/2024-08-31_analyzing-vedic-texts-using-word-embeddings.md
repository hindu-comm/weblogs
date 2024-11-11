+++
title = "Analyzing Vedic texts"
full_title = "Analyzing Vedic texts using word embeddings"
upstream_url = "https://manasataramgini.wordpress.com/2024/08/31/analyzing-vedic-texts-using-word-embeddings/"
date = "2024-08-31"

+++
Source: [here](https://manasataramgini.wordpress.com/2024/08/31/analyzing-vedic-texts-using-word-embeddings/).

Analyzing Vedic texts using word embeddings

Word2Vec is a natural language processing technique developed by Mikolov and colleagues that generates word embeddings, i.e., dense vector representations of words in a text, which capture their semantic relationships. It has become central to textual analysis in the past decade, along with a more recent, similar method, “fasttext,” which further performs sub-word analysis. Briefly, its workings can be explained thus:  
1. It digests the input text into a vocabulary of unique words of size ![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002). This vocabulary is then used to define the architecture of a shallow neural network that is at the heart of this method. The input and output layers of the NN, respectively, have one neuron for each word in the vocabulary. The hidden layer has a much smaller set of neurons, and it learns to represent words as dense vectors with a pre-defined number of dimensions ![m](https://s0.wp.com/latex.php?latex=m&bg=ffffff&fg=333333&s=0&c=20201002). This results in a ![n \\times m](https://s0.wp.com/latex.php?latex=n+%5Ctimes+m&bg=ffffff&fg=333333&s=0&c=20201002) matrix that can be analyzed directly or via principle component analysis.  
2. The unsupervised training objective of the Word2Vec NN is to predict words from their context or vice versa. Thus, the models learn vector representations capturing semantic relationships between words.  
3. The Word2Vec implements two models: (1) Continuous Bag of Words (cbow), which predicts a target word from its context words, and (2) skip-gram, which predicts context words given a target word. To define the context of each word, Word2Vec uses a sliding window of size ![k](https://s0.wp.com/latex.php?latex=k&bg=ffffff&fg=333333&s=0&c=20201002). The output embeddings are very sensitive to this parameter, and empirical analysis is needed to get the “right” ![k](https://s0.wp.com/latex.php?latex=k&bg=ffffff&fg=333333&s=0&c=20201002).  
4. In principle, upon training, words with similar semantic contexts should be close to each other in the output vector space of ![m](https://s0.wp.com/latex.php?latex=m&bg=ffffff&fg=333333&s=0&c=20201002)-dimensions. This can be explored by using cosine similarity between a pair of vectors ![(\\overrightarrow{A}, \\overrightarrow{B})](https://s0.wp.com/latex.php?latex=%28%5Coverrightarrow%7BA%7D%2C+%5Coverrightarrow%7BB%7D%29&bg=ffffff&fg=333333&s=0&c=20201002):  
![\\cos(\\theta)=\\dfrac{\\overrightarrow{A} \\cdot \\overrightarrow{B}}{\|\|\\overrightarrow{A}\|\|
\\overrightarrow{B}\|\|}](https://s0.wp.com/latex.php?latex=%5Ccos%28%5Ctheta%29%3D%5Cdfrac%7B%5Coverrightarrow%7BA%7D+%5Ccdot+%5Coverrightarrow%7BB%7D%7D%7B%7C%7C%5Coverrightarrow%7BA%7D%7C%7C+%5Coverrightarrow%7BB%7D%7C%7C%7D&bg=ffffff&fg=333333&s=0&c=20201002)  
Thus, if one takes a given word as a query, one can extract the words closest to it in the output vector space based on cosine similarity.

In practice, other than the model type, output vector dimension, and sliding window size, the output matrix is highly sensitive to some other hyper-parameters going into the training. These include the number of iterations over the entire corpus, the learning rate, which is the step size for the gradient descent algorithm, and the number of random words drawn from the vocabulary as “negative” samples (negative sampling). Word2Vec works best with a large corpus. However, it is hindered considerably by highly inflected and euphonically transformed (saṃdhi) languages like Sanskrit unless the text is lemmatized. It also fares poorly if the language/text is riddled with polysemic words.

We sought to apply Word2Vec to Vedic texts to see if they capture anything meaningful. We were not necessarily expecting any profound insight but merely checking if it could capture any meaningful features that we were quite certain of from our manual analysis. While the large size of the Vedic texts is a positive for Word2Vec analysis, they face the disadvantage of inflection and euphonicity. Hence, we used two texts for the purpose of our analysis: the padapāṭha of the Ṛgveda (RV) and Keith’s English translation of the Taittirīya Saṃhitā (TS) of Kṛṣṇa-Yajurveda. The first deals with the issue of euphonicity as all saṃdhi-s are dissolved in it. The second transforms the text into a non-inflectional language, allowing for an analysis unhindered to a degree by the dispersion of the vocabulary from the highly inflected nature of Sanskrit. Our empirical analysis showed that skip-gram outperformed cbow for these texts.

The RV padapāṭha has a word length per ṛk in the range of 4..39 with a median length of 19 and a mean length of 17.7. Thus, we set up the skip-gram model with the following hyper-parameters: a sliding window = 18; learning rate = 0.05; vector dimension = 100; \# of iterations ![i= 50](https://s0.wp.com/latex.php?latex=i%3D+50&bg=ffffff&fg=333333&s=0&c=20201002), minimum count of word to be considered = 7. Even with extensive hyper-parameter tuning, convergence is not achieved, and the word embeddings from each run are different. However, if we take the nearest cosine distance neighbors of a given anchor word over multiple runs, we obtain overlapping results. Thus, we can aggregate the results of multiple runs into a single table by taking the mean cosine distance. Below is one example for the word “Varuṇa” in the vocative case (Table 1).

| term    | Cos.dist |
|:--------|---------:|
| Mitra   |     0.80 |
| Aryaman |     0.78 |
| āgaḥ    |     0.70 |
| Ādityāḥ |     0.67 |
| vocata  |     0.66 |
| cakṛma  |     0.66 |
| mṛḻa    |     0.65 |
| adite   |     0.65 |
| anṛtam  |     0.65 |
| Savitaḥ |     0.65 |
| priya   |     0.65 |
| rājan   |     0.64 |
| mo      |     0.64 |
| heḻaḥ   |     0.64 |
| āyam    |     0.64 |
| dyūn    |     0.63 |
| mā      |     0.62 |

It captures many essential features of the entreaties directed to the god in the RV. He is known as the king (rājan). His association with brother Āditya deities (Mitra, Aryaman, generic Ādityāḥ) and their mother (Adite) also clearly emerges. We see the simultaneous allusions to his fury (heḻaḥ) and its counter — his mercy (mṛḻa). The entreaties for mercy are primarily from punishment for the sins of falsehood (anṛtam) and transgression of the natural law (āgaḥ) in the hope that the god might become dear (priya).

[![RV_pada1](https://manasataramgini.wordpress.com/wp-content/uploads/2024/08/rv_pada1.png)](https://manasataramgini.wordpress.com/wp-content/uploads/2024/08/rv_pada1.png)Figure 1.

One could also do PCA on the output matrix for dimensionality reduction to see where particular words fall in 2D space. As an example, we chose multiple prominent deities from the RV in the nominative case and plotted the first and second components of their embeddings (red points in Figure 1) against the backdrop of the same components of the rest of the vocabulary (Figure 1, gray points). They are depicted in terms of the position from the centroid of these components for the entire vocabulary. One can see a spatial grouping of the Āditya-s and Aditi closer to the centroid. Similarly, the Rudrian deities, Rudra, Marut-s and the Aśvin-s, occupy their own distinct space. The so-called “yājñīkī devatā”, or the major focal deities of the śrauta ritual — Indra, Agni, Soma, Savitṛ — unique occupy distant positions, each of their own. Thus, the embeddings are capturing some real, subtle linkages that can be seen even on dimensionality reduction. One can cycle through further components (1..4) and see some other subtle linkages (Figure 2).

[![RV_pada2](https://manasataramgini.wordpress.com/wp-content/uploads/2024/08/rv_pada2.png)](https://manasataramgini.wordpress.com/wp-content/uploads/2024/08/rv_pada2.png)Figure 2.

The second analysis was on the translated TS (TS-t). For this analysis, taking into account the structure of English, we ignored a body of “stop words” namely, prepositions, common conjunctions, interjections like “verily, indeed, O”, pronouns and filler verbs used to translate certain mantra expressions. The window size was set to the modal sentence length of 11 because the TS-t, reflecting the original, has a very wide range of sentence lengths from verse to prose. A similar procedure as done above for the RV-padapāṭha was carried out with four prominent gods as queries. The training of the NN was done four times, and the 12 most cosine similar words to the query deity were extracted and aggregated into a single table. The closest words for each of the query deities are tabulated below:

**Rudra**

| term         | Cos.dist |
|:-------------|---------:|
| blow         |     0.71 |
| secondary    |     0.71 |
| Bhava        |     0.70 |
| loosen       |     0.69 |
| terrible     |     0.69 |
| dart         |     0.69 |
| liver        |     0.68 |
| dogs         |     0.68 |
| appeases     |     0.67 |
| Tiṣya        |     0.67 |
| Vāstoṣpati   |     0.67 |
| cast         |     0.67 |
| tiger        |     0.67 |
| anger        |     0.67 |
| stirs        |     0.66 |
| designs      |     0.66 |
| appeased     |     0.66 |
| instigations |     0.66 |
| thick        |     0.65 |

**Indra**

| term       | Cos.dist |
|:-----------|---------:|
| Bṛhaspati  |     0.73 |
| slew       |     0.72 |
| Vṛtra      |     0.72 |
| Marut-s    |     0.69 |
| string     |     0.69 |
| saviour    |     0.69 |
| Ṛbhu-s     |     0.68 |
| fellowship |     0.68 |
| gladness   |     0.68 |
| bearers    |     0.68 |
| fumigate   |     0.68 |
| Mahendra   |     0.68 |
| fierce     |     0.68 |
| protects   |     0.68 |
| svasti     |     0.68 |
| driver     |     0.67 |
| infirm     |     0.67 |
| panic      |     0.67 |
| lordly     |     0.66 |

**Varuṇa**

| term        | Cos.dist |
|:------------|---------:|
| Mitra       |     0.89 |
| noose       |     0.77 |
| loosed      |     0.76 |
| pillar      |     0.70 |
| Ka          |     0.70 |
| stagnant    |     0.70 |
| soothing    |     0.69 |
| frees       |     0.69 |
| protecting  |     0.69 |
| bought      |     0.69 |
| Māruta      |     0.69 |
| Dyutāna     |     0.69 |
| savior      |     0.69 |
| propitiates |     0.68 |
| seize       |     0.68 |
| unyoked     |     0.68 |
| tied        |     0.68 |
| unloose     |     0.67 |
| slaughtered |     0.67 |

**Viṣṇu**

| term         | Cos.dist |
|:-------------|---------:|
| dwarf        |     0.74 |
| strove       |     0.72 |
| stride       |     0.72 |
| stepping     |     0.69 |
| fumigate     |     0.69 |
| Śipivisṭa    |     0.68 |
| stealers     |     0.67 |
| destroyers   |     0.67 |
| step         |     0.67 |
| string       |     0.66 |
| addressed    |     0.66 |
| Indra        |     0.65 |
| imprecations |     0.65 |
| redundancy   |     0.65 |

Examining these tables, one can see each of them broadly captures some key features of the said deity: 1. Ectypes/ Ectypic deity appellations (e.g., Mahendra for Indra; Śipivisṭa for Viṣṇu); 2. Common partner deities (e.g., Mitra for Varuṇa); 3. Key features of the deity: e.g., Indra as the slayer of Vṛtra; striding/steps as a feature of Viṣṇu; the noose as an accouterment of Varuṇa etc. Thus, the word embeddings give a reasonable “executive” summary of each of the deities, which would be immediately familiar to those who understand their character in the Śruti. However, there are several words that are puzzling and not immediately apparent. These stem from the local minima, and yet others are not captured as 4 independent trainings of the NN are not sufficient for a meta-convergence. In conclusion, the word2vec method with the skip-gram model is a useful starting point for the analysis of a large textual corpus, as the shallow NN can be rapidly trained on a generic laptop. It can be used in a complementary fashion to other techniques, such as the word cloud.
