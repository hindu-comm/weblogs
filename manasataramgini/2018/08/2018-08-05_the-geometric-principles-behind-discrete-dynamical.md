+++
title = "The geometric principles behind discrete dynamical systems based on the generalized Witch of Agnesi"
date = "2018-08-05"
upstream_url = "https://manasataramgini.wordpress.com/2018/08/05/the-geometric-principles-behind-discrete-dynamical-systems-based-on-the-generalized-witch-of-agnesi/"

+++
Source: [here](https://manasataramgini.wordpress.com/2018/08/05/the-geometric-principles-behind-discrete-dynamical-systems-based-on-the-generalized-witch-of-agnesi/).

Consider the family of curves defined by the equation following parametric equation

![x=\\dfrac{1}{\\sqrt{\\pi\\left(1-a\\right)}}\\left(\\cos\\left(\\alpha\\right)\\left(t+1\\right)+\\dfrac{\\sin\\left(\\alpha\\right)\\left(1+at+at^2+at^3\\right)}{1+t^2}-1\\right)](https://s0.wp.com/latex.php?latex=x%3D%5Cdfrac%7B1%7D%7B%5Csqrt%7B%5Cpi%5Cleft%281-a%5Cright%29%7D%7D%5Cleft%28%5Ccos%5Cleft%28%5Calpha%5Cright%29%5Cleft%28t%2B1%5Cright%29%2B%5Cdfrac%7B%5Csin%5Cleft%28%5Calpha%5Cright%29%5Cleft%281%2Bat%2Bat%5E2%2Bat%5E3%5Cright%29%7D%7B1%2Bt%5E2%7D-1%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),

![y=\\dfrac{1}{\\sqrt{\\pi\\left(1-a\\right)}}\\left(-\\sin\\left(\\alpha\\right)\\left(t+1\\right)+\\dfrac{\\cos\\left(\\alpha\\right)\\left(1+at+at^2+at^3\\right)}{1+t^2}\\right)](https://s0.wp.com/latex.php?latex=y%3D%5Cdfrac%7B1%7D%7B%5Csqrt%7B%5Cpi%5Cleft%281-a%5Cright%29%7D%7D%5Cleft%28-%5Csin%5Cleft%28%5Calpha%5Cright%29%5Cleft%28t%2B1%5Cright%29%2B%5Cdfrac%7B%5Ccos%5Cleft%28%5Calpha%5Cright%29%5Cleft%281%2Bat%2Bat%5E2%2Bat%5E3%5Cright%29%7D%7B1%2Bt%5E2%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002)

where ![\\alpha= \\textrm{atan}(a)](https://s0.wp.com/latex.php?latex=%5Calpha%3D+%5Ctextrm%7Batan%7D%28a%29&bg=ffffff&fg=333333&s=0&c=20201002) and ![-1\\le a \\le 1](https://s0.wp.com/latex.php?latex=-1%5Cle+a+%5Cle+1&bg=ffffff&fg=333333&s=0&c=20201002)

It defines a family of probability distribution functions (PDFs): This can be seen from the above equations because

![\\displaystyle \\int\_{-\\infty}^\\infty y\\dfrac{dx}{dt} dt=1](https://s0.wp.com/latex.php?latex=%5Cdisplaystyle+%5Cint_%7B-%5Cinfty%7D%5E%5Cinfty+y%5Cdfrac%7Bdx%7D%7Bdt%7D+dt%3D1&bg=ffffff&fg=333333&s=0&c=20201002)

[![Figure1_Miroid_PDFs](https://manasataramgini.files.wordpress.com/2018/08/figure1_miroid_pdfs.png?w=640)](https://manasataramgini.files.wordpress.com/2018/08/figure1_miroid_pdfs.png)Figure 1

Examples of these PDFs are illustrated in Figure 1. One can see that when
![a=0](https://s0.wp.com/latex.php?latex=a%3D0&bg=ffffff&fg=333333&s=0&c=20201002)
it is symmetric and reduces to a Cauchy distribution, which was discovered by Poisson and Cauchy. This distribution is famous for having “fat tails” and violating the Central Limit Theorem. A simple geometric example of this distribution is the following: Let the point ![P=(0, 1)](https://s0.wp.com/latex.php?latex=P%3D%280%2C+1%29&bg=ffffff&fg=333333&s=0&c=20201002) be the source of rays that are emanated at an equal angular separation from the adjacent ray. Then the density of the x-intercepts of the rays is equivalent to the PDF corresponding to
![a=0](https://s0.wp.com/latex.php?latex=a%3D0&bg=ffffff&fg=333333&s=0&c=20201002).
The family of PDFs in Figure 1 are a generalization of the Cauchy distribution case. When ![-1 \\le a \< 0](https://s0.wp.com/latex.php?latex=-1+%5Cle+a+%3C+0&bg=ffffff&fg=333333&s=0&c=20201002) the distribution is more peaked and skewed to the left. Conversely, when
![0\< a \<
1](https://s0.wp.com/latex.php?latex=0%3C+a+%3C+1&bg=ffffff&fg=333333&s=0&c=20201002) the distribution is less-peaked and skewed to the right. When ![a\\to 1](https://s0.wp.com/latex.php?latex=a%5Cto+1&bg=ffffff&fg=333333&s=0&c=20201002), the distribution become more and more flat and uniform. They all have fat tails like the Cauchy distribution case. Are these other distributions encountered anywhere? While we have some suspicions that such distributions might occur in the path-lengths of searching behaviors of certain organisms, this is a question we have not been able to definitively answer. Nevertheless, the function behind the above PDFs generates a very interesting class of maps exhibiting chaotic behavior and this is what we shall discuss below.

The function which determines the shapes above PDFs can be written as,

![y=\\dfrac{1+ax+ax^2+ax^3}{1+x^2}](https://s0.wp.com/latex.php?latex=y%3D%5Cdfrac%7B1%2Bax%2Bax%5E2%2Bax%5E3%7D%7B1%2Bx%5E2%7D&bg=ffffff&fg=333333&s=0&c=20201002)

[![Figure2_Miroid_fx](https://manasataramgini.files.wordpress.com/2018/08/figure2_miroid_fx.png?w=578&h=578)](https://manasataramgini.files.wordpress.com/2018/08/figure2_miroid_fx.png)

Figure 2

Examples of this curve as illustrated in Figure 2. One notices that it essentially produces unscaled versions of the above PDF curves, which are rotated about the point
![(-1,0)](https://s0.wp.com/latex.php?latex=%28-1%2C0%29&bg=ffffff&fg=333333&s=0&c=20201002)
by the angle ![\\alpha= \\textrm{atan}(a)](https://s0.wp.com/latex.php?latex=%5Calpha%3D+%5Ctextrm%7Batan%7D%28a%29&bg=ffffff&fg=333333&s=0&c=20201002). As a result, the x-axis of the PDF curves now becomes the asymptote of these curves which has the equation
![y=ax+a](https://s0.wp.com/latex.php?latex=y%3Dax%2Ba&bg=ffffff&fg=333333&s=0&c=20201002).
When
![a=0](https://s0.wp.com/latex.php?latex=a%3D0&bg=ffffff&fg=333333&s=0&c=20201002),
again this curve reduces to the shape-determining curve of the Cauchy distribution, i.e. the [Witch (of Agnesi)](https://manasataramgini.wordpress.com/2016/10/23/syllable-number-and-rules-in-the-ideal-realm/). For
![a=1](https://s0.wp.com/latex.php?latex=a%3D1&bg=ffffff&fg=333333&s=0&c=20201002)
it becomes identical with the
![45^o](https://s0.wp.com/latex.php?latex=45%5Eo&bg=ffffff&fg=333333&s=0&c=20201002)
asymptotic line.

We then consider the following mapping procedure:

1\) Take (equally-spaced) points on a circle with center at origin and radius
![r](https://s0.wp.com/latex.php?latex=r&bg=ffffff&fg=333333&s=0&c=20201002).
For reasonable aesthetics we commonly take
![r=5](https://s0.wp.com/latex.php?latex=r%3D5&bg=ffffff&fg=333333&s=0&c=20201002)

2\) Then subject each of these points ![P_0=(x_0, y_0)](https://s0.wp.com/latex.php?latex=P_0%3D%28x_0%2C+y_0%29&bg=ffffff&fg=333333&s=0&c=20201002) to the iterative mapping:

![x\_{n+1}=by_n+f(x_n)](https://s0.wp.com/latex.php?latex=x_%7Bn%2B1%7D%3Dby_n%2Bf%28x_n%29&bg=ffffff&fg=333333&s=0&c=20201002)

![y\_{n+1}=-x_n+f(x\_{n+1})](https://s0.wp.com/latex.php?latex=y_%7Bn%2B1%7D%3D-x_n%2Bf%28x_%7Bn%2B1%7D%29&bg=ffffff&fg=333333&s=0&c=20201002)

Here,
![b](https://s0.wp.com/latex.php?latex=b&bg=ffffff&fg=333333&s=0&c=20201002)
is a constant that is taken as 1 or a value close to it; ![.99 \\le b \\le 1.001](https://s0.wp.com/latex.php?latex=.99+%5Cle+b+%5Cle+1.001&bg=ffffff&fg=333333&s=0&c=20201002) produces the best aesthetics.

![f(x)=\\dfrac{1+ax+ax^2+ax^3}{1+x^2}](https://s0.wp.com/latex.php?latex=f%28x%29%3D%5Cdfrac%7B1%2Bax%2Bax%5E2%2Bax%5E3%7D%7B1%2Bx%5E2%7D&bg=ffffff&fg=333333&s=0&c=20201002), i.e the above shape-determining function of the above PDFs.

3\) Plot the orbits of all ![P_0=(x_0, y_0)](https://s0.wp.com/latex.php?latex=P_0%3D%28x_0%2C+y_0%29&bg=ffffff&fg=333333&s=0&c=20201002) on the circle under this map.

[![Figure3_Miroid_mapping](https://manasataramgini.files.wordpress.com/2018/08/figure3_miroid_mapping.png?w=666&h=516)](https://manasataramgini.files.wordpress.com/2018/08/figure3_miroid_mapping.png)Figure 3

This mapping procedure is illustrated with an example in Figure 3. We start with a circle shown in red,
![r=5](https://s0.wp.com/latex.php?latex=r%3D5&bg=ffffff&fg=333333&s=0&c=20201002),
on which 360 equally spaced starting points
![P_0](https://s0.wp.com/latex.php?latex=P_0&bg=ffffff&fg=333333&s=0&c=20201002)
lie. We then use
![P_0](https://s0.wp.com/latex.php?latex=P_0&bg=ffffff&fg=333333&s=0&c=20201002)
to sample the curve
![f(x)](https://s0.wp.com/latex.php?latex=f%28x%29&bg=ffffff&fg=333333&s=0&c=20201002)
with
![a=0.525](https://s0.wp.com/latex.php?latex=a%3D0.525&bg=ffffff&fg=333333&s=0&c=20201002)
twice, as indicated in the above map, to get the next point. The curve
![f(x)](https://s0.wp.com/latex.php?latex=f%28x%29&bg=ffffff&fg=333333&s=0&c=20201002)
is shown in green. Its unrotated equivalent, which determines the shape of the corresponding PDF is shown in blue. For this map we take
![b=1](https://s0.wp.com/latex.php?latex=b%3D1&bg=ffffff&fg=333333&s=0&c=20201002)
and the iterate it for 250 times. The 250 points comprising the orbit of one
![P_0](https://s0.wp.com/latex.php?latex=P_0&bg=ffffff&fg=333333&s=0&c=20201002)
are then plotted. This is repeated for all the 360
![P_0](https://s0.wp.com/latex.php?latex=P_0&bg=ffffff&fg=333333&s=0&c=20201002)s
to get the map show in black in Figure 3. Superimposed on the map is the orbital path of a particular
![P_0](https://s0.wp.com/latex.php?latex=P_0&bg=ffffff&fg=333333&s=0&c=20201002)
(shown in cyan) for the 250 iterates. The evolution of the orbit is
indicated by orange triangles whose three vertices are respectively the two points sampled on
![f(x)](https://s0.wp.com/latex.php?latex=f%28x%29&bg=ffffff&fg=333333&s=0&c=20201002)
(shown in red and green on the curve) for a given mapping step and the
third is the corresponding point on the map. One can see that the map initiated with this particular
![P_0](https://s0.wp.com/latex.php?latex=P_0&bg=ffffff&fg=333333&s=0&c=20201002)
samples only 4 specific regions of the
![f(x)](https://s0.wp.com/latex.php?latex=f%28x%29&bg=ffffff&fg=333333&s=0&c=20201002).
Consequently, the orbit results in the six closed loops. Other
![P_0](https://s0.wp.com/latex.php?latex=P_0&bg=ffffff&fg=333333&s=0&c=20201002)
might sample
![f(x)](https://s0.wp.com/latex.php?latex=f%28x%29&bg=ffffff&fg=333333&s=0&c=20201002)
more extensively and uniformly, resulting in a more widely dispersed or chaotic orbit. Thus, the union of the orbits of all the initiating
![P_0](https://s0.wp.com/latex.php?latex=P_0&bg=ffffff&fg=333333&s=0&c=20201002)s
on our circle results in a map with fractal structure (Figure 3). The chaotic nature of map becomes immediately apparent from the high degree of sensitivity of the orbits to the starting points.

Having worked out this map, we realized that orbits of single points under above mapping with appropriate change of coordinates are related to the map published in 1980 by Gumowski and Mira (G-M). This was among the first strange attractors for which we, like many others before and after us, had written code for (though we must mention that to date we have not read Gumowski and Mira’s paper). It was then than we became curious about the rotational periodicity exhibited by some examples of the G-M map resulting in rotational quasi-symmetry. We were able to finally provide the rationale for this geometry when we discovered the map which we are currently discussing. The maps discussed here show a strong tendency for rotational periodicity — for example, the above example shows a 6-fold periodicity — what we term the n-ad structure. Indeed, these maps are better for understanding the rotational periodicity than the original G-M maps because all the powers of
![x](https://s0.wp.com/latex.php?latex=x&bg=ffffff&fg=333333&s=0&c=20201002)
in
![f(x)](https://s0.wp.com/latex.php?latex=f%28x%29&bg=ffffff&fg=333333&s=0&c=20201002)
have the same sign in this map.

In order understand the rotational periodicity in the map we shall have to consider two cases of it separately: first, the case when the radius of the circle on which the starting
![P_0](https://s0.wp.com/latex.php?latex=P_0&bg=ffffff&fg=333333&s=0&c=20201002)s
lie is large; this is empirically taken as ![r \\ge 4](https://s0.wp.com/latex.php?latex=r+%5Cge+4&bg=ffffff&fg=333333&s=0&c=20201002). The second case is when it is small; this is take ![r\< 4](https://s0.wp.com/latex.php?latex=r%3C+4&bg=ffffff&fg=333333&s=0&c=20201002). To examine the former case let us consider the cases in the following figures.

[![Figure4_Miroid_rad5_b9985](https://manasataramgini.files.wordpress.com/2018/08/figure4_miroid_rad5_b9985.png?w=640)](https://manasataramgini.files.wordpress.com/2018/08/figure4_miroid_rad5_b9985.png)Figure 4. Here
![b=0.9985](https://s0.wp.com/latex.php?latex=b%3D0.9985&bg=ffffff&fg=333333&s=0&c=20201002),
![r=5](https://s0.wp.com/latex.php?latex=r%3D5&bg=ffffff&fg=333333&s=0&c=20201002)
and
![a](https://s0.wp.com/latex.php?latex=a&bg=ffffff&fg=333333&s=0&c=20201002)
is the sequence of the first few irreducible vulgar fractions, both positive and negative, i.e. the first few fractions of the form
![\\tfrac{p}{q}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bp%7D%7Bq%7D&bg=ffffff&fg=333333&s=0&c=20201002),
where
![p](https://s0.wp.com/latex.php?latex=p&bg=ffffff&fg=333333&s=0&c=20201002)
and
![q](https://s0.wp.com/latex.php?latex=q&bg=ffffff&fg=333333&s=0&c=20201002)
are mutually prime. Each
![P_0](https://s0.wp.com/latex.php?latex=P_0&bg=ffffff&fg=333333&s=0&c=20201002)’s
orbit is plotted in 1 of 7 different shades of blue in this figure and all subsequent ones. Thus, we keep cycling through these 7 shades for after every 7th
![P_0](https://s0.wp.com/latex.php?latex=P_0&bg=ffffff&fg=333333&s=0&c=20201002).

[![Figure5_Miroid_rad5_b9985](https://manasataramgini.files.wordpress.com/2018/08/figure5_miroid_rad5_b9985.png?w=640)](https://manasataramgini.files.wordpress.com/2018/08/figure5_miroid_rad5_b9985.png)Figure 5. Here
![b=0.9985](https://s0.wp.com/latex.php?latex=b%3D0.9985&bg=ffffff&fg=333333&s=0&c=20201002),
![r=5](https://s0.wp.com/latex.php?latex=r%3D5&bg=ffffff&fg=333333&s=0&c=20201002)
and
![a](https://s0.wp.com/latex.php?latex=a&bg=ffffff&fg=333333&s=0&c=20201002)
is the sequence of further positive irreducible vulgar fractions.

[![Figure6_Miroid_rad5_b9985](https://manasataramgini.files.wordpress.com/2018/08/figure6_miroid_rad5_b9985.png?w=640)](https://manasataramgini.files.wordpress.com/2018/08/figure6_miroid_rad5_b9985.png)Figure 6. Here
![b=0.9985](https://s0.wp.com/latex.php?latex=b%3D0.9985&bg=ffffff&fg=333333&s=0&c=20201002),
![r=5](https://s0.wp.com/latex.php?latex=r%3D5&bg=ffffff&fg=333333&s=0&c=20201002)
and
![a](https://s0.wp.com/latex.php?latex=a&bg=ffffff&fg=333333&s=0&c=20201002)
is the sequence of further irreducible vulgar fractions which are negatives of the above.

Few features become immediately apparent:

1\) The maps exhibit strong rotational periodicity. E.g. for
![a=0](https://s0.wp.com/latex.php?latex=a%3D0&bg=ffffff&fg=333333&s=0&c=20201002)
we get a tetrad structure.

2\) At certain values there is considerable rotational symmetry e.g.
![a=\\tfrac{1}{6}, a=-\\tfrac{3}{4},
-\\tfrac{1}{7}](https://s0.wp.com/latex.php?latex=a%3D%5Ctfrac%7B1%7D%7B6%7D%2C+a%3D-%5Ctfrac%7B3%7D%7B4%7D%2C+-%5Ctfrac%7B1%7D%7B7%7D&bg=ffffff&fg=333333&s=0&c=20201002).

3\) The extreme cases of this are when the map collapses to a completely symmetric radial structure for ![a=\\tfrac{1}{2}, -\\tfrac {1}{2}, -1](https://s0.wp.com/latex.php?latex=a%3D%5Ctfrac%7B1%7D%7B2%7D%2C+-%5Ctfrac+%7B1%7D%7B2%7D%2C+-1&bg=ffffff&fg=333333&s=0&c=20201002)

4\) As the value of ![a \\to \\pm 1](https://s0.wp.com/latex.php?latex=a+%5Cto+%5Cpm+1&bg=ffffff&fg=333333&s=0&c=20201002) the aspect ratio of the map becomes lower and lower along the y-axis and converges to a straight line-segment at the limiting values of
![a](https://s0.wp.com/latex.php?latex=a&bg=ffffff&fg=333333&s=0&c=20201002).

5\) For values of
![a](https://s0.wp.com/latex.php?latex=a&bg=ffffff&fg=333333&s=0&c=20201002)
close to 0 on either side we get maps with aspect ratio closer to 1.

These observations allowed us to develop a formal description of the geometric principles behind these maps:

1\) Since ![-1\\le a \\le 1](https://s0.wp.com/latex.php?latex=-1%5Cle+a+%5Cle+1&bg=ffffff&fg=333333&s=0&c=20201002) it can be considered the cosine of an angle
![\\gamma](https://s0.wp.com/latex.php?latex=%5Cgamma&bg=ffffff&fg=333333&s=0&c=20201002).
Thus, we can write:

![\\textrm{acos}(a)=\\gamma=\\dfrac{2\\pi}{n/m}](https://s0.wp.com/latex.php?latex=%5Ctextrm%7Bacos%7D%28a%29%3D%5Cgamma%3D%5Cdfrac%7B2%5Cpi%7D%7Bn%2Fm%7D&bg=ffffff&fg=333333&s=0&c=20201002), where
![n,m](https://s0.wp.com/latex.php?latex=n%2Cm&bg=ffffff&fg=333333&s=0&c=20201002)
are mutually prime integers.

This fraction
![\\tfrac{n}{m}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bm%7D&bg=ffffff&fg=333333&s=0&c=20201002)
is the shape-determining fraction of the map (Figure 7). When the radius of our starting circle ![r \\ge 4](https://s0.wp.com/latex.php?latex=r+%5Cge+4&bg=ffffff&fg=333333&s=0&c=20201002), then the basic rotational periodicity of the map is determined by
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
and it shows an n-ad structure(Figure 7). Thus, when
![\\tfrac{n}{m}=3](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bm%7D%3D3&bg=ffffff&fg=333333&s=0&c=20201002),
![\\gamma=\\tfrac{2\\pi}{3}](https://s0.wp.com/latex.php?latex=%5Cgamma%3D%5Ctfrac%7B2%5Cpi%7D%7B3%7D&bg=ffffff&fg=333333&s=0&c=20201002).
Hence,
![a=\\cos\\left(\\tfrac{2\\pi}{3}\\right)=-\\tfrac{1}{2}](https://s0.wp.com/latex.php?latex=a%3D%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B3%7D%5Cright%29%3D-%5Ctfrac%7B1%7D%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002).
Thus, as we see in Figure 4,
![a=-\\tfrac{1}{2}](https://s0.wp.com/latex.php?latex=a%3D-%5Ctfrac%7B1%7D%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002)
has a triad structure corresponding to
![n=3](https://s0.wp.com/latex.php?latex=n%3D3&bg=ffffff&fg=333333&s=0&c=20201002).
Similarly, when
![\\tfrac{n}{m}=4](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bm%7D%3D4&bg=ffffff&fg=333333&s=0&c=20201002),
![a=\\cos\\left(\\tfrac{2\\pi}{4}\\right)=0](https://s0.wp.com/latex.php?latex=a%3D%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B4%7D%5Cright%29%3D0&bg=ffffff&fg=333333&s=0&c=20201002);
thus,
![a=0](https://s0.wp.com/latex.php?latex=a%3D0&bg=ffffff&fg=333333&s=0&c=20201002)
results in a map with tetrad structure corresponding to
![n=4](https://s0.wp.com/latex.php?latex=n%3D4&bg=ffffff&fg=333333&s=0&c=20201002)
(Figure 4).

2\) If
![\\gamma=\\textrm{acos}(a)](https://s0.wp.com/latex.php?latex=%5Cgamma%3D%5Ctextrm%7Bacos%7D%28a%29&bg=ffffff&fg=333333&s=0&c=20201002),
then this angle
![\\gamma](https://s0.wp.com/latex.php?latex=%5Cgamma&bg=ffffff&fg=333333&s=0&c=20201002)
can be taken to be the interior angle of a polygon inscribed in a circle
(Figure 7). Now, flatten this circle into an ellipse such that the
eccentricity of the ellipse is
![\|\\tan(\\alpha)\|=\|a\|](https://s0.wp.com/latex.php?latex=%7C%5Ctan%28%5Calpha%29%7C%3D%7Ca%7C&bg=ffffff&fg=333333&s=0&c=20201002)
(Figure 7). Thus, ![0\\le \|a\| \\le
1](https://s0.wp.com/latex.php?latex=0%5Cle+%7Ca%7C+%5Cle+1&bg=ffffff&fg=333333&s=0&c=20201002) describes ellipses within which the map is bounded, which span the entire range from one close to a circle when ![\|a\| \\to 0](https://s0.wp.com/latex.php?latex=%7Ca%7C+%5Cto+0&bg=ffffff&fg=333333&s=0&c=20201002) to one close to a segment when ![\|a\| \\to 1](https://s0.wp.com/latex.php?latex=%7Ca%7C+%5Cto+1&bg=ffffff&fg=333333&s=0&c=20201002). The polygon inscribed in the original circle correspondingly gets flattened into a polygon inscribed in the ellipse (Figure 7). This polygon describes both the n-ad structure of the map as described above, whereas the eccentricity of its bounding ellipse describes the aspect ratio of the maps under consideration.

[![Figure7_Miroid_geometry](https://manasataramgini.files.wordpress.com/2018/08/figure7_miroid_geometry.png?w=640)](https://manasataramgini.files.wordpress.com/2018/08/figure7_miroid_geometry.png)Figure 7. The original generalization of the Witch is in red. The free-rotating version used in the current maps is in green. The polygon inscribed in the circle defined by the
![\\angle{\\gamma}](https://s0.wp.com/latex.php?latex=%5Cangle%7B%5Cgamma%7D&bg=ffffff&fg=333333&s=0&c=20201002)
is shown in blue dotted segments. The ellipse whose eccentricity is determined by the
![\|a\|=\|\\tan(\\alpha)\|](https://s0.wp.com/latex.php?latex=%7Ca%7C%3D%7C%5Ctan%28%5Calpha%29%7C&bg=ffffff&fg=333333&s=0&c=20201002)
is shown in red, with the final polygon inscribed in it in violet.

3\) In order to illustrate the above principles and describe the finer intricacies of the structure of the map beyond the “coarse features” accounted for by the above rules we need to examine several specific examples. Since cases like ![a=\\pm \\tfrac{1}{2}](https://s0.wp.com/latex.php?latex=a%3D%5Cpm+%5Ctfrac%7B1%7D%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002) result a “collapse” of the map to a radial structure (Figure 4), to explain in its entirety the role of the fraction
![\\tfrac{n}{m}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bm%7D&bg=ffffff&fg=333333&s=0&c=20201002)
in determining map shape we add a small positive
![\\epsilon](https://s0.wp.com/latex.php?latex=%5Cepsilon&bg=ffffff&fg=333333&s=0&c=20201002)
to define
![a=\\cos\\left(\\tfrac{2\\pi}{n/m}\\right)+\\epsilon](https://s0.wp.com/latex.php?latex=a%3D%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7Bn%2Fm%7D%5Cright%29%2B%5Cepsilon&bg=ffffff&fg=333333&s=0&c=20201002).

[![Figure8_Miroid_rad5_b9985_d0025](https://manasataramgini.files.wordpress.com/2018/08/figure8_miroid_rad5_b9985_d0025.png?w=640)](https://manasataramgini.files.wordpress.com/2018/08/figure8_miroid_rad5_b9985_d0025.png)Figure 8. In this set of maps the radius of the starting circle
![r=5](https://s0.wp.com/latex.php?latex=r%3D5&bg=ffffff&fg=333333&s=0&c=20201002),
![b=0.9985](https://s0.wp.com/latex.php?latex=b%3D0.9985&bg=ffffff&fg=333333&s=0&c=20201002),
![\\epsilon=.0025](https://s0.wp.com/latex.php?latex=%5Cepsilon%3D.0025&bg=ffffff&fg=333333&s=0&c=20201002).
![a](https://s0.wp.com/latex.php?latex=a&bg=ffffff&fg=333333&s=0&c=20201002)
is expressed as sequence of cosines shown with the corresponding angles and
![\\tfrac{n}{m}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bm%7D&bg=ffffff&fg=333333&s=0&c=20201002)
above each map in this and the subsequent figures.

In the first 7 cases,
![\\tfrac{n}{m}=3,4,5,6,7,8,9](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bm%7D%3D3%2C4%2C5%2C6%2C7%2C8%2C9&bg=ffffff&fg=333333&s=0&c=20201002).
According to the above described geometric rules we find that the map adopts a triad, tetrad, pentad…nonad structure with decreasing aspect ratio (Figure 8).

When
![\\tfrac{n}{m}=\\tfrac{9}{2},\\tfrac{11}{2},\\tfrac{13}{3},\\tfrac{15}{4},\\tfrac{17}{4}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bm%7D%3D%5Ctfrac%7B9%7D%7B2%7D%2C%5Ctfrac%7B11%7D%7B2%7D%2C%5Ctfrac%7B13%7D%7B3%7D%2C%5Ctfrac%7B15%7D%7B4%7D%2C%5Ctfrac%7B17%7D%7B4%7D&bg=ffffff&fg=333333&s=0&c=20201002),
we see an obvious 9-, 11-, 13-, 15-, 17-ad structure but with much higher aspect ratios than what would be expected if the denominator were 1. This is because the
![a=\\cos\\left(\\tfrac{2\\pi}{n/m}\\right)+\\epsilon](https://s0.wp.com/latex.php?latex=a%3D%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7Bn%2Fm%7D%5Cright%29%2B%5Cepsilon&bg=ffffff&fg=333333&s=0&c=20201002)
results in eccentricities closer to 0. Thus, choosing such
![\\tfrac{n}{m}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bm%7D&bg=ffffff&fg=333333&s=0&c=20201002)
allows you to obtain n-ad structures at higher aspect ratios (Figure 8).

Further, note the internal structure of the map, i.e. the region close to the center, setting aside the above described patterns for the more peripheral structure described above. The following
![\\tfrac{n}{m}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bm%7D&bg=ffffff&fg=333333&s=0&c=20201002)
are notable:

For
![\\tfrac{9}{2}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7B9%7D%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002)
we get a tetrad interior;

For
![\\tfrac{11}{2}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7B11%7D%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002)
— pentad interior;

For
![\\tfrac{13}{3}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7B13%7D%7B3%7D&bg=ffffff&fg=333333&s=0&c=20201002)
— tetrad interior;

For
![\\tfrac{15}{4}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7B15%7D%7B4%7D&bg=ffffff&fg=333333&s=0&c=20201002)
— triad interior;

For
![\\tfrac{17}{4}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7B17%7D%7B4%7D&bg=ffffff&fg=333333&s=0&c=20201002)
— tetrad interior (Figure 8).

This indicates that for maps with high aspect ratio, the n-ad structure close to the center is determined by the number ![k_1=\\left \\lfloor \\tfrac{n}{m} \\right \\rfloor](https://s0.wp.com/latex.php?latex=k_1%3D%5Cleft+%5Clfloor+%5Ctfrac%7Bn%7D%7Bm%7D+%5Cright+%5Crfloor&bg=ffffff&fg=333333&s=0&c=20201002). In some cases, the value of
![k_1](https://s0.wp.com/latex.php?latex=k_1&bg=ffffff&fg=333333&s=0&c=20201002)
can dominate the shape of the map. For example, when ![k_1=\\left \\lfloor \\tfrac{17}{5} \\right \\rfloor=3, \\left \\lfloor \\tfrac{19}{3} \\right \\rfloor=6](https://s0.wp.com/latex.php?latex=k_1%3D%5Cleft+%5Clfloor+%5Ctfrac%7B17%7D%7B5%7D+%5Cright+%5Crfloor%3D3%2C+%5Cleft+%5Clfloor+%5Ctfrac%7B19%7D%7B3%7D+%5Cright+%5Crfloor%3D6&bg=ffffff&fg=333333&s=0&c=20201002) we see that
![k_1](https://s0.wp.com/latex.php?latex=k_1&bg=ffffff&fg=333333&s=0&c=20201002)
is the dominant n-ad of the shape. However, keeping the primary n-ad rule in each of these cases, the periphery shows 17 and 19 spikes respectively.

Next, note the structure of the map where ![\\tfrac{n}{m} =\\tfrac{17}{3}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bm%7D+%3D%5Ctfrac%7B17%7D%7B3%7D&bg=ffffff&fg=333333&s=0&c=20201002). At the periphery we see 17 “spikes” keeping with the basic structure determining number
![n=17](https://s0.wp.com/latex.php?latex=n%3D17&bg=ffffff&fg=333333&s=0&c=20201002).
Close to the center, we see the pentad structure keeping with the principle described above: ![\\left \\lfloor \\tfrac{17}{3} \\right \\rfloor=5](https://s0.wp.com/latex.php?latex=%5Cleft+%5Clfloor+%5Ctfrac%7B17%7D%7B3%7D+%5Cright+%5Crfloor%3D5&bg=ffffff&fg=333333&s=0&c=20201002) However, the overall map is dominated by a hexad structure — i.e., the 17 spikes are arranged into a hexad pattern. This hexad pattern is also seen in the structure of middle layer of the map. This gives us another principle: Especially for larger
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
if ![k_2=\\textrm{round}\\left(\\tfrac{n}{m} \\right) \> \\left \\lfloor \\tfrac{n}{m} \\right \\rfloor](https://s0.wp.com/latex.php?latex=k_2%3D%5Ctextrm%7Bround%7D%5Cleft%28%5Ctfrac%7Bn%7D%7Bm%7D+%5Cright%29+%3E+%5Cleft+%5Clfloor+%5Ctfrac%7Bn%7D%7Bm%7D+%5Cright+%5Crfloor&bg=ffffff&fg=333333&s=0&c=20201002), then we can get a further layer of structure with a n-ad structure determined by
![k_2](https://s0.wp.com/latex.php?latex=k_2&bg=ffffff&fg=333333&s=0&c=20201002).
This can again be seen in the case of
![\\tfrac{19}{4}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7B19%7D%7B4%7D&bg=ffffff&fg=333333&s=0&c=20201002),
where
![k_2=5](https://s0.wp.com/latex.php?latex=k_2%3D5&bg=ffffff&fg=333333&s=0&c=20201002).
This results in a pentad dominance with a middle pentad layer between the outer 19 spikes and inner tetrad structure (Figure 8).

4\) Finally, we consider the case when the starting circle has
![r\<4](https://s0.wp.com/latex.php?latex=r%3C4&bg=ffffff&fg=333333&s=0&c=20201002).
In this range we observe that the maps do not entirely obey the above rules. We see a progressive “step-down” in the n-ad structure for values other than
![\\tfrac{n}{m}=3](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bm%7D%3D3&bg=ffffff&fg=333333&s=0&c=20201002).
This is illustrated with examples in Figure 9.

[![Figure9_Miroid_radphi_b9985_d001](https://manasataramgini.files.wordpress.com/2018/08/figure9_miroid_radphi_b9985_d001.png?w=640)](https://manasataramgini.files.wordpress.com/2018/08/figure9_miroid_radphi_b9985_d001.png)Figure 9. Here
![r=\\tfrac{1}{\\phi}](https://s0.wp.com/latex.php?latex=r%3D%5Ctfrac%7B1%7D%7B%5Cphi%7D&bg=ffffff&fg=333333&s=0&c=20201002),
where
![\\phi](https://s0.wp.com/latex.php?latex=%5Cphi&bg=ffffff&fg=333333&s=0&c=20201002)
is the Golden ratio;
![b=0.9985](https://s0.wp.com/latex.php?latex=b%3D0.9985&bg=ffffff&fg=333333&s=0&c=20201002);
![\\epsilon=.001](https://s0.wp.com/latex.php?latex=%5Cepsilon%3D.001&bg=ffffff&fg=333333&s=0&c=20201002).

We observe right away that for
![\\tfrac{n}{m}=4](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bm%7D%3D4&bg=ffffff&fg=333333&s=0&c=20201002)
the structure is only incipiently tetrad. For ![\\tfrac{n}{m}=5, 6, 7, 8](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bm%7D%3D5%2C+6%2C+7%2C+8&bg=ffffff&fg=333333&s=0&c=20201002), on the other hand the n-ad structure of the map is respectively a tetrad, pentad, hexad and heptad. Thus, the rotational periodicity rather being equal to
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
comes down to
![n-1](https://s0.wp.com/latex.php?latex=n-1&bg=ffffff&fg=333333&s=0&c=20201002).
For the other fractional
![\\tfrac{n}{m}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bm%7D&bg=ffffff&fg=333333&s=0&c=20201002)
we see only the
![k_1](https://s0.wp.com/latex.php?latex=k_1&bg=ffffff&fg=333333&s=0&c=20201002)
structure, where ![k_1=\\left \\lfloor \\tfrac{n}{m} \\right \\rfloor](https://s0.wp.com/latex.php?latex=k_1%3D%5Cleft+%5Clfloor+%5Ctfrac%7Bn%7D%7Bm%7D+%5Cright+%5Crfloor&bg=ffffff&fg=333333&s=0&c=20201002). We do not see the structure derived from
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
in
![\\tfrac{n}{m}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bm%7D&bg=ffffff&fg=333333&s=0&c=20201002).
In the range ![\\tfrac{1}{\\phi} \\le r \\le 4](https://s0.wp.com/latex.php?latex=%5Ctfrac%7B1%7D%7B%5Cphi%7D+%5Cle+r+%5Cle+4&bg=ffffff&fg=333333&s=0&c=20201002) we see a gradual recovery of the structure that clearly manifests at
![r\\ge
4](https://s0.wp.com/latex.php?latex=r%5Cge+4&bg=ffffff&fg=333333&s=0&c=20201002). We illustrate this in Figure 10.

[![Figure10_Miroid_rad2_b9985_d001](https://manasataramgini.files.wordpress.com/2018/08/figure10_miroid_rad2_b9985_d001.png?w=640)](https://manasataramgini.files.wordpress.com/2018/08/figure10_miroid_rad2_b9985_d001.png)Figure 10. Here
![r=2](https://s0.wp.com/latex.php?latex=r%3D2&bg=ffffff&fg=333333&s=0&c=20201002);
![b=0.9985](https://s0.wp.com/latex.php?latex=b%3D0.9985&bg=ffffff&fg=333333&s=0&c=20201002);
![\\epsilon=.001](https://s0.wp.com/latex.php?latex=%5Cepsilon%3D.001&bg=ffffff&fg=333333&s=0&c=20201002).

We observe that for ![\\tfrac{n}{m}=4, 5, 6, 7, 8, 9, \\tfrac{9}{2}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bm%7D%3D4%2C+5%2C+6%2C+7%2C+8%2C+9%2C+%5Ctfrac%7B9%7D%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002) the typical n-ad structure determined by
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
as seen in the maps where ![r\\ge 4](https://s0.wp.com/latex.php?latex=r%5Cge+4&bg=ffffff&fg=333333&s=0&c=20201002) is restored. However, for the remaining
![\\tfrac{n}{m}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bm%7D&bg=ffffff&fg=333333&s=0&c=20201002),
![k_1=\\left \\lfloor \\tfrac{n}{m} \\right
\\rfloor](https://s0.wp.com/latex.php?latex=k_1%3D%5Cleft+%5Clfloor+%5Ctfrac%7Bn%7D%7Bm%7D+%5Cright+%5Crfloor&bg=ffffff&fg=333333&s=0&c=20201002) is the dominant determinant of the map’s rotational periodicity (Figure 10) and we have to wait till ![r \\ge 4](https://s0.wp.com/latex.php?latex=r+%5Cge+4&bg=ffffff&fg=333333&s=0&c=20201002) for a n-ad structure determined by
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
to emerge. The emergence of the clear n-ad structure only at higher radius values combined with a more complex chaotic behavior at lower radius values is also seen in the well-known Zaslavsky map based on the Hamiltonian of a kicked rotor. However, it is notable that maps with these values of
![\\tfrac{n}{m}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bm%7D&bg=ffffff&fg=333333&s=0&c=20201002)
at low
![r](https://s0.wp.com/latex.php?latex=r&bg=ffffff&fg=333333&s=0&c=20201002)
values have some complex internal structures that are difficult to account for by any of these rules. For example, consider
![\\tfrac{n}{m}=\\tfrac{13}{3}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bm%7D%3D%5Ctfrac%7B13%7D%7B3%7D&bg=ffffff&fg=333333&s=0&c=20201002)
(Figure 10). In each of the 4 outer projections of the tetrad structure
we see an internal hexad attractor. Inside that hexad attractor we see a further pentad attractor. Within the central tetrad element of this map we see a triad excluded space. Finally, in the border of this central tetrad element we see a 7-fold attractor! This is reminiscent of the structures seen in the famous Standard map of Chirikov.

In conclusion, as we saw with [an earlier map that we had discovered](https://manasataramgini.wordpress.com/2018/03/25/the-remarkable-behavior-of-a-map-displaying-derived-from-a-simple-model-for-a-biological-conflict/) and the maps derived from certain [Hamiltonians](https://manasataramgini.wordpress.com/2017/10/30/the-incredible-beauty-of-certain-hamiltonian-mappings/) of kicked rotors/oscillators, there is a hidden role for the irreducible vulgar fractions in determining the shape of the map. While it is easy to see that the rational numbers are distributed uniformly, that is not the case if they are ordered as per their rank based on their numerators and/or denominators. Examples of such fraction sequences are those described by Moritz Stern, Farey and Brocot. Even as in the fractal structure defined by these fraction sequences, the rank of the fraction is central to the definition of the map’s rotational periodicity in current case. The higher ranked
![\\tfrac{n}{m}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bm%7D&bg=ffffff&fg=333333&s=0&c=20201002),
i.e. the low magnitude integers like 3, 4, 5, 6 dominate the n-ad shape of the map relative the other rational numbers in their interstices. However, those interstitial values interact with these dominant values to give layers of complex structure to the map.
