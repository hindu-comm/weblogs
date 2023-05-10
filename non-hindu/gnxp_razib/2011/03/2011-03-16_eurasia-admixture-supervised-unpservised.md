+++
title = "Eurasia, ADMIXTURE"
full_title = "Eurasia, ADMIXTURE supervised & unsupervised"
date = "2011-03-16"
upstream_url = "https://www.gnxp.com/WordPress/2011/03/16/eurasia-admixture-supervised-unpservised/"

+++
Source: [here](https://www.gnxp.com/WordPress/2011/03/16/eurasia-admixture-supervised-unpservised/).

Eurasia, ADMIXTURE supervised & unsupervised

After [yesterday’s post](http://blogs.discovermagazine.com/gnxp/2011/03/analyzing-ancestry-with-admixture-step-by-step/) I thought it might be useful to see how running ADMIXTURE in different modes would impact the outcomes. Probably the major reason I wish more people would use this software is that **they’d see that this program is *just* a program, and stop assuming its outputs to be divine writ.** Over the years I’ve noticed a tendency of individuals anchoring to one specific plot in one specific paper as if it supported their argument definitively. Running ADMIXTURE or PCA plots via [EIGENSOFT](http://genepath.med.harvard.edu/~reich/Software.htm) makes you very aware of how useless this sort of stance is.

Today I’ve limited the population set to be “South Asia-centric.” Specifically, there are only a few Middle Eastern, European, and East Asian populations, along with one African population. The goal is to figure out how different South Asian groups relate to these non-South Asian groups. First, I ran ADMIXTURE K = 2 to K = 9. Then, I ran ADMIXTURE in “supervised” mode for K = 9. Basically, I set nine populations as as “pure” references. They were:

– Tamil Dalit  
– French Basque  
– Lithuanian  
– Adygei  
– Palestinian  
– Buryat (Altaic region)  
– Dai (South Asian)  
– Papuan  
– Luhya (Kenya)

  
The command was:

    ./admixture -j2 --supervised southasian.bed 9

–j2 is because I have two cores. It can be omitted. To run in supervised mode you need a .pop file (same name as pedigree file, but .pop). After reading the docs and [consulting](https://dienekes.blogspot.com/) someone, it turns out to be really easy to do. Basically the .pop file is a text file with N number of lines, where N = number of individuals in your .fam file. For those individuals you have as part of your reference population have them labeled by their population ID, and those who are not, but are to be calculated, leave those lines blank. For example, an N = 9, with 3 Yoruba, 3 African Americans, and 3 Tuscans, might be like so for the .pop file:

    Yoruba
    Yoruba
    Yoruba

    Tuscan
    Tuscan
    Tuscan

In the slide show below I have some PCA plots. I generated them with EIGENSOFT. It’s rather easy to use this program. Just [download it](http://www.hsph.harvard.edu/faculty/alkes-price/files/EIG3.0.tar.gz). It has some old libraries, so you’ll need to go find those and install them in the appropriate directory. The error will tell you what to get and where to put it once you try and run the program. Once you have EIGENSOFT, go into the POPGEN directory. That’s where you’ll run the commands, again, from the terminal. There are bunch of different commands and such you have to run, and the program takes different formats. You need to convert your .bed files to .ped. So go into the Plink directory, and do this:

    ./plink --bfile yourbedfile --recode --tab --out yourpedfile

This will generate a .ped and .map file. You also need an .ind file. I wrote a script to generate that. It is [here](https://www.gnxp.com/pedToInd.txt). Just rename it from .txt to .pl, and run it like so in the directory where you have your .ped file:

    perl pedToInd.pl "yourpedfile"

Now you have a .ind file. Take the three files, and move them to /EIGENSOFT/POPGEN if they aren’t already there. You can now do your thing by reading the documentation. But to make it simple, I wrote another script by modifying some of the scripts which come with EIGENSOFT. The script has two parameters, the file name, and the number of dimensions you want to generate. You can find it [here](https://www.gnxp.com/eigenscript.txt). Remember to change it from .txt to .pl (or .perl). You run it just like this:

    perl eigenscript.pl "yourpedfile" 4

This is in the case of 4 dimensions, which is what I usually look for. In general I find PCA plots come out quicker than ADMIXTURE, for what it’s worth. After the script is done it will output a bunch of files. You will probably find yourpedfile.evec the easiest one to understand. It will have the IDs in the first column, and the eigenvectors (dimensions) in subsequent columns, in order of their eigenvalue (magnitude). It’s easy to import this into a spreadsheet and manipulate it. I usually pull it into R and plot it in an ad hoc fashion. My experience with Open Office Calc is that too many data points make it *really* sluggish, but it’s doable.

A few notes on the results below. The Luhya Kenyan sample is an African outgroup. I didn’t post PC 1 vs. 2, because as usual it simply separates Africans from non-Africans. PC 2 is the west-east divide in Asia, while 3 seems to be a south vs. north split in Eurasia. PC 4 divides East Asians into northern and southern branches. Note especially the differences between K = 9, K = 9 supervised. I know that unsupervised runs are model-free, but after you’ve run ADMIXTURE a bit I do suspect that implicitly you begin to realize that the input you throw into the machine constrains the range of product.

In terms of concrete results. In the unsupervised run the Kalash generally form their own cluster (albeit, that cluster generally has a low genetic distance to Europeans in comparison to other South Asians). But in the supervised run they’re mostly like the Lithuanians. In contrast, the other Pakistan populations tend to resemble the Adygei, from the Caucasus. Another of my reference populations was Pakistani, and notice that while the Adygei spans the Iranians and Pakistanis, the Palestinian component in South Asians is very low, while it is substantial in Iran.

\[zenphotopress album=274 sort=sort_order number=13\]

### Related Posts:

- [Ancestry analysis
  quickstart](https://www.gnxp.com/WordPress/2020/07/17/ancestry-analysis-quickstart/) - [History and Geography of Genes on a
  Desktop](https://www.gnxp.com/WordPress/2010/10/25/history-and-geography-of-genes-on-a-desktop/) - [A note on open
  genomics](https://www.gnxp.com/WordPress/2012/08/28/a-note-on-open-genomics/) - [Input determining output in
  ADMIXTURE](https://www.gnxp.com/WordPress/2011/03/21/input-determining-output-in-admixture/) - [ADMIXTURE, African Ancestry Project, and confirmation
  bias](https://www.gnxp.com/WordPress/2011/05/02/admixture-african-ancestry-project-and-confirmation-bias/) - [Inferring and visualizing patterns in genomic
  data](https://www.gnxp.com/WordPress/2011/02/09/inferring-and-visualizing-patterns-in-genomic-data/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F03%2F16%2Feurasia-admixture-supervised-unpservised%2F&linkname=Eurasia%2C%20ADMIXTURE%20supervised%20%26%20unsupervised "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F03%2F16%2Feurasia-admixture-supervised-unpservised%2F&linkname=Eurasia%2C%20ADMIXTURE%20supervised%20%26%20unsupervised "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2011%2F03%2F16%2Feurasia-admixture-supervised-unpservised%2F&linkname=Eurasia%2C%20ADMIXTURE%20supervised%20%26%20unsupervised "Email")[](https://www.addtoany.com/share)
