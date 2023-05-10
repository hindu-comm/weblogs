+++
title = "Waves of stationary"
full_title = "Waves of stationary shape"
date = "2009-05-23"
upstream_url = "https://www.gnxp.com/WordPress/2009/05/23/waves-of-stationary-shape/"

+++
Source: [here](https://www.gnxp.com/WordPress/2009/05/23/waves-of-stationary-shape/).

Waves of stationary shape

NOTE: I had a couple typos in my equations in the original. This is updated and fixed, and hopefully totally correct. Thanks to bioIgnoramous for pointing it out.

Over at [Scienceblogs](http://www.scienceblogs.com/), people are talking about waves. Of course, everyone thinks that waves are in the domain of physics, and people always forget about one of my favorite subjects: waves of advance. Way back in the day, RA Fisher wondered what might happen if genes had to spread not just locally but across space, and he published his findings in a landmark article called [The Wave of Advance of Advantageous Genes](http://digital.library.adelaide.edu.au/dspace/handle/2440/15125). This paper was not just important for its contributions to population genetics, but because of fundamental contributions to applied mathematics. As far as I can tell, Fisher and the great mathematician Kolmogorov published similar findings on this same subject in the same year. To that end, these kinds of waves of advance are often referred to as “Fisherian” waves.

What was Fisher’s model, what did he find, and how has it been extended?

Fisher assumed (without much justification) that genes should diffuse through a population, much like dye diffusing through a glass of water. In addition, at each point the dynamics would be affected by natural selection. This led Fisher to writing down a partial differential equation:

Where p is the frequency of the advantageous allele, t is time, and x is space. The parameter sigma^2 is the varaiance in the parent-offspring distance, and s is the selective advantage of one allele over the other. He then assumed that the solution had the form of a wave of stationary shape, and was able to derive a necessary condition on the velocity, namely that the velocity is at least

This showed that even though a gene can sweep through a local population relatively quickly, e.g. \~900 generations to go from a frequency of of .01 to .99 with a selective advantage of 1%, it will take a while for it to spread spatially. That same gene will take an additional 250 generations to fix, say, 50 meters away, assuming parent-offspring variance of 2 meters^2 per unit time. An interesting observation, at least.

But what’s particularly interesting are some extensions of this work. One of the major extensions comes when the “reaction” term is changed to something just a little bit more complex:

Where the p with the triangle on it, called “p-hat” by those in the know, is an internal equilibrium. What kind of biology might be relevant to this situation? Well, that equation is one way of expressing the famous allee effect in ecology, which describes populations who have lowered growth rates both when the population is large (too much competition, for example) and when it is small (it’s hard to find a mate). In evolution, it was thought that that equation could describe the phenomenon of hybrid zones. In another landmark paper, NH Barton described [The Dynamics of Hybrid Zones](http://www.nature.com/hdy/journal/v43/n3/abs/hdy197987a.html) (unfortunately not open access). Now, to be quite honest, I have no idea what Barton is doing in this paper—he’s using methods from physics that I’m not really familiar with. Nonetheless, he proved that if the internal equilibrium is too large, specifically if p-hat is bigger than 1/2, then the wave of advance stops dead in its tracks. It can also be stopped by steep changes in population density, among other things. This result is pretty cool: it seemed to explain why some hybrid zones moved, and why some hybrid zones stayed in their placee.

Unfortuantely, hybrid zones probably AREN’T described by the simple dynamics above. But we can use that simple equation to learn a lot of stuff about them, nonetheless!

### Related Posts:

- [Fisher's Wave of Advance & Hybrid
  Zones](https://www.gnxp.com/WordPress/2009/05/24/fishers-wave-of-advance-hybrid-zones/) - [The Neandertal Genome &
  Us](https://www.gnxp.com/WordPress/2010/05/06/the-neandertal-genome-us/) - [Culture and wave of
  advance](https://www.gnxp.com/WordPress/2007/05/18/culture-and-wave-of-advance/) - [Pots, people &
  seeds](https://www.gnxp.com/WordPress/2009/08/30/pots-people-seeds/) - [Agriculture &
  Europe](https://www.gnxp.com/WordPress/2007/10/01/agriculture-europe/) - [Daily Data Dump -
  Wednesday](https://www.gnxp.com/WordPress/2010/10/13/daily-data-dump-wednesday-22/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F05%2F23%2Fwaves-of-stationary-shape%2F&linkname=Waves%20of%20stationary%20shape "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F05%2F23%2Fwaves-of-stationary-shape%2F&linkname=Waves%20of%20stationary%20shape "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F05%2F23%2Fwaves-of-stationary-shape%2F&linkname=Waves%20of%20stationary%20shape "Email")[](https://www.addtoany.com/share)
