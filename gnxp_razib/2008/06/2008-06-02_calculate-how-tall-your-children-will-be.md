+++
title = "Calculate how tall your"
full_title = "Calculate how tall your children will be"
date = "2008-06-02"
upstream_url = "https://www.gnxp.com/WordPress/2008/06/02/calculate-how-tall-your-children-will-be/"

+++
Source: [here](https://www.gnxp.com/WordPress/2008/06/02/calculate-how-tall-your-children-will-be/).

Calculate how tall your children will be

I realized today that my post about doing quantitative genetic back-of-the-envelopes was rather wordy. And, I have a hunch that those who “got it” already have an intuitive feel for what I’m talking about, so I thought perhaps the easiest way to get people to develop a better feel was to roll up the calculations into a small Javascript calculator. You can find it below the fold. The terms are defined in the earlier post, but I plugged in the default values (you can change them if you want). Obviously you enter in inches or centimeters depending on whether you’re normal or Canadian. Finally, if you are from another dimension where heritabilities are outside of the 0 to 1 interval and heights are negative then you will encounter problems. Remember the garbage-in-garbage-out principle; I did this in a hurry so no catching your errors and throwing back intelligible warnings.

  
\<!—-\>

input.calcNorm{ width:50px; clear:none;}  
.unitsCm { display:none;}  
.unitsIn { display:block; }  
span { clear:none;}  
div.widG{ padding-bottom:25px;}  
\#calcOutput {display:none;}

Inches  
Metric

Father  
Mother  
Mean for fathers  
Mean for mothers  
Standard Deviation

Heritability

for expected male offspring height

for expected female offspring height

68.27% male offspring will be between and  
68.27% female offspring will be between and  
95.45% male offspring will be between and  
95.45% female offspring will be between and

function init()  
{  
doc = window.document.form;  
}  
function unitConvert(units)  
{  
document.getElementById(“calcOutput”).style.display = “none”;  
doc = window.document.form;  
if (units == “Cm”)  
{  
doc.heightMother.value = Math.round(doc.heightMother.value/(0.393700787402)\*100)/100;  
doc.heightFather.value = Math.round(doc.heightFather.value/(0.393700787402)\*100)/100;  
doc.meanFather.value = Math.round(doc.meanFather.value/(0.393700787402)\*100)/100;  
doc.meanMother.value = Math.round(doc.meanMother.value/(0.393700787402)\*100)/100;  
doc.standardDeviation.value = Math.round(doc.standardDeviation.value/(0.393700787402)\*100)/100;  
}  
if (units == “In”)  
{  
doc.heightMother.value = Math.round(doc.heightMother.value\*(0.393700787402)\*100)/100;  
doc.heightFather.value = Math.round(doc.heightFather.value\*(0.393700787402)\*100)/100;  
doc.meanFather.value = Math.round(doc.meanFather.value\*(0.393700787402)\*100)/100;  
doc.meanMother.value = Math.round(doc.meanMother.value\*(0.393700787402)\*100)/100;  
doc.standardDeviation.value = Math.round(doc.standardDeviation.value\*(0.393700787402)\*100)/100;  
}  
}  
function calcHeights()  
{  
doc = window.document.form;  
// convert parents to std units  
fathDev = (1\*doc.heightFather.value – 1\*doc.meanFather.value)/doc.standardDeviation.value;  
mothDev = (1\*doc.heightMother.value – 1\*doc.meanMother.value)/doc.standardDeviation.value;  
midparent = (1\*fathDev + 1\*mothDev)/2;  
regparam = 1\*midparent\*(1-1\*doc.heritability.value);  
finalExpDev = 1\*midparent – 1\*regparam;  
convToUnitExp = 1\*finalExpDev\*doc.standardDeviation.value;  
doc.meanMale.value = Math.round((1\*convToUnitExp + 1\*doc.meanFather.value)\*100)/100  
doc.meanFemale.value = Math.round((1\*convToUnitExp + 1\*doc.meanMother.value)\*100)/100  
doc.onesiglowmale.value = Math.round((1\*doc.meanMale.value – 1\*doc.standardDeviation.value)\*100)/100  
doc.onesighighmale.value = Math.round((1\*doc.meanMale.value + 1\*doc.standardDeviation.value)\*100)/100  
doc.onesiglowfemale.value = Math.round((1\*doc.meanFemale.value – 1\*doc.standardDeviation.value)\*100)/100  
doc.onesighighfemale.value = Math.round((1\*doc.meanFemale.value + 1\*doc.standardDeviation.value)\*100)/100  
doc.twosiglowmale.value = Math.round((1\*doc.meanMale.value – 2\*doc.standardDeviation.value)\*100)/100  
doc.twosighighmale.value = Math.round((1\*doc.meanMale.value + 2\*doc.standardDeviation.value)\*100)/100  
doc.twosiglowfemale.value = Math.round((1\*doc.meanFemale.value – 2\*doc.standardDeviation.value)\*100)/100  
doc.twosighighfemale.value = Math.round((1\*doc.meanFemale.value + 2\*doc.standardDeviation.value)\*100)/100  
document.getElementById(“calcOutput”).style.display = “block”;  
}  
onLoad=init();

### Related Posts:

- [How tall will your children
  be?](https://www.gnxp.com/WordPress/2008/06/01/how-tall-will-your-children-be/) - [How tall will Megan McArdle & Peter
  Suderman's…](https://www.gnxp.com/WordPress/2009/07/06/how-tall-will-megan-mcardle-peter-sudermans-theoretical-offspring-be/) - [Religion & public attitudes: Europe vs.
  USA](https://www.gnxp.com/WordPress/2008/05/22/religion-public-attitudes-europe-vs-usa/) - [Stumpies are
  fugly?](https://www.gnxp.com/WordPress/2008/01/16/stumpies-are-fugly/) - [How much do siblings differ in
  height?](https://www.gnxp.com/WordPress/2011/12/24/how-much-do-siblings-differ-in-height/) - [Just pushing
  buttons](https://www.gnxp.com/WordPress/2010/08/24/just-pushing-buttons/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F06%2F02%2Fcalculate-how-tall-your-children-will-be%2F&linkname=Calculate%20how%20tall%20your%20children%20will%20be "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F06%2F02%2Fcalculate-how-tall-your-children-will-be%2F&linkname=Calculate%20how%20tall%20your%20children%20will%20be "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F06%2F02%2Fcalculate-how-tall-your-children-will-be%2F&linkname=Calculate%20how%20tall%20your%20children%20will%20be "Email")[](https://www.addtoany.com/share)
