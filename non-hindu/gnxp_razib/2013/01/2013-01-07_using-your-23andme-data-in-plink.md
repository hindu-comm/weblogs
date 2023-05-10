+++
title = "Using your 23andMe data"
full_title = "Using your 23andMe data in Plink"
date = "2013-01-07"
upstream_url = "https://www.gnxp.com/WordPress/2013/01/07/using-your-23andme-data-in-plink/"

+++
Source: [here](https://www.gnxp.com/WordPress/2013/01/07/using-your-23andme-data-in-plink/).

Using your 23andMe data in Plink

With the recent [\$99 price point](https://www.23andme.com/store/cart/) for 23andMe many of my friends have purchased kits (finally!). 23andMe’s interpretive results are pretty rich now, but there are still things missing. There are plenty of [third party tools](http://www.23andyou.com/3rdparty) you can use, but I know some people might want to do their own data analysis. There are many ways you could go about this, but I want to put up some posts on DIY genomic data analysis to making the learning curve a little less steep, and get people started. Motivation to actually begin going down this road is a big issue, but I think once you get over the hump it gets a lot easier.

First, you need [Plink](http://pngu.mgh.harvard.edu/~purcell/plink/download.shtml#download). It is really preferable that you work on a Mac or in Linux to engage in heavy duty analysis, but in this post I’ll assume you are working on the Windows platform. Again, the point here is to make this accessible. Download Plink if you don’t have it, and extract it where ever you like.

  
Plink is a command line tool, which means that you need to into the folder with the old MS-DOS interface. So use the cd command to get into that folder. Here is a screenshot of my shell:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/plinkshot.jpg?resize=553%2C29 "plinkshot")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/plinkshot.jpg?resize=553%2C29 "plinkshot")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/plinkshot.jpg)

The selection “plink –noweb –bfile PhyloF –genome” is a command that I entered. It is not part of the directory structure. If you don’t know about the cd command, please see the [Wikipediaentry](https://en.wikipedia.org/wiki/Cd_(command)). It’s really just a simple way to step through the directory structure of your files and folders.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/git.jpg?resize=259%2C206 "git")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/git.jpg?resize=259%2C206 "git")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/git.jpg)Now you have Plink. We need to put your 23andMe data into pedigree format. Additionally it would be convenient to have other reference data sets . Go to[here](https://github.com/razibkkhan/RazibKhanDataCode). You now need to click the ZIP option. That will download a 74 MB zip containing all the files you see listed to the left. Most of that is in the two zip files, which are pedigree file data sets that I have provided for your future use. More on that later. First you need to use “CONVERT_23AME_PED.pl” This a Perl script which takes the 23andMe text file, and converts it to pedigree format which Plink can use. You need to have Perl to use this script.

If you are on Windows you need to get ActivePerl. [Download it](http://www.activestate.com/activeperl/downloads). Again you have to open the command prompt and go into the appropriate folder. On my computer (this is the first time I’m using Perl on Windows in 10 years, the sacrifices I make for the readership of this weblog!) it is in the C: directory, so you probably have to move “up” the directory tree twice by typing “cd ..” (if you do this you’ll see what I mean). Once you are in the Perl directory you need to go into the bin directory. Remember to move the Perl script into the Perl directory. Here is a screen of what I get when I try and run the Perl script without any parameters:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/ped1.jpg?resize=580%2C148 "ped1")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/ped1.jpg?resize=580%2C148 "ped1")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/ped1.jpg)

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/browse.jpg?resize=140%2C111 "browse")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/browse.jpg?resize=140%2C111 "browse")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/browse.jpg)Basically there needs to be a file for the script to process. You should have a 23andMe text file, your raw data. It will start like so: “genome\_”. If you don’t have it, go into your account, and click “Browse Raw Data.”
On this page there will be options to download various peoples’ data if you have multiple accounts. It will download whoever is selected in your profile (for most it will be just one person of course).

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/down.jpg?resize=159%2C27 "down")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/down.jpg?resize=159%2C27 "down")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/down.jpg)

