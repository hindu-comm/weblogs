+++
title = "Indic civilization came"
full_title = "Indic civilization came to Southeast Asia because Indian people came to Southeast Asia Lots of them"
date = "2018-09-20"
upstream_url = "https://www.gnxp.com/WordPress/2018/09/20/indic-civilization-came-to-southeast-asia-because-indian-people-came-to-southeast-asia-lots-of-them/"

+++
Source: [here](https://www.gnxp.com/WordPress/2018/09/20/indic-civilization-came-to-southeast-asia-because-indian-people-came-to-southeast-asia-lots-of-them/).

Indic civilization came to Southeast Asia because Indian people came to Southeast Asia. Lots of them

![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/09/angkor-wat-towers.jpg?resize=625%2C387&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/09/angkor-wat-towers.jpg?resize=625%2C387&ssl=1)

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/09/indonesia_brief.jpeg?resize=181%2C279&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/09/indonesia_brief.jpeg?resize=181%2C279&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/0300105185/geneexpressio-20/)Reading [Indonesia: Peoples and Histories](https://www.amazon.com/exec/obidos/ASIN/0300105185/geneexpressio-20/ref=as_at?creativeASIN=0300105185&linkCode=w61&imprToken=Gw9jPkFBs.tKR20KNgfS0w&slotNum=0). I selected it because unlike many books it wasn’t incredibly skewed to the early modern and postcolonial period. The author makes the interesting point that the Islamicization of western Indonesia and the rise of the great Javanese Hindu kingdom of [Majapahit](https://en.wikipedia.org/wiki/Majapahit) occurred around the same time. This, in contrast to the skein of Indic civilization which had been layered over maritime Southeast Asia for hundreds of years before the medieval period, starting around 500 AD with polities such as that of [Kalingga](https://en.wikipedia.org/wiki/Kalingga_Kingdom).

As is usual in these sorts of books, **it is emphasized that Indian civilization spread through *cultural* diffusion** (in contrast to the fact that though Chinese trade was evident and present early on, the cultural impact was minimal). Any migrations are dismissed as legends, with the possible exception of a few elite religious functionaries.

I now believe this is wrong. I’ve discussed this extensively in the past, but the Singapore Genome Variation Project (SGVP) data set along with more Southeast Asians allows me to illustrate rather clearly the issues. The short of it is that it is highly likely that substantial South Asian ancestry exists within Southeast Asia, and that that ancestry is not just a function of colonial contact (e.g., as certainly occurred in Malaysia).

![Click to enlarge](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/09/sea1.png?resize=300%2C179&ssl=1)

Merging the various data sets together I got 172,000 SNPs. The initial PC plot shows that Southeast Asian populations exist on a cline to Indians (these are Tamils from the SGVP). The Burmese and Malays in particular have a wide distribution toward the Indians, indicate of a range of ancestry due to continuous admixture. I separated the SGVP Malays into two groups: Malay, and MalayMix. The MalayMix are those Malays who are more shifted toward the Indians, and like the Burmese show wide variance. The Mala proper as a more straightforward cluster. Shifted toward Indians more as a group.

![Click to enlarge](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/09/sea2.png?resize=300%2C179&ssl=1)

Zooming in you see that Malays (not MalayMix) are not too different from Cambodians, but are slightly shifted toward Papuans. Filipino samples are similar, but further from Indians. Please note that Malaysia and the Philippines both are somewhat shifted toward the Papuans, and these are two nations where there are still extant Negrito populations (in contrast to Cambodia).

Groups like Lahu, Dai, Koreans, and the Dayak samples from Borneo I put in there partly because I assumed they would be less admixed with South Asians.

![Click to enlarge](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/09/seaadmix.png?resize=300%2C643&ssl=1)

Running the samples in an admixture model with K = 5, the results are pretty clean even in unsupervised mode. Part of this is that I did do some outlier analysis and pruning ahead of time.

The Melanesian sample has admixture from something that is maximized in Filipinos and the Borneo samples. This is clearly Austronesian. Notice that the Melanesian samples don’t have any other Southeast Asian ancestry. This indicates that the cosmopolitan nature of some Austronesian groups in maritime Southeast Asia were due to later admixture. In particular, I accept the argument of [Lipson et al.](https://reich.hms.harvard.edu/sites/reich.hms.harvard.edu/files/inline-files/SEA_published_0.pdf) that there was an Austro-Asiatic substrate that was absorbed by incoming Austronesians.

Because I was very particular about sample selection, **the Indians are nearly fixed for their modal ancestral component**. Notice which groups don’t have the Indian ancestry in Southeast Asia: the Borneo samples. Additionally, the frequency in the Philippines may be due to European ancestry. Notice that in the Filipino samples the more diverse individuals tend to have more Indian ancestry, perhaps indicative of cosmopolitanism.

The Lahu and Dai do not have any the Indian modal ancestry, suggesting that this was not present when the Southeast Asians arrived.

The Cambodians have the Indian modal ancestry, as do many of the Malays. The MalayMix population has a lot, as expected. They are rather like the Burmese samples in that way. Some of the Malays don’t have Indian ancestry though. I think this may be due to the reality that the Malay population is actually cosmopolitan in origin, absorbing Indians, Chinese, and, [Orang Asli](https://en.wikipedia.org/wiki/Orang_Asli) groups. The latter of which may not have had Indian ancestry.

![Click to enlarge](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/09/seatree.jpg?resize=300%2C172&ssl=1)

Next I ran some Treemix. Cambodians and MalayMix have affinity with Indians, as you’d expect. The Malay group gets gene flow from the Borneo population, and is positioned rather closer to Indians.

Here are some f3-statistics. At least those with z less than -2.

|          |          |                |              |          |
|:---------|:---------|:---------------|:-------------|:---------|
| **out**  | **p1**   | **p2**         | **f3**       | **z**    |
| Burm     | Korea    | Indian         | -0.00371314  | -40.1063 |
| Burm     | Dai      | Indian         | -0.00368793  | -36.4354 |
| Burm     | Lahu     | Indian         | -0.00363462  | -33.3115 |
| Burm     | Borneo   | Indian         | -0.00297696  | -30.3724 |
| Burm     | Filipino | Indian         | -0.00222445  | -24.3581 |
| Burm     | Korea    | Papuan         | -0.00243075  | -19.9711 |
| Burm     | Dai      | Papuan         | -0.00213815  | -15.6106 |
| Burm     | Malay    | Indian         | -0.00133932  | -15.233  |
| Burm     | Korea    | NAN_Melanesian | -0.00158736  | -12.6428 |
| Burm     | Cambodia | Indian         | -0.000991136 | -10.9863 |
| Burm     | Lahu     | Papuan         | -0.00185199  | -10.8255 |
| Burm     | Dai      | NAN_Melanesian | -0.0011808   | -8.7863  |
| Burm     | Lahu     | NAN_Melanesian | -0.00136834  | -8.35811 |
| Burm     | Korea    | MalayMix       | -0.000470731 | -7.64052 |
| Burm     | Borneo   | Papuan         | -0.00105531  | -7.04586 |
| Burm     | Korea    | Cambodia       | -0.000388278 | -6.74484 |
| Cambodia | Dai      | Indian         | -0.00166543  | -19.5634 |
| Cambodia | Borneo   | Indian         | -0.00135571  | -16.9002 |
| Cambodia | Lahu     | Indian         | -0.00106449  | -10.9303 |
| Cambodia | Dai      | Papuan         | -0.00128886  | -9.86858 |
| Cambodia | Borneo   | Papuan         | -0.000607278 | -4.5826  |
| Cambodia | Dai      | NAN_Melanesian | -0.000449035 | -3.69865 |
| Cambodia | Lahu     | Papuan         | -0.000455081 | -2.64151 |
| Filipino | Borneo   | Papuan         | -0.000462553 | -3.8874  |
| Filipino | Borneo   | NAN_Melanesian | -0.000325208 | -3.54648 |
| Malay    | Filipino | Cambodia       | -0.000763086 | -32.6034 |
| Malay    | Borneo   | Indian         | -0.0020853   | -29.1425 |
| Malay    | Borneo   | Cambodia       | -0.000613918 | -26.5048 |
| Malay    | Borneo   | Papuan         | -0.00223031  | -20.037  |
| Malay    | Dai      | Indian         | -0.00136434  | -14.4879 |
| Malay    | Borneo   | NAN_Melanesian | -0.00131484  | -14.4241 |
| Malay    | Dai      | Papuan         | -0.00188121  | -13.6787 |
| Malay    | Filipino | Indian         | -0.000850623 | -12.4534 |
| Malay    | Borneo   | Burm           | -0.000447661 | -11.0181 |
| Malay    | Dai      | NAN_Melanesian | -0.00122082  | -10.1649 |
| Malay    | Lahu     | Indian         | -0.000658295 | -6.56147 |
| Malay    | Filipino | Papuan         | -0.00061669  | -6.52747 |
| Malay    | Borneo   | MalayMix       | -0.000237474 | -5.75298 |
| Malay    | Lahu     | Papuan         | -0.000942326 | -5.35136 |
| Malay    | Lahu     | NAN_Melanesian | -0.000755618 | -5.0158  |
| Malay    | Korea    | Papuan         | -0.000473046 | -3.65977 |
| Malay    | Dai      | MalayMix       | -8.93679E-05 | -2.12082 |
| MalayMix | Borneo   | Indian         | -0.00469843  | -45.6919 |
| MalayMix | Filipino | Indian         | -0.00377864  | -39.6124 |
| MalayMix | Dai      | Indian         | -0.00412557  | -35.9643 |
| MalayMix | Malay    | Indian         | -0.0028506   | -33.0568 |
| MalayMix | Lahu     | Indian         | -0.00345861  | -28.1738 |
| MalayMix | Korea    | Indian         | -0.00281846  | -23.528  |
| MalayMix | Borneo   | Papuan         | -0.00322593  | -21.9346 |
| MalayMix | Cambodia | Indian         | -0.00192058  | -19.5189 |
| MalayMix | Dai      | Papuan         | -0.00302494  | -19.2884 |
| MalayMix | Borneo   | NAN_Melanesian | -0.00208153  | -15.6894 |
| MalayMix | Dai      | NAN_Melanesian | -0.00213561  | -14.4382 |
| MalayMix | Filipino | Papuan         | -0.0019272   | -14.0354 |
| MalayMix | Korea    | Papuan         | -0.00198522  | -12.4299 |
| MalayMix | Cambodia | NAN_Melanesian | -0.00114701  | -11.2074 |
| MalayMix | Malay    | Papuan         | -0.00123309  | -10.69   |
| MalayMix | Cambodia | Papuan         | -0.00119651  | -10.578  |
| MalayMix | Lahu     | Papuan         | -0.00212514  | -10.5372 |
| MalayMix | Malay    | NAN_Melanesian | -0.00100416  | -9.70624 |
| MalayMix | Lahu     | NAN_Melanesian | -0.0017095   | -9.61884 |
| MalayMix | Korea    | NAN_Melanesian | -0.00120984  | -7.54544 |
| MalayMix | Filipino | NAN_Melanesian | -0.000920147 | -6.96775 |
| MalayMix | Borneo   | Burm           | -0.000446434 | -5.966   |
| MalayMix | Filipino | Cambodia       | -0.000336794 | -5.33937 |
| MalayMix | Filipino | Burm           | -0.000279165 | -4.31016 |
| MalayMix | Burm     | Malay          | -0.000236247 | -4.15308 |

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/10/strangep1.jpeg?resize=183%2C275&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/10/strangep1.jpeg?resize=183%2C275&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/0521530369/geneexpressio-20/ref=as_at/?imprToken=16Hz7GhPBhHmbB6SuL5JHg&slotNum=54&creativeASIN=0878933085&linkCode=w61&imprToken=QiG2bf7fc5-czG6VLZ9cSg&slotNum=164)No big surprises.

I’m trying to get rolloff to work on one of the Reich lab datasets, but it isn’t working (says not enough snps, but the file has 350,000!). I need to establish the admixture date. Perhaps I’ll look to use fineStructure?

Note that this paper shows that of [125 male Cambodians](https://www.ncbi.nlm.nih.gov/pubmed/17381059), 9 of them carry R1a1a. This is unlikely to come from French, and Cambodia, unlike Malaysia, doesn’t have a colonial Indian community.

More to come….

### Related Posts:

- [Indian ancestry maritime Southeast
  Asia](https://www.gnxp.com/WordPress/2020/01/26/indian-ancestry-maritime-southeast-asia/) - [Indian culture came to Southeast Asia through Indian
  people](https://www.gnxp.com/WordPress/2021/01/23/indian-culture-came-to-southeast-asia-through-indian-people/) - [The genetic legacy of Greater
  India](https://www.gnxp.com/WordPress/2016/09/15/the-genetic-legacy-of-greater-india/) - [Likely male-mediated Indianization in Southeast
  Asia](https://www.gnxp.com/WordPress/2018/10/06/likely-male-mediated-indianization-in-southeast-asia/) - [Why Indian forms dominated Chinese forms in
  mainland…](https://www.gnxp.com/WordPress/2019/01/04/why-indian-forms-dominated-chinese-forms-in-mainland-southeast-asia/) - [God's trade](https://www.gnxp.com/WordPress/2010/08/29/gods-trade/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F09%2F20%2Findic-civilization-came-to-southeast-asia-because-indian-people-came-to-southeast-asia-lots-of-them%2F&linkname=Indic%20civilization%20came%20to%20Southeast%20Asia%20because%20Indian%20people%20came%20to%20Southeast%20Asia.%20Lots%20of%20them "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F09%2F20%2Findic-civilization-came-to-southeast-asia-because-indian-people-came-to-southeast-asia-lots-of-them%2F&linkname=Indic%20civilization%20came%20to%20Southeast%20Asia%20because%20Indian%20people%20came%20to%20Southeast%20Asia.%20Lots%20of%20them "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F09%2F20%2Findic-civilization-came-to-southeast-asia-because-indian-people-came-to-southeast-asia-lots-of-them%2F&linkname=Indic%20civilization%20came%20to%20Southeast%20Asia%20because%20Indian%20people%20came%20to%20Southeast%20Asia.%20Lots%20of%20them "Email")[](https://www.addtoany.com/share)
