+++
title = "Some observations on the"
full_title = "Some observations on the LekkerkerkerZeckendorf decomposition of integers"
date = "2022-01-19"
upstream_url = "https://manasataramgini.wordpress.com/2022/01/19/some-observations-on-the-lekkerkerker-zeckendorf-decomposition-of-integers/"

+++
Source: [here](https://manasataramgini.wordpress.com/2022/01/19/some-observations-on-the-lekkerkerker-zeckendorf-decomposition-of-integers/).

Some observations on the Lekkerkerker-Zeckendorf decomposition of integers

In our youth, we learned of a nice arithmetic theorem of Lekkerkerker
(more popularly known after Zeckendorf; hereinafter L-Z) that relates to
the famous Mātrā-meru sequence
![M](https://s0.wp.com/latex.php?latex=M&bg=ffffff&fg=333333&s=0&c=20201002):
0, 1, 1, 2, 3, 5, 8… defined by the recurrence relationship
![f\[n+2\]=f\[n+1\]+f\[n\]](https://s0.wp.com/latex.php?latex=f%5Bn%2B2%5D%3Df%5Bn%2B1%5D%2Bf%5Bn%5D&bg=ffffff&fg=333333&s=0&c=20201002).
The theorem states that all positive integers can be uniquely expressed
as a sum of one or more distinct non-consecutive terms of
![M](https://s0.wp.com/latex.php?latex=M&bg=ffffff&fg=333333&s=0&c=20201002).
A proof for this theorem can be visualized through a simple geometric
construction (Figure 1).

[![Zeckendorf_decomposition](https://manasataramgini.files.wordpress.com/2022/01/zeckendorf_decomposition.png?w=608&h=504)](https://manasataramgini.files.wordpress.com/2022/01/zeckendorf_decomposition.png)The
graphical L-Z decomposition of integers from 1..12

Pile rectangles whose sides are two successive terms of
![M](https://s0.wp.com/latex.php?latex=M&bg=ffffff&fg=333333&s=0&c=20201002)
so as to make a ![n \\times
n](https://s0.wp.com/latex.php?latex=n+%5Ctimes+n&bg=ffffff&fg=333333&s=0&c=20201002)
half-square (Figure 1). One can see that every integer can be reached by
a horizontal path of such rectangles. This also specifies the algorithm
for the L-Z decomposition of an integer
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002).
Find the largest term
![m](https://s0.wp.com/latex.php?latex=m&bg=ffffff&fg=333333&s=0&c=20201002)
of
![M](https://s0.wp.com/latex.php?latex=M&bg=ffffff&fg=333333&s=0&c=20201002)
such that ![m \\le
n](https://s0.wp.com/latex.php?latex=m+%5Cle+n&bg=ffffff&fg=333333&s=0&c=20201002).
If ![m \<
n](https://s0.wp.com/latex.php?latex=m+%3C+n&bg=ffffff&fg=333333&s=0&c=20201002)
then continue the same procedure on the difference
![n-m](https://s0.wp.com/latex.php?latex=n-m&bg=ffffff&fg=333333&s=0&c=20201002)
till
![n-m=0](https://s0.wp.com/latex.php?latex=n-m%3D0&bg=ffffff&fg=333333&s=0&c=20201002).
This gives us the decompositions shown in Figure 1.

One can define sequence
![f](https://s0.wp.com/latex.php?latex=f&bg=ffffff&fg=333333&s=0&c=20201002)
that counts the length of the L-Z decomposition of each integer
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002).
For example, we see that 12=8+3+1, i.e., it is decomposed into 3 terms.
Thus,
![f\[12\]=3](https://s0.wp.com/latex.php?latex=f%5B12%5D%3D3&bg=ffffff&fg=333333&s=0&c=20201002);
similarly ![f\[11\]=2= f\[10\]=
f\[9\]=2](https://s0.wp.com/latex.php?latex=f%5B11%5D%3D2%3D+f%5B10%5D%3D+f%5B9%5D%3D2&bg=ffffff&fg=333333&s=0&c=20201002).
![f](https://s0.wp.com/latex.php?latex=f&bg=ffffff&fg=333333&s=0&c=20201002)
goes as: 1, 1, 1, 2, 1, 2, 2, 1, 2, 2, 2, 3, 1, 2, 2, 2, 3, 2, 3, 3, 1,
2, 2, 2, 3, 2, 3, 3, 2, 3, 3, 3, 4, 1, 2,
![\\cdots](https://s0.wp.com/latex.php?latex=%5Ccdots&bg=ffffff&fg=333333&s=0&c=20201002)

One see that the value jumps by 1 for the first time at certain values
of
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
(Figure 2): ![f\[1\]=1, f\[4\]=2, f\[12\]=3,
f\[33\]=4](https://s0.wp.com/latex.php?latex=f%5B1%5D%3D1%2C+f%5B4%5D%3D2%2C+f%5B12%5D%3D3%2C+f%5B33%5D%3D4&bg=ffffff&fg=333333&s=0&c=20201002).
Using these
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
we define a new sequence
![f_m](https://s0.wp.com/latex.php?latex=f_m&bg=ffffff&fg=333333&s=0&c=20201002):
1, 4, 12, 33
![\\cdots](https://s0.wp.com/latex.php?latex=%5Ccdots&bg=ffffff&fg=333333&s=0&c=20201002)
We can then ask what is its convergent? We found that,

![\\displaystyle n \\to \\infty, \\;
\\dfrac{f_m\[n+1\]}{f_m\[n\]}=\\phi^2=\\phi+1](https://s0.wp.com/latex.php?latex=%5Cdisplaystyle+n+%5Cto+%5Cinfty%2C+%5C%3B+%5Cdfrac%7Bf_m%5Bn%2B1%5D%7D%7Bf_m%5Bn%5D%7D%3D%5Cphi%5E2%3D%5Cphi%2B1&bg=ffffff&fg=333333&s=0&c=20201002),

where
![\\phi](https://s0.wp.com/latex.php?latex=%5Cphi&bg=ffffff&fg=333333&s=0&c=20201002)
is the Golden ratio
![\\tfrac{1+\\sqrt{5}}{2}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7B1%2B%5Csqrt%7B5%7D%7D%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002).

We can then ask if there is a closed expression for
![f_m](https://s0.wp.com/latex.php?latex=f_m&bg=ffffff&fg=333333&s=0&c=20201002).
We derived this to be:

![\\displaystyle f_m\[n\] = \\left\\lfloor 2\\sum\_{k=0}^{\\infty} -1^k
\\phi^{2n-3k-1}
\\right\\rfloor](https://s0.wp.com/latex.php?latex=%5Cdisplaystyle+f_m%5Bn%5D+%3D+%5Cleft%5Clfloor+2%5Csum_%7Bk%3D0%7D%5E%7B%5Cinfty%7D+-1%5Ek+%5Cphi%5E%7B2n-3k-1%7D+%5Cright%5Crfloor&bg=ffffff&fg=333333&s=0&c=20201002)

[![LZ_Fig2](https://manasataramgini.files.wordpress.com/2022/01/lz_fig2.png?w=620&h=451)](https://manasataramgini.files.wordpress.com/2022/01/lz_fig2.png)Figure
2

Another class of sequences we explored was
![f_k](https://s0.wp.com/latex.php?latex=f_k&bg=ffffff&fg=333333&s=0&c=20201002),
the lengths of the L-Z decompositions of
![k^n](https://s0.wp.com/latex.php?latex=k%5En&bg=ffffff&fg=333333&s=0&c=20201002),
where ![k=2, 3, 4,
5](https://s0.wp.com/latex.php?latex=k%3D2%2C+3%2C+4%2C+5&bg=ffffff&fg=333333&s=0&c=20201002)
and ![n=0, 1, 2
\\cdots](https://s0.wp.com/latex.php?latex=n%3D0%2C+1%2C+2+%5Ccdots&bg=ffffff&fg=333333&s=0&c=20201002),
i.e., the powers of integers. For example,
![f_2](https://s0.wp.com/latex.php?latex=f_2&bg=ffffff&fg=333333&s=0&c=20201002)
goes thus: 1, 1, 2, 1, 2, 3, 3, 3, 3, 6
![\\cdots](https://s0.wp.com/latex.php?latex=%5Ccdots&bg=ffffff&fg=333333&s=0&c=20201002).
Plots of
![f_k](https://s0.wp.com/latex.php?latex=f_k&bg=ffffff&fg=333333&s=0&c=20201002)
against
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
show a good fit for a linear growth in the range in which we computed
these values (Figure 3; it is computationally intensive), albeit with
increasing dispersion as
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
increases. If we take their growth to be linear, we then can ask the
question: what would be the slope of these lines? Interestingly, we
empirically found the slopes of the lines approximating the L-Z
decomposition lengths of ![2^n, 3^n, 4^n,
5^n](https://s0.wp.com/latex.php?latex=2%5En%2C+3%5En%2C+4%5En%2C+5%5En&bg=ffffff&fg=333333&s=0&c=20201002)
to be respectively ![2^{-4/3}, 2^{-2/3}, 2^{-1/3},
2^{-1/9}](https://s0.wp.com/latex.php?latex=2%5E%7B-4%2F3%7D%2C+2%5E%7B-2%2F3%7D%2C+2%5E%7B-1%2F3%7D%2C+2%5E%7B-1%2F9%7D&bg=ffffff&fg=333333&s=0&c=20201002).
Can this be proven or is there an alternative description of the growth
of these sequences?

[![LZ_Fig3](https://manasataramgini.files.wordpress.com/2022/01/lz_fig3.png?w=636&h=462)](https://manasataramgini.files.wordpress.com/2022/01/lz_fig3.png)Figure
3
