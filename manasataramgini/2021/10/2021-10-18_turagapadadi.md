+++
title = "Turagapadādi"
full_title = "Turagapadādi"
date = "2021-10-18"
upstream_url = "https://manasataramgini.wordpress.com/2021/10/18/turagapadadi/"

+++
Source: [here](https://manasataramgini.wordpress.com/2021/10/18/turagapadadi/).

Turagapadādi

This note stems from a recent conversation with a friend, where he
pointed out that the graph representing all possible positions the horse
(knight) can take on the chessboard from a given starting square
produces interesting graphs. It struck us that this would indeed be an
interesting exploration to introduce neophytes into the graph theory and
computational exercises relating to it. Hence, we prepared this
elementary note for pedagogical purposes and to show some pretty
pictures. The origin of this class of problems lies in the Hindu
tradition of citrabandha-s and yukti-s, which have been extensively
discussed and illustrated by various medieval authors in kāvya and
encyclopedic literature (e.g. Mānasollāsa of the Cālukya emperor
Someśvara-deva). In his Śiśupāla-vadha, Māgha states:

viṣamaṃ sarvatobhadra-cakra-gomūtrikādibhiḥ ।  
ślokair iva mahākāvyaṃ vyūhais tad abhavad balam ॥  
That force was difficult to penetrate being equipped with  
the sarvatobhadra, cakra and gomūtrikā and like of formations,  
even as a mahākāvya furnished with such verses.

Here, he uses a simile to compare the military formations like
sarvatobhadra (comparable to the Roman testudo), etc., with the
equivalent citrabandha-s or structural constraints used in kāvya.
Several of the early medieval examples of such citrabandha-s in kāvya
are related to the description of battle scenes: e.g., the Haravijaya of
Rājānaka Ratnākara, the Śiśupāla-vadha of Māgha, the [Kirātārjunīya of
Bhāravi](https://manasataramgini.wordpress.com/2013/01/06/between-the-rasarnava-and-the-chitrabandha-s/)
and the Jānakīharaṇa of Kumāradāsa; thus, it seems likely that the
authors were trying to embed images of the yuddhavyūha-s of the yuddha-s
under description in their kāvya, as suggested by the above verse of
Māgha. However, such devices are also used widely in stotra literature,
for instance to depict the weapons of the deities instead of the vyūha-s
— the Kaśmīrian Sāmavedin, Rudraṭa Śatānanda, uses such in his
Durgāṣṭaka. Since we first learned of the use of such structural
constraints in kāvya in our youth from the praise of Durgā by the great
Kaśmīrian kavi Ānandavardhana, it struck us that just as they have place
in illustrating battle-formations, they also represent an early example
of using ideas that intersect with graph theory and symmetry with far
more general implications. Indeed, even as the “Kavi-prajāpati (to use
Kalhaṇa’s term)” selects for such constraints to bring meaning to his
kāvya, natural selection picks such constraints in words formed by the
alphabet of nucleic acids and proteins to generate biochemical function.

Keeping with the military connections of the citrabandha-s, one such
citrabandha, the turagapada, is based on the horse’s movements in that
ultimate “war-game” which spread widely in the Gupta age, caturaṅga,
i.e., the steps of a horse on the chessboard. While we do not play
chess, we found the abstraction to be of interest. On an infinite
chessboard, the horse on a given square can reach 8 other squares
(Figure 1).

[![](https://manasataramgini.files.wordpress.com/2021/10/chess_01.png?w=334&h=336)](https://manasataramgini.files.wordpress.com/2021/10/chess_01.png)**Figure
1. Possible paths of the horse.**

However, some of these are unavailable at squares on the boundary or the
penultimate circuit on a board of finite length and breadth. For
convenience, going forward, we shall only look at square boards. This is
stated for an ![8 \\times
8](https://s0.wp.com/latex.php?latex=8+%5Ctimes+8&bg=ffffff&fg=333333&s=0&c=20201002)
board by emperor Someśvara-deva in his Mānasollāsa thus:

koṇa-pārśvasthitasyāsya turagasya pada-trayam ॥  
koṇasthasya pada-dvandvaṃ prānte pada-catuṣṭayam ।  
dvitīya-valaye koṇe haye pada-catuṣṭayam ॥  
dvitīya-valaye’nyatra pada-ṣaṭkaṃ nigadyate ।  
madhye ṣoḍaśa\[koṣṭheṣu\] sthitasya turagasya ca ॥  
padāṣṭakaṃ vinirdiṣṭaṃ caturaṅga-viśāradaiḥ ॥

In the cell next to the corners, the horse has 3 moves; in the corner
cells, it has 2 moves; interior to these cells, on the border circuit,
it has 4 moves; in the corner cell of the second circuit, it has 4
moves; in the interior cells of the second circuit, it has 6 moves; in
the 16 interior cells, it has 8 moves each. Thus it has been expounded
by the chess experts.

We can consider the cells of an ![n \\times
n](https://s0.wp.com/latex.php?latex=n+%5Ctimes+n&bg=ffffff&fg=333333&s=0&c=20201002)
chessboard, labeled from 1 to
![n^2](https://s0.wp.com/latex.php?latex=n%5E2&bg=ffffff&fg=333333&s=0&c=20201002)
by rows, as the nodes of a graph. An edge connects two nodes in this
graph if they can be reached from each other by the move of a horse —
the turagapada. The horse can make no moves on boards with ![n=1,
2](https://s0.wp.com/latex.php?latex=n%3D1%2C+2&bg=ffffff&fg=333333&s=0&c=20201002).
Figure 2 illustrates the graph for
![n=3](https://s0.wp.com/latex.php?latex=n%3D3&bg=ffffff&fg=333333&s=0&c=20201002).
One can easily see that the horse can reach every cell from every other
cell except for cell 5. Thus the graph is a simple cycle of 8 nodes with
one disjoint node 5.

[![](https://manasataramgini.files.wordpress.com/2021/10/chess_02.png?w=318&h=310)](https://manasataramgini.files.wordpress.com/2021/10/chess_02.png)**Figure
2. Moves of a horse on a ![3 \\times
3](https://s0.wp.com/latex.php?latex=3+%5Ctimes+3&bg=ffffff&fg=333333&s=0&c=20201002)
board.**

From
![n=4](https://s0.wp.com/latex.php?latex=n%3D4&bg=ffffff&fg=333333&s=0&c=20201002)
board onward (Figure 3), we get single-component graphs with no disjoint
nodes. From
![n=4](https://s0.wp.com/latex.php?latex=n%3D4&bg=ffffff&fg=333333&s=0&c=20201002),
all the graphs have 4 nodes with just two connections corresponding to
the corners of the board, as mentioned by Someśvara. The nodes are
colored as per the number of edges connecting to them. This graph can be
rendered as a 3D object, which, in principle, could be the structure of
a hydrocarbon. However, it remains unclear to us if such a hydrocarbon
exists or can be synthesized in reality.

[![](https://manasataramgini.files.wordpress.com/2021/10/chess_03.png?w=372&h=305)](https://manasataramgini.files.wordpress.com/2021/10/chess_03.png)**Figure
3. Moves of a horse on a ![4 \\times
4](https://s0.wp.com/latex.php?latex=4+%5Ctimes+4&bg=ffffff&fg=333333&s=0&c=20201002)
board.**

From
![n=5](https://s0.wp.com/latex.php?latex=n%3D5&bg=ffffff&fg=333333&s=0&c=20201002)
onward, we get nodes all the possible connections, namely those with 2,
3, 4, 6, 8. We have a single maximal node at
![n=5](https://s0.wp.com/latex.php?latex=n%3D5&bg=ffffff&fg=333333&s=0&c=20201002),
node 13, with 8 connections. When we render this graph using the
Kamada-Kawai force-direct spring algorithm, we get a structure with
bilateral symmetry and interesting relationships between symmetrically
equivalent neighboring nodes (Figure 4). For example: nodes 1, 19; 7,25,
both pairs differ by 18. The nodes 9, 21; 5, 17 differ by 12. The 4 edge
nodes 8, 12 and 14, 18 represent another such pair of symmetries.

[![](https://manasataramgini.files.wordpress.com/2021/10/chess_04.png?w=408&h=384)](https://manasataramgini.files.wordpress.com/2021/10/chess_04.png)**Figure
4. Moves of a horse on a ![5 \\times
5](https://s0.wp.com/latex.php?latex=5+%5Ctimes+5&bg=ffffff&fg=333333&s=0&c=20201002)
board.**

These graphs lead us to the classic turagapada problem of kāvya and its
solutions, which simply stated goes as: can you find a path such that
the horse visits each cell on the board only once? In terms of the
graph, it can be stated as: can you find the path passing through all
nodes of the horse graph only once. In modern computational literature,
this is called the knight’s tour problem. The above graphs show that no
such tour can exist for ![n=3,
4](https://s0.wp.com/latex.php?latex=n%3D3%2C+4&bg=ffffff&fg=333333&s=0&c=20201002).
For
![n=3](https://s0.wp.com/latex.php?latex=n%3D3&bg=ffffff&fg=333333&s=0&c=20201002),
cell 5 cannot be reached, but the remaining cells can be visited by a
closed cyclic tour path (Figure 5). For
![n=4](https://s0.wp.com/latex.php?latex=n%3D4&bg=ffffff&fg=333333&s=0&c=20201002),
though the graph has a single component, the fact that a pair of 2-edge
nodes connect to the same pair of nodes means that a tour cannot be
completed. However, 15 of the 16 possible cells can be visited on tour
(Figure 6).

[![](https://manasataramgini.files.wordpress.com/2021/10/chess_05.png?w=323&h=322)](https://manasataramgini.files.wordpress.com/2021/10/chess_05.png)**Figure
5. Incomplete turagapada on a ![3 \\times
3](https://s0.wp.com/latex.php?latex=3+%5Ctimes+3&bg=ffffff&fg=333333&s=0&c=20201002)
board.**

[![](https://manasataramgini.files.wordpress.com/2021/10/chess_06.png?w=406&h=408)](https://manasataramgini.files.wordpress.com/2021/10/chess_06.png)**Figure
6. Incomplete turagapada on a ![4 \\times
4](https://s0.wp.com/latex.php?latex=4+%5Ctimes+4&bg=ffffff&fg=333333&s=0&c=20201002)
board.**

From
![n=5](https://s0.wp.com/latex.php?latex=n%3D5&bg=ffffff&fg=333333&s=0&c=20201002)
onward, one can always find multiple tours that visit every cell. Figure
7 shows such an example on a ![5 \\times
5](https://s0.wp.com/latex.php?latex=5+%5Ctimes+5&bg=ffffff&fg=333333&s=0&c=20201002)
board.

[![](https://manasataramgini.files.wordpress.com/2021/10/chess_07.png?w=463&h=463)](https://manasataramgini.files.wordpress.com/2021/10/chess_07.png)**Figure
7. Turagapada on ![5 \\times
5](https://s0.wp.com/latex.php?latex=5+%5Ctimes+5&bg=ffffff&fg=333333&s=0&c=20201002)
board**

It is easy to see with the graph that solving the turagapada by
brute-force walks along the graph is very inefficient and will explode
as
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
increases. However, a simple algorithm for finding a turagapada exists:
(1) Start with a given node and move to a neighboring node from which
the fewest non-0 number of further possible moves are available. For the
possible available moves, only those neighbors which have not yet been
visited are counted. (2) If a tie occurs, then one simply goes to the
cell with a smaller index. (3) While these two steps are sufficient to
yield solutions from several cells, it is not foolproof. Hence, one may
look one level down to see if there are neighbors’ neighbors from which
the fewest possible moves are available to find turagapada-s with
greater certainty.

[![](https://manasataramgini.files.wordpress.com/2021/10/chess_08.png?w=640&h=642)](https://manasataramgini.files.wordpress.com/2021/10/chess_08.png)**Figure
8. Turagapada on ![8 \\times
8](https://s0.wp.com/latex.php?latex=8+%5Ctimes+8&bg=ffffff&fg=333333&s=0&c=20201002)
board**

Figure 8 shows a solution for an ![8 \\times
8](https://s0.wp.com/latex.php?latex=8+%5Ctimes+8&bg=ffffff&fg=333333&s=0&c=20201002)
board using the above algorithm starting from cell 1. Given that
Someśvara explicitly lists out all the possible moves from a given cell,
he implicitly seems to have used a similar algorithm with symmetry
considerations to find a turagapada. He specifies it by first providing
a chessboard with coordinates indicated by the syllables formed by the
first 8 vowel conjunctions (a, ā, i, ī, u, ū, e ai) of the 8 consonants
(c, g, n, d, ṭ, r, s, p). He then gives the turagapada asā sequence of
64 syllables shown below (Figure 9).

**![Chess_09](https://manasataramgini.files.wordpress.com/2021/10/chess_09-2.png?w=640)Figure
9. Someśvara’s turagapada**.

pa si pu se ṭai ne cai gū । nī cu gi ca nā ṭa sā pī ।  
sū pai re dai ge dū gu ci । ga dā ra pā sī pū sai ṭe ।  
nai ce nū gai cū gī cā na । ṭā sa pi su pe rai de nu ।  
ṭū rī di ṭu ri dī ru ṭi । du ni cī gā da rā ṭī rū ।

Other than this yukti presented by Someśvara, several kavi-s have given
their own solutions for complete tours. We have Rudraṭa’s solution in
the form of a prosodic pattern with repeating strings of nā and lī
interspersed between two distinct syllables, namely se and le
(supposedly you can use the principles of saṃdhi and samāsa-vigraha to
read this as a Sanskrit verse). His commentator, Namisādhu, provides a
mnemonic using the Sanskrit varṇamālā. Ratnākara and
Veṅkaṭanātha-(Vedānta) deśika provide pairs of verses with one laying
the chessboard and the other providing a solution tour. Rudraṭa,
Ratnākara and Veṅkaṭanātha, exploit the fact that the anuṣtubh meter has
four feet of 8 syllables each. Thus, they can cover 32 syllables or half
a chessboard with a single śloka. This solution is symmetric; hence, it
can be reflected to provide a full board solution. The widespread use of
turagapada as a citrabandha, from Kāśmīra to Drāviḍa, suggests that a
version of the algorithm stated above was imparted in traditional
medieval education.

This tradition was transmitted to the Mohammedans, and from them, it
appears to have been transmitted to Europe. However, to our knowledge,
the first solution appears relatively late in Europe, being provided by
Leonhard Euler. William Hamilton considered a related problem: let a
dodecahedron represent a graph with 20 nodes and 30 edges. Find a cyclic
path that passes through all edges only once. Here every node is
connected to 3 edges. A similar question can be asked for the
horse-graph — i.e., finding a complete tour that is also a cycle. A
solution to this problem is recorded in the late medieval encyclopedia
of Nīlakaṇṭha Bhaṭṭa (Bhagavanta-Bhāskara), but I do not have it handy
right now. In any case, a vast body of literature exists on algorithms
for tours and their use in kāvya; hence, we do not tarry any more on
this point.

Finally, few other interesting questions emerge from the horse graphs.
First, the diameter of a graph is defined as the longest shortest path
between two nodes of a graph. The distance between two nodes is a
geodesic — i.e., the shortest path along the graph. The longest such
geodesic between any two pairs of nodes in the graph is its diameter.
For the horse graph with ![n=3, 4, \\cdots,
14](https://s0.wp.com/latex.php?latex=n%3D3%2C+4%2C+%5Ccdots%2C+14&bg=ffffff&fg=333333&s=0&c=20201002)
we can compute this sequence to be: 4, 5, 4, 4, 5, 6, 6, 7, 8, 8, 9, 10.
Can one come up with a closed expression for this?

Second, there are
![m](https://s0.wp.com/latex.php?latex=m&bg=ffffff&fg=333333&s=0&c=20201002)
shortest paths between node 1 and node
![n^2](https://s0.wp.com/latex.php?latex=n%5E2&bg=ffffff&fg=333333&s=0&c=20201002)
for a given horse graph. For ![n=3, 4, \\cdots,
8](https://s0.wp.com/latex.php?latex=n%3D3%2C+4%2C+%5Ccdots%2C+8&bg=ffffff&fg=333333&s=0&c=20201002)
this sequence goes as: 2, 2, 8, 4, 6, 108. A colleague of ours, a
professional mathematician, showed us a complicated formula that can
describe this strange sequence. While I am not providing that here, it
shows a dramatic jump whenever ![n \\mod 3 \\equiv
2](https://s0.wp.com/latex.php?latex=n+%5Cmod+3+%5Cequiv+2&bg=ffffff&fg=333333&s=0&c=20201002).
Thus, we see a jump at
![n=8](https://s0.wp.com/latex.php?latex=n%3D8&bg=ffffff&fg=333333&s=0&c=20201002),
making it more than the number of shortest paths found for the ![n=9,
10](https://s0.wp.com/latex.php?latex=n%3D9%2C+10&bg=ffffff&fg=333333&s=0&c=20201002).
Thus, it appears the inventors of the game chose
![n](https://s0.wp.com/latex.php?latex=n&bg=ffffff&fg=333333&s=0&c=20201002)
to provide a maximal diversity in the movement of the horse for boards
of a similar order.
