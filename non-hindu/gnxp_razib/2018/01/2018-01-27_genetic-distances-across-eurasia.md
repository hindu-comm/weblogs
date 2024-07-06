+++
title = "Genetic distances across"
full_title = "Genetic distances across Eurasia"
date = "2018-01-27"
upstream_url = "https://www.gnxp.com/WordPress/2018/01/27/genetic-distances-across-eurasia/"

+++
Source: [here](https://www.gnxp.com/WordPress/2018/01/27/genetic-distances-across-eurasia/).

Genetic distances across Eurasia

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/01/EurasiaFst-1024x641.png?resize=640%2C401&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/01/EurasiaFst-1024x641.png?resize=640%2C401&ssl=1)](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/01/EurasiaFst.jpg?ssl=1)

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/01/eurasianPCA-2.jpg?resize=300%2C193&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/01/eurasianPCA-2.jpg?resize=300%2C193&ssl=1)](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/01/eurasianPCA-2.jpg?ssl=1)I feel that for whatever reason that over the past few years that many people have started to exhibit weak intuitions about the magnitude of between population differences on this weblog. Two suggestions for why this might occur.

\* First, the proliferation of PCA plots with individuals can make it hard to discern averages

\* Second, model-based admixture plots don’t explicitly quantify the differences between the different clusters

To get a better sense of between-group differences I decided to take a step back and look at F_(st).F_(st) basically looks all the genetic variance between groups and quantifies the proportion that can be attributed to differences between groups.

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/01/eurasiaTreemix.jpg?resize=300%2C190&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/01/eurasiaTreemix.jpg?resize=300%2C190&ssl=1)](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/01/eurasiaTreemix.jpg?ssl=1)

The plot at the top of this post is from an[F_(st) matrix](https://www.dropbox.com/s/ch40kgmj6slq58q/FstMatrix.csv?dl=0) I generated with Plink (I wrote a script to do the pairwise comparison). I did some PCA pruning of the populations to be clear (e.g., with both Cambodians and Filipinos I made them more distinct than they would otherwise be). The goal was to give people a sense of genetic distances within regions and between them.

I also generated a PCA plot and a Treemix plot, for the sake of comparison.

It’s also useful to look at a few group comparisons and judge them in a global context.

|                    |                         |          |
|--------------------|-------------------------|----------|
|                    |                         | **Fst**  |
| Tamil              | Telugu                  | 0.0011   |
| Tamil              | Tamil Scheduled Caste   | 0.0016   |
| Tamil              | Bangladeshi             | 0.0024   |
| Tamil              | South Indian Brahmin    | 0.0031   |
| Tamil              | Uttar Pradesh Brahmin   | 0.0041   |
| Tamil              | Sindhi                  | 0.0087   |
| Tamil              | Vietnamese              | 0.0668   |
| *Southern Chinese* | *Northern Chinese*      | *0.0033* |
| *Southern Chinese* | *Vietnamese*            | *0.0034* |
| *Southern Chinese* | *Korea*                 | *0.0045* |
| *Southern Chinese* | *Japanese*              | *0.0087* |
| *Southern Chinese* | *Tamil*                 | *0.0711* |
| *Southern Chinese* | *Polish*                | *0.1141* |
| Gujurati_Patel     | Telugu                  | 0.0062   |
| Gujurati_Patel     | Uttar Pradesh Brahmin   | 0.0065   |
| Gujurati_Patel     | Bangladeshi             | 0.0069   |
| Gujurati_Patel     | Velama                  | 0.0094   |
| Gujurati_Patel     | Sindhi                  | 0.0104   |
| Gujurati_Patel     | Polish                  | 0.0405   |
| Gujurati_Patel     | Japanese                | 0.0781   |
| *GreatBritain*     | *Ireland*               | *0.0015* |
| *GreatBritain*     | *Polish*                | *0.0043* |
| *GreatBritain*     | *Sicily*                | *0.0077* |
| *GreatBritain*     | *Uttar Pradesh Brahmin* | *0.0264* |
| *GreatBritain*     | *Tamil*                 | *0.0430* |
| *GreatBritain*     | *Korea*                 | *0.1130* |
|                    |                         |          |

The non-Brahmin and non-Dalit samples in the 1000 Genomes are not much partitioned much by geography. The Tamil vs. Telugu difference is smaller than that between the British and Irish. Within Tamil Nadu Brahmins though are nearly as different from typical Tamils as Poles are from the English (most of the British sample is English). The biggest differences in Europe are between Sicilians and Northern European groups, which similar in a degree to that between South Indians and Pakistanis. The South Chinese sample is nearly as close to Vietnamese as it is to a North Chinese group, while the difference between Koreans and Chinese is relatively small when compared to the variance you see in South Asia and Europe.

Note: Drift tends to inflateF_(st).

### Related Posts:

- [PCA remains the swiss-army-knife to explore
  population…](https://www.gnxp.com/WordPress/2017/11/16/pca-remains-the-swiss-army-knife-to-explore-population-structure/) - [1 migrant needed to prevent genetic
  divergence](https://www.gnxp.com/WordPress/2012/01/26/1-migrant-needed-to-prevent-genetic-divergence/) - [Cultural group selection across
  time](https://www.gnxp.com/WordPress/2020/08/13/cultural-group-selection-across-time/) - [Ashkenazi Jews are more European in
  ancestry](https://www.gnxp.com/WordPress/2009/09/04/ashkenazi-jews-are-more-european-in-ancestry/) - [Population Pairwise Fst on 250,000
  SNPs](https://www.gnxp.com/WordPress/2021/10/28/pairwise-fst-on-250000-snps/) - [Population substructure in
  Japan](https://www.gnxp.com/WordPress/2008/09/25/population-substructure-in-japan/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F01%2F27%2Fgenetic-distances-across-eurasia%2F&linkname=Genetic%20distances%20across%20Eurasia "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F01%2F27%2Fgenetic-distances-across-eurasia%2F&linkname=Genetic%20distances%20across%20Eurasia "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F01%2F27%2Fgenetic-distances-across-eurasia%2F&linkname=Genetic%20distances%20across%20Eurasia "Email")[](https://www.addtoany.com/share)
