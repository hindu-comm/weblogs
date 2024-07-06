+++
title = "The nonEuropean ancestry"
full_title = "The nonEuropean ancestry of Afrikaners"
date = "2017-09-22"
upstream_url = "https://www.gnxp.com/WordPress/2017/09/22/the-non-european-ancestry-of-afrikaners/"

+++
Source: [here](https://www.gnxp.com/WordPress/2017/09/22/the-non-european-ancestry-of-afrikaners/).

The non-European ancestry of Afrikaners

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/Southafrica1.jpg?resize=600%2C550)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/Southafrica1.jpg?resize=600%2C550)](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/Southafrica1.jpg)  
[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/afrikaners.jpg?resize=175%2C250)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/afrikaners.jpg?resize=175%2C250)](https://www.amazon.com/exec/obidos/ASIN/0813930553/geneexpressio-20)A few years ago I got some South African genotypes. Some of the individuals were clearly African. A few mapped perfectly upon Northern Europeans. **But many of the samples consistently were European but shifted toward non-European populations.**

Based on history of the assimilation of slaves into the European population of Cape Colony in the 18th century, my assumption is that these individuals are Afrikaners.

Recently I realized that [Brenna Henn had released some more Khoisan](https://ecoevo.stonybrook.edu/hennlab/data-software/) samples, so I decided to look at this question of admixture again. The two Khoisan populations are the Nama and the Khomani. I removed those with lots of Bantu and European admixture and combined them together into one population.

Running unsupervised Admixture shows how distinct the South African whites are.

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/southafrica2.jpg?resize=600%2C651)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/southafrica2.jpg?resize=600%2C651)](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/southafrica2.jpg)

The average Utah white in this sample (this population is a mix of British, German, and Scandinavian in ancestry) is 99% European modal cluster, and 1% South Asian. The average for the white South Africans in this data set is 94% European modal cluster. The residual is 1% East Asian (Dai modal), 1% Khosian, 1% non-Khoisan African, and 2% South Asian.

I ran Treemix a bunch of times, and every single plot came out like this when I ran it for three migrations:

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/SouthAfrica.8.Tree_.jpg?resize=600%2C400)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/SouthAfrica.8.Tree_.jpg?resize=600%2C400)](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/SouthAfrica.8.Tree_.jpg)

The gene flow from the Utah whites to the Gujuratis is simply an artifact of the fact that the Gujurati sample is mixed caste, and some of the Brahmin or Lohannas have more “Ancestral North Indian.” The gene flow from the Europeans to the Khoisan is probably real, or, might be due to pastoralist admixture via East Africans. The last migration arrow goes fromtheAfrican populations to the South African whites, with a shift toward the Khoisan.

I also ran a three population test where A is the outgroup, and B and C are a clade. A significantly negative f3-statistic indicates admixture in population A. The negative values are listed below:

|              |              |           |              |              |             |
|--------------|--------------|-----------|--------------|--------------|-------------|
| **A**        | **B**        | **C**     | **f3**       | **f3-error** | **Z-score** |
| Gujrati      | Dai          | UtahWhite | -0.00121718  | 0.000140141  | -8.68539    |
| South_Africa | EsanNigeria  | UtahWhite | -0.00127718  | 0.000147982  | -8.63059    |
| South_Africa | Khoisan_SA   | UtahWhite | -0.0012928   | 0.000151416  | -8.53802    |
| Gujrati      | South_Africa | Dai       | -0.000778791 | 0.000155656  | -5.00329    |
| South_Africa | Dai          | UtahWhite | -0.000541974 | 0.000133262  | -4.06699    |
| South_Africa | UtahWhite    | Gujrati   | -0.000103581 | 8.46193e-05  | -1.22408    |

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/convenant.jpeg?resize=184%2C274)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2017/09/convenant.jpeg?resize=184%2C274)](https://www.amazon.com/exec/obidos/ASIN/B00H6JHMMM/geneexpressio-20)This aligns well with the Admixture results. **Afrikaners have both African ancestries, and, Asian ancestry**.

In James Michener’s [The Covenant](https://www.amazon.com/exec/obidos/ASIN/B00H6JHMMM/geneexpressio-20) one of the plot lines alludes to mixed ancestry in one of the Afrikaner families. The results above suggest that mixed ancestry is very common, and perhaps ubiquitous, in this population. True, there are some Afrikaners such as [Hendrik Verwoerd](https://en.wikipedia.org/wiki/Hendrik_Verwoerd) who migrated to South Africa from the Netherlands in the past century or so, but these are uncommon to my knowledge.

### Related Posts:

- [Admixture in South African
  Afrikaners](https://www.gnxp.com/WordPress/2014/08/18/admixture-in-south-african-afrikaners/) - [The non-European admixture in
  Afrikaners](https://www.gnxp.com/WordPress/2021/07/14/the-non-european-admixture-in-afrikaners/) - [Not all the Dominions are the
  same](https://www.gnxp.com/WordPress/2014/08/19/not-all-the-dominions-are-the-same/) - [The quest for an Afrikaner
  genotype](https://www.gnxp.com/WordPress/2012/01/21/the-quest-for-an-afrikaner-genotype/) - [Yes I think about 1% of Afrikaner ancestry is
  probably…](https://www.gnxp.com/WordPress/2017/09/27/yes-i-think-about-1-of-afrikaner-ancestry-is-probably-khoikhoi/) - [The Cape Coloureds are a mix of
  everything](https://www.gnxp.com/WordPress/2011/06/16/the-cape-coloureds-are-a-mix-of-everything/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F09%2F22%2Fthe-non-european-ancestry-of-afrikaners%2F&linkname=The%20non-European%20ancestry%20of%20Afrikaners "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F09%2F22%2Fthe-non-european-ancestry-of-afrikaners%2F&linkname=The%20non-European%20ancestry%20of%20Afrikaners "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2017%2F09%2F22%2Fthe-non-european-ancestry-of-afrikaners%2F&linkname=The%20non-European%20ancestry%20of%20Afrikaners "Email")[](https://www.addtoany.com/share)
