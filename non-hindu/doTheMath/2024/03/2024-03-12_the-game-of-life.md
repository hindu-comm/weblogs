+++
title = "The Game of Life"
full_title = "The Game of Life"
upstream_url = "https://dothemath.ucsd.edu/2024/03/the-game-of-life/"
date = "2024-03-12"

+++
Source: [here](https://dothemath.ucsd.edu/2024/03/the-game-of-life/).

The Game of Life

<div id="attachment_5444" class="wp-caption alignright" style="width: 310px">

[![](https://dothemath.ucsd.edu/wp-content/uploads/2024/03/acorn-400-300x300.png)](https://dothemath.ucsd.edu/wp-content/uploads/2024/03/acorn-400.png)

Step 400 of the acorn methuselah. Gliders exit at 12:30 and 5:00.

</div>

Despite a lifetime of overlap, and many opportunities to cross paths, I am only now learning of the [Game of Life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life), introduced by John Conway in 1970—the same year that I was introduced to the world. After a few exploratory hours, I knew I’d have to share the insights I gained from it relating to how we react to the present predicament.

What is it that I mean by The Game of Life? Aren’t we all caught up in it? I refer, here, to a zero-player “game” taking place on a two-dimensional grid of square cells (pixels) that can either be alive (on; black) or dead (off; white). Only two simple rules govern whether a cell will live or die in the next time step of the game:

1.  Only “live” squares having two or three adjacent live neighbors (out
    of 8 possible) survive to the next step. 2.  An empty (“dead”) square having exactly three live neighbors will be
    “born” into living status on the next step.

The first rule captures a sense of balanced population density: too sparse and survival is hard; too dense and overshoot kills. The second rule is a sexy three-way approach to procreation. Settle down, people.

A surprising degree of complexity emerges from these simple rules, whose deterministic prescription nonetheless leads to essentially unpredictable outcomes. The lessons and parallels to real life—and even breakdowns in the comparison—are highly instructive, I find.

## Emergent Complexity

The first point of amazement is how cool the outcomes to such simple rules can be. Small sets of a dozen or fewer “starter” cells can cascade into surprisingly intricate and dynamic patterns—leaving behind persistent structures, evolving over impressively long times (sometimes indefinite), and producing a menagerie of different “animals” of varying complexity. One can even create logic gates and thus a computer—and then [run the Game of Life](https://www.youtube.com/watch?v=xP5-iIeKXE8) **on this computer**!

Many of the emerging structures have acquired names in a [Game of Life lexicon](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life#Examples_of_patterns). Stable, static structures (“still lifes”) called blocks, beehives, loafs, ponds, boats, and ships are common products. Periodically repeating patterns (oscillators) called blinkers, toads, beacons, pulsars, and the penta-decathlon run through a sequence of morphologies before returning to the original state and starting over again. A really cool class called “spaceships” execute a repeating pattern that also shifts its position in the process so that it translates across the space as it goes. The simplest of these is a ubiquitous 5-cell arrangement called a “[glider](https://conwaylife.com/wiki/Glider)” (figure below) that moves like a bishop on a chess board and appears as a spontaneous creation in many runs. A few special arrangements called “[glider guns](https://conwaylife.com/wiki/Gosper_glider_gun)” have been found that spit out a steady barrage of gliders. Some spaceships, called “puffers” leave a trail of debris that could be any of these previously named structures. In fact, [one design](https://conwaylife.com/wiki/Breeder_1) leaves—of all things—*glider guns* in its wake so that the growth of live cells is quadratic as an ever-expanding armada of gliders sets off to nowhere.

<div id="attachment_5499" class="wp-caption alignnone" style="width: 310px">

[![](https://dothemath.ucsd.edu/wp-content/uploads/2024/03/GoL-gliders-1-300x300.png)](https://dothemath.ucsd.edu/wp-content/uploads/2024/03/GoL-gliders-1.png)

Five gliders in a line traveling to lower right, showing the four evolutionary steps before repeating. Each one will land on the next one’s position 17 steps later.

</div>

I encourage you to take a detour and play around, if this “world” is new to you. A number of sites provide a means to launch graphical simulations, including an [extensive Wiki page](https://conwaylife.com/wiki/Main_Page) and a [Lexicon page](https://playgameoflife.com/lexicon). Don’t forget to come back to this article three hours later.

That all of these phenomena can arise from such simple rules in limited dimensionality is an important lesson. It doesn’t take much.

## Unpredictability

The emergent complexity is significant enough that one cannot look at a random assortment of even a half-dozen live cells (close enough to each other not to trivially die out) and decide how long it might run or what sorts of structures might emerge. The only way to know is to execute the sequence. This fact makes the outcome *seem* random, even if it is not.

Industrious explorers made a game out of finding long-lived runs based on compact, simple beginnings (called “methuselahs”; [see a long-lived example](https://conwaylife.com/wiki/47575M#Smaller_forms) and [this table](https://conwaylife.com/wiki/List_of_long-lived_methuselahs) summarizing the properties of various instances). For example, the rabbits and bunnies can go for over 17,000 steps, resulting in over 1,700 populated static/oscillating cells (and a few dozen escaping gliders) all starting from fewer than a dozen “live” cells.

<div id="attachment_5447" class="wp-caption alignnone" style="width: 594px">

[![](https://dothemath.ucsd.edu/wp-content/uploads/2024/03/GoL-pentas-1024x303.png)](https://dothemath.ucsd.edu/wp-content/uploads/2024/03/GoL-pentas.png)

Slight variations produce dramatic differences: one of these dies completely in 3 steps, while another goes 1103 steps and releases six gliders.

</div>

To illustrate the difficulty of prediction, one of the above shapes (in isolation) goes on for 1,103 steps and releases six gliders, while others die after three steps, enter oscillation after 6, or become a static loaf after 5. They only differ in the placement of one cell. You can try them in an interactive tool using, for instance, the [R-pentomino](https://conwaylife.com/wiki/R-pentomino) as a starting point (launch via the box in the upper right and use the draw tool to toggle pixels; run/play or do one step at a time). This degree of unpredictability is just from a five-cell example (results from left to right: dead in 3; loaf in 5; methuselah; 4 blinkers in 6). In our real world of *vastly* more richly-interacting agents, how could one possibly predict the future even under perfectly deterministic rules? I encourage you *not* to think about your own brain at this point. Save that for later.

## Determinism

The Game of Life is strictly deterministic: the same initial pattern will *always* produce the same result, time after time. After all, the rules are simple and operate without exception.

That said, the unpredictability (without actually running the full simulation) makes it *feel* open-ended. Deterministic behavior can therefore have every appearance of being wild and untamed—a very important lesson.

Sure, we might peek into sub-units and understand the complex emergence of, say, a glider and be able to describe its workings, thus predicting that an isolated glider goes on “forever.” But outcomes of *interactions* are much harder to predict. And guess what: the real world is full of interactions (unlike GoL that starts in the middle of an infinite void).

## Invalidities

To be sure, our world is *not* well represented by The Game of Life (GoL), which possesses the merest shadow of the degree of complexity found in our real world. The table below highlights some of the key differences.

|                |                  |                        | |----------------|------------------|------------------------| | Attribute      | Game of Life     | Real World             | | Dimensionality | 2                | 3                      | | Space          | discrete squares | continuous             | | Time           | discrete steps   | continuous             | | Range          | adjacent only    | infinite               | | Reactions      | binary: live/die | continuous             | | States         | 2                | multitude              | | Rules          | 2, simple        | many, nuanced          | | Surroundings   | empty void       | connected, interactive | | Determinism    | strict           | quantum probabilities  |

In every way, the GoL is simpler than the real world: fewer dimensions; more restricted interaction range; binary states and reactions; and only two rules (vs. what is found in a physics textbook). Many GoL simulations produce gliders heading off into the void, predictably lasting “forever” as they cruise into empty space. Life on Earth affords no such escape from interaction.

To me, the myriad shortcomings of the GoL model in representing the real world **only serve to emphasize how much richer emergent complexity can be under a richer contextual framework**. I mean, if the unpredictable swirling conflagrations of activity one sees in GoL runs can arise in such a restricted space, it boggles the mind to consider what might emerge on a far more elaborate stage.

Indeed, the emergence of even single-cellular life boggles our minds: we cannot fully connect the dots from first principles as to how such magnificent beasts arose. The emergence of consciousness in animals is *literally* mind-boggling—and always will be, in all likelihood. Yet, at *least* as challenging is coming up with some clever mechanism that could act to **defeat** the emergence of complexity in our world. Just try to stop it! We simply can’t rule out that the world we see is emergent from basic relationships between particles—even if we can’t comprehend the scope of the complexity using our own limited brains.

<div id="attachment_5465" class="wp-caption alignnone" style="width: 1342px">

[![](https://dothemath.ucsd.edu/wp-content/uploads/2024/03/GoL-breeder-1.png)](https://dothemath.ucsd.edu/wp-content/uploads/2024/03/GoL-breeder-1.png)

“Breeder 1” puffer that generates glider guns in its wake.

</div>

Think about it this way: imagine looking at the [glider gun puffer](https://conwaylife.com/wiki/Breeder_1) (image above; a “breeder”) in the context of the simple rules of GoL. How easy is it to understand what each part does and how its morphology cyclicly transforms **without** explicitly executing the algorithmic sequence of steps? It’s nearly impossible, and keep in mind that this “device”—along with its rule set—is pathetically simple compared to a microbe. Even so, the GoL is *already* complex enough that the only way to appreciate outcomes is to just run the sim. I invite you to think on that.

## Determinism in Reality

Now shift, if you can, to consideration of our physical universe involving quarks, electrons, gluons, photons—all interacting via four fundamental forces (two of which are infinite range)—based on masses, electric charges, “color charges,” spin states, relative positions, momenta (velocities)…all in three dimensions and all in relationship (not just nearest-neighbor as in GoL). Can funky complexity emerge, even if everything is following a finite rule set of physics? First: who are we to say no? What hubris would accompany such a claim? Second: look around! Gaze at your own navel. At this point it’s okay to think about your brain.

The physical universe is roiling with interactions, and even though the rules have been elucidated, the consequences have not. One can imagine the real world as being a much more elaborate version of the Game of Life, applying the rules one step at a time (except time is now continuous, inviting the use of calculus). However, the universe throws in a monkey wrench, in that every interaction at the quantum level has a probabilistic nature—ruining perfect clockwork determinism. But even these probabilities operate within unbreakable rules, in a quasi-deterministic fashion.

The universe, therefore, appears to simply unfold by a set of rules—quantum indeterminacy included. Many find this proposition to be extremely distasteful, and reject it out-of-hand based on no evidence that things behave otherwise (while we also lack evidence that the rules of physics are *ever* broken). Indeed, nothing about life **feels** deterministic. It *feels* open-ended and subject to our impulses/control. Likewise, watching a GoL run, one is struck by a sense of unpredictability and seeming open-endedness, even though we know intellectually that it is even more deterministic than the actual world (no probabilistic element thrown in).

## Your Role in Life

Just as the only way to ascertain the outcome of a non-trivial GoL setup is to run the damn thing, the only way to appreciate the future states of our universe is to *experience* the outcome of our own “simulation.” Thus, we are *operationally* open-ended, even if living on a quasi-deterministic foundation.

A common reaction to the prospect of determinism is aversion to the notion that we are slaves to a script—merely executing a known future. Life **really** doesn’t feel like that! Yet, we are indeed slaves to physics (take that as a dare, if you wish), but “script” is taking it a bit far. There is not, and never has been a script. The future is not, and cannot be known. Just as one might create a GoL initial setup and define rules, this act is far short of scripting outcomes (and the inverse problem of coming up with initial conditions to produce any desired complex outcome is essentially impossible, unless learning from prior “forward” run behavior). In the GoL, we can’t know what “script” will emerge (from non-trivial starting points), just as no earthly being can possibly know in every detail how the universe—and life and individual choices—will evolve. The universe can dutifully follow rules without exception and without being scripted. It’s a self-writing play that goes where it must, following its nose.

Your “role” in the giant act is, therefore, unknown to you or to anybody. Let’s say that in reaction to information you receive about the predicament we’re in (e.g., from this blog and other sources) you are convinced to embrace a different vision for the future that you would like to help realize. That’s great! Maybe that’s your role. But is it truly *your own* choice if you’re a compulsory actor in a quasi-deterministic evolution? Who cares? Sure? Why make this about ownership for the sake of vanity? Why not focus on the *outcome*, and be pleased to play any role in its achievement? If that’s the way the universe happens to unfold, and you played a part in reaction to the full history of stimuli presented to you, then why protest?

Of course, if you’re the sort that refuses to go with the flow in this way, then that too is part of how the universe unfolds—not ruled out—and your role will be what it is. Determinism easily accommodates (crafts?) those whose brains reject it.

Consider that this post could, in principle, persuade someone to relinquish non-productive concern about their existential specialness, appreciating that they are simply a magnificent cog in an intricate universe of emergent complexity, humbly accepting a role as a part of nature (not its master, steward, underlying purpose, owner, etc.), rolling up sleeves and starting to do *something* to change the course of modernity at the local level—however modest. Such motivation would not operate outside of a tangled deterministic history of stimuli and responses, and Ill take what we can get!

## Reconciling My Role

How is it that I keep pressing for change when I call [free will](https://dothemath.ucsd.edu/2024/01/free-will-good-riddance/) an [illusion](https://dothemath.ucsd.edu/2024/02/mysterious-materialism/) and [give myself](https://dothemath.ucsd.edu/2024/01/a-religion-of-life/) to the quasi-deterministic flow of nature? Why isn’t my reaction to absolve myself of any responsibility and spend my days trying to set records for Ding Dong consumption?

Well, apparently I’m not wired that way—although the Ding Dong option is tempting. I am a human being capable of absorbing and reacting to situational stimuli in the context of my evolutionary history as a social animal. Just as every fiber of my being reacts in vehement opposition to the thought of ripping a leg off a baby, a coyote, a newt, or even an ant, I react in horror to the knowledge that modernity has initiated the sixth mass extinction—quite senselessly. Call me crazy, but my impulse is to try to reverse this practice and avert a tragic outcome. Stimulus—response. No intervention to “deterministic” physics is necessary, and I’m 100% okay with that (not that it’s for me to say, anyway).

I guess the reason I keep returning to this theme of emergent complexity, seemingly open-ended determinism, and free-will-dismissal is that I see removal of pretense as a crucial part of the journey. [Human supremacism](https://dothemath.ucsd.edu/2022/02/human-exceptionalism/) is perhaps the core flaw in the operating system of modernity, and self-elevation to something special/transcendent is part and parcel of this attitude. Humility is better realized by accepting our existence as nothing more than incredible products of evolution, united in kinship to all other life, responding to troublesome inputs in a staggeringly sophisticated way.

Humans have demonstrated quite convincingly the capacity to inflict great harm to ecological health at a global scale. What happens next depends on the unpredictable outcome of the battle between concerns for **self** (needs, desires, drives, competition, procreation, the present and vested near-future) and **not-self** (social groups, cooperation, the community of life, biodiversity, the far future). I [have argued](https://dothemath.ucsd.edu/2024/03/lets-make-a-deal/) that we don’t even have the option to continue satisfying selfish desires in the face of ecological collapse: we depend on the entire community of life in ways we do not appreciate (and never will, fully). So, human self-focus becomes self-defeating in the full context. This puts me strongly in the camp of advocating for *not-self* concern. Again, it’s part of my wiring as a social animal. I seem to care.

In the end, it comes down to whether this creature who evolved a set of skills so exceptional that it could destroy the world has also developed a sufficiently broad social sense to value the more-than-human world enough to protect it from itself. There are no guarantees at all that evolution contrived to make restraint and wisdom powerful enough to prevail over the exercise of power. At present, the outcome is not looking so great—perhaps one of many experimental [blunders of evolution](https://dothemath.ucsd.edu/2021/04/in-breach-of-contract/). Yet, I am bolstered by knowledge that some (Indigenous) cultures have prioritized the community of life and exercised the wisdom to within bounds. That’s huge!

Whatever the case, I will continue to play the role it seems I am set out to play, and hope that I happen to be on the “right side of history.” In the game of life, the only way to know is to keep playing.

*Postscript*: I found [this article](https://www.nytimes.com/2020/12/28/science/math-conway-game-of-life.html) to be an informative history and commentary on The Game of Life.

Hits: 2266

<div class="addtoany_share_save_container addtoany_content addtoany_content_bottom">

<div class="a2a_kit a2a_kit_size_32 addtoany_list" a2a-title="The Game of Life" a2a-url="https://dothemath.ucsd.edu/2024/03/the-game-of-life/">

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2024%2F03%2Fthe-game-of-life%2F&linkname=The%20Game%20of%20Life "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2024%2F03%2Fthe-game-of-life%2F&linkname=The%20Game%20of%20Life "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2024%2F03%2Fthe-game-of-life%2F&linkname=The%20Game%20of%20Life "Email")[](https://www.addtoany.com/share)

</div>

</div>