Now you need to just select the button and enter your password. An 8 MB zip file will come down from the server. Put it into your Perl/bin folder by extracting it. Do not try and process the zip file! Once in there you now add it as your first parameter. I’d rename it something short and sweet since you’ll be typing it in. You don’t need to put a unique id parameter in, but I would if I were you. Try “me.” And “me” for the family id. At some point you’ll do more sophisticated things and need less silly ids, but not right now.

Here’s a screenshot of me running the Perl script with my own data (I renamed the text file). If the file name isn’t recognized make sure that you didn’t add the file extension within Windows, that might confuse it (e.g., for razibdata.txt if that’s what you see in the directory, you’d have to enter in razibdata.txt.txt in the parameter value since the extension is hidden):

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/conv.jpg?resize=472%2C45 "conv")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/conv.jpg?resize=472%2C45 "conv")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/conv.jpg)

There are two output files. In my case they are razibdata.ped and razibdata.map. As you can see they are named from your original file. You need to move both into the Plink directory. The .ped file has your individual data, the first half a dozen columns being the same as the parameters you may, or may not, have entered above. But it is very large because the whole line is filled out with your 23andMe genotype. The .map file basically has the information about the SNPs. These are both text files, and unwieldy. You need to make it into a binary file. At the end of this there are three new files of the same name with extensions .bed, .bim, .fam:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/makebed.jpg?resize=576%2C527 "makebed")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/makebed.jpg?resize=576%2C527 "makebed")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/makebed.jpg)

You can see a lot of information. Most of it is not relevant to you, but note the number of SNPs. So now you have a pedigree file! Great. What do you do with it? Lots of stuff. You can look at the [Plink documentation](http://pngu.mgh.harvard.edu/~purcell/plink/). Because the .bed file is a binary, never open it. The .bim has SNP info. You shouldn’t open this. On the other hand when you merge data sets .fam is useful. It’s a text file with all your individual and family id information. In this case with one file it isn’t informative, though you could change the id by editing the .fam file.

One thing you can do with just one individual is look for runs of homozygosity. The command is:

##### plink –bfile mydata –homozyg

You enter your binary pedigree file name, without the extension. Observe that now we are use –bfile instead of –file. Many commands will be bCommand instead of just Command if you are using binary files instead of the conventional ones. Binary files are smaller and the commands finish much faster, so use them! The output files, unless you use the –out command at the end to define them, usually begin with plink. So above you have plink.hom. It has some interesting information about the runs of homozygosity, but it is probably not too illuminating unless you suspect you are inbred!

Ultimately what I want you do by the end of this is compute an MDS with your own data against a reference set. That’s PHYLO in the data I’ve provided. It has 99,000 SNPs that overlap with 23andMe, and 1,500 individuals. I’ve altered the .fam file so that all the family ids are recognizable as populations. This will make analysis of the output easier for you. First you need to merge the files. It will be useful for you to prune your data set down, since you have a lot of extra SNPs.

Assuming you’ve extracted PHYLO out of the zip downloaded here is my command writing out the list of SNPs within PHYLO:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/snplist.jpg?resize=577%2C506 "snplist")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/snplist.jpg?resize=577%2C506 "snplist")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/snplist.jpg)

You can see from reading this that this data set has \~99,000 SNPs. I pruned it so that it ran quicker for phylogenetic analysis. This is more than a sufficient number for most analysis. What you want to next is create a copy of your own data which doesn’t have so many SNPs, so you can merge them well. Because I created this data set I can tell you that all of the above SNPs are probably in your 23andMe file. With the commands above there is a file, plink.snplist, which you will use to filter your data set.

Here’s how to do it:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/extract.jpg?resize=574%2C586 "extract")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/extract.jpg?resize=574%2C586 "extract")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/extract.jpg)

