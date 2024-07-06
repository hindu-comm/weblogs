+++
title = "Haldane's Selection"
full_title = "Haldane's Selection Theorem"
date = "2007-01-11"
upstream_url = "https://www.gnxp.com/WordPress/2007/01/11/haldane-s-selection-theorem/"

+++
Source: [here](https://www.gnxp.com/WordPress/2007/01/11/haldane-s-selection-theorem/).

Haldane's Selection Theorem

Razib has several times mentioned an important theorem of population genetics, credited to **J. B. S. Haldane**, that the probability of a single favourable mutation surviving and spreading throughout a population is approximately 2s, where s is its selective advantage relative to other alleles. So for example if a mutation has a selective advantage of 1 per cent, it will have approximately a 2 per cent chance of ultimately sweeping through the population. This may seem a low probability, but if the same mutation recurs more than a few dozen times in the species, it is virtually certain to be successful. A recent [paper](https://www.gnxp.com/blog/2006/12/now-it-can-be-told.php) by **John Hawks** and **Greg Cochran** makes a central use of Haldane’s theorem.

As a matter of historical curiosity I wanted to see Haldane’s original statement of this principle, and how he derived it.

Hawks and Cochran give the citation ‘Haldane, J. B. S. (1927): A mathematical theory of natural and artificial selection, part v: Selection and mutation. Proceedings of the Cambridge Philosophical Society, 28, 838-44.’ I find that the correct volume number is 23, not 28. The same incorrect citation is given by Crow and Kimura’s An Introduction to Population Genetics Theory (1970).

The paper is also reprinted in Selected Genetics Papers of J. B. S. Haldane, edited with an introduction by Krishna R. Dronamraju, Garland Publishing, NY, 1990, at pp. 90-96. I have transcribed the key passage from the paper below. Incidentally, Haldane uses k, rather than s, for the selective advantage, but this is a trivial matter of notation. More important, Haldane’s theorem only applies where the population is sufficiently large. If the breeding population n is very small (less than about 50) there is a significant chance that a single mutation will be fixed by genetic drift before selection has had much effect. For a single neutral or favourable mutation there is always a probability of at least 1/2n that it will ultimately be fixed, since in the absence of recurrent mutation one of the 2n genes in the population will ultimately be the ancestor of all surviving genes.

It is interesting that Haldane himself does not claim great novelty for his 1927 theorem, but presents it as an application of the methods set out by R. A. Fisher in his 1922 paper ‘On the dominance ratio’. Fisher himself later gave a more elaborate treatment of the same problem in a 1930 paper, ‘The Distribution of Gene Ratios for Rare Mutations’, Proceedings of the Royal Society of Edinburgh, 1930, 50, 205-20. (Like most of Fisher’s papers, this is available online from the [Fisher archives](http://digital.library.adelaide.edu.au/coll/special//fisher/) at Adelaide.) This includes the conclusion that:

> The probability of a mutant, enjoying a small selective advantage a, > spreading until it establishes itself throughout the entire population > is thus found to be 2a/(1 – e^-4an); it is easy to see that with an > indefinitely large population, or in any case if 4an \[population size x selective advantage\] is large, this expression reduces to 2a. Thus a mutation conferring a selective advantage of 1 per cent will have practically a 2 per cent chance of establishing itself.

In 1930 Fisher, rather characteristically, did not cite Haldane’s 1927 treatment of the selection problem. Sewall Wright, in his 1931 paper on ‘Evolution in Mendelian populations’, states a similar proposition and credits Fisher, but not Haldane, with prior publication. This might raise a question whether Haldane or Fisher should be given the main credit for the theorem. As far as I can judge, Haldane does make a heavy use of Fisher’s 1922 methods, but Fisher himself did not (in 1922) explicitly calculate the probability that an advantageous mutation would survive, and Haldane’s application of Fisher’s methods in 1927 was by no means as easy as falling off a log. I think therefore that Haldane does deserve the credit for the theorem itself.

In any case, as often turns out in issues of priority, there are neglected earlier candidates. As early as 1873, the Rev H. W. Watson, in response to a request from his friend Francis Galton, had published a method for calculating the ‘extinction of surnames’ which contains much of the technique later used by Fisher for calculating the random extinction of genes. And even earlier, in 1845, a French mathematician called Bienayme had published a brief paper with results suggesting that he may have discovered some of the same methods, though he did not give details. (See Michael Bulmer, Francis Galton: Pioneer of Heredity and Biometry (2003), pp.156-60.) There is nothing to suggest that Fisher or Haldane knew of these earlier efforts.

The following extract from Haldane’s 1927 paper contains his proof of the theorem. I cannot reproduce all of the mathematical notation, so I will use S to indicate summation, x^n to indicate the n’th power of x, and x_a (etc) to indicate subscripts. I have added some comments (in square brackets) and notes in an attempt to explain the derivation, as far as I can follow it myself. No doubt much of this will be self-evident to expert mathematicians, but expert mathematicians have a tendency to underestimate the difficulty of following mathematical proofs for the rest of us.

EXTRACT

…the treatment of Fisher \[1922\] is followed.

In a large population let p_r be the chance that a factor \[allele\] present in a zygote at a given stage in the life-cycle will appear in r of its children in the next generation. If the individual considered is homozygous, this is the chance of leaving r children, if mutation is neglected. Let S p_r(x^r) = f(x) \[note 1\]. Therefore f(1) = 1, f(0) = p_0 \[note 2\], the probability of the factor disappearing, while f ‘ (1) = S rp_r, \[note 3\] i.e. the probable number of individuals possessing the factor in the next generation. The probability of m individuals bearing one each of the factors considered leaving r descendants is clearly the coefficient of x^r in \[f(x)\]^m, if we neglect the possibility of a mating between two such individuals, which we may legitimately do if m is small compared with the total number of the population. If then the probability of the factor being present in r zygotes of the nth generation be the coefficient of x^r in F(x), the corresponding probability in the (n + 1)th generation is the same coefficient in F\[f(x)\]. Hence if a single factor appears in one zygote, the probability of its presence in r zygotes after n generations is the coefficient of x in S(x) \[S has subscript f and superscript n\], i.e. f(f(f…f(x)…)), the operation being repeated n times \[note 4\]. The probability of its disappearance is therefore LtS(0) \[note 5\]. By Koenigs’ theorem this is the root of x = f(x) in the neighbourhood of zero \[note 6\].

Now in the case of a dominant factor appearing in a population in equilibrium, and conferring an advantage measured by k, as in Part I(5) \[of Haldane’s series of papers\] f ‘ (1) = 1 + k. Since f ‘ (x) and f ” (x) are positive, x = f(x) has two and only two real positive roots, one equal to unity, the other lying between 0 and 1, but near the latter value if k be small \[note 7\]. Hence any advantageous dominant factor which has once appeared has a finite chance of survival, however large the total population may be.

If a large number of offspring is possible, as in most organisms, the series p_n approximates to a Poisson series, provided that adult organisms be counted, and since  
f'(1) = 1 + k, f(x) = e^(1 + k)(x – 1). Hence the probability of extinction 1 – y is given by 1 – y = e^-(1 + k)y \[note 8\].

Hence (1 + k)y = -log(1 – y) \[note 9\]

and k = y/2 + (y^2)/3 + (y^3)/4 + … \[note 10\]

and if k be small, y = 2k approximately \[since the terms after y/2  
are orders of magnitude smaller\]. Hence an advantageous dominant gene has a probability 2k of survival after only a single appearance in an adult zygote, and if in the whole history of the species it appears more than log_e2/2k times \[the natural logarithm of 2, divided by 2k\] it will probably spread through the species. But, however large k may be, the factor may be extinguished after a single appearance. Thus, if k = 1, so that the new type probably leaves twice as many offspring as the normal, the probability of its extinction is still .203. If in any generation there are m dominant individuals the probability of extinction is reduced to y^m, where y is the smaller positive root of x = f(x). When k is small this reduces to (1 – 2k)^m. Hence if in any generation more than log_e2/2k adult dominants exist, the factor will probably spread through the whole population.

NOTES

\[Note 1\] Summation is over values of the subscript r from zero to infinity. Since r is the number of an individual’s offspring, it can only take integer values.

\[Note 2\] The sum is p_0(x^0) + p_1(x^1) + p_2(x^2) + p_3(x^3)… For the value x = 1 this equals p_0 + p_1 + p_2 + p_3… , which sums to 1, since the probabilities are mutually exclusive and cover all possible outcomes. For the value x = 0 the terms from p_1(x^1) onward are all equal to zero, so the series reduces to p_0(0^0), which = p_0 if we accept that 0^0 = 1. I am not sure that there is any agreed convention on this point, as the usual proofs that x^0 = 1 (e.g. 1 = (x^a)/(x^a) = x^(a – a) = x^0) break down for the case x = 0. Fisher, in his formulation of the series, presents it as p_0 + p_1(x^1) + p_2(x^2) + p_3(x^3), which avoids any doubt on this point.

\[Note 3\] Summation is over values of r from zero to infinity. The expression f ‘ (1) evidently means the first derivative of the function f(x) with respect to x, for the value x = 1. Each term in the sum f(x) has the form p_r(x^r), so by elementary calculus its first derivative is rp_r(x^(r – 1)), and the first derivative of the sum f(x) as a whole is the sum of the first derivatives of its component terms. But for the value x = 1 these each reduce to rp_r, so the first derivative of f(x) is equal to S rp_r, as in Haldane’s formula.

\[Note 4\] Haldane’s treatment here is closely based on Fisher, but uses different notation.

\[Note 5\] Lt is the limit as n goes to infinity, in other words as the function is iterated indefinitely with its own previous value as argument.

\[Note 6\] This part of the derivation evidently requires advanced knowledge of the theory of functions, and I can only take it on trust. Haldane gives the cryptic reference ‘Koenigs. Darb. Bull. (2) 7, p.340, 1883.’ I wondered if ‘Koenigs’ might be an error for ‘Koenig’, possibly Julius Koenig, but on consulting the Dictionary of Scientific Biography I found an entry for a French mathematician, Gabriel Koenigs (1858-1931). Among his many accomplishments, according to the DSB, Koenigs was ‘one of the first to take an interest in iteration theory’. Koenigs was also a pupil of Gaston Darboux, founder and editor of the Bulletin des Sciences Mathematiques et Astronomiques, sometimes known as ‘Darboux’s Bulletin’. So Haldane’s cryptic reference to ‘Darb. Bull.’ is probably to an article by Gabriel Koenigs in the Bulletin des Sciences Mathematiques et Astronomiques, 2nd series, volume 7, 1883, at p.340. I find that there is indeed an article by Koenigs, ‘Recherches sur les substitutions uniformes’, at the cited place, but its mathematics is far beyond me.

\[Note 7\] Haldane does not consider the trivial cases p_0 = 1, where the gene is always extinguished immediately, or p_1 = 1, where it always produces one and only one offspring per generation. In the first case f(x) would have the value 1 for all values of x, while in the second case it would have the value x for all values of x. For non-trivial cases the value of the function f(x) increases continually and at an increasing rate with increasing x, so the first and second derivatives of f(x) are positive. Haldane also states that the equation x = f(x) has two and only two real positive roots, one of which is 1, and the other between 0 and 1. I am not sure I could give a rigorous proof of this, but I suggest the following approach. If we plot a graph of the function y = f(x), for real positive values of x, then f(x) = y = x wherever the curve representing the function touches or intersects a line through the origin at 45 degrees to the axes. As f ‘ and f ” (the first and second derivatives) are both positive, the curve is concave upwards, i.e. it has just one ‘bend’, with the inner part of the bend on its upper side. The curve must start from the y axis at the value p_0, since we know that f(0) = p_0, which is somewhere between 0 and 1. We also know that f(1) = 1, so the curve must touch or intersect the 45 degree line at x = y = 1, which is accordingly a real positive root of x = f(x). The curve must therefore pass in some way from the point (x = 0, y = p_0), which is above the 45-degree line, to the point (x = 1, y = 1), which is on that line. As the curve is concave upward, it cannot touch or intersect a straight line in more than two points. Since it touches or intersects the 45-degree line at the point (x = 1, y = 1), there are three possible ways of doing so: (a) it is a tangent to the line at that point; (b) it intersects the line at that point from above the line (in its approach from its starting point on the y axis); or (c) it intersects the line from below the line. But it cannot be a tangent to the line at that point, because the first derivative of the function would then be equal to the slope of the line, which is 1, whereas by assumption the first derivative at that point is 1 + k, with non-zero k. Possibility (a) is therefore excluded. Possibility (b) can be excluded for a similar reason. If the curve intersects the 45-degree line from above, a tangent to the curve at that point must make an angle of less than 45 degrees with the x axis. But this means that the first derivative of the function at the point of intersection must be less than 1, whereas by assumption it is greater than 1. This leaves only possibility (c), that the curve intersects the line from below, which is consistent with the fact that the first derivative is greater than 1, so that a tangent to the curve would have an angle greater than 45 degrees. But this implies that in passing from (x = 0, y = p_0), which is above the line, to (x = 1, y = 1), it has first intersected the line at some other value of x between 0 and 1, which is another real positive root of x = f(x), as required by Haldane’s proof.

\[Note 8\] Here Haldane follows Fisher closely, but with a significant modification. Fisher (1922) had given the formula f(x) = e^m(x – 1), where m:1 is the ratio of the total population in generation (n + 1) to the population in generation n; in other words he allows for the growth of a neutral allele in line with any expansion of the population as a whole. Haldane’s significant innovation is to allow for genes which increase in numbers because of a selective advantage, k, relative to other genes in a static population. Fisher’s f(x) = e^m(x – 1) then becomes Haldane’s f(x) = e^(1 + k)(x – 1), and Haldane is able to find an explicit expression for the chance of survival in terms of the selective advantage k (see Note 9).

\[Note 9\] Haldane denotes the probability of the gene surviving as y, so the probability of extinction is 1 – y. But the probability of extinction is the appropriate root of the equation x = f(x) = e^(1 + k)(x – 1). So substituting 1 – y for x we get 1 – y = e^-(1 + k)y. In the right hand side of this equation the expression -(1 + k)y is the (natural) logarithm of the left hand side, which is 1 – y, so, taking the negative of both sides, (1 + k)y = -log(1 – y).

\[Note 10\] Here Haldane assumes knowledge of a theorem equivalent to -log(1 – y) = y + (y^2)/2 + (  
y^3)/3 + (y^4)/4: see this Wiki [article](https://en.wikipedia.org/wiki/Logarithm) on logarithms. Given this theorem, we have

(1 + k)y = -log(1 – y) = y + (y^2)/2 + (y^3)/3 + (y^4)/4 …

therefore, dividing both sides by y and then subtracting 1 from both sides, we get

k = (y^2)/2y + (y^3)/3y + (y^4)/4y … = y/2 + (y^2)/3 + (y^3)/4 + …

as stated by Haldane.

### Related Posts:

- [My
  fixations](https://www.gnxp.com/WordPress/2006/08/06/my-fixations/) - [You only go extinct
  once....](https://www.gnxp.com/WordPress/2006/10/29/you-only-go-extinct-once/) - [A note on
  '2s'](https://www.gnxp.com/WordPress/2007/04/03/a-note-on-2s/) - [R. A. Fisher on Epistasis (yet
  again)](https://www.gnxp.com/WordPress/2008/09/04/r-a-fisher-on-epistasis-yet-again/) - [Hold one hand still, move the
  other](https://www.gnxp.com/WordPress/2006/03/03/hold-one-hand-still-move-the-other/) - [Now It Can Be
  Told](https://www.gnxp.com/WordPress/2006/12/17/now-it-can-be-told/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F01%2F11%2Fhaldane-s-selection-theorem%2F&linkname=Haldane%27s%20Selection%20Theorem "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F01%2F11%2Fhaldane-s-selection-theorem%2F&linkname=Haldane%27s%20Selection%20Theorem "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2007%2F01%2F11%2Fhaldane-s-selection-theorem%2F&linkname=Haldane%27s%20Selection%20Theorem "Email")[](https://www.addtoany.com/share)
