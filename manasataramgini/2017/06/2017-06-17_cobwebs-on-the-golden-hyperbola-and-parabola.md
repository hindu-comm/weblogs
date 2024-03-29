+++
title = "Cobwebs on the golden hyperbola and parabola"
date = "2017-06-17"
upstream_url = "https://manasataramgini.wordpress.com/2017/06/17/cobwebs-on-the-golden-hyperbola-and-parabola/"

+++
Source: [here](https://manasataramgini.wordpress.com/2017/06/17/cobwebs-on-the-golden-hyperbola-and-parabola/).

The material presented here is rather trivial to those who have spent even a small time looking at chaotic systems. Nevertheless, we found it instructive when we first discovered it for ourselves while studying conics. Hence, as part of recording such little tidbits of trivia that over the years have caught our eyes we are putting it down here.

Consider the iterative map,  
![x\_{n+1}=1+\\dfrac{1}{x_n}](https://s0.wp.com/latex.php?latex=x_%7Bn%2B1%7D%3D1%2B%5Cdfrac%7B1%7D%7Bx_n%7D&bg=ffffff&fg=333333&s=0&c=20201002)  
Notably, irrespective of what starting number
![x_n](https://s0.wp.com/latex.php?latex=x_n&bg=ffffff&fg=333333&s=0&c=20201002)
you take (with one exception) it converges to the Golden ratio
![\\phi=1.61803...](https://s0.wp.com/latex.php?latex=%5Cphi%3D1.61803...&bg=ffffff&fg=333333&s=0&c=20201002)
(Figure 1).

![golden_ratio_convergence](https://manasataramgini.files.wordpress.com/2017/06/golden_ratio_convergence.png?w=640)

Figure 1

The one exception is when
![x_0=-\\tfrac{1}{\\phi}](https://s0.wp.com/latex.php?latex=x_0%3D-%5Ctfrac%7B1%7D%7B%5Cphi%7D&bg=ffffff&fg=333333&s=0&c=20201002).
In this case it is rather obvious why it remains fixed at
![-\\tfrac{1}{\\phi}](https://s0.wp.com/latex.php?latex=-%5Ctfrac%7B1%7D%7B%5Cphi%7D&bg=ffffff&fg=333333&s=0&c=20201002).
However, notably, say you are very close to
![x_0=-\\tfrac{1}{\\phi}](https://s0.wp.com/latex.php?latex=x_0%3D-%5Ctfrac%7B1%7D%7B%5Cphi%7D&bg=ffffff&fg=333333&s=0&c=20201002),
e.g. -.61804, then you hover close to
![-\\tfrac{1}{\\phi}](https://s0.wp.com/latex.php?latex=-%5Ctfrac%7B1%7D%7B%5Cphi%7D&bg=ffffff&fg=333333&s=0&c=20201002)
for around 7 iterations and then drift away rapidly to converge to
![\\phi](https://s0.wp.com/latex.php?latex=%5Cphi&bg=ffffff&fg=333333&s=0&c=20201002)
quite rapidly. The rate of convergence measured as the number of iterations you take to converge within a certain range of
![\\phi](https://s0.wp.com/latex.php?latex=%5Cphi&bg=ffffff&fg=333333&s=0&c=20201002)
(say ![\\pm
10^{-7}](https://s0.wp.com/latex.php?latex=%5Cpm+10%5E%7B-7%7D&bg=ffffff&fg=333333&s=0&c=20201002) in below figure) shows an interesting pattern: for values closer and closer to
![-\\tfrac{1}{\\phi}](https://s0.wp.com/latex.php?latex=-%5Ctfrac%7B1%7D%7B%5Cphi%7D&bg=ffffff&fg=333333&s=0&c=20201002)
you take longer and longer to converge to
![\\phi](https://s0.wp.com/latex.php?latex=%5Cphi&bg=ffffff&fg=333333&s=0&c=20201002)
whereas values closer to
![\\phi](https://s0.wp.com/latex.php?latex=%5Cphi&bg=ffffff&fg=333333&s=0&c=20201002),
not surprisingly, converge faster. Thus, while
![\\phi](https://s0.wp.com/latex.php?latex=%5Cphi&bg=ffffff&fg=333333&s=0&c=20201002)
serves as the near universal attractor and
![-\\tfrac{1}{\\phi}](https://s0.wp.com/latex.php?latex=-%5Ctfrac%7B1%7D%7B%5Cphi%7D&bg=ffffff&fg=333333&s=0&c=20201002)
as the near universal repellor for this map, the repellor is actually weaker at repelling values that lie closer to it (Figure 2).

![Golden_Ratio_convergence3](https://manasataramgini.files.wordpress.com/2017/06/golden_ratio_convergence3.png?w=640)  
Figure 2

Rather dramatic jumps but still convergent behavior can be obtained at certain points: When ![x_0=0, -\\tfrac{1}{2}, -\\tfrac{3}{5}, -1](https://s0.wp.com/latex.php?latex=x_0%3D0%2C+-%5Ctfrac%7B1%7D%7B2%7D%2C+-%5Ctfrac%7B3%7D%7B5%7D%2C+-1&bg=ffffff&fg=333333&s=0&c=20201002) we jump between 0 and
![\\infty](https://s0.wp.com/latex.php?latex=%5Cinfty&bg=ffffff&fg=333333&s=0&c=20201002)
before moving towards convergence. This behavior can be studied in terms of the maximum value reached by
![x_n](https://s0.wp.com/latex.php?latex=x_n&bg=ffffff&fg=333333&s=0&c=20201002)
before convergence towards
![\\phi](https://s0.wp.com/latex.php?latex=%5Cphi&bg=ffffff&fg=333333&s=0&c=20201002).
The distribution of these values for various starting
![x_0](https://s0.wp.com/latex.php?latex=x_0&bg=ffffff&fg=333333&s=0&c=20201002)
shows a peculiar fractal structure with peaks of decreasing heights as one moves towards the repellor
![-\\tfrac{1}{\\phi}](https://s0.wp.com/latex.php?latex=-%5Ctfrac%7B1%7D%7B%5Cphi%7D&bg=ffffff&fg=333333&s=0&c=20201002)
from either direction (Figure 3).

![golden_ratio_convergence2](https://manasataramgini.files.wordpress.com/2017/06/golden_ratio_convergence2.png?w=640)  
Figure 3

So what it is the connection to conics alluded to above? One can see right away that the above map corresponds to the hyperbola,  
![y=1+\\dfrac{1}{x}](https://s0.wp.com/latex.php?latex=y%3D1%2B%5Cdfrac%7B1%7D%7Bx%7D&bg=ffffff&fg=333333&s=0&c=20201002)

The iterations of the map can be rendered geometrically as the famous cobweb diagram used by students of chaotic dynamics: Start with a curve and a point representing
![x_0](https://s0.wp.com/latex.php?latex=x_0&bg=ffffff&fg=333333&s=0&c=20201002)
on the x-y plane. Move along the vertical direction from that point till you hit the nearest point on the curve. Mark that segment. Then proceed in the horizontal direction till you hit a point on the line
![y=x](https://s0.wp.com/latex.php?latex=y%3Dx&bg=ffffff&fg=333333&s=0&c=20201002).
Mark that segment. Then move vertically again to hit the curve and so on. Repeat this procedure till you converge. When you do this procedure for the above hyperbola (Figure 4) then every point except one with x-coordinate
![-\\tfrac{1}{\\phi}](https://s0.wp.com/latex.php?latex=-%5Ctfrac%7B1%7D%7B%5Cphi%7D&bg=ffffff&fg=333333&s=0&c=20201002)
converges to the point ![(\\phi, \\phi)](https://s0.wp.com/latex.php?latex=%28%5Cphi%2C+%5Cphi%29&bg=ffffff&fg=333333&s=0&c=20201002), which is the attractor. The repellor is
![(-\\tfrac{1}{\\phi},-\\tfrac{1}{\\phi})](https://s0.wp.com/latex.php?latex=%28-%5Ctfrac%7B1%7D%7B%5Cphi%7D%2C-%5Ctfrac%7B1%7D%7B%5Cphi%7D%29&bg=ffffff&fg=333333&s=0&c=20201002).
One can see that these fixed points are intersects of the said hyperbola and the line
![y=x](https://s0.wp.com/latex.php?latex=y%3Dx&bg=ffffff&fg=333333&s=0&c=20201002)

![Cobwebs01](https://manasataramgini.files.wordpress.com/2017/06/cobwebs01.png?w=640)  
Figure 4

Now there exists a parabola with the same fixed points as the above hyperbola:  
![y=x^2-1](https://s0.wp.com/latex.php?latex=y%3Dx%5E2-1&bg=ffffff&fg=333333&s=0&c=20201002)

For this parabola, if a starting point for the cobweb diagram lies in the band delimited by the lines ![y=\\pm \\phi](https://s0.wp.com/latex.php?latex=y%3D%5Cpm+%5Cphi&bg=ffffff&fg=333333&s=0&c=20201002) then it moves towards
![-\\tfrac{1}{\\phi}](https://s0.wp.com/latex.php?latex=-%5Ctfrac%7B1%7D%7B%5Cphi%7D&bg=ffffff&fg=333333&s=0&c=20201002).
But it does not converge to that point. Instead it is eventually trapped in a four-point orbit: ![(0,0); (-1,0); (-1,-1);
(0,-1)](https://s0.wp.com/latex.php?latex=%280%2C0%29%3B+%28-1%2C0%29%3B+%28-1%2C-1%29%3B+%280%2C-1%29&bg=ffffff&fg=333333&s=0&c=20201002)
(Figure 5). If the starting point lies outside the above band then it
races away to
![\\infty](https://s0.wp.com/latex.php?latex=%5Cinfty&bg=ffffff&fg=333333&s=0&c=20201002).
But there are a some points where it actually converges to one of the fixed points. Any point whose x-coordinate is ![\\pm \\phi](https://s0.wp.com/latex.php?latex=%5Cpm+%5Cphi&bg=ffffff&fg=333333&s=0&c=20201002) converges to ![(\\phi, \\phi)](https://s0.wp.com/latex.php?latex=%28%5Cphi%2C+%5Cphi%29&bg=ffffff&fg=333333&s=0&c=20201002). Any point whose x-coordinate is ![\\pm \\sqrt{\\phi}](https://s0.wp.com/latex.php?latex=%5Cpm+%5Csqrt%7B%5Cphi%7D&bg=ffffff&fg=333333&s=0&c=20201002) or ![\\pm \\tfrac{1}{\\phi}](https://s0.wp.com/latex.php?latex=%5Cpm+%5Ctfrac%7B1%7D%7B%5Cphi%7D&bg=ffffff&fg=333333&s=0&c=20201002) converges to
![(-\\tfrac{1}{\\phi},-\\tfrac{1}{\\phi})](https://s0.wp.com/latex.php?latex=%28-%5Ctfrac%7B1%7D%7B%5Cphi%7D%2C-%5Ctfrac%7B1%7D%7B%5Cphi%7D%29&bg=ffffff&fg=333333&s=0&c=20201002).
The closer point’s x-coordinate is to one of the above values the greater the number of iterations it requires to be placed in the final four-point orbit. Thus, the parabola with the same fixed points as the said hyperbola displays a very different behavior — the outcomes are convergence to a fixed point, divergence to
![\\infty](https://s0.wp.com/latex.php?latex=%5Cinfty&bg=ffffff&fg=333333&s=0&c=20201002)
or eventually settling into a fixed orbit. However, for certain parabolas such as the logistic parabola, ![y=k x(1-x)](https://s0.wp.com/latex.php?latex=y%3Dk+x%281-x%29&bg=ffffff&fg=333333&s=0&c=20201002) we see the famous chaotic behavior for certain values of
![k](https://s0.wp.com/latex.php?latex=k&bg=ffffff&fg=333333&s=0&c=20201002).

![Cobwebs02](https://manasataramgini.files.wordpress.com/2017/06/cobwebs02.png?w=640)  
Figure 5
