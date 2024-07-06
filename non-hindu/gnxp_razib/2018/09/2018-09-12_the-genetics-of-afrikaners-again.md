+++
title = "The genetics of"
full_title = "The genetics of Afrikaners"
date = "2018-09-12"
upstream_url = "https://www.gnxp.com/WordPress/2018/09/12/the-genetics-of-afrikaners-again/"

+++
Source: [here](https://www.gnxp.com/WordPress/2018/09/12/the-genetics-of-afrikaners-again/).

The genetics of Afrikaners (again)



I personally get asked about the genetics of Afrikaners, because I’ve written about/analyzed the issue before. The main outlines seem to be established, but I thought I might go and revisit it again. The main reason is that we have [ancient South African DNA](https://reich.hms.harvard.edu/sites/reich.hms.harvard.edu/files/inline-files/Skoglund_Cell_2017_3.pdf), and I’ve been adding it to my personal analyses for a while. It might be worthwhile to reanalyze the South Africa samples I do have with some of these added in.

The plot at the top shows the core populations I started with. I did some outlier pruning. I only kept the South African samples that were overwhelmingly white. I picked Malays and a South Indian population because of Cape Coloureds, a mixed-race Afrikaans speaking group which has Asian ancestry that can be attributed to both South and Southeast Asian populations (the Dutch imported many slaves from India and had outposts in Java). I also used Bantu samples from South Africa, Kenya, as well as a Nigeria population. Finally, I also had some Hadza as a different hunter-gatherer population than the San Bushmen. For Europeans, I used white Dutch.

The final marker density as 200,000 SNPs, so not too bad.

As you can see if you click on the image all of the South African whiteswere shifted away from the Dutch. There were two outlier individuals, one of which was closer to the Dutch cluster, and one further. All the other individuals form a neat cluster. None of these individuals were close relatives.

![Click to enlarge](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/09/treemixSA.jpg?resize=300%2C173&ssl=1)

I ran Treemix on the data with multiple migrations until the migrations stopped making sense to me. The African populations’ exhibit migration flows to each other. Much of it is entirely comprehensible. The Esan receive no migration, highlighting that this population did not receive gene flow from any groups in these data. The Kenya Bantus receive gene flow from the direction of Eurasians. This is also certainly Nilotic mediated. The gene flow they receive from the base of the ancient San is more enigmatic, but probably reflects uptake of local ancestry as the Bantus expanded. The southern Bantus receive gene flow from modern San.

The South African whitesreceive gene flow from a position on the graph between the modern San and other non-San African groups.

![Click to enlarge](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/09/sa.png?resize=150%2C479&ssl=1)

Next, I ran Admixture in the unsupervised mode with K = 6. The two populations mostly light-blue are South African whitesand the Dutch, from the top to the bottom. **You can see though that the South African whites clearly have other ancestral components**. Most of these individuals have the components modal in the San, Esan Nigerians, Indians, and Malays. The two outlier individuals are also clear. The individual very close to the Dutch, but shifted toward the Asians, in the PCA does not have any African admixture. The individual shifted more toward the non-Europeans in the PCA also has more non-European fractions of ancestral components (that is, those components modal in non-European populations).

Next, I decided to confirm things by running a three population test. If you read this blog you’ve seen this before. Basically this is measuring shared ancestry by looking at deviations from a particular phylogenetic model: (test population(pop 1, pop2)). The relatedness of the test population to either pop1 or pop2 (that is, it’s a mix of the two) is measured by the negative f3 statistic, and I focused on z-scores greater than two.

Here they are:

|                    |             |                    |         |        |
|:-------------------|------------:|-------------------:|--------:|-------:|
| **Outgroup**       |    **Pop1** |           **Pop2** |  **f3** |  **z** |
| Bantu_NE           | EsanNigeria |              Dutch | -0.0009 |  -6.54 |
| Bantu_NE           | EsanNigeria | South_Africa_White | -0.0010 |  -6.54 |
| Bantu_NE           | EsanNigeria |              Malay | -0.0009 |  -6.33 |
| Bantu_NE           | EsanNigeria |             Telegu | -0.0008 |  -6.00 |
| Bantu_NE           |     Bantu_S | South_Africa_White | -0.0008 |  -4.84 |
| Bantu_NE           |     Bantu_S |              Dutch | -0.0008 |  -4.77 |
| Bantu_NE           |     Bantu_S |              Malay | -0.0007 |  -4.21 |
| Bantu_NE           |     Bantu_S |             Telegu | -0.0007 |  -4.05 |
| Bantu_NE           |       Dutch |        San_Ancient | -0.0009 |  -3.02 |
| Bantu_NE           |       Hadza |        EsanNigeria | -0.0004 |  -2.97 |
| Bantu_NE           |      Telegu |        San_Ancient | -0.0007 |  -2.32 |
| Bantu_NE           |       Malay |        San_Ancient | -0.0007 |  -2.04 |
| Bantu_S            | EsanNigeria |         San_Modern | -0.0028 | -21.62 |
| Bantu_S            | EsanNigeria |        San_Ancient | -0.0039 | -20.78 |
| Bantu_S            | San_Ancient |           Bantu_NE | -0.0030 | -12.91 |
| Bantu_S            |  San_Modern |           Bantu_NE | -0.0019 | -12.45 |
| Bantu_S            |       Dutch |        San_Ancient | -0.0031 | -10.63 |
| Bantu_S            |      Telegu |        San_Ancient | -0.0030 | -10.33 |
| Bantu_S            | San_Ancient | South_Africa_White | -0.0027 |  -9.17 |
| Bantu_S            |       Malay |        San_Ancient | -0.0029 |  -8.97 |
| San_Modern         |       Dutch |        San_Ancient | -0.0091 | -34.96 |
| San_Modern         |      Telegu |        San_Ancient | -0.0087 | -33.86 |
| San_Modern         | San_Ancient | South_Africa_White | -0.0089 | -33.54 |
| San_Modern         | San_Ancient |           Bantu_NE | -0.0063 | -31.93 |
| San_Modern         |       Malay |        San_Ancient | -0.0085 | -30.98 |
| San_Modern         |     Bantu_S |        San_Ancient | -0.0052 | -28.91 |
| San_Modern         |       Hadza |        San_Ancient | -0.0051 | -27.58 |
| South_Africa_White |       Dutch |           Bantu_NE | -0.0017 | -12.96 |
| South_Africa_White | EsanNigeria |              Dutch | -0.0017 | -12.68 |
| South_Africa_White |  San_Modern |              Dutch | -0.0018 | -12.41 |
| South_Africa_White |     Bantu_S |              Dutch | -0.0017 | -12.36 |
| South_Africa_White |       Dutch |        San_Ancient | -0.0021 | -12.14 |
| South_Africa_White |       Hadza |              Dutch | -0.0014 | -10.41 |
| South_Africa_White |       Malay |              Dutch | -0.0007 |  -5.97 |
| South_Africa_White |      Telegu |              Dutch | -0.0003 |  -3.64 |
| Telegu             |       Malay |              Dutch | -0.0004 |  -2.79 |



No surprises so far. One thing that did surprise me though was the extent of the admixture even after PCA outlier removal. So I took the output you saw above and removed individuals that were very mixed, except for the case of the white South Africans. Then, I ran admixture in supervised mode, where the “pure” populations were fixed as references (I merged the moden San without much admixture with the ancient San). You can see the results below:

![Click to enlarge](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/09/admixture2.png?resize=625%2C363&ssl=1)

Re-running the three population test with these “pure” populations I only got significant results for the below cases:

|                    |          |             |         |          |
|:-------------------|---------:|------------:|--------:|---------:|
| **Outgroup**       | **Pop1** |    **Pop2** |  **f3** |    **z** |
| South_Africa_White |    Dutch | EsanNigeria | -0.0017 | -13.1937 |
| South_Africa_White |      San |       Dutch | -0.0020 | -12.6910 |
| South_Africa_White |    Hadza |       Dutch | -0.0014 |  -9.7246 |
| South_Africa_White |    Malay |       Dutch | -0.0009 |  -6.6481 |
| South_Africa_White |   Telegu |       Dutch | -0.0004 |  -4.6167 |

No big surprise.

The average European ancestry I got in my South African white samples, N = 12, is 93.5%. Making a composite individual, note that if someone had great-great-grandparents who were not European, they would be expected to have 6.25% non-European ancestry. That’s 4 generations back. So about 100 years. These individuals are presumably adults. Let’s say they are 25 years old. That goes back 125 years. It’s probably reasonable in a single person admixture people to suggest it was sometime in the mid to late 19th century.

This seems unlikely. The evenness of admixture and balance between different groups indicates that it is older than that, and they are obtaining it from different lineages. Traditional genealogical estimates suggested in the range of 5-7.5% non-European ancestry in Afrikaners, and one study of 185 individuals showed [18% non-European mtDNA](http://www.genza.org.za/index.php?option=com_content&view=article&id=360%3Agenetic-heritage-mtdan-and-ychromosome&catid=129%3Antvl-branch-activities).

I will probably do some ancestry deconvolution and see if I can get a figure for the time of admixture (though the fractions here are very small, as is the sample size of the admixtured population). But the non-European ancestry of Afrikaners is uncannily similar to the non-European ancestry of the Cape Coloureds. That to me leads us to the conclusion that in the early European settler community a fair number of mixed-race women married in. Those mixed-race women who married mixed-race men helped found the Cape Coloureds.

### Related Posts:

- [The non-European admixture in
  Afrikaners](https://www.gnxp.com/WordPress/2021/07/14/the-non-european-admixture-in-afrikaners/) - [Admixture in South African
  Afrikaners](https://www.gnxp.com/WordPress/2014/08/18/admixture-in-south-african-afrikaners/) - [Yes I think about 1% of Afrikaner ancestry is
  probably…](https://www.gnxp.com/WordPress/2017/09/27/yes-i-think-about-1-of-afrikaner-ancestry-is-probably-khoikhoi/) - [The quest for an Afrikaner
  genotype](https://www.gnxp.com/WordPress/2012/01/21/the-quest-for-an-afrikaner-genotype/) - [The non-European ancestry of
  Afrikaners](https://www.gnxp.com/WordPress/2017/09/22/the-non-european-ancestry-of-afrikaners/) - [Supernatural sex
  differences](https://www.gnxp.com/WordPress/2008/04/17/supernatural-sex-differences/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F09%2F12%2Fthe-genetics-of-afrikaners-again%2F&linkname=The%20genetics%20of%20Afrikaners%20%28again%29 "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F09%2F12%2Fthe-genetics-of-afrikaners-again%2F&linkname=The%20genetics%20of%20Afrikaners%20%28again%29 "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F09%2F12%2Fthe-genetics-of-afrikaners-again%2F&linkname=The%20genetics%20of%20Afrikaners%20%28again%29 "Email")[](https://www.addtoany.com/share)
