+++
title = "Relationships between"
full_title = "Relationships between incircles of the “equilateral triangles in a square” system"
date = "2021-12-20"
upstream_url = "https://manasataramgini.wordpress.com/2021/12/20/relationships-between-incircles-of-the-equilateral-triangles-in-a-square-system/"

+++
Source: [here](https://manasataramgini.wordpress.com/2021/12/20/relationships-between-incircles-of-the-equilateral-triangles-in-a-square-system/).

Relationships between incircles of the “equilateral triangles in a square” system

This note relates to geometric relationships that may be likened to the Japanese temple-tablet problems. The inspiration for discovering and exploring it came from an origami construction presented by the pioneer in that field, Sundara Rao of Kumbhaghoṇa, in the late 1800s. Given a square piece of paper, how does one fold it into an equilateral triangle? The construction which Rao gave was that of an equilateral triangle with sides equal to that of the starting square and sharing one side with it (Figure 1). Based on Figure 1, it is easy to see how that might be achieved. When we first folded this in our youth, we realized that it is not the largest equilateral triangle that can be placed inside a square. However, examining the origami construction for the above, we realized that it also gave us an easy origami construction for the largest equilateral triangle that can be inscribed in a square (the blue triangle in Figure 1). That construction should be self-evident once the first equilateral triangle sharing a side with the square is in place). These two equilateral triangles and the square result in a configuration of 7 other triangles (Figure 1).