Now we’ve got it ready to merge. **I will warn you that this takes forever on Windows!**No idea why. Also, Windows tends to do strange things with the file extensions. If Plink tells you that a .fam does not exist, look to the file extension. If you label something as something.fam, it might actually be something.fam.fam. In any case, here’s how you merge:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/merge.jpg?resize=569%2C26 "merge")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/merge.jpg?resize=569%2C26 "merge")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/merge.jpg)

This is going to give you lots of warnings. Often this won’t matter, but sometimes it will tell you that you might need to “flip” one of the files. Try flipping it. If it still doesn’t work I would remove the SNPs causing problems. Something like this:

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/misssnp.jpg?resize=577%2C25 "misssnp")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/misssnp.jpg?resize=577%2C25 "misssnp")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/misssnp.jpg)

Honestly you might have to do a lot of things to get data sets to merge. But this particular combination of 23andMe genotype and PHYLO shouldn’t be too bad. Let’s assume that your merge worked. What do you want to do? One thing that might be interesting is an MDS plot (it’s like a PCA plot).

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/genomeplot.jpg?resize=302%2C22 "genomeplot")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/genomeplot.jpg?resize=302%2C22 "genomeplot")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/genomeplot.jpg)First you run the genome command, which takes forever to finish. It might be best if you did this before you go to sleep, and just check in in the morning. The genome command will produce an output that you’ll use next.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/mdsplot6.jpg?resize=575%2C33 "mdsplot6")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/mdsplot6.jpg?resize=575%2C33 "mdsplot6")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/mdsplot6.jpg)

Notice the input file. That was generated in the previous step. The value 6 is a parameter that defines how many dimensions you want to output. My experience with this is that it doesn’t take too long, so I go for 6 at least. The final result of this is that you have an plink.mds file with an ordered list of family and individual ids, along with positions for 6 dimensions. It should be straightforward to import this into Excel, and then plot your MDS, emphasizing your own position. Since I can no longer use Excel I couldn’t be bothered to figure out how to plot my own position, but the distribution should be familiar.

[![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/mdsfinal.jpg?resize=338%2C314 "mdsfinal")![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/mdsfinal.jpg?resize=338%2C314 "mdsfinal")](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/2013/01/mdsfinal.jpg)

That’s about it for now. I’ll put up another post focusing less on phylogenetics, using the HapMap data set that I provided. I don’t know if I can continue to do this in Windows, but hopefully this illustrated how easy (if tedious) most of this is.

### Related Posts:

- [The Dodecad ancestry
  project](https://www.gnxp.com/WordPress/2010/10/25/the-dodecad-ancestry-project/) - [23andMe is back; but a higher price for fewer
  results?](https://www.gnxp.com/WordPress/2015/10/21/23andme-is-back-but-a-higher-price-for-fewer-results/) - [The future of personal genomics is bright.
  23andMe....](https://www.gnxp.com/WordPress/2013/12/07/the-future-of-personal-genomics-is-bright-23andme/) - [23andme Sale Tomorrow (April 11th,
  2011)](https://www.gnxp.com/WordPress/2011/04/10/23andme-sale-tomorrow-april-11th-2011/) - [\$99 for 1 million
  markers](https://www.gnxp.com/WordPress/2012/12/11/99-for-1-million-markers/) - [23andMe controversies in the genetic genealogy
  community](https://www.gnxp.com/WordPress/2012/01/01/23andme-controversies-in-the-genetic-genealogy-community/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F01%2F07%2Fusing-your-23andme-data-in-plink%2F&linkname=Using%20your%2023andMe%20data%20in%20Plink "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F01%2F07%2Fusing-your-23andme-data-in-plink%2F&linkname=Using%20your%2023andMe%20data%20in%20Plink "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2013%2F01%2F07%2Fusing-your-23andme-data-in-plink%2F&linkname=Using%20your%2023andMe%20data%20in%20Plink "Email")[](https://www.addtoany.com/share)
