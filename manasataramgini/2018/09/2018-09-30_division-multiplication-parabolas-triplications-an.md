+++
title = "Division-multiplication parabolas, triplications, and quadratic residues"
date = "2018-09-30"
upstream_url = "https://manasataramgini.wordpress.com/2018/09/30/division-multiplication-parabolas-triplications-and-quadratic-residues/"

+++
Source: [here](https://manasataramgini.wordpress.com/2018/09/30/division-multiplication-parabolas-triplications-and-quadratic-residues/).

**Introduction**

Many strands of our investigations on conic-generating integer
sequences, word fractals and cellular automaton models for pattern
formation came together in an unexpected manner while investigating a
simple integer sequence. While some of these connections have have been
known before, others are to our knowledge unreported. We present our
investigations in this regard below.

**The division-multiplication parabola sequence and
otherassociatedsequences**

Consider the following sequence
![f](https://s0.wp.com/latex.php?latex=f&bg=ffffff&fg=333333&s=0&c=20201002):

![f\[1\]=1](https://s0.wp.com/latex.php?latex=f%5B1%5D%3D1&bg=ffffff&fg=333333&s=0&c=20201002);
thereafter if,

![n \< f\[n-1\],
f\[n\]=\\left\\lfloor\\dfrac{f\[n-1\]}{n}\\right\\rfloor](https://s0.wp.com/latex.php?latex=n+%3C+f%5Bn-1%5D%2C+f%5Bn%5D%3D%5Cleft%5Clfloor%5Cdfrac%7Bf%5Bn-1%5D%7D%7Bn%7D%5Cright%5Crfloor&bg=ffffff&fg=333333&s=0&c=20201002);

else, ![n \>
f\[n-1\]](https://s0.wp.com/latex.php?latex=n+%3E+f%5Bn-1%5D&bg=ffffff&fg=333333&s=0&c=20201002)
and ![f\[n\]= n\\cdot
f\[n-1\]](https://s0.wp.com/latex.php?latex=f%5Bn%5D%3D+n%5Ccdot+f%5Bn-1%5D&bg=ffffff&fg=333333&s=0&c=20201002)

Following our initial investigation, a search of OEIS revealed that this
sequence was reported therein by Amarnath Murthy (A076039). The first
few terms of
![f](https://s0.wp.com/latex.php?latex=f&bg=ffffff&fg=333333&s=0&c=20201002)
are: 1, 2, 6, 1, 5, 30, 4, 32, 3, 30, 2, 24, 1, 14… A more detailed view
of
![f](https://s0.wp.com/latex.php?latex=f&bg=ffffff&fg=333333&s=0&c=20201002)
for increasing values of maximum
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
is shown in Figure 1.

[![Div_mult_parabola_Fig1](https://manasataramgini.files.wordpress.com/2018/09/div_mult_parabola_fig1.png?w=640)](https://manasataramgini.files.wordpress.com/2018/09/div_mult_parabola_fig1.png)Figure
1

An examination of the sequence and its plot in Figure 1 reveals the
following features:

1\) The action of division and multiplication by
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
takes place alternately. Hence, the sequence alternately bounces between
high and low values.

2\) However, on the larger scale it becomes apparent that the sequence
shows cycles, each with the same overall pattern but of increasing
magnitude (Figure 1).

3\) A closer examination of these cycles shows that within each cycle
the high values climb to a maximum and then fall off to reach a value
which is 1 more than the first low value of the next cycle. In contrast,
within each cycle the low values keep linearly decreasing until reaching
1. Then they start again with a new starting value in the next cycle.

4\) Each new cycle starts with a large jump in magnitude relative the
previous cycle. We can define the start of each new cycle objectively as
after when
![f\[n\]=n](https://s0.wp.com/latex.php?latex=f%5Bn%5D%3Dn&bg=ffffff&fg=333333&s=0&c=20201002).
We find that
![f\[n\]=n](https://s0.wp.com/latex.php?latex=f%5Bn%5D%3Dn&bg=ffffff&fg=333333&s=0&c=20201002)
when
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
takes the values: 1, 2, 5, 14, 41, 122, 365, 1094, 3281, 9842, 29525,
88574, 265721, 797162, 2391485, 7174454… This sequence
![m](https://s0.wp.com/latex.php?latex=m&bg=ffffff&fg=333333&s=0&c=20201002)
can be described by the formula:

![m\[n+1\]=\\dfrac{3^n+1}{2}](https://s0.wp.com/latex.php?latex=m%5Bn%2B1%5D%3D%5Cdfrac%7B3%5En%2B1%7D%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002),
where
![n=0,1,2,3...](https://s0.wp.com/latex.php?latex=n%3D0%2C1%2C2%2C3...&bg=ffffff&fg=333333&s=0&c=20201002)

We may also recursively define it as ![m\[n\]=3\\cdot
m\[n-1\]-1](https://s0.wp.com/latex.php?latex=m%5Bn%5D%3D3%5Ccdot+m%5Bn-1%5D-1&bg=ffffff&fg=333333&s=0&c=20201002),
from
![n=2](https://s0.wp.com/latex.php?latex=n%3D2&bg=ffffff&fg=333333&s=0&c=20201002)
onward after defining the first term
![m\[1\]=1](https://s0.wp.com/latex.php?latex=m%5B1%5D%3D1&bg=ffffff&fg=333333&s=0&c=20201002).
We will show below that this sequence
![m](https://s0.wp.com/latex.php?latex=m&bg=ffffff&fg=333333&s=0&c=20201002),
which appears in the context of the cycles of
![f](https://s0.wp.com/latex.php?latex=f&bg=ffffff&fg=333333&s=0&c=20201002),
also appears in several other seemingly unrelated mathematical
structures with interesting properties. It is also numerologically
interesting that the 7th cycle corresponds to the approximate length of
the earth year in days: 365.

5\) The determination of the sequence
![m](https://s0.wp.com/latex.php?latex=m&bg=ffffff&fg=333333&s=0&c=20201002)
allow us to trivially prove that the length of each cycle is:

![3^n=1, 3, 9, 27, 81,
243...](https://s0.wp.com/latex.php?latex=3%5En%3D1%2C+3%2C+9%2C+27%2C+81%2C+243...&bg=ffffff&fg=333333&s=0&c=20201002),
where ![n=0, 1, 2, 3, 4,
5...](https://s0.wp.com/latex.php?latex=n%3D0%2C+1%2C+2%2C+3%2C+4%2C+5...&bg=ffffff&fg=333333&s=0&c=20201002).
Thus, the expansion of the sequence is by the powers of 3.

6\) The maximum value of each cycle is reached at the midpoint of each
cycle and is attained when
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
is 1, 2, 3, 8, 21, 62, 183, 548, 1641, 4922, 14763, 44288, 132861,
398582, 1195743, 3587228… This novel sequence termed
![m_p](https://s0.wp.com/latex.php?latex=m_p&bg=ffffff&fg=333333&s=0&c=20201002)
can be described by the below formula:

![m_p\[n\]=\\left \\lfloor\\dfrac{m\[n\]+2}{2}\\right\\rfloor = \\left
\\lfloor\\dfrac{3^n+5}{4}\\right\\rfloor](https://s0.wp.com/latex.php?latex=m_p%5Bn%5D%3D%5Cleft+%5Clfloor%5Cdfrac%7Bm%5Bn%5D%2B2%7D%7B2%7D%5Cright%5Crfloor+%3D+%5Cleft+%5Clfloor%5Cdfrac%7B3%5En%2B5%7D%7B4%7D%5Cright%5Crfloor&bg=ffffff&fg=333333&s=0&c=20201002)

7\) The maximum value of each cycle is given by the novel sequence
![m_x](https://s0.wp.com/latex.php?latex=m_x&bg=ffffff&fg=333333&s=0&c=20201002):
1, 2, 6, 32, 231, 1922, 16836, 150152, 1347261, 12113042, 108980466,
980713472, 8826089091…
![m_x](https://s0.wp.com/latex.php?latex=m_x&bg=ffffff&fg=333333&s=0&c=20201002)
can be obtained by the formula:

![m_x= \\left \\lfloor\\dfrac{3^n+5}{4}\\right\\rfloor \\cdot \\left
\\lfloor \\dfrac{3^n+ 9}{8} \\right
\\rfloor](https://s0.wp.com/latex.php?latex=m_x%3D+%5Cleft+%5Clfloor%5Cdfrac%7B3%5En%2B5%7D%7B4%7D%5Cright%5Crfloor+%5Ccdot+%5Cleft+%5Clfloor+%5Cdfrac%7B3%5En%2B+9%7D%7B8%7D+%5Cright+%5Crfloor&bg=ffffff&fg=333333&s=0&c=20201002)
where ![n=0, 1, 2, 3,
...](https://s0.wp.com/latex.php?latex=n%3D0%2C+1%2C+2%2C+3%2C+...&bg=ffffff&fg=333333&s=0&c=20201002)

8\) Thus, the ratio
![\\tfrac{m_x}{m_p}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bm_x%7D%7Bm_p%7D&bg=ffffff&fg=333333&s=0&c=20201002)
is the sequence 1, 1, 2, 4, 11, 31, 92, 274, 821, 2461, 7382… defined by
the formula:

![\\dfrac{m_x}{m_p}\[n\]=\\left \\lfloor \\dfrac{3^n+ 9}{8} \\right
\\rfloor](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Bm_x%7D%7Bm_p%7D%5Bn%5D%3D%5Cleft+%5Clfloor+%5Cdfrac%7B3%5En%2B+9%7D%7B8%7D+%5Cright+%5Crfloor&bg=ffffff&fg=333333&s=0&c=20201002)

This sequence can also be generated from
![m_p](https://s0.wp.com/latex.php?latex=m_p&bg=ffffff&fg=333333&s=0&c=20201002)
by the formula:

![\\dfrac{m_x}{m_p}\[n\]=\\left \\lceil \\dfrac{m_p\[n\]}{2} \\right
\\rceil](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Bm_x%7D%7Bm_p%7D%5Bn%5D%3D%5Cleft+%5Clceil+%5Cdfrac%7Bm_p%5Bn%5D%7D%7B2%7D+%5Cright+%5Crceil&bg=ffffff&fg=333333&s=0&c=20201002)

We will see below that this sequence remarkably also emerges in another
area of higher arithmetic.

9\) Whereas the low values of
![f](https://s0.wp.com/latex.php?latex=f&bg=ffffff&fg=333333&s=0&c=20201002)
decrease linearly from their starting point in a cycle till they reach
1, the high values which they alternate with appear to be defined by
successively larger parabolic arcs (Figure 2). We determined these
parabolic arcs to have the general equation of the form:

![y= \\dfrac{x}{2} \\left(3
m\[n-1\]+1-x\\right)](https://s0.wp.com/latex.php?latex=y%3D+%5Cdfrac%7Bx%7D%7B2%7D+%5Cleft%283+m%5Bn-1%5D%2B1-x%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002)

Here,
![n=2,3,4...](https://s0.wp.com/latex.php?latex=n%3D2%2C3%2C4...&bg=ffffff&fg=333333&s=0&c=20201002)
and each successive arc spans the high values in the range ![x=
m\[n-1\]+1](https://s0.wp.com/latex.php?latex=x%3D+m%5Bn-1%5D%2B1&bg=ffffff&fg=333333&s=0&c=20201002)
to ![x=
m\[n\]](https://s0.wp.com/latex.php?latex=x%3D+m%5Bn%5D&bg=ffffff&fg=333333&s=0&c=20201002).
Hence, we term sequence
![f](https://s0.wp.com/latex.php?latex=f&bg=ffffff&fg=333333&s=0&c=20201002)
the division-multiplication-parabola sequence (DMPS). Thus, in a sense
our sequence is a “triessential” sequence with the number 3 being
fundamentally linked to it in many ways.

[![Div_mult_parabola_Fig2](https://manasataramgini.files.wordpress.com/2018/09/div_mult_parabola_fig2.png?w=640)](https://manasataramgini.files.wordpress.com/2018/09/div_mult_parabola_fig2.png)Figure
2.

The idea of this type of parabola first came to us over 23 years ago in
the context of trying to understand if natural selection might tend to
select oligo-functional proteins over both purely mono-functional ones
and those that perform a large number of distinct functions. The idea is
each new function gained by a protein results in an increased cost for
the other functions it performs; however, there could be a net fitness
gain from the compounding of the capacity to now perform multiple
functions. This would result in an optimal point after which the
performance in each function will deteriorate too much to have net
fitness gain despite the compounding. The result would be a parabolic
arc similar to that obtained in the DMPS.

In the remainder of this article we shall discuss the connections we
have found between the sequences associated with the DMPS and other
mathematical objects.

**The Mephisto-Waltz words**

A Mephisto-Waltz word is a word in a two-symbol alphabet that is
generated by a triplicative substitution system with the rules ![0
\\rightarrow 001, 1 \\rightarrow
110](https://s0.wp.com/latex.php?latex=0+%5Crightarrow+001%2C+1+%5Crightarrow+110&bg=ffffff&fg=333333&s=0&c=20201002).
The growth is initiated with
![MW\[1\]=0](https://s0.wp.com/latex.php?latex=MW%5B1%5D%3D0&bg=ffffff&fg=333333&s=0&c=20201002).
Thus, we get the following words:

![0; 001; 001001110;
001001110001001110110110001](https://s0.wp.com/latex.php?latex=0%3B+001%3B+001001110%3B+001001110001001110110110001&bg=ffffff&fg=333333&s=0&c=20201002)
and so on. This can be graphically represented as the triplicative
growth of circular cells with differentiation (Figure 3).

[![Div_mult_parabola_Fig3_MW](https://manasataramgini.files.wordpress.com/2018/09/div_mult_parabola_fig3_mw-e1538283343328.png?w=640)](https://manasataramgini.files.wordpress.com/2018/09/div_mult_parabola_fig3_mw-e1538283343328.png)Figure
3.

The Mephisto-Waltz words can also be used to generate another kind of
pattern in the form of a square using Cantor’s pairing function.
Cantor’s pairing function maps every ordered pair of non-negative
integers
![(j,k)](https://s0.wp.com/latex.php?latex=%28j%2Ck%29&bg=ffffff&fg=333333&s=0&c=20201002)
to a single unique integer
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002):

![n=j+\\dfrac{(j+k)(j+k+1)}{2}](https://s0.wp.com/latex.php?latex=n%3Dj%2B%5Cdfrac%7B%28j%2Bk%29%28j%2Bk%2B1%29%7D%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002)

Now, if we pair every ‘letter’ in the Mephisto-Waltz word with every
other ‘letter’ in it with the above Cantor function then get the square
pattern shown in Figure 4. Since there are four distinct pairings
possible between 0 and 1, i.e. (0,0), (0,1), (1,0) and (1,1), under the
the Cantor function each cell of the ensuing square matrix can have one
of four values, each shown in a different color.

[![Div_mult_parabola_Fig4_MW_Cantor](https://manasataramgini.files.wordpress.com/2018/09/div_mult_parabola_fig4_mw_cantor.png?w=650&h=650)](https://manasataramgini.files.wordpress.com/2018/09/div_mult_parabola_fig4_mw_cantor.png)Figure
4.

We can also apply a form of “epigenetic” information to the genetic
encoding of a folding instruction in the two symbol Mephisto-Waltz word.
It goes thus: We start out drawing a line segment in a certain
direction. If we encounter a
![0](https://s0.wp.com/latex.php?latex=0&bg=ffffff&fg=333333&s=0&c=20201002)
we draw a line segment of fixed length in the same direction as we are
currently oriented in. If we encounter
![1](https://s0.wp.com/latex.php?latex=1&bg=ffffff&fg=333333&s=0&c=20201002)
and it is in an even position (epigenetic information) then we turn by
an angle of
![\\tfrac{\\pi}{2}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7B%5Cpi%7D%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002)
and draw a line segment of the same fixed length in the new orientation.
If we encounter
![1](https://s0.wp.com/latex.php?latex=1&bg=ffffff&fg=333333&s=0&c=20201002)
in an odd position in then we do the same but turning by
![-\\tfrac{\\pi}{2}](https://s0.wp.com/latex.php?latex=-%5Ctfrac%7B%5Cpi%7D%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002).
This results in the fractal “wave” illustrated in Figure 5.

[![Div_mult_parabola_Fig5_MW_fractal](https://manasataramgini.files.wordpress.com/2018/09/div_mult_parabola_fig5_mw_fractal.png?w=640)](https://manasataramgini.files.wordpress.com/2018/09/div_mult_parabola_fig5_mw_fractal.png)Figure
5.

Mephisto-Waltz words show an intimate connection to sequences emerging
from the DMPS: First, given that they have a triplicative growth pattern
their length grows as
![3^n](https://s0.wp.com/latex.php?latex=3%5En&bg=ffffff&fg=333333&s=0&c=20201002),
which is the same as the length of the cycles of the DMPS. Second, the
numbers of zeros in the Mephisto-Waltz words grow as the sequence ![m=1,
2, 5, 14, 41, 122,
365](https://s0.wp.com/latex.php?latex=m%3D1%2C+2%2C+5%2C+14%2C+41%2C+122%2C+365&bg=ffffff&fg=333333&s=0&c=20201002),
which defines the points of transition to the next cycle of the DMPS.
The numbers of 1s in these words grow as
![m-1](https://s0.wp.com/latex.php?latex=m-1&bg=ffffff&fg=333333&s=0&c=20201002).
Thus in a sense the sequence
![m](https://s0.wp.com/latex.php?latex=m&bg=ffffff&fg=333333&s=0&c=20201002)
captures the ‘median’ growth of these words.

**Standard order words in a 3-symbol alphabet**

Consider an alphabet with 3 symbols. We can denote those 3 alphabets by
the numbers 1, 2, 3. Then we write the following words in the this
alphabet:

1, 12, 12123, 12123123123123, 12123123123123123123123123123123123123123
…

One observes that the process goes thus: we first write 1, then 12,
which form the first two words. Then from the 3rd word onward we add
![3^n](https://s0.wp.com/latex.php?latex=3%5En&bg=ffffff&fg=333333&s=0&c=20201002)
letters (where ![n=1, 2,
3,...](https://s0.wp.com/latex.php?latex=n%3D1%2C+2%2C+3%2C...&bg=ffffff&fg=333333&s=0&c=20201002))
in the form of repeats of 123. Thus, the length of these words grows as
1, 2, 5, 14, 41, 122… which is the same as the sequence
![m](https://s0.wp.com/latex.php?latex=m&bg=ffffff&fg=333333&s=0&c=20201002)
defining the transitions to the next cycle in the DMPS.

Standard order means that a later symbol of the alphabet cannot appear
in the word unless the symbol earlier to it has already appeared in the
word. Thus, 2 cannot appear in the word unless 1 has already appeared.
Likewise, 3 cannot appear in a word unless 1 and 2 have already
appeared. Thus, if traverse through the above-generated 3-symbol words
from the one to the next we can create
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)-letter
words with a maximum of 3-symbols in standard order:

For 1-letter words we can only have: 1  
For 2-letter words we can only get: 11, 12  
For 3-letter words we get: 111, 112, 121, 122, 123  
For 4-letter words we get: 1111, 1112, 1121, 1122, 1123, 1211, 1212,
1213, 1221, 1222, 1223, 1231, 1232, 1233  
So on (OEIS: A278985). Thus, the number of
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)-letter
standard order words we can get in a 3-symbol alphabet is the same as
the sequence ![m=1, 2, 5, 14, 41,
122...](https://s0.wp.com/latex.php?latex=m%3D1%2C+2%2C+5%2C+14%2C+41%2C+122...&bg=ffffff&fg=333333&s=0&c=20201002).

**The number of quadratic residues of
![3^n](https://s0.wp.com/latex.php?latex=3%5En&bg=ffffff&fg=333333&s=0&c=20201002)**

Quadratic residues were extensively studied by Carl Gauss in his
celebrated *Disquisitiones Arithmeticae*. The quadratic residues for a
number
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
are determined by considering all ![0 \\le a \<
n](https://s0.wp.com/latex.php?latex=0+%5Cle+a+%3C+n&bg=ffffff&fg=333333&s=0&c=20201002).
Then ![q= a^2 \\mod
n](https://s0.wp.com/latex.php?latex=q%3D+a%5E2+%5Cmod+n&bg=ffffff&fg=333333&s=0&c=20201002).
Further, given that ![\\left((n-a)^2 \\right) \\mod n= a^2 \\mod
n](https://s0.wp.com/latex.php?latex=%5Cleft%28%28n-a%29%5E2+%5Cright%29+%5Cmod+n%3D+a%5E2+%5Cmod+n&bg=ffffff&fg=333333&s=0&c=20201002),
we only need to compute the residues for ![0 \\le a \< \\left \\lfloor
\\dfrac{n}{2} \\right
\\rfloor](https://s0.wp.com/latex.php?latex=0+%5Cle+a+%3C+%5Cleft+%5Clfloor+%5Cdfrac%7Bn%7D%7B2%7D+%5Cright+%5Crfloor&bg=ffffff&fg=333333&s=0&c=20201002).

For example, if we take
![n=9](https://s0.wp.com/latex.php?latex=n%3D9&bg=ffffff&fg=333333&s=0&c=20201002),
then we have the residues: ![0=(0^2) \\mod 9; 1=(1^2) \\mod 9; 4= (2^2)
\\mod 9; 0=(3^2) \\mod 9; 7= (4^2) \\mod
9](https://s0.wp.com/latex.php?latex=0%3D%280%5E2%29+%5Cmod+9%3B+1%3D%281%5E2%29+%5Cmod+9%3B+4%3D+%282%5E2%29+%5Cmod+9%3B+0%3D%283%5E2%29+%5Cmod+9%3B+7%3D+%284%5E2%29+%5Cmod+9&bg=ffffff&fg=333333&s=0&c=20201002).
Thus, for
![n=9](https://s0.wp.com/latex.php?latex=n%3D9&bg=ffffff&fg=333333&s=0&c=20201002),
the numbers 0, 1, 4, 7 are its quadratic residues. We observe that of
the numbers from 0 to (9-1=8) the following are not represented: 2, 3,
5, 6, 8. These are the quadratic non-residues of 9.

Let us now consider the quadratic residues of the powers of 3 and count
how many of them are there for each power:

![3^0: 0; n=1 \\\\ 3^1: 0, 1; n=2\\\\ 3^2: 0, 1, 4, 7; n=4\\\\ 3^3: 0,
1, 4, 7, 9, 10, 13, 16, 19, 22, 25; n=11\\\\ 3^4: 0, 1, 4, 7, 9, 10, 13,
16, 19, 22, 25, 28, 31, 34, 36, 37, 40, 43, 46, 49, 52, 55, 58, 61, 63,
64, 67, 70, 73, 76, 79;
n=31](https://s0.wp.com/latex.php?latex=3%5E0%3A+0%3B+n%3D1+%5C%5C+3%5E1%3A+0%2C+1%3B+n%3D2%5C%5C+3%5E2%3A+0%2C+1%2C+4%2C+7%3B+n%3D4%5C%5C+3%5E3%3A+0%2C+1%2C+4%2C+7%2C+9%2C+10%2C+13%2C+16%2C+19%2C+22%2C+25%3B+n%3D11%5C%5C+3%5E4%3A+0%2C+1%2C+4%2C+7%2C+9%2C+10%2C+13%2C+16%2C+19%2C+22%2C+25%2C+28%2C+31%2C+34%2C+36%2C+37%2C+40%2C+43%2C+46%2C+49%2C+52%2C+55%2C+58%2C+61%2C+63%2C+64%2C+67%2C+70%2C+73%2C+76%2C+79%3B+n%3D31&bg=ffffff&fg=333333&s=0&c=20201002)  
So on…

We see than the number of quadratic residues for the powers of 3 specify
the sequence ![\\tfrac{m_x}{m_p}
\[n\]](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bm_x%7D%7Bm_p%7D+%5Bn%5D&bg=ffffff&fg=333333&s=0&c=20201002)
starting from the second term. This is the ratio of the maximum value to
the midpoint of the cycle of the DMPS where it is attained.

We also noted that a sequence closely related to ![\\tfrac{m_x}{m_p}
\[n\]](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bm_x%7D%7Bm_p%7D+%5Bn%5D&bg=ffffff&fg=333333&s=0&c=20201002)
turns up in the graph theory. While ![\\tfrac{m_x}{m_p}\[n\]=\\left
\\lceil \\tfrac{m_p\[n\]}{2} \\right
\\rceil](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bm_x%7D%7Bm_p%7D%5Bn%5D%3D%5Cleft+%5Clceil+%5Ctfrac%7Bm_p%5Bn%5D%7D%7B2%7D+%5Cright+%5Crceil&bg=ffffff&fg=333333&s=0&c=20201002)
this sequence is defined as:

![\\rho'\[n\]=\\left \\lfloor \\dfrac{m_p\[n\]}{2} \\right
\\rfloor](https://s0.wp.com/latex.php?latex=%5Crho%27%5Bn%5D%3D%5Cleft+%5Clfloor+%5Cdfrac%7Bm_p%5Bn%5D%7D%7B2%7D+%5Cright+%5Crfloor&bg=ffffff&fg=333333&s=0&c=20201002)

In graph theory a circuit is defined as graph in which by passing
through adjacent vertices one can reach the same vertex. Now, if we
specify that adjacent vertices should be colored using different colors,
then we need a minimum of 4 colors to color all vertices of any circuit
graph. The number of distinct configurations that a circuit graph with
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
vertices can be colored with 4 colors was shown to be
![\\rho'\[n\]](https://s0.wp.com/latex.php?latex=%5Crho%27%5Bn%5D&bg=ffffff&fg=333333&s=0&c=20201002)
by Bernhart (OEIS: A006342). This sequence goes as: 0, 1, 1, 4, 10, 31,
91, 274, 820, 2461, 7381, 22144, 66430, 199291, 597871, 1793614 … One
can see that it differs from ![\\tfrac{m_x}{m_p}
\[n\]](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bm_x%7D%7Bm_p%7D+%5Bn%5D&bg=ffffff&fg=333333&s=0&c=20201002)
by 1 at every odd
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002),
i.e.
![n=2k+1](https://s0.wp.com/latex.php?latex=n%3D2k%2B1&bg=ffffff&fg=333333&s=0&c=20201002).

Thus, rather notably, a simple arithmetic procedure generates the DMPS,
with associated sequences bearing connections to other seemingly
unrelated mathematical objects pointing to the pervasiveness of certain
combinatoric numbers.
