+++
title = "Running AdmixTools"
full_title = "Running AdmixTools through R – admixr"
date = "2018-12-14"
upstream_url = "https://www.gnxp.com/WordPress/2018/12/14/running-admixtools-through-r-admixr/"

+++
Source: [here](https://www.gnxp.com/WordPress/2018/12/14/running-admixtools-through-r-admixr/).

Running AdmixTools through R – admixr

[![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/12/rfordatascience.png?resize=183%2C275&ssl=1)![](https://i0.wp.com/www.gnxp.com/WordPress/wp-content/uploads/2018/12/rfordatascience.png?resize=183%2C275&ssl=1)](https://www.amazon.com/exec/obidos/ASIN/B01NAJAEN5/geneexpressio-20?imprToken=Q1mry5m2z173HEA7UGeZtg&slotNum=0&creativeASIN=0195149300&linkCode=w61&imprToken=rji8sv2CD1zc4Tl3VlqU5Q&slotNum=124)One of the reasons that I don’t post [AdmixTools](https://github.com/DReichLab/AdmixTools) results too much is that the framework requires more statistical “deep thought” than just popping out a PCA or even running some model-based clustering. Read the methods supplements of one of the Reich lab’s papers, and you’ll see what I’m getting at. But a more prosaic reason is that I generally work in the plink format, and format conversion, as well as editing parameter files, is a pain. In general, I don’t do much “exploratory AdmixTools” stuff for a reason.

[Martin Petr](https://twitter.com/fleventy5/status/1073192381959294976) has made the second excuse a lot less of an excuse. His [admixr](https://bodkan.net/admixr/articles/tutorial.html#qpwave-and-qpadm) package gives one an easy interface into AdmixTools. In particular, it allows one not to have to edit parameter files so much. It took me about \~15 minutes to get it downloaded and running. I’m on a Mac and for R use RStudio.

– remember to install wget if you are on a Mac (this will show up if you want to use online datasets)

– You need to make sure to set the path to AdmixTools. In the RStudio console, I just entered:

`Sys.setenv("PATH"="~/MyPath/To/AdmixTools/bin/")`

If you can get[AdmixTools](https://github.com/DReichLab/AdmixTools) installed in the first place,[admixr](https://bodkan.net/admixr/articles/tutorial.html#qpwave-and-qpadm)should be very easy.

### Related Posts:

- [Latest version of ADMIXTOOLS is
  up!](https://www.gnxp.com/WordPress/2016/06/13/latest-version-of-admixtools-is-up/) - [New version of
  ADMIXTOOLS](https://www.gnxp.com/WordPress/2015/03/11/new-version-of-admixtools/) - [Dienekes and
  ADMIXTOOLS](https://www.gnxp.com/WordPress/2012/10/08/dienekes-and-admixtools/) - [ADMIXTOOLS is
  out](https://www.gnxp.com/WordPress/2012/09/13/admixtools-is-out/) - [Lots and lots of genotype
  data!](https://www.gnxp.com/WordPress/2013/01/09/lots-and-lots-of-genotype-data/) - [Allen Ancient DNA Resource in PLINK
  format](https://www.gnxp.com/WordPress/2021/02/26/allen-ancient-dna-resource-in-plink-format/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F12%2F14%2Frunning-admixtools-through-r-admixr%2F&linkname=Running%20AdmixTools%20through%20R%20%E2%80%93%20admixr "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F12%2F14%2Frunning-admixtools-through-r-admixr%2F&linkname=Running%20AdmixTools%20through%20R%20%E2%80%93%20admixr "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2018%2F12%2F14%2Frunning-admixtools-through-r-admixr%2F&linkname=Running%20AdmixTools%20through%20R%20%E2%80%93%20admixr "Email")[](https://www.addtoany.com/share)
