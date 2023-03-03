+++
title = "How White are you?"
full_title = "How White are you?"
date = "2008-09-07"
upstream_url = "https://www.gnxp.com/WordPress/2008/09/07/how-white-are-you-stuff-white-people-like/"

+++
Source: [here](https://www.gnxp.com/WordPress/2008/09/07/how-white-are-you-stuff-white-people-like/).

How White are you? (Stuff White People Like)

A friend of mine emailed me that he scored a 21 out of 107 on the [full list of Stuff White People Like](http://stuffwhitepeoplelike.com/full-list-of-stuff-white-people-like/). I thought it was a little tedious to count, so I wrote up a small script which counts it up for you via the checks you make. Below the fold….

.wholeRapper { padding:10px; }  
.whiteThings { padding:5px; padding-right:10px; padding-bottom: 10px; float:left; clear: none;}  
\#outPutBox { padding:20px; clear:both; font-size:36px; font-style:italic;}  
\#totalWhite {background-color:#CCCCCC; width:400px; padding:20px;}

function toteUp()  
{  
var totNum = 0;  
var formElementsNum = document.form.length;  
a = 0;  
while ( a \< formElementsNum )  
{  
if (document.form.elements\[a\].checked == true)  
{  
totNum++;  
} // end if  
a++;  
}// end while  
document.getElementById("totalWhite").innerHTML = totNum + " out of 107 Stuffs White People Like  
“;  
imageChange(totNum);  
}// end function  
function imageChange(totNum)  
{  
if (totNum == 107)  
{  
document\[‘headShot’\].src=’http://scienceblogs.com/gnxp/107.jpg’;  
window.open(‘http://www.sierraclub.org/’,’youraresowhite’,’width=600,height=600′);  
}  
else if (totNum \> 99)  
{  
document\[‘headShot’\].src=’http://scienceblogs.com/gnxp/100.jpg’;  
}  
else if (totNum \> 79)  
{  
document\[‘headShot’\].src=’http://scienceblogs.com/gnxp/80.jpg’;  
}  
else if (totNum \> 59)  
{  
document\[‘headShot’\].src=’http://scienceblogs.com/gnxp/60.jpg’;  
}  
else if (totNum \> 39)  
{  
document\[‘headShot’\].src=’http://scienceblogs.com/gnxp/40.jpg’;  
}  
else if (totNum \> 19)  
{  
document\[‘headShot’\].src=’http://scienceblogs.com/gnxp/20.jpg’;  
}  
else  
{  
document\[‘headShot’\].src=’http://scienceblogs.com/gnxp/0.jpg’;  
}  
}// end function

![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/0.jpg?w=640)![](https://i0.wp.com/blogs.discovermagazine.com/gnxp/files/0.jpg?w=640)

\#107 Self Aware Hip Hop References  
\#106 Facebook  
\#105 Unpaid Internships  
\#104 Girls with Bangs  
\#103 Sweaters  
\#102 Children’s Games as Adults  
\#101 Being Offended  
\#100 Bumper Stickers  
\#99 Grammar  
\#98 The Ivy League  
\#97 Scarves  
\#96 New Balance Shoes  
\#95 Rugby  
\#94 Free Healthcare  
\#93 Music Piracy  
\#92 Book Deals  
\#91 San Francisco  
\#90 Dinner Parties  
\#89 St. Patrick’s Day  
\#88 Having Gay Friends  
\#87 Outdoor Performance Clothes  
\#86 Shorts  
\#85 The Wire  
\#84 T-Shirts  
\#83 Bad Memories of High School  
\#82 Hating Corporations  
\#81 Graduate School  
\#80 The Idea of Soccer  
\#79 Modern Furniture  
\#78 Multilingual Children  
\#77 Musical Comedy  
\#76 Bottles of Water  
\#75 Threatening to Move to Canada  
\#74 Oscar Parties  
\#73 Gentrification  
\#72 Study Abroad  
\#71 Being the only white person around  
\#70 Difficult Breakups  
\#69 Mos Def  
\#68 Michel Gondry  
\#67 Standing Still at Concerts  
\#66 Divorce  
\#65 Co-Ed Sports  
\#64 Recycling  
\#63 Expensive Sandwiches  
\#62 Knowing What’s Best for Poor People  
\#61 Bicycles  
\#60 Toyota Prius  
\#59 Natural Medicine  
\#58 Japan  
\#57 Juno  
\#56 Lawyers  
\#55 Apologies  
\#54 Kitchen Gadgets  
\#53 Dogs  
\#52 Sarah Silverman  
\#51 Living by the Water  
\#50 Irony  
\#49 Vintage  
\#48 Whole Foods and Grocery Co-ops  
\#47 Arts Degrees  
\#46 The Sunday New York Times  
\#45 Asian Fusion Food  
\#44 Public Radio  
\#43 Plays  
\#42 Sushi  
\#41 Indie Music  
\#40 Apple Products  
\#39 Netflix  
\#38 Arrested Development  
\#37 Renovations  
\#36 Breakfast Places  
\#35 The Daily Show/Colbert Report  
\#34 Architecture  
\#33 Marijuana  
\#32 Vegan/Vegetarianism  
\#31 Snowboarding  
\#30 Wrigley Field  
\#29 80s Night  
\#28 Not having a TV  
\#27 Marathons  
\#26 Manhattan (now Brooklyn too!)  
\#25 David Sedaris  
\#24 Wine  
\#23 Microbreweries  
\#22 Having Two Last Names  
\#21 Writers Workshops  
\#20 Being an expert on YOUR culture  
\#19 Traveling  
\#18 Awareness  
\#17 Hating their Parents  
\#16 Gifted Children  
\#15 Yoga  
\#14 Having Black Friends  
\#13 Tea  
\#12 Non-Profit Organizations  
\#11 Asian Girls  
\#10 Wes Anderson Movies  
\#9 Making you feel bad about not going outside  
\#8 Barack Obama  
\#7 Diversity  
\#6 Organic Food  
\#5 Farmer’s Markets  
\#4 Assists  
\#3 Film Festivals  
\#2 Religions their parents don’t belong to  
\#1 Coffee

onLoad = toteUp();

### Related Posts:

- [Sign up for A Week of
  Science](https://www.gnxp.com/WordPress/2007/01/18/sign-up-for-a-week-of-science/) - [Sign up for A Week of
  Science](https://www.gnxp.com/WordPress/2007/01/19/sign-up-for-a-week-of-science-2/) - [Calculate how tall your children will
  be](https://www.gnxp.com/WordPress/2008/06/02/calculate-how-tall-your-children-will-be/) - [Get your White
  on](https://www.gnxp.com/WordPress/2008/09/07/get-your-white-on/) - [How did you find this
  weblog?](https://www.gnxp.com/WordPress/2006/07/11/how-did-you-find-this-weblog/) - [Indian Y chromosomes in
  Thailand](https://www.gnxp.com/WordPress/2020/01/21/indian-y-chromosomes-in-thailand/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F09%2F07%2Fhow-white-are-you-stuff-white-people-like%2F&linkname=How%20White%20are%20you%3F%20%28Stuff%20White%20People%20Like%29 "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F09%2F07%2Fhow-white-are-you-stuff-white-people-like%2F&linkname=How%20White%20are%20you%3F%20%28Stuff%20White%20People%20Like%29 "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F09%2F07%2Fhow-white-are-you-stuff-white-people-like%2F&linkname=How%20White%20are%20you%3F%20%28Stuff%20White%20People%20Like%29 "Email")[](https://www.addtoany.com/share)
