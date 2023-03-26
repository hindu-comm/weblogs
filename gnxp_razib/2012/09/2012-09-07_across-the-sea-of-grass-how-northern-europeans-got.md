+++
title = "Across the sea of grass"
full_title = "Across the sea of grass how Northern Europeans got to be ~10% Northeast Asian"
date = "2012-09-07"
upstream_url = "https://www.gnxp.com/WordPress/2012/09/07/across-the-sea-of-grass-how-northern-europeans-got-to-be-10-northeast-asian/"

+++
Source: [here](https://www.gnxp.com/WordPress/2012/09/07/across-the-sea-of-grass-how-northern-europeans-got-to-be-10-northeast-asian/).

Across the sea of grass: how Northern Europeans got to be ~10% Northeast Asian

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/euro.png?resize=548%2C204)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/euro.png?resize=548%2C204)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/euro.png)

**The Pith:** *You’re Asian. Yes, you!*

A conclusion to an important paper, [Nick Patterson, Priya Moorjani, Yontao Luo, Swapan Mallick, NadinRohland, Yiping Zhan, Teri Genschoreck, Teresa Webster, and David Reich](http://www.genetics.org/content/early/2012/09/06/genetics.112.145037.abstract):

*In particular, we have presented evidence suggesting thatthe genetic history of Europe from around 5000 B.C. includes:  
*

*1. The arrival of Neolithic farmers probably from the Middle East.  
*

*2. Nearly complete replacement of the indigenous Mesolithic southern European populationsby Neolithic migrants, and admixture between the Neolithic farmers and the indigenousEuropeans in the north.*

*3. Substantial population movement into Spain occurring around the same time as the archaeologicallyattested Bell-Beaker phenomenon (HARRISON, 1980).  
*

*4. Subsequent mating between peoples of neighboring regions, resulting in isolation-by-distance(LAO et al., 2008; NOVEMBRE et al., 2008). This tended to smooth out population structurethat existed 4,000 years ago.  
*

*Further, the populations of Sardinia and the Basque country today have been substantially lessinfluenced by these events.*



It’s in *Genetics*, [Ancient Admixture in Human History](http://www.genetics.org/content/early/2012/09/06/genetics.112.145037.abstract). Reading through it I can see why it wasn’t published in *Nature* or *Science*: **methods are of the essence.**The authors review five population genetic statistics of phylogenetic and evolutionary genetic import, before moving onto the novel results. These statistics, which measure the possibility of admixture, the extent of admixture, and the date of admixture, are often presented, but nested into supplements, in previous papers by the same group. On the one hand this removes from view the engines which are driving the science. On the other hand I have always appreciated that a benefit of this injustice to the methods which make insight possible is that those without academic access can actually bite into the meat of the researcher’s mode of thought.

I did read through the methods. Twice. I’ve encountered all the statistics before, and I’ve read how they were generated, **but I’ll be honest and admit that I haven’t internalized them.** That has to end now, because the authors have finally released a software package which implements the statistics, ADMIXTOOLS. I plan to use it in the near future, and it is generally best if you understand the underlying mechanisms of a software package if you are at the bleeding end of analytics. I will review the technical points in more detail in future posts, more for my own edification than yours. But for the moment I’ll be a bit more cursory. Four of the tests use comparisons of allele frequencies along explicit phylogenetic trees. That’s so general as to be uninformative as a description, but I think it’s accurate to the best of my knowledge. In the basics the tests are seeing if a model fits the data (as opposed to [TreeMix](https://code.google.com/p/treemix/), which finds the best model out of a range to fit the data). The last method, *rolloff*, infers the timing of an admixture event based upon the decay of [linkage disequilibrium](https://en.wikipedia.org/wiki/Linkage_disequilibrium). In short, admixture between two very distinct populations has the concrete result of producing striking genomic correlations. Over time these correlations dissipate due to recombination. The magnitude of dissipation can allow one to gauge the time in the past when the original admixture occurred.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/tab31.png?resize=312%2C409)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/tab31.png?resize=312%2C409)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/tab31.png)Let’s look at some results. To the left is a section of a table which illustrates the most significant 3-population test scores in the HGDP. The authors checked all the various combinations, and these came out at the top as likely admixtures (i.e., the two sources produce particular patterns in the target). Please remember that these triads should not be taken literally. The Uygur are not descended from Japanese and Italians. Rather, they are descended from populations with genetic affinities to these two sources. Precisely, the Uygurs are descended from Northeast Asian Turks, who assimilated an Indo-European speaking substratum. Most of the results are rather obvious and explicable. Several Middle Eastern populations are known to have Sub-Saharan African admixture, and this is shows up in the results. Others may be more confusing because of the obscurity of the populations, but the Burusho clearly have ancient East Asian ancestry on clustering algorithms, so their presence is not surprising to me. Similarly, the Russians in the HGDP data set have an ‘eastern’ affinity (or at least some do), either due to Finno-Ugric or Turkic ancestry (Tatars regularly assimilated into a Russian ethnic identity as the Tsars expanded their domains).

Some of the other results are more confusing, but one can still find a historical explanation. I have seen evidence that some of the Cambodian samples may have old Indian admixture, though it is not entirely clear to me. But that could explain why there is a signature of West Eurasian admixture into this population (though one wonders why the donor was not Baloch or Pathan.). The Xibo and Tu are Northeast Asian groups, on the border between China proper and the great Eurasian interior. West Eurasian admixture into these groups is not unexpected. West Eurasians are historically attested among the mercenaries and soldiers who arrived on the North China plain after the collapse of the Han dynasty, down to the Alans who served under Kublai Khan. Some of Mongolian and Turkic peoples have individuals who are attested as having characteristics more typical of Europeans (e.g., red hair), so it is likely that this admixture was relatively old and widespread, well before the era of the *Pax Mongolica*.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/220px-Museum_für_Indische_Kunst_Dahlem_Berlin_Mai_2006_063.jpg?resize=220%2C225)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/220px-Museum_für_Indische_Kunst_Dahlem_Berlin_Mai_2006_063.jpg?resize=220%2C225)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/220px-Museum_für_Indische_Kunst_Dahlem_Berlin_Mai_2006_063.jpg)There is a minor dissonant note in these results above. The authors used *rolloff* and inferred an admixture of \~800 years before the present. This is far lower than earlier estimates, which were \>2,000 years before the present. First, I have to say that I was mildly skeptical of the higher value reported earlier. From what little I know the roiling of Turco-Mongol peoples which reordered the Inner Asian landscape did not really establish itself beyond the Chinese fringe at this time. Recall that Central Asia was the domain of the Iranians from prehistory down to the Islamic age (the full transition of Central Asia from Persianate to Turkic has not completed itself to this date, though it has progressed over the centuries since 1000 A.D.). Is it creditable that the Turkic hordes were shut on the other side of the Pamirs for \~1,000 years? Perhaps. But it should warrant skepticism, and openness to the lower values proffered here. The technical reason that the authors consider is that STRUCTURE based inferences may overestimate admixture when reference populations are not appropriate. And yet the authors still concede that 800 years is simply difficult to credit when one consults the historical literature. Strangely though it does align with the date of the Mongol ascendancy, during which time the Uygurs served as civil servants in the barbarian empire (Mongol script derives from the old Uygur script). I managed to dig up a cave painting of Uygurs from this period. There is surely artistic license, but they look rather East Asian to me, as opposed to the hybrid Eurasian appearance modal among modern Uygurs. I won’t touch upon the rather fraught and complex ethnology and ethnogenesis of modern Uygurs, and their relationship to Russian and Chinese ethnographers, but suffice it to say that one needs to be careful about excessive reliance on the literality of historical documents in this area, because of semantic confusions.

So let’s move to the main course: **what’s going on in Europe**? Before putting the spotlight on the macro picture, let’s highlight one secondary aspect: the authors detect evidence of massive gene flow into Spain from Northern Europe \~4,000 years before the present. I’ll let them speak here:

> We hypothesize that we are seeing here a genetic signal of the > ‘Bell-Beaker culture’ (HARRISON, 1980). Initial cultural flow of the > Bell-Beakers appears to have been from South to North, but the full > story may be complex. Indeed one hypothesis is that after an initial > expansion from Iberia there was a reverse flow back to Iberia > (CZEBRESZUK, 2003); **this ‘reflux’ model is broadly concordant with > our genetic results, and if this is the correct explanation it > suggests that this reverse flow may have been accompanied by > substantial population movement.**

Two things to hammer home here. First, **pots move with people.** That’s the inference being drawn from the results. It’s not pots-not-people, it’s people-and-pots. Second, the idea of reversals in the direction of gene flow are intriguing, and, I think need to be taken more seriously. It seems the most plausible candidate here are the people who later became the [Celtiberians](https://en.wikipedia.org/wiki/Celtiberians). Celts have been associated with the Bell Beakers before.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/sard.jpg?resize=150%2C389)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/sard.jpg?resize=150%2C389)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/sard.jpg)But the bigger shock is that **Europeans, and especially Northern Europeans, seem to have a substantial Northeast Asian component.**From the nature of the prose I feel that the authors were definitely taken aback. They basically say so in so many words. In the process of resolving their confusion they skinned the cat every which way. And it does look to me that Northern Europeans are truly descended in part from a population which has affinities to the “First Americans.” I say this specifically because the Siberian samples they tested actually gave a weaker result than the South American Amerindians on the 3-population test.

So what’s the proportion of ancestry? Using the Siberian population they came up with an interval of 5-18 percent in Northern Europeans. The authors used the Sardinians as their “pure” European reference, and admit that it is likely that their admixture estimate is lower than real value due to this fact. Inference is inference, do you trust this result? As it happens **the authors also checked Ötzi the Iceman, and found that like the modern Sardinians he had very little Northeast Asian ancestry.** Ötzi is dated to \~5,000 years before he present. Using *rolloff* the authors estimate an admixture date of \~4,000 years before the present, with an error of nearly 1,000. Additionally, using a different data set they came with an admixture date of \~2,000 years before the present. The latter is obviously wrong (they explain why this could happen in the text). But Ötzi seems to put a boundary on how early it could have been, at least in Southern Europe.

As of publication the authors did not have time to include a reference to this interesting nugget from the abstracts of [ASHG 2012](http://www.ashg.org/2012meeting/abstracts/fulltext/f120123058.htm):

> The complete genome of the 5,300 year old mummy of the Tyrolean > Iceman, found in 1991 on a glacier near the border of Italy and > Austria, has recently been published and yielded new insights into his > origin and relationship to modern European populations. A key finding > of this study has been an apparent recent common ancestry with > individuals from Southern Europe, in particular Sardinians…We used > unpublished data from whole genome sequencing of 452 Sardinian > individuals, together with publicly available data from Complete > Genomics and the 1000 Genomes project, to confirm that the Iceman is > most closely related to contemporary Sardinians. An analysis of these > data together with ancient DNA data from a recently published study on > Neolithic farmers and hunter-gatherers from Sweden shows the Iceman > most closely related to the farmer individual, but not the > hunter-gatherers, with the Sardinians again being the contemporary > Europeans with the highest affinity. **Strikingly, an analysis > including novel ancient DNA data from an early Iron Age individual > from Bulgaria also shows the strongest affinity of this individual > with modern-day Sardinians.** Our results show that the Tyrolean > Iceman was not a recent migrant from Sardinia, but rather that among > contemporary Europeans, Sardinians represent the population most > closely related to populations present in the Southern Alpine region > around 5000 years ago. **The genetic affinity of ancient DNA samples > from distant parts of Europe with Sardinians also suggests that this > genetic signature was much more widespread across Europe during the > Bronze Age.**

I’m betting that this Bulgarian sample won’t exhibit Northeast Asian ancestry, though who knows?

There is a definite geographic pattern within Europe to the strength of the signature of admixture. Northern European populations have the greatest, Southern European populations less, and islanders like Cypriots hardly any. Recall that Sardinians seem to be the best reference, so the \~0 floor may just be a statistical artifact of the measuring stick we have. All that being said, **what went on \<5,000 years before the present to reorder the European landscape?**

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/basque.jpg?resize=300%2C666)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/basque.jpg?resize=300%2C666)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/basque.jpg)The answer may sound crazy, but I think the most probable explanation (even if it is unlikely) is something to do with the Indo-Europeans. We know that Indo-European languages were spoken in Greece by \~1500 BC at the latest. **One thing that is clear from less advanced clustering algorithms is that Basques and Finns are somewhat distinctive in relation to their neighbors.** Though they are not genetically that different, they still lack some “interesting”elements. The results to the left are from [Dienekes](https://dienekes.blogspot.com/), though I’ve replicated it. You can see a similar difference between French, and French Basques. The Basques seem to lack something which has affinities with West Asia. These results, and hints elsewhere, imply that the Basque may not be descended from hunter-gatherers, but the first European farmers. So who came after them?

Though it strikes me as a bizarre conjecture, but I can’t help but imagine the rapid expansion of Indo-European populations into Europe, pushing into the peninsulas of the south. These people may have been a newly formed cosmopolitan mix of West Asians, Northern European Mesolithics, and Northeast Asians. I am at a loss to hazard a guess as to who the First American-like Northeast Asians were, though perhaps they were a western offshoot of the [Kets](https://en.wikipedia.org/wiki/Ket_people)? These people were then absorbed into a melange of tribes who themselves emerged from a synthesis between immigrant West Asian farmers and Northern Europeans. In shorthand: **perhaps the Indo-Europeans were mongrels!** This is not an entirely crazy proposition if you look at the historical record. Conquest populations often synthesized and absorbed those who they conquered. Sometimes they even became the conquered in deep cultural ways (e.g., the Bulgars).

[  
](http://blogs.discovermagazine.com/gnxp/files/2012/09/220px-Bjork_and_the_Swan_Dress.jpg)To ward off accusations of glib and facile speculations, **I well understand that much of what I suggest above is likely wrong.** But bizarre results are going to elicit unhinged hypotheses. And I shouldn’t overplay how strange these results are, I think they are going to stand the test of time. The authors are top notch, and [Dr. Joseph Pickrell found the same pattern](http://arxiv.org/pdf/1206.2332v1.pdf) (a connection between Europeans and Native Americans) with TreeMix! If we sit back and reflect on phenotype it shouldn’t be entirely surprising. Some Scandinavians have always struck me as having a generalized Eurasian cast to their features. Obviously this tendency is stronger among the Sami and Finns, but you can see it in Swedes and others. This is far less evident to me among Southern European peoples. I doubt one would ever confuse a Sardinian for a Eurasian, and I never had that feeling when I spent some time in Italy a few years back (in contrast, some Finns did look Asiatic to me).

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/220px-Bjork_and_the_Swan_Dress.jpg?resize=220%2C230)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/220px-Bjork_and_the_Swan_Dress.jpg?resize=220%2C230)](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2012/09/220px-Bjork_and_the_Swan_Dress.jpg)Finally, **this paper highlights the reality that population genetics has little to do with Plato.** A population within a species is simply not clear and distinct in a sense which would satisfy an Idealist. The authors of the above paper nod to this, illustrating how their tests for admixture are confounded and confused by constant gene flow via isolation-by-distance dynamics. These results indicate that Northern Europeans are on the order of 10% Northeast Asian. Does this mean that Northern Europeans are 10% non-white? Well, it turns out that **white people were always 10% non-white! We just didn’t know.** Is my daughter (who is 50% Northern European) now majority non-white? Oh wait, I’m South Asian. That means [I’m \~50% white](http://www.nature.com/nature/journal/v461/n7263/abs/nature08365.html)! Is my friend who is 25% Japanese now more than 25% Northeast Asian? Words and concepts fail us on the boundary of unfamiliarity, in time and space. Populations and genealogies don’t brook our categorizations. **On a deep level we are all admixtures, and partitioning of ancestry along phylogenetic trees are useful and comprehensible fictions.** These techniques put flesh upon the bones of archaeology and smoke out the outlines of history. But we always need to be aware that that history is not made by humans, rather, we excavating it, and then giving it appropriate glosses in our museums. And yet it *is*.

**Related:** [Dienekes](https://dienekes.blogspot.com/2012/09/estimating-admixture-proportions-and.html) has much to say (obviously).

***Image credit:** [Wikipedia](https://en.wikipedia.org/wiki/File:Museum_f%C3%BCr_Indische_Kunst_Dahlem_Berlin_Mai_2006_063.jpg), [Wikipedia](https://en.wikipedia.org/wiki/File:Bjork_and_the_Swan_Dress.jpg), and [Wikipedia](https://en.wikipedia.org/wiki/File:Giorgia_Palmas.jpg).*

**Cite:** [10.1534/genetics.112.145037](https://dx.doi.org/10.1534/genetics.112.145037)

### Related Posts:

- [Agriculture &
  Europe](https://www.gnxp.com/WordPress/2007/10/01/agriculture-europe/) - [Whole genomes of ancient farmers and
  hunter-gatherers](https://www.gnxp.com/WordPress/2020/11/24/whole-genomes-of-ancient-farmers-and-hunter-gatherers/) - [Peeling away the
  past](https://www.gnxp.com/WordPress/2015/06/06/peeling-away-the-past/) - [More notes on the Neolithic &
  Europe](https://www.gnxp.com/WordPress/2008/01/22/more-notes-on-the-neolithic-europe/) - [How Europe was settled by
  farmers](https://www.gnxp.com/WordPress/2016/01/10/how-europe-was-settled-by-farmers/) - [The introduction of farming & new genes to
  Europe](https://www.gnxp.com/WordPress/2009/09/03/the-introduction-of-farming-new-genes-to-europe/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F09%2F07%2Facross-the-sea-of-grass-how-northern-europeans-got-to-be-10-northeast-asian%2F&linkname=Across%20the%20sea%20of%20grass%3A%20how%20Northern%20Europeans%20got%20to%20be%20~10%25%20Northeast%20Asian "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F09%2F07%2Facross-the-sea-of-grass-how-northern-europeans-got-to-be-10-northeast-asian%2F&linkname=Across%20the%20sea%20of%20grass%3A%20how%20Northern%20Europeans%20got%20to%20be%20~10%25%20Northeast%20Asian "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F09%2F07%2Facross-the-sea-of-grass-how-northern-europeans-got-to-be-10-northeast-asian%2F&linkname=Across%20the%20sea%20of%20grass%3A%20how%20Northern%20Europeans%20got%20to%20be%20~10%25%20Northeast%20Asian "Email")[](https://www.addtoany.com/share)