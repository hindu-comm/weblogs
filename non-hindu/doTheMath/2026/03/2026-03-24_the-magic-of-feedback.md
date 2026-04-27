+++
title = "The Magic of Feedback"
full_title = "The Magic of Feedback"
upstream_url = "https://dothemath.ucsd.edu/2026/03/the-magic-of-feedback/"
date = "2026-03-24"
+++
Source: [here](https://dothemath.ucsd.edu/2026/03/the-magic-of-feedback/).

The Magic of Feedback

[![](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/baby-macaque-1024x683.jpg)](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/baby-macaque.jpg)

This young macaque learns to employ negative feedback to keep it safe (Image by [Anne-Ed C.](https://pixabay.com/users/anwic-21500104/?utm_source=link-attribution&utm_medium=referral&utm_campaign=image&utm_content=8256950) from [Pixabay](https://pixabay.com//?utm_source=link-attribution&utm_medium=referral&utm_campaign=image&utm_content=8256950)).

What we don’t or can’t comprehend might be called magic. By this measure, most of the universe is—and always will be—magic. That’s okay. The faith of a [materialist monist](https://dothemath.ucsd.edu/2025/12/ditching-dualism-6-maybe-monism/) is that the universe “knows” what it’s doing, and expresses itself in astoundingly diverse ways using an elegantly small number of particle and interaction types: more than compensating via breathtaking emergent complexity. We needn’t grok it all for everything to still work splendidly.

Often, the universe—or an element within it—appears to our naïve eyes to express intent. Organisms seem purposeful. Some aspects of our existence appear to be tuned just-so; self-referential; tautological; teleological. A star perches right on the edge of fusion, sipping its fuel as slowly as it effectively can. Earth finds thermal balance because a 1% departure from normal (absolute) temperature results in a 4% change in the rate of heat loss in the opposite direction (hotter amps up cooling; cooler curtails it substantially). The cell membrane of an egg yolk—or an egg shell, for that matter—is as thick as it needs to be to maintain integrity, but no thicker. Bones are as big as they need to be, and no bigger. Plants and animals tend to exercise sound judgment on the when, where, and how of the actions they take. It’s a world full of Goldilocks scenarios.

The result really is amazing and can easily seem magical. In such cases, ask whether the circular just-so nature might be attributable to **feedback**, which is also loop-like, and holds more power than is apparent. This post attempts to teach a bit of electronics before returning to how feedback performs effective magic in the real world. While it might seem a diversion, a grasp of feedback in the (much simpler/tidier) electronic domain can bolster appreciation of its power (magic) in the wider world.

# Ideal Op-Amps

Imagine a “perfect” electronic device that, besides obligatory power-supply lines, has two inputs—whose voltages are to be compared to one another—and one output that amplifies the voltage difference between its two inputs enormously—like by a factor of a million. This means that a one-microvolt difference between the two inputs would become one volt at the output, and a millivolt difference would be expressed at the output as 1,000 volts. Such a device might take the weakest signal and move mountains.

The greater the amplification (“gain”), the more “ideal” our amplifier is. But hold on. It seems we’ve gone overboard. Firstly, electronics are often supplied with voltages far lower than 1,000 volts, and thus would be incapable of conjuring 1,000 volts for output. Most devices we plug into the wall take the hundred(s of) volts of alternating current and immediately drop down to direct current of 12 volts, 5 volts, 3.3 volts, or the like to power digital electronics. Alternating current at high voltage is an efficient and safe way to *transmit* power, but if directly applied to most electronic circuits would make popping noises and let the smoke out. It is well known among electronics gurus that internal smoke *must* be what makes all devices work (it’s the magic ingredient). The evidence is quite strong: any time you let the smoke out, the thing never works again.

Anyhow, our “ideal” amplifier is not able to fabricate an output outside of the voltage supply range (limits!), so that even a several-microvolt difference at the input terminals would “rail” the amplifier to its supply voltage. That’s pretty useless, as all kinds of effects produce even millivolts of “noise” on the input lines.

Yet, operational amplifiers (op-amps) indeed have enormous “open loop” gain: the more the better! How do we square the purported uselessness of “infinite” gain with the fact that these workhorses of electronic design embrace exactly this high-gain feature? The clue is in the “open loop” qualifier. To illustrate open loop, imagine trying to thread a needle. But one person holds the thread and another holds the needle. Neither are allowed to look, touch, or communicate. Good luck…

Op-amps are almost always placed in circuits providing a literal conductive loop connecting the output to one of the inputs. They are designed for use **in feedback**.

# Feedback is Good?

If you’ve ever suffered the piercing squeal of a speaker near a microphone, you might know that this is called feedback, and is not wanted. So feedback is bad. But feedback comes in two flavors: positive and negative. Which one is nasty? *Positive feedback is positively nasty*. Huh? That’s not what we think when it comes to grades or performance evaluations! Associating positive feedback with “good” is a consequence of thinking in words—made easier within a culture dangerously predicated on several vaunted positive feedback arrangements.

Positive feedback leads to runaway, or exponential growth. A little change produces encouragement to change *more in the same direction*, which produces even greater encouragement to go further, etc. The squeal of a sound system is a sure sign of positive feedback: the microphone picks up a little noise from the speaker, and tells the speaker to produce “more of that,” getting ever-louder until the system is saturated (“rails”). Trying to thread a needle under positive feedback would go like: “you’re a little to the right, so go a lot more to the right!” Basically: any departure is the right thing, so keep doing more of that. Deviations are encouraged, amplified, driven further.

Negative feedback is negative in the sense of being *corrective*: too high should go lower; too far left should go right. The action of negative feedback is unrelated to any valuation of good or bad we might assign, and tends to operate in *both* directions depending on offset: a boat floats higher if finding itself too low, or sinks a bit if too high. Threading a needle requires negative feedback (via sensory signals). Negative feedback produces a damping influence; stability; equilibrium. The world is *full* of negative feedback mechanisms—precisely because those mechanisms *last*. Positive feedback blows itself up and fails to sustain: a runaway phenomenon destined to be a flash in the pan. Squealing modernity is riddled with positive-feedback innovations, which contribute to its spiraling insanity and manifestly temporary nature.

To our (distorted) cultural sensibilities, negative feedback often feels punitive or oppressive. So, our culture strives to eliminate sources of negative (corrective) feedback—rejecting their “rights” to exist, as they impose on our own. [Supreme humans](https://dothemath.ucsd.edu/2024/08/mm-12-human-supremacy/) ought not be correctable by dumb nature, or subject to *limits* for goodness’ sake. Fabricated “rights” are stacked heavily in favor of humans, in the short term.

# Op-Amp Feedback

Following convention, we’ll depict the op-amp as a sideways triangle (like a “play” symbol) with two inputs labeled + and − on the “blunt” side, and an output emerging from the opposite vertex. Power supply lines (e.g., ±5V) are not always depicted (implied), but if drawn are often shown entering the top and bottom of the triangle in circuit diagrams. The “−” input is often called the *inverting* input, while the “+” is the *non-inverting* input (a double-negative).

[![](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/op-amp-symbol.png)](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/op-amp-symbol.png)

Basic op-amp symbol.

Only two rules are needed to analyze basically any op-amp circuit.

1.  Neither input draws or sources any current (shut), while the output
    may sink or source a wide range of currents (open). 2.  If the “+” input is even a *smidge* higher than the “−” input
    (voltage-wise), then the output goes higher, toward the
    positive-voltage supply “rail” (and opposite if reversed).

[![](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/op-amp-open.png)](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/op-amp-open.png)

In open-loop, op-amps go bananas over the smallest difference at the inputs.

So, in the case that we’re supplying a bare op-amp (no feedback loop) with ±5V, if we put 2.002V on the “+” input and 2.001V on the “−” input, the output will quickly soar up toward +5V, limited by the power supply from climbing further. Keeping the same voltage on the “+” input and applying 2.003V to the “−” terminal, the output will crash to −5V. Pretty useless, except as a threshold detector producing a “digital” output (called a “comparator”: reference voltage on “+” and test voltage on “−”).

Let’s consider two simplest-case “topologies” for feedback. First, we contrive positive feedback by hooking the output back to the + terminal.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/op-amp-pfb.png)](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/op-amp-pfb.png)

Positive feedback is stupid.

Let’s say when we power the system up, the output (and thus non-inverting input) is at zero volts and the “−” input is tied to ground (via some non-zero resistance). Inevitably, some tiny bit of thermal noise will cause the voltage at the “inverting” (−) input to move from 0.00000V, either positive or negative. As soon as it does so the op-amp says: “I hear you, okay!” and moves the output toward one supply voltage or the other, depending on the sign of the voltage difference between the two terminals. The immediate result is that the non-inverting (+) input is being pushed (by dint of direct connection to the output) to be dramatically *further* from the minuscule transgression on the inverting (−) input, only reinforcing the op-amp behavior and quickly sending it to the supply “rail,” where it will stay pegged. Freakin’ useless (except when conditioned to manage hysteresis, but that’s not for here).

Now we explore a negative feedback topology:

[![](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/op-amp-nfb.png)](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/op-amp-nfb.png)

Negative feedback gets interesting.

We’ll assume the same starting conditions as last time, with the output (and thus inverting input) at ground. Then we apply some voltage—say 1.23456V—to the non-inverting (+) input. Because it is now markedly higher than the inverting input, the output races upward. But as soon as it pokes above 1.23456V, the relative input polarity reverses and the op-amp gets the memo that it should start heading toward the negative rail. It doesn’t get far before polarity switches again. It’s basically pinned to 1.23456V in a tiny dance of corrective moves. The larger the op-amp’s intrinsic (open-loop) gain, the smaller and faster—and thus more invisible—the corrections.

This might also seem useless: a circuit that just produces at its output the same voltage you put in. A simple wire can do that! Ah, but this is where the current limits come in. The op-amp lets you set a voltage on the non-inverting input from some wimpy source incapable of producing much useful current—not able to drive much in the way of light or sound or a transmission line. But the op-amp output is able to source far more current than the signal source, so it does the hard work without taxing the signal source. This “follower” arrangement “buffers” the input from the demands of the load. It’s incredibly useful, and thus ubiquitous.

A huge number of variations in negative feedback (involving resistors in the feedback loop and along the input lines) produce simple circuits that can add or subtract voltages (weighted however you like). Introducing diodes allows op-amps to multiply or divide. “Reactive” components like capacitors support calculus operations of integration and differentiation. Op-amps in negative feedback become little analog math machines!

As an aside, the second rule above—in the context of negative feedback—becomes: the op-amp will do everything in its power to make the two input terminals equal in voltage. As an instructor helping students in labs involving op-amps, the first thing I would check in a malfunctioning circuit was whether op-amp input voltages were equal. If not, something else is keeping the op-amp from satisfying its mission.

# But Magic?

Okay, the negative feedback arrangement proves itself to be incredibly useful, but it might not rise to the level of seeming like magic.

So here’s a concrete example of where magic can enter. For all its cuteness, an op-amp typically does not source more than a few tens of milli-amps of current, which might be fine to light an LED or send a signal down a transmission line, but won’t really drive a hefty load like a speaker very well. Transistor circuits can handle far more current (several amps), but transistors are not terribly linear, have “dead zones” (unresponsive when the input voltage is modestly low), and other undesirable features that create serious distortion in the signal one wants to amplify.

The op-amp says: “Allow me to fool those transistors into behaving!” Just stick the noisome transistor circuit into the (negative) feedback loop, tasking the transistor arrangement with the job of supplying large currents. It will produce all sorts of nasty distortions, which the [lab manual from Hayes and Horowitz](https://physics.bu.edu/adlab_and_elab/wp-content/uploads/2023/03/Thomas-C.-Hayes-Paul-Horowitz-The-Art-of-Electronics-Student-Manual-Cambridge-University-Press-1989.pdf) rather amusingly drew in cartoon form as fish bones, opened/empty tin cans, and a junkyard dog: trashy. The op-amp, undaunted, and knowing nothing about the vagaries of the dog, will contrive an “inverse dog” at its output so that when passed through the junkyard, the output will again (“magically”) match the value of the non-inverting input. The op-amp does everything in its considerable power to adjust its output so that the two inputs match.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/op-amp-dog.png)](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/op-amp-dog.png)

Negative feedback can work magic to counteract bad influences, forcing the output to look like the input.

This is the magic. The op-amp figures out what to feed the dog so the dog’s output is actually what you want. Any arbitrary non-linearity, hiccups, or other trash (within slew-rate and bandwidth limits) is perfectly inverted by the op-amp. We might not even be able to characterize the vagaries adequately via mathematical functions, let alone invert the expression (often tricky or impossible). The op-amp is undaunted: just does it, without a brain.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/distort-seq.png)](https://dothemath.ucsd.edu/wp-content/uploads/2026/03/distort-seq.png)

Feed the beast a pure signal (top; blue) and get the red crap out. The op-amp in negative feedback, listening to the blue signal, conjures the green signal to feed to the beast, so the beast is tricked into putting out something that looks just like the blue signal—but now stronger.

Above is an example. The blue curve at top is a pristine sine wave that you want to amplify, without suffering distortion. But if fed the blue signal, the powerful-but-junky amplifier creates the red curve, which I constructed to have a time-variable crossover distortion (dead spots), and a time-variable nonlinearity continuously evolving from a square-root at the left edge to a cube at the right edge. The red curve looks (and sounds) nothing like the blue curve, and is one trashy signal. But if the nonlinear beast is stuck into the feedback loop, the op-amp *contrives* the green signal at bottom to feed to the beast, “tricking” it into putting out the blue signal with greater amperage capability. It does so by constantly checking the output (comparing it to the “+” input) and quickly adjusting however it needs in order to make them match. It’s stupidly clever.

An enjoyable bit of Steve Martin’s *[L.A. Story](https://en.wikipedia.org/wiki/L.A._Story)* is when he’s trying to salvage a budding relationship that suddenly went sideways.

> I know there’s something that would make you stay! The right word,
> attitude, plan… But these are all tricks! So let’s forego that! Let’s
> assume that it happened, that my hand went down your throat, grabbed
> your heart and squoze it! There comes a time when it’s now or never!
> It’s now or never! Listen to a poem. “Oh pointy birds, oh pointy,
> pointy, anoint…\[SLAM\]”

I couldn’t leave out the poignant poem (cut off by a slamming door). But the key feature is that *some* magic combination of words would do the trick. The op-amp foregoes any analysis and just conjures *whatever is necessary* to have the output look right. It all comes down to negative feedback in the context of high gain and fast reaction. It’s incessantly asking: “Is this right? How about now? Still right?” It’s extremely attentive!

# Organismic Feedback

The op-amp contrivances are a useful parallel to how thickness of membrane, shell, or bone lands in an optimal compromise: because it’s part of a feedback system constantly testing and “suffering” corrections in a strong feedback loop. Any time a living being uses senses, those inputs are part of a feedback loop: reacting to the stimulus in ways that themselves are shaped by feedback. Just standing upright involves lots of negative feedback. Any stability tends to owe itself to negative feedback.

As covered before, [decisions](https://dothemath.ucsd.edu/2025/01/decisions-decisions/) are shaped by a [long history of feedback](https://dothemath.ucsd.edu/2025/07/what-is-life/) to be generally effective. It sure seems like magic to our uncomprehending meat-brains. But there’s a method underneath the madness. Just as the op-amp doesn’t need to “know” math or junkyard distortion theory, it has no problem contriving arbitrary complexity—as long as said complexity is solidly situated within the feedback loop.

Life is feedback. Evolution is feedback. Feedback is where the magic lies. *We live within the protective embrace of negative feedback*. And if that sounds off, consider that maybe our heads aren’t on straight—thanks to modernity—which is part of the whole problem.

# When Loops Break

Most mutations or behavioral changes transpire solidly within closed-loop negative feedback systems already long-established. The parameters of any loop may change, leading to a shifting equilibrium. But deep context provides safety. The system can accommodate tweaks: bending rather than breaking. One could say that the feedback loops comprising ecology evolve *themselves*. Evolution is not a bunch of isolated changes, but a fully-integrated *co-evolution* of many species *and* of the loops that bind them all together. Generally speaking, persistently-intact negative feedback loops are the stable geniuses supporting the Community of Life. Beings are born, live, and die deeply ensconced within them.

Sometimes an organism tries something entirely novel, either breaking existing loops or simply managing without relevant ecological loops in place. Such operation is open-loop, which means the outcome is highly unpredictable. Even more dangerous is instantiation of positive feedback insufficiently countered by negative feedback. Now a runaway process can change ecological relationships rapidly and dramatically.

The universe does not tolerate positive feedback for long. In the case of op-amps, power supply voltages limit the runaway. If a star goes supernova, it blows up (positive feedback) but that itself produces a strong negative feedback that prevents the “blowing up” from continuing forever: it runs out of fuel. A population explosion is *always* ultimately limited by “external” factors.

As explored in the [deviations post](https://dothemath.ucsd.edu/2026/03/ecological-deviation-application/), fire, stone tools, and horticulture began as open-loop experiments, but have persisted long enough that the Community of life adapted appropriate negative feedback stability around these practices (e.g., African megafauna survived). Migration from Africa was an open-loop and even positive-feedback phenomenon that did a fair bit of damage, but like a supernova explosion ran out of fuel (continents). Agriculture broke out of established negative-feedback arrangements, instituting a number of open-loop and positive-feedback behaviors that initiated a marked expansion—still in progress at an accelerated rate (characteristic of positive feedback). Late-stage modernity (fossil fuels, etc.) established even more positive-feedback situations as we screech and squeal and careen toward the rails (planetary limits).

I may get in trouble from the Human Reich, here, but we also opened the loop on the usual selective pressures of evolution by developing work-arounds for poor health and fitness. If a similar feat of preservation were applied across the board from adorable chickadees and fawns to thistles and mosquitos (eliminating infant mortality, for example, and supporting virtually any malady), then chaos would ensue: not only in numbers, but in fitness. Arbitrary configurations no longer “fit” in an ecological context. I even wonder if the increasing preponderance of poor human health has some component (among others) in basically releasing ourselves from age-old negative feedback safety mechanisms. We went open-loop, which isn’t how we got here as a species.

Relatedly, the normal feedback loops for honeybees—selective pressures from a broader ecology—were hijacked by human desires and market forces, substituting selective pressure for traits like docility, queen/split suppression, and honey production. Having broken ecological loops, these “poodle” bees have become vulnerable to a huge raft of maladies. During the pandemic shutdown I played host to a feral set of bees for a year, who were more aggressive than my neighbor’s “[boughten](https://youarecurrent.com/2015/04/07/column-little-grammar-question-on-the-prairie/)” bees, which were high-bred for “desirable” traits. By comparison, my buzzy coyote companions were far better wild foragers, had zero problems with wax moths or mites, would steal unguarded nectar from the neighbor’s bees, and split like maniacs as successful reproducers (the first queen out of a cell did not kill other unborn queens: all got their chance to set up a new shop). The feral bees were still well-ensconced in ecological feedback loops, and were far healthier for it.

# Bring the Magic Back

Negative feedback has magic in it. It reflects tested ([vetted](https://dothemath.ucsd.edu/2026/03/ecological-deviation-application/)) [wisdom](https://dothemath.ucsd.edu/2024/01/a-religion-of-life/). It can contrive an inverse-dog simply by being hyper-attentive to the *result* in a complete context. What would you feed a dog to get caviar out? The op-amp figures it out.

By pulling away from the Community of Life, some humans assumed the role of producing our own, new magic. But like the [Sorcerer’s Apprentice](https://video.disney.com/watch/sorcerer-s-apprentice-fantasia-4ea9ebc01a74ea59a5867853), they had no clue what they were doing. They (we) eschewed negative feedback, happily went open-loop in many respects and established positive feedback loops in others: all this with no time-tested grasp on consequences. Perhaps we’re the first species possessing that capability, now quickly learning the perils of [meat-brains](https://dothemath.ucsd.edu/2024/12/shortcut-brains/) as large as ours. Cognition is no substitute for ecological wisdom and long-established negative feedback networks.

The entire Community of Life—humans included—were better off when shrouded in the mysterious magic of the living world: held in awe, humility, and respect. We came into being inside the feedback loop, and [threaten to destroy much](https://dothemath.ucsd.edu/2025/09/is-the-6me-hyperbole/) when presuming to extract ourselves from its magical protection.

Views: 1934

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2026%2F03%2Fthe-magic-of-feedback%2F&linkname=The%20Magic%20of%20Feedback "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2026%2F03%2Fthe-magic-of-feedback%2F&linkname=The%20Magic%20of%20Feedback "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2026%2F03%2Fthe-magic-of-feedback%2F&linkname=The%20Magic%20of%20Feedback "Email")[](https://www.addtoany.com/share)
