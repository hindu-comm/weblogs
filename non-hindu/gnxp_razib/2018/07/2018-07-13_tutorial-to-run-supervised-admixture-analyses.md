+++
title = "Tutorial to run"
full_title = "Tutorial to run supervised admixture analyses"
date = "2018-07-13"
upstream_url = "https://www.gnxp.com/WordPress/2018/07/13/tutorial-to-run-supervised-admixture-analyses/"

+++
Source: [here](https://www.gnxp.com/WordPress/2018/07/13/tutorial-to-run-supervised-admixture-analyses/).

Tutorial to run supervised admixture analyses

|                |         |             |                 |               |           |
|:---------------|:--------|:------------|:----------------|:--------------|:----------|
| **ID**         | **Dai** | **Gujrati** | **Lithuanians** | **Sardinian** | **Tamil** |
| razib_23andMe  | 0.14    | 0.26        | 0.02            | 0.00          | 0.58      |
| razib_ancestry | 0.14    | 0.26        | 0.02            | 0.00          | 0.58      |
| razib_ftdna    | 0.14    | 0.26        | 0.02            | 0.00          | 0.57      |
| razib_daughter | 0.05    | 0.14        | 0.29            | 0.18          | 0.34      |
| razib_son      | 0.07    | 0.17        | 0.28            | 0.19          | 0.30      |
| razib_son_2    | 0.06    | 0.19        | 0.29            | 0.19          | 0.27      |
| razib_wife     | 0.00    | 0.07        | 0.55            | 0.38          | 0.00      |

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/04/molecularpopulationgenetics.jpeg?resize=180%2C238&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/04/molecularpopulationgenetics.jpeg?resize=180%2C238&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/0878939652/geneexpressio-20/ref=as_at/?imprToken=GYtvccvxlp7mLzvT7EYqnQ&slotNum=0&imprToken=Ki36zn7u5lcccf4N9d1YDg&slotNum=0&creativeASIN=B00RTY0LPO&linkCode=w61&imprToken=TlKC3Z.2TonJfIX35XEb3g&slotNum=96)This is a follow-up to my earlier post, [Tutorial To Run PCA, Admixture, Treemix And Pairwise Fst In One Command](https://www.gnxp.com/WordPress/2018/07/11/tutorial-to-run-pca-admixture-treemix-and-pairwise-fst-in-one-command/). Hopefully, you’ll be able to run supervised `admixture` analysis with less hassle after reading this. Here I’m pretty much aiming for laypeople. If you are a trainee you need to write your own scripts. The main goal here is to allow people to run a lot of tests to develop an intuition for this stuff.

The above results are from a supervised admixture analysis of my family and myself. The fact that there are three replicates of me is because I converted my [23andMe](https://www.amazon.com/exec/obidos/ASIN/B01LZ5K87Z/geneexpressio-20/ref=as_at?creativeASIN=B073NP8WT3&linkCode=w61&imprToken=RzJuxhmkBoz-sF9efWFnhg&slotNum=50), [Ancestry](https://www.amazon.com/exec/obidos/ASIN/B00TRLVKW0/geneexpressio-20/ref=as_at?creativeASIN=B073NP8WT3&linkCode=w61&imprToken=RzJuxhmkBoz-sF9efWFnhg&slotNum=50), and [Family Tree DNA](https://www.amazon.com/exec/obidos/ASIN/B01NAQ1UCW/geneexpressio-20/ref=as_at?creativeASIN=B073NP8WT3&linkCode=w61&imprToken=RzJuxhmkBoz-sF9efWFnhg&slotNum=50) raw data into plink files three times. Notice that the results are broadly consistent. **This emphasizes that discrepancies between DTC companies in their results are due to their analytic pipeline, not becauseof data quality**.

The results are not surprising. I’m about \~14% “Dai”, reflecting East Asian admixture into Bengalis. My wife is \~0% “Dai”. My children are somewhere in between. At a low fraction, you expect some variance in the F1.

Now below are results for three Swedes with the same reference panel:

|           |          |         |             |                 |               |           |
|:----------|:---------|:--------|:------------|:----------------|:--------------|:----------|
| **Group** | **ID**   | **Dai** | **Gujrati** | **Lithuanians** | **Sardinian** | **Tamil** |
| Sweden    | Sweden17 | 0.00    | 0.09        | 0.63            | 0.28          | 0.00      |
| Sweden    | Sweden18 | 0.00    | 0.08        | 0.62            | 0.31          | 0.00      |
| Sweden    | Sweden20 | 0.00    | 0.05        | 0.72            | 0.23          | 0.00      |

All these were run on supervised admixture frameworks where I used Dai, Gujrati, Lithuanians, Sardinians, and Tamils, as the reference “ancestral” populations. Another way to think about it is: taking the genetic variation of these input groups, what fractions does a given test focal individual shake out at?

The commands are rather simple. For my family:  
`bash rawFile_To_Supervised_Results.sh TestScript`

For the Swedes:  
`bash supervisedTest.sh Sweden TestScript`

The commands need to be run in a folder: `ancestry_supervised/`.

You can download the [zip file](https://www.dropbox.com/s/267ua1gah6caj0o/ancestry_supervised.zip?dl=0). Decompress and put it somewhere you can find it.

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/bioinfodata.jpeg?resize=196%2C257&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/bioinfodata.jpeg?resize=196%2C257&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/B010RHZ208/geneexpressio-20/ref=as_at?creativeASIN=B073NP8WT3&linkCode=w61&imprToken=VJgyWuaCMwPo8ROH7fZKlA&slotNum=48)Here is what the scripts do. First, imagine you have raw genotype files downloaded from [23andMe](https://www.amazon.com/exec/obidos/ASIN/B01LZ5K87Z/geneexpressio-20/ref=as_at?creativeASIN=B073NP8WT3&linkCode=w61&imprToken=RzJuxhmkBoz-sF9efWFnhg&slotNum=50), [Ancestry](https://www.amazon.com/exec/obidos/ASIN/B00TRLVKW0/geneexpressio-20/ref=as_at?creativeASIN=B073NP8WT3&linkCode=w61&imprToken=RzJuxhmkBoz-sF9efWFnhg&slotNum=50), and [Family Tree DNA](https://www.amazon.com/exec/obidos/ASIN/B01NAQ1UCW/geneexpressio-20/ref=as_at?creativeASIN=B073NP8WT3&linkCode=w61&imprToken=RzJuxhmkBoz-sF9efWFnhg&slotNum=50).

Download the files as usual. Rename them in an intelligible way, because the file names are going to be used for generating IDs. So above, I renamed them “razib_23andMe.txt” and such because I wanted to recognize the downstream files produced from each raw genotype. Leave the extensions as they are. You need to make sure they are not compressed obviously. Then place them all in `RAWINPUT/`.

The script looks for the files in there. You don’t need to specify names, it will find them. In `plink` the family ID and individual ID will be taken from the text before the extension in the file name. Output files will also have the file name.

Aside from the raw genotype files, **you need to determine a reference file.** In `REFERENCEFILES/` you see the binary pedigree/plink file Est1000HGDP. The same file from the earlier post. **It would be crazy to run supervised admixture on the dozens of populations in this file.** You need to create a subset.

For the above I did this:  
`grep "Dai\|Guj\|Lithua\|Sardi\|Tamil" Est1000HGDP.fam > ../keep.keep`

Then:  
`./plink --bfile REFERENCEFILES/Est1000HGDP --keep keep.keep --make-bed --out REFERENCEFILES/TestScript`

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/bioiinforpthon.jpeg?resize=201%2C251&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/bioiinforpthon.jpeg?resize=201%2C251&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/B00YSILRYS/geneexpressio-20/ref=as_at?creativeASIN=B073NP8WT3&linkCode=w61&imprToken=2SlOgQWH4EZhWTVbvfyMmw&slotNum=1)When the script runs, it converts the raw genotype files into plink files, and puts them in `INDIVPLINKFILES/`. Then it takes each plink file and uses it as a test against the reference population file. That file has a preprend on group/family IDs of the form AA_Ref\_. **This is essential for the script to understand that this is a reference population.** The .pop files are automatically generated, and the script inputs in the correct K by looking for unique population numbers.

The admixture is going to be slow. I recommend you modify `runadmixture.pl` by adding the number of cores parameters so it can go multi-threaded.

When the script is done it will put the results in `RESULTFILES/`. They will be .csv files with strange names (they will have the original file name you provided, but there are timestamps in there so that if you run the files with a different reference and such it won’t overwrite everything). Each individual is run separately and has a separate output file (a .csv).

But this is not always convenient. **Sometimes you want to test a larger batch of individuals**. Perhaps you want to use the reference file I provided as a source for a population to test? For the Swedes I did this:  
`grep "Swede" REFERENCEFILES/Est1000HGDP.fam > ../keep.keep`

Then:  
`./plink --bfile REFERENCEFILES/Est1000HGDP --keep keep.keep --make-bed --out INDIVPLINKFILES/Sweden`

**Please note the folder.** There are modifications you can make, but the script assumes that the test files are in`INDIVPLINKFILES/`. The next part is important. The Swedish individuals will have AA_Ref\_ prepended on each row since you got them out of Est1000HGDP. **You need to remove this.** If you don’t remove it, it won’t work. In my case, I modified using the vim editor:  
`vim Sweden.fam`

You can do it with a text editor too. It doesn’t matter. Though it has to be the .fam file.

After the script is done, it will put the .csv file in `RESULTFILES/`. It will be a single .csv with multiple rows. Each individual is tested separately though, so what the script does is append each result to the file (the individuals are output to different plink files and merged in; you don’ t need to know the details). If you have 100 individuals, it will take a long time. You may want to look in the .csv file as the individuals are being added to make sure it looks right.

The convenience of these scripts is that it does some merging/flipping/cleaning for you. And, it formats the output so you don’t have to.

I originally developed these scripts on a Mac, but to get it to work on Ubuntu I made a few small modifications. I don’t know if it still works on Mac, but you should be able to make the modifications if not. Remember for a Mac you will need the make versions of plink and admixture.

For supervised analysis, the reference populations need to make sense and be coherent. Please check the earlier [tutorial](https://www.gnxp.com/WordPress/2018/07/11/tutorial-to-run-pca-admixture-treemix-and-pairwise-fst-in-one-command/) and use the PCA functions to remove outliers.

Again, here is the [download to the zip files](https://www.dropbox.com/s/267ua1gah6caj0o/ancestry_supervised.zip?dl=0). And, remember, this only works on Ubuntu for sure (though now I hear it’s easy to run Ubuntu in Windows).

### Related Posts:

- [Ancestry analysis
  quickstart](https://www.gnxp.com/WordPress/2020/07/17/ancestry-analysis-quickstart/) - [Eurasia, ADMIXTURE supervised &
  unsupervised](https://www.gnxp.com/WordPress/2011/03/16/eurasia-admixture-supervised-unpservised/) - [PCA remains the swiss-army-knife to explore
  population…](https://www.gnxp.com/WordPress/2017/11/16/pca-remains-the-swiss-army-knife-to-explore-population-structure/) - [Tutorial to run PCA, Admixture, Treemix and pairwise Fst
  in…](https://www.gnxp.com/WordPress/2018/07/11/tutorial-to-run-pca-admixture-treemix-and-pairwise-fst-in-one-command/) - [D.I.Y. population structure
  analysis](https://www.gnxp.com/WordPress/2011/12/26/d-i-y-population-structure-analysis/) - [A best case scenario for unsupervised
  ADMIXTURE?](https://www.gnxp.com/WordPress/2011/04/07/a-best-case-scenario-for-unsupervised-admixture/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F07%2F13%2Ftutorial-to-run-supervised-admixture-analyses%2F&linkname=Tutorial%20to%20run%20supervised%20admixture%20analyses "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F07%2F13%2Ftutorial-to-run-supervised-admixture-analyses%2F&linkname=Tutorial%20to%20run%20supervised%20admixture%20analyses "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F07%2F13%2Ftutorial-to-run-supervised-admixture-analyses%2F&linkname=Tutorial%20to%20run%20supervised%20admixture%20analyses "Email")[](https://www.addtoany.com/share)
