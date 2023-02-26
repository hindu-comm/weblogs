+++
title = "Neuroscience Basics II"
full_title = "Neuroscience Basics II Dendrites, Axons and Action Potentials"
date = "2007-04-16"
upstream_url = "https://www.gnxp.com/WordPress/2007/04/16/neuroscience-basics-ii-dendrites-axons-and-action-potentials/"

+++
Source: [here](https://www.gnxp.com/WordPress/2007/04/16/neuroscience-basics-ii-dendrites-axons-and-action-potentials/).

Neuroscience Basics II: Dendrites, Axons and Action Potentials

There are four kinds of ions involved in the intricate [feedback system described in Part I](https://www.gnxp.com/blog/2007/04/neuroscience-basics-i-electricity-and.php): calcium (Ca2+), potassium (K+), sodium (Na+), and chloride (Cl-). They all serve different functions, but for now all you need to know is that first three carry a positive charge while last is negative, and that “at rest” the interior of the neuron caries a negative charge relative to its surrounding environment. With me so far? Onward.

Each type of ion exists in different concentrations within the the neuron when it’s “at rest”, and this concentration is governed by how permeable the cell membrane is under conditions of inactivity. In this state, K+ flows pretty freely in and out of the membrane and is close to equlibrium, but the others are all restricted (and thus out of chemical equilibrium) to varying degrees: Na+, Cl-, and Ca2+ are all banging at the gates to get inside. Also, each type of ion channel permits flow at different rates, K+ being the slowest of the four. I mention this now because it becomes important later on.

So let’s say that while a neuron is just minding its own business, some meddling neuroscientist comes along and injects a bunch of Na+ ions into it. Since sodium ions carry a positive charge, this would make the voltage across the cell membrane tend to become less negative—i.e. it would move the neuron closer to electrical equilibrium with its environment (known as “depolarization”). If it had been Cl- ions instead, the opposite would occur: the voltage would become more negative, moving the system further from equilibrium (known as “hyperpolarization”). Or suppose instead that some K+ ions were sucked out; hyperpolarization would tend to occur in this case too. But in each case, the excess ions would gradually be pumped out by the cell’s regulatory system (or more ions allowed to flow in, in the K+ example), bringing it back to the initial set point.

This is exactly what happens in normal neural activity, except instead of a meddling neuroscientist it’s mediated by ion channels. When the synaptic endpoints of the neuron’s dendrites (which I’ll talk more about in a later post) recieve a particular neurotransmitter, their [ion channels](https://en.wikipedia.org/wiki/Ion_channel) for Na+ or Cl- will open depending on which neurotransmitter it is. We’ll get into neurotransmitters more later, but for now I’ll just introduce two of them: [GABA](https://en.wikipedia.org/wiki/Gamma-aminobutyric_acid) and [glutamate](https://en.wikipedia.org/wiki/Glutamic_acid).

To simplify it in very crude terms for now, GABA is the signal for “open some Cl- channels” and glutamate is the signal for “open some Na+ channels”, which will cause an influx of these respective ions into the cell, lowering or raising the voltage accordingly. Glutamatergic transmissions from other neurons are considered “exicitory modulation” because they tend to encourage the neuron to fire, while GABAergic transmissions are considered “inhibitory modulation” because they tend to discourage it.

Whether or not a neuron “fires” depends on whether the summed ionic charges inside it cause the neuron to depolarize below a certain threshold: in the short run, if there’s an equal influx of Cl- ions and Na+ ions then the effects will be a wash—the overall voltage doesn’t change and nothing happens. Once the dust clears, the sodium and chloride ions get pumped out and the cell goes back to waiting for the next round of stimulus.

But if the influx of Na+ outweighs the influx of Cl- by a certain threshold (i.e. the excitory stimulus outweighs the inhibitory stimulus), it sets off a chain reaction which I’ll now describe. Remember that I said in [Part I](https://www.gnxp.com/blog/2007/04/neuroscience-basics-i-electricity-and.php) that some (but not all) of the ion channels in the cell were voltage-senstive (or “[voltage-gated](https://en.wikipedia.org/wiki/Voltage-gated_ion_channel)“); now two of these become important.

First, there are voltage-gated [Na+ channels](https://en.wikipedia.org/wiki/Sodium_ion_channel) that start to open up when the cell depolarizes, allowing *more* sodium ions in and depolarizing it further in a wave of [positive feedback](https://en.wikipedia.org/wiki/Positive_feedback) that starts in the dendritic region and spreads along the cell body toward the axon. (When Cl- ions are predominant, they act to cut this process off at its starting point by overpowering the positive charge and keeping the downstream sodium gates from opening, halting the chain reaction before it really takes off.) Once the cell depolarizes past a certain point, these gates close again and the Na+ stops flowing in.

As the influx of Na+ spreads through the cell, it triggers the opening of a special set of [K+ channels](https://en.wikipedia.org/wiki/Voltage-gated_potassium_channel) that are normally closed, but open up when the cell depolarizes past a certain threshold, allowing K+ ions to flow out of the neuron and causing the cell’s voltage to start going negative again. As I mentioned a few paragraphs ago, the action of these K+ gates is slower than those for Na+, so you end up with a second wave of re-polarization lagging behind the initial wave of depolarization.

Once the depolarizing wave reaches the [axon](https://en.wikipedia.org/wiki/Axon), the real action begins. Most axons in mammals are coated with a sheath of [myelin](https://en.wikipedia.org/wiki/Myelin) (basically a special extra-thick layer of phospholipids), which acts as an insulator preventing any ion transfer across the cell membrane and makes the axon the most highly conductive region of the neuron. If it isn’t obvious why, you can think of an unmeylinated axon as a leaky pipe: when a pipe is full of holes, it takes a lot of force to push water all the way through it because the water keeps diffusing outward. Myelin effectively “plugs the holes”, which means it requires less force to push “water” (charge) through the “pipe” (axon) at a faster rate. So myelin speeds up transmission along the length of the axon by easing propagation of electrical charge.\[1\]

However, there are still only so many ions, so in order to keep the charge from dimnishing as it travels the length of the axon, fresh influxes of Na+ are necessary. For this purpose, there are periodic breaks in the myelin sheath about a micron wide, known as [nodes of Ranvier](https://en.wikipedia.org/wiki/Node_of_Ranvier).\[2\] These nodes are each loaded with a whole bunch of hair-trigger Na+ channels that will open up under conditions of depolarization, and their combined effect is to make the current move along the axon in a series of [fast hops](https://en.wikipedia.org/wiki/Saltatory_conduction), basically acting as [voltage repeaters](https://en.wikipedia.org/wiki/Repeater).

The K+ channels continue to play catch-up, bringing the charge back to normal negative polarity in the wake of the wave of positive charge. Eventually the [ion pumps](https://en.wikipedia.org/wiki/Ion_transporter) in the cell will clean everything up and bring all the ion levels back to baseline, but right now the cell is busy just trying to normalize its voltage. This entire process is called an “action potential”, or simply a “spike” because of the spike that appears on a voltmeter monitoring the neuron during an action potential. One important feature of an action potential is that “a spike is a spike is a spike”—the amplitude of the wave is always the same for every single action potential. This is the only part of the neuron that can be considered “digital”: either it fires or it doesn’t, with no grey area. (What *can* change is the number and frequency of spikes, but that’s for later posts.)

Once the wave of positive charge reaches the e  
ndpoints of the axons (“axon terminals”), sodium’s job is done and [voltage-gated calcium channels](https://en.wikipedia.org/wiki/Voltage-gated_calcium_channel) are waiting to pick up the ball. When the voltage at the axon terminal goes positive, there’s a flood of Ca2+ into the axon terminal, which triggers . . . well, we’ll get into that later after we cover synapses in the next post.

**Addendum:** There are, of course, many more ways of modulating neural activity than I’ve presented here, but when writing an introduction to the workings of any complex system you have to balance the need for thoroughness against the need to avoid overwhelming the reader with too much at once. For instance, there’s almost no such thing as a neurotransmitter or ion that just does *one* thing in the brain, but the goal for now is to get the gist across so everyone has a working mental model of neural processes and then build up the complexities from there.

Notes:

\[1\] Those of you with an interest in Ashkenazi intelligence & diseases will rightly perk up here. Some of recessive diseases they’re prone to like [Niemann-Pick](https://en.wikipedia.org/wiki/Niemann-Pick_disease) screw up the myelin sheath in ways that likely result in faster signal propagation in a heterozygote.

\[2\] How [these guys](http://www.nodesofranvier.com/) got a piece of neuroanatamy named after them, I’ll never know.

### Related Posts:

- [Neuroscience Basics I: Electricity and
  Equilibrium](https://www.gnxp.com/WordPress/2007/04/07/neuroscience-basics-i-electricity-and-equilibrium/) - [Resonance and
  plasticity](https://www.gnxp.com/WordPress/2008/02/07/resonance-and-plasticity/) - [Basics:
  synapses](https://www.gnxp.com/WordPress/2006/11/16/basics-synapses/) - [Neurotransmitters and
  vesicles](https://www.gnxp.com/WordPress/2006/11/22/neurotransmitters-and-vesicles/) - [Multi-unit recording: SFN
  decompression](https://www.gnxp.com/WordPress/2006/10/17/multi-unit-recording-sfn-decompression/) - [Glowing channels shed light on
  plasticity](https://www.gnxp.com/WordPress/2006/10/05/glowing-channels-shed-light-on-plasticity/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F04%2F16%2Fneuroscience-basics-ii-dendrites-axons-and-action-potentials%2F&linkname=Neuroscience%20Basics%20II%3A%20Dendrites%2C%20Axons%20and%20Action%20Potentials "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F04%2F16%2Fneuroscience-basics-ii-dendrites-axons-and-action-potentials%2F&linkname=Neuroscience%20Basics%20II%3A%20Dendrites%2C%20Axons%20and%20Action%20Potentials "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F04%2F16%2Fneuroscience-basics-ii-dendrites-axons-and-action-potentials%2F&linkname=Neuroscience%20Basics%20II%3A%20Dendrites%2C%20Axons%20and%20Action%20Potentials "Email")[](https://www.addtoany.com/share)
