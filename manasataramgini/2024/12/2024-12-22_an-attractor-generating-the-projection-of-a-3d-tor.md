+++
title = "An attractor generating"
full_title = "An attractor generating the projection of a 3D torus on a plane"
upstream_url = "https://manasataramgini.wordpress.com/2024/12/22/an-attractor-generating-the-projection-of-a-3d-torus-on-a-plane/"
date = "2024-12-22"

+++
Source: [here](https://manasataramgini.wordpress.com/2024/12/22/an-attractor-generating-the-projection-of-a-3d-torus-on-a-plane/).

An attractor generating the projection of a 3D torus on a plane

The attractor in consideration was probably rediscovered by multiple explorers of chaotic maps in the early days of the computational exploration of such objects. We first discovered it in our 14th or 15th year when access to computers was just beginning to become a little easier in our regions. We are recording it here as part of an attempt to collate the story of our exploration. The generator of this attractor is a simple 4-parameter trigonometric map defined thus:  
![x\_{n+1}=d \\sin(a x_n) - \\sin(b y_n)](https://s0.wp.com/latex.php?latex=x_%7Bn%2B1%7D%3Dd+%5Csin%28a+x_n%29+-+%5Csin%28b+y_n%29&bg=ffffff&fg=333333&s=0&c=20201002)  
![y\_{n+1}=c \\cos(a x_n) + \\cos(b y_n)](https://s0.wp.com/latex.php?latex=y_%7Bn%2B1%7D%3Dc+%5Ccos%28a+x_n%29+%2B+%5Ccos%28b+y_n%29&bg=ffffff&fg=333333&s=0&c=20201002)

All attractors in this exploration were initiated with ![x_0=0.45, y_0=0.56](https://s0.wp.com/latex.php?latex=x_0%3D0.45%2C+y_0%3D0.56&bg=ffffff&fg=333333&s=0&c=20201002). The parameters ![c, d](https://s0.wp.com/latex.php?latex=c%2C+d&bg=ffffff&fg=333333&s=0&c=20201002) have similar effects on the shape of the attractor; hence, we hold ![d=-1](https://s0.wp.com/latex.php?latex=d%3D-1&bg=ffffff&fg=333333&s=0&c=20201002) and vary ![c](https://s0.wp.com/latex.php?latex=c&bg=ffffff&fg=333333&s=0&c=20201002). At lower absolute values of ![a, b](https://s0.wp.com/latex.php?latex=a%2C+b&bg=ffffff&fg=333333&s=0&c=20201002), approximately ![-3.5 \\le a \\le 3.5](https://s0.wp.com/latex.php?latex=-3.5+%5Cle+a+%5Cle+3.5&bg=ffffff&fg=333333&s=0&c=20201002) and ![-2.85 \\le b \\le 2.85](https://s0.wp.com/latex.php?latex=-2.85+%5Cle+b+%5Cle+2.85&bg=ffffff&fg=333333&s=0&c=20201002), we tend to get a variety of strange attractors, which we do not consider further in this note. Thus, we fix ![a=3.5](https://s0.wp.com/latex.php?latex=a%3D3.5&bg=ffffff&fg=333333&s=0&c=20201002) and ![b=2.85](https://s0.wp.com/latex.php?latex=b%3D2.85&bg=ffffff&fg=333333&s=0&c=20201002) for the below runs. Interestingly, while ![0 \\le c \\le 1](https://s0.wp.com/latex.php?latex=0+%5Cle+c+%5Cle+1&bg=ffffff&fg=333333&s=0&c=20201002), we find that the attractor takes the form of the projection of a 3D torus on the XY plane. The surface of the torus shows some “painting” of structure determined by ![a, b](https://s0.wp.com/latex.php?latex=a%2C+b&bg=ffffff&fg=333333&s=0&c=20201002).

[![sven01](https://manasataramgini.wordpress.com/wp-content/uploads/2024/12/sven01.png)](https://manasataramgini.wordpress.com/wp-content/uploads/2024/12/sven01.png)Figure 1. Attractors for ![0 \\le c \\le 1](https://s0.wp.com/latex.php?latex=0+%5Cle+c+%5Cle+1&bg=ffffff&fg=333333&s=0&c=20201002)

A torus is a surface defined by the parametric equations (Figure 2):  
![x= (R+r \\cos(v)) \\cos(u)](https://s0.wp.com/latex.php?latex=x%3D+%28R%2Br+%5Ccos%28v%29%29+%5Ccos%28u%29&bg=ffffff&fg=333333&s=0&c=20201002),  
![y= (R+r \\cos(v)) \\sin(u),](https://s0.wp.com/latex.php?latex=y%3D+%28R%2Br+%5Ccos%28v%29%29+%5Csin%28u%29%2C&bg=ffffff&fg=333333&s=0&c=20201002)  
![z= r\\sin(v)](https://s0.wp.com/latex.php?latex=z%3D+r%5Csin%28v%29&bg=ffffff&fg=333333&s=0&c=20201002),  
where ![R](https://s0.wp.com/latex.php?latex=R&bg=ffffff&fg=333333&s=0&c=20201002) is the major radius (the distance from the center of the tube to the center of the torus) and ![r](https://s0.wp.com/latex.php?latex=r&bg=ffffff&fg=333333&s=0&c=20201002) is the minor radius (the radius of the tube).

<div class="tiled-gallery type-rectangular tiled-gallery-unresized" carousel-extra="{&quot;blog_id&quot;:2579045,&quot;permalink&quot;:&quot;https:\/\/manasataramgini.wordpress.com\/2024\/12\/22\/an-attractor-generating-the-projection-of-a-3d-torus-on-a-plane\/&quot;,&quot;likes_blog_id&quot;:2579045}" original-width="640" itemscope="" itemtype="http://schema.org/ImageGallery">

<div class="gallery-row" original-height="283" original-width="640" style="width: 640px; height: 283px;">

<div class="gallery-group images-1" original-height="283" original-width="326" style="width: 326px; height: 283px;">

<div class="tiled-gallery-item tiled-gallery-item-large" itemprop="associatedMedia" itemscope="" itemtype="http://schema.org/ImageObject">

[](https://manasataramgini.wordpress.com/2024/12/22/an-attractor-generating-the-projection-of-a-3d-torus-on-a-plane/torus1/)

![Torus1](https://i0.wp.com/manasataramgini.wordpress.com/wp-content/uploads/2024/12/torus1.jpeg?w=322&h=279&ssl=1 "Torus1")

</div>

</div>

<div class="gallery-group images-1" original-height="283" original-width="314" style="width: 314px; height: 283px;">

<div class="tiled-gallery-item tiled-gallery-item-large" itemprop="associatedMedia" itemscope="" itemtype="http://schema.org/ImageObject">

[](https://manasataramgini.wordpress.com/2024/12/22/an-attractor-generating-the-projection-of-a-3d-torus-on-a-plane/torus2/)

![torus2](https://i0.wp.com/manasataramgini.wordpress.com/wp-content/uploads/2024/12/torus2.jpeg?w=310&h=279&ssl=1 "torus2")

</div>

</div>

</div>

</div>

Figure 2. Tori with ![R=r](https://s0.wp.com/latex.php?latex=R%3Dr&bg=ffffff&fg=333333&s=0&c=20201002) and ![R=2r](https://s0.wp.com/latex.php?latex=R%3D2r&bg=ffffff&fg=333333&s=0&c=20201002)

With regard to the above map, we observe that it is the projection of the torus with ![R=r](https://s0.wp.com/latex.php?latex=R%3Dr&bg=ffffff&fg=333333&s=0&c=20201002) on the XY plane. Further, we observe that the projection represents the rotation of the “horizontal” plane of the torus with the X-axis as the axis of rotation. One can establish that the angle of rotation is ![\\theta = \\arcsin(c)](https://s0.wp.com/latex.php?latex=%5Ctheta+%3D+%5Carcsin%28c%29&bg=ffffff&fg=333333&s=0&c=20201002); thus, at ![c=0, \\theta=0](https://s0.wp.com/latex.php?latex=c%3D0%2C+%5Ctheta%3D0&bg=ffffff&fg=333333&s=0&c=20201002) the torus is projected “side-on” and at ![c=1, \\theta=\\tfrac{\\pi}{2}](https://s0.wp.com/latex.php?latex=c%3D1%2C+%5Ctheta%3D%5Ctfrac%7B%5Cpi%7D%7B2%7D&bg=ffffff&fg=333333&s=0&c=20201002) it is projected face-on. More generally, whenever the ![\|d\| = \|c\|](https://s0.wp.com/latex.php?latex=%7Cd%7C+%3D+%7Cc%7C&bg=ffffff&fg=333333&s=0&c=20201002), the attractor always takes the form of a torus projected face-on with ![R=\|c\|=\|d\|, r=1](https://s0.wp.com/latex.php?latex=R%3D%7Cc%7C%3D%7Cd%7C%2C+r%3D1&bg=ffffff&fg=333333&s=0&c=20201002) (Figure 3).

[![torus3](https://manasataramgini.wordpress.com/wp-content/uploads/2024/12/torus3.jpeg)](https://manasataramgini.wordpress.com/wp-content/uploads/2024/12/torus3.jpeg)Figure 3. Face-on projection of torus.

When ![d=-1](https://s0.wp.com/latex.php?latex=d%3D-1&bg=ffffff&fg=333333&s=0&c=20201002) and ![c\>1](https://s0.wp.com/latex.php?latex=c%3E1&bg=ffffff&fg=333333&s=0&c=20201002), the attractor takes the form of the planar projection of a torus with ![R= \|c\|, r=1](https://s0.wp.com/latex.php?latex=R%3D+%7Cc%7C%2C+r%3D1&bg=ffffff&fg=333333&s=0&c=20201002). This torus is oriented such that its axis of rotation is the Y-axis (passing through the body of the torus rather than the aperture as above). It is rotated such that the projection of the outer edge of the tube touches the projection of the inner edge of the tube directly opposite to it (Figure 4). As a non-mathematician, the open question to us is how exactly one converts this 2D map into an actual 3D map whose attractor sits on a torus, thereby explaining the cause of its form.

![sven02](https://manasataramgini.wordpress.com/wp-content/uploads/2024/12/sven02.png)Figure 4. Attractors for ![c \\ge 1](https://s0.wp.com/latex.php?latex=c+%5Cge+1&bg=ffffff&fg=333333&s=0&c=20201002)
