+++
title = "BhāskaraII’s polygons"
full_title = "BhāskaraII’s polygons and an algebraic approximation for sines of pi by x"
date = "2022-12-28"
upstream_url = "https://manasataramgini.wordpress.com/2022/12/28/bhaskara-iis-polygons-and-an-algebraic-approximation-for-sines-of-pi-by-x/"

+++
Source: [here](https://manasataramgini.wordpress.com/2022/12/28/bhaskara-iis-polygons-and-an-algebraic-approximation-for-sines-of-pi-by-x/).

Bhāskara-II’s polygons and an algebraic approximation for sines of pi by x

Unlike the Greeks, the Hindus were not particularly obsessed with constructions involving just a compass and a straightedge. Nevertheless, their pre-modern architecture and yantra-s from the tāntrika tradition indicate that they routinely constructed various regular polygons inscribed in circles. Of course, the common ones, namely the equilateral triangle, square, hexagon, and octagon are trivial, and the earliest preserved geometry of the Hindus is sufficient to construct these. The pentagon and its double the decagon are a bit more involved but are still constructible by the Greek compass and straightedge method; however, few have looked into how the Hindus might have constructed it. These aside, we do have multiple examples of yantra-s with heptagons and nonagons. A particularly striking example is the wide use of the nonagon in yantra-s (likely related to the early Śrīkula tradition of 9 yoginī-s and the division of the Vyomavyāpin mantra of the saiddhāntika-s) found at the Marundīśvara temple near Chennai. The kaula tradition of the Kubjikā-mata-tantra has a sūtra that mentions a yantra with multiple regular polygons relating to pacifying the seizure by Ṣaṣṭhī and others (trikoṇaṃ navakoṇaṃ ca ṣaṭkoṇaṃ maṇḍalākṛtiḥ \|). The heptagon and the nonagon cannot be constructed using just a compass and a straightedge. To construct them precisely, one would require a means of accurately drawing conics (other than circles and straight lines) of particular specifications. While Archimedes invented a machine to draw ellipses, and examples of ellipses are occasionally encountered in early Hindu architecture, the technology for the easy generation of desired conics was unlikely to have been widely available to premodern architects. Hence, the Hindus should have constructed their regular polygons, including heptagons and nonagons through other means.

![Polygon_Sine](https://manasataramgini.files.wordpress.com/2022/12/polygon_sine.png?w=436&h=515)Figure 1.

It is easy to see (Figure 1) that for a circle of diameter ![d](https://s0.wp.com/latex.php?latex=d&bg=ffffff&fg=333333&s=0&c=20201002) the side ![s](https://s0.wp.com/latex.php?latex=s&bg=ffffff&fg=333333&s=0&c=20201002) of an inscribed regular polygon of ![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002) sides is ![s=d\sin\left(\tfrac{\pi}{n}\right)](https://s0.wp.com/latex.php?latex=s%3Dd%5Csin%5Cleft%28%5Ctfrac%7B%5Cpi%7D%7Bn%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002). Thus, if one does not insist on a compass and straightedge construction, one can easily draw any polygon as long as one has a sine table. The Hindus have had a long history of generating sine tables as well as algebraic functions that approximate the sine function to varying degrees of accuracy. Thus, one would expect that this was the most likely route they took. This still leaves us with the question of how exactly they did it in practice. A likely answer for this comes from Bhāskara-II’s Līlāvatī though this knowledge appears to have been lost in some parts of India in the late medieval period.

In Līlāvatī 206-209, Bhāskara gives a table for the sides of the inscribed polygons in three anuṣtubh-s (see below) followed by a numerical example (L 209). We have resolved the saṃdhi with a + for ease of reading the numbers:

tri-dvyaṅkāgni-nabhaś-chandrais tribāṇāṣṭayugāṣṭabhiḥ \|  
vedāgni-bāṇa-khāśvaiś ca kha-khābhrābhra-rasaiḥ kramāt \|\| L 206

tri+dvi +aṅka +agni +nabhaś +candrais (103923)  
tri +bāṇa +aṣṭa +yuga +aṣṭabhiḥ (84853) \|  
veda +agni +bāṇa +kha +aśvaiś (70534)  
ca kha +kha +abhra +abhra +rasaiḥ (60000) kramāt \|\|

bāṇeṣu-nakha-bāṇaiś ca dvi-dvi-nandeṣu sāgaraiḥ \|  
ku-rāma-daśa-vedaiś ca vṛtta-vyāse samāhate \|\| L 207

bāṇa +iṣu +nakha +bāṇaiś (52055) ca  
dvi +dvi +nanda +iṣu +sāgaraiḥ (45922)  
ku +rāma +daśa +vedaiś ca (41031)

kha-kha-khābhrārka saṃbhakte labhyante kramaśo bhujā \|  
vṛttāntar tryasra-pūrvāṇāṃ navāsrāntam pṛthak pṛthak \|\| L 208

vṛtta-vyāse samāhate kha +kha +kha +abhra +arka (120000) saṃbhakte labhyante kramaśo bhujā  
vṛtta-antar tri +asra-pūrvāṇām nava +asra-antam pṛthak pṛthak

Essentially, the above means that one should multiply the diameter of the circle with the numbers specified in the above table in verse form and divide them by 120000. This gives, in order, the sides of the inscribed regular polygons from a triangle to a nonagon. Thus, the ratios of these numbers provide rational approximations for ![\sin\left(\tfrac{\pi}{n}\right)](https://s0.wp.com/latex.php?latex=%5Csin%5Cleft%28%5Ctfrac%7B%5Cpi%7D%7Bn%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002) for ![n=3..9](https://s0.wp.com/latex.php?latex=n%3D3..9&bg=ffffff&fg=333333&s=0&c=20201002). We compare these to the actual values in the below table:

![sine_Table1](https://manasataramgini.files.wordpress.com/2022/12/sine_table1.png?w=608&h=529)

These rational approximations provided by Bhāskara are best for a triangle, square, pentagon, hexagon and octagon. These are the angles for which he derives closed forms in his Jyotpatti (On the generation of sines) and correspond to the constructible polygons of the Greek tradition. The sines of the heptagonal and nonagonal angles which have no closed forms were obtained using serial interpolations or a sine-approximating function.

In terms of the latter, Bhāskara specifies a formula for the length of a cord corresponding to an arc in a Vasantalikā verse that can be used to obtain an algebraic function approximating ![\sin\left(\tfrac{\pi}{x}\right)](https://s0.wp.com/latex.php?latex=%5Csin%5Cleft%28%5Ctfrac%7B%5Cpi%7D%7Bx%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002):  
cāpona-nighna-paridhiḥ pratham-āhvayaḥ  
syāt pañcāhataḥ paridhi-varga-caturtha-bhāgaḥ \|  
ādyonitena khalu tena bhajec catur-ghna  
vyāsāhatam prathamam āptam iha jyakā syāt \|\| L 210

cāpa +ūna-nighna-paridhiḥ prathama +āhvayaḥ  
syāt pañca +āhatas paridhi-varga-caturtha-bhāgaḥ \|  
ādya +ūnitena khalu tena bhajet +catur +ghna-  
vyāsa +āhatam prathamam āptam iha jyakā syāt \|\|

The circumference is reduced by the arc and multiplied by the arc: this is called the prathama.  
One-fourth of the circumference squared is multiplied by 5  
This is then reduced by the prathamā. The prathamā multiplied by 4  
and the diameter should be divided by the above result. The fraction thus obtained is the chord.

Let the diameter of the circle be ![d](https://s0.wp.com/latex.php?latex=d&bg=ffffff&fg=333333&s=0&c=20201002), its circumference ![c](https://s0.wp.com/latex.php?latex=c&bg=ffffff&fg=333333&s=0&c=20201002), the length of the given arc ![a](https://s0.wp.com/latex.php?latex=a&bg=ffffff&fg=333333&s=0&c=20201002) and ![y](https://s0.wp.com/latex.php?latex=y&bg=ffffff&fg=333333&s=0&c=20201002) its chord. Then the above can be written in modern notation as:

![y= \dfrac{4da(c-a)}{\frac{5c^2}{4}-a(c-a)} = \dfrac{16da(c-a)}{5c^2-4a(c-a)}](https://s0.wp.com/latex.php?latex=y%3D+%5Cdfrac%7B4da%28c-a%29%7D%7B%5Cfrac%7B5c%5E2%7D%7B4%7D-a%28c-a%29%7D+%3D+%5Cdfrac%7B16da%28c-a%29%7D%7B5c%5E2-4a%28c-a%29%7D&bg=ffffff&fg=333333&s=0&c=20201002)

Now, the arc can be written as the ![x^{\mathrm{th}}](https://s0.wp.com/latex.php?latex=x%5E%7B%5Cmathrm%7Bth%7D%7D&bg=ffffff&fg=333333&s=0&c=20201002) fraction of the circumference, ![\therefore a=\tfrac{c}{x}](https://s0.wp.com/latex.php?latex=%5Ctherefore+a%3D%5Ctfrac%7Bc%7D%7Bx%7D&bg=ffffff&fg=333333&s=0&c=20201002). By plugging this into the above equation, we get:

![y= \dfrac{16d\tfrac{c}{x}(c-\tfrac{c}{x})}{5c^2-4\tfrac{c}{x}(c-\tfrac{c}{x})}](https://s0.wp.com/latex.php?latex=y%3D+%5Cdfrac%7B16d%5Ctfrac%7Bc%7D%7Bx%7D%28c-%5Ctfrac%7Bc%7D%7Bx%7D%29%7D%7B5c%5E2-4%5Ctfrac%7Bc%7D%7Bx%7D%28c-%5Ctfrac%7Bc%7D%7Bx%7D%29%7D&bg=ffffff&fg=333333&s=0&c=20201002)

This allows us to eliminate ![c](https://s0.wp.com/latex.php?latex=c&bg=ffffff&fg=333333&s=0&c=20201002) and write

![y=\dfrac{16d\left(x-1\right)}{5x^{2}-4\left(x-1\right)}](https://s0.wp.com/latex.php?latex=y%3D%5Cdfrac%7B16d%5Cleft%28x-1%5Cright%29%7D%7B5x%5E%7B2%7D-4%5Cleft%28x-1%5Cright%29%7D&bg=ffffff&fg=333333&s=0&c=20201002)

Thus, we get an algebraic function approximating ![y=\sin\left(\tfrac{\pi}{x}\right)](https://s0.wp.com/latex.php?latex=y%3D%5Csin%5Cleft%28%5Ctfrac%7B%5Cpi%7D%7Bx%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002):

![y=\dfrac{16\left(x-1\right)}{5x^{2}-4\left(x-1\right)}](https://s0.wp.com/latex.php?latex=y%3D%5Cdfrac%7B16%5Cleft%28x-1%5Cright%29%7D%7B5x%5E%7B2%7D-4%5Cleft%28x-1%5Cright%29%7D&bg=ffffff&fg=333333&s=0&c=20201002)

[![Bhaskara_sinpibyx](https://manasataramgini.files.wordpress.com/2022/12/bhaskara_sinpibyx.png?w=640)](https://www.desmos.com/calculator/5fuqv86r2b)  
Figure 2.

In the below table we show the values of the polygon sines for ![n=3..9](https://s0.wp.com/latex.php?latex=n%3D3..9&bg=ffffff&fg=333333&s=0&c=20201002) generated by this formula and compare them with the earlier table provided by Bhāskara and the actual value:

![sine_Table2](https://manasataramgini.files.wordpress.com/2022/12/sine_table2.png?w=610&h=358)

We can see that the values from this function are more approximate than those provided by the table. Thus, it is clear that Bhāskara did not use this algebraic function to generate his table. However, the fact that he provides this formula after the table indicates that he meant this as an alternative method to get rational approximations for the polygonal sines. Such a method too could have been readily used by artists/artisans in their polygonal constructions in architecture and yantra preparation.
