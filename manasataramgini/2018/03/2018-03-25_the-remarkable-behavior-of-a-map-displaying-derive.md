+++
title = "The remarkable behavior of a map displaying derived from a simple model for a biological conflict"
date = "2018-03-25"
upstream_url = "https://manasataramgini.wordpress.com/2018/03/25/the-remarkable-behavior-of-a-map-displaying-derived-from-a-simple-model-for-a-biological-conflict/"

+++
Source: [here](https://manasataramgini.wordpress.com/2018/03/25/the-remarkable-behavior-of-a-map-displaying-derived-from-a-simple-model-for-a-biological-conflict/).

One of the simplest yet profound mathematical models for biological growth emerged sometime in the middle of the 1800s due to the work of Verhulst. It describes population growth thus: let
![x](https://s0.wp.com/latex.php?latex=x&bg=ffffff&fg=333333&s=0&c=20201002)
be the population of the organism at time
![t](https://s0.wp.com/latex.php?latex=t&bg=ffffff&fg=333333&s=0&c=20201002).
![r](https://s0.wp.com/latex.php?latex=r&bg=ffffff&fg=333333&s=0&c=20201002)
is the Malthusian parameter or the rate of maximum population growth.
![K](https://s0.wp.com/latex.php?latex=K&bg=ffffff&fg=333333&s=0&c=20201002)
is the carrying capacity or the maximum sustainable population in a given environment. Then we have the following ordinary differential equation (ODE) as a descriptor of population growth:

![\\dfrac{dx}{dt}=\\dfrac{rx(K-x)}{K}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Bdx%7D%7Bdt%7D%3D%5Cdfrac%7Brx%28K-x%29%7D%7BK%7D&bg=ffffff&fg=333333&s=0&c=20201002)

This is the logistic model that profoundly informs us about various aspects of biology. By define a new ![x \\equiv \\tfrac{x}{K}](https://s0.wp.com/latex.php?latex=x+%5Cequiv+%5Ctfrac%7Bx%7D%7BK%7D&bg=ffffff&fg=333333&s=0&c=20201002) we get:

![\\dfrac{dx}{dt}=rx(1-x)](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Bdx%7D%7Bdt%7D%3Drx%281-x%29&bg=ffffff&fg=333333&s=0&c=20201002)

This simplified form can be next converted into a discrete equation thus:

![x\_{n+1}=rx_n(1-x_n)](https://s0.wp.com/latex.php?latex=x_%7Bn%2B1%7D%3Drx_n%281-x_n%29&bg=ffffff&fg=333333&s=0&c=20201002)

This is the famous logistic map. Simple as it looks, starting with von Neumann’s work and then that of Ulam and Feigenbaum thereafter, it became clear that it exhibits notoriously complex behavior that have considerable implications for dynamics of systems. We had earlier described an exploration of some of this via the vehicle of [Kaneko’s coupled-map lattices](https://manasataramgini.wordpress.com/2017/11/26/pattern-formation-in-coupled-map-lattices-with-the-circle-map-tanh-map-and-chebyshev-map/). Since our teenage years we have been fascinated by the complexity in simplicity of this map and wondered if we might uncover other such cases in simple models of biological systems. Here we describe an example of such, which we discovered.

Consider a two species-system where one species
![x](https://s0.wp.com/latex.php?latex=x&bg=ffffff&fg=333333&s=0&c=20201002)
is a parasite or predator, whose growth rate depends on the number of the host/prey species that it utilizes. The host/prey species
![y](https://s0.wp.com/latex.php?latex=y&bg=ffffff&fg=333333&s=0&c=20201002)
is communal in that it produces certain public goods, which all members of its community share. It incurs a certain cost for producing these. More its population less is this cost because it gets spreadout over more individuals. It grows like any other free-living organism otherwise with growth rate proportional to the number of individuals at a given instant. Its growth is further negatively affected by the predator/parasite which kills all infected individuals. In principle, this system might be described by the below ODEs:

![\\dfrac{dx}{dt}=k_1 y](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Bdx%7D%7Bdt%7D%3Dk_1+y&bg=ffffff&fg=333333&s=0&c=20201002)

![\\dfrac{dy}{dt}=\\dfrac{k_a}{y}+k_b y-k_2 x](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Bdy%7D%7Bdt%7D%3D%5Cdfrac%7Bk_a%7D%7By%7D%2Bk_b+y-k_2+x&bg=ffffff&fg=333333&s=0&c=20201002)

By simplifying this by taking
![k_1=k_2=1](https://s0.wp.com/latex.php?latex=k_1%3Dk_2%3D1&bg=ffffff&fg=333333&s=0&c=20201002)
and expressing it as a discrete equation we get:

![x\_{n+1}=y_n](https://s0.wp.com/latex.php?latex=x_%7Bn%2B1%7D%3Dy_n&bg=ffffff&fg=333333&s=0&c=20201002)

![y\_{n+1}=\\dfrac{k_a}{y_n}+k_b y_n-x_n](https://s0.wp.com/latex.php?latex=y_%7Bn%2B1%7D%3D%5Cdfrac%7Bk_a%7D%7By_n%7D%2Bk_b+y_n-x_n&bg=ffffff&fg=333333&s=0&c=20201002)

Since
![k_a](https://s0.wp.com/latex.php?latex=k_a&bg=ffffff&fg=333333&s=0&c=20201002)
is a cost of public goods production by the communal organism it will always be negative, while
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
being a regular growth constant will be positive. This is the form of the map, which we shall explore further for its dynamics. A few things are readily apparent if
![y_n=0](https://s0.wp.com/latex.php?latex=y_n%3D0&bg=ffffff&fg=333333&s=0&c=20201002)
then the first term of second equation of the map goes to
![-\\infty](https://s0.wp.com/latex.php?latex=-%5Cinfty&bg=ffffff&fg=333333&s=0&c=20201002)
resulting in a singularity. Second both
![\|y_n\|](https://s0.wp.com/latex.php?latex=%7Cy_n%7C&bg=ffffff&fg=333333&s=0&c=20201002)
and
![\|x_n\|](https://s0.wp.com/latex.php?latex=%7Cx_n%7C&bg=ffffff&fg=333333&s=0&c=20201002)
can wander away towards
![\\infty](https://s0.wp.com/latex.php?latex=%5Cinfty&bg=ffffff&fg=333333&s=0&c=20201002);
hence in out experiments we terminate our runs if certain arbitrarily defined limit is reached.

[![Fig_1\_elliptical_2param](https://manasataramgini.files.wordpress.com/2018/03/fig_1_elliptical_2param.png?w=640)](https://manasataramgini.files.wordpress.com/2018/03/fig_1_elliptical_2param.png)Figure 1

Figure 1 shows a run of this system for 100 generations with
![k_a=-0.288,
k_b=0.51](https://s0.wp.com/latex.php?latex=k_a%3D-0.288%2C+k_b%3D0.51&bg=ffffff&fg=333333&s=0&c=20201002) and initiated with ![x_0=-0.0001, y_0=0.04997](https://s0.wp.com/latex.php?latex=x_0%3D-0.0001%2C+y_0%3D0.04997&bg=ffffff&fg=333333&s=0&c=20201002). The expected pattern of
![x_n](https://s0.wp.com/latex.php?latex=x_n&bg=ffffff&fg=333333&s=0&c=20201002)
tracking
![y_n](https://s0.wp.com/latex.php?latex=y_n&bg=ffffff&fg=333333&s=0&c=20201002)
is seen in the oscillatory pattern typical of predator/parasite-prey/host system. We can better understand this by plotting a phase diagram of
![x_n,y_n](https://s0.wp.com/latex.php?latex=x_n%2Cy_n&bg=ffffff&fg=333333&s=0&c=20201002)
as can be seen in Figure 2.

[![Fig2_ellipse_2param_1orb_kaminus.188_kb.45](https://manasataramgini.files.wordpress.com/2018/03/fig2_ellipse_2param_1orb_kaminus-188_kb-45.png?w=640)](https://manasataramgini.files.wordpress.com/2018/03/fig2_ellipse_2param_1orb_kaminus-188_kb-45.png)Figure 2

In Figure 2 we have 9 different runs of the map with different starting
![x_0,
y_0](https://s0.wp.com/latex.php?latex=x_0%2C+y_0&bg=ffffff&fg=333333&s=0&c=20201002) and ![ka=-0.188, kb=0.45](https://s0.wp.com/latex.php?latex=ka%3D-0.188%2C+kb%3D0.45&bg=ffffff&fg=333333&s=0&c=20201002) evolving up to 10000 iterations or terminated if it hits a singularity
(in practice we set some absolute value cut off of say 100 above which
we stop further iterations). The maps are symmetric about the
![x=y](https://s0.wp.com/latex.php?latex=x%3Dy&bg=ffffff&fg=333333&s=0&c=20201002)
line, which arises from the form of the first equation in the map. The map is always bounded by an ellipse of the form
![x^2+y^2-kxy=1](https://s0.wp.com/latex.php?latex=x%5E2%2By%5E2-kxy%3D1&bg=ffffff&fg=333333&s=0&c=20201002),
where ![0 \\le \|k\| \< 2](https://s0.wp.com/latex.php?latex=0+%5Cle+%7Ck%7C+%3C+2&bg=ffffff&fg=333333&s=0&c=20201002). Hence, we call it the 2-parameter elliptical map. Figure 2 reveals that the map is extremely sensitive to changes in the initial conditions: changes in the 3rd to 5th place after the decimal point can result in dramatic differences in the evolution of the
![x_0,y_0](https://s0.wp.com/latex.php?latex=x_0%2Cy_0&bg=ffffff&fg=333333&s=0&c=20201002).

[![Fig3_ellipse_2param_1orb_x0minus.0001_y0\_.04997](https://manasataramgini.files.wordpress.com/2018/03/fig3_ellipse_2param_1orb_x0minus-0001_y0_-04997.png?w=640)](https://manasataramgini.files.wordpress.com/2018/03/fig3_ellipse_2param_1orb_x0minus-0001_y0_-04997.png)Figure 3

Figure 3 shows 9 runs of the evolution of ![x_0=-0.0001, y_0=0.04997](https://s0.wp.com/latex.php?latex=x_0%3D-0.0001%2C+y_0%3D0.04997&bg=ffffff&fg=333333&s=0&c=20201002) for different ![k_a, k_b](https://s0.wp.com/latex.php?latex=k_a%2C+k_b&bg=ffffff&fg=333333&s=0&c=20201002). We gain see that the map is very sensitive to changes in both the parameters and the evolution of the initial point dramatically varies with these changes.

[![Fig4_elliptical_2param_random1](https://manasataramgini.files.wordpress.com/2018/03/fig4_elliptical_2param_random1.png?w=640)](https://manasataramgini.files.wordpress.com/2018/03/fig4_elliptical_2param_random1.png)Figure 4

In Figure 4 we run the following experiment: We chose a square region defined by the diagonal (0.2, 0.2):(-0.2, -0.2). Within this square we chose 3 different sets of 100 random points and allow each set of these points to evolve for a given ![k_a, k_b](https://s0.wp.com/latex.php?latex=k_a%2C+k_b&bg=ffffff&fg=333333&s=0&c=20201002). Thus, each row in Figure 4 is the evolution of the three different sets of random points for a given ![k_a, k_b](https://s0.wp.com/latex.php?latex=k_a%2C+k_b&bg=ffffff&fg=333333&s=0&c=20201002). The evolution of each of the 100 random points for a given run is plotted in a different color. We observe that each run shows a different color pattern because the points are random and evolve very differently, as we know from the single point runs shown in Figures 2 and 3. However, remarkably, the overall structure of the map for a given ![k_a, k_b](https://s0.wp.com/latex.php?latex=k_a%2C+k_b&bg=ffffff&fg=333333&s=0&c=20201002) converges to a constant form. This suggests that even though the map is very sensitive to the initial conditions, the average evolution of a given region, i.e. a random set of points drawn from the region, is conservative for a given parameter set.

[![Fig5_ellipse_2param_circ_evol_ab_changing](https://manasataramgini.files.wordpress.com/2018/03/fig5_ellipse_2param_circ_evol_ab_changing.png?w=640)](https://manasataramgini.files.wordpress.com/2018/03/fig5_ellipse_2param_circ_evol_ab_changing.png)Figure 5

In the next experiment (Figure 5) we try to understand the effect of the
![k_a,
k_b](https://s0.wp.com/latex.php?latex=k_a%2C+k_b&bg=ffffff&fg=333333&s=0&c=20201002) on the average evolution of a given “region”. However, we use a slightly variant definition of the region in this case: we chose 64 points on a circle of radius
![r=0.25](https://s0.wp.com/latex.php?latex=r%3D0.25&bg=ffffff&fg=333333&s=0&c=20201002)
each separated from the next by an angle of
![\\pi\\big/32](https://s0.wp.com/latex.php?latex=%5Cpi%5Cbig%2F32&bg=ffffff&fg=333333&s=0&c=20201002)
radians from 0 to
![2\\pi](https://s0.wp.com/latex.php?latex=2%5Cpi&bg=ffffff&fg=333333&s=0&c=20201002).
We then let these points evolve for 5000 iterations or until they explode to a singularity. The evolution of each point is plotted in a different color as above. For each row
![k_a](https://s0.wp.com/latex.php?latex=k_a&bg=ffffff&fg=333333&s=0&c=20201002)
is constant while
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
changes. For each column
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
is constant while
![k_a](https://s0.wp.com/latex.php?latex=k_a&bg=ffffff&fg=333333&s=0&c=20201002)
changes. The effect of increasing
![k_a](https://s0.wp.com/latex.php?latex=k_a&bg=ffffff&fg=333333&s=0&c=20201002)
is like that of a magnifier. Thus, the increasing
![k_a](https://s0.wp.com/latex.php?latex=k_a&bg=ffffff&fg=333333&s=0&c=20201002)
acts like zooming in on the structure of the interior of the map. The obvious effect of changing
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
is immediately apparent: with increasing
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
the eccentricity of the bounding ellipse of the map increases. As the bounding ellipse is of the form
![x^2+y^2-kxy=1](https://s0.wp.com/latex.php?latex=x%5E2%2By%5E2-kxy%3D1&bg=ffffff&fg=333333&s=0&c=20201002),
essentially
![k=k_b](https://s0.wp.com/latex.php?latex=k%3Dk_b&bg=ffffff&fg=333333&s=0&c=20201002).
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
also defines the internal structure of the map, such as its basic geometry as well as the zones of complete occupancy and the zones of exclusion. One notices these changing with changes in
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002).

[![Fig6A_ellipse_2param_circ_evol_a\_const.irr6](https://manasataramgini.files.wordpress.com/2018/03/fig6a_ellipse_2param_circ_evol_a_const-irr6.png?w=640)](https://manasataramgini.files.wordpress.com/2018/03/fig6a_ellipse_2param_circ_evol_a_const-irr6.png)Figure 6A.
![k_b=](https://s0.wp.com/latex.php?latex=k_b%3D&bg=ffffff&fg=333333&s=0&c=20201002)
0.61,
![\\tfrac{1}{\\phi}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7B1%7D%7B%5Cphi%7D&bg=ffffff&fg=333333&s=0&c=20201002),
.62, .99, 1, 1.01, 1.24,
![2\\cos\\left(\\tfrac{2\\pi}{7}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B7%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),
1.2475

This effect of the role of
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
on the internal structure is explored at greater depth in the several parts of Figure 6, which were essentially rendered by running the map as in Figure 5 with a constant
![k_a=0.618](https://s0.wp.com/latex.php?latex=k_a%3D0.618&bg=ffffff&fg=333333&s=0&c=20201002)
and various
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002).
Remarkably, at
![k_b=\\tfrac{1}{\\phi}](https://s0.wp.com/latex.php?latex=k_b%3D%5Ctfrac%7B1%7D%7B%5Cphi%7D&bg=ffffff&fg=333333&s=0&c=20201002),
where
![\\phi](https://s0.wp.com/latex.php?latex=%5Cphi&bg=ffffff&fg=333333&s=0&c=20201002)
is the Golden ratio, the map assumes a 10-rayed form with a tendency to diverge rapidly only along those rays (panel 2 of Figure 6A). This value is the ratio of the side of a regular pentagon to its diagonal. This
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
is the central value of the “pentad” state, i.e.
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
close to it on either side will show the characteristic pentad geometry as can be seen in panels 1 and 3 of Figure 6A. Similarly, we observe that
![k_b=1](https://s0.wp.com/latex.php?latex=k_b%3D1&bg=ffffff&fg=333333&s=0&c=20201002)
is the central value of the hexad state (panel 5 of Figure 6A). At values close to it on either side the map assumes a hexad form as can be seen in panels 4 and 5 of Figure 6A. Another central value is
![k_b=2\\cos\\left(\\tfrac{2\\pi}{7}\\right) \\approx
1.2469...](https://s0.wp.com/latex.php?latex=k_b%3D2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B7%7D%5Cright%29+%5Capprox+1.2469...&bg=ffffff&fg=333333&s=0&c=20201002). This number is derived from heptagonal equivalents of the Golden ratio: it is the ratio of the length of the larger diagonal to the smaller diagonal of a regular heptagon. Here again we see a radiating structure with 14 rays (panel 8 of Figure 6A). As
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
approaches this value we see the interior of the map assuming a heptad structure (panel 7 and 9, Figure 6A). These cases illustrate that for values close to the central value but less than it the map displays a
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)-ad
polygonal interior structure. For the values close to but greater than the central value the
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)-ad
interior structure assumes a rosette form with zones of exclusion defined by the rosette.

[![Fig6B_ellipse_2param_circ_evol_a\_const.irr7](https://manasataramgini.files.wordpress.com/2018/03/fig6b_ellipse_2param_circ_evol_a_const-irr7.png?w=640)](https://manasataramgini.files.wordpress.com/2018/03/fig6b_ellipse_2param_circ_evol_a_const-irr7.png)Figure 6B. where
![k_b=](https://s0.wp.com/latex.php?latex=k_b%3D&bg=ffffff&fg=333333&s=0&c=20201002)
1.4,
![\\sqrt{2}](https://s0.wp.com/latex.php?latex=%5Csqrt%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002),
1.53,
![2\\cos\\left(\\tfrac{2\\pi}{9}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B9%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),
1.61,
![\\phi](https://s0.wp.com/latex.php?latex=%5Cphi&bg=ffffff&fg=333333&s=0&c=20201002),
![2\\cos\\left(\\tfrac{2\\pi}{11}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B11%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),
1.73,
![\\sqrt{3}](https://s0.wp.com/latex.php?latex=%5Csqrt%7B3%7D&bg=ffffff&fg=333333&s=0&c=20201002)

Continuing this way, we can find further central values associated with higher
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)-ads.
At
![k_b=\\sqrt{2}](https://s0.wp.com/latex.php?latex=k_b%3D%5Csqrt%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002),
the map displays 8 rays (panel 2, Figure 6B). This corresponds to the ratio of the largest to the shortest diagonal of a regular octagon. As we approach this value we get a map with an octad structure (panel 1, Figure 6B). This is followed by the central point defined by
![k_b=2\\cos\\left(\\tfrac{2\\pi}{9}\\right)](https://s0.wp.com/latex.php?latex=k_b%3D2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B9%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),
which displays a map with 18 rays (panel 4, Figure 6B). This
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
corresponds to the ratio of the largest to the shortest diagonal of a regular nonagon. Thus, as we approach this value the map takes on a nonad structure (panel 3, Figure 6B). The next central value is
![k_b=\\phi](https://s0.wp.com/latex.php?latex=k_b%3D%5Cphi&bg=ffffff&fg=333333&s=0&c=20201002)
(panel 6, Figure 6B), which again results in a 10-rayed map and values
approaching it have a decad structure (panel 5, Figure 6B). The hendecad
(11-fold) central value is
![k_b=2\\cos\\left(\\tfrac{2\\pi}{11}\\right)](https://s0.wp.com/latex.php?latex=k_b%3D2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B11%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),
which results in a 22-rayed map (panel 7, Figure 6B). Similarly,
![k_b=\\sqrt{3}](https://s0.wp.com/latex.php?latex=k_b%3D%5Csqrt%7B3%7D&bg=ffffff&fg=333333&s=0&c=20201002)
is the central point for the dodecad structure (panels 8 and 9, Figure 6B). Studying these central values of
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002),
which mark the
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)-ad
geometry of the map, we can derive a general relationship between these
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
to the ratio of the diagonals of the corresponding regular
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)-sided
polygon thus: Given a vertex of the regular polygon with
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
sides, let
![d_1](https://s0.wp.com/latex.php?latex=d_1&bg=ffffff&fg=333333&s=0&c=20201002)
be the  
first side of the polygon emanating from that vertex. Then ![d_2, d_3, d_4,...d\_{n-2}](https://s0.wp.com/latex.php?latex=d_2%2C+d_3%2C+d_4%2C...d_%7Bn-2%7D&bg=ffffff&fg=333333&s=0&c=20201002) will be the successive diagonals and
![d\_{n-1}](https://s0.wp.com/latex.php?latex=d_%7Bn-1%7D&bg=ffffff&fg=333333&s=0&c=20201002)
will the second side emanating from that vertex. Then,

![k_b=\\dfrac{d_4}{d_2}](https://s0.wp.com/latex.php?latex=k_b%3D%5Cdfrac%7Bd_4%7D%7Bd_2%7D&bg=ffffff&fg=333333&s=0&c=20201002)

Using some trigonometry, we can show that for a
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)-sided
polygon with unit sides the length of the
![j](https://s0.wp.com/latex.php?latex=j&bg=ffffff&fg=333333&s=0&c=20201002)th
diagonal (including sides) connected to a given vertex is:

![d_j=\\dfrac{\\sin\\left(\\dfrac{j\\pi}{n}\\right)}{\\sin\\left(\\dfrac{\\pi}{n}\\right)}](https://s0.wp.com/latex.php?latex=d_j%3D%5Cdfrac%7B%5Csin%5Cleft%28%5Cdfrac%7Bj%5Cpi%7D%7Bn%7D%5Cright%29%7D%7B%5Csin%5Cleft%28%5Cdfrac%7B%5Cpi%7D%7Bn%7D%5Cright%29%7D&bg=ffffff&fg=333333&s=0&c=20201002)

![\\therefore k_b= \\dfrac{\\sin\\left(\\dfrac{4\\pi}{n}\\right)}{\\sin\\left(\\dfrac{\\pi}{n}\\right)} \\Bigg / \\dfrac{\\sin\\left(\\dfrac{2\\pi}{n}\\right)}{\\sin\\left(\\dfrac{\\pi}{n}\\right)}=\\dfrac{\\sin\\left(\\dfrac{4\\pi}{n}\\right)}{\\sin\\left(\\dfrac{2\\pi}{n}\\right)}=\\dfrac{2\\sin\\left(\\dfrac{2\\pi}{n}\\right)\\cos\\left(\\dfrac{2\\pi}{n}\\right)}{\\sin\\left(\\dfrac{2\\pi}{n}\\right)} =
2\\cos\\left(\\dfrac{2\\pi}{n}\\right)](https://s0.wp.com/latex.php?latex=%5Ctherefore+k_b%3D+%5Cdfrac%7B%5Csin%5Cleft%28%5Cdfrac%7B4%5Cpi%7D%7Bn%7D%5Cright%29%7D%7B%5Csin%5Cleft%28%5Cdfrac%7B%5Cpi%7D%7Bn%7D%5Cright%29%7D+%5CBigg+%2F+%5Cdfrac%7B%5Csin%5Cleft%28%5Cdfrac%7B2%5Cpi%7D%7Bn%7D%5Cright%29%7D%7B%5Csin%5Cleft%28%5Cdfrac%7B%5Cpi%7D%7Bn%7D%5Cright%29%7D%3D%5Cdfrac%7B%5Csin%5Cleft%28%5Cdfrac%7B4%5Cpi%7D%7Bn%7D%5Cright%29%7D%7B%5Csin%5Cleft%28%5Cdfrac%7B2%5Cpi%7D%7Bn%7D%5Cright%29%7D%3D%5Cdfrac%7B2%5Csin%5Cleft%28%5Cdfrac%7B2%5Cpi%7D%7Bn%7D%5Cright%29%5Ccos%5Cleft%28%5Cdfrac%7B2%5Cpi%7D%7Bn%7D%5Cright%29%7D%7B%5Csin%5Cleft%28%5Cdfrac%7B2%5Cpi%7D%7Bn%7D%5Cright%29%7D+%3D+2%5Ccos%5Cleft%28%5Cdfrac%7B2%5Cpi%7D%7Bn%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002)

This defines the
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
values at which the 2-parameter elliptical map will take a divergent form with
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)-rays
(if
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
is even) or
![2n](https://s0.wp.com/latex.php?latex=2n&bg=ffffff&fg=333333&s=0&c=20201002)-rays
(if
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
is odd). At values approaching these
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
it will show a pronounced
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)-ad
internal structure. This explains why the pentad is centered at
![\\tfrac{d_4}{d_2}=\\tfrac{1}{\\phi}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bd_4%7D%7Bd_2%7D%3D%5Ctfrac%7B1%7D%7B%5Cphi%7D&bg=ffffff&fg=333333&s=0&c=20201002)
where
![d_2=\\phi](https://s0.wp.com/latex.php?latex=d_2%3D%5Cphi&bg=ffffff&fg=333333&s=0&c=20201002)
and
![d_4=1](https://s0.wp.com/latex.php?latex=d_4%3D1&bg=ffffff&fg=333333&s=0&c=20201002)
for a unit pentagon. The tetrad has no
![d_4](https://s0.wp.com/latex.php?latex=d_4&bg=ffffff&fg=333333&s=0&c=20201002);
hence its central value would correspond to
![k_b=0](https://s0.wp.com/latex.php?latex=k_b%3D0&bg=ffffff&fg=333333&s=0&c=20201002):
that’s why we see the tetrad structure at
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
closer to zero (Figure 5). For
![n=12](https://s0.wp.com/latex.php?latex=n%3D12&bg=ffffff&fg=333333&s=0&c=20201002)
we already reach ![k_b=\\sqrt{3} \\approx 1.73205](https://s0.wp.com/latex.php?latex=k_b%3D%5Csqrt%7B3%7D+%5Capprox+1.73205&bg=ffffff&fg=333333&s=0&c=20201002). As
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
increases we have:

![\\displaystyle \\lim\_{n\\to\\infty} k_b= 2\\cos\\left(\\dfrac{2\\pi}{n}\\right)=2](https://s0.wp.com/latex.php?latex=%5Cdisplaystyle+%5Clim_%7Bn%5Cto%5Cinfty%7D+k_b%3D+2%5Ccos%5Cleft%28%5Cdfrac%7B2%5Cpi%7D%7Bn%7D%5Cright%29%3D2&bg=ffffff&fg=333333&s=0&c=20201002)

Thus, the higher
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)-ad
structures are closely clustered near 2. The derivation of the above formula for
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
enabled us to investigate other central points, where instead of integer
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
we have a rational number
![\\tfrac{p}{q}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bp%7D%7Bq%7D&bg=ffffff&fg=333333&s=0&c=20201002);
![p,q](https://s0.wp.com/latex.php?latex=p%2Cq&bg=ffffff&fg=333333&s=0&c=20201002)
being mutually prime. Thus we consider
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
of the form:

![k_b=2\\cos\\left(\\dfrac{2\\pi}{p/q}\\right)](https://s0.wp.com/latex.php?latex=k_b%3D2%5Ccos%5Cleft%28%5Cdfrac%7B2%5Cpi%7D%7Bp%2Fq%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002)

[![Fig7A_ellipse_2param_circ_evol_a\_const.irr9](https://manasataramgini.files.wordpress.com/2018/03/fig7a_ellipse_2param_circ_evol_a_const-irr9.png?w=640)](https://manasataramgini.files.wordpress.com/2018/03/fig7a_ellipse_2param_circ_evol_a_const-irr9.png)Figure 7A.
![k_b=](https://s0.wp.com/latex.php?latex=k_b%3D&bg=ffffff&fg=333333&s=0&c=20201002)
0.5165,
![2\\cos\\left(\\tfrac{2\\pi}{24/5}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B24%2F5%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),
0.5195, 0.8672,
![2\\cos\\left(\\tfrac{2\\pi}{28/5}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B28%2F5%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),
0.8683, 0.39,
![2\\cos\\left(\\tfrac{2\\pi}{32/7}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B32%2F7%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),
0.3911

The transition points associated with such rational values are explored in the various parts of Figure 7. In Figure 7A, we show the maps associated with ![\\tfrac{p}{q}= \\tfrac{24}{5}, \\tfrac{28}{5}, \\tfrac{32}{7}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bp%7D%7Bq%7D%3D+%5Ctfrac%7B24%7D%7B5%7D%2C+%5Ctfrac%7B28%7D%7B5%7D%2C+%5Ctfrac%7B32%7D%7B7%7D&bg=ffffff&fg=333333&s=0&c=20201002)
(panels 2, 5, 8). Each of these shows the
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)-rayed
structure typical of the the central points. Further, the number of rays corresponds to the value of
![p](https://s0.wp.com/latex.php?latex=p&bg=ffffff&fg=333333&s=0&c=20201002).
Again as in the case of the
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
corresponding to integer
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
as we approach the
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
corresponding to
![\\tfrac{p}{q}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bp%7D%7Bq%7D&bg=ffffff&fg=333333&s=0&c=20201002)
we get
![p](https://s0.wp.com/latex.php?latex=p&bg=ffffff&fg=333333&s=0&c=20201002)-ad
structures with a similar pattern as with the former. Here we have chosen 24, 28 and 32 (the syllable counts of the gāyatrī, uṣnik and anuṣṭubh meters).

[![Fig7B_ellipse_2param_circ_evol_a\_const.irr8](https://manasataramgini.files.wordpress.com/2018/03/fig7b_ellipse_2param_circ_evol_a_const-irr8.png?w=640)](https://manasataramgini.files.wordpress.com/2018/03/fig7b_ellipse_2param_circ_evol_a_const-irr8.png)Figure 7B.
![k_b=](https://s0.wp.com/latex.php?latex=k_b%3D&bg=ffffff&fg=333333&s=0&c=20201002)
![2\\cos\\left(\\tfrac{2\\pi}{7/2}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B7%2F2%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),
-0.44,
![2\\cos\\left(\\tfrac{2\\pi}{9/2}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B9%2F2%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),
0.342,
![2\\cos\\left(\\tfrac{2\\pi}{13/3}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B13%2F3%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),
0.24, -0.28,
![2\\cos\\left(\\tfrac{2\\pi}{11/3}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B11%2F3%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),
-0.2855

In figure 7B we explore further cases of
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
corresponding to different
![\\tfrac{p}{q}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bp%7D%7Bq%7D&bg=ffffff&fg=333333&s=0&c=20201002).
Notably, using these
![\\tfrac{p}{q}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bp%7D%7Bq%7D&bg=ffffff&fg=333333&s=0&c=20201002)
we get lower values of
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
at which we can get central points of hept-, hendec- and 13- ad structures. Interestingly, at some of these values
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
is negative (Figure 7B, panels 1,2 and 7,8,9). When
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
is negative, we see that the map becomes a mirror image of the positive
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002),
now being symmetric along the
![y=-x](https://s0.wp.com/latex.php?latex=y%3D-x&bg=ffffff&fg=333333&s=0&c=20201002)
line and maintaining an elliptical form between
![(-2,0)](https://s0.wp.com/latex.php?latex=%28-2%2C0%29&bg=ffffff&fg=333333&s=0&c=20201002).
A negative
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
is not quite meaningful in the original biological model in which the map was defined because it is a growth constant and positive. However, we could still contrive a definition wherein the negative
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
specifies a decaying population, which has a positive effect by reducing the parasite load, which is directly dependent on it, and thereby allowing relative growth.

[![Fig8_double_period](https://manasataramgini.files.wordpress.com/2018/03/fig8_double_period.png?w=640)](https://manasataramgini.files.wordpress.com/2018/03/fig8_double_period.png)Figure 8.
![k_b=](https://s0.wp.com/latex.php?latex=k_b%3D&bg=ffffff&fg=333333&s=0&c=20201002)
![2\\cos\\left(\\tfrac{2\\pi}{64/15}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B64%2F15%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),
![2\\cos\\left(\\tfrac{2\\pi}{128/31}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B128%2F31%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),
![2\\cos\\left(\\tfrac{2\\pi}{96/23}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B96%2F23%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),
![2\\cos\\left(\\tfrac{2\\pi}{100/23}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B100%2F23%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002)

In Figure 8 we explore the more complex effects of the fraction
![\\tfrac{p}{q}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bp%7D%7Bq%7D&bg=ffffff&fg=333333&s=0&c=20201002)
on the structure of the map. The outer structure of each of these maps respectively shows 64, 128, 96 and 100 rays as would be expected from value of
![p](https://s0.wp.com/latex.php?latex=p&bg=ffffff&fg=333333&s=0&c=20201002).
However, in the case of
![\\tfrac{64}{15}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7B64%7D%7B15%7D&bg=ffffff&fg=333333&s=0&c=20201002),
a closer look at the interior of the map reveals first a 17-ad and then closest to the center a tetrad structure (Figure 8, panel 1). Similarly, with
![\\tfrac{128}{31}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7B128%7D%7B31%7D&bg=ffffff&fg=333333&s=0&c=20201002)
we see an inner 33-ad and innermost tetrad structure (Figure 8, panel 2). For
![\\tfrac{96}{23}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7B96%7D%7B23%7D&bg=ffffff&fg=333333&s=0&c=20201002)
we likewise see a inward progression first to a 25-ad and then a tetrad structure (Figure 8, panel 3). For
![\\tfrac{100}{23}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7B100%7D%7B23%7D&bg=ffffff&fg=333333&s=0&c=20201002)
we see an inward progression to a 13-ad then tetrad structure. In each of these cases the innermost state is a tetrad. The corresponding value of
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
is: 0.1960, 0.0981 0.1308, 0.2506. In each case is much smaller than
![\\tfrac{1}{\\phi}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7B1%7D%7B%5Cphi%7D&bg=ffffff&fg=333333&s=0&c=20201002)
and closer to 0, which is the center of the tetrad state. Hence, it in each of these cases at the innermost level the effect of tetrad central value i.e. 0 dominates. Beyond that we see that
![k_b=0.1960](https://s0.wp.com/latex.php?latex=k_b%3D0.1960&bg=ffffff&fg=333333&s=0&c=20201002)
is close to
![2\\cos\\left(\\tfrac{2\\pi}{17/13}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B17%2F13%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),
thus resulting in the emergence of 17-ad structure in next level. Similarly for
![k_b=0.0981](https://s0.wp.com/latex.php?latex=k_b%3D0.0981&bg=ffffff&fg=333333&s=0&c=20201002),
we see that it is close to
![2\\cos\\left(\\tfrac{2\\pi}{33/25}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B33%2F25%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002)
which results in the 33-ad structure at the second level. It is notable that both ![\\tfrac{p}{q}=\\tfrac{64}{15}, \\tfrac{128}{31}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bp%7D%7Bq%7D%3D%5Ctfrac%7B64%7D%7B15%7D%2C+%5Ctfrac%7B128%7D%7B31%7D&bg=ffffff&fg=333333&s=0&c=20201002) have a comparable second layer
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)-ad
of the form
![\\tfrac{p}{4}+1](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bp%7D%7B4%7D%2B1&bg=ffffff&fg=333333&s=0&c=20201002).
Now in the case of
![k_b=0.1308](https://s0.wp.com/latex.php?latex=k_b%3D0.1308&bg=ffffff&fg=333333&s=0&c=20201002)
we have
![2\\cos\\left(\\tfrac{2\\pi}{25/19}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B25%2F19%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002)
close to it resulting a 25-ad second layer. Finally, with
![k_b=0.2506](https://s0.wp.com/latex.php?latex=k_b%3D0.2506&bg=ffffff&fg=333333&s=0&c=20201002)
we have
![2\\cos\\left(\\tfrac{2\\pi}{13/3}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7B13%2F3%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002)
near it resulting in a 13-ad second layer. Thus, the value of
![p](https://s0.wp.com/latex.php?latex=p&bg=ffffff&fg=333333&s=0&c=20201002)
in the fraction
![\\tfrac{p}{q}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bp%7D%7Bq%7D&bg=ffffff&fg=333333&s=0&c=20201002)
in the formula
![k_b=2\\cos\\left(\\tfrac{2\\pi}{p/q}\\right)](https://s0.wp.com/latex.php?latex=k_b%3D2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7Bp%2Fq%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002)
determines the general
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)-ad
structure of the map and actual value of
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
determined by the fraction
![\\tfrac{p}{q}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bp%7D%7Bq%7D&bg=ffffff&fg=333333&s=0&c=20201002)
determines its fine structure. In general terms, the resultant map at a certain
![\\tfrac{p}{q}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bp%7D%7Bq%7D&bg=ffffff&fg=333333&s=0&c=20201002)
may be viewed as a superposition of the corresponding
![p](https://s0.wp.com/latex.php?latex=p&bg=ffffff&fg=333333&s=0&c=20201002)-ad
structure in the outer layers with all the
![p](https://s0.wp.com/latex.php?latex=p&bg=ffffff&fg=333333&s=0&c=20201002)-s
of the nearby fractions competing to contribute to the inner layers. Thus, away from the strong central values, such as those from integer
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
we get more complex maps.

The lower
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
values at which we get higher
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)-ad
structures result in lower eccentricities of the bounding ellipse of the map. This allows us to visualize them better than at
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
values derived from integer
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
because the latter result in bounding ellipses with high eccentricity. The absolute value of
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
determines the eccentricity
![e_e](https://s0.wp.com/latex.php?latex=e_e&bg=ffffff&fg=333333&s=0&c=20201002)
of the bounding ellipse of the map: As ![\|k_b\| \\to 2, \\; e_e \\to 1](https://s0.wp.com/latex.php?latex=%7Ck_b%7C+%5Cto+2%2C+%5C%3B+e_e+%5Cto+1&bg=ffffff&fg=333333&s=0&c=20201002)
(the eccentricity of an ellipse
![0\<e_e\<1](https://s0.wp.com/latex.php?latex=0%3Ce_e%3C1&bg=ffffff&fg=333333&s=0&c=20201002);
at eccentricity 0 we get a circle and at eccentricity of 1 a parabola). We can derive the below formula giving the relationship between the the parameter
![\|k_b\|](https://s0.wp.com/latex.php?latex=%7Ck_b%7C&bg=ffffff&fg=333333&s=0&c=20201002)
and
![e_e](https://s0.wp.com/latex.php?latex=e_e&bg=ffffff&fg=333333&s=0&c=20201002).
For the bounding ellipse with
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
corresponding to the
![\\tfrac{p}{q}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bp%7D%7Bq%7D&bg=ffffff&fg=333333&s=0&c=20201002)
discussed above we can write the eccentricity thus:

![e_e=\\sqrt{1-\\tan^2\\left(\\dfrac{\\pi}{p/q}\\right)}](https://s0.wp.com/latex.php?latex=e_e%3D%5Csqrt%7B1-%5Ctan%5E2%5Cleft%28%5Cdfrac%7B%5Cpi%7D%7Bp%2Fq%7D%5Cright%29%7D&bg=ffffff&fg=333333&s=0&c=20201002)

By expressing
![\\tan^2\\left(\\tfrac{\\pi}{p/q}\\right)](https://s0.wp.com/latex.php?latex=%5Ctan%5E2%5Cleft%28%5Ctfrac%7B%5Cpi%7D%7Bp%2Fq%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002)
in terms of
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
using the above formula we derived for it and doing some trigonometric manipulations we get:

![e_e=\\sqrt{\\dfrac{2\|k_b\|}{\|k_b\|+2}}](https://s0.wp.com/latex.php?latex=e_e%3D%5Csqrt%7B%5Cdfrac%7B2%7Ck_b%7C%7D%7B%7Ck_b%7C%2B2%7D%7D&bg=ffffff&fg=333333&s=0&c=20201002)

Thus, one can see how only for
![\|k_b\|\<2](https://s0.wp.com/latex.php?latex=%7Ck_b%7C%3C2&bg=ffffff&fg=333333&s=0&c=20201002),
![e_e\<1](https://s0.wp.com/latex.php?latex=e_e%3C1&bg=ffffff&fg=333333&s=0&c=20201002)
and the map is elliptical.

In a final experiment we performed a Julia-like operation:
![k_a](https://s0.wp.com/latex.php?latex=k_a&bg=ffffff&fg=333333&s=0&c=20201002)
was kept constant and
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
was changed. The evolution was studied for all points separated from each other by 0.001 in the square defined by the diagonal
(-.2,-.2):(.2,.2). The points were allowed to evolve to a maximum of
5000 iterations if they did not crash to a singularity or reach an absolute value greater than (100,100). Each point in this square is colored by the number of iterations it survived on a color scale from black to gray via the colors dark blue, dark red, burlywood, coral, chartreuse, and cadet blue. Thus, the points that crash out after the first iteration are black and those that last all 5000 iterations are gray. Figure 9 shows the results of this run for selected
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)

[![Fig9_2param_Julia1](https://manasataramgini.files.wordpress.com/2018/03/fig9_2param_julia1.png?w=640)](https://manasataramgini.files.wordpress.com/2018/03/fig9_2param_julia1.png)Figure 9.
![k_a=-0.24](https://s0.wp.com/latex.php?latex=k_a%3D-0.24&bg=ffffff&fg=333333&s=0&c=20201002),
![k_b=](https://s0.wp.com/latex.php?latex=k_b%3D&bg=ffffff&fg=333333&s=0&c=20201002)
.25,
![2\\cos\\left(\\dfrac{2\\pi}{100/23}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Cdfrac%7B2%5Cpi%7D%7B100%2F23%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),
.26, .6,
![2\\cos\\left(\\dfrac{2\\pi}{5}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Cdfrac%7B2%5Cpi%7D%7B5%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),
0.62, 0.99,
![2\\cos\\left(\\dfrac{2\\pi}{5}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Cdfrac%7B2%5Cpi%7D%7B5%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),
.62, .99,
![2\\cos\\left(\\dfrac{2\\pi}{6}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Cdfrac%7B2%5Cpi%7D%7B6%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002),
1.05.

From this figure it becomes clear that beyond the basic symmetry axis along the
![y=x](https://s0.wp.com/latex.php?latex=y%3Dx&bg=ffffff&fg=333333&s=0&c=20201002)
line the plots are rather “entropic”, i.e. there is not much sign of order in arrangement of the points in terms of the number of iterations they survive. However, one tendency becomes clear, consistent with the actual structure of the maps plotted above: If
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
takes the form
![2\\cos\\left(\\tfrac{2\\pi}{n}\\right)](https://s0.wp.com/latex.php?latex=2%5Ccos%5Cleft%28%5Ctfrac%7B2%5Cpi%7D%7Bn%7D%5Cright%29&bg=ffffff&fg=333333&s=0&c=20201002)
with integer
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002),
like
![n=5,6](https://s0.wp.com/latex.php?latex=n%3D5%2C6&bg=ffffff&fg=333333&s=0&c=20201002)
(Figure 9, panel 5, 8) then the majority of points do not survive the
entire 5000 iterations — we see little gray. Thus, when
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
corresponds to
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
or fractions of the form
![\\tfrac{p}{q}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bp%7D%7Bq%7D&bg=ffffff&fg=333333&s=0&c=20201002)
with relatively small
![p](https://s0.wp.com/latex.php?latex=p&bg=ffffff&fg=333333&s=0&c=20201002)
then most points are not stable in their evolution and crash to a singularity or diverge rapidly. On the other hand, if
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
is defined by a
![\\tfrac{p}{q}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bp%7D%7Bq%7D&bg=ffffff&fg=333333&s=0&c=20201002)
with relatively large
![p](https://s0.wp.com/latex.php?latex=p&bg=ffffff&fg=333333&s=0&c=20201002)
(Figure 9, panel 2) or is not defined by a rational number in the
formula, then we get many more points evolving stably over a large number of iterations (the remaining panels of Figure 9) — here we see much more gray. The fraction of points surviving at least 5000 iterations is approximately half the total number of points (fraction ranges from 0.509 for Figure 8, panel 7 to 0.599 for panel 2). The remaining points bail out at fewer iterations in decaying fractions when grouped by bins of 100 from 100 to 4900 iterations (Figure 10). However,  
the mostly disordered distribution of these points, relates to the mostly convergent structure of the map for a given region that was illustrated above.

[![Fig10_ellipse_2param_julia_bins](https://manasataramgini.files.wordpress.com/2018/03/fig10_ellipse_2param_julia_bins.png?w=640)](https://manasataramgini.files.wordpress.com/2018/03/fig10_ellipse_2param_julia_bins.png)Figure 10. Histogram of bailout or survival till 5000 iterations with same parameters as in Figure 9.

In conclusion, while this simple map shows astounding visual beauty, interesting mathematical structure, and deep links to polygons and coprimality of numbers, one may ask if it provides any biological insights at all. At first sight it does seem like a rather unrealistic model for a biological system given the negative values of population that it generates. But perhaps even this can be remedied by the suggestion that these negative values are not absolute population sizes but only represent the part of a larger population which actually participates in the dynamics. But the key lessons the map provides for biological systems are of a more qualitative type: 1) On one hand it shows how systems even with just two species locked in biological conflict can show chaotic dynamics, where the long term out come is highly dependent on the initial conditions. Even small changes can push the system, for the same parameter set, from long-term stability to instability (defined as singularity or blowout divergence). 2) On the other hand, despite the above, it shows that, as an aggregate, a set of different initial conditions strongly tend to converge to dynamics of a constant form for a set of parameters. Thus, even if individual starting populations have very different fates, a population of populations tends to have predictable dynamics when taken as an aggregate. Such analogies might help understand the stable conflict despite ongoing arms races that have lasted for few billion years (e.g. between bacteria and their phages). 3) The high instability of certain points such the
![k_b](https://s0.wp.com/latex.php?latex=k_b&bg=ffffff&fg=333333&s=0&c=20201002)
corresponding to integer
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
and certain rational fractions suggests that the dynamics of the system might have some deep numerical constraints and natural selection might essentially have to play the role of selecting between parameters that conform to underlying numerical constraints that favor long terms stability.
