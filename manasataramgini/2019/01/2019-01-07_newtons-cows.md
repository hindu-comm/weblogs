+++
title = "Newton’s cows"
date = "2019-01-07"
upstream_url = "https://manasataramgini.wordpress.com/2019/01/07/newtons-cows/"

+++
Source: [here](https://manasataramgini.wordpress.com/2019/01/07/newtons-cows/).

Cultures with an Indo-European background have had a long history of symbiosis with the bovine animal since they started herding on the steppes in the Black Sea-Caspian region. Indeed, the very emergence of the modern steppes of Eurasia is likely a result of human-animal action to foster a certain pattern and type of grass growth. Hence, not surprisingly, cows frequently appear even in their mathematical literature, like the Greek problem of cows attributed to Archimedes or Nārāyaṇa’s cow population problem. Even after the destruction of Indo-European tradition by Abrahamism in groups like the English such problems persisted and once such example is Newton’s problem from his
*Arithmetica universalis*. It goes thus:  
![a_1](https://s0.wp.com/latex.php?latex=a_1&bg=ffffff&fg=333333&s=0&c=20201002)
cows graze
![b_1](https://s0.wp.com/latex.php?latex=b_1&bg=ffffff&fg=333333&s=0&c=20201002)
fields bare in
![c_1](https://s0.wp.com/latex.php?latex=c_1&bg=ffffff&fg=333333&s=0&c=20201002)
days,  
![a_2](https://s0.wp.com/latex.php?latex=a_2&bg=ffffff&fg=333333&s=0&c=20201002)
cows graze
![b_2](https://s0.wp.com/latex.php?latex=b_2&bg=ffffff&fg=333333&s=0&c=20201002)
fields bare in
![c_2](https://s0.wp.com/latex.php?latex=c_2&bg=ffffff&fg=333333&s=0&c=20201002)
days,  
![a_3](https://s0.wp.com/latex.php?latex=a_3&bg=ffffff&fg=333333&s=0&c=20201002)
cows graze
![b_3](https://s0.wp.com/latex.php?latex=b_3&bg=ffffff&fg=333333&s=0&c=20201002)
fields bare in
![c_3](https://s0.wp.com/latex.php?latex=c_3&bg=ffffff&fg=333333&s=0&c=20201002)
days,  
What relationship exists between the 9 quantities from ![a_1, a_2, a_3...c_3](https://s0.wp.com/latex.php?latex=a_1%2C+a_2%2C+a_3...c_3&bg=ffffff&fg=333333&s=0&c=20201002)?

To solve this we must make some assumptions that Newton indicates in his work: 1) On an average the cows and fields are equivalent. That would mean that we can take each cow to eat the same amount
![w](https://s0.wp.com/latex.php?latex=w&bg=ffffff&fg=333333&s=0&c=20201002)
daily and each field to have the same type and amount of grass
![x](https://s0.wp.com/latex.php?latex=x&bg=ffffff&fg=333333&s=0&c=20201002).
Grass, ungulates and fungi are in a complex relationship. Grass “hire” fungal symbionts to produce toxins like the ergot alkaloids to deter ungulates. There is some empirical evidence that grazing by ungulates triggers grass growth. So we get the assumption: 2) The grass is not at standstill while being grazed daily but is growing back at a daily rate of
![y](https://s0.wp.com/latex.php?latex=y&bg=ffffff&fg=333333&s=0&c=20201002).

From the above, for the first set of cows and fields, we have
![b_1x](https://s0.wp.com/latex.php?latex=b_1x&bg=ffffff&fg=333333&s=0&c=20201002)
as the total amount of grass at the start of the grazing. The amount of grass growing on the field in day 1 would be ![b_1\\times 1 \\times y](https://s0.wp.com/latex.php?latex=b_1%5Ctimes+1+%5Ctimes+y&bg=ffffff&fg=333333&s=0&c=20201002). The total amount of grass eaten by the
![a_1](https://s0.wp.com/latex.php?latex=a_1&bg=ffffff&fg=333333&s=0&c=20201002)
cows at the end of the day would be ![a_1\\times 1 \\times w](https://s0.wp.com/latex.php?latex=a_1%5Ctimes+1+%5Ctimes+w&bg=ffffff&fg=333333&s=0&c=20201002). Thus, we can calculate the amount of grass at the end of day 1 as:
![b_1x +1b_1y -
1a_1w](https://s0.wp.com/latex.php?latex=b_1x+%2B1b_1y+-+1a_1w&bg=ffffff&fg=333333&s=0&c=20201002)  
At the end of day 2 we get:
![b_1x+2b_1y-2a_1w](https://s0.wp.com/latex.php?latex=b_1x%2B2b_1y-2a_1w&bg=ffffff&fg=333333&s=0&c=20201002)
and so on.  
Hence, when the fields are grazed bare in
![c_1](https://s0.wp.com/latex.php?latex=c_1&bg=ffffff&fg=333333&s=0&c=20201002)
days we get:
![b_1x+c_1b_1y-c_1a_1w=0](https://s0.wp.com/latex.php?latex=b_1x%2Bc_1b_1y-c_1a_1w%3D0&bg=ffffff&fg=333333&s=0&c=20201002).
By writing
![z=-w](https://s0.wp.com/latex.php?latex=z%3D-w&bg=ffffff&fg=333333&s=0&c=20201002)
we get the equation:
![b_1x+b_1c_1y+a_1c_1z=0](https://s0.wp.com/latex.php?latex=b_1x%2Bb_1c_1y%2Ba_1c_1z%3D0&bg=ffffff&fg=333333&s=0&c=20201002).
Similarly, for the other two sets of cows and fields we get the equations:
![b_2x+b_2c_2y+a_2c_2z=0](https://s0.wp.com/latex.php?latex=b_2x%2Bb_2c_2y%2Ba_2c_2z%3D0&bg=ffffff&fg=333333&s=0&c=20201002)
and
![b_3x+b_3c_3y+c_3a_3z=0](https://s0.wp.com/latex.php?latex=b_3x%2Bb_3c_3y%2Bc_3a_3z%3D0&bg=ffffff&fg=333333&s=0&c=20201002).
We thus have as set of 3 simultaneous equations in 3 variables:

![b_1x+b_1c_1y+a_1c_1z=0](https://s0.wp.com/latex.php?latex=b_1x%2Bb_1c_1y%2Ba_1c_1z%3D0&bg=ffffff&fg=333333&s=0&c=20201002)  
![b_2x+b_2c_2y+a_2c_2z=0](https://s0.wp.com/latex.php?latex=b_2x%2Bb_2c_2y%2Ba_2c_2z%3D0&bg=ffffff&fg=333333&s=0&c=20201002)  
![b_3x+b_3c_3y+c_3a_3z=0](https://s0.wp.com/latex.php?latex=b_3x%2Bb_3c_3y%2Bc_3a_3z%3D0&bg=ffffff&fg=333333&s=0&c=20201002)

We can hence eliminate ![x, y, z](https://s0.wp.com/latex.php?latex=x%2C+y%2C+z&bg=ffffff&fg=333333&s=0&c=20201002) using the determinant of the system ![\\det A= 0](https://s0.wp.com/latex.php?latex=%5Cdet+A%3D+0&bg=ffffff&fg=333333&s=0&c=20201002)

![\\det A = \\begin{vmatrix} b_1 & b_1c_1 & a_1c_1 \\\\ b_2 & b_2c_2 & a_2c_2 \\\\ b_3 & b_3c_3 & a_3c_3 \\end{vmatrix} =0](https://s0.wp.com/latex.php?latex=%5Cdet+A+%3D+%5Cbegin%7Bvmatrix%7D+b_1+%26+b_1c_1+%26+a_1c_1+%5C%5C++b_2+%26+b_2c_2+%26+a_2c_2+%5C%5C++b_3+%26+b_3c_3+%26++a_3c_3+%5Cend%7Bvmatrix%7D+%3D0&bg=ffffff&fg=333333&s=0&c=20201002)

If one wants to avoid ![\\det A=0](https://s0.wp.com/latex.php?latex=%5Cdet+A%3D0&bg=ffffff&fg=333333&s=0&c=20201002) being obtained for solutions: 1) where the amount of grass eaten by a cow is
![w=0](https://s0.wp.com/latex.php?latex=w%3D0&bg=ffffff&fg=333333&s=0&c=20201002);
2) negative values for
![y](https://s0.wp.com/latex.php?latex=y&bg=ffffff&fg=333333&s=0&c=20201002)
or
![w](https://s0.wp.com/latex.php?latex=w&bg=ffffff&fg=333333&s=0&c=20201002)
we have to set further constraints:  
![a_1, a_2,
a_3...c_3\>0](https://s0.wp.com/latex.php?latex=a_1%2C+a_2%2C+a_3...c_3%3E0&bg=ffffff&fg=333333&s=0&c=20201002)  
![c_2\>c_1](https://s0.wp.com/latex.php?latex=c_2%3Ec_1&bg=ffffff&fg=333333&s=0&c=20201002)  
![a_1b_2-a_2b_1\>0](https://s0.wp.com/latex.php?latex=a_1b_2-a_2b_1%3E0&bg=ffffff&fg=333333&s=0&c=20201002)  
![a_2b_1c_2-a_1b_2c_1\>0](https://s0.wp.com/latex.php?latex=a_2b_1c_2-a_1b_2c_1%3E0&bg=ffffff&fg=333333&s=0&c=20201002)

In Newton’s original numerical example the matrix of the 9 values is:

![\\begin{bmatrix} a_1 & b_1 & c_1 \\\\ a_2 & b_2 & c_2 \\\\ a_3 & b_3 & c_3 \\end{bmatrix} = \\begin{bmatrix} 36 & 10 & 12 \\\\ 63 & 30 & 27 \\\\ 162 & 108 & 54 \\end{bmatrix} ](https://s0.wp.com/latex.php?latex=%5Cbegin%7Bbmatrix%7D+a_1+%26+b_1+%26+c_1+%5C%5C++a_2+%26+b_2+%26+c_2+%5C%5C++a_3+%26+b_3+%26++c_3+%5Cend%7Bbmatrix%7D+%3D+%5Cbegin%7Bbmatrix%7D++36+%26++10+%26+12+%5C%5C+++63++%26+30+%26+27+%5C%5C++162+%26+108+%26+54+%5Cend%7Bbmatrix%7D+&bg=ffffff&fg=333333&s=0&c=20201002)

This yields:

![\\det A = \\begin{vmatrix} 10 & 120 & 432 \\\\ 30 & 810 & 1701 \\\\ 108 & 5832 &8748 \\end{vmatrix} =0](https://s0.wp.com/latex.php?latex=%5Cdet+A+%3D+%5Cbegin%7Bvmatrix%7D++10+%26++120+%26++432+%5C%5C+++30+%26+810+%26+1701+%5C%5C++108+%26+5832+%268748++%5Cend%7Bvmatrix%7D+%3D0&bg=ffffff&fg=333333&s=0&c=20201002)

There seems to have been a error in Newton’s original copy of this problem which he corrected late in his life. A question that comes to us is: Is there some easy algorithm for generating such valid integer nonads and is there some pattern to them?
