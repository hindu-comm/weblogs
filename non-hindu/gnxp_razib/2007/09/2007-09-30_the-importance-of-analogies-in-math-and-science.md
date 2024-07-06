+++
title = "The importance of"
full_title = "The importance of analogies in math and science"
date = "2007-09-30"
upstream_url = "https://www.gnxp.com/WordPress/2007/09/30/the-importance-of-analogies-in-math-and-science/"

+++
Source: [here](https://www.gnxp.com/WordPress/2007/09/30/the-importance-of-analogies-in-math-and-science/).

The importance of analogies in math and science

“Good mathematicians see analogies. Great mathematicians see analogies between analogies.”  
—[Stefan Banach](https://en.wikipedia.org/wiki/Stefan_Banach)

A recent Cognitive Daily post called [“Why aren’t more women in science”](http://scienceblogs.com/cognitivedaily/2007/09/why_arent_more_women_in_scienc.php) (part 1) reviews some of the lit on sex differences in cognitive abilities. Dave Munger notes:

> In the verbal portion of the \[SAT\] test, the male advantage is eliminated if the analogy portion of the test is eliminated; arguably this is more a test of mapping relationships than literacy.

The analogy portion was, of course, scrapped as of the spring 2005 SAT. \[1\] The boldfaced clause above shows why it matters more than the other Verbal portions: figuring out relationships between ideas matters, and reporting what some author said does not. Analogies are highly g-loaded, reading comprehension much less so. But aside from better detecting who the smarties are, analogies are more reflective of real-world math, science, and engineering. (And they matter in the humanities too \[2\].) If A got one more math question than B, but B got three more analogy questions than A, I’d bet on B doing better in math, even if an IQ test showed they had the same IQ.

What follows is mostly a diversion to show the importance of analogies in math, starting with high school material and moving to some college material. I hope you learn something new, but mostly the goal is to put it on the record, with examples, how important a person’s verbal analogy score is in predicting their success in math and science.

Example 1. A bouncy-ball is dropped from 2 feet, and after hitting the ground, bounces up only 1/2 as high as its previous maximum height. Pretend that it bounces forever like this. In the long run, how much distance does the ball travel?

We can make a table that shows how much distance the ball travels in a particular trip, either up or down, like so:

Trip 1, 2, 3, 4, 5, 6, 7, …  
Dist. 2, 1, 1, 1/2, 1/2, 1/4, 1/4, …

This problem is introduced in a pre-calculus class during the unit on the sum of an infinite [geometric series](https://en.wikipedia.org/wiki/Geometric_series) — infinite because it starts but never ends, and “geometric” meaning you multiply by the same number to get from one term to the next. The formula for such a sum is t1 / (1 – r), where t1 is the first term, and r is the constant that multiplies one term to get to the next. So if we only had these values, we’d be all set! Unfortunately, if we guess that r is 1/2, when we try to go from 1 to 1 — we don’t multiply by 1/2 anymore (or from 1/2 to 1/2). Damn. Plainly, the above series is not geometric, and at that point most students will opt to make better use of their time by yakking with friends on their cell phone.

Ah, but the students in the class who are good analogical thinkers will notice a geometric series hiding behind the series above — in fact, they’ll discover two of them. The terms of one are interlocking with the terms of the other, like two rows of teeth that complete a zipper. That analogy suggests a strategy: unzip the above series. Then we have two series that go:

2, 1, 1/2, 1/4, … and  
1, 1/2, 1/4, …

Bingo! In each of these, you multiply by a constant (1/2) to get from one term to the next. And we know the first term of each, so we can plug in values for t1 and r in the sum formula. We get 2 / (1 – 1/2) = 4, and 1 / (1 – 1/2) = 2. So all together, the ball traveled 6 feet. That’s a neat analogy, but it only makes sense when there are two series meshed into one. We’d like to generalize to any number of series that dovetail into one — and no one makes zippers with more than two rows of teeth. So a better analogy might be the following:

[](https://www.gnxp.com/blog/uploaded_images/series-772753.JPG)  
Here there are two strands woven one around the other infinitely, with beads bearing numbers that face us, and there is a knot at the start where the strands fuse. Could we think up series with three or more geometric series hiding inside them? Sure, just as we could make a rope with three or more strands. And to make that series easy to solve, we would just unbraid the strands and work with the beads of each one separately. See note \[3\] for more uses of this braid analogy.

Example 2. Here are some (x,y) pairs associated with a function. What is the degree of this function? That is, does it look like x, x^2, x^3, etc.?  
x = 1, 2, 3, 4, 5, 6…  
y = 2, 14, 34, 62, 98, 142…

This problem also comes from high school math — or middle school, if you took algebra then. There, you were taught to look for the difference between consecutive terms, and maybe repeat this process, until you got a sequence of the same number. The number of runs you have to make is the degree of the function. So for the above, the differences are:  
12, 20, 28, 36, 44

OK, not the same number, but take the difference again:  
8, 8, 8, 8

Ta-da. We had to go through 2 runs, so it must be some function like x^2 (in fact, it is 4x^2 – 2). I guarantee you never knew why this worked when you learned it — and even after calculus or more advanced math, you may still have treated it as a mysterious trick. But there are analogies between discrete and continuous areas of math, and they are pervasive. If you took at least a semester of calculus, you know that if you take the 1st derivative of a function like 4x^2 – 2, you get something with the independent variable still in it — 8x. And sure enough, in our discrete case, the first differences are 8x plus a constant 4.

But if you then take the derivative of the derivative, you get a constant — 8, the same 8 that appeared in our constant sequence after the 2nd run. A constant second difference in the discrete case is analogous to a constant second derivative in the continuous case. That also shows why you knew, back in high school, that you didn’t have a polynomial function like x or x^2 or x^3 when you saw something like this:  
x = 1, 2, 3, 4, 5, 6…  
y = 2, 4, 8, 16, 32, 64…

You can take differences of differences of differences of… and you’ll never get a constnant sequence for this function, which is 2^x. In first-semester calculus, you learned that e^x is its own derivative, so that if you keep taking the derivative over and over, you always get back e^x — the independent variable never goes away, so you never get a constant. This resilience to your effort to tease a constant derivative out of it is true of all exponential functions, which by analogy tells us that we’d never come up with a constant difference in the discrete case above.

Since there are a billion other discrete-continuous analogies, I’ll leave it there. I don’t think they’re that neat since it’s only like switching between a British and American accent, not like translating between Farsi and Chinese. On a closing note, the entire domain of [represenation theory](https://en.wikipedia.org/wiki/Representation_theory) in algebra is based on finding good analogies: they attempt to better understand how some [group](https://en.wikipedia.org/wiki/Group_%28mathematics%29) works by casting the problem in terms of matrices and linear algebra, which are better understood. All of this shows how indispensable this way of thinking is to fields that many assume are primarily about visuospatial skills (though those are key too). Analogies are to all types of thinkers what SONAR and nets are to deep-sea fishermen regardless of which species they hunt.

\[1\] According to CollegeBoard’s [2007 national report](http://www.collegeboard.com/prod_%20downloads/about/news_info/cbsenior/yr2007/national-report.pdf) of college-bound seniors, it does appear that within the past couple of years, the male mean for Verbal is only about two points above the female mean, shrinking from a difference of about 11 to 12 points that had persisted since about 1980. And at the high end, in 2007, 1.98 % of males and 1.84 % of females scored 750 – 800. Data from other years on the elite scorers are not contained in the 2007 report, and I’m not interested enough in this topic to pursue them. The point is that gutting the analogy portion seems to have served its purpose.

\[2\] When the retiring of the analogy questions was announced, an educator named Ted Sutton got an [op-ed](http://www.boston.com/news/education/k_12/articles/2005/01/21/analogies_are_to_sats_what_babies_are_to_bathwater/) into the very liberal Boston Globe and made a [guest appearance](http://www.onpointradio.org/shows/2005/01/20050125_a_main.asp) on the very liberal radio show On Point (which airs on NPR). He lamented the change, focusing on the centrality of analogies to the great philosophical and humanistic traditions. Older-style liberals like Sutton appear unaware that their social engineering cousins are the ones responsible for flushing great ideas down the drain, so that the gap between the sexes on a test might close.

At least there are still analogies on the GRE — despite a plan to [re-vamp the test](https://www.gnxp.com/blog/2007/04/new-gre-cancelled-cost-of-attempted-gap.php) with the same gap-narrowing agenda in mind. And thank God for the [Miller Analogies Test](https://en.wikipedia.org/wiki/Miller_Analogies_Test) — not a single “how does the author most likely feel about X” question at all!

\[3\] The braid idea can also guide your intuition when you have a homework problem in a college-level course that says: “Prove that a countable union of countable sets is countable.” I provided a [visual proof here](https://akinokure.blogspot.com/2007/06/visual-countable-union-of-countable.html) (with a more detailed proof at the end), but I didn’t think of the braid analogy, which makes it even easier to picture. The argument is as I wrote before, but when you’re introducing yet another countable set into the union, it’s like adding a new strand to a rope. You look at the place where the n strands have shown themselves once — and before the first strand winds around the second time, you push it over and braid in your new strand. When they n strands have shown up twice, you push the first strand over before it winds around the third time, and there’s the second place where the new strand goes. And so on to infinity. The union of these strands is a rope whose beads are countable and, more importantly, ordered in a straightforward way.

More explicitly, we can think of the strands as equivalence classes and the rope as the space they fill out. We can imagine a rope that extends infinitely in either direction, like the even and odd integers woven together. We’ve already seen a rope with a knot but which continues to weave itself forever in one direction. A rope with knots at both ends is pretty boring — unless they were the same point, i.e. the rope circled back so that each strand fed back into itself, as with a sequence that’s cyclic (for instance: x, y, x^2, y^2, x^3, y^3, x, y, …).

### Related Posts:

- [Analogies
  seconded](https://www.gnxp.com/WordPress/2009/01/12/analogies-seconded/) - [The New SAT](https://www.gnxp.com/WordPress/2005/03/13/the-new-sat/) - [Scores on the new SAT for the 2006 cohort of
  college-bound…](https://www.gnxp.com/WordPress/2007/04/09/scores-on-the-new-sat-for-the-2006-cohort-of-college-bound-seniors-sex-and-ethnic-breakdown/) - [Predicting academic achievement with cognitive
  ability](https://www.gnxp.com/WordPress/2006/07/20/predicting-academic-achievement-with-cognitive-ability/) - [New GRE cancelled - the cost of attempted
  gap-reduction?](https://www.gnxp.com/WordPress/2007/04/04/new-gre-cancelled-the-cost-of-attempted-gap-reduction/) - [Standardized test scores: math and
  verbal](https://www.gnxp.com/WordPress/2012/04/16/standardized-test-scores-math-and-verbal/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F09%2F30%2Fthe-importance-of-analogies-in-math-and-science%2F&linkname=The%20importance%20of%20analogies%20in%20math%20and%20science "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F09%2F30%2Fthe-importance-of-analogies-in-math-and-science%2F&linkname=The%20importance%20of%20analogies%20in%20math%20and%20science "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F09%2F30%2Fthe-importance-of-analogies-in-math-and-science%2F&linkname=The%20importance%20of%20analogies%20in%20math%20and%20science "Email")[](https://www.addtoany.com/share)