The below study concerns the relationship between the incircles of these 7 triangles ![(c_1, c_2, \\cdots, c_7)](https://s0.wp.com/latex.php?latex=%28c_1%2C+c_2%2C+%5Ccdots%2C+c_7%29&bg=ffffff&fg=333333&s=0&c=20201002) and two additional incircles, namely that of the starting square
![c_s](https://s0.wp.com/latex.php?latex=c_s&bg=ffffff&fg=333333&s=0&c=20201002)
and the Raoian triangle constructed from it
![c_t](https://s0.wp.com/latex.php?latex=c_t&bg=ffffff&fg=333333&s=0&c=20201002).
Their radii, which the relationships connect, will be respectively,
![r_1, r_2, \\cdots,
r_7](https://s0.wp.com/latex.php?latex=r_1%2C+r_2%2C+%5Ccdots%2C+r_7&bg=ffffff&fg=333333&s=0&c=20201002) and ![r_s, r_t](https://s0.wp.com/latex.php?latex=r_s%2C+r_t&bg=ffffff&fg=333333&s=0&c=20201002). We outline the proof rather than present all the tedious trigonometry and radical algebra. If you like to do that with paper and pencil and are good at that, you can try the same. However, we cut through the tedium of the at times complicated algebra using a combination of recognizing key patterns and the open-source computer algebra system from GeoGebra that seamlessly interfaces with its geometric constructions. Nevertheless, we will show a few obvious ones to lay the background.

[![equilateral_in_square](https://manasataramgini.files.wordpress.com/2021/12/equilateral_in_square.png?w=640)](https://manasataramgini.files.wordpress.com/2021/12/equilateral_in_square.png)

**Figure 1.**

• First, with is straightforward trigonometry to show that

![\\dfrac{r_s}{r_t}=\\sqrt{3}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Br_s%7D%7Br_t%7D%3D%5Csqrt%7B3%7D&bg=ffffff&fg=333333&s=0&c=20201002)

• The proportion of the radii of the incircles is equal to the proportion of the equivalent sides of their triangles.

• Let the side of the largest inscribed equilateral triangle (blue) be
![t_1](https://s0.wp.com/latex.php?latex=t_1&bg=ffffff&fg=333333&s=0&c=20201002)
and the smaller one (sharing the side with the square) be
![t_2](https://s0.wp.com/latex.php?latex=t_2&bg=ffffff&fg=333333&s=0&c=20201002).
We can use the half-angle formula to show that
![\\cos\\left(15^\\circ\\right) =
\\tfrac{\\sqrt{2}(1+\\sqrt{3})}{4}](https://s0.wp.com/latex.php?latex=%5Ccos%5Cleft%2815%5E%5Ccirc%5Cright%29+%3D+%5Ctfrac%7B%5Csqrt%7B2%7D%281%2B%5Csqrt%7B3%7D%29%7D%7B4%7D&bg=ffffff&fg=333333&s=0&c=20201002). In turn, that means ![\\tfrac{t_1}{t_2}= \\tfrac{1}{\\cos\\left(15^\\circ\\right)} = \\sqrt{2}\\left(\\sqrt{3}-1\\right)](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bt_1%7D%7Bt_2%7D%3D+%5Ctfrac%7B1%7D%7B%5Ccos%5Cleft%2815%5E%5Ccirc%5Cright%29%7D+%3D+%5Csqrt%7B2%7D%5Cleft%28%5Csqrt%7B3%7D-1%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002)

• We can see that triangles with incircles
![c_2](https://s0.wp.com/latex.php?latex=c_2&bg=ffffff&fg=333333&s=0&c=20201002),
![c_4](https://s0.wp.com/latex.php?latex=c_4&bg=ffffff&fg=333333&s=0&c=20201002),
![c_5](https://s0.wp.com/latex.php?latex=c_5&bg=ffffff&fg=333333&s=0&c=20201002)
and
![c_6](https://s0.wp.com/latex.php?latex=c_6&bg=ffffff&fg=333333&s=0&c=20201002)
are similar
![45^\\circ-60^\\circ-75^\\circ](https://s0.wp.com/latex.php?latex=45%5E%5Ccirc-60%5E%5Ccirc-75%5E%5Ccirc&bg=ffffff&fg=333333&s=0&c=20201002)
triangles. Using the Sine Law we can show that the sides of such a triangle are in the ratio ![1: \\sqrt{\\tfrac{3}{2}}: \\tfrac{1+\\sqrt{3}}{2}](https://s0.wp.com/latex.php?latex=1%3A+%5Csqrt%7B%5Ctfrac%7B3%7D%7B2%7D%7D%3A+%5Ctfrac%7B1%2B%5Csqrt%7B3%7D%7D%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002). With this and the above we can get the proportionality of these triangles. For example, we can show that the sides of the triangles with
![c_2](https://s0.wp.com/latex.php?latex=c_2&bg=ffffff&fg=333333&s=0&c=20201002)
and
![c_4](https://s0.wp.com/latex.php?latex=c_4&bg=ffffff&fg=333333&s=0&c=20201002)
are in the proportion:
![\\tfrac{\\sqrt{2}\\left(1+\\sqrt{3}\\right)}{2}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7B%5Csqrt%7B2%7D%5Cleft%281%2B%5Csqrt%7B3%7D%5Cright%29%7D%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002).
:

![\\dfrac{r_2}{r_4}=\\dfrac{\\sqrt{2}\\left(1+\\sqrt{3}\\right)}{2}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Br_2%7D%7Br_4%7D%3D%5Cdfrac%7B%5Csqrt%7B2%7D%5Cleft%281%2B%5Csqrt%7B3%7D%5Cright%29%7D%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002)

![\\dfrac{r_6}{r_2}= \\sqrt{2}\\left(\\sqrt{3}-1\\right)](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Br_6%7D%7Br_2%7D%3D+%5Csqrt%7B2%7D%5Cleft%28%5Csqrt%7B3%7D-1%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002)

![\\dfrac{r_6}{r_4}=2](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Br_6%7D%7Br_4%7D%3D2&bg=ffffff&fg=333333&s=0&c=20201002)

![\\dfrac{r_6}{r_5}=\\sqrt{2}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Br_6%7D%7Br_5%7D%3D%5Csqrt%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002)

![\\dfrac{r_5}{r_4}=\\sqrt{2}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Br_5%7D%7Br_4%7D%3D%5Csqrt%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002)

![\\dfrac{r_5}{r_2}=\\sqrt{3}-1](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Br_5%7D%7Br_2%7D%3D%5Csqrt%7B3%7D-1&bg=ffffff&fg=333333&s=0&c=20201002)

• Next, we use Brahmagupta’s formula for the incircle of a triangle,
![r=\\tfrac{A(\\triangle)}{s}](https://s0.wp.com/latex.php?latex=r%3D%5Ctfrac%7BA%28%5Ctriangle%29%7D%7Bs%7D&bg=ffffff&fg=333333&s=0&c=20201002),
where
![s](https://s0.wp.com/latex.php?latex=s&bg=ffffff&fg=333333&s=0&c=20201002)
is the semiperimeter (half the perimeter) of the triangle. From the proportions of the triangle sides, we can show that the ratio of the areas and the perimeters of the triangles whose incircles are
![c_3](https://s0.wp.com/latex.php?latex=c_3&bg=ffffff&fg=333333&s=0&c=20201002)
and
![c_4](https://s0.wp.com/latex.php?latex=c_4&bg=ffffff&fg=333333&s=0&c=20201002)
are both
![1+\\tfrac{2\\sqrt{3}}{3}](https://s0.wp.com/latex.php?latex=1%2B%5Ctfrac%7B2%5Csqrt%7B3%7D%7D%7B3%7D&bg=ffffff&fg=333333&s=0&c=20201002)

![\\therefore r_3=r_4](https://s0.wp.com/latex.php?latex=%5Ctherefore+r_3%3Dr_4&bg=ffffff&fg=333333&s=0&c=20201002)

• Thus, from above we have:
![r_6=2r_4](https://s0.wp.com/latex.php?latex=r_6%3D2r_4&bg=ffffff&fg=333333&s=0&c=20201002)
and ![r_5^2 = r_4 r_6 = r_3 r_6](https://s0.wp.com/latex.php?latex=r_5%5E2+%3D+r_4+r_6+%3D+r_3+r_6&bg=ffffff&fg=333333&s=0&c=20201002), i.e., a geometric mean relationship.

• Similarly, we use Brahmagupta’s formula to obtain the incircle radii of
![c_1](https://s0.wp.com/latex.php?latex=c_1&bg=ffffff&fg=333333&s=0&c=20201002)
and
![c_7](https://s0.wp.com/latex.php?latex=c_7&bg=ffffff&fg=333333&s=0&c=20201002).
With that, we get the following relationships:

![\\dfrac{r_1}{r_2}=1+\\sqrt{2}-\\sqrt{3}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Br_1%7D%7Br_2%7D%3D1%2B%5Csqrt%7B2%7D-%5Csqrt%7B3%7D&bg=ffffff&fg=333333&s=0&c=20201002)

![\\dfrac{r_1}{r_4}= \\dfrac{r_1}{r_3} = 1-\\sqrt{2}+\\sqrt{3}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Br_1%7D%7Br_4%7D%3D+%5Cdfrac%7Br_1%7D%7Br_3%7D+%3D+1-%5Csqrt%7B2%7D%2B%5Csqrt%7B3%7D&bg=ffffff&fg=333333&s=0&c=20201002)

![\\therefore r_1 = \\dfrac{2 r_2 r_3}{r_2+r_3} = \\dfrac{2 r_2 r_4}{r_2+r_4}](https://s0.wp.com/latex.php?latex=%5Ctherefore+r_1+%3D+%5Cdfrac%7B2+r_2+r_3%7D%7Br_2%2Br_3%7D+%3D+%5Cdfrac%7B2+r_2+r_4%7D%7Br_2%2Br_4%7D&bg=ffffff&fg=333333&s=0&c=20201002), i.e., a harmonic mean relationship.

![\\dfrac{r_6}{r_7}=2-\\dfrac{\\sqrt{2}(\\sqrt{3}-1)}{2}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Br_6%7D%7Br_7%7D%3D2-%5Cdfrac%7B%5Csqrt%7B2%7D%28%5Csqrt%7B3%7D-1%29%7D%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002)

![\\dfrac{r_6}{r_2}= \\sqrt{2}\\left(\\sqrt{3}-1\\right)](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Br_6%7D%7Br_2%7D%3D+%5Csqrt%7B2%7D%5Cleft%28%5Csqrt%7B3%7D-1%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002)

![\\therefore r_6 = \\dfrac{4 r_2 r_7}{2 r_2+r_7}](https://s0.wp.com/latex.php?latex=%5Ctherefore+r_6+%3D+%5Cdfrac%7B4+r_2+r_7%7D%7B2+r_2%2Br_7%7D&bg=ffffff&fg=333333&s=0&c=20201002), i.e.,
![r_6](https://s0.wp.com/latex.php?latex=r_6&bg=ffffff&fg=333333&s=0&c=20201002)
is the harmonic mean of ![(2 r_2, r_7)](https://s0.wp.com/latex.php?latex=%282+r_2%2C+r_7%29&bg=ffffff&fg=333333&s=0&c=20201002).

• One can also get relationships connecting the radii of all the 7 incircles ![c_1 \\cdots c_7](https://s0.wp.com/latex.php?latex=c_1+%5Ccdots+c_7&bg=ffffff&fg=333333&s=0&c=20201002) and also all 9 incircles in the configuration (Figure 1):

![r_2 r_5 r_6 - r_3 r_5 r_7= 2 r_1 r_4 r_7](https://s0.wp.com/latex.php?latex=r_2+r_5+r_6+-+r_3+r_5+r_7%3D+2+r_1+r_4+r_7&bg=ffffff&fg=333333&s=0&c=20201002)

![\\dfrac{r_2}{r_3} \\dfrac{r_6}{r_7}-2 \\dfrac{r_1}{r_5}=\\dfrac{r_s}{r_t}-\\dfrac{r_5}{r_2}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Br_2%7D%7Br_3%7D+%5Cdfrac%7Br_6%7D%7Br_7%7D-2+%5Cdfrac%7Br_1%7D%7Br_5%7D%3D%5Cdfrac%7Br_s%7D%7Br_t%7D-%5Cdfrac%7Br_5%7D%7Br_2%7D&bg=ffffff&fg=333333&s=0&c=20201002)

Thus, one can see the “2-ness” of the square in the form of
![\\sqrt{2}](https://s0.wp.com/latex.php?latex=%5Csqrt%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002)
and the “3-ness” of the equilateral triangle in the form of
![\\sqrt{3}](https://s0.wp.com/latex.php?latex=%5Csqrt%7B3%7D&bg=ffffff&fg=333333&s=0&c=20201002)
pervades the system.
