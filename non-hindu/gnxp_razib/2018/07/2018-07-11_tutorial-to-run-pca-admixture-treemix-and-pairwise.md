+++
title = "Tutorial to run PCA,"
full_title = "Tutorial to run PCA, Admixture, Treemix and pairwise Fst in one command"
date = "2018-07-11"
upstream_url = "https://www.gnxp.com/WordPress/2018/07/11/tutorial-to-run-pca-admixture-treemix-and-pairwise-fst-in-one-command/"

+++
Source: [here](https://www.gnxp.com/WordPress/2018/07/11/tutorial-to-run-pca-admixture-treemix-and-pairwise-fst-in-one-command/).

Tutorial to run PCA, Admixture, Treemix and pairwise Fst in one command

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/Rplot.png?resize=625%2C454&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/Rplot.png?resize=625%2C454&ssl=1)](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/Rplot.png?ssl=1)  
[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/04/molecularpopulationgenetics.jpeg?resize=180%2C238&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/04/molecularpopulationgenetics.jpeg?resize=180%2C238&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/0878939652/geneexpressio-20/ref=as_at/?imprToken=Ki36zn7u5lcccf4N9d1YDg&slotNum=0&creativeASIN=B00RTY0LPO&linkCode=w61&imprToken=TlKC3Z.2TonJfIX35XEb3g&slotNum=96)Today on [Twitter](https://twitter.com/razibkhan) I stated that “if the average person knew how to run PCA with `plink` and visualize with `R` they wouldn’t need to ask me anything.” What I meant by this is that the average person often asks me “Razib, is population X closer to population Y than Z?” To answer this sort of question I dig through my datasets and run a few exploratory analyses, and get back to them.

I’ve been meaning to write up and distribute a “quickstart” for a while to help people do their own analyses. So here I go.

The audience of this post is probably two-fold:

1.  “Trainees” who are starting graduate school and want to dig in
    quickly into empirical data sets while they’re really getting a
    handle on things. This tutorial will probably suffice for a week.
    You should quickly move on to three population and four population
    tests, and `Eigensoft` and `AdmixTools`. As well `fineStructure` 2.  **The larger audience is technically oriented readers who are not,
    and never will be, geneticists professionally.**

What do you need? **First, you need to be able to work in a Linux or** **Linux-environment.** I work both in Ubuntu and on a Mac, but this tutorial and these scripts were tested on Ubuntu. They should work OK on a Mac, but there may need to be some modifications on the bash scripts and such.

Assuming you have a Linux environment, you need to download this [zip](https://www.dropbox.com/s/qtfiuuw18t18hc6/ancestry.zip?dl=0) or [tar.xzfile](https://www.dropbox.com/s/zr2zshwc6auk2os/ancestry.tar.xz?dl=0). Once you open this file it should decompress a folder`ancestry/`.

There are a bunch of files in there. Some of them are scripts I wrote. Some of them are output files that aren’t cleaned up. Some of them are packages that you’ve heard of. Of the latter:

- `admixture`
- `plink`
- `treemix`

You can find these online too, though these versions should work out of the box on Ubuntu. If you have a Mac, you need the Mac versions. Just replace the Mac versions into the folder`ancestry/`. You may need some libraries installed into Ubuntu too if you recompile yourselves. Check the errors and make search engines your friends.

**You will need to install `R` (or R Studio).** If you are running Mac or Ubuntu on the command line you know how to get `R`. If not, Google it.

I also put some data in the file. In particular, a `plink` set of files `Est1000HGDP`. These are merged from the [Estonian Biocentre](http://evolbio.ut.ee), HGDP, and 1000 Genomes. There are 4,899 individuals in the data, with 135,000 high-quality SNPs (very low missingness).

If you look in the “family” file you will see an important part of the structure. So do:

`less Est1000HGDP.fam`

You’ll see something like this:  
`Abhkasians abh154 0 0 1 -9`  
`Abhkasians abh165 0 0 1 -9`  
`Abkhazian abkhazian1_1m 0 0 2 -9`  
`Abkhazian abkhazian5_1m 0 0 1 -9`  
`Abkhazian abkhazian6_1m 0 0 1 -9`  
`AfricanBarbados HG01879 0 0 0 -9`  
`AfricanBarbados HG01880 0 0 0 -9`  

There are 4,899 rows corresponding to each individual. I have used the first column to label the ethnic/group identity. The second column is the individual ID. You can ignore the last 4 columns.

**There is no way you want to analyze all the different ethnic groups.** Usually, you want to look at a few. For that, you can use lots of commands, but what you need is a subset of the rows above. The `grep` command matches and returns rows with particular patterns. It’s handy. Let’s say I want just Yoruba, British (who are in the group GreatBritain), Gujurati, Han Chinese, and Druze. The command below will work (note that Han matches HanBeijing, Han_S, Han_N, etc.).

`grep "Yoruba\|Great\|Guj\|Han\|Druze" Est1000HGDP.fam > keep.txt`

The file `keep.txt` has the individuals you want. Now you put it through `plink` to generate a new file:

`./plink --bfile Est1000HGDP --keep keep.txt --make-bed --out EstSubset`

This new file has only 634 individuals. That’s more manageable. But more important is that there are far fewer groups for visualization and analysis.

As for that analysis, I have a Perl script with a bash script within it (and some system commands). Here is what they do:

1\) they perform PCA to 10 dimensions  
2) then they run admixture on the number of K clusters you want (unsupervised), and generate a .csv file you can look at  
3) then I wrote a script to do pairwise F_(st) between populations, and output the data into a text file  
4) finally, I create the input file necessary for the `treemix` package and then run treemix with the number of migrations you want

There are **lots of parameters and specifications for these packages.** You don’t get those unless you to edit the scripts or make them more extensible (I have versions that are more flexible but I think newbies will just get confused so I’m keeping it simple).

Assuming I create the plink file above, running the following commands mean that `admixture` does K = 2 and `treemix` does 1 migration edge (that is, `-m 1`). The PCA and pairwise **Fst** automatically runs.

`perl pairwise.perl EstSubset 2 1`

Just walk away from your box for a while. The admixture will take the longest. If you want to speed it up, figure out how many cores you have, and edit the file `makecluster.sh`, go to line 16 where you see admixture. If you have 4 cores, then type -j4 as a parameter. It will speed admixture up and hog all your cores.

There is as .csv that has the admixture output. `EstSubset.admix.csv`. If you open it you see something like this:  
`Druze HGDP00603 0.550210 0.449790`  
`Druze HGDP00604 0.569070 0.430930`  
`Druze HGDP00605 0.562854 0.437146`  
`Druze HGDP00606 0.555205 0.444795`  
`GreatBritain HG00096 0.598871 0.401129`  
`GreatBritain HG00097 0.590040 0.409960`  
`GreatBritain HG00099 0.592654 0.407346`  
`GreatBritain HG00100 0.590847 0.409153`  

Column 1 will always be the group, column 2 the individual, and all subsequent columns will be the K’s. Since K = 2, there are two columns. Space separated. You should be able to open the .csv or process it however you want to process it.

You’ll also see two other files: `plink.eigenval plink.eigenvec`. These are generic output files for the PCA. The .eigenvec file has the individuals along with the values for each PC. The .eigenval file shows the magnitude of the dimension. It looks like this:  
`68.7974`  
`38.4125`  
`7.16859`  
`3.3837`  
`2.05858`  
`1.85725`  
`1.73196`  
`1.63946`  
`1.56449`  
`1.53666`  

Basically, this means that PC 1 explains twice as much of the variance as PC 2. Beyond PC 4 it looks like they’re really bunched together. You can open up this file as a .csv and visualize it however you like. **But I gave you an R script.** It’s `RPCA.R`.

You need to install some packages. First, open R or R studio. If you want to go command line at the terminal, type **R**. Then type:  
`install.packages("ggplot2")`  
`install.packages("reshape2")`  
`install.packages("plyr")`  
`install.packages("ape")`  
`install.packages("igraph")`  
`install.packages("ggplot2")`  

Once those packages are loaded you can use the script:  
`source("RPCA.R")`

Then, to generate the plot at the top of this post:  
`plinkPCA()`

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/Rplot2.png?resize=300%2C218&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/Rplot2.png?resize=300%2C218&ssl=1)](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/Rplot2.png?ssl=1)There are some useful parameters in this function. The plot to the left adds some shape labels to highlight two populations. A third population I label by individual ID. This second is important if you want to do outlier pruning, since there are mislabels, or just plain outlier individuals, in a lot of data (including in this). I also zoomed in.

Here’s how I did that:  
`plinkPCA(subVec = c("Druze","GreatBritain"),labelPlot = c("Lithuanians"),xLim=c(-0.01,0.0125),yLim=c(0.05,0.062))`

To look at stuff besides PC 1 and PC 2 you can do `plinkPCA(PC=c("PC3","PC6"))`.

I put the PCA function in the script, but to remove individuals you will want to run the PCA manually:

`./plink --bfile EstSubset --pca 10`

You can remove individuals manually by creating a remove file. What I like to do though is something like this:  
`grep "randomID27 " EstSubset.fam >> remove.txt`

The double-carat **appends** to the remove.txt file, so you can add individuals in the terminal in one window while running PCA and visualizing with R in the other (`Eigensoft` has an automatic outlier removal feature). Once you have the individuals you want to remove, then:  
  
