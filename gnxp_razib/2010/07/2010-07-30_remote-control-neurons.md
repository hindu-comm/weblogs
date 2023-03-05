+++
title = "Remote control neurons"
full_title = "Remote control neurons"
date = "2010-07-30"
upstream_url = "https://www.gnxp.com/WordPress/2010/07/30/remote-control-neurons/"

+++
Source: [here](https://www.gnxp.com/WordPress/2010/07/30/remote-control-neurons/).

Remote control neurons

Mirrored from [http://wiringthebrain.blogspot.com](https://wiringthebrain.blogspot.com)

Clever, elegant and extremely powerful – techniques to activate specific sets of neurons with light have the potential to revolutionise cellular and systems neuroscience. Optogenetics has already been used to address a number of questions which have been resistant to answer by other techniques, and also holds great promise for neurotherapeutics and prosthetics. A new paper adds another approach to the toolkit – the ability to activate neurons with a radio frequency magnetic field. While very much a proof of principle, with a ways to go before it proves its worth, this approach offers some obvious advantages over optogenetics, most obviously that magnetic fields pass into brains much more readily than light.

When trying to figure out what different brain circuits do, one of the most obvious experimental approaches is to ask: what happens if I make these neurons fire? Neuroscientists have traditionally used electrodes to activate neurons in the brain or in slices of brain tissue. This approach is powerful but crude – even with microelectrodes it is difficult to stimulate just the neurons you want. In fact, in many cases it is impossible as different types of neurons tend to be intermingled with each other. If you want to figure out the job of just one of those types then it’s no good sticking an electrode in that part of the brain and zapping all of them at the same time.

The technique of optogenetics takes advantage of the fact that different types of neurons express distinct profiles of genes (each encoding a separate protein) – that’s what makes them different. A gene consists of two parts – one stretch of DNA that encodes the protein and another, adjacent stretch of DNA that encodes the instructions of when and where that protein should be made. The trick is this – that second bit of DNA can be cloned and attached to a different piece of DNA that codes for a different protein – your favourite protein. Now if that new combined DNA construct is put back into the organism then your favourite protein will be made in only the cells that normally make the original protein. As we learn more and more of the molecular details of different types of neurons in the brain our ability to express proteins in more selective subsets of cells increases all the time.

The second trick in optogenetics was to find a protein that would make neurons responsive to light. The answer came from an unlikely source – green algae. These organisms detect light with an opsin protein, called Channelrhodopsin-2 (ChR2), which is related to those that we use in our own photoreceptor cells in our eyes. But the algal protein is different in that it performs this function without the help of any other proteins – when light (specifically blue light) hits the protein, which sits in the membrane of the cell, the protein changes its conformation, opening a channel and letting sodium ions flow into the cell. Algae use this as a chemical signal but neurons use the flow of sodium ions as an electrical signal to trigger firing of an action potential.

So, it is possible to make a DNA construct fusing the control elements of some gene with the coding elements of ChR2. The resultant construct can then be inserted into the cells of the organism you wish to study in two main ways: one is to make a transgenic animal by inserting the construct DNA into the organism’s own chromosomes in the germline – then all the cells of the offspring will carry the transgene. The other, which has for more therapeutic potential, is to use a virus to carry the transgene into cells of the organism. Both techniques have been used to create animals where some specific neurons express the ChR2 protein (or other variants which respond to different wavelengths of light, some of which turn off neurons by letting chloride ions into the cell). If you shine light on these neurons then you can almost instantaneously activate them and when you turn the light off they rapidly stop firing.

This has allowed a series of incredibly powerful experiments to dissect the functions of very specific sets of cells with unprecedented precision. These have, for example, dissected the cellular circuitry underlying the motor symptoms of Parkinson’s disease, elucidated the roles of a specific class of inhibitory neuron in coupling the firing of ensembles of neurons, establishing high-frequency brain rhythms and shown that a class of non-neuronal cells called astrocytes are involved in controlling breathing rate. Optogenetics has also been used to directly show what kinds of neuronal activity drives the signals seen in functional magnetic resonance imaging scans, which had only been inferred previously, and even to restore some degree of vision in a mouse model of retinitis pigmentosa, where the normal rhodopsin protein is absent.

The only problem with this approach from an experimental point of view is that getting light deep into the brain is not so easy. It has been accomplished to date by inserting micro-optical fibres or light-emitting diodes. While the results have been amazing, it is still far from ideal to have to employ these invasive techniques. This is why the recent paper describing a method to activate neurons with a magnetic field is so exciting. Arnd Pralle and colleagues have devised a fiendishly clever combination of nanoscience and neurogenetics to accomplish this feat.

There aren’t any known proteins that are endogenously sensitive to magnetic fields (at least not known to me) so a proxy was required – in this case, the trick was to use the magnetic field to cause an increase in temperature and to make the neurons responsive to this change. To target this effect to specific neurons involved several components, some of which the Borg themselves would have been proud of. The first is a manganese-ferrite (MnFe2O4 for those of you keeping score) nanoparticle, which have the property that they rapidly heat up in a magnetic field. (For a similar reason, people with heavy tattooing are usually advised not to go in a magnetic resonance scanner as the iron in the ink can heat up to painful levels). These nanoparticles were attached to a small chemical tag called streptavidin. When presented in an aqueous solution these nanoparticles will stick to another chemical tag, biotin, which can be attached to a specific protein, which can be expressed in just some cells, using the kinds of transgenic technologies described above. The final component is another channel protein that is sensitive to heat – called TRPV1. These proteins are normally expressed in sensory neurons in the skin that respond to heat and pain. Incidentally, they also are expressed in the tongue and respond to capsaicin – the spicy ingredient in chili peppers, explaining why this tastes “hot” and painful. By itself, the TRPV1 channel simply lets ions into the cell – the interpretation of that signal depends on which part of the brain the message is sent to, so the protein can be used in other cells without inducing a painful sensation.

Putting it all together: two transgenes are used to express a biotin-tagged protein which will capture the nanoparticles on the surface of the cell and a TRPV1 channel, both in the same specific set of cells. When a radio frequency magnetic field is applied, the nanoparticles heat up – very locally and not enough to cause any damage but enough to activate the nearby TRPV1 channel, which then opens, causing the neurons to fire. Nice!

This technology still needs some work to be ready for prime time but something along these lines should succeed and will provide a very useful complement to optogenetic approaches, where the requirement to get light into the tissue is too limiting.

Lee, J., Durand, R., Gradinaru, V., Zhang, F., Goshen, I., Kim, D., Fenno, L., Ramakrishnan, C., & Deisseroth, K. (2010). Global and local fMRI signals driven by neurons defined optogenetically by type and wiring Nature, 465 (7299), 788-792 DOI: [10.1038/nature09108](https://dx.doi.org/10.1038/nature09108)

Busskamp, V., Duebel, J., Balya, D., Fradot, M., Viney, T., Siegert, S., Groner, A., Cabuy, E., Forster, V., Seeliger, M., Biel, M., Humphries, P., Paques, M., Mohand-Said, S., Trono, D., Deisseroth, K., Sahel, J., Picaud, S., & Roska, B. (2010). Genetic Reactivation of Cone Photoreceptors Restores Visual Responses in Retinitis Pigmentosa Science, 329 (5990), 413-417 DOI: [10.1126/science.1190897](https://dx.doi.org/10.1126/science.1190897)

Kravitz, A., Freeze, B., Parker, P., Kay, K., Thwin, M., Deisseroth, K., & Kreitzer, A. (2010). Regulation of parkinsonian motor behaviours by optogenetic control of basal ganglia circuitry Nature, 466 (7306), 622-626 DOI: [10.1038/nature09159](https://dx.doi.org/10.1038/nature09159)

Huang, H., Delikanli, S., Zeng, H., Ferkey, D., & Pralle, A. (2010). Remote control of ion channels and neurons through magnetic-field heating of nanoparticles Nature Nanotechnology DOI: [10.1038/nnano.2010.125](https://dx.doi.org/10.1038/nnano.2010.125)

### Related Posts:

- [Math and
  neuroscience](https://www.gnxp.com/WordPress/2007/07/23/math-and-neuroscience/) - [Mirror neurons not all
  that?](https://www.gnxp.com/WordPress/2009/06/02/mirror-neurons-not-all-that/) - [Multi-unit recording: SFN
  decompression](https://www.gnxp.com/WordPress/2006/10/17/multi-unit-recording-sfn-decompression/) - [Associative neurons in the
  amygdala](https://www.gnxp.com/WordPress/2006/10/19/associative-neurons-in-the-amygdala/) - [Neuronal taxonomy based on expression
  profiles](https://www.gnxp.com/WordPress/2006/09/17/neuronal-taxonomy-based-on-expression-profiles/) - [Knocking out stimulant
  reward](https://www.gnxp.com/WordPress/2006/07/30/knocking-out-stimulant-reward/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F07%2F30%2Fremote-control-neurons%2F&linkname=Remote%20control%20neurons "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F07%2F30%2Fremote-control-neurons%2F&linkname=Remote%20control%20neurons "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2010%2F07%2F30%2Fremote-control-neurons%2F&linkname=Remote%20control%20neurons "Email")[](https://www.addtoany.com/share)
