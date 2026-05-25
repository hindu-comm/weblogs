+++
title = "The Democracy Glitch Why"
full_title = "The Democracy Glitch Why Math Makes Honest Elections Impossible"
upstream_url = "https://ramaseshanchandrasekaran.substack.com/p/the-democracy-glitch-why-math-makes"
date = "2026-01-11"
+++
Source: [here](https://ramaseshanchandrasekaran.substack.com/p/the-democracy-glitch-why-math-makes).

The Democracy Glitch: Why Math Makes Honest Elections Impossible

# The Democracy Glitch: Why Math Makes Honest Elections Impossible

### In this article, I prove a famous mathematical result that has massive implications in political theory and choice theory (in sociology) as to why there can never be a fair election !

[](https://substack.com/@ramaseshanc)

![Rama Seshan Chandrasekaran's avatar](https://substackcdn.com/image/fetch/$s_!ZHOm!,w_36,h_36,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11e50d60-b811-4831-8bbc-4d320762e60b_96x96.png)

[Rama Seshan Chandrasekaran](https://substack.com/@ramaseshanc)

Jan 11, 2026

13

3

5

Share

[](https://substackcdn.com/image/fetch/$s_!jrE3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa8848ed7-2e6c-4336-b4ac-cd10a5008f2e_1200x675.jpeg)

![Fixing India's electoral rolls](https://substackcdn.com/image/fetch/$s_!jrE3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa8848ed7-2e6c-4336-b4ac-cd10a5008f2e_1200x675.jpeg "Fixing India's electoral rolls")

Do you think that in the system of democracy, every citizen’s honest preference in elections always contributes to a fair outcome? Imagine standing in a voting booth, pen in hand, hovering over the name of the candidate you truly love. Then, you hesitate. You feel that voting for your favorite might actually help the candidate you hate the most win. With a sigh of frustration, you cast your vote for a “lesser of two evils” instead. Does this feeling feel familiar to you?

**Why does democracy feel like a game of strategy rather than an expression of honesty?**

It turns out that the “flaws” we see in our elections like the sudden collapse of third parties, the rise of rigid two-party systems, and the strange phenomenon of people voting in blocks against their own interests, aren’t just “dirty politics.” They are the downstream consequences of a profound mathematical “glitch.”

In this article, we are going to explore the **Gibbard-Satterthwaite Theorem**. Through a simple yet undeniable proof, we will reveal why any voting system with more than two choices is mathematically “deceitful.” We will walk through the construction of five specific voting profiles to show that unless an electoral system is a literal dictatorship, it will always reward voters for lying about who they actually want. Prepare to see the “will of the people” through a new lens: one where logic itself explains why the system we built for fairness often forces us into the most unfair of choices.

One class of the most fascinating theorems in mathematics is the class of **impossibility theorem**s. They tell us that there can exist no object that satisfies a given set of properties. Many impossibility theorems are revolutionary and reveal deep and profound properties of logic, computation, and probability. To fully appreciate these class of theorems however requires understanding their proof. This article states and proves an impossibility theorem that has profound implications in social science and uses no sophisticated jargon and intuitively illuminates the result. This result that I am going to prove is nothing but the **Gibbard-Satterthwaite (GS) theorem**. A little more general version of this theorem called **Arrow’s theorem** is more popular and was first proven and holds central importance in the areas of voting theory, economoics, political science, sociology, and so forth. Sen says :

Virtually all models to analyse political competition originate in some way or the other from Arrow’s impossibility theorem for fair voting.

# Defining Fair Elections

The most intuitive context to discuss the GS theorem is that of an election. Let there be ‘**m**’ number of candidates and ‘**n**’ number of voters. Let each voter provide a **preference list** where in they rank the ‘m’ candidates in the order of their preference (no ties allowed).

> The collection of the preference lists for all the ‘**n**’ voters is
> called a **voter** **profile** and is denoted by P.

An example for a voting profile P with 3 voters and three candidates A,B,C is shown below.

[](https://substackcdn.com/image/fetch/$s_!Gqou!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F61ef30d2-bfca-4419-a4e7-8b03c686e22a_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!Gqou!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F61ef30d2-bfca-4419-a4e7-8b03c686e22a_2816x1536.heic)

Now, we define an important concept called the **election mechanism**.

> *Definition* : An **election mechanism (EM)** is an algorith or a
> machine that takes any possible voter profile P and declares a
> **winning candidate** for each profile.
>
> Note that ties are not allowed and there should be **one and exactly
> one** winning candidate for each voting profile under the election
> mechanism.

[](https://substackcdn.com/image/fetch/$s_!imJf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F00d2faa5-a687-4ef3-a4f4-ffca3489c366_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!imJf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F00d2faa5-a687-4ef3-a4f4-ffca3489c366_2816x1536.heic)

Note that EM is a method of winner evaluation for a profile. It is intuitive that there are many methods to declare a winner and that different election mechanisms can lead to different types of outcome for the same profile.

Now, we would want any sensible and fair election mechanism to satisfy the following three properties and let us call them **axioms of fairness**.

> *Axiom 1* - **Unanimity** : If a candidate X is the first preference
> for all the “n” voters, then the election mechanism should declare X
> to be the winner.

This is a sensible thing to ask. If X tops the preference list of all voters, then everyone wants X as their first preference. Hence, a fair mechanism must declare X to be the winner in that case.

[](https://substackcdn.com/image/fetch/$s_!FlL8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F885a0c4d-9e35-4aab-9ee7-0730fcf72549_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!FlL8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F885a0c4d-9e35-4aab-9ee7-0730fcf72549_2816x1536.heic)

> *Axiom 2* - **No Voter Dictatorship** : The election mechanism is said
> to satisfy the “no voter dictatorship” criterion if there does not
> exist a voter (say V_i) such that his first preference is always
> declared the winner for any election profile P.

This is also a very sensible thing to ask for the fairness of an election mechanism. If an election mechanism after getting any profile, sees only the preferences of one particular voter and declares his first preference to be the winner and ignores the preference of all other voters, then that voter is acting like a dictator. We do not want such dictators in fair elections and hence the second axiom says that a fair election mechanism should not allow any voter to be a dictator.

[](https://substackcdn.com/image/fetch/$s_!7usJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe9f7c01f-e9db-4f98-b0f6-468c6ae691cb_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!7usJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe9f7c01f-e9db-4f98-b0f6-468c6ae691cb_2816x1536.heic)

The third axiom for a fair election is little more subtle but also obviously necessary to be true once you see it.

> *Axiom 3* - **Consistency** : For a given profile P, let the election
> mechanism EM declare the candidate X to be the winner. Consider
> another voting profile P’ that has the property that : for every voter
> V_i, no candidate who was below X in the voting of V_i under profile P
> has moved to be above X in the new profile P’. Or in other words, X
> has moved only up or stayed at the same place for all voters from P to
> P’. Then, the mechanism EM is said to be consistent if it still
> declares X to be the winner for all such profiles P’ satistying the
> previously mentioned property.

This is also very easy to understand. Suppose people vote in a given profile P for which X is declared to be the winer under the mechanism EM. Under this profile P, let X be above a certain group of candidates. Then, if even in another voting profile P’, if X continues to be above the same group of candidates in P (if not more) for every voter, then he deserves to win. He will ask : I have been placed above the same (or more) group of candidates in P’ as I have been in P. Then, why am I winning in P but not in P’?

[](https://substackcdn.com/image/fetch/$s_!y-Qm!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F04cf23fa-c956-400a-b29e-3cc8ad496399_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!y-Qm!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F04cf23fa-c956-400a-b29e-3cc8ad496399_2816x1536.heic)

These three fairness axioms that we have demanded so far - unanimity, no voter dictatorship, and consistency are a minimum set of common sensical demands for an election mechanism that we believe is fair. Now, with these ingredients in hand, let us state the shocking statement of the main theorem that we are going to prove in this article which is the **Gibbard-Satterthwaite (GS) theorem**.

> ***GS Theorem :*** There is no single election mechanism EM that obeys
> all the three of fairness axioms simultaneously when there are more
> than two (i.e. three or more) election candidates !

This astouding result will come as a surprise to most of you! But turns out this is true.

[](https://substackcdn.com/image/fetch/$s_!LXyh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5c566317-c784-407f-a5c6-ae25ec517973_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!LXyh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5c566317-c784-407f-a5c6-ae25ec517973_2816x1536.heic)

# Deceit Immunity

In a sensible electoral system, a voter would vote his honest preferences out to make his preferred candidate wins, even if he had access to what others are voting. But when that is not the case, the mechanism is called deceitful.

> *Definition* - **Deceitful** : An electoral mechanism is called
> deceitful if the following can happen
>
> Assume two profiles P and P’ are otherwise identical except for the
> preference of the last voter. Assume that X wins P’ and Y wins P
> despite Y being above X by the last voter in P’.

Note that in such a mechanism, when the last voter who wants Y to win and was honest about Y and placed it above X (case P’), his candidate Y lost but some other dishonest preference in P made his candidate Y win. Such a candidate, if he has access to other votes or believes that others will vote in a certain way, might be incentivised to be dishonest in voting to make his preferred candidate win. Such an electoral mechanism where deceit is incentivised is called a deceitful election mechanism.

[](https://substackcdn.com/image/fetch/$s_!K7KD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc6a8656e-8085-4209-a7ee-07508775a8db_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!K7KD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc6a8656e-8085-4209-a7ee-07508775a8db_2816x1536.heic)

Shall we add this requirement of election mechanisms being deciet-free too in our list of axioms as the fourth axiom? Turns out that we can replace the third axiom by deceit-freeness axiom because mathematically, deceit-freeness guarantees consistency. The proof of it will be done after the proof of the GS theorem. But I am saying this now itself to motivate the next section.

# Practical Implications

The GS (Gibbard-Satterthwaite) theorem is fundamentally unsettling because it reveals a mathematical “glitch” in the heart of collective decision-making. We often view democracy as a system where every citizen’s honest preference contributes to a fair outcome. However, the theorem proves that in any election with more than two candidates, a voting system that is both fair (unanimous) and logical (consistent) is impossible unless it is a **dictatorship**. It essentially strips away the illusion that we can design a perfect mechanism for choice, proving that any such system will inherently incentivize “strategic voting” rather than honest expression.

In real life, the implications are profound and often frustrating. It explains why voters frequently feel forced to engage in **tactical voting** (voting for a “lesser of two evils” rather than their favorite candidate) to avoid throwing their vote away. This is most visible in multi-party systems where a popular third candidate might inadvertently act as a “spoiler,” helping the candidate they most oppose to win. Because no system can be entirely strategy-proof, voters are often rewarded for being dishonest about their preferences, which can lead to outcomes that don’t truly represent the “will of the people.” Ultimately, the theorem teaches us that every voting rule is a compromise; since a perfect system is mathematically impossible, we must choose which specific “unfairness” we are most willing to tolerate.

The GS theorem provides a rigorous mathematical foundation for several frustrating phenomena we observe in modern politics. By proving that every non-dictatorial voting system is prone to inconsistency, it explains why “honest” voting is often a losing strategy.

### The Gravity of the Two-Party System

The theorem explains why multi-party systems often experience “centripetal force” that pulls them toward two dominant parties (a phenomenon often called **Duverger’s Law**). Because any system with three or more candidates is mathematically unstable and open to manipulation, voters quickly realize that supporting a third-party candidate (even if that candidate is their true favorite) can act as a “spoiler.”

By splitting the vote among like-minded people, they inadvertently help the candidate they like the *least* to win. To prevent this “logical contradiction” in their own interests, voters and politicians coalesce into two massive “big tent” parties. These parties act as pre-election coalitions where the compromising happens *before* the ballot is cast, rather than through a multi-candidate election.

### The Death of the Honest Preference

In a perfect world, you would vote for Candidate A because you like them best. However, GS proves that you are often rewarded for **strategic lying**. If you know your favorite (Candidate A) has no chance of winning, but your second choice (Candidate B) is neck-and-neck with your most-hated choice (Candidate C), the theorem shows that the only way to impact the outcome is to abandon Candidate A entirely.

This leads to the **“Lesser of Two Evils”** trap. People vote as a group or a bloc not necessarily because they agree on everything, but because they are trying to collectively act as the **“Pivotal Voter”** (who acts as the dictator that we will identify in our proof below). They realize that individual “honest” preferences are mathematically ignored by the mechanism unless they align with a large enough group to flip the winner from one major contender to another.

### Polarization and “Negative Partisanship”

Because the mechanism is “consistent” (as we used in the proof), it reacts sharply to changes in the preference list. This creates a culture of **Negative Partisanship**, where voters are driven more by the fear of Candidate C winning than by the hope of Candidate A winning. Since the theorem proves that no system can perfectly reflect the nuances of a diverse electorate without being a dictatorship, political players focus on the “all-or-nothing” nature of the pivot point. This encourages parties to polarize, moving further apart to create clear, un-nuanced choices that force voters into one of two camps.

If you are interested in the proof of this theorem, continue further ( I highly recommend so). There is no advanced mathematics of any sort involved. You have to just follow a series of profile constructions that are richly illustrated by yours truly !

------------------------------------------------------------------------

Let us break down the proof of this result into small manageable common sensical chunks.

# Consistency and Single Pair Reversal

Let X and Y be two candidates. Let P and P’ be two voting profiles of the voters where all the preference votes are identical except for the vote of a single candidate V_i. And let it be that the only difference in the vote of V_i between the profiles P and P’ is that X was one step above Y in V_i under P and is now one step below Y in P’ with all other preferences being the same. We call such a pair of profile P’ as the **single pair reversal** of P and vice versa.

> *Definition* - **(X,Y) Reversal** : A profile P’ is said to be an
> (X,Y) reversal of another profile P if the vote preferences of all but
> one candidates are exactly the same in both the profiles and on the
> differing voter, the only difference is that candidate X is
> immediately above Y in P while being immediately below Y in P’ with
> all the other preferences being the same.

Here is an illustration of two profiles P and P’ related by (X,Y) reversal for the first six voters and six candidates (A,B,C,D,X,Y) with the first vote alone differing between P and P’.

[](https://substackcdn.com/image/fetch/$s_!SOyR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4f71a0a3-d2ac-4c3a-b269-39f3e747e950_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!SOyR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4f71a0a3-d2ac-4c3a-b269-39f3e747e950_2816x1536.heic)

Now with this definition, let us prove a small result. We will call small results that are useful to prove the main GS theorem as lemmas.

> **Single Pair Reversal Lemma** : Suppose that an election mechanism EM
> declares candidate X to be the winner for a voting profile P and let
> P’ be the (X,Y) reversal pf P. Then, if EM is consistent (satisfies
> axiom 3), it must declare either X or Y to be the winner for P’ and
> not any other third candidate.

**Proof** : Let us assume contrary to what we want to prove that X is the winner for P but some other third candidate Z is the winner for P’. Now, let us exchange the positions of X and Y for the vote V_i in the profile P’. Doing this creates the profile P only again.

In this switch, only the single vote V_i is changed and even there X and Y which were flipped are immediately one below each other. Since X and Y are both immediately next to each other, if they both were below Z in P’, they still remain below Z even after flipped to create P. Hence, X and Y if both below in P’ cannot move above Z if they alone are flipped and only with each other (note that the votes of all other candidates except V_i remain the same in both P and P’). But since we assumed that EM is consistent, if it declares Z to be the winner for P’, it must also declare Z to be the winner for its (X,Y) reversal P wherein nobody below Z in P’ has moved above Z in P for any voter. So, EM should also declare Z to be the winner in P as well. But we already assumed that EM declares X to be the winner in P. So, we have contradicted one of our our own assumptions by assuming the result contrary to the theorem we want to prove. This is stupid ; assuming EM to declare X to be the winner in P, we proved that EM declares Z to be the winner in P which are logical contradictions and cannot be both true simultaneously. But, we could do this only when we assumed the falsity of the theorem that we wanted to prove. Hence, the falsity of the theorem should be discarded since it produces logical contradiction. So, our original theorem must be true.

[](https://substackcdn.com/image/fetch/$s_!l9AL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc2f0fed2-7fb2-4bb5-9819-1c25bde7c1fd_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!l9AL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc2f0fed2-7fb2-4bb5-9819-1c25bde7c1fd_2816x1536.heic)

# Proof of Impossibility of a Fair Election Mechanism

## The Overall Game Plan

The overall method of approach to the proof of the main theorem goes as follows. To prove that there can be no election mechanism that satisfies all the three fairness axioms, we show that if a mechanism satisfies two of the three axioms, it has to violate the third axiom. More specifically, we will assume an arbitrarily fixed election mechanism EM is both consistent (satisfies axiom 3) and is unanimous (satisfies axiom 1) and then using this, we will end up proving that there is a voter who is a dictator and thus procving that the “no voter dictatorship” (axiom 2) is violated.

To go in more detail, we will construct a series of five profiles =\> P1, P2, P3, P4, P5. Using consistency and unanimity, we will deduce we argue who is the winner for each of these profiles. We will ultimately reach the profile P5 where there is some voter called the **pivotal voter** and some candidate A such that A is at the top of the pivotal voter’s list, but at the bottom of the preference list of all other voters but the mechanism EM ends up declaring A to be the winner. This must raise eyebrows and suspicion already.

Then, we will repeat the construction of profiles with other candidates in place of A and see that whichever candidate is at the top of the list of the pivotal voter, the mechanism EM will only declare that candidate to be the winner, no matter whatever the other details of the profile with other voters are. This will prove that the pivot voter is a dictator for this election mechanism and this proves the main result.

## From the First to Third Profile (P1 → P2 → P3)

To start, let P1 be a profile with A at the top and B and the bottom of every voter’s preference. The other details of P1 are arbitrary and irrelevant. By the unanimity of the mechanism EM, it must declare A to be a winner for the profile P1.

[](https://substackcdn.com/image/fetch/$s_!xMld!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6266b262-e8b3-4870-a137-de1e5348705d_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!xMld!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6266b262-e8b3-4870-a137-de1e5348705d_2816x1536.heic)

Now modify P1 by moving the candidate B upward to just below candidate A in the list of voter 1 alone and moving all other entries one step down. Now, by consistency, A will still be the winner.

[](https://substackcdn.com/image/fetch/$s_!Jw9s!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F66c5e0e7-e575-4c3b-aa82-491ffa446d90_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!Jw9s!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F66c5e0e7-e575-4c3b-aa82-491ffa446d90_2816x1536.heic)

Next, exchange the positions of A and B in this modified P1 so that B is at the top position and A is at the second position for voter 1. As usual, all other votes remain the same. Now, after this modification, by single pair reversal lemma, the winner of this new profile would be either A or B.

[](https://substackcdn.com/image/fetch/$s_!aHEO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe7a4b699-2471-4fd1-8d66-0086f4bf5d82_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!aHEO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe7a4b699-2471-4fd1-8d66-0086f4bf5d82_2816x1536.heic)

If the winner after this (A,B) reversal on the first voter changes the winner from A to B, stop here. If the winner is still A, then perform this same sequence of steps on voter 2 (move B to the second last position and move all others one step down. By the same logics of consistency and single pair reversal lemma, the winner will again only be either A or B. If the winner now atleast changes from A to B, stop. If it still remains A, then continue repeating this sequence of steps on the third voter until B wins. Note that eventually B must win because at the end, after we do this to all voters till the end, B will be in the top of the preference list of all voters after we do these steps on the last vote. Unanimity must at this last stage make B win. But B might win before itself in the middle. The first point in the voter list at which the winner flips from A to B (after which further moves are stopped) should be called as the pivotal voter. The profile at this stage is the third profile P3 and the profile just before this stage P2 (the last time that A won) is called P1.

[](https://substackcdn.com/image/fetch/$s_!xcx9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9bd000ac-69d6-4efc-9fe1-9d74dce774fc_2816x1504.heic)

![](https://substackcdn.com/image/fetch/$s_!xcx9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9bd000ac-69d6-4efc-9fe1-9d74dce774fc_2816x1504.heic)

## From the Third to Fourth Profile (P3 → P4)

Now consider the profile P3 where we have identified the pivotal voter. Now, do not change the votes of this pivotal voter. But do the following changes on all the other voters :

- For every voter who is to the left of the pivot (where, if you
  remember, B is top and A is second), move candidate A down to the
  bottom of the preference list.

- For all voters on the right of the pivotal voter (where, if you
  remember again, A is at the top and B is at the bottom), move
  candidate A down to the bottom of the preference list to be placed
  just one step above candidate B.

Call this resulting profile as P3’. Note that upon comparing profiles P3 and P3’, we realise that for every voter, whoever candidates that B beats in P3, he also beats in P3’. But since B is the winner in P3, by consistency axiom, B should win in P3’ also.

[](https://substackcdn.com/image/fetch/$s_!T1Ea!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6dafffd8-7cfb-48ab-864d-d3b12c0386c0_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!T1Ea!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6dafffd8-7cfb-48ab-864d-d3b12c0386c0_2816x1536.heic)

Now let us do the exact same thing on the profile P2. Move A to the bottom of each list to the left of the pivot, to the second bottom just above B to the elements right of the pivot, while keeping the pivot unchanged. Let the resulting profile be called P2’. Note that the only difference between P2’ and P3’ is the pivotal voter entry where A and B which are immediately succeeding each other have switched places. So, by the single pair reversal lemma, since B is the winner for P3’, the winner for P2’ must either be A or B.

[](https://substackcdn.com/image/fetch/$s_!3auF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F10a4c3f2-32f5-48fb-8937-1e2a85ff7bd0_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!3auF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F10a4c3f2-32f5-48fb-8937-1e2a85ff7bd0_2816x1536.heic)

Given these two options A and B, we now prove that the winner for profile P2’ must be A (and not B). Why? In each voter’s list of preferences, the set of candidates below B in P2 is the same as in P2’. By consistency requirement, if B wins P2’, he should win P2 also. But we already assumed that A wins P2 (remember in the series of constructions from P1 that P2 is the stage just before P3 where B wins for the first time after defeating A who had been winning thus far). So, we have arrived at a contradiction by assuming that B wins P2’. So, that assumption must be wrong and hence it must be A that wins P2’.

[](https://substackcdn.com/image/fetch/$s_!JBVE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0cf16079-0356-4c0c-98a2-0a9701bd0179_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!JBVE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0cf16079-0356-4c0c-98a2-0a9701bd0179_2816x1536.heic)

So far, we thus have that A wins P2’ and B wins P3’ to recap again.

[](https://substackcdn.com/image/fetch/$s_!3kH2!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc3497caa-214d-4331-9085-1b8306331f29_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!3kH2!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc3497caa-214d-4331-9085-1b8306331f29_2816x1536.heic)

Now let us start modifying P2’ again to create another profile P4. Pick an arbitrary third candidate X, other than A or B. Then, starting from P2’, move (if necessary) A,B and X around so that :

- For every voter to the left of the pivotal voter, the bottom three
  candidates in the list of the voter are X, B, and A in that exact
  order where A is the bottommost and B is above A and X is above B.

- The top three candidates in the list of the pivotal voter are A, X,
  and B in that order with A at the top, X just below A and B just below
  X.

- For every voter to the right of the pivotal voter, the bottom three
  candidates in the list of the voter are X, A, and B in that exact
  order where B is the bottommost and A is above B and X is above A.

My claim is that A is still the winner of this P4. Why? Starting from P2’ (where A is the winner), no candidate that is below A in any voter preference, moves above A after the rearrangement. To be more specific,

- A is at the bottom of the list in both P2’ and P4 to the left of the
  pivot.

- A is the top of the list for the pivotal voter in both P2’ and P4.

- A and B are both in the bottom two positions in the list for the
  voters to the right of the pivotal voter in both P2’ and P4.

So, A is above the same set of candidates in both P2’ and P4 and hence by consistency, if A wins P2’, he must win P4 also.

[](https://substackcdn.com/image/fetch/$s_!nmd2!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe9c2855a-5fa5-409c-8792-85e411bc8dfc_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!nmd2!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe9c2855a-5fa5-409c-8792-85e411bc8dfc_2816x1536.heic)

## From the Fourth to Fifth Profile (P4 → P5)

Now let us create the last profile P5 from P4 where A is the winner. We just flip the positions of A and B for voters right of the pivotal voter one at a time, to finally create P5. Note that A and B are successive pairs at the bottom in P4. Each such transformation when viewed one at a time is a single pair reversal and hence by the lemma, after each exchange, we are guarateed that the winner will either remain A or flip to B. By carrying it all the way, we see that the winner of P5 is also either A or B. We will soon prove that it can’t be B and that A wins P5. But before that, assume that A does win P5. But something interesting is happening : In P5, A is at the bottom of every list except for the pivotal voter except for the pivotal voter where A is at the top. But still A manages to win !

[](https://substackcdn.com/image/fetch/$s_!a00x!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fffd1cc57-66d0-4531-a3ef-a1e07803fec8_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!a00x!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fffd1cc57-66d0-4531-a3ef-a1e07803fec8_2816x1536.heic)

Now let us prove that why A wins P5 and not B. Assume for the contrary that it is B that wins. Now, X is above B for every voter in P5. Note that X is above B for every voter in P5. So, now if we raise X to the top of the list for all voters, the set of candidates below B will still remain the same. So, by consistency, if B wins P5, it must also win after X is pushed to the top of every voter’s list. But, unanimity requires that if X is at the top of every voter’s list, it is X that must win. We cannot have two winners and hence what we assumed (B winning P5) must be wrong and hence it is only A that must win P5.

[](https://substackcdn.com/image/fetch/$s_!i7AS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2d9be166-72c7-46c8-a617-622ebd4da33e_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!i7AS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2d9be166-72c7-46c8-a617-622ebd4da33e_2816x1536.heic)

So, at last, we have that :

> In P5, A is at the top preference only for the pivotal voter and the
> bottom most and last preference for all other voters, but still
> manages to win !

[](https://substackcdn.com/image/fetch/$s_!6yTl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3eda0cfc-142a-4b23-a1e3-118e6daab5bf_1408x768.heic)

![](https://substackcdn.com/image/fetch/$s_!6yTl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3eda0cfc-142a-4b23-a1e3-118e6daab5bf_1408x768.heic)

## Proving that the pivotal voter is a dictator

Now, comes the crucial part of the proof. We have used consistency and unanimity to construct this P5 where A is the winner despite being top only for the pivotal voter, and being at the bottom for all other voters. Now, whatever change we make to the non-pivot vote, it is still A that wins. Because note here that A is at its worst (absolute rock bottom) for all non-pivotal votes. Any movement and change that we make to the non-pivot vote at this point can only make A fare better, if not the same. If A improves or remains the same, consistency hence dictates that it must still continue to win no matter whatever is the choice of the other non-pivot voters. The only thing that matters is that A is at the top in the pivotal voter’s list. Thus, we have that

> In any profile with three or more candidates where candidate A is at
> the top of the preference list of the pivotal voter (details of other
> voters are irrelevant), any voting mechanism that is unannimous and
> consistent will declare only A to be the winner !

Now in all the constructions starting from P1 to P5, A was just an arbitrary candidate and could have been anyone (replace A by B or C or D or anyone and all the constructions and the arguments above still hold). What simply mattered above is that A is at the top of the pivotal voter list. Thus, we have that any candidate that tops the preference list of a pivotal voter (call it A or whatever) is declared to be the winner in any mechanism that is consistent and unanimous !!

[](https://substackcdn.com/image/fetch/$s_!_o0_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2080460c-ddf8-44fe-91ee-e6ce6f1c9ff1_1408x768.heic)

![](https://substackcdn.com/image/fetch/$s_!_o0_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2080460c-ddf8-44fe-91ee-e6ce6f1c9ff1_1408x768.heic)

So we have finally proved the GS theorem ! Note that we did not use any fancy tools, techniques, and advanced operations. Just simple constructions and permutations that you had to patiently follow !

------------------------------------------------------------------------

# Deceit-Freeness Guarantees Consistency

In this final section, we will prove that deceit-freeness guarantees consistency. For this, we assume that an election mechanism is not consistent and end up showing that it is deceitful. The proof goes as follows :

Imagine an election with two profiles, **Profile A** and **Profile B**. They are identical except for one voter (let’s call him “Voter 1”).

1.  **In Profile A:** Candidate **X** is the winner.

2.  **In Profile B:** Voter 1 moves Candidate **X** higher in their
    preference list. Everything else in the entire election stays
    exactly the same.

**The Goal:** We want to prove that in a deceit-free system, candidate **X** *must* still win in Profile B (to prove consistence). Again , assume for the sake of contradiction that the system is **deceit-free**, but **inconsistent**. This would mean that when X moves up in Profile B, a different candidate (let’s call them **Y)** suddenly wins instead.

### Step 1: Voter 1’s perspective in Profile B

If the winner is **Y** in Profile B, Voter 1 has a problem.

- In Profile B, Voter 1 actually prefers **X** over **Y** (since X moved
  up).

- Voter 1 knows that if they “lied” and reported their ranking from
  Profile A instead, the winner would switch from **Y** back to **X**.

- Since Voter 1 prefers **X**, they are incentivized to misrepresent
  their vote.

- **Conclusion:** The system is **deceitful** at Profile B.

### Step 2: Voter 1’s perspective in Profile A

Now let’s look at it from the other side. Imagine the “true” preferences of Voter 1 are actually those in Profile B, but they are currently in Profile A.

- In Profile A, **X** wins.

- But if the system were consistent, and the winner in Profile B was
  **Y**, Voter 1 (who prefers Y in Profile A) would have an incentive to
  stay silent or “lie” to ensure their preferred outcome.

- Actually, the most direct contradiction is simpler: If moving a winner
  **up** causes them to **lose**, it creates a situation where a voter
  can change the outcome to a preferred candidate by reporting a *lower*
  preference for that candidate.

Thus, if a system is truly deceit-free, it is impossible for a winner to lose power by gaining support.

> **The Rule:** If X wins, and I like X *more* now than I did before,
> and my change in vote causes X to *lose*, then the system has
> effectively punished me for being honest about my support.

Therefore, to prevent “deceit” (strategic manipulation), the system **must** be consistent. Any “glitch” where moving a winner up causes them to lose would immediately create a strategic incentive for a voter to lie and pretend they like that candidate less than they actually do.

13

3

5

Share