`./plink --bfile EstSubset --remove remove.txt --make-bed --out EstSubset`  
`./plink --bfile EstSubset --pca 10`  

Then visualize!

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/clad.png?resize=300%2C218&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/clad.png?resize=300%2C218&ssl=1)](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/clad.png?ssl=1)To make use of the pairwise F_(st) you need the `fst.R` script. If everything is set up right, all you need to do is type:  
`source("fst.R")`

It will load the file and generate the tree. You can modify the script so you have an unrooted tree too.

The R script is what generates the `FstMatrix.csv` file, which has the matrix you know and love.

So now you have the PCA,F_(st)and admixture. What else? Well, there’s treemix.

I set the number of SNPs for the blocks to be 1000. So -k 1000. As well as global rearrangement. You can change the details in the perl script itself. Look to the bottom. I think the main utility of my script is that it generates the input files. The treemix package isn’t hard to run once you have those input files.

Also, as you know treemix comes with R plotting functions. So run treemix with however many migration edges (you can have 0), and then when the script is done, load R.

Then:  
`>source("src/plotting_funcs.R")`  
`>plot_tree("TreeMix")`  
  
[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/TreeMix.TreeMix.Tree_.png?resize=250%2C167&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/TreeMix.TreeMix.Tree_.png?resize=250%2C167&ssl=1)](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/07/TreeMix.TreeMix.Tree_.png?ssl=1)But actually, you don’t need to do the above. **I added a script to generate a .png file with the treemix plot in pairwise.perl.** It’s called `TreeMix.TreeMix.Tree.png`.

OK, so that’s it.

**To review:**

Download[zip](https://www.dropbox.com/s/qtfiuuw18t18hc6/ancestry.zip?dl=0) or [tar.xzfile](https://www.dropbox.com/s/zr2zshwc6auk2os/ancestry.tar.xz?dl=0). Decompress. All the packages and scripts should be in there, along with a pretty big dataset of modern populations. If you are on a non-Mac Linux you are good to go. If you are on a Mac, you need the Mac versions of [admixture](https://www.genetics.ucla.edu/software/admixture/download.html), [plink](https://www.cog-genomics.org/plink2), and [treemix](https://bitbucket.org/nygcresearch/treemix/downloads/). I’m going to warn youcompiling treemix can be kind of a pain. I’ve done it on Linux and Mac machines, and gotten it to work, but sometimes it took time.

You need [R](https://www.r-project.org) and/or [R Studio](https://www.rstudio.com) (or something like R Studio). Make sure to install the packages or the scripts for visualizing results from PCA and pairwiseF_(st) won’t work.\*

There is already a .csv output from admixture. The PCA also generates expected output files. You may want to sort, so open it in a spreadsheet.

**This is potentially just the start. But if you are a** layperson **with a nagging question and can’t wait for me, this could be you where you need to go!**

\* I wrote a lot of these things piecemeal and often a long time ago. It may be that not all the packages are even used. Don’t bother to tell me.

### Related Posts:

- [Ancestry analysis
  quickstart](https://www.gnxp.com/WordPress/2020/07/17/ancestry-analysis-quickstart/) - [PCA remains the swiss-army-knife to explore
  population…](https://www.gnxp.com/WordPress/2017/11/16/pca-remains-the-swiss-army-knife-to-explore-population-structure/) - [Tutorial to run supervised admixture
  analyses](https://www.gnxp.com/WordPress/2018/07/13/tutorial-to-run-supervised-admixture-analyses/) - [Using your 23andMe data: exploring with
  MDS](https://www.gnxp.com/WordPress/2013/01/08/using-your-23andme-data-exploring-with-mds/) - [Eurasia, ADMIXTURE supervised &
  unsupervised](https://www.gnxp.com/WordPress/2011/03/16/eurasia-admixture-supervised-unpservised/) - [D.I.Y. population structure
  analysis](https://www.gnxp.com/WordPress/2011/12/26/d-i-y-population-structure-analysis/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F07%2F11%2Ftutorial-to-run-pca-admixture-treemix-and-pairwise-fst-in-one-command%2F&linkname=Tutorial%20to%20run%20PCA%2C%20Admixture%2C%20Treemix%20and%20pairwise%20Fst%20in%20one%20command "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F07%2F11%2Ftutorial-to-run-pca-admixture-treemix-and-pairwise-fst-in-one-command%2F&linkname=Tutorial%20to%20run%20PCA%2C%20Admixture%2C%20Treemix%20and%20pairwise%20Fst%20in%20one%20command "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F07%2F11%2Ftutorial-to-run-pca-admixture-treemix-and-pairwise-fst-in-one-command%2F&linkname=Tutorial%20to%20run%20PCA%2C%20Admixture%2C%20Treemix%20and%20pairwise%20Fst%20in%20one%20command "Email")[](https://www.addtoany.com/share)
