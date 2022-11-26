+++
title = "A catalog of attractors,"
full_title = "A catalog of attractors, repellors, cycles, and other oscillations of some common functional iterates"
date = "2022-10-03"
upstream_url = "https://manasataramgini.wordpress.com/2022/10/03/a-catalog-of-attractors-repellors-cycles-and-other-oscillations-of-some-common-functional-iterates/"

+++
Source: [here](https://manasataramgini.wordpress.com/2022/10/03/a-catalog-of-attractors-repellors-cycles-and-other-oscillations-of-some-common-functional-iterates/).

A catalog of attractors, repellors, cycles, and other oscillations of some common functional iterates

One of the reasons we became interested in functional iterates was from seeking an analogy for the effect of selective pressure on the mean values of a measurable biological trait in a population. Let us consider a biological trait under selection to have a mean value of ![x_n](https://s0.wp.com/latex.php?latex=x_n&bg=ffffff&fg=333333&s=0&c=20201002) at a given point in time in a population. Under the selective pressure acting on it, in the next generation, it will become ![x\_{n+1}](https://s0.wp.com/latex.php?latex=x_%7Bn%2B1%7D&bg=ffffff&fg=333333&s=0&c=20201002). Thus, the selective pressure can be conceived as a function that brings about the transformation ![x\_{n+1} = f(x_n)](https://s0.wp.com/latex.php?latex=x_%7Bn%2B1%7D+%3D+f%28x_n%29&bg=ffffff&fg=333333&s=0&c=20201002). Thus, iterating this function with its prior value with give us the trajectory of the measure of the said trait in the population. While it might be difficult to establish the exact function ![f](https://s0.wp.com/latex.php?latex=f&bg=ffffff&fg=333333&s=0&c=20201002) for a real-life biological trait under selection, we can imagine it as being any common function for a simplistic analogical model. This led us to the geometric representation of the process — the cobweb diagram.

[![FP_fig1_cobweb1](https://manasataramgini.files.wordpress.com/2022/10/fp_fig1_cobweb1.png?w=640)](https://manasataramgini.files.wordpress.com/2022/10/fp_fig1_cobweb1.png)*Figure 1. Cobweb diagram for the functional iterates of ![f(x)=\tfrac{1+x}{2+x^2}](https://s0.wp.com/latex.php?latex=f%28x%29%3D%5Ctfrac%7B1%2Bx%7D%7B2%2Bx%5E2%7D&bg=ffffff&fg=333333&s=0&c=20201002)*

For example, let us take the function acting on ![x_n](https://s0.wp.com/latex.php?latex=x_n&bg=ffffff&fg=333333&s=0&c=20201002) to be ![f(x)=\tfrac{1+x}{2+x^2}](https://s0.wp.com/latex.php?latex=f%28x%29%3D%5Ctfrac%7B1%2Bx%7D%7B2%2Bx%5E2%7D&bg=ffffff&fg=333333&s=0&c=20201002) (Figure 1). We can see that the iterative application of this function on any starting ![x_0](https://s0.wp.com/latex.php?latex=x_0&bg=ffffff&fg=333333&s=0&c=20201002) (point B in Figure 1) eventually leads to convergence to a fixed point that can be determined by obtaining the intersection between ![f(x)](https://s0.wp.com/latex.php?latex=f%28x%29&bg=ffffff&fg=333333&s=0&c=20201002) and the line ![y=x](https://s0.wp.com/latex.php?latex=y%3Dx&bg=ffffff&fg=333333&s=0&c=20201002). In this case, one can prove that it will be 0.6823278…, the only real root of the equation ![x^3+x-1=0](https://s0.wp.com/latex.php?latex=x%5E3%2Bx-1%3D0&bg=ffffff&fg=333333&s=0&c=20201002). Thus, 0.6823278… can be described as the attracting fixed point or attractor of this functional iteration.

[![FP_Fig2_cobweb2](https://manasataramgini.files.wordpress.com/2022/10/fp_fig2_cobweb2.png?w=534&h=500)](https://manasataramgini.files.wordpress.com/2022/10/fp_fig2_cobweb2.png)

*Figure 2. Cobweb diagram for the functional iterates of ![f(x)=\tfrac{1}{x}-x](https://s0.wp.com/latex.php?latex=f%28x%29%3D%5Ctfrac%7B1%7D%7Bx%7D-x&bg=ffffff&fg=333333&s=0&c=20201002)*

Instead, consider the same process under the function ![f(x)=\tfrac{1}{x}-x](https://s0.wp.com/latex.php?latex=f%28x%29%3D%5Ctfrac%7B1%7D%7Bx%7D-x&bg=ffffff&fg=333333&s=0&c=20201002) (Figure 2). Here, we can show that there would be two points that emerge as a result of the intersection between ![f(x)](https://s0.wp.com/latex.php?latex=f%28x%29&bg=ffffff&fg=333333&s=0&c=20201002) and ![y=x](https://s0.wp.com/latex.php?latex=y%3Dx&bg=ffffff&fg=333333&s=0&c=20201002): the two roots of the equation ![2x^2-1=0](https://s0.wp.com/latex.php?latex=2x%5E2-1%3D0&bg=ffffff&fg=333333&s=0&c=20201002), ![\pm \tfrac{1}{\sqrt{2}}](https://s0.wp.com/latex.php?latex=%5Cpm+%5Ctfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D&bg=ffffff&fg=333333&s=0&c=20201002). These two points draw the iterates towards themselves but the competition between them results in the outcome being chaos unless ![x_0](https://s0.wp.com/latex.php?latex=x_0&bg=ffffff&fg=333333&s=0&c=20201002) is exactly at one of them. Thus, these two fixed points can be described as repelling fixed points or repellors. Thus, exploring different simple functions, we realized that there can be three possible broad outcomes for functional iterates: (1) Convergence to an attractor; (2) Convergence to a cyclic attractor, where the endpoint is to cycle between 2 or more fixed points; (3) Chaotic oscillations driven by repellors. Hence, we conjectured that even in the evolutionary process under selection we will see these three outcomes. Convergence to an attractor is commonly observed when populations starting with different mean values of the trait are driven by selection to a similar endpoint. The cycle is less common but might be seen in situations like the coexistence of different morphs of males and females, each with a distinct mating strategy, e.g., in beetles, damselflies and lizards. Finally, the absence of convergence but chaotic wandering of the trait is less-appreciated but we believe is also manifested in nature. We shall see below that there are different forms of chaos and each of them might have rather different consequences.

One can find some of the fixed points or other consequences of functional iteration in certain mathematical volumes or online resources. However, we did not find any of those to be comprehensive enough for easy reference. Hence, we thought it would be useful to provide such a catalog covering a subset of the common functions we have explored. We provide these by stating the function and the consequence of the iteration (attractors, cycles or chaos with associated repellors), followed by comments in some cases. We omit trivial cases like ![\sin(x)](https://s0.wp.com/latex.php?latex=%5Csin%28x%29&bg=ffffff&fg=333333&s=0&c=20201002), which shows a gradual convergence to 0. The gradual convergence in cases like this is related to their limit as ![x\to 0](https://s0.wp.com/latex.php?latex=x%5Cto+0&bg=ffffff&fg=333333&s=0&c=20201002); e.g., ![\lim\_{x \to 0} \tfrac{\sin(x)}{x} =1](https://s0.wp.com/latex.php?latex=%5Clim_%7Bx+%5Cto+0%7D+%5Ctfrac%7B%5Csin%28x%29%7D%7Bx%7D+%3D1&bg=ffffff&fg=333333&s=0&c=20201002). In the below catalog, ![\phi](https://s0.wp.com/latex.php?latex=%5Cphi&bg=ffffff&fg=333333&s=0&c=20201002) denotes the Golden Ratio and ![\phi'](https://s0.wp.com/latex.php?latex=%5Cphi%27&bg=ffffff&fg=333333&s=0&c=20201002) its reciprocal.

\(1\) Simple algebraic functions. Here the attractors or repellors can be easily determined by solving the polynomial equations defined by the difference equation specifying the map.  
![\sqrt{1+\|x\|}](https://s0.wp.com/latex.php?latex=%5Csqrt%7B1%2B%7Cx%7C%7D&bg=ffffff&fg=333333&s=0&c=20201002): ![\phi](https://s0.wp.com/latex.php?latex=%5Cphi&bg=ffffff&fg=333333&s=0&c=20201002)

![1+\dfrac{1}{x}](https://s0.wp.com/latex.php?latex=1%2B%5Cdfrac%7B1%7D%7Bx%7D&bg=ffffff&fg=333333&s=0&c=20201002): ![\phi](https://s0.wp.com/latex.php?latex=%5Cphi&bg=ffffff&fg=333333&s=0&c=20201002); This attractor also extends to the complex plane. For more discussion of this system see [our earlier note](https://manasataramgini.wordpress.com/2017/06/17/cobwebs-on-the-golden-hyperbola-and-parabola/).

![2+\dfrac{1}{x}](https://s0.wp.com/latex.php?latex=2%2B%5Cdfrac%7B1%7D%7Bx%7D&bg=ffffff&fg=333333&s=0&c=20201002): ![1+\sqrt{2}](https://s0.wp.com/latex.php?latex=1%2B%5Csqrt%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002); This attractor also extends to the complex plane.

![1+\dfrac{1}{2x}](https://s0.wp.com/latex.php?latex=1%2B%5Cdfrac%7B1%7D%7B2x%7D&bg=ffffff&fg=333333&s=0&c=20201002): ![\dfrac{1+\sqrt{3}}{2}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7B1%2B%5Csqrt%7B3%7D%7D%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002)

![2+\dfrac{1}{2x}](https://s0.wp.com/latex.php?latex=2%2B%5Cdfrac%7B1%7D%7B2x%7D&bg=ffffff&fg=333333&s=0&c=20201002): ![1+\sqrt{\frac{3}{2}}](https://s0.wp.com/latex.php?latex=1%2B%5Csqrt%7B%5Cfrac%7B3%7D%7B2%7D%7D&bg=ffffff&fg=333333&s=0&c=20201002)

![\dfrac{1+x}{2+x}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7B1%2Bx%7D%7B2%2Bx%7D&bg=ffffff&fg=333333&s=0&c=20201002): ![\phi'](https://s0.wp.com/latex.php?latex=%5Cphi%27&bg=ffffff&fg=333333&s=0&c=20201002)

*[![FP3_algebraic_map](https://manasataramgini.files.wordpress.com/2022/10/fp3_algebraic_map.png?w=640)](https://manasataramgini.files.wordpress.com/2022/10/fp3_algebraic_map.png)Figure 3. Chaotic functional iterates of some simple algebraic functions*

![\dfrac{1}{x}-x](https://s0.wp.com/latex.php?latex=%5Cdfrac%7B1%7D%7Bx%7D-x&bg=ffffff&fg=333333&s=0&c=20201002): symmetric sawtooth chaos: ![\phi, \phi'](https://s0.wp.com/latex.php?latex=%5Cphi%2C+%5Cphi%27&bg=ffffff&fg=333333&s=0&c=20201002) are repellors.

![x-\dfrac{1}{x}](https://s0.wp.com/latex.php?latex=x-%5Cdfrac%7B1%7D%7Bx%7D&bg=ffffff&fg=333333&s=0&c=20201002): sawtooth chaos: ![\phi, \phi'](https://s0.wp.com/latex.php?latex=%5Cphi%2C+%5Cphi%27&bg=ffffff&fg=333333&s=0&c=20201002) are repellors.

The two above systems (Figure 3, first two panels) show chaotic behavior with a peculiar pattern. In the first one, there are rapid oscillations giving an overall symmetric appearance. In the second one, there is a sharp rise to the local peak or valley followed by a slower, convex return towards 0. The profiles of these maps have a tooth-like appearance, though the first is constituted by oscillations fitting into a similar profile as the second.

![2x^2-1](https://s0.wp.com/latex.php?latex=2x%5E2-1&bg=ffffff&fg=333333&s=0&c=20201002) (Chebyshev 2): chaotic (-1,1)

![4x^3 -3x](https://s0.wp.com/latex.php?latex=4x%5E3+-3x&bg=ffffff&fg=333333&s=0&c=20201002) (Chebyshev 3): chaotic (-1,1)

These next two functions are the Chebyshev polynomials 2 and 3, which show chaotic behavior if ![x_0](https://s0.wp.com/latex.php?latex=x_0&bg=ffffff&fg=333333&s=0&c=20201002) lies in the interval (-1,1). At -1,1 they remain stationary and beyond those they diverge. Despite the chaos, the values of the iterates show a characteristic U-shaped distribution, with the highest density close to the boundaries, -1, 1, and low densities throughout the middle of the interval (Figure 4). This type of distribution is typical of many chaotic iterates of polynomial functions, e.g., the famous logistic map.

[![FP4_cheb3_hist](https://manasataramgini.files.wordpress.com/2022/10/fp4_cheb3_hist.png?w=640)](https://manasataramgini.files.wordpress.com/2022/10/fp4_cheb3_hist.png)*Figure 4. Distribution of the functional iterates of ![4x^3 -3x](https://s0.wp.com/latex.php?latex=4x%5E3+-3x&bg=ffffff&fg=333333&s=0&c=20201002)*

\(2\) Circular trigonometric functions

[![FP5_cos_complex](https://manasataramgini.files.wordpress.com/2022/10/fp5_cos_complex.png?w=640)](https://manasataramgini.files.wordpress.com/2022/10/fp5_cos_complex.png)*Figure 5. Number of iterations to convergence or divergence to ![\infty](https://s0.wp.com/latex.php?latex=%5Cinfty&bg=ffffff&fg=333333&s=0&c=20201002) of iterates of ![\cos(x)](https://s0.wp.com/latex.php?latex=%5Ccos%28x%29&bg=ffffff&fg=333333&s=0&c=20201002)*

![\cos(x)](https://s0.wp.com/latex.php?latex=%5Ccos%28x%29&bg=ffffff&fg=333333&s=0&c=20201002): 0.73908513321516 (the solution of the equation ![x=\cos(x)](https://s0.wp.com/latex.php?latex=x%3D%5Ccos%28x%29&bg=ffffff&fg=333333&s=0&c=20201002)) is the attractor for all real values. On the complex plane, other than those values in the white region (Figure 5), all values within a fractal boundary converge at different rates (indicated by coloring) to the same attractor.

[![FP6_tan_map](https://manasataramgini.files.wordpress.com/2022/10/fp6_tan_map.png?w=640)](https://manasataramgini.files.wordpress.com/2022/10/fp6_tan_map.png)

*Figure 6. Iterates of ![\tan(x)](https://s0.wp.com/latex.php?latex=%5Ctan%28x%29&bg=ffffff&fg=333333&s=0&c=20201002) from different starting points.*

![\tan(x)](https://s0.wp.com/latex.php?latex=%5Ctan%28x%29&bg=ffffff&fg=333333&s=0&c=20201002): chaotic (Figure 6). The oscillations are generally of low amplitude but are punctuated by rare “explosions” of huge amplitude (hence, shown in ![\mathrm{arcsinh}](https://s0.wp.com/latex.php?latex=%5Cmathrm%7Barcsinh%7D&bg=ffffff&fg=333333&s=0&c=20201002) scale in the figure). See our [earlier note](https://manasataramgini.wordpress.com/2019/08/27/chaos-eruptions-and-root-convergence-in-one-dimensional-maps-based-on-metallic-sequence-generating-functions/) on functions with comparable behavior. Such behavior is analogous to what have been termed Levy flights.

![\sin(2x)](https://s0.wp.com/latex.php?latex=%5Csin%282x%29&bg=ffffff&fg=333333&s=0&c=20201002): 0.94774713351699

![FP7_cos2x_hist](https://manasataramgini.files.wordpress.com/2022/10/fp7_cos2x_hist.png?w=640)*Figure 7. Distribution of the functional iterates of ![\cos(2x)](https://s0.wp.com/latex.php?latex=%5Ccos%282x%29&bg=ffffff&fg=333333&s=0&c=20201002)*

![\cos(2x)](https://s0.wp.com/latex.php?latex=%5Ccos%282x%29&bg=ffffff&fg=333333&s=0&c=20201002): chaotic. The iterates are contained in the interval ![(-1,1)](https://s0.wp.com/latex.php?latex=%28-1%2C1%29&bg=ffffff&fg=333333&s=0&c=20201002) with certain exclusion zones. The most prominent exclusion zone contains the primary repellor 0.514933264661… (solution of the equation ![x=\cos(2x)](https://s0.wp.com/latex.php?latex=x%3D%5Ccos%282x%29&bg=ffffff&fg=333333&s=0&c=20201002); red point in Figure 7).In the negative part of real line, the exclusion begins at ![\cos(2)](https://s0.wp.com/latex.php?latex=%5Ccos%282%29&bg=ffffff&fg=333333&s=0&c=20201002) (purple point in Figure 7). The points of the other exclusions zones (black points) are more mysterious.

![\tan(2x)](https://s0.wp.com/latex.php?latex=%5Ctan%282x%29&bg=ffffff&fg=333333&s=0&c=20201002): chaotic

![\sin(x)-\cos(x)](https://s0.wp.com/latex.php?latex=%5Csin%28x%29-%5Ccos%28x%29&bg=ffffff&fg=333333&s=0&c=20201002): -1.25872817749268

![\sin(x)+\cos(x)](https://s0.wp.com/latex.php?latex=%5Csin%28x%29%2B%5Ccos%28x%29&bg=ffffff&fg=333333&s=0&c=20201002): 1.2587281774927

![\cos(x)-\sin(x)](https://s0.wp.com/latex.php?latex=%5Ccos%28x%29-%5Csin%28x%29&bg=ffffff&fg=333333&s=0&c=20201002): bicycle: -0.83019851706782, 1.41279458572762; These attractors are also valid in the complex plane.

[![FP8_secx](https://manasataramgini.files.wordpress.com/2022/10/fp8_secx.png?w=640)](https://manasataramgini.files.wordpress.com/2022/10/fp8_secx.png)  
*Figure 8. Functional iterates of 160801 starting points of ![\sec(x)](https://s0.wp.com/latex.php?latex=%5Csec%28x%29&bg=ffffff&fg=333333&s=0&c=20201002) in the complex plane*

![\sec(x)](https://s0.wp.com/latex.php?latex=%5Csec%28x%29&bg=ffffff&fg=333333&s=0&c=20201002): chaotic for both real and complex values. Interestingly, in the complex plane, the iterates show certain preferred regions of density that are symmetric about the real axis (Figure 8). The centers of these regions of density appear to be close to the multiple of ![\pi](https://s0.wp.com/latex.php?latex=%5Cpi&bg=ffffff&fg=333333&s=0&c=20201002) Figure 8; red points).

![\cot(x)](https://s0.wp.com/latex.php?latex=%5Ccot%28x%29&bg=ffffff&fg=333333&s=0&c=20201002): While it is chaotic on the real line, on the complex plane it converges to either ![\pm 1.1996786402577i](https://s0.wp.com/latex.php?latex=%5Cpm+1.1996786402577i&bg=ffffff&fg=333333&s=0&c=20201002) depending on the initial point.

![\csc(x)](https://s0.wp.com/latex.php?latex=%5Ccsc%28x%29&bg=ffffff&fg=333333&s=0&c=20201002): 1.1141571408719

[![FP9_cossquared](https://manasataramgini.files.wordpress.com/2022/10/fp9_cossquared.png?w=640)](https://manasataramgini.files.wordpress.com/2022/10/fp9_cossquared.png)*Figure 9. Regions of convergence or divergence to ![\infty](https://s0.wp.com/latex.php?latex=%5Cinfty&bg=ffffff&fg=333333&s=0&c=20201002) of iterates of ![\cos^2(x)](https://s0.wp.com/latex.php?latex=%5Ccos%5E2%28x%29&bg=ffffff&fg=333333&s=0&c=20201002). The light-yellow regions converge to the attractor indicated as a blue point*

![\cos^2(x)](https://s0.wp.com/latex.php?latex=%5Ccos%5E2%28x%29&bg=ffffff&fg=333333&s=0&c=20201002): 0.6417143708 is the attractor for real starting points. In the complex plane all initial points withing the fractal boundary converge to the same attractor while the rest diverge (Figure 9).

[![FP10_cscsquaredx](https://manasataramgini.files.wordpress.com/2022/10/fp10_cscsquaredx.png?w=640)](https://manasataramgini.files.wordpress.com/2022/10/fp10_cscsquaredx.png)*Figure 10. Regions of convergence of iterates of ![\csc^2(x)](https://s0.wp.com/latex.php?latex=%5Ccsc%5E2%28x%29&bg=ffffff&fg=333333&s=0&c=20201002) or divergence to ![\infty](https://s0.wp.com/latex.php?latex=%5Cinfty&bg=ffffff&fg=333333&s=0&c=20201002). The light yellow regions converge to the attractor indicated as a blue point*

![\csc^2(x)](https://s0.wp.com/latex.php?latex=%5Ccsc%5E2%28x%29&bg=ffffff&fg=333333&s=0&c=20201002): 1.17479617129 is the attractor for real starting points. In the complex plane all initial points withing the fractal boundary converge to the same attractor while the rest diverge (Figure 10).

![\sec^2(x)](https://s0.wp.com/latex.php?latex=%5Csec%5E2%28x%29&bg=ffffff&fg=333333&s=0&c=20201002): chaotic

*[![FP11_xbytanx](https://manasataramgini.files.wordpress.com/2022/10/fp11_xbytanx.png?w=640)](https://manasataramgini.files.wordpress.com/2022/10/fp11_xbytanx.png)Figure 11. Number of iterations of function ![\tfrac{x}{\tan(x)}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bx%7D%7B%5Ctan%28x%29%7D&bg=ffffff&fg=333333&s=0&c=20201002) for convergence or divergence to ![\infty](https://s0.wp.com/latex.php?latex=%5Cinfty&bg=ffffff&fg=333333&s=0&c=20201002)*

![\dfrac{x}{\tan(x)}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7Bx%7D%7B%5Ctan%28x%29%7D&bg=ffffff&fg=333333&s=0&c=20201002): The attractor on the real line is ![\dfrac{\pi}{4}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7B%5Cpi%7D%7B4%7D&bg=ffffff&fg=333333&s=0&c=20201002). On the complex plane, the points within a fractal boundary (Figure 11) converge to the same point at different rates (the contours in Figure 11).

![\sin(\cos(x))](https://s0.wp.com/latex.php?latex=%5Csin%28%5Ccos%28x%29%29&bg=ffffff&fg=333333&s=0&c=20201002): 0.69481969073079

![\tan(\sin(x))](https://s0.wp.com/latex.php?latex=%5Ctan%28%5Csin%28x%29%29&bg=ffffff&fg=333333&s=0&c=20201002): 1.5570858155247

![\sin(\tan(x))](https://s0.wp.com/latex.php?latex=%5Csin%28%5Ctan%28x%29%29&bg=ffffff&fg=333333&s=0&c=20201002): -0.99990601241267

![\sin(\sec(x))](https://s0.wp.com/latex.php?latex=%5Csin%28%5Csec%28x%29%29&bg=ffffff&fg=333333&s=0&c=20201002): 0.97678326638014

![\cos(\sec(x))](https://s0.wp.com/latex.php?latex=%5Ccos%28%5Csec%28x%29%29&bg=ffffff&fg=333333&s=0&c=20201002): 0.44604767999913 (root of the equation ![\cos(x)= \tfrac{1}{\arccos(x)}](https://s0.wp.com/latex.php?latex=%5Ccos%28x%29%3D+%5Ctfrac%7B1%7D%7B%5Carccos%28x%29%7D&bg=ffffff&fg=333333&s=0&c=20201002)) it the attractor both on the real line and the complex plane.

![\sin(\csc(x))](https://s0.wp.com/latex.php?latex=%5Csin%28%5Ccsc%28x%29%29&bg=ffffff&fg=333333&s=0&c=20201002): ![\pm 0.94403906661161](https://s0.wp.com/latex.php?latex=%5Cpm+0.94403906661161&bg=ffffff&fg=333333&s=0&c=20201002) is the attractor both of the real line and the complex plane depending on the starting point defined by (root of the equation ![\sin(x)= \tfrac{1}{\arcsin(x)}](https://s0.wp.com/latex.php?latex=%5Csin%28x%29%3D+%5Ctfrac%7B1%7D%7B%5Carcsin%28x%29%7D&bg=ffffff&fg=333333&s=0&c=20201002)

![\tan(\cos(x))](https://s0.wp.com/latex.php?latex=%5Ctan%28%5Ccos%28x%29%29&bg=ffffff&fg=333333&s=0&c=20201002): bicycle: 0.013710961966803, 1.55708579436399; These values are remarkably close to but not identical to the solution of the equation ![\arccos(x)= \tan(\cos(x))](https://s0.wp.com/latex.php?latex=%5Carccos%28x%29%3D+%5Ctan%28%5Ccos%28x%29%29&bg=ffffff&fg=333333&s=0&c=20201002), i.e., ![r=0.01371006057](https://s0.wp.com/latex.php?latex=r%3D0.01371006057&bg=ffffff&fg=333333&s=0&c=20201002) and ![\arccos(r)=\tan(\cos(r))=1.55708583668](https://s0.wp.com/latex.php?latex=%5Carccos%28r%29%3D%5Ctan%28%5Ccos%28r%29%29%3D1.55708583668&bg=ffffff&fg=333333&s=0&c=20201002). Thus, the sum of these two values is close to ![\tfrac{pi}{2}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bpi%7D%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002).

![\cos(\tan(x))](https://s0.wp.com/latex.php?latex=%5Ccos%28%5Ctan%28x%29%29&bg=ffffff&fg=333333&s=0&c=20201002): bicycle: 0.013710102886935, 0.999906006233481; These values are remarkably close to but not identical to the solution of the equation ![\arccos(x)= \cos(\tan(x))](https://s0.wp.com/latex.php?latex=%5Carccos%28x%29%3D+%5Ccos%28%5Ctan%28x%29%29&bg=ffffff&fg=333333&s=0&c=20201002), i.e., ![r=0.999906018592](https://s0.wp.com/latex.php?latex=r%3D0.999906018592&bg=ffffff&fg=333333&s=0&c=20201002) and ![\arccos(r)=\cos(\tan(r))=0.01371006057](https://s0.wp.com/latex.php?latex=%5Carccos%28r%29%3D%5Ccos%28%5Ctan%28r%29%29%3D0.01371006057&bg=ffffff&fg=333333&s=0&c=20201002).

![\cos(\csc(x))](https://s0.wp.com/latex.php?latex=%5Ccos%28%5Ccsc%28x%29%29&bg=ffffff&fg=333333&s=0&c=20201002): octocycle: 0.366798375086067, -0.938273127439933, 0.324922488718667, -0.999958528842272, 0.373119965761099, -0.921730305866654, 0.310327826505175, -0.991153343837468; this cycle appears to be associated with oscillations close to ![r=\arcsin(\tfrac{1}{\pi})=\mathrm{arccsc}(\pi)=0.323946106932](https://s0.wp.com/latex.php?latex=r%3D%5Carcsin%28%5Ctfrac%7B1%7D%7B%5Cpi%7D%29%3D%5Cmathrm%7Barccsc%7D%28%5Cpi%29%3D0.323946106932&bg=ffffff&fg=333333&s=0&c=20201002) and ![\cos(\csc(r))=-1](https://s0.wp.com/latex.php?latex=%5Ccos%28%5Ccsc%28r%29%29%3D-1&bg=ffffff&fg=333333&s=0&c=20201002)

\(3\) Hyperbolic trigonometric functions  
![\coth(x)](https://s0.wp.com/latex.php?latex=%5Ccoth%28x%29&bg=ffffff&fg=333333&s=0&c=20201002): converges to either ![\pm 1.19967864026](https://s0.wp.com/latex.php?latex=%5Cpm+1.19967864026&bg=ffffff&fg=333333&s=0&c=20201002) (solutions of the equation ![x= coth(x)](https://s0.wp.com/latex.php?latex=x%3D+coth%28x%29&bg=ffffff&fg=333333&s=0&c=20201002)) depending on the starting point.

![\mathrm{sech}(x)](https://s0.wp.com/latex.php?latex=%5Cmathrm%7Bsech%7D%28x%29&bg=ffffff&fg=333333&s=0&c=20201002): 0.7650100

![\dfrac{1}{\mathrm{arcsinh}(x)}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7B1%7D%7B%5Cmathrm%7Barcsinh%7D%28x%29%7D&bg=ffffff&fg=333333&s=0&c=20201002): ![\pm 1.07293831517215](https://s0.wp.com/latex.php?latex=%5Cpm+1.07293831517215&bg=ffffff&fg=333333&s=0&c=20201002) depending on the starting point.

\(4\) Exponential functions  
![e^{-x}](https://s0.wp.com/latex.php?latex=e%5E%7B-x%7D&bg=ffffff&fg=333333&s=0&c=20201002): 0.5671433; remarkably this is ![\mathrm{W}(1)](https://s0.wp.com/latex.php?latex=%5Cmathrm%7BW%7D%281%29&bg=ffffff&fg=333333&s=0&c=20201002), where ![\mathrm{W}(x)](https://s0.wp.com/latex.php?latex=%5Cmathrm%7BW%7D%28x%29&bg=ffffff&fg=333333&s=0&c=20201002) is the function discovered by the polymath Johann Heinrich Lambert, in the 1700s. This value can be computed using the below definite integral:

![k= \displaystyle\int\_{-\pi}^{\pi}\log\left(1+\dfrac{\sin(x)}{x}e^{\tfrac{x}{\tan(x)}}\right) dx](https://s0.wp.com/latex.php?latex=k%3D+%5Cdisplaystyle%5Cint_%7B-%5Cpi%7D%5E%7B%5Cpi%7D%5Clog%5Cleft%281%2B%5Cdfrac%7B%5Csin%28x%29%7D%7Bx%7De%5E%7B%5Ctfrac%7Bx%7D%7B%5Ctan%28x%29%7D%7D%5Cright%29+dx&bg=ffffff&fg=333333&s=0&c=20201002)

Then the fixed point of the exponential function, ![\textrm{F}(e^{-x})=\dfrac{k}{2\pi} \approx 0.5671433 \cdots ](https://s0.wp.com/latex.php?latex=%5Ctextrm%7BF%7D%28e%5E%7B-x%7D%29%3D%5Cdfrac%7Bk%7D%7B2%5Cpi%7D+%5Capprox+0.5671433+%5Ccdots+&bg=ffffff&fg=333333&s=0&c=20201002)latex

[![FP12_expdecay_complex](https://manasataramgini.files.wordpress.com/2022/10/fp12_expdecay_complex.png?w=640)](https://manasataramgini.files.wordpress.com/2022/10/fp12_expdecay_complex.png)*Figure 12. Number of iterations for convergence of functional iterates of ![e^{-x}](https://s0.wp.com/latex.php?latex=e%5E%7B-x%7D&bg=ffffff&fg=333333&s=0&c=20201002) or divergence to ![\infty](https://s0.wp.com/latex.php?latex=%5Cinfty&bg=ffffff&fg=333333&s=0&c=20201002)*

In the complex plane, all points within the fractal boundary (Figure 12) converge to the same attractor at different rates or diverge to ![\infty](https://s0.wp.com/latex.php?latex=%5Cinfty&bg=ffffff&fg=333333&s=0&c=20201002) (white regions).

![2^{-x}](https://s0.wp.com/latex.php?latex=2%5E%7B-x%7D&bg=ffffff&fg=333333&s=0&c=20201002): 0.64118574450499; comparable behavior as above in the complex plane. The closed form for this fixed point can be derived from the Lambert function: ![\textrm{W}(x)](https://s0.wp.com/latex.php?latex=%5Ctextrm%7BW%7D%28x%29&bg=ffffff&fg=333333&s=0&c=20201002):

![\displaystyle \textrm{W}(x)=\dfrac{1}{2\pi}\int\_{-\pi}^{\pi}\log\left(1+\frac{x\sin\left(t\right)}{t}e^{\frac{t}{\tan\left(t\right)}}\right)dt](https://s0.wp.com/latex.php?latex=%5Cdisplaystyle+%5Ctextrm%7BW%7D%28x%29%3D%5Cdfrac%7B1%7D%7B2%5Cpi%7D%5Cint_%7B-%5Cpi%7D%5E%7B%5Cpi%7D%5Clog%5Cleft%281%2B%5Cfrac%7Bx%5Csin%5Cleft%28t%5Cright%29%7D%7Bt%7De%5E%7B%5Cfrac%7Bt%7D%7B%5Ctan%5Cleft%28t%5Cright%29%7D%7D%5Cright%29dt&bg=ffffff&fg=333333&s=0&c=20201002)

Then the ![\textrm{FP}(2^{-x})= e^{-\textrm{W}(\log(2))}](https://s0.wp.com/latex.php?latex=%5Ctextrm%7BFP%7D%282%5E%7B-x%7D%29%3D+e%5E%7B-%5Ctextrm%7BW%7D%28%5Clog%282%29%29%7D&bg=ffffff&fg=333333&s=0&c=20201002)

![e^{-\tan(x)}](https://s0.wp.com/latex.php?latex=e%5E%7B-%5Ctan%28x%29%7D&bg=ffffff&fg=333333&s=0&c=20201002): 0.54522571736464

[![FP13_gaussian](https://manasataramgini.files.wordpress.com/2022/10/fp13_gaussian.png?w=640)](https://manasataramgini.files.wordpress.com/2022/10/fp13_gaussian.png)*Figure 13. Number of iterations for convergence of functional iterates of ![e^{-x^2}](https://s0.wp.com/latex.php?latex=e%5E%7B-x%5E2%7D&bg=ffffff&fg=333333&s=0&c=20201002) or divergence to ![\infty](https://s0.wp.com/latex.php?latex=%5Cinfty&bg=ffffff&fg=333333&s=0&c=20201002)*

![e^{-x^2}](https://s0.wp.com/latex.php?latex=e%5E%7B-x%5E2%7D&bg=ffffff&fg=333333&s=0&c=20201002): the attractor 0.652918640419 is the solution to the equation ![x^2+\log(x)=0](https://s0.wp.com/latex.php?latex=x%5E2%2B%5Clog%28x%29%3D0&bg=ffffff&fg=333333&s=0&c=20201002). We can again find a closed form for this fixed point using ![\textrm{W}(x)](https://s0.wp.com/latex.php?latex=%5Ctextrm%7BW%7D%28x%29&bg=ffffff&fg=333333&s=0&c=20201002):

![\textrm{FP}(e^{-x^2})= e^{-\frac{\textrm{W}(2)}{2}}](https://s0.wp.com/latex.php?latex=%5Ctextrm%7BFP%7D%28e%5E%7B-x%5E2%7D%29%3D+e%5E%7B-%5Cfrac%7B%5Ctextrm%7BW%7D%282%29%7D%7B2%7D%7D&bg=ffffff&fg=333333&s=0&c=20201002)

In the complex plane, all points within the fractal boundary (Figure 13) converge to the same attractor at different rates or diverge to ![\infty](https://s0.wp.com/latex.php?latex=%5Cinfty&bg=ffffff&fg=333333&s=0&c=20201002) (white regions). It is interesting to see that one of the convergence contours recapitulates the curve ![y=e^{-x^2}](https://s0.wp.com/latex.php?latex=y%3De%5E%7B-x%5E2%7D&bg=ffffff&fg=333333&s=0&c=20201002) reflected about the real axis (Figure 13).

![\dfrac{1}{e^x-x}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7B1%7D%7Be%5Ex-x%7D&bg=ffffff&fg=333333&s=0&c=20201002): 0.7384324007018

![\dfrac{1}{(e^x-x)^2}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7B1%7D%7B%28e%5Ex-x%29%5E2%7D&bg=ffffff&fg=333333&s=0&c=20201002): 0.63654121332649

[![FP14_1bylogofxsquared_complex](https://manasataramgini.files.wordpress.com/2022/10/fp14_1bylogofxsquared_complex.png?w=640)](https://manasataramgini.files.wordpress.com/2022/10/fp14_1bylogofxsquared_complex.png)*Figure 14. Number of iterations for convergence of functional iterates of ![\tfrac{1}{\log(x^2)}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7B1%7D%7B%5Clog%28x%5E2%29%7D&bg=ffffff&fg=333333&s=0&c=20201002)*

![\dfrac{1}{\log(x^2)}](https://s0.wp.com/latex.php?latex=%5Cdfrac%7B1%7D%7B%5Clog%28x%5E2%29%7D&bg=ffffff&fg=333333&s=0&c=20201002): This function is interesting in that it is chaotic on the real line with a repellor at 1.4215299358831… As the iterates approach 1 from below they are prone to negative explosions; if they do so from above, they undergo a positive explosion. The distribution of the iterates shows a preponderance of small values but when extreme values occur they are very large (explosions). Interestingly, in the complex plane, it converges to -0.32447650840966+0.31470495550992i (Figure 14). The number of iterations to convergence reveals a fractal pattern of interlocking circles.

While the fixed points can be determined by numerical solving the equations specifying them, the closed forms, if any, remain unknown for many of them. Finding if they exist would be a good exercise for the mathematically minded.
