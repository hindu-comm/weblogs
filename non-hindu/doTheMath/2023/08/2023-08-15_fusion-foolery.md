+++
title = "Fusion Foolery"
full_title = "Fusion Foolery"
upstream_url = "https://dothemath.ucsd.edu/2023/08/fusion-foolery/"
date = "2023-08-15"

+++
Source: [here](https://dothemath.ucsd.edu/2023/08/fusion-foolery/).

Fusion Foolery

[![](https://dothemath.ucsd.edu/wp-content/uploads/2023/08/nif-llnl-300x240.png)](https://dothemath.ucsd.edu/wp-content/uploads/2023/08/nif-llnl.png)

National Ignition Facility at the Lawrence Livermore National Lab

Great. The fusion hype is bad enough already. Now its resurgence is going to interrupt the series of posts I’m in the middle of publishing in order for this post to be “timely.”

The first (and much bigger) round of breathless excitement came in December 2022 when the National Ignition Facility (NIF) at the Lawrence Livermore National Lab (LLNL) announced a (legitimate) breakthrough in achieving fusion: more energy came out of the target than laser energy injected.

At the time, I brushed it off without even reading any articles because I already knew about the NIF’s purpose and limitations, and a few headlines told me everything I needed to know. Who cares how much *laser* energy went in: how much energy went into *creating* the laser energy? The laser I used for lunar ranging took 5 kW from the wall plug and delivered 2 W of laser power for a dismal 0.04% efficiency. Such is the cost for shaping ultra-brief pulses: lots of energy is thrown away. The headlines were clearly overblown.

Enough students in my energy class in Spring 2023 asked about the fusion breakthrough (doesn’t that mean we’re done?) that I dug into the details. Even so, I still deemed it unworthy of writing up as a post. But a few days ago, my friend asked me if I was excited about the recent fusion news. I hadn’t heard a peep, but after searching I found a new round of articles based on a second “net gain” laser shot and realized I probably ought to put out a quantitative post on the matter, reminiscent of my blogging origins.

In the end, the NIF fusion accomplishment might be called a stunt.
Stunts explore what we *can* do (often after an insane amount of preparation, practice, and failure), rather than what’s practical.
Stunts hide the pains and present an appearance of ease and grace, but it’s a show.

Quantitatively, it’s as if you spot a slot machine in a casino that looks very promising. You’re dying to play, because it just feels right—mysteriously appealing to your sense of self. It calls to you. You notice that it takes \$2 tokens, but you have none. You go to the window to purchase a token, and are shocked to learn that one \$2 token costs \$400. Not wanting to look like an uninformed fool, you gulp and buy the token. This slot machine had better live up to its promise! You pull the lever, and surprise! You actually *do* win! You put in a \$2 token and the machine makes very happy noises and flashes lots of lights as it spits out…\$3 (and some neutrons, oddly). Queue the headlines! Want to play again? Actually, this wasn’t your first shot: just the first success after years of trying (but hush!).

### Energetics

That’s the essence of the story. The December announcement indicated that they launched 2.05MJ of laser energy onto the target sphere, and 3.15MJ came out. The recent articles indicate a second “score,” but fail to give energy specifics, other than “more” energy out. I am assuming an incremental bump, still under 4MJ—otherwise the factor of improvement would be prominently touted in the coverage.

Let’s pause to say: well done! Honestly. No sarcasm. What they did was ridiculously hard, and it finally worked after more than a decade of trying. They actually produced a significant number of fusion events! There’s no faking that, and I’d like to see you try. So let’s be clear that I’m not knocking the accomplishment in itself. My major beef is how we interpret the implications for society. To be fair, the scientists did not supply the hype. They didn’t have to: the rest of the universe was more than ready to fill in that yawning gap.

As I scanned articles from December 2022, most were about the triumph, a reminder that the sun works by fusion, and talk about being the first major step toward limitless clean energy. That’s what people want to hear. It plays right into our cultural mythology: humans defy all limits through ingenuity and technology. Build a story around that theme, and you’ve got yourself some guaranteed click-bait.

A *very* few articles mentioned the energetic price of generating the laser pulse. In particular, I found [one in The Atlantic](https://www.theatlantic.com/technology/archive/2022/12/department-of-energy-nuclear-fusion-breakthrough-nif-livermore/672439/) by Charles Seife:

> The “more energy out than laser energy in” equation masks several > fundamental problems. NIF’s doped glass lasers have an efficiency of about 0.5 percent, meaning that they would have sucked in roughly 400 megajoules of energy from the grid in order to produce the 2.1 megajoules of light energy…

The second was a [Big Think article](https://bigthink.com/the-future/fusion-power-nif-hype-lose-energy/) by Tom Hartsfield.

> The laser energy delivered to the target was 2.05 MJ, and the fusion output was likely about 3.15 MJ. According to multiple sources on NIF’s website, the input energy to the laser system is somewhere between 384 and 400 MJ.

And that’s just the laser energetics. The whole facility consumes scads more for countless other purposes. According to the [LLNL NIF FAQs](https://lasers.llnl.gov/about/faqs) (are you letting me get away with a triple acronym?),

> NIF’s 192 powerful laser beams, housed in a **10-story building** the size of **3 football fields**, can deliver more than 2 million joules of ultraviolet laser energy in billionth-of-a-second pulses onto a target about the size of a pencil eraser.

The emphasis is mine, to highlight the point that this is a massive laser and facility. It’s like ten Walmart superstores stacked on top of each other. The lighting *alone* is likely taking tens of kilowatts, which could hypothetically be run for less than a minute on the energy gain from the fusion pop. It would be fun to count all the megajoules that went into press coverage of the event!

### Power Plant Energetics

Let’s connect the 3 MJ output to that of actual power plants, forgetting for a moment the tremendous energy loss represented in getting 3 MJ out from a 400 MJ input. A typical electrical power plant (nuclear, coal, etc.) delivers about 1 GW of electrical power. But it’s a heat engine operating at 30–40% thermodynamic efficiency. So it takes roughly 3 GW of *thermal* energy to export 1GW as electricity. 3GW is 3GJ per second, or 3,000MJ per second.

The same efficiency factor would apply to a putative fusion plant. The concept behind fusion power is that it’s *just* another thermal source—an excruciatingly elaborate way to boil water to make steam to drive a turbine to run a generator. So our 3MJ would need to be replicated 1,000 times per second to amount to 3GW.

Laser repetition rates can be all over the map. 1,000 Hz is not in itself unusually fast by any stretch. What is the repetition rate of the NIF laser? Handily, LLNL [provides these statistics](https://lasers.llnl.gov/for-users/nif-target-shot-metrics). The average since 2015 is 377 shots per year, with a high of 417 and a low of 327. That’s about a shot per day—or two on a good day. It’s only 100 million times shy of 1 kHz. Oh dear.

### Economics

An [interview](https://thebulletin.org/2022/12/the-energy-departments-fusion-breakthrough-its-not-really-about-generating-electricity/) of physicist Bob Rosner in the Bulletin of Atomic Scientists helpfully puts the NIF in context (it’s not about societal energy). In it, he reinforces some of what we’ve covered, and adds some financial detail.

> This facility can do one shot a day; this is at slightly more than two > megajoules (of output). For an energy source, it would have to do the > same thing at least 10 times a second. If you ask, “Do the lasers exist that can do this?” Not in your dream. The pellet cost a bit over \$100,000 to manufacture.

The 10 shots per second, I gather, is if the fusion yield could be improved by a couple orders of magnitude—approaching actual break-even. At \$100,000 per (literal) pop, and even just ten shots per second, we’re talking a cool million dollars per second!

Let’s wave a magic wand for a minute and say that the 400 MJ input produced a 700 MJ output for a net of 300 MJ: 100 times the recent breakthrough. This accords with the ten shots per second mentioned above. What is the price of the delivered electricity? After thermodynamic inefficiency is accounted, we get 100 MJ out for \$100,000 cost, or \$1,000 per megajoule. We are accustomed to using the kilowatt-hour (kWh) as a measure of delivered energy, which is 3.6 MJ. The cost becomes, then, \$3,600 per kWh. Typical electricity costs are in the neighborhood of \$0.15–0.20 per kWh, so we’re dealing with a cost that is 20,000 times higher than nominal. And don’t forget, we used a magic wand to even get there. It’s closer to 2 million times more expensive currently, and as a net energy loser to boot.

Granted, the research and development phase is not characteristic of operational costs. But try knocking on a venture capitalist’s door and making the argument that you can trim costs to 0.005% of their current amount. Slam!

This massive reduction, incidentally, translates to a cost of \$5 per pellet. I don’t care what mass-production slave labor you might dream of employing. A cryogenic hydrogen-ice target made to demanding precision specifications, containing deuterium and transmuted lithium (to make tritium) is not going to cost \$5. You lost me at cryogenic. Also, they would have made many pellets by now and I’m sure don’t relish spending \$100,000 each. If they’re clever enough to accomplish fusion, they would be clever enough to have already reduced costs dramatically if it were straightforward.

### Fusion Efficiency

Here’s the part where I earn my keep as a physicist translating technical matters. I found details about the NIF targets in a [2017 paper](https://www.tandfonline.com/doi/abs/10.13182/FST10-3697) by Bernard Koziokiemski et al. The abstract alone clarifies much. The target is a shell of hydrogen ice 75 μm thick on a 1 mm radius sphere, cooled below 19 K. Pause for a moment to contemplate the challenges that would be involved if trying to maintain the targets at such low temperatures in a 3 GW power plant “furnace” environment.

Hydrogen ice has a density of 86kg/m³, which in the specified volume (10⁻⁹m³) translates to 5×10¹⁹ lattice sites (nuclei/atoms). Deuterium/tritium ice has a higher density than hydrogen ice, but the atomic spacing is unchanged so that the pure hydrogen calculation gives the correct number.

How many fusion events took place to crank out 3MJ of energy? Each deuterium–tritium fusion event releases 17.6MeV of energy, or 2.8×10⁻¹²J. Calling this 3×10⁻¹²J (among friends; makes for easy math), we find that we need 10¹⁸ fusion events to amount to 3 MJ. Each event involves 2 nuclei. We calculated above that the shell contains 50×10¹⁸ nuclei, meaning that 4% of them participated in fusion.

This event therefore produced a 4% yield. I’m actually very impressed! That’s nothing to sneeze at. The laser-induced implosion is very fast, very violent, and leaves lots of room for nuclei failing to “find” each other if not compressed almost flawlessly and symmetrically to sub-micron scale. Before doing the calculation, I might have guessed a yield orders-of-magnitude smaller.

So this news is both good and bad. Hats off for cracking into single-digit yield! But that leaves less room to improve. Even at 100% efficiency, we’d get just 25 times more energy out, or 75MJ. That’s still not enough to pay for the price of admission (400MJ, just for the laser part).

### NIF Purpose

This avenue, therefore, seems painfully far away from achieving practical societal energy. Even 100% yield (for the present design) could not produce net energy. Even if it *could* produce net energy, the laser repetition rate is a million times too slow. And then, even if the laser could fire fast enough, the cost of each target is prohibitively high by over four orders-of-magnitude.

Then, we have a raft of practical considerations for turning an experimental facility into a functional power plant. No design exists at present to extract the heat produced at NIF. That’s not what it’s for—it wouldn’t make any sense to put effort in that direction. Such a design would have the unenviable thermal challenge of delivering cryogenic targets into a hellfire-hot environment. For energy extraction, tokamak designs like ITER are less unsuitable. In either case, all this to boil water. Bless their hearts.

But the NIF was never “about” societal energy. Its primary purpose is nuclear weapons research. This pesky thing called the nuclear test ban treaty means we can’t just go around detonating nuclear bombs whenever we feel like it. Surely we did not run out of South Pacific island paradises to blow to smithereens. The NIF allows study of matter at extremely high energy density. Other targets besides deuterium–tritium can be placed in the converging laser beams. Essentially, we can create the unbelievably hot conditions relevant to nuclear detonations in the safety of our own national lab.

Inertial confinement fusion (ICF) constitutes a small fraction of [NIF’s laser shots](https://lasers.llnl.gov/for-users/nif-target-shot-metrics). Most of the work is labeled HED for high-energy-density research. The people at NIF are under no false impression about the potential of this type of approach for generating societal energy. They know what they’re about. At the same time, why not poke? It certainly has some benefits in terms of public attention, translating to funding.

### How Embarrassing

So what can we say about the public reaction to this news? Headlines in December gushed about the dawn of a new era of limitless energy. People got excited. Many of my students came away thinking it was basically a done deal—now just a matter of putting into practice. That’s how it works in entertainment: a genius breakthrough followed by immediate implementation free of complication. The emphasis is on human ingenuity, not on physical reality. In my experience, ideas are a dime-a-dozen. The hard part is coming up with an idea that can be practically brought to fruition.

I often encounter a disconnect on matters of this sort when interacting with people—whether about space colonization, fusion, renewable energy, or prospects for modernity’s continuation. I frequently find myself outnumbered. Why am I so negative about these things? The disconnect might have something to do with how information is received and processed. If all I had to go on were popular media accounts, word-of-mouth, and entertainment, I’d probably be similarly miscalibrated. But my background, training, experiences, and accomplishments enable an uncommon approach that is less dependent on what other people are saying, and more strongly tied to the underlying drivers. That’s not to say I’ll always have a more accurate take, but just that my process generally involves more independent thought and analysis than I suspect it does for most people. I’m no fun at parties.

In any case, the public reaction to the fusion story tells me a lot about our collective psychology. To me, it speaks to a sense of desperation. I think people sense that the “bad news” side of the ledger is overcrowded of late, and it’s starting to dawn on people that the future could possibly be worse than the present. This causes a cognitive dissonance in that our cultural narrative is one of progress, growth, and innovation. How can these competing visions be squared? News of fusion has the effect of temporarily permitting people to shed the anxiety and embrace the dream all the more strongly. Words that come to mind are: embarrassing, pathetic, humiliating.

What if you see a movie star across the street, overcome by excitement as they stop, look at you, and wave enthusiastically. You, of course, wave back. They *see* you. They recognize you as special, just as you knew all along. Only, it then becomes apparent that their movie star fling (according to the tabloids) was passing behind you. Now how do you feel? How could you fall for it? That’s the question I find myself asking about the fusion hype. It’s so obviously far from relevant, how could we (and the media establishment) fall for it?

My suspicion is that it plays perfectly into our culture’s irrational hopes and dreams. We have a weak spot in our armor for things that sound too good to be true. We want to believe the narrative (mythology) that humans are exempt from all limits, and that our ingenuity will save the day every time. We want to believe that the movie star would adore us, if only they got the chance to meet us. Instant besties!

Many in our culture truly believe in “the amazing future,” uncritically extrapolating our fossil-fueled joy ride into ever-more impressive innovations and technologies. Of course we will someday roam the galaxy. Of course we will have warp drive (how else would we roam the galaxy?). Of course fusion is a necessary stepping stone on this path. It’s silly to imagine warp drive and teleportation without first cracking fusion. So societal fusion power *has* to happen, in their imaginations.

The problem is that such imaginings are not tethered to physical reality. They are driven by ideology, or I would say mythology. The physical reality is that we are living in an ecologically, evolutionarily untested paradigm that is very recent (on relevant timescales) and powered by patently unsustainable practices and resource use. The cost is rapid ecological degradation and global disruption to the biosphere. It seems quite clear that the track we are on does not lead to the stars, but to ignominious self-termination of this whacky mode called modernity. It simply does not add up, once the mythology is stripped away. The venture capitalist of nature is about to slam the door on our faces.

Hits: 52098

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2023%2F08%2Ffusion-foolery%2F&linkname=Fusion%20Foolery "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2023%2F08%2Ffusion-foolery%2F&linkname=Fusion%20Foolery "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2023%2F08%2Ffusion-foolery%2F&linkname=Fusion%20Foolery "Email")[](https://www.addtoany.com/share)
