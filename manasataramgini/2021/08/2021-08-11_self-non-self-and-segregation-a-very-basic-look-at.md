+++
title = "Self, non-self and segregation: a very basic look at agent-based lattice models"
date = "2021-08-11"
upstream_url = "https://manasataramgini.wordpress.com/2021/08/11/self-non-self-and-segregation-a-very-basic-look-at-agent-based-lattice-models/"

+++
Source: [here](https://manasataramgini.wordpress.com/2021/08/11/self-non-self-and-segregation-a-very-basic-look-at-agent-based-lattice-models/).

In our college days, a part time physics teacher from an old and respected V![\_1](https://s0.wp.com/latex.php?latex=_1&bg=ffffff&fg=333333&s=0&c=20201002) clan used to chat with us about issues of mutual interest that were beyond that of the rest of the class (or for that matter the rest of the teachers) and well out of the scope of the syllabus. He was the only one among the physics staff with an interest in science for science’s sake. We always felt he had it in him to be a scientist and he was indeed was pursuing a doctoral program at his own pace on the side. However, he clarified to us that he was the big fish in the small pond and that every man’s ambition is like a rocket set off on a Dīpāvalī night — drawing out a parabola on the board he declared with his characteristic smirk: “It will come down; hence, why trouble yourself with a dizzying fall”. In course of one involved conversation spanning thermodynamics, dynamical systems and biological ensembles, he declared to us: “I agree with you that there are several problems where the actual entities are fungible. It doesn’t matter if we are dealing with atoms, cells or animals, they could as well just be numbers. You should explore the Ising models — maybe you will find something there to answer your questions.” We are not really into “proving a few theorems”; however, playing with things on paper or a computer has always excited us. Hence, the next time we could access a computer we began looking into those models and soon realized that it could be used to understand some basic aspects of biological systems.

Here we shall describe some experiments with such models that go no further than the most basic exploration of these systems. In physics, such models were first proposed by Lenz and his student Ising. In sociology, they were introduced by Schelling (of whose work we learnt much later) who carried out the experiments with a graph paper and coins. Today we can do them easily by writing some code on a little computer. The basic rules for the games we shall look at go thus:

1\) The games are played on a lattice on the surface of a torus but for visualization we shall cut open the torus and render it as a square board. Thus it would look like this:

![Fig_Schel01](https://manasataramgini.files.wordpress.com/2021/08/fig_schel01.png?w=376&h=373)

2\) Each cell of the lattice can be occupied by an “agent” of one of two colors (as above) or be empty.  
3) The system has strict conservation laws: the agents can neither be created nor destroyed and the number of agents of each color will be conserved.  
4) The neighborhood of an agent is determined by the “span”
![l](https://s0.wp.com/latex.php?latex=l&bg=ffffff&fg=333333&s=0&c=20201002)
which defines a square grid of a centered on it with
![(2l+1)^2-1](https://s0.wp.com/latex.php?latex=%282l%2B1%29%5E2-1&bg=ffffff&fg=333333&s=0&c=20201002)
neighbors.
![l=1](https://s0.wp.com/latex.php?latex=l%3D1&bg=ffffff&fg=333333&s=0&c=20201002)
means a ![3 \\times 3](https://s0.wp.com/latex.php?latex=3+%5Ctimes+3&bg=ffffff&fg=333333&s=0&c=20201002) grid with the agent at the center and 8 lattice positions available for neighbors around it. Thus, the agent marked with a black dot (above) has 5 neighbors at
![l=1](https://s0.wp.com/latex.php?latex=l%3D1&bg=ffffff&fg=333333&s=0&c=20201002):
2 blue and 3 yellow.
![l=2](https://s0.wp.com/latex.php?latex=l%3D2&bg=ffffff&fg=333333&s=0&c=20201002)
means a ![5 \\times 5](https://s0.wp.com/latex.php?latex=5+%5Ctimes+5&bg=ffffff&fg=333333&s=0&c=20201002) grid with the agent in the center and 24 available lattice positions for neighbors in two concentric shells around it.  
5) The agency of the agent manifests as its ability to read the number and color of its neighbors and either stay put where it is or move over to a random empty cell in the lattice.  
6) Beyond this is there is occupancy,
![o](https://s0.wp.com/latex.php?latex=o&bg=ffffff&fg=333333&s=0&c=20201002),
i.e. the fraction of the total available cells in the lattice that are occupied by agents.

All the experiments described below are played on a ![50 \\times 50](https://s0.wp.com/latex.php?latex=50+%5Ctimes+50&bg=ffffff&fg=333333&s=0&c=20201002) lattice, i.e. there are 2500 cells available to the agents. In all experiments, the agents move to an available empty cell if the number of its neighbors of any color are ![\\le s](https://s0.wp.com/latex.php?latex=%5Cle+s&bg=ffffff&fg=333333&s=0&c=20201002), the sociality factor. Thus, if
![s=0](https://s0.wp.com/latex.php?latex=s%3D0&bg=ffffff&fg=333333&s=0&c=20201002)
then the agent will move from their current location if they have no neighbors at all. In the first set of experiments, they additionally sense the the absolute number of non-self neighbors, i.e. those of a different color and move if it is ![\\ge c_n](https://s0.wp.com/latex.php?latex=%5Cge+c_n&bg=ffffff&fg=333333&s=0&c=20201002), the non-self count. The movements of the agents are repeated over and over until stability is reached or 30 successive rounds of movement have elapsed. The games are illustrated thus: the plot to the left is the initial configuration where the agents are randomly introduced into the lattice and the plot to the right is the final configuration that is reached as mentioned above. We measure segregation by looking at the
![\\tfrac{n}{s}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bs%7D&bg=ffffff&fg=333333&s=0&c=20201002),
i.e. the mean non-self: self ratio in the neighborhood of the agents. As the agents are randomly introduced, the game would start with
![\\tfrac{n}{s} \\approx
1](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bs%7D+%5Capprox+1&bg=ffffff&fg=333333&s=0&c=20201002). The degree of segregation can be statistically assessed at the beginning and end of the run by means of the t-test to see if the mean number of self and non-self agents in the neighborhood of any given agent are significantly different. At the start of the run the difference would be insignificant.

Game 1 is a run with low occupancy
![o=0.4](https://s0.wp.com/latex.php?latex=o%3D0.4&bg=ffffff&fg=333333&s=0&c=20201002)
and an equal number of agents of the two colors (blue and orange);
![l=1](https://s0.wp.com/latex.php?latex=l%3D1&bg=ffffff&fg=333333&s=0&c=20201002),
i.e. a neighborhood with 8 available cells;
![s=0](https://s0.wp.com/latex.php?latex=s%3D0&bg=ffffff&fg=333333&s=0&c=20201002);
![c_n=5](https://s0.wp.com/latex.php?latex=c_n%3D5&bg=ffffff&fg=333333&s=0&c=20201002),
i.e. the agents tolerate up to half of the 8 available lattice points in the neighborhoods being occupied by non-self agents.

[![sch_Fig01](https://manasataramgini.files.wordpress.com/2021/08/sch_fig01.png?w=600&h=300)](https://manasataramgini.files.wordpress.com/2021/08/sch_fig01.png)Game 1

We see that at the end of the run
![\\tfrac{n}{s}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bs%7D&bg=ffffff&fg=333333&s=0&c=20201002)
remains close to 1 and the mean number of self and non-self neighbors of an agent is not significantly different suggesting that tolerating non-self agents in up to half of the available neighborhoods does not result in segregation at low occupancy and low sociality.

Game 2 is run with the same parameters as above, except that we increase sociality
![s=3](https://s0.wp.com/latex.php?latex=s%3D3&bg=ffffff&fg=333333&s=0&c=20201002).

[![sch_Fig02](https://manasataramgini.files.wordpress.com/2021/08/sch_fig02.png?w=640)](https://manasataramgini.files.wordpress.com/2021/08/sch_fig02.png)  
Game 2

Notably, the increased sociality results in highly significant segregation. It also results in greater clumping of the agents, resulting in clustered but clearly segregated domains.

Game 3 is run with the same parameters as Game 1 but we increase the occupancy
![o=0.6](https://s0.wp.com/latex.php?latex=o%3D0.6&bg=ffffff&fg=333333&s=0&c=20201002).

[![sch_Fig03](https://manasataramgini.files.wordpress.com/2021/08/sch_fig03.png?w=640)](https://manasataramgini.files.wordpress.com/2021/08/sch_fig03.png)Game 3

Here, we see a small but significant reduction of
![\\tfrac{n}{s}](https://s0.wp.com/latex.php?latex=%5Ctfrac%7Bn%7D%7Bs%7D&bg=ffffff&fg=333333&s=0&c=20201002).
Thus, increasing the population with same level of tolerance for non-self by itself results in some segregation that is not seen at low occupancy.

Game 4 is run with
![l=2](https://s0.wp.com/latex.php?latex=l%3D2&bg=ffffff&fg=333333&s=0&c=20201002);
thus, the agent responds to the status of the 24 available lattice points of the neighborhood around it. The occupancy is low
![o=.4](https://s0.wp.com/latex.php?latex=o%3D.4&bg=ffffff&fg=333333&s=0&c=20201002);
![c_n=
11](https://s0.wp.com/latex.php?latex=c_n%3D+11&bg=ffffff&fg=333333&s=0&c=20201002) i.e. less than half the available neighborhood positions tolerated as non-self;
![s=6](https://s0.wp.com/latex.php?latex=s%3D6&bg=ffffff&fg=333333&s=0&c=20201002).

[![sch_Fig04](https://manasataramgini.files.wordpress.com/2021/08/sch_fig04.png?w=640)](https://manasataramgini.files.wordpress.com/2021/08/sch_fig04.png)

Game 4

In these runs we often seen no significant segregation of the agents despite the relatively low tolerance to non-self; however, we see greater clumping of the agents resulting in a more anisotropic distribution of the agents at the conclusion of the run. Thus, when larger neighborhoods are sensed by the agents, even relatively low tolerance for non-self is overridden under low occupancy leading to paradoxical clumping of self and non-self into spatially restricted domains.

Game 5 is similar to 4 but the sociality of the agents is increased to
![s=8](https://s0.wp.com/latex.php?latex=s%3D8&bg=ffffff&fg=333333&s=0&c=20201002).

[![sch_Fig05](https://manasataramgini.files.wordpress.com/2021/08/sch_fig05.png?w=640)](https://manasataramgini.files.wordpress.com/2021/08/sch_fig05.png)  
Game 5

This change has the dramatic effect of moving the agents towards strong segregation along with formation closely packed monotypic domains of the two agents, with clear boundaries. Thus, the sociality parameter drives a phase transition from packing with little segregation despite relatively strong non-self tolerance to nearly complete separation into domains with shared borders.

Game 6 is different from the previous ones in that it senses the relative non-self fraction rather than the absolute count of non-self in the neighborhood,
![f_n=\\tfrac{c_n}{c_t}](https://s0.wp.com/latex.php?latex=f_n%3D%5Ctfrac%7Bc_n%7D%7Bc_t%7D&bg=ffffff&fg=333333&s=0&c=20201002),
where
![c_t](https://s0.wp.com/latex.php?latex=c_t&bg=ffffff&fg=333333&s=0&c=20201002)
is the total number of occupied lattice points in the neighborhood. The sociality factor
![s](https://s0.wp.com/latex.php?latex=s&bg=ffffff&fg=333333&s=0&c=20201002)
is applied just as in the above cases. In this run, we set
![s=0](https://s0.wp.com/latex.php?latex=s%3D0&bg=ffffff&fg=333333&s=0&c=20201002),
i.e. the agent moves only if it has no neighbors.
![f_n=.7](https://s0.wp.com/latex.php?latex=f_n%3D.7&bg=ffffff&fg=333333&s=0&c=20201002),
i.e., the agent move only if the fraction of its non-self neighbors is greater or equal to
![f_n](https://s0.wp.com/latex.php?latex=f_n&bg=ffffff&fg=333333&s=0&c=20201002).
Thus, if an agent has 5 neighbors and 4 of them are non-self then
![f_n=0.8](https://s0.wp.com/latex.php?latex=f_n%3D0.8&bg=ffffff&fg=333333&s=0&c=20201002)
and it would move. We set it to a low occupancy of
![o=0.4](https://s0.wp.com/latex.php?latex=o%3D0.4&bg=ffffff&fg=333333&s=0&c=20201002).

[![sch_Fig06](https://manasataramgini.files.wordpress.com/2021/08/sch_fig06.png?w=640)](https://manasataramgini.files.wordpress.com/2021/08/sch_fig06.png)

Game 6

We observe that even with a low occupancy, high tolerance for non-self and low sociality, relative sensing drives significant segregation. Thus, with relative sensing the
![f_n](https://s0.wp.com/latex.php?latex=f_n&bg=ffffff&fg=333333&s=0&c=20201002)
is the primary determinant of segregation.

What might be some real-life scenarios where these games matter? We can easily imagine the system of agents being a set of living cells showing their agency in response to chemotactic signals. At a macroscopic level, we can imagine these as individual animals (e.g. humans). Indeed, Game 6 was the one played by Schelling as a model for the sociology of segregation. In terms of cells, we can conceive of the following mechanisms: 1) cells are primitively motile; hence, they can move. 2) they can exhibit sociality by means of adhesion molecules (usually proteins) that are expressed on the cell surface. Unless these adhesion interactions are satisfied to a given degree, they would keep moving. 3) They can sense self from non-self. In the simplest case this can again happen via adhesion molecules. Indeed, such mechanisms are used by fungi and ciliates, among others, for discriminating self from non-self for mating or hyphal anastomosis. This kind of adhesion-based self-non-self discrimination can be a mechanism of sensing the absolute number of non-self neighbors. Alternatively, it can happen through sensing of diffusible signals. This mechanism is best suited for relative sensing of the ratio of non-self to total neighbors. Either way the cellular agent could respond to nonself agents in the environment.

Thus, these simple models show how the interplay of sociality and non-self tolerance can result in segregation or paradoxical grouping. In the case of relative sensing (game 6), even with high tolerance and low sociality we see segregation. This is the reality of human societies that many modern occidentally oriented social observers find very hard to swallow. But they are simply tilting against a mathematical reality, much like their medieval representative, old Don Quixote, charging a windmill. Similarly, absolute-count-sensing shows the role of sociality and crowding in segregation (e.g. Games 2, 3 and 5). Greater crowding and sociality can lead to greater segregation when compared to the same, relatively high, tolerance for non-self under low crowding and sociality. Similarly, certain middling level of sociality with sensing of larger neighborhoods can trigger long-lasting clustering without strong segregation despite lower than half tolerance for absolute number non-self agents in the available neighborhood spots (Game 4). This scenario could explain the grouping of bacteria in mixed species biofilms or relatively long-lived clustering of distinct groups in a social setting, e.g. the jāti-s in an Indian village. In conclusion, some social phenomena can be accounted for by simple lattice models of agents which are entirely agnostic to the actual mechanism of agency and sensing.
