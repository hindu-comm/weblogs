+++
title = "Nature is a Computer How"
full_title = "Nature is a Computer How Physics is just Dijkstra's Algorithm with Infinite Resolution"
upstream_url = "https://ramaseshanchandrasekaran.substack.com/p/nature-is-a-computer-how-the-universe"
date = "2026-05-08"
+++
Source: [here](https://ramaseshanchandrasekaran.substack.com/p/nature-is-a-computer-how-the-universe).

Nature is a Computer : How Physics is just Dijkstra's Algorithm with Infinite Resolution 

# Nature is a Computer : How Physics is just Dijkstra's Algorithm with Infinite Resolution

### How just one common sensical principle of optimality used widely in the discrete world of computing is also behind most of the concepts in the continuum world of physics

[](https://substack.com/@ramaseshanc)

![Rama Seshan Chandrasekaran's avatar](https://substackcdn.com/image/fetch/$s_!ZHOm!,w_36,h_36,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11e50d60-b811-4831-8bbc-4d320762e60b_96x96.png)

[Rama Seshan Chandrasekaran](https://substack.com/@ramaseshanc)

Dec 26, 2025

13

3

3

Share

There are few concepts in mathematics that have a reach that far exceeds their simplicity and elegance. In this article, I write about one such principle - the **Bellman’s Principle of Optimality** and an algorithm based on it which is the **Dijkstra’s algorithm**. Hope you enjoy it!

[](https://substackcdn.com/image/fetch/$s_!8E6J!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F097c2e8e-32d0-420d-bddb-11cbe18f679b_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!8E6J!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F097c2e8e-32d0-420d-bddb-11cbe18f679b_2816x1536.heic)

**Note** : This is quite a long article and has lots of topics at various levels. As you move along, you may find some topics very simple and some topics very complex. I have written it in such a way that any curious person with basic school level of mathematics can follow along and is intrigued. But I do hope that there is something in it for everybody (even lay people) and I also think lay people can enjoy this article even though if not following every argument and proof (feel free to skip any math-heavy argument or proof). Please do skim through the easy parts even though it is trivial because it will set the language and notation for talking about the difficult parts.

# Bellman’s Principle of Optimality

This principle is so obvious that you might be surprised by the hype I am giving it. Consider the problem of finding the path of shortest time between your home A and your office E taking into consideration, the road map and traffic statistics of your city. Let us assume that you have found the path of shortest time by some method. Let us assume that this optimal path involves passing through a point C (central square).

Now, let us say that you are on that optimal path from home A to office E and when you are at the central square C, your co-worker who is starting off from his house there, asks you that what is the path that takes the shortest time from the central square C to the same office E? What would you say?

Bellman’s Optimality Principle states that you will recommend your co-worker to follow along with you and continue along the same path that you are on. The path that is optimal from A to E and passes through C, is also the optimal path from C to E. This is illustrated in the diagram below where the optimal paths are shown in blue.

[](https://substackcdn.com/image/fetch/$s_!gas8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76332c6f-2229-43a2-ace8-33f35b4fa2ad_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!gas8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76332c6f-2229-43a2-ace8-33f35b4fa2ad_2816x1536.heic)

How so? Let us try to prove this mathematically. This works because the total time taken (which is to be minimised here in this optimisation problem) is additive across the path ; the time taken on your trip from Chennai to Delhi that passes via Bangalore is the sum of the time taken from Chennai to Bangalore and the time taken from Bangalore to Delhi. This additivity of the cost (that has to be minimised) is what is crucial in proving the optimality of the subpaths. Let us now prove it more formally.

> **Proof of the Optimality Principle by Contradiction** :
>
> Assume that your proposed blue path A-C-E is optimal from A to E and
> passes through C. Also, for the sake of contradiction assume that the
> blue sub path C-E is not optimal from C to E and that somebody else is
> able to give another yellow path C’-E’ (see the diagram) as the
> optimal path from C to E.
>
> Now, consider the composite path that follows the blue one in the
> route A-C from A to C but follows the yellow path C’-E’ from C to E.
> Now, because of our contradictory assumption that the yellow path
> C’-E’ takes shorter time than C-E (because it is the optimal path), we
> have
>
> \\Time(C'E') \< Time(CE)\\
>
> Now add the time taken from A to C both sides of the equation above,
> we get
>
> \\Time(AC) + Time(C'E') \< Time(AC) + Time(CE)\\
>
> But due to the additivity of the time, we have that the sum of the
> time taken between A-C and between C’-E’ is the total time taken in
> the composite path A-C’-E’ in LHS. Similarly in the RHS, the sum of
> the time taken between A-C and between C-E is the total time taken in
> the path A-C-E the original blue path). This means that the equation
> above is telling us
>
> \\Time(\text{composite path}) \< Time(\text{blue path})\\
>
> But this means that the composite path takes lesser time to go from A
> to E than the blue path from A to E. This contradicts the original
> assumption that the blue path A-C-E is the optional path from A to E
> because if a path is time-optimal, there can be no other path takes
> lesser time than it. But here we have come across another path that
> challenges the assumption that A-C-E is optimal. So we assumed
> something contrary to the statement that we want (that the subpaths of
> an optimal path are not optimal) and we got something stupid. That is
> how proofs by contradiction work. To prove something is true, assume
> it is not true, and then derive something stupid (illogical) from it
> so that the something is forced to be true.

The formal statement of Bellman's Principle is :

For additive costs, the sub-path of any optimal path is also optimal

This principle is so simple right?

# Rama at Crossroads

Let us now consider an instance of the road routing problem in more detail to inspire a more general class of problems called **dynamic programming**. Consider the road map of a part of a city shown below with the time taken in minutes along each segment of the road marked. The roads are all one way and can be traversed only in the directions marked.

[](https://substackcdn.com/image/fetch/$s_!JBgb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff68bdf5b-6cd1-4da0-ae57-6d4146831661_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!JBgb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff68bdf5b-6cd1-4da0-ae57-6d4146831661_2816x1536.heic)

Assume that a biker named Rama wants to start from the initial point “a” and wants to reach “h” in minimum time. Now, instead of an exhaustive search of considering all possible paths and calculating all their times and choosing one that minimises, Rama wants to do something intelligent so that he can develop a very generic algorithm out of it. Rama had heard an inspiring quote that one finds his own happiness by making others happy.

So, he decides to start helping others. It is obvious to Rama that the optimal path from the points ‘e’ and ‘g’ are simply following the direct road connecting them to the destination ‘h’ as they are directly connected to it by road. And it will take 8 minutes from ‘e’ to ‘h’ and ‘2’ mins from ‘g’ to ‘h’. This is shown in violet below.

[](https://substackcdn.com/image/fetch/$s_!xnSf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5f45055e-e3ef-4548-81cd-e04851f87c72_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!xnSf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5f45055e-e3ef-4548-81cd-e04851f87c72_2816x1536.heic)

Now, Rama wants to help his friend Krishna whose house is in ‘f’ and wants to reach ‘h’. Rama now finds this problem much easier to solve. He knows that there are only two ways to go from ‘f’ to ‘h’. Either via ‘e’ or via ‘g’. He calculates the total cost to go from ‘f’ to ‘h’ along both these paths to compare :

F-G-H : Total cost = 3 + 2 = 5

F-E-H : Total cost = 2 + 8 = 10

Obviously, Rama knows that the best path here is F-G-H via G as its time taken is lower. So, Rama now asks Krishna to go to ‘h’ via ‘g’ and notes in his register that the minimum time taken from ‘f’ to ‘h’ is 5 (via F-G-H). His note is shown below.

[](https://substackcdn.com/image/fetch/$s_!rkWd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd0416080-04a0-4171-ad44-a158adbbdade_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!rkWd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd0416080-04a0-4171-ad44-a158adbbdade_2816x1536.heic)

Now, Rama continues his resolve to help his friends. He has another friend Guha, whose house is at ‘d’ and wants to reach ‘h’. Rama finds this easy now. From ‘d’, Guha can only go to ‘e’ as that is the only option. And from ‘e’, Guha can directly g to ‘h’. So, the only path (if there is only one option, it is trivially the best) from ‘d’ to ‘h’ is D-E-H and the total time taken from ‘d’ along that path is 3 + 8 which is 11. Rama notes this in his register which is shown below in violet.

[](https://substackcdn.com/image/fetch/$s_!u1KO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc718fd9b-707f-4ee7-8877-6c9bc0673a15_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!u1KO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc718fd9b-707f-4ee7-8877-6c9bc0673a15_2816x1536.heic)

Rama continues helping. Another friend Sudama is now in ‘c’ and wants to reach ‘h’. Now Sudama has two immediate steps that he can take - he can either go to ‘d’ or ‘f’ from there. But if Sudama goes to ‘d’, it will take him 5 minutes to go there and from ‘d’, the shortest path to ‘h’ will take him 11 minutes (as already evaluated for Guha). But if Sudama goes to ‘f’, it will take him 3 minutes to go there and from ‘f’, the shortest path to ‘h’ will take 5 minutes (as already evaluated for Krishna). So, Rama now compares the two options.

C-D → H : Cost = 5 + 11 = 16

C-F → H : Cost = 3 + 5 = 8

So, the better option here is to go via F and hence Krishna recommends Sudama to go on the path via F with the minimum time from there taking 8 minutes. Rama now updates this in his register as shown below.

[](https://substackcdn.com/image/fetch/$s_!XXHY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5dc85905-d609-48c1-adc1-da15415b1429_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!XXHY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5dc85905-d609-48c1-adc1-da15415b1429_2816x1536.heic)

Finally, Rama’s another friend Vibhishana at ‘b’ calls who also wants to reach ‘h’. Vibhishana has only one immediate option which is to go to ‘c’. And from ‘c’, Rama has already found the optimal path from there and already recommended it to Sudama. The total optimal time taken for Vibhishana from ‘b’ would be 9 minutes to go to ‘c’ plus the 8 minutes to go to ‘h’ which is 17. Rama notes this now in his entry which is shown below.

[](https://substackcdn.com/image/fetch/$s_!kjDV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7e662cc4-03a9-45b1-92c4-d6a419e3bd82_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!kjDV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7e662cc4-03a9-45b1-92c4-d6a419e3bd82_2816x1536.heic)

Now, Rama is stunned. He now figures out that he can solve his own problem. He wants to go to ‘h’ in minimum time. His only immediate options are to go to either ‘d’ other ‘b’. But he had already helped Guha from ‘d’ and Vibhishana at ‘b’. The shortest time from ‘b’ would be 17 minutes (as for Vibhishana) while the shortest time from ‘d’ would take 11 minutes as done for Guha. Now Rama compares the total cost of both the options :

A-D → H : Total cost = 8 + 11 = 19

A-B → H : Total cost = 5 + 17 = 22

So, Rama now determines that the best thing to for him is to go to ‘d’ and then be on the path that he recommend to Guha so that the total cost would be 22 minutes only.

[](https://substackcdn.com/image/fetch/$s_!RurM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F60cd9cd1-9a87-44b8-aab4-ba429b547716_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!RurM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F60cd9cd1-9a87-44b8-aab4-ba429b547716_2816x1536.heic)

Note that Rama has helped himself by helping others. He first found out the trivial solution from points “e” and “g”. Then, he helped Krishna from “f” using the trivial solutions in “e” and “g”. Then, he helped Guha at ‘d’ and Sudama at ‘c’. Finally he helped Vibhishana. In each iteration, he finds that the help that he had given in the previous iterations had come in handy and as he kept on helping friends nearer to ‘h’ , he eventually helped himself using all the previous help that he had done. All this involved the use of Bellman’s principle of optimality. Rama knows that his optimal path from “a’ has to contain an optimal subpath. So, since he had two options - 'd’ and ‘b’, he knew the optimal subpaths from ‘d’ and ‘b’ by helping Vibhishana and Guha. So, he used that information to decide what was best for him. Note that Rama had to finally just take a one-shot decision - whether to go to ‘d’ or ‘b’. Since he had already decided what is optimal from ‘d’ and ‘b’, and knew that his own optimal path would also be made of optimal subpaths (from either ‘b’ or ‘d’), he now had to choose between just ‘b’ and ‘d’. So, you see this iteration proceeding backwards from ‘h’ and hitting the target initial point ‘a’ ? This is the essence of **dynamic programming**.

The process of solving step-by-step starting near the final point and using that to expand far and wide until we hit our target initial point where we make more nodes violet - let me call it by an informal name - let me call it as “**the violet-ification of space**”. Formally in the literature of dynamic programming, it is called “**backward induction**”.

There are also a lot of advantages in following this approach of helping everyone else until you find the help needed for yourself. One is that you can handle changes easily. If someone lays a new road from a new intersection, you can utilise the optimal costs for the old network and solve for the case where one starts from the newly constructed intersection. If you find that one road is closed upon arrival, no problem again - you can follow the sub-optimal path from there on.

# Dynamic Programming

Now that we have solved a routing problem by hand, let us step back and analyse in more abstract terms what we actually did. We didn't just stumble upon the answer; we followed a rigorous, repeatable process. This process is the heart of Dynamic Programming. To formalise this, we need to translate our "intersections" and "roads" into the universal language of systems and control.

### Components

#### Formulation

Every discrete dynamic programming problem, whether it's routing a car, landing a rocket, or managing a stock portfolio, has these four defining characteristics:

1.  **Stage / Time / Iteration** : In our road map, the “stages” were
    implicit—they represented how far along we were. In a general
    system, a stage usually represents **time** or **iteration**.

    - *Notation:* **k** = 0, 1, 2, … , N (where N is the final time)

2.  **State :** The state is the information you need to know right now
    to make a decision. In our example, the state was simply “at which
    intersection am I at?” (e.g., x = node ‘c’ ).

    - *Notation:* **x(k)** is the state of the system at stage k

3.  **Control / Decision / Policy :** This is the choice you make from a
    given state at a given stage/time. At intersection c, our control
    options were either “Go East to f” or “Go North to d.”

    - *Notation:* **u** is the control applied at stage k from state
      x(k)

4.  **Dynamics :** This is the rule of physics or logic that tells you
    where you will end up next, if you are at a given state at a given
    time and apply the given control. In the routing problem, the
    dynamics says that if you are at ‘c’ at time now and choose the
    control option “North,” you will end up at d in the next instance.
    More generically, it is notated as “f” and written as :

    - *Notation:* x(k+1) = f (x(k),u(k))

#### Cost Function

We don't just want *any* path; we want the *best* path. To define "best," we need a cost function. In the routing problem we considered, the cost was time. In general, the cost has two components :

1.  **Running Cost** : The cost incurred during a single step. In our
    map, these were the numbers (time in minutes) written on the arrows
    (e.g., traveling c→d costs 3 minutes). Note that the cost depends on
    both the current state an the current input - in our case, the cost
    we incur on a step depends on both the state (which is the current
    intersection where I am at now), and also on the controls that I
    take (the road I choose to follow) ; for example ; if I am at ‘c’,
    and decide to go ‘north’, I incur a running cost of 5 minutes of
    time.

    - *Notation:* L(x(k),u(k))

2.  **Terminal Cost** : The penalty for where you end up at the very
    end. In our map, reaching the destination h had a "penalty" of 0,
    but if we had stopped anywhere else, the penalty would have been
    infinite (failure) because we had a hard constraint that we had to
    be finally at ‘h’.

    - *Notation:* ϕ(x(N))

3.  Total Cost : The sum of running cost between each unit of time and
    the terminal cost.

    - *Notation:* S

\\S = \sum\_{k=0}^{N-1} L(x(k),u(k)) + \phi(x(N))\\

#### Backward Induction : The Bellman Equation (from the Principle of Optimality)

This is the equation that describes abstractly how we solved our map. Recall how we calculated the value for intersection c.

> *“The cost from ‘c’ is the immediate travel time to the next
> intersection, PLUS the optimal cost from that next intersection to the
> end.”*

Mathematically, if V(x) is the minimum cost to go from state x to the end, we wrote:

\\V(c) = \min \left\\ \begin{aligned} & \text{Cost}(c \to d) + V(d) \\ & \text{Cost}(c \to f) + V(f) \end{aligned} \right\\\\

This function V(x) is called as “the cost to go” from ‘x’. We can then generalise this equation abstractly into what is called as the **Discrete Bellman Equation**. Since the next state x(k+1) is described by the dynamics x(k+1) = f(x(k),u(k)), the fundamental recurrence relation of dynamic programming is :

\\V(x_k) = \min\_{u_k} \Big\\ \underbrace{L(x_k, u_k)}\_{\text{Running Cost from x(k) to x(k+1)}} + \underbrace{V(f(x_k, u_k))}\_{\text{Optimal Cost from x(k+1) to the end}} \Big\\\\

**Why is the above equation powerful?** It turns a massive, overwhelming search problem into a sequence of tiny, manageable decisions. You never worry about the whole path at once. You only worry about **one step** and trust that the V(⋅) function has already taken care of the rest.

Now we will see several applications of dynamic programming and see the implementation of a systematic algorithm to evaluate the value function V for a generic class problems. Once the value functions at all intersections are updated, the optimal path is obtained by simply solving the Bellman equation.

# Dijkstra's Algorithm & the Internet

What is the shortest way to travel from Rotterdam to Groningen, in general: from given city to given city. It is the algorithm for the shortest path, which I designed in about twenty minutes. One morning I was shopping in Amsterdam with my young fiancée, and tired, we sat down on the café terrace to drink a cup of coffee and I was just thinking about whether I could do this, and I then designed the algorithm for the shortest path. As I said, it was a twenty-minute invention. In fact, it was published in ‘59, three years later. The publication is still readable, it is, in fact, quite nice. One of the reasons that it is so nice was that I designed it without pencil and paper. I learned later that one of the advantages of designing without pencil and paper is that you are almost forced to avoid all avoidable complexities. Eventually, that algorithm became to my great amazement, one of the cornerstones of my fame.

— **Edsger Dijkstra**, in an interview with Philip L. Frana, Communications of the ACM, 2001

The problem of moving data packets from your laptop to a server across the globe is, at its core, the same as our toy road map problem. The internet system is a massive road network (called a **graph** / **network**) where intersections (called **nodes**) are your routers and the roads (called **edges**) are fibre optic links. Each link has a "cost"to minimise (that usually captures either latency \[time delay\] or bandwidth congestion). Routing protocols like **OSPF (Open Shortest Path First)**, used extensively in large enterprise and ISP networks, rely on every router calculating the fastest path to every other network segment. They do this using what is called in computer science as the **Dijkstra's algorithm** or **greedy algorithm,** also called as **uniform-cost search** by the AI community.

Let us motivate this algorithm now. We have formulated the DP that is too generic. We expand neighbour by neighbour starting from the final node. But we might not want to help everybody and prioritise our expansion strategy so that the initial target is reached as fast as possible. Also, we have to be more systematic as to what nodes we help first and what node we help next - closeness to the target may not always be a good criterion to choose. Because of these two things, we need an important algorithm called the **Dijkstra’s algorithm**. This is efficient way to find the value function by iterative updation (for subsequently to be used in the Bellman equation to find the optimal path as was shown in the above example). For a vast class of problems—specifically those where the “cost” of a step is never negative (like distance or time)—the premier solution is **Dijkstra’s Algorithm**. While often taught in introductory computer science as a “**greedy algorithm**” Dijkstra is best understood as a highly optimised implementation of Dynamic Programming where the initial node is reached as soon as possible. It uses the Principle of Optimality to systematically propagate a kind of “wavefront” (the ripples that you see when you drop a stone in a pond of water) of solved states.

Let me first illustrate this with a toy example as usual. To visualise, imagine the destination node S emits a pulse of violet light. This light travels along the roads “upstream” (against the direction of traffic). The speed at which the light travels along a road is inversely determined by the road’s cost (higher cost = slower travel) ; that is the violet light hits the lower cost-to-go nodes first. Let us divide the nodes into three categories :

1.  **Settled nodes** : Nodes that have gotten the violet light and
    whose optimal cost-to-go (or value function) we know for sure.

2.  **Current Node** : The node of interest now that is about to get the
    violet light next

3.  **Fringe nodes / Discovered Nodes** : Neighbours of the current node
    and the other nodes (neighbours of previous violet nodes) that we
    have visited but whose optimal cost-to-go we know only tentatively
    (will be updated as we explore further).

4.  **Unvisited nodes** : Nodes that have not been interacted with at
    all

Step 1 : Initial State

We begin with a graph where the source node **S** is our starting point. Its cost-to-go is 0. All other nodes have an infinite ∞ (in practice, a very large number) cost-to-go, as we haven't found the cost-to-go (optimal cost of the optimal path) from them yet. The source node is the first "fringe" node and is selected as the current node.

[](https://substackcdn.com/image/fetch/$s_!-d_A!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2f749aee-da13-4f99-9ea6-e4fa498185a4_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!-d_A!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2f749aee-da13-4f99-9ea6-e4fa498185a4_2816x1536.heic)

Step 2 : Processing Node S

We explore the neighbours of the current node, **S**.

- The path to **A** has a cost of 0 (cost of S) + 1 (edge S-A) = 1.

- The path to **B** has a cost of 0 (cost of S) + 5 (edge S-B) = 5.

We update the costs of A and B with their tentative optimal cost-to-go as 1 and 5 respectively and add them to the “fringe” (black). Node S is now “settled” (violet) because we have processed all its neighbors. We then look at the fringe nodes (A and B) and pick the one with the lowest cost to be the next current node that will get the violet light next and from where the next search operation will begin. The winner is **A** with a cost of 1.

[](https://substackcdn.com/image/fetch/$s_!W9r-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fea8174c7-0072-4d69-8e33-ccde805a6753_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!W9r-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fea8174c7-0072-4d69-8e33-ccde805a6753_2816x1536.heic)

Step 3 : Processing Node A

Now A is the current node. We look at its neighbors. S is already settled, so we ignore it. The only other neighbor is **C**.

- The path to **C** has a cost of 1 (cost of A) + 1 (edge A-C) = 2.

We update C’s cost to 2 and add it to the fringe. Node A is now settled. The fringe nodes in black are now B (cost 5) and C (cost 2). We pick the one with the lowest cost, which is **C** and move on it, making A violet.

[](https://substackcdn.com/image/fetch/$s_!CPd1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fffdd3f6b-a1a2-43ed-96e2-f83f0d82730e_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!CPd1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fffdd3f6b-a1a2-43ed-96e2-f83f0d82730e_2816x1536.heic)

Step 4 : Processing Node C

**C** is the current node. Its neighbours are A (already settled) and **D**.

- The path to **D** has a cost of 2 (cost of C) + 1 (edge C-D) = 3.

We update D’s cost to 3 and add it to the fringe. Node C is now settled. The fringe nodes are B (cost 5) and D (cost 3). We pick **D** as it has the lower cost 3. (Note that B is still not selected)

[](https://substackcdn.com/image/fetch/$s_!r-0h!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F363b2268-1d43-4457-999e-7c6eb4d56b40_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!r-0h!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F363b2268-1d43-4457-999e-7c6eb4d56b40_2816x1536.heic)

Step 5 : Processing Node D

**D** is the current node. Its neighbors are C (settled), **B**, and **T**.

- **For B**: The path via D has a cost of 3 (cost of D) + 1 (edge D-B)
  = 4. The current cost of B is 5. Since 4 is less than 5, we **update
  B’s cost to 4**. This is a crucial difference from simple dynamic
  programming: we can update the cost of a node that is already in the
  fringe if we find a shorter path to it.

- **For T**: The path to **T** has a cost of 3 (cost of D) + 1 (edge
  D-T) = 4.

We update B’s cost, add T to the fringe with a cost of 4, and settle node D. The fringe now contains B (cost 4) and T (cost 4). We can choose either; let’s pick **T**.

[](https://substackcdn.com/image/fetch/$s_!ARSD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4d24d7b8-46ee-41d1-b371-0241b6f265ac_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!ARSD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4d24d7b8-46ee-41d1-b371-0241b6f265ac_2816x1536.heic)

Step 6: Final State

**T** is the current node. Its neighbors are B and D.

- **For B**: The path via T has a cost of 4 (cost of T) + 1 (edge T-B)
  = 5. The current cost of B is 4. Since 5 is not less than 4, we do not
  update B’s cost.

- **For D**: The path via T has a cost of 4 (cost of T) + 1 (edge T-D)
  = 5. Node D is already settled with a cost of 3, so we do not update
  it.

Node T is now settled. Since T is our target node, the algorithm terminates. We have found the shortest path from S to T, which is **S
-\> A -\> C -\> D -\> T** with a total cost of **4**. Node B remains a fringe node because it was never selected as the minimum-cost node before the algorithm finished.

[](https://substackcdn.com/image/fetch/$s_!f3fL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F69dd5146-7165-469a-a150-6b32ffdbe412_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!f3fL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F69dd5146-7165-469a-a150-6b32ffdbe412_2816x1536.heic)

**In summary, Dijkstra's algorithm works like a wavefront in propagation of light wave, always expanding from the source node itself and then progressing to make nodes violet so that those nodes that have smaller known cost-to-go (value function) from the source get coloured violet first.**

> Note this bolded sentence firmly for it will be pivotal when we study
> about propagation of light in a future section .

This greedy strategy, combined with the ability to update the costs of fringe nodes after selecting them carefully, allows it to efficiently find the shortest path in a graph with non-negative edge weights, distinguishing it from more general dynamic programming approaches.

Note that the optimal path from B is not the direct edge connecting it to S which has a high cost 5 but the indirect one B-D-C-A-S which has only cost 4 which is lower. This is why B remains fringe for a long time before it gets violet-ified. In the toy example above, we did not face this issue because the graphs were directed and had no multiple paths between any two nodes.

> Dijkstra’s algorithm is thus a systematic way of evaluating the
> cost-to-go by successive updation as the algorithm expands from the
> source to the target, violet-ifying all nodes one-by-in the order of
> their increasing cost-to- go value functions.

[](https://substackcdn.com/image/fetch/$s_!eLeW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1f15b539-c553-4de9-b79c-e3239e6f11cd_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!eLeW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1f15b539-c553-4de9-b79c-e3239e6f11cd_2816x1536.heic)

Now let us present the algorithm systematically. To align with our “cost-to-go” approach, we will solve for the shortest path to a fixed destination node (x_end) from everywhere else. The algorithm maintains two sets of nodes:

1.  **The Settled Set (Violet):** Nodes for which the light has fully
    arrived. We know absolutely the fastest way from these nodes to the
    end. Their V(x) value is frozen.

2.  **The Fringe Set (Grey):** Nodes that the light has reached, but we
    aren’t sure if it’s the fastest ray of light yet (like the fringe
    node B which remained fringe and whose tentative cost-to-go remained
    5 until we found a lower alternative) . We have a *tentative* V(x)
    value for the fringe nodes but until they are selected as lowest
    cost neighbour in some stage and become violet, this V(x) remains
    only tentative for them.

**The Algorithm Steps:**

1.  **Initialise:** Set the “cost-to-go” V(x_end)=0. Set all other nodes
    tentatively to infinity (V(x)=∞). Place the destination node into a
    priority queue (a list sorted by current cost).

2.  **Select Best Candidate:** Look at the Fringe set (the priority
    queue) and pop the node with the *smallest* current V(x). Let’s call
    this current node u.

3.  **Settle:** Color node u **violet**. Because edge costs are
    non-negative, we know for a fact that we will never find a faster
    path to the end from u later on. Its value is locked.

4.  **Relax Neighbors:** Look at all nodes v that can reach u (incoming
    edges). Apply the Bellman logic:

    - *New proposed cost* = Cost to get from v to u + V(u).

    - If this *New proposed cost* is lower than the current tentative
      V(v), update V(v) to this new lower value. Add v to the Fringe set
      if it wasn’t there already.

5.  **Repeat:** Loop back to step 2 until all reachable nodes are
    settled.

Why is this more efficient than just trying every path? Because once a node turns violet, we never have to process it again. We only move forward.

# Light Rays : Fermat’s Principle of Least Time

In this section, we take a detour to discuss a subject in physics that is so familiar to all of us - **geometric optics**. Here, we study about how light rays travel. Although light is technically a quantum mess of a wave-particle, whenever the dimensions of the objects involved are much larger than its wavelength, and when the energies involved are much larger than the quanta of energy, we can approximate light to be travelling in a one-dimensional path called a **ray**. Hence this domain of optics where we ignore the wave nature and quantum nature of light is also called **ray optics**. The following are the three popular laws of ray optics that all have studied in their school days :

1.  **Law of Rectilinear Propagation** : In a homogeneous (uniform)
    medium, a ray of light travels in a straight line with constant
    speed.

2.  **Law of Reflection** : When a ray of light encounters a medium
    through which it can neither travel nor get absorbed into (such
    media are called mirrors), then something happens at the boundary
    wherein the ray bounces back. In this context, that the angle made
    by the light ray with the normal to the boundary (**angle of
    incidence**) is equal to the angle made by the bounced-off light ray
    with the normal to the boundary (**angle of reflection**).

    [](https://substackcdn.com/image/fetch/$s_!v_tY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8940315f-a411-40a5-9db5-979f43a308c7_766x410.heic)
    ![](https://substackcdn.com/image/fetch/$s_!v_tY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8940315f-a411-40a5-9db5-979f43a308c7_766x410.heic)

**Law of Refraction** : When a ray of light suddenly encounters another medium (through which it can travel), it bends at the boundary separating the two media. This process is called refraction and the angles made by the rays with the normal to the boundaries (separating the media) obeys a precise law which is called **Snell’s law** given by :  

\\\frac{\sin \theta_i}{\sin \theta_r} = \frac{c_i}{c_r}\\

  
where c_i and c_r are the speed of light in the incident medium and refracted medium respectively.

[](https://substackcdn.com/image/fetch/$s_!BU9O!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F78cacd6a-cb02-4cdf-a0a9-bf66f9e03c33_778x542.heic)

![](https://substackcdn.com/image/fetch/$s_!BU9O!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F78cacd6a-cb02-4cdf-a0a9-bf66f9e03c33_778x542.heic)

Till here is very familiar ground for anyone from middle school. These laws themselves are not obvious (especially Snell’s law) and are summaries of lots of observations and experiments. For example, the ancient Greeks merely had look up tables for some of the angles of incidence and the angles of refraction between air and water. The 16th century physicist **Snell** observed that the ratio of the sines of the angles of incidence and refraction is constant between a pair of media. It was much later when it was possible to measure the speed of light that this constant was found to be the ratio of the speeds of light in both the media.

But it turns out that there is a single elegant principle that summarises all these three laws into one. Feynman says something about this in his lectures on physics.

Now in the further development of science, we want more than just a formula. First we have an observation, then we have numbers that we measure, then we have a law which summarizes all the numbers. But the real *glory* of science is that *we can find a way of thinking* such that the law is *evident*. The first way of thinking that made the law about the behaviour of light evident was discovered by Fermat in about 1650, and it is called *the **principle of least time***, or ***Fermat’s principle***.

Fermat’s Principle is summarised as follows :

> **Out of all possible paths that it might take to get from one point
> to another, a light ray takes the path which requires the**
> ***shortest time of travel*****.**

Does this remind you of the office guy or Rama who wants to get to a place in the shortest possible time ! Turns out light rays also are solving the same problem through these three laws. Let us first verify that this Fermat’s principle of least time is consistent with the three laws we told above.

When the speed of light is constant in a homogeneous medium, then minimising distance is same as minimising time since speed is distance divided by time and hence if speed is constant, distance travelled is proportional to time taken. So, the law of rectilinear propagation is obvious from the principle of least time because the path of shortest distance connecting any two points is a straight line and in homogeneous medium where speed of light is constant, minimising time is same as minimising distance. Let us now do it for the other two laws where the connection is non trivial.

### Putting out a fire and the law of reflection

Imagine that you are standing at a point A and then you observe that your house at point B is on fire.

[](https://substackcdn.com/image/fetch/$s_!Hgnd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F422a1e29-4a59-4762-ba5e-a4d8f51de771_2464x1728.heic)

![](https://substackcdn.com/image/fetch/$s_!Hgnd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F422a1e29-4a59-4762-ba5e-a4d8f51de771_2464x1728.heic)

Now imagine there is a river that flows straight along the line joining M and M’. Now, you obviously want to reach from A to your house B in the shortest time but you cannot simply travel on the straight line connecting A to B. This is because you want to put out the fire and you need water for that. So, the problem is that given a constant maximum speed that you can run, you have to reach from A to B in the shortest time with the constraint that you have to pass through the line MM’. Let us say you first pass through the point C from A in the line MM’ to collect water and then rush back to your house from C to B. C can technically be anywhere but what Fermat’s principle of least time is saying is that for the total time taken to be minimum, angle ACD should be equal to angle BCF (this is same as saying angle of incidence is equal to angle of reflection). This path is shown in violet in the picture. If we choose to meet the river at others points like D or E, Fermat’s principle tells us that it will take a longer total time.

Once again, since the speed is constant, minimum time is same as minimum distance. To prove that the distance AC + CB is the least among all other combinations (like AD + DB or AE + EB), we do a simple high school level geometric construction. Construct on the other side of the mirror MM′ an artificial point B′, which is the same perpendicular distance below the plane MM′ as the point B is above the plane (BF = FB’). Then we draw the line EB′. Now because BFM is a right angle and BF=FB′, EB is equal to EB′. Therefore the sum of the two distances, AE+EB, which is proportional to the time it will take if the light travels with constant velocity, is also the sum of the two lengths AE+EB′. Therefore the problem becomes, when is the sum of these two lengths the least? The answer is easy: when the line goes through point C as a *straight line* from A to B′! In other words, we have to find the point where we go toward the artificial poin B’ in a straight line, and that will be the correct one!!.

Now if ACB′ is that path of least distance such that ACB’ is a straight line, then angle BCF is equal to angle B′CF and then to angle ACM. Thus the statement that the angle of incidence equals the angle of reflection is equivalent to the statement that the light goes to the mirror in such a way that it comes back to the point B in the *least possible time*. Originally, the statement was made by **Heron of Alexandria** that the light travels in such a way that it goes to the mirror and to the other point in the shortest possible *distance*, so it is not exactly a modern theory. It was this that inspired Fermat to suggest to himself that perhaps refraction also operated on a similar basis. But for refraction, light obviously does not use the path of shortest *distance*, so Fermat tried the idea that it takes the shortest *time* as the speed of light in the two media are obviously different.

### The drowning child, the lifeguard, and Snell’s Law

To illustrate that the best thing to do is not just to go in a straight line, let us imagine that a beautiful girl in a lake has fallen out of a boat and is screaming for help in the water at point B. The x-axis is the shoreline separating land and water. A lifeguard is at point A on land, and he sees the accident, and he can run and can also swim. But he can run faster than he can swim. What does he do? Does he go in a straight line connecting A and B? That would not be a wise approach here as by using a little more intelligence, he would realise that it would be advantageous to travel a little greater distance on land in order to decrease the distance in the water, because he goes much slower in the water. Fermat show us that the final solution to the problem is the path ACB that obeys Snell’s law such that the sines of the angles of incidence (ACN) and refraction (BCN’) with the normal NN’ is same as the ratio of the speeds in air and water respectively. If the Snell’s law path is indeed the path of least time, this means that if we take any other path, the time will be longer.

[](https://substackcdn.com/image/fetch/$s_!CkNL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6712eea7-c525-4b9b-a081-0cd36dc33479_2496x1696.heic)

![](https://substackcdn.com/image/fetch/$s_!CkNL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6712eea7-c525-4b9b-a081-0cd36dc33479_2496x1696.heic)

Now, the total time taken from A to B depends on where C is. If C is shifted to the left or right slightly, the time taken also continuously shift continuously. The ratio between the change of the function (total time) to the change of its argument (location of C) is nothing but the derivative or its slope which you must have learnt in high school calculus. Now we also learnt in calculus that when we are at a minimum, the slope or the first order rate of change of the function is zero.

[](https://substackcdn.com/image/fetch/$s_!e6RN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc8be2b06-7cfe-486e-a65d-ebdaeca9e5da_724x464.heic)

![](https://substackcdn.com/image/fetch/$s_!e6RN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc8be2b06-7cfe-486e-a65d-ebdaeca9e5da_724x464.heic)

That is, if C is the point in the x-axis of minimum time, then if we slightly shift the location of C to another point X, there should infinitesimally be no change upto first order in the total time taken. That means, upto first order, the amount on time gained on one medium should be exactly cancelled by the amount of time lost on another medium upto first order.

So our way of finding the law will be to consider that we move the place C by a very small amount to X, and demand that there be essentially no change in time. (Of course there is an infinitesimal change of a *second* order; we ought to have a positive increase for displacements in either direction from C.) So we consider a nearby point X and we calculate how long it would take to go from A to B by the two paths, and compare the new path with the old path. It is very easy to do. We want the difference, of course, to be nearly zero upto first order, if the distance XC is short.

First, look at the path on land. If we draw a perpendicular XE to AC, we see that this path on land is shortened by the amount XC. But upto first order, XC ≈ EC. Let us say we gain by not having to go that extra distance. On the other hand, in the water, by drawing a corresponding perpendicular, CF to CB, we find that we have to go the extra distance XC in water, and that is what we lose. But upto first order, XC ≈ XF.

So, in time, upto first order, we gain the time it would have taken to go the distance EC, but we lose the time it would have taken to go the distance XF. Those times must be equal since, in the first approximation, there is to be no change in time. But supposing that in the air, the speed is n times as fast as in water, then we must have

\\EC = n . XF\\

Therefore we see that when we have the right point,

\\XC \sin\angle{EXC} = n . XC. \sin\angle{XCF}\\

Cancelling the common hypotenuse length XC, we get

\\ \sin\angle{EXC} = n . \sin\angle{XCF}\\

But from the geometry of the problem (think about high school geometry and properties of right angled triangles), angle EXC = angle NCA = angle of incidence and angle XCF = angle N’CB = angle of refraction and hence we have

\\\sin \theta_i = n \sin \theta_r\\

which is Snell’s law.

Thus, we see that the ray of light is moving in order to optimise something - the time of travel between two points ! So, like our Rama at crossroads, our light ray also wants to travel in a path such that it takes least time to go given the different speeds at different media.

### Design of Optical Devices & Fermat’s Principle

I just want to touch upon few important applications of optical instrument design that you might have come across in high school (and mostly hated it and found them tough and boring) but they now become very transparent and obvious once you understand Fermat’s principle. Suppose we wish to arrange some mirrors so that all the light from source P always goes to P′. So, we must ensure that all rays of light from P end up at P’ and nowhere else.

[](https://substackcdn.com/image/fetch/$s_!p9Dj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7e3c0608-f5e9-4353-b1b2-fb02dd702219_412x286.heic)

![](https://substackcdn.com/image/fetch/$s_!p9Dj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7e3c0608-f5e9-4353-b1b2-fb02dd702219_412x286.heic)

By principle of least time, it must mean that a light ray on any path, whenever it goes to hit the mirror and come back, all times must be equal. Why? Let us prove by contradiction.

> Let us take two points A and B on the focusing mirror such that all
> light rays from P after reflection from the mirror, pass through P’.
> Take two points on the mirro A and B which gives two paths for the
> light ray to travel - they are : the P→A→P’ path or the P→B→P’ path.
> My claim is that for any two points A and B, the total time on both
> the paths must be the same. Why?
>
> Assume for the contrary that they are not the same and one of the
> times (say in P→A→P’) is higher than the other time (say in P→B→P’).
> By Fermat’s principle of least time that the light ray travels only on
> those paths that take least time, it can definitely not travel on the
> path P→A→P’ as the time taken on it is higher than another path
> (P→B→P). But some light ray from P will hit A and hence there will
> always be a light ray PA. So, since the path P→A→P’ is forbidden, it
> must mean that the light ray PA after reflection, cannot travel on the
> path AP’. So, it must travel along some other line segment. But if it
> travels by some other line segment, it will not reach P’ ! But we
> assumed that all light rays from P come to P’ after reflection which
> is now contradicted! Hence the contrary proposition must not be true.

Consider the total time taken to go from P to a P’. Here the light always travels in air, so the time and the distance are proportional. Therefore the statement that all the total times from P to P’ are the same is the same as the statement that the total distance (distance from P to the point on the mirror and from the point on the mirror to P’) is the same for all points on the mirror (A or B or anything). Thus, in the figure, the sum of the two distances r1 and r2 in the figure must be a constant for all points on the mirror. We know from mathematics that ***ellipse*** is that curve which has the property that the sum of the distances from two points (called its foci) is a constant for every point on the ellipse; thus we can be sure that the light from one focus will come to the other when we design an elliptic mirror with foci at P and P’. Indeed, ellipsoidal mirrors are used in all applications where it is required to focus all of light from one point to another point.

[](https://substackcdn.com/image/fetch/$s_!NW4D!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F169bc9ba-f913-4759-ad34-03f64029d1b0_257x196.jpeg)

![Ellipsoidal Mirrors](https://substackcdn.com/image/fetch/$s_!NW4D!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F169bc9ba-f913-4759-ad34-03f64029d1b0_257x196.jpeg "Ellipsoidal Mirrors")

Now let us say that the source of light is very very far (e.g. the sun or a distant star) and hence all rays from it become parallel. To hence focus sunlight, we need to ensure that all rays parallel in a certain direction (called the principal axis of a mirror) must pass through a certain point P’ (called the **principal focus**) after reflection. Let us assume that the direction of parallel rays is vertical by moving the y-axis on that direction and let KK’ be the plane perpendicular to the vertical direction (xz plane).

[](https://substackcdn.com/image/fetch/$s_!oLS0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F75cbc8d0-026f-4a01-ad8d-ac8ead83304a_908x590.heic)

![](https://substackcdn.com/image/fetch/$s_!oLS0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F75cbc8d0-026f-4a01-ad8d-ac8ead83304a_908x590.heic)

So, by the same logic for the ellipse, we want a mirror such that the sum of the distances from any point on the mirror to the line KK’ and to the point P’ must be constant. We know from mathematics again that the ***parabola*** is that curve which satisfied the property that the sum of distances to a point and a line is constant across all points on it. The particular point is called the ***focus*** of the parabola and the particular line is called the ***latus rectum*** of the parabola. So, in order to focus parallel light rays, we have to design a **paraboloidal mirror** with its latus rectum perpendicular to the direction of parallel rays and its focus being the desired point where we want to focus our light to. Note that to focus all parallel rays in a given direction, the parabola has to be infinitely long and keep going extended but practically, it is not possible and hence a finite paraboloidal mirror can focus only some of those parallel rays (this problem does not arise for an ellipse because an ellipse is a bounded curve).

Even today, solar cells and telescopes collecting starlight are placed at the focus of a paraboloidal focusing mirrors. The picture of a parabolic reflector is shown below.

[](https://substackcdn.com/image/fetch/$s_!iZYU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F03d97e99-95ae-4568-bbd0-3b9abc2c29d0_259x194.jpeg)

![Parabolic reflector - Wikipedia](https://substackcdn.com/image/fetch/$s_!iZYU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F03d97e99-95ae-4568-bbd0-3b9abc2c29d0_259x194.jpeg "Parabolic reflector - Wikipedia")

The **Palomar observatory** in California that has several telescopes to observe distant astronomical objects have paraboloidal focusing mirrors to focus their starlight of interest.

Let us now see some applications of refraction. One example is the **mirage** that one often sees while driving on hot roads. One sees “water” on the road, but when he gets there, it is as dry as desert! What is really happening is that the sky light is “reflected” on the road: light from the sky, heading for the road, can end up in the eye, as shown in the picture below. Why?

[](https://substackcdn.com/image/fetch/$s_!dCP5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F51a627d0-e4ca-4cd1-b207-ee692f8e8d70_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!dCP5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F51a627d0-e4ca-4cd1-b207-ee692f8e8d70_2816x1536.heic)

The air is very hot just above the road but it is cooler up higher. Hotter air is more expanded than cooler air and is thinner, and this decreases the speed of light less. That is to say, light goes faster in the hot region than in the cool region. Therefore, instead of the light from the sky deciding to come to your eyes in the straightforward way, it also now has a least-time path by which it goes into the hotter region near the road where it goes faster for a while, in order to save time. So, it can go in a curve.

Now let us come back to the initial problem of focusing all rays from a given point P to another point P’. We used mirrors for focusing and now let us ask what would be the case if we use a refracting medium (called a lens) to focus from P to P’ by refraction instead of reflection. As we saw for mirrors, the only way that the light can be perfectly satisfied to take several adjacent paths from P to P’ is to make all those travel times along all such paths from P to P’ through the lens *exactly equal!* See the picture below.

[](https://substackcdn.com/image/fetch/$s_!SZ1R!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2dc206cc-f6e9-46dd-84a1-9f8cec5ac588_922x450.heic)

![](https://substackcdn.com/image/fetch/$s_!SZ1R!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2dc206cc-f6e9-46dd-84a1-9f8cec5ac588_922x450.heic)

Now consider a ray which goes in air in the path PQP′. That is a longer path than from P directly to P′ and no doubt takes a longer time. But if we were to insert a piece of glass of just the right thickness in the middle, even though the path P→R→R’→P’ is shorter than P→Q→P’ , a glass of right thickness might exactly compensate the lower length by reducing the speed in the area R→R’ such that it would take the light the exact same time along P→R→R’→P as P→Q→P ! Also, as R approaches closer to the line PP’, the path length P→R→R’→P keeps getting shorter and shorter and hence the glass thickness should get larger and larger to slow it down even more so that the time is exactly equal to that of P→Q→P’. So, such a lens should bulge as it goes from Q to the line PP’. But once we cross the line PP’ and R goes above the line PP’, the path lengths P→R→R’→P again starts increasing and hence we need to reduce the thickness of the glass to make the time equal and by symmetry, the shape of the lens below PP’ should be the same as above PP’. If the thickness of the glass is exactly rightly chosen as a function of vertical position, then we can arrange that the time the light takes to go straight from P to P’ is the same as the time it takes to go in the path PQP′, and along all other intermediate paths P→R→R’→P. We then end up with a piece of glass that looks like the figure above. With this shape, all the light which comes from P will go to P′. This, of course, is well known to us, and we call such a device a **converging lens**. The same can be asked for focusing all parallel rays (of a certain direction) to a point P’ and we can ask what shape they should be. The exact shape of such a perfectly focusing lenses can be determined but they turn out to be a fourth degree algebraic curve (unlike ellipses and parabolae which are conics and hence of second degree) and are also hence difficult to design. So, as an approximation, converging lenses are designed spherically in shape so that the two surfaces at the boundaries of the glass medium are parts of spheres. When the radius of the sphere is carefully chosen and the position of the lenses are placed appropriately, we get what the desired focusing effect at least for rays close to the centre.

But the focusing using spherical lenses is not exact (as the sphere is only an approximation for the fourth degree exact focusing surface) and the term for errors resulting from them is called as **spherical aberration** as the sphere is only an approximation to the actual complex focusing surface. Another kind of aberration is the **chromatic aberration** because the speed of light in a medium depends on its colour (wavelength). So, a lens designed to focus one colour even if exactly, will not exactly focus rays of other wavelengths. Studying and remedying all these problems is the focus of optical instrument design. I just hope that I have whetted your appetite enough for you to explore more or that you will at least appreciate how elegant Fermat’s principle is in explaining many diverse phenomena and solving many design problems simply and elegantly.

# From Discrete Agents to Continuum Optics

The discrete world of finding the path of least time in a road network and the problem of light ray travelling along a continuous ray following the path of least time are not that disjoint (as it would appear so in the first place). The entire point of this article is to show that they are exactly parallel. For that, let us know first how to translate between the discrete world of grids, lines, and iterations to the continuum of space and time.

[](https://substackcdn.com/image/fetch/$s_!qYOA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2d591e7a-59dc-4584-b381-53129f5318cc_1881x1528.jpeg)

![](https://substackcdn.com/image/fetch/$s_!qYOA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2d591e7a-59dc-4584-b381-53129f5318cc_1881x1528.jpeg)

On the left side of the visual above (the coarse grid), any movement is a series of discrete “Manhattan” steps as would be in a well planned city : you can only go strictly right/left or strictly up/down along the bolded edges. To move diagonally, you are forced to “staircase”—go right, then up, then right, then up. You can’t curve. This is the **Discrete World**. It is rigid. You are always at a specific “address” (intersection), and you make distinct choices at discrete moments. Now, imagine we shrink those grid squares as the length of each square tends to zero. As the grid lines get closer together, the “steps” of the staircase become microscopic. The jaggedness of paths begin to blur and while the paths still follows the lines, but to the naked eye from afar, it starts to look like a smooth curve as in the right part of the figure.

So, we can think of light as following the path of least time in our usual city network only like Rama but just that the network is made of grids and the grid size is getting very very finer such that the number of allowed intersections is getting larger and larger while the size of each allowed road is getting smaller and smaller. So, Fermat’s principle and the city problem deal with the exact situation once we are able to think back and forth between the grid world and the continuum world.

# How does a Light Ray Know?

This is one of the deepest philosophical questions in physics that bothers everyone when they first encounter Fermat’s Principle. If you throw a stone, it flies in a parabola because at every instant, gravity accelerates it down in a particular direction *at that very same instant* ; and when does that every instant and see the big picture , the overall shape of its trajectory turns out to be a parabola. The stone did not plan that it would move in a parabola ; the parabola was just an emergent property of local and instantaneous cause and effects. But **Fermat’s Principle** sounds completely different. It says light chooses a path to minimise the *total* *time* to a destination it hasn't even reached yet! Consider the classic setup of refraction when light travels from Point A (in Air) to Point B (in water). To get there fastest, we know that it shouldn’t go in a straight line but that It should travel longer in the air (where it’s fast) and shorter in the water (where it’s slow). The light ray bends exactly at the air-water interface to satisfy this. It seems to know *exactly* where to bend, as the light seemingly needs to know where Point B is beforehand. It looks like the light is **teleological** (driven by a future goal) rather than **mechanistic** (driven by past causes).

How can a photon “sniff out” all possible paths, calculate the path length for each, possible path, and then choose the best one before it even leaves the source? Does the light ray have a map? Does it have a brain? The answer again lies in **Bellman’s Principle of Optimality**. Recall what it says:

> **“An optimal policy has the property that whatever the initial state
> and decisions are, the remaining decisions must constitute an optimal
> policy with regard to the state resulting from the first decision.”**

In plain English: **You don’t need to see the finish line to run the perfect race. You just need to make the perfect move** ***right now*** **from where you are standing.** It turns out that “Global Intelligence” for additive costs (planning ahead) is mathematically identical to “Local Blindness” (acting optimally right now based on the value function).

> *The light ray is **not** calculating the future. It is simply obeying
> a local rule* (using Bellman’s Equality) *that happens to be a global
> solution.*

Computers use the Dijkstra’s algorithm that systematically expands from the source node to progressively find nodes in the order of increasing value function and make them violet. When we approximate what light does by considering a fine discretisation, what does the local physics that moves the light look like as it propagates from a source ? Turns out, it is the same old Dijkstra’s algorithm that expands from the source and progressively violet-ifies the space !!!

> **Nature is simply running Dijkstra’s algorithm on space-time with
> infinite resolution for propagating light !!**

This is one of those topics that sits exactly at the boundary where computer science algorithms transform into fundamental physics. Turns out that the continuum version of Dijkstra’s algorithm that physics uses in nature, was invented centuries before Dijkstra by a Dutch physicist Christian Huygens and is called the **Huygens’ principl**e !! Huygens' principle is essentially the "operating system" that nature uses to run Dijkstra's algorithm continuously in the real world.

Let us now illustrate our exact discrete world scenario. Let us divide space into intersections of grids and time into discrete units and run Dijsktra’s algorithm to minimise total time of the grid journey from a lifeguard to drowning girl. Turns out in doing so, you have simulated the propagation of light !!! Let us begin slowly.

[](https://substackcdn.com/image/fetch/$s_!0zbN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F23e40628-77db-40c5-8e3b-dadc5b640ae9_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!0zbN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F23e40628-77db-40c5-8e3b-dadc5b640ae9_2816x1536.heic)

What about the edges of this grid world? Consider that every node (intersection) has 16 neighbours shown below (we choose 16 instead of 4 or 8 directions so that continuous trajectories can be better approximated). The 16 nearest intersections in the grid are considered immediate edges of our grid world.

[](https://substackcdn.com/image/fetch/$s_!9oBi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F37582bca-f8a6-40c5-b0f9-6b3adef62488_724x752.heic)

![](https://substackcdn.com/image/fetch/$s_!9oBi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F37582bca-f8a6-40c5-b0f9-6b3adef62488_724x752.heic)

The cost associated with each edge is its distance divided by the speed of light in the medium where the vertex is in. So if light travels faster, the cost is lower in the grid. Now, consider the case where there is air at the top and a denser medium at the bottom and that the speed of light in air is 3 times faster than in the medium. Now, we will simulate Dijkstra’s algorithm on this scenario. The curves in white are where the cost-to-go is constant (their values are given on the curve only). After expanding through the violet propagation and calculating the cost-to-go at all concerned nodes, the final lowest cost path taken (least time path) taken by an agent in the discrete world from the source to the target is shown below. Note that at the bottom medium, even moving a short distance increases the cost by an amount that is changed in the top medium by travelling a larger distance. Note the final shape of the agent almost resembles the one expected by Snell’s law.

[](https://substackcdn.com/image/fetch/$s_!kntO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F81f7fb24-d487-4daa-8b9b-b68af1e784fb_1448x1440.heic)

![](https://substackcdn.com/image/fetch/$s_!kntO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F81f7fb24-d487-4daa-8b9b-b68af1e784fb_1448x1440.heic)

The code for this can be found in the appendix of the article.

For other values of costs, the exact path according to Snell’s law is shown below for comparison so that you can see how discretisation has affected the behaviour.

[](https://substackcdn.com/image/fetch/$s_!t5QB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fac7d6717-707f-492e-9043-75a44dd83031_726x736.heic)

![](https://substackcdn.com/image/fetch/$s_!t5QB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fac7d6717-707f-492e-9043-75a44dd83031_726x736.heic)

Do you see that the curves of constant cost-to-go look like the circular ripples of waves when you throw a pebble on a pond? I told that the violet-ification of nodes in Dijsktra’s algorithm resembled a wave propagation except that instead of the wavefront ripples being equidistant from the source point (circles in a pond) , Dijkstra violets are having same cost-to-go from the source (equi-source).

What does the Huygens’ principle exactly say?

> Huygens’ Principle : **Every point on a wavefront acts as a source of
> new, expanding spherical wavelets (secondary waves) that travel at the
> same speed as the original wave**; the new wavefront at any later time
> is the common tangent (or envelope) to these wavelets,

[](https://substackcdn.com/image/fetch/$s_!70kA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F605e8a38-6265-4ff4-be6c-39ec2f6b8965_483x490.png)

![Read the passage given below and answer the following questions : Huygen's principle is the basis of wave theory of](https://substackcdn.com/image/fetch/$s_!70kA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F605e8a38-6265-4ff4-be6c-39ec2f6b8965_483x490.png "Read the passage given below and answer the following questions : Huygen's  principle is the basis of wave theory of")

This is exactly same as in Dijkstra where the wavefront is nothing but the boundary between the visited nodes and the unvisited nodes ! A systematic comparison is given below.

### Part 1: The Discrete World (Dijkstra’s Algorithm)

Imagine a map that is a perfect grid of intersections.

- **The Upper Half (Air):** Fast roads. Travel cost = 1 minute per
  block.

- **The Lower Half (Water):** Slow roads (mud). Travel cost = 2 minutes
  per block.

We start a **Violet Fire** (the “Source”) at a point in the Air. We want to find the fastest path to a point deep in the Water.

#### Step 1: The Spark (Initialization)

Dijkstra begins by marking the Start Node as **Violet** (Cost = 0).

- **Analogy:** This is the moment you turn on the light bulb.

#### Step 2: The Expansion (Checking Neighbors)

The algorithm looks at the immediate neighbors (Up, Down, Left, Right, …).

- It calculates the time to reach them.

- The “Violet Wave” expands outward in a polygonal shape.

- **Crucial Discrete Mechanism:** A node turns Violet, and then it
  “wakes up” its neighbors to calculate their potential costs.

#### Step 3: Hitting the Mud (The Boundary)

The expanding wavefront hits the boundary between Air and Water.

- **In Air:** The wave continues expanding fast (1 block per minute).

- **In Water:** The wave slows down. It takes *twice as long* to cover
  the same distance.

This causes the shape of the Violet Wavefront to **distort**. It bulges out far in the air but remains compressed in the water.

#### Step 4: Backtracking the Path

Once the wave reaches the destination, we act like a detective. We ask the destination: *“Which neighbor got you here fastest?”*

- We trace the pointers backward.

- Because the wave moved faster in the air, the optimal path is not a
  straight line. It spends **more distance in the air** (to use the
  higher speed) and cuts sharply across the water (to minimise the
  expensive distance).

- **Result:** A bent path.

------------------------------------------------------------------------

### Part 2: The Continuous World (Huygens’ Principle)

Now, shrink the grid squares until they vanish. The “Air” and “Water” are now continuous blocks of material. We switch from Dijkstra to **Huygens**.

Huygens’ Principle is the “Continuous Source Code” for how waves move. It states:

> **“Every point on a wavefront acts as the source of secondary
> spherical wavelets. The new position of the wavefront is the envelope
> of these wavelets.”**

Let’s break this down step-by-step to match Dijkstra.

#### 1. “Checking Neighbors” becomes “Secondary Wavelets”

- **Dijkstra:** A node checks its neighbors.

- **Huygens:** A point on the wavefront creates a tiny “bubble”
  (wavelet) of light around itself.

- **Why?** This bubble represents the “reach” of the light in the next
  infinitesimal instant of time. It is the continuous equivalent of
  checking the “edges” connected to a node.

#### 2. “Edge Weights” become “Wavelet Size”

- **Dijkstra:** If the edge weight is high (slow), the “cost” increases
  quickly, effectively “shortening” the reach for a given time budget.

- **Huygens:** If the medium is slow (Water), the radius of the tiny
  wavelet is **small**. If the medium is fast (Air), the radius is
  **large**.

- **Visual:** In the air, the bubbles are big. In the water, the bubbles
  are tiny.

#### 3. “Updating the Wavefront” becomes “The Envelope”

- **Dijkstra:** The new “Frontier” is the set of best nodes we just
  found.

- **Huygens:** The new wavefront is the line that connects the edges of
  all those tiny bubbles.

#### 4. The Bending (Refraction)

This is where the magic happens. Imagine the wavefront is a long line of soldiers marching forward, holding hands.

- The soldiers on the left (Air) are marching fast (Big bubbles).

- The soldiers on the right (Water) are marching slow (Small bubbles).

Because the left side moves faster than the right side, the entire line **pivots**. The wavefront bends. Since the “Ray of Light” (the path) is always perpendicular to the wavefront, the ray bends too.

> This is Fermat’s Principle. The light didn’t “calculate” the bending.
> The bending happened automatically because the “Dijkstra Wavefront”
> lagged behind in the slow zone.

Finally, why is the light ray perpendicular to the wavefront? This means that the path followed by an agent is perpendicular to the curve at which the cost (time) is constant. This is again a consequence of Bellman inequality. The shortest path between two parallel straight lines is the line connecting them perpendicularly. Similarly, the path of least time between two parallel wavefronts is perpendicular to their tangents. But if you want a more mathematical derivation, refer the book I recommend in the next section.

[](https://substackcdn.com/image/fetch/$s_!r4Cf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb8e425b2-a2b0-4e69-9594-018419daf9f7_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!r4Cf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb8e425b2-a2b0-4e69-9594-018419daf9f7_2816x1536.heic)

# The Principle of Least Action :  All of Newton’s Mechanics is Dijkstra

Now I will introduce you to a topic that excited Richard Feynman the most. He writes about this as follows :

When I was in high school, my physics teacher—whose name was Mr. Bader—called me down one day after physics class and said, : “You look bored; I want to tell you something interesting”. Then, he told me something which I found absolutely fascinating, and have, since then, always found fascinating. Every time the subject comes up, I work on it. In fact, when I began to prepare this lecture I found myself making more analyses on the thing. Instead of worrying about the lecture, I got involved in a new problem. The subject is this—**the principle of least action.**

In geometric optics, we saw that how Fermat’s principle tells us the motion of light rays in all circumstances can be summed up by the maxim that light rays take the path of least time. It turns out that all of Newtonian physics also can be summarised by a similar maxim that any particle moves in such a way that it minimises something !! This is what is the principle of least action. Let us continue with Feynman for a while.

Mr. Bader told me the following: Suppose you have a particle (in a gravitational field, for instance) which starts somewhere and moves to some other point by free motion—you throw it, and it goes up and comes down. It goes from the original place to the final place in a certain amount of time. Now, you try a different motion. Suppose that to get from here to there, it went as shown in some other imaginary path, but got there in just the same amount of time. Then he said this: If you calculate the kinetic energy at every moment on the path, take away (subtract) the potential energy, and integrate it over the time during the whole path, you’ll find that the number you’ll get is *bigger* than that for the actual motion

In other words, the laws of Newton ( “F=ma” ) could be stated in the equivalent form:

> The total kinetic energy minus the average potential energy over time
> is as little as possible for the path of an object going from one
> point-velocity pair to another.

Let the difference between kinetic and potential energy be L. Then, we have that :

The following cost S is minimised :

\\S = \int\_{t_0}^{t_f} \bigg (\frac{1}{2}m\left\\v\right\\^2 - U(x) \bigg) dt := \int\_{t_0}^{t_f} L \space dt\\

That is, between two points and two velocities and two times, the actual path of the particle (that obeys Newton’s laws and the initial and final positions and velocities) turns out to be the one for which the above integral cost is the least. This total cost S is also called action and hence this principle is called the **Principle of Least Action** !

This is now another kind of Fermat principle that summarises all of Newtonian mechanics instead of optics !! The only difference is that the space is not just space-time but also the space of velocities as we have the cost depending on the velocity as well (which means that initial and final velocity are considered an independent variable as well apart from initial and final points that are positions).

> The principle of least action also is valid for a multi-particle
> system in which case it is operating in the very high dimensional
> space whose coordinates are the positions and velocities of all
> particles together!! So, nature seems to be running Dijkstra’s
> algorithm in extremely high dimensions (think of all the particles of
> the universe!!) with infinite resolution !!

I will not go into the details of deriving Newton’s law

\\m \ddot{x} = \text{Force} = -\nabla V(x)\\

as the minimising solution of the action integral. (It will be too heavy if you don’t already know it. And if the math is not heavy for you, you would most probably know it already!!).

But, you do realise that this is something really freaking ! As Feynman said :

The actual motion (of a particle under some potential energy) is some kind of a curve——and gives a certain value for the action integral S. But we could *imagine* some other motion … in some peculiar way. We can calculate the kinetic energy minus the potential energy and integrate for such a path … or for any other path we want. The miracle is that the true path (that obeys Newton’s laws) is the one for which that integral is least.

[](https://substackcdn.com/image/fetch/$s_!FO1e!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F37fd6961-4b53-4df3-bb5f-ce8e248c4e85_2816x1536.heic)

![](https://substackcdn.com/image/fetch/$s_!FO1e!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F37fd6961-4b53-4df3-bb5f-ce8e248c4e85_2816x1536.heic)

Again philosophically, Newton’s law is local and causal. But the principle of least time is teleological and intelligent ! Seeing the inspiration from optics, you may be tempted to ask two questions.

> 1.  **Is Newton’s law a continuous version of the Dijkstra’s algorithm
>     for continuum space-velocity-time?**
>
> 2.  **If light rays that obey principle of least time are really
>     waves** with the wavefront telling about the evolution of the
>     increasing surfaces of constant cost-to-go values, then **is every
>     particle obeying Newton’s laws too a kind of wave** (of very low
>     wavelength as we don’t see the wave effects in everyday life) with
>     the Newtonian trajectory of the particle being the ray
>     corresponding to the perpendicular to the wavefront of a sort of
>     wave?

The answer to the first question turns out to be yes and the continuum version of the Bellman equation corresponding to the action S in Newtonian mechanics turns out to be a very famous equation in classical mechanics called simply as the **Hamilton-Jacobi Equation** (instead of the generic continuous version which is confusingly called as the **Hamilton-Jacobi-Bellman (HJB)** Equation). The answer to the second question is also a resounding yes - if light rays following least time are actually waves, then are particles obeying least action (that is equivalent to Newton’s laws) too waves fundamentally? Yes, yes, yes and if you indeed follow the math based on this thought process to wherever it takes you logically, all it takes is a little more inspiration to derive the **Schrödinger Wave Equation** in Quantum mechanics which says that all particles are actually waves (remember **de Broglie**??!!!!) If you are very interested in these topics and can handle the math and physics, I recommend you this amazing book :

[](https://substackcdn.com/image/fetch/$s_!hkDl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F09ab621b-1135-429e-adff-595283827916_662x1020.heic)

![](https://substackcdn.com/image/fetch/$s_!hkDl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F09ab621b-1135-429e-adff-595283827916_662x1020.heic)

# Codes

Python Code for Dijkstra illustrating Huygens

    import numpy as np
    import matplotlib.pyplot as plt
    import heapq

    def simulate_optical_dijkstra(res=1000, n1=1.0, n2=3.0):
        # 1. Setup the High-Res Grid
        height, width = res, res
        # Top = Fast (n=1.0), Bottom = Slow (n=3.0)
        weights = np.ones((height, width)) * n1
        interface_y = height // 2
        weights[interface_y:, :] = n2

        start = (int(height * 0.1), int(width * 0.1))
        target = (int(height * 0.9), int(width * 0.9))

        # 2. Dijkstra with 16-neighbor connectivity (to ensure circular wavelets)
        distances = np.full((height, width), np.inf)
        distances[start] = 0
        pq = [(0, start)]
        parent = {}

        # Define 16-neighbor moves: 8 standard + 8 'Knight' moves
        # This approximates a circular wavefront much better than 4 or 8 neighbors
        moves = []
        for dy in range(-2, 3):
            for dx in range(-2, 3):
                if dy == 0 and dx == 0: continue
                moves.append((dy, dx, np.sqrt(dy**2 + dx**2)))

        print("Propagating wavefronts (This may take a moment for 1000x1000)...")
        while pq:
            d, (y, x) = heapq.heappop(pq)
            if d > distances[y, x]: continue
            if (y, x) == target: break

            for dy, dx, step_d in moves:
                ny, nx = y + dy, x + dx
                if 0 <= ny < height and 0 <= nx < width:
                    # Cost = Physical distance * refractive index
                    cost = step_d * weights[ny, nx]
                    if d + cost < distances[ny, nx]:
                        distances[ny, nx] = d + cost
                        parent[(ny, nx)] = (y, x)
                        heapq.heappush(pq, (distances[ny, nx], (ny, nx)))

        # 3. Path Reconstruction (The Fermat Ray)
        path_y, path_x = [], []
        curr = target
        while curr in parent:
            path_y.append(curr[0]); path_x.append(curr[1])
            curr = parent[curr]

        # 4. Visualization
        plt.figure(figsize=(12, 12))
        # Time Field (Phase)
        plt.imshow(distances, cmap='inferno', origin='upper')
        
        # Wavefronts (Huygens Principle - Constant Cost)
        levels = np.linspace(0, np.max(distances[distances != np.inf]), 40)
        contours = plt.contour(distances, levels=levels, colors='white', linewidths=0.5, alpha=0.6)
        plt.clabel(contours, inline=True, fontsize=8, fmt='%1.0f')

        # The Ray (Fermat's Path) - Should be straight and then BEND
        plt.plot(path_x, path_y, color='cyan', linewidth=3, label="Light Ray (Refracted)")
        plt.axhline(interface_y, color='red', linestyle='--', label="Interface")
        
        plt.title(f"1000x1000 Dijkstra: Huygens Wavefronts & Fermat Ray (n1={n1}, n2={n2})")
        plt.legend()
        plt.show()

    simulate_optical_dijkstra()

13

3

3

Share
