+++
title = "Reich + Ancient DNA"
full_title = "Reich + Ancient DNA Willerslev + 1000 Genomes South Indian data"
date = "2015-08-01"
upstream_url = "https://www.gnxp.com/WordPress/2015/08/01/riech-ancient-dna-willerslev-1000-genomes-south-indian-data/"

+++
Source: [here](https://www.gnxp.com/WordPress/2015/08/01/riech-ancient-dna-willerslev-1000-genomes-south-indian-data/).

Reich + Ancient DNA Willerslev + 1000 Genomes South Indian data

There’s a lot of genetic data out there. Many of the Reich lab [data](http://genetics.med.harvard.edu/reich/Reich_Lab/Datasets.html) are downloadable. Additionally, [Martin Sikora](https://twitter.com/siko76) gave me a pedigree file with a lot of the ancient genotypes in their recent paper (much appreciated since pulling genotypes out of a lot of big sequence files of varied coverage was going to take some time and care). I merged the two together. But for whatever reason the Reich data set did not include anything from the South Indian samples from the 1000 Genomes. Since I have those, I decided to add a bunch. These are Telegu and Tamil speakers who are neither Brahmins nor scheduled castes and tribes (for those curious, the [Velama](https://en.wikipedia.org/wiki/Velama_(caste)) map pretty well on PCA to the “South Indians” I culled from the 1000 Genomes).

You can download it [here](https://www.dropbox.com/s/1aeiwerqf4t2hjc/HaakRise1000Genomes.tar.gz?dl=0). It’s a 200 MB tarball. It’s in [plink format](https://www.cog-genomics.org/plink2/). I did a minor allele frequency filter out 0.05, and got it down to 385,000 SNPs. Please note: **these data vary greatly in quality on the individual level.** A lot of the ancient samples are missing a lot of positions, so keep that in mind when you analyze them (e.g., if you run PCA some of the dimensions are pretty obviously just ancient samples missing lots of markers in a systematic manner). Finally, there are non-human outgroups in the data. For example if you run a PC analysis without subsettingPC 1 will separate Marmoset from humans, with other primates and ancient samples in spanning the gap. If you leave in ancient populations, a lot of them are going to be of much lower quality than the run-of-the-mill population.

Below are the samples by population and size. Most of the labels are from the Haak et al. data set. Obviously they’re a little idiosyncratic, but I figure you can figure it out. Please note that the .fam file has population labels in the family ID column. I added them manually where they didn’t exist (e.g., the Willerslev data and the 1000 Genomes did not have them, so I added them where appropriate).

|                            |       |
|----------------------------|-------|
| **Group**                  | **N** |
| S_India                    | 136   |
| Yoruba                     | 70    |
| Turkish                    | 56    |
| Spanish                    | 53    |
| Druze                      | 39    |
| Palestinia                 | 38    |
| Han                        | 33    |
| Basque                     | 29    |
| Japanese                   | 29    |
| Sardinian                  | 27    |
| BedouinA                   | 25    |
| French                     | 25    |
| Ulchi                      | 25    |
| Burusho                    | 23    |
| Chukchi                    | 23    |
| Eskimo                     | 22    |
| Russian                    | 22    |
| Tubalar                    | 22    |
| Brahui                     | 21    |
| Mozabite                   | 21    |
| Balochi                    | 20    |
| Biaka                      | 20    |
| Greek                      | 20    |
| Hungarian                  | 20    |
| Makrani                    | 20    |
| Yakut                      | 20    |
| BedouinB                   | 19    |
| Pathan                     | 19    |
| Yukagir                    | 19    |
| Egyptian                   | 18    |
| Kalash                     | 18    |
| Mayan                      | 18    |
| Sindhi                     | 18    |
| Adygei                     | 17    |
| Mandenka                   | 17    |
| Bell_Beaker                | 15    |
| Unetice                    | 15    |
| Yamnaya                    | 15    |
| Hazara                     | 14    |
| Papuan                     | 14    |
| Pima                       | 14    |
| HungaryGam                 | 13    |
| Orcadian                   | 13    |
| Somali                     | 13    |
| AA                         | 12    |
| Bergamo                    | 12    |
| Icelandic                  | 12    |
| Karitiana                  | 12    |
| LBK_EN                     | 12    |
| Masai                      | 12    |
| Corded_Ware                | 11    |
| Khomani                    | 11    |
| Nganasan                   | 11    |
| Norwegian                  | 11    |
| Sicilian                   | 11    |
| SwedenSkog                 | 11    |
| Ami                        | 10    |
| Armenian                   | 10    |
| Balkar                     | 10    |
| Belarusian                 | 10    |
| Bougainvil                 | 10    |
| Bulgarian                  | 10    |
| Chuvash                    | 10    |
| Croatian                   | 10    |
| Czech                      | 10    |
| Dai                        | 10    |
| English                    | 10    |
| Estonian                   | 10    |
| Even                       | 10    |
| Georgian                   | 10    |
| Han_NChina                 | 10    |
| Kalmyk                     | 10    |
| Kusunda                    | 10    |
| Lithuanian                 | 10    |
| Mbuti                      | 10    |
| Miao                       | 10    |
| Mixe                       | 10    |
| Mixtec                     | 10    |
| Mordovian                  | 10    |
| North_Osse                 | 10    |
| Selkup                     | 10    |
| She                        | 10    |
| Thai                       | 10    |
| Tu                         | 10    |
| Tujia                      | 10    |
| Tuvinian                   | 10    |
| Uygur                      | 10    |
| Uzbek                      | 10    |
| Yi                         | 10    |
| Zapotec                    | 10    |
| Abkhasian                  | 9     |
| Atayal                     | 9     |
| Chechen                    | 9     |
| Daur                       | 9     |
| Iranian_Je                 | 9     |
| Jordanian                  | 9     |
| Koryak                     | 9     |
| Kyrgyz                     | 9     |
| Lezgin                     | 9     |
| Libyan_Jew                 | 9     |
| Naxi                       | 9     |
| Nogai                      | 9     |
| Oroqen                     | 9     |
| Ukrainian                  | 9     |
| BantuSA                    | 8     |
| Cambodian                  | 8     |
| Cypriot                    | 8     |
| Esan                       | 8     |
| Hezhen                     | 8     |
| Iranian                    | 8     |
| Kinh                       | 8     |
| Kumyk                      | 8     |
| Lahu                       | 8     |
| Lebanese                   | 8     |
| Luhya                      | 8     |
| Luo                        | 8     |
| Maltese                    | 8     |
| Mansi                      | 8     |
| Mende                      | 8     |
| Punjabi                    | 8     |
| Saudi                      | 8     |
| Surui                      | 8     |
| Syrian                     | 8     |
| Tajik_Pomi                 | 8     |
| Tunisian                   | 8     |
| Tuscan                     | 8     |
| Yemenite_J                 | 8     |
| Aleut                      | 7     |
| Algerian                   | 7     |
| Altaian                    | 7     |
| Ashkenazi                  | 7     |
| Bengali                    | 7     |
| Bolivian                   | 7     |
| Ethiopian                  | 7     |
| Finnish                    | 7     |
| French_Sou                 | 7     |
| Georgian_J                 | 7     |
| Karasuk                    | 7     |
| Motala_HG                  | 7     |
| Tunisian_J                 | 7     |
| Turkmen                    | 7     |
| Xibo                       | 7     |
| Albanian                   | 6     |
| BantuKenya                 | 6     |
| Gambian                    | 6     |
| Hungary_Vatya              | 6     |
| Iraqi_Jew                  | 6     |
| Itelmen                    | 6     |
| Korean                     | 6     |
| Mongola                    | 6     |
| Moroccan_J                 | 6     |
| Saharawi                   | 6     |
| Yemen                      | 6     |
| Afanasievo                 | 5     |
| Armenia_LBA                | 5     |
| Cochin_Jew                 | 5     |
| GujaratiA                  | 5     |
| GujaratiB                  | 5     |
| GujaratiC                  | 5     |
| GujaratiD                  | 5     |
| Hadza                      | 5     |
| Ju_hoan_No                 | 5     |
| MTurkish_J                 | 5     |
| Quechua                    | 5     |
| Spanish_No                 | 5     |
| Andronovo                  | 4     |
| Kikuyu                     | 4     |
| Piapoco                    | 4     |
| Russia_Iron_Age            | 4     |
| Scottish                   | 4     |
| Sintashta                  | 4     |
| Spain_EN                   | 4     |
| Spain_MN                   | 4     |
| Tlingit                    | 4     |
| Armenia_MBA                | 3     |
| Australian                 | 3     |
| Baalberge                  | 3     |
| Benzigerod                 | 3     |
| Datog                      | 3     |
| Dolgan                     | 3     |
| FTurkish_J                 | 3     |
| Hungary_Maros              | 3     |
| Italy_Remedello            | 3     |
| Mezhovskaya                | 3     |
| Sweden_Nordic_BA           | 3     |
| Athabascan                 | 2     |
| Botocudo                   | 2     |
| Canary_Isl                 | 2     |
| Denmark_Nordic_BA          | 2     |
| Denmark_Nordic_LN          | 2     |
| Greenland                  | 2     |
| MiddleDors                 | 2     |
| Nivkh                      | 2     |
| Okunevo                    | 2     |
| Russia_LBA                 | 2     |
| Sweden_Nordic_LN           | 2     |
| AG2                        | 1     |
| Alberstedt                 | 1     |
| Aleutian                   | 1     |
| Altai                      | 1     |
| Ancient_De                 | 1     |
| Ancient_Ne                 | 1     |
| Birnirk                    | 1     |
| Chimp                      | 1     |
| Clovis                     | 1     |
| Denisovan                  | 1     |
| Denmark_Nordic_LBA         | 1     |
| Denmark_Nordic_MN_B        | 1     |
| EBA                        | 1     |
| Esperstedt                 | 1     |
| Germany_BA                 | 1     |
| Gorilla                    | 1     |
| Halberstad                 | 1     |
| hg19ref                    | 1     |
| Hungary_MBA                | 1     |
| Iceman                     | 1     |
| Italian_So                 | 1     |
| Karelia_HG                 | 1     |
| Karsdorf_L                 | 1     |
| Kazakhstan_Sintashta       | 1     |
| Kostenki14                 | 1     |
| LaBrana1                   | 1     |
| LateDorset                 | 1     |
| LBKT_EN                    | 1     |
| Lithuania_LBA              | 1     |
| Loschbour                  | 1     |
| MA1                        | 1     |
| Macaque                    | 1     |
| Marmoset                   | 1     |
| Mezmaiskay                 | 1     |
| Montenegro_Iron_Age        | 1     |
| Montenegro_LBA             | 1     |
| Orang                      | 1     |
| RR                         | 1     |
| Saami_WGA                  | 1     |
| Samara_HG                  | 1     |
| Saqqaq                     | 1     |
| Spain_EN_r                 | 1     |
| Starcevo_E                 | 1     |
| Stuttgart                  | 1     |
| Sweden_Battle_Axe          | 1     |
| Sweden_Battle_AxeNordic_LN | 1     |
| Sweden_Iron_Age            | 1     |
| Thule                      | 1     |
| Ust_Ishim                  | 1     |
| Vindija                    | 1     |

### Related Posts:

- [Unleash the data
  kraken!](https://www.gnxp.com/WordPress/2019/04/05/unleash-the-data-kraken/) - [Allen Ancient DNA Resource in PLINK
  format](https://www.gnxp.com/WordPress/2021/02/26/allen-ancient-dna-resource-in-plink-format/) - [Carl Zimmer profile of the Reich group at
  work](https://www.gnxp.com/WordPress/2018/03/20/carl-zimmer-profile-of-the-reich-group-at-work/) - [New version of Reich lab
  dataset](https://www.gnxp.com/WordPress/2020/03/10/new-version-of-reich-lab-dataset/) - [1000 Genomes data, 290,000
  SNPs](https://www.gnxp.com/WordPress/2015/09/30/1000-genomes-data-290000-snps/) - [Structure in 1000 Genomes South Asian
  data](https://www.gnxp.com/WordPress/2015/07/12/structure-in-1000-genomes-south-asian-data/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F08%2F01%2Friech-ancient-dna-willerslev-1000-genomes-south-indian-data%2F&linkname=Reich%20%2B%20Ancient%20DNA%20Willerslev%20%2B%201000%20Genomes%20South%20Indian%20data "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F08%2F01%2Friech-ancient-dna-willerslev-1000-genomes-south-indian-data%2F&linkname=Reich%20%2B%20Ancient%20DNA%20Willerslev%20%2B%201000%20Genomes%20South%20Indian%20data "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2015%2F08%2F01%2Friech-ancient-dna-willerslev-1000-genomes-south-indian-data%2F&linkname=Reich%20%2B%20Ancient%20DNA%20Willerslev%20%2B%201000%20Genomes%20South%20Indian%20data "Email")[](https://www.addtoany.com/share)
