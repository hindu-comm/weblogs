+++
title = "Elusive Entropy"
full_title = "Elusive Entropy"
upstream_url = "https://dothemath.ucsd.edu/2013/05/elusive-entropy/"
date = "2013-05-28"

+++
Source: [here](https://dothemath.ucsd.edu/2013/05/elusive-entropy/).

Elusive Entropy

[![partial mix](https://dothemath.ucsd.edu/wp-content/uploads/2013/05/partial-150x150.jpg)](https://dothemath.ucsd.edu/wp-content/uploads/2013/05/partial.jpg)We’ve all heard it. We think we understand it: entropy is a measure of disorder. Combined with the Second Law of Thermodynamics—that the total entropy of a closed system may never decrease—it seems we have a profound statement that the Universe is destined to become less ordered.

The consequences are unsettling. Sure, the application of energy can reverse entropy locally, but if our society enters an energy-scarce regime, how can we maintain order? It makes intuitive sense: an energy-neglected infrastructure will rust and crumble. And the Second Law stands as a sentinel, unsympathetic to deniers of this fact.

A narrative has developed around this theme that we take in low entropy energy and emit a high entropy wake of waste. That life displays marvelous order—permitted by continuous feeding of this low entropy energy—while death and decay represent higher entropy end states. That we extract low entropy concentrations of materials (ores) from the ground, then disperse the contents around the world in a higher entropy arrangement. The Second Law warns that there is no going back: at least not without substantial infusion of energy.

But wait just a minute! The preceding paragraph is **mostly wrong**! An unfortunate conflation of the concepts of **entropy** and **disorder** has resulted in widespread misunderstanding of what **thermodynamic entropy** actually means. And if you want to invoke the gravitas of the Second Law of Thermodynamics, you’d better make darned sure you’re talking about *thermodynamic* entropy—whose connection to order is not as strong as you might be led to believe. Entropy can be quantified, in Joules per Kelvin. Let’s build from there.

### The Measure of Entropy

From a thermodynamic standpoint, the total entropy of a system has a simple definition. If I add an amount of energy *ΔE* (measured in Joules, say), to a system at temperature *T* (measured on an absolute scale, like Kelvin), the entropy changes according to *ΔS=ΔE/T*. The units are Joules per Kelvin.

This is *very* closely related to the **heat capacity** of a system or object. If we measure for a substance how much the temperature changes when we add a bit of energy, the ratio is the heat capacity. Divide by the object’s mass and we have a property of the material: the **specific heat capacity**. For example, the specific heat capacity of water is *c*_(p)≈4184J/kg/K. If we heat one liter (1kg) of water by 10°C (same as a change by 10K), it takes 41,840J of energy. Most everyday substances (air, wood, rock, plastic) have specific heat capacities around 1000J/kg/K. Metals have lower specific heat capacities, typically in the few-hundred J/kg/K range.

So if we know the specific heat capacity as a function of temperature, and start the material out at absolute zero temperature, adding energy until it comes up to the temperature of interest (room temperature, in many cases), we can compute the total entropy by adding (integrating) all the little pieces *ΔS=ΔE/T*, where *ΔE*=*c*_(p)*mΔT*, and *m* is the mass of the object of interest.

Most materials have a specific heat capacity dropping to zero at zero temperature, and rising to some nearly constant value at intermediate temperatures. The result of the integration for total entropy (sparing details) pencils out to approximately equal the heat capacity, *c*_(p)*m*, within a factor of a few. For a kilogram of ordinary matter, the total entropy therefore falls into the ballpark of 1000J/K.

Because entropy and heat capacity are so intimately related, we can instantly order entropies of everyday substances: metals are lowest, followed by stuff like wood and rock, and liquids have the highest (water, especially), on a per-kilogram basis.

### Where is the Disorder?

Note that we have managed to quantify entropy—at least in broad brush, order-of-magnitude style—without making reference to order.

Well, it turns out that if one can count the number of quantum mechanical states available to a system at a given (fixed) energy—in other words, counting all the possible configurations that result in the same total energy—and call this ginormous number *Ω*, then the absolute entropy can also be described as *S*=*k*_(B)ln*Ω*, where *k*_(B)=1.38×10⁻²³J/K is the Boltzmann constant (note that it has units of entropy), and ln() is the natural logarithm function. This relation is inscribed on Boltzmann’s tomb.

It is this amazing relationship that forms the foundation of **statistical mechanics**, by which classical thermodynamics can be understood as the way energy distributes among microscopic states in the form of velocity distributions, collisions, vibrations, rotations, etc. Intuitively, the more ways energy can tuck into microscopic modes of motion, the less apparent it is to the outside world in the form of increased temperature. A system with deep pockets will not increase temperature as much for a given injection of energy. Substances with higher heat capacities have deep pockets, and therefore more ways to spread out the energy internally. The states of these systems require a greater amount of information to describe (e.g., rotational and vibrational modes of motion in addition to velocities, intermolecular interactions, etc.): they are a mess. This is the origin of the notion of entropy as disorder. But we must always remember that it is in the context of how energy can be distributed into the *microscopic* states (microstates) of a system.

### Informational Entropy

The fans went wild. In 1949, Claude Shannon was characterizing information loss, and needed a term for the degree to which information is scrambled. Visiting mathematical physicist John von Neumann, he received the following advice:

> You should call it entropy…nobody knows what entropy really is, so in > a debate you will always have the advantage.

Gee, von Neumann couldn’t have been more right. The resulting duplicate use of the term “entropy” in both thermodynamic and information contexts has created an unfortunate degree of confusion. While they share some properties and mathematical relationships, only one is bound to obey the Second Law of Thermodynamics (can you guess which one?). But this does not stop folks from invoking entropy as a trump card in arguments—usually unchallenged.

But informational entropy does not generally transfer into the thermodynamic realm. A deck of cards has the **same** thermodynamic properties (including thermodynamic entropy) *no matter how* the cards are sequenced within the deck. A shuffled deck has increased informational entropy, but is thermodynamically identical to the ordered deck.

### What’s the Difference?

To determine whether two different states of some real or imagined system is meaningfully different in thermodynamic entropy, ask yourself these questions:

1.  If I took the system to zero temperature and then added energy until getting back to the original temperature, would the amount of energy required be different for the two configurations? 2.  Is there an intrinsic physical process by which one state may evolve to the other spontaneously? In other words, are the items continuously jostling about and changing configuration via collisions or some other form of agitation?

The first question primarily boils down to whether the microscopic structure has been changed, so that the places energy gets stored will look different before and after. If the change has been chemical in nature, then almost certainly the micro-level energy storage properties will be different. If it’s just a matter of moving macroscopic pieces about, then any entropy change is probably too small to care about.

The second question concerns the relevance of entropic differences, and highlights the notion that entropy only really makes sense for systems in thermodynamic equilibrium. Salt grains and coffee grains sitting in two separate piles on a flat surface will sit that way indefinitely over any timescale we consider to be relevant. Absent air currents or other disturbances, there may be small thermal jostling that over billions of times the age of the Universe could work to mix the two populations. But such timescales lose meaning for practical situations. Likewise, books and papers heaped on the floor have no random process of self-rearrangement, so the configuration is not thermodynamically relevant. Applying the test outlined by the first question above would have the same thermodynamic result in either configuration.

[![salt and coffee](https://dothemath.ucsd.edu/wp-content/uploads/2013/05/separate-300x200.jpg)](https://dothemath.ucsd.edu/wp-content/uploads/2013/05/separate.jpg)

Salt and coffee grains, in separate piles.

[![mixed up](https://dothemath.ucsd.edu/wp-content/uploads/2013/05/mixed-300x200.jpg)](https://dothemath.ucsd.edu/wp-content/uploads/2013/05/mixed.jpg)

Same grains, mixed up: entropy unchanged.

Another way to say this is: it does not make sense to characterize the entropy of a given frozen arrangement. The salt and coffee example, whether mixed or separated (with no barrier between, let’s say) are both equally probable instances of the same system energy. Yes, there are myriad more ways to arrange a mixed state. But a *particular* mixed state is just as special as the separated piles. If we had a removable barrier between separated piles and provided a random agitating process by which grains could rearrange themselves on relevant timescales, then we *could* describe the entropy difference between the *ensemble* of separated states *with* a barrier to the *ensemble* of mixed states *without* a barrier. But we can’t really get away with discussing the entropy of a particular non-thermalized (static) arrangement.

#### Nitpicky Difference

Okay, after saying that configuration changes of macroscopic arrangements effectively carry no difference in thermodynamic entropy, I will make the tiniest retraction and clarify that this is not *exactly* true. Going back to the coffee/salt grains example, a system of two species of particles *does* carry a finite and quantifiable entropic change associated with mixing—assuming some agitating mechanism exists. In the case where the number of grains per unit area is the same for the two clusters, the post-mixed arrangement (occupying the same area as the initial separate piles) has an entropy change of

[![entropy-eqn](https://dothemath.ucsd.edu/wp-content/uploads/2013/05/entropy-eqn-300x38.png)](https://dothemath.ucsd.edu/wp-content/uploads/2013/05/entropy-eqn.png)where *k*_(B) is the tiny Boltzmann constant, and the *N* values count the number of particles or grains in group 1 and group 2. Simplifying to the case where each group contains the same number of particles just gives *ΔS*=2*Nk*_(B)ln2, or about 1.4*Nk*_(B).

In atomic and molecular arrangements, we commonly deal with **moles** of particles, so that *N*≈10²⁴ particles (the Avogadro number), and the mixing entropy comes out to something of order 10J/K (compare to absolute entropy often around 1000J/K). But dealing with macroscopic items, like grains of salt or coffee, we might have *N*≈10,000, in which case the entropy difference in mixing is about 10⁻¹⁹J/K.

So there *can be* a real thermodynamic difference between the two states, some twenty orders of magnitude down from the gross thermodynamic entropy of the system. Why do I use the words “can be” and not the simpler “is?” Because question 2 comes in. If there is no statistical process by which the particles can thermalize (mix) over timescales relevant to our interest, then the entropy difference has no meaning. If we apply the test in question 1 to the pre-mixed and post-mixed piles, the procedure does not provide an opportunity for random rearrangements, and thus no measured change in system entropy will manifest itself in an observable way.

### Some Examples

In order to clarify some mistaken themes relating to entropy, let’s look again at the third paragraph of the post, repeated here:

> A narrative has developed around this theme that we take in low > entropy energy and emit a high entropy wake of waste. That life > displays marvelous order—permitted by continuous feeding of this low > entropy energy—while death and decay represent higher entropy end > states. That we extract low entropy concentrations of materials (ores) > from the ground, then disperse the contents around the world in a > higher entropy arrangement. The Second Law warns that there is no > going back: at least not without substantial infusion of energy.

#### Low Entropy Energy?

Characterizing an energy source as high or low entropy makes little sense. Take the Sun, for example. The surface of the Sun is about 5800K. Every Joule of energy that leaves the Sun removes about 0.17mJ/K of entropy from the Sun, according to *ΔS=ΔE/T*. In this way, the Sun’s total entropy actually *decreases* with time (internally, it consolidates micro-particles: hydrogen into helium; externally, it spews photons, neutrinos, and solar wind hither and yon). So the Sun is a prodigious *exporter* of entropy. Let’s say we catch this Joule of energy on Earth. When absorbed at a temperature of 300K, we could say that we have deposited 3.3mJ/K of entropy. So that Joule of energy does not have a fixed entropic price tag associated with it: 0.17mJ/K became 3.3mJ/K. If we cleverly divert the energy into a useful purpose, rather than letting it thermalize (heat something up), the Second Law requires that we at least increase terrestrial entropy by 0.17mJ/K to balance the books. We are therefore mandated to deposit at least 0.17/3.3, or 5% (50mJ) of the energy into thermal absorption, leaving 0.95J free to do useful work. This results in a 95% efficiency, which is the standard thermodynamic limit associated with operation between 5800K and 300K (see related [post on heat pumps](https://dothemath.ucsd.edu/2012/06/heat-pumps-work-miracles/ "Heat Pumps Work Miracles")).

The point is that rather than characterize solar input energy as low entropy (little meaning), we should just focus on the fact that we have a large temperature difference between Sun and Earth. It is the large temperature difference that allows a flow of energy from one to the other, and the Second Law allows diversion of some fraction of this energy into a non-thermal path without reducing overall system entropy.

By the way, the entropy of the Earth as a whole, like the Sun, also decreases in the long term, made possible by a net exodus of stored thermal energy and the lightest gases (hydrogen and helium).

#### The Quick and the Dead

What about the entropy of living vs. dead things? If we drop our notion of which is more or less orderly, and think thermodynamics, it becomes easy. A 50kg living person has lots of water content. The heat capacity is high. The entropy of this system is large. A dry, decaying corpse, let’s say also 50kg, has a lower heat capacity, lacking liquids. So the thermodynamic entropy of the corpse is lower than that of the living thing.

This comparison may or may not be surprising, but it wasn’t necessarily fair. The living version of the 50kg corpse had a larger living mass, and as the water evaporated the entropy of the entire system (tracking all the mass) goes up. It’s just that the solid remains, in a pound-for-pound comparison, ends up at lower entropy. Note that this result does not respect our sense of “order” as low entropy. The presence of lots of improbably operational subsystems in the living organism does not translate to a lower entropy state, thermodynamically speaking.

A related matter is the notion that we eat low entropy food and produce high entropy waste. In this context we associate “usefulness” with entropy—or lack thereof. We can eat a useful burrito, but cannot derive sustenance by eating our solid waste. In a direct comparison, the solid waste (out of which our bodies remove as much water as possible) has lower thermodynamic entropy than the same mass of burrito—since the latter has more water content. Sorry to be gross here, but this makes the comparisons personally relevant. Sure, the *system* entropy increased in the process of digesting food (e.g., via respirated gases). But the measure of thermodynamic entropy for a “thing” is not a measure of its usefulness.

#### Mining Materials

The story goes that we extract low entropy (i.e., concentrated) resources from the ground, and turn them into high entropy products. Sometimes this happens, but often it is the reverse. When we pull fossil fuels out of the ground and combust them into several species of gases, we increase entropy. All the king’s horses and all the king’s men will never put fossil fuels back together again. At least not at an energetic bargain.

But let’s look at another common case. Mineral ores are local concentrations of some material of value—like copper, aluminum, gold, etc. The ore is fantastically more concentrated than the average crustal abundance. Our information-entropy minds tag this as low entropy material. But the ore is still far from pure: maybe a few percent of the ore contains the metal we want. The rest is rock we care little about. Our quest is to purify (concentrate further) the material.

First, let’s compare a kilogram of copper ore and a kilogram of refined copper. The ore has low-heat-capacity metal (copper), plus higher-heat-capacity rock. The entropy in the ore is higher than the entropy in the product. So far, no one is perturbed, because the purity, or orderliness, has increased (wrong reason to think the copper is lower entropy, but okay). Now the copper is deposited on circuit boards in small traces and put into cell phones that get shipped around the world, many ending up in landfills. What is the entropy of the 1 kg of copper now, having been strewn across the planet? Thermodynamically, it’s the *same*. If we somehow contrived the test of adding energy to bring this globally distributed copper from 0K to 300K, the amount of energy required (performed quickly enough that we may ignore diffusion into surrounding media) would be the same for the block as for the distributed mass. Macroscopic configuration changes don’t contribute measurably to changes in thermodynamic entropy.

Note that if for some reason I happened to be interested in the material with higher heat capacity—mixed with lower heat capacity material—the process of separating the material would produce a chunk of pure material with a *higher* thermodynamic entropy than a similar mass of raw material. So it’s not the purification, or ordering, that makes the entropy go down. It’s the thermodynamic properties with respect to how readily energy is absorbed and distributed into microstates.

The other way to look at the ore situation is to take 100kg of a 1% concentration ore, and separate it into 99kg of rock and 1kg of the target material. What is the entropy difference in the original ore and the separated piles? As long as the grain size of the good stuff is semi-macroscopic (well away from atomic scale), then the entropic difference is negligible. If it is chemically mixed at the atomic scale, like if we wanted to extract chlorine from salt, then the entropy difference could in principle go either way, depending on resultant material properties. But the sorting process has negligible impact on entropy.

### Interpretation

The context of this discussion is mis-application of the Second Law of Thermodynamics to systems that might appear to exhibit entropy differences in the form of orderliness of macroscopic arrangements of matter. But many of these “intuitive” cases of entropy differences translate to little or no *thermodynamic* entropy differences, and therefore do not fall under the jurisdiction of the Second Law.

Simpler statements that are consistent with the laws of thermodynamics and bear on our societal options are:

1.  Energy may be extracted when temperature differences exist (e.g., combustion chamber compared to ambient environment; solar surface temperature compared to Earth surface). Entropy measures of the energy itself are not meaningful. 2.  Net energy from fossil fuels may only be extracted once. 3.  Efficiencies are capped at 100%, and often are theoretically much lower as a consequence of the Second Law.

Meanwhile, we should break the habit of invoking the Second Law to point to the irreversibility or even just the energy cost of restoring ordered arrangements of matter (as in mined ores and recycling). Even if the thermodynamic entropy of processed goods is higher than the feedstock (usually not the case, and at best negligibly different), the Second Law is not the primary barrier to reversing the process. As long as 10¹⁷W flows from the Sun to the Earth, physics and entropy impose no fundamental limits on irreversibility. Our limitations are more on the practical than on the theoretical side.

*I thank Eric Michelsen, Kim Griest, and George Fuller for sharing insights in a fascinating discussion about the nature of entropy. It is said that when a group of scientists discusses entropy, they’ll be talking nonsense inside of ten minutes. I think we managed to steer clear of this common peril. I also learned from [these](http://www.science20.com/train_thought/blog/entropy_not_disorder-75081 "Entrop is Not Disorder") [links](http://entropysite.oxy.edu/ "Entropy Site").*

Hits: 2969

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2013%2F05%2Felusive-entropy%2F&linkname=Elusive%20Entropy "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2013%2F05%2Felusive-entropy%2F&linkname=Elusive%20Entropy "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2013%2F05%2Felusive-entropy%2F&linkname=Elusive%20Entropy "Email")[](https://www.addtoany.com/share)
