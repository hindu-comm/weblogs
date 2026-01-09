+++
title = "An Indian King, The Boon"
full_title = "An Indian King, The Boon of High Dimensional Garages & Natural Language Processing"
upstream_url = "https://ramaseshanchandrasekaran.substack.com/p/an-indian-king-high-dimensional-garages"
date = "2026-01-01"
+++
Source: [here](https://ramaseshanchandrasekaran.substack.com/p/an-indian-king-high-dimensional-garages).

An Indian King, The Boon of High Dimensional Garages & Natural Language Processing

# An Indian King, The Boon of High Dimensional Garages & Natural Language Processing

### In this article, I prove the result that the number of approximately orthogonal vectors increases exponentially with the dimension of the space and how it matters for natural language processing.

[](https://substack.com/@ramaseshanc)

![Rama Seshan Chandrasekaran's avatar](https://substackcdn.com/image/fetch/$s_!ZHOm!,w_36,h_36,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11e50d60-b811-4831-8bbc-4d320762e60b_96x96.png)

[Rama Seshan Chandrasekaran](https://substack.com/@ramaseshanc)

Dec 24, 2025

15

4

5

Share

**Note** : This article assumes you know basic linear algebra and probability theory - more precisely, you must know what a dot product is, and also some properties of the Gaussian probability distribution.

**Also Note** : I could have written this proof deliberately more precisely using very complex notation and exactness but since I want to emphasise intuition over rigour, I have done some handwaving in my arguments here and there. So, mathematical purists beware.

[](https://substackcdn.com/image/fetch/$s_!cKJl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd3286831-7c73-474a-9c73-380e8b835125_1498x1068.jpeg)

![Hello Word Cloud Different Languages World Stock Illustration 453116998 \|
Shutterstock](https://substackcdn.com/image/fetch/$s_!cKJl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd3286831-7c73-474a-9c73-380e8b835125_1498x1068.jpeg "Hello Word Cloud Different Languages World Stock Illustration 453116998 |  Shutterstock")

# Exact & Approximate Orthogonality : An Interesting Perspective

In two dimensions, there are two independent perpendicular directions possible. In three dimensions, there are three independent perpendicular directions possible. If we want to place a fourth vector in 3D, we can't place it independently of the other three vectors.

[](https://substackcdn.com/image/fetch/$s_!s10K!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd44a0418-0f20-458b-825f-c789514cd765_331x152.png)

![7.1. Orthogonal complements — Linear algebra](https://substackcdn.com/image/fetch/$s_!s10K!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd44a0418-0f20-458b-825f-c789514cd765_331x152.png "7.1. Orthogonal complements — Linear algebra")

We all know from basic linear algebra that in N-dimensions, there are utmost N independent perpendicular directions possible. In fact, this is what it technically means for a vector space to be N-dimensional ! We also know that given two vectors in N-dimensional space where each vector has N coordinates, we also know that the dot product between the two vectors is given by

\\x . y = (x_1,x_2,\ldots,x_N) . (y_1,y_2,\ldots,y_N) = \sum\_{i=1}^N x_i y_i = \left\\ x\right\\ \left\\ y\right\\\cos\theta\_{x,y}\\

From this, we can find the cosine of the angle between two vectors “x” and “y” as

\\\cos \theta\_{x,y} = \frac{x.y}{\left\\ x \right\\ \left\\ y \right\\ }\\

We can hence see that this cosine lies between -1 and 1. The magnitude of this cosine is zero if the vectors are perpendicular and approaches unity as the vectors are more similar or opposite in direction. Hence, this cosine between two vectors is also called as the **cosine similarity**.

So what we have seen so far can be summarised as

> In a N-dimensional space, there are utmost N vectors such that the
> cosine similarity between any two distinct pairs of those vectors is
> exactly zero.

Upto this is all intuitive and okay. But what if we give up on exact perpendicularity and are okay with every pairs of vectors being approximately perpendicular to each other. Instead of 0, if we choose a small number **ε**\>0**,** and then demand to choose a bunch of vectors so that the magnitude of the cosine similarity between all these pairs of vectors is less than this **ε** (instead of being exactly zero as in the case for exact orthogonality). In other words, we are asking :

\\v_1,v_2,v_3,....v\_{how-many?} \Longrightarrow \|\cos\theta\_{i,j}\|
\leq \epsilon\\

Turns out that for every **ε**\>0 degree of approximation, this number of approximately orthogonal vectors that we can choose that are all mutually approximately orthogonal to each other is proportional to the exponential of N !

> **While the maximum possible number of vectors exactly orthogonal to
> each other increases linearly with the number of dimensions N** (in
> fact it is exactly equal to N), **the maximum possible number of
> vectors that are approximately orthogonal to each other increases
> exponentially with N**

## Step 1 :  Calculating the Probability of Approximately Orthogonal Pairs of Vectors

First, let us generate two random independent directions in the N dimensional space. What is the probability of this pair of vectors is approximately orthogonal of **ε** degree? Let us first calculate this.

How do I generate two random independent directions such that each direction is equally likely to be generated as the other? Let us consider the Gaussian probability density function (PDF) in N-dimensions with mean 0 and variance 1 which is described by

\\p(x_1,x_2,x_3,\ldots,x_N) = \frac{1}{2\pi^{\frac{N}{2}}}e^{-\frac{1}{2}\left\\x\right\\^2}\\

Note that this PDF in N-dimensions depends only the magnitude of “x” (distance from origin) and hence it is equally likely to generate vectors in any direction since if two vectors share the same distance from origin, their probability densities are exactly the same.

Another thing to note about this PDF which you might have learnt in a basic course on probability is that this multivariate Gaussian PDF is a product of N independent 1-dimensional PDFs each with mean 0 and variance 1. Expanding

\\\left\\x\right\\^2 = x_1^2 + x_2^2 + x_3^2 + \ldots + x_N^2 \\

and hence

\\e^{-\frac{\left\\x\right\\^2}{2}} = e^{\frac{-x_1^2 -x_2^2 - x_3^2 - \ldots - x_N^2}{2} } = e^{-\frac{x_1^2}{2}}.e^{-\frac{x_2^2}{2}}.e^{-\frac{x_3^2}{2}}\ldots e^{-\frac{x_N^2}{2}}\\

gives us that

\\p(x_1,x_2,x_3,\ldots,x_N) = \frac{1}{2\pi^{\frac{N}{2}}}e^{-\frac{1}{2}\left\\x\right\\^2} = \prod\_{i=1}^N \bigg(\frac{1}{\sqrt{2\pi}}e^{-\frac{1}{2}x_i^2}\bigg)\\

Hence, this multivariate PDF is simply generated by collecting each coordinate separately from a single variable Gaussian density with mean 0 and variance 1 as the multivariate probability density neatly decomposes as a product of N univariate probability densities for each coordinate x_i.

Now, if we generate two random vectors from this N-dimensional zero mean and unit variance Gaussian PDF, then directions corresponding to the pairs are truly random. Now, due to the symmetry of the Gaussian PDF, we can rotate the coordinate axes such that the first randomly generated point is on the x1 axis and we can choose the units of length such that it has length unity. Thus, the first randomly generated point can be assumed as (1, 0, 0, …. 0) without loss of generality. So, let the second randomly generated vector be v = (v1, v2, v3, …. , vN).

Now, the cosine similarity C between the two randomly generated pairs of vectors e_1 = (1, 0, 0, …. 0) and v = (v1, v2, v3, …. , vN) is given as

\\C = \frac{e_1.v}{\left\\e_1\right\\.\left\\v\right\\}= \frac{v_1}{\sqrt{v_1^2+v_2^2+\ldots+v_N^2}} = \frac{v_1}{\left\\v\right\\}\\

To understand the probability density of the cosine C that lies between
-1 and 1, we need to understand the distributions of the numerator v_1 and denominator \|\|v\|\|. We know that the first coordinate v_1 is simply a univariate Gaussian with mean 0 and variance 1 which is plotted below.

[](https://substackcdn.com/image/fetch/$s_!5AbK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F64cf21c3-8b42-4a0f-b58a-fbbf6308864e_2533x1689.jpeg)

![Image of ](https://substackcdn.com/image/fetch/$s_!5AbK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F64cf21c3-8b42-4a0f-b58a-fbbf6308864e_2533x1689.jpeg "Image of ")

What about the denominator \|\|v\|\| ? Given a multivariate Gaussian, what is the distribution of its norm? Let us first calculate the mean (E) and variance.

Mean of \|\|v\|\| :

Let us first calculate the expected square length of v.

\\E(\left\\v\right\\^2) = \sum\_{i=1}^N E(v_i^2) = \sum\_{i=1}^N var(v_i) = \sum\_{i=1}^N (1) = N\\

So, then what is the mean of the length is the square root of the above quantity? The formula is not that easy. It is given by the messy expression

\\E(\left\\ v\right\\) = \sqrt{2}\frac{\Gamma(\frac{N+1}{2})}{\Gamma(\frac{N}{2})}\\

The Gamma function is a generalisation of the factorial function. But what is true is that as N becomes large, this expression becomes very simple which is

\\E(\left\\ v\right\\) \approx \sqrt{N}\\

You can verify this numerically. The following is the python code for that.

    import numpy as np
    import matplotlib.pyplot as plt
    from scipy.special import gamma

    def verify_norm_concentration(max_n=50, trials=2000):
        n_values = range(1, max_n + 1)
        
        exact_means = []
        asymptotic_means = []
        sample_means = []
        
        print(f"Simulating up to dimension N={max_n} with {trials} trials each...")
        
        for N in n_values:
            # 1. Asymptotic Approximation: sqrt(N)
            # Note: A slightly better approximation is sqrt(N - 0.5), but we use sqrt(N) 
            # to test the user's specific query.
            asymptotic = np.sqrt(N)
            asymptotic_means.append(asymptotic)
            
            # 2. Exact Theoretical Mean (using Gamma functions)
            # Formula: sqrt(2) * Gamma((N+1)/2) / Gamma(N/2)
            exact = np.sqrt(2) * gamma((N + 1) / 2) / gamma(N / 2)
            exact_means.append(exact)
            
            # 3. Empirical Simulation
            # Generate 'trials' vectors of dimension N
            vectors = np.random.randn(trials, N)
            # Calculate lengths (Euclidean norms)
            lengths = np.linalg.norm(vectors, axis=1)
            # Take the average length
            sample_mean = np.mean(lengths)
            sample_means.append(sample_mean)

        # --- Plotting ---
        plt.figure(figsize=(12, 6))
        
        # Plot 1: Comparison of Means
        plt.subplot(1, 2, 1)
        plt.plot(n_values, asymptotic_means, 'r--', label='Asymptotic ($\sqrt{N}$)', linewidth=2)
        plt.plot(n_values, exact_means, 'k-', label='Exact (Gamma function)', linewidth=2.5, alpha=0.6)
        plt.plot(n_values, sample_means, 'bo', label='Sample Mean (Simulation)', markersize=4, alpha=0.5)
        plt.title('Expected Length of Gaussian Vector vs N')
        plt.xlabel('Dimension N')
        plt.ylabel('Expected Length $E[\|v\|]$')
        plt.legend()
        plt.grid(True, alpha=0.3)
        
        # Plot 2: The Relative Error
        # Shows how quickly the difference between Exact and Sqrt(N) vanishes
        plt.subplot(1, 2, 2)
        relative_error = 100 * (np.array(asymptotic_means) - np.array(exact_means)) / np.array(exact_means)
        plt.plot(n_values, relative_error, 'g-', linewidth=2)
        plt.title('Relative Error: $\sqrt{N}$ vs Exact Mean')
        plt.xlabel('Dimension N')
        plt.ylabel('% Overestimation by $\sqrt{N}$')
        plt.grid(True, alpha=0.3)
        
        plt.tight_layout()
        plt.show()

    # Run the verification
    verify_norm_concentration(max_n=50)

The result is as follows :

[](https://substackcdn.com/image/fetch/$s_!NMHJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F855ac4b0-b64a-48dc-897f-77e7264f6133_1452x756.heic)

![](https://substackcdn.com/image/fetch/$s_!NMHJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F855ac4b0-b64a-48dc-897f-77e7264f6133_1452x756.heic)

Next, having got the mean of the length of the vector \|\|v\|\| as square root of N, by the **law of large numbers**, as N becomes very large, the probability of the value of the average of N IID RVs (independent identically distributed random variables) drifting away from their mean reduces to 0. This result is a mathematical generalisation of the intuition that when you toss an unbiased coin twice, the fraction of times you get heads drifts erratically but when you toss the coin 10,000 times, you can be almost sure that you get half of them heads and half tails. So, as N increases, the quantity \|\|v\|\|
is tightly wrapped around √N.

So, for large N, the cosine similarity C is basically for all practical purposes, given by

\\C = \frac{v_1}{\left\\v\right\\} \approx \frac{v_1}{\sqrt{N}}\\

Now, let us calculate the probability that the cosine similarity exceeds **ε** which means that the pair of vectors are not approximately orthogonal to each other (due to the greater than sign of \|C\|).

\\P(\|C\|\geq\epsilon) = P( \|v_1\|\geq \epsilon \sqrt{N})\\

Now we know that since v_1 is a Gaussian random variable with zero mean and variance 1, the probability that its absolute value exceeds any number R \> 0 becomes small as R increases (look at the rapidly decaying tail of the above graph in blue). Formally, we can prove that

\\ P( \|v_1\|\geq \epsilon \sqrt{N}) = P(\|C\|\geq\epsilon) \leq 2e^{-\frac{N\epsilon^2}{2}}\\

Now, for two vectors to be approximately orthogonal, we want the cosine similarity between them to be less than **ε**. So, the probability of \|C\|≥**ε** is actually the probability of the vectors not being approximately orthogonal to each other.

What we observe is that the probability of two random vectors not being approximately orthogonal is upper bounded by a term that exponentially falls to zero with N for any **ε** !

I am attaching a python code below that verifies this inequality numerically.

    import numpy as np
    import matplotlib.pyplot as plt

    def simulate_cosine_concentration(epsilon, n_values, trials=10000):
        """
        Simulates the probability that |cosine_similarity| > epsilon
        for random vectors in R^N as N increases.
        """
        probabilities = []

        print(f"Simulating for epsilon = {epsilon}...")
        
        for N in n_values:
            # METHOD: The Gaussian Trick
            # 1. Generate random vectors from Standard Normal Distribution
            # We generate 'trials' number of vector pairs (u, v) at once for speed
            u = np.random.randn(trials, N)
            v = np.random.randn(trials, N)
            
            # 2. Compute dot product (numerator)
            # Sum over the N dimensions (axis 1)
            dot_product = np.sum(u * v, axis=1)
            
            # 3. Compute norms (denominator)
            norm_u = np.linalg.norm(u, axis=1)
            norm_v = np.linalg.norm(v, axis=1)
            
            # 4. Calculate Cosine Similarity
            # cos_theta = (u . v) / (|u| * |v|)
            cosine_sim = dot_product / (norm_u * norm_v)
            
            # 5. Count how many have absolute value > epsilon
            count_outliers = np.sum(np.abs(cosine_sim) > epsilon)
            prob = count_outliers / trials
            
            probabilities.append(prob)

        return probabilities

    # --- Configuration ---
    epsilon = 0.2  # The threshold for "similarity"
    n_values = range(10, 300, 10) # Dimensions from 10 to 300
    trials = 5000  # Number of random pairs per dimension

    # --- Run Simulation ---
    probs = simulate_cosine_concentration(epsilon, n_values, trials)

    # --- Theoretical Bound (Chernoff) for comparison ---
    # Bound: 2 * exp(-N * epsilon^2 / 2)
    theoretical_bound = [2 * np.exp(-n * epsilon**2 / 2) for n in n_values]

    # --- Plotting ---
    plt.figure(figsize=(10, 6))

    # Plot Simulation
    plt.plot(n_values, probs, 'o-', label=f'Simulation (Trials={trials})', linewidth=2)

    # Plot Theoretical Bound
    plt.plot(n_values, theoretical_bound, 'r--', label='Theoretical Bound ($2e^{-N\epsilon^2/2}$)')

    plt.title(f'Probability of |Cosine Similarity| > {epsilon} vs Dimension N', fontsize=14)
    plt.xlabel('Dimension (N)', fontsize=12)
    plt.ylabel('Probability', fontsize=12)
    plt.grid(True, which='both', linestyle='--', alpha=0.7)
    plt.legend()

    plt.show()

The result of this code is the graph below with **ε = 0.2** :

[](https://substackcdn.com/image/fetch/$s_!01WQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F087c00ff-cacd-44de-984b-f19c00eb2a25_1754x1108.heic)

![](https://substackcdn.com/image/fetch/$s_!01WQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F087c00ff-cacd-44de-984b-f19c00eb2a25_1754x1108.heic)

## Step 2 :  Number of Approximately Orthogonal Vectors is Exponential

Now, instead of two randomly generated vectors from N dimensional space, consider now that we generate “K” independent random vectors from N dimensional space! The number of distinct pairs among K items is

\\\binom{K}{2} =\frac{K(K-1)}{2} = \frac{K^2-K}{2}\\

Imagine a system made of serially connected “m” engineering modules 1 =\> 2 =\> … =\> m. For the system to work, all of the modules have to work but for the system to fail, it is enough even if one fails. Let the probability of the module “i” failing be the number P_i. So, how do we calculate the probability of the system failing (which is same as saying that atleasty one of the modules fail)? A naive approach would be to add the probabilities of failure of each module which is the sum of all the P_i. But this is not true because this assumes that the modules do not interact and are made of fully different independent components. In real life, these systems can be coupled and have common components and correlations. Hence, it turns out that this sum indeed not equal to the probability of failure but indeed upper bounds the probability of the failure of the system. This result is called as **Boole’s Inequality** in probability. Let A_i denote the event of the failure of the module “i” failing. Then, we have :

\\P(\text{system failure}) = P(A_1\cup A_2 \cup \ldots \cup A_m) \leq \sum\_{i=1}^m P(A_i)\\

------------------------------------------------------------------------

If you are still not convinced, consider this scenario : Let us assume that an exam has two components (say, written and oral) and you have to pass both the components to succeed and clear it, but failing in even one component makes you fail. So, for failing, you need to fail at least in one of the two components. If I want to calculate the number of people who failed the exam as a whole, a naive approach would be to add the number of people who failed in the first component and the number of people who failed in the second component. But this overcounts the actual number because there can be lot of people who failed in both the components and they got overcounted by being counted twice in the enumeration. So, I have to subtract the number of people who failed in both components and got overcounted to get the actual sum. But this actual sum is still an upper bound for the number of people failing in the exam because it involves a subtraction from the sum due to overcounting. This sum still represents the worst case scenario when there is no one who failed in both the components. So, as an upper bound, this sum is still exact. The same intuition when transferred to probability, gives Boole’s Inequality.

------------------------------------------------------------------------

Thus, if we generate K independent random vectors in N dimensional space, we want all the distinct pairs of those K vectors to be orthogonal to each other. If even one pair of those K vectors have their cosine similarity bigger than **ε**, the entire set is no longer made of mutually orthogonal vectors. Let a pair of vectors being approximately orthogonal count as success and a pair of vectors not being approximately orthogonal count as failure. For success of the overall set, we want every pair to be successful whereas for failure, it is enough if just one pair fails. Using **Boole’s inequality**, we have for the probability of failure as

\\ S\_{\epsilon,K} = P(\text{K vectors failing to be approximately orthogonal}) \leq \sum\_{\|i,j\|=\binom{K}{2}} P(\|S\_{ij}\|\geq \epsilon)\\

  
Using the above lower bound we derived in the previous section, we have

\\S\_{\epsilon,K} \leq \sum\_{\|i,j\|=\binom{K}{2}} 2e^{-\frac{N\epsilon^2}{2}} = \bigg(\frac{K^2-K}{2}\bigg) e^{-\frac{N\epsilon^2}{2}} \leq K^2e^{-\frac{N\epsilon^2}{2}}\\

Thus, we have finally have that the probability of a random set of K-vectors to not be approximately orthogonal is upper bounded as

\\S\_{\epsilon,K} \leq K^2e^{-\frac{N\epsilon^2}{2}}\\

This probability of failure increases quadratically with the number of vectors K but falls exponentially with the dimension N of the space.

Now, for us to choose K approximately orthogonal vectors in N dimensions, the probability of the failure of K set of vectors in being orthogonal is to be strictly less than 1. For example, if we are sure that

\\S\_{\epsilon,K} \leq 0.5\\

Then, we can be sure that this orthogonality failure will occur only utmost half of the time, which means that a random vector generator that generates K vectors will produce approximately orthogonal vectors at least half of the time, which is good.

But if we want to just prove the existence of a set of K orthogonal vectors, then we just need to ensure that the probability of failure is strictly less than 1 which guarantees that the probability of success is strictly greater than zero. Thus, in general, to be assured of existence of a successful tuple of K approximately orthogonal vectors, it is enough if we are assured that the probability of failure is strictly less than 1 (does not matter that it will take a large number of trials to achieve it). So, we can replace the 0.5 by 1.

\\ \text{For just existence : } S\_{\epsilon,K}\< 1 \\

This is guaranteed if we can guarantee that

\\ K^2e^{-\frac{N\epsilon^2}{2}} \< 1\\

Rearranging this, and separating K^2 we get

\\K^2 \< e^{\frac{\epsilon^2 N}{2}}\\

Taking square root, we have

\\K \< e^{\frac{\epsilon^2 N}{4}} \\

Thus, for a N-dimensional space, for any degree of approximation **ε,** we have that as long as the number K is less than a number that depends exponentially on N, there is a possibility for existence of K vectors (generating them from a Gaussian) such that they are **ε-**approximately mutually orthogonal !!

So, we have finally derived the result that we wanted !

# The Curse (or Boon) of Exponential Growth

There is a famous Indian legend about the invention of chess. The king was so delighted by the game that he offered the inventor any reward he wanted.

The inventor, a humble sage, said: *“Oh King, I am a simple man. I only ask for rice. Place one grain of rice on the first square of the chessboard. Then, place two grains on the second square, four on the third, eight on the fourth, and so on. Just keep doubling the number of grains for each of the 64 squares.”*

The King laughed, thinking the sage was a fool for asking for such a meager reward. He ordered his treasurer to pay the man immediately.

**The Trap:**

- **Square 1:** 1 grain. (2^0)

- **Square 2:** 2 grains. (2^1)

- **Square 3:** 4 grains. (2^2)

- **Square 10:** 512 grains (a small handful). (2^9)

At this point, the king was still smiling. But then they passed the halfway mark of the board.

- **Square 32:** ~4 billion grains (2^31 - about a large field’s
  harvest)

- **Square 64:** 18,446,744,073,709,551,615 grains….

This isn’t a sack of rice. This is a mountain of rice larger than Mount Everest. It is more rice than has been produced in the entire history of the human race. The King went bankrupt not because he was poor, but because he didn’t understand **exponential Growth**. Exponential growth starts slow and looks harmless. But once it hits the “knee of the curve,” it shoots up vertically, becoming effectively infinite.

[](https://substackcdn.com/image/fetch/$s_!MtU6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F04c32919-1253-41d6-81a1-e3f537d0c63c_960x640.jpeg)

![The Legend Of Rice And Chess: Exponential Growth - Pragati Rice](https://substackcdn.com/image/fetch/$s_!MtU6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F04c32919-1253-41d6-81a1-e3f537d0c63c_960x640.jpeg "The Legend Of Rice And Chess: Exponential Growth - Pragati Rice")

Now, how does this relate to our math problem about vectors and orthogonality?

In this story, the squares of the chessboard represent the dimension (N) of our space. The **number of rice grains** represents the **orthogonal** **capacity (K)**—the number of distinct, approximately orthogonal vectors we can fit in that space.

In **low dimensions** (the first few squares)**,** when we are in 1D, 2D, or 3D space (like the first few squares of the chessboard), the “room” available for orthogonal vectors is tiny. In 2D Space, you can only have **2** perpendicular vectors (X and Y). In 3D Space**,** you can only have **3** (X, Y, Z). It feels crowded. If you try to add a 4th vector, it ***must*** **overlap** with the others. There is no “space” left. But, in high dimensions **(**the second half of the Chessboard**),** as we increase N (the dimension), we are moving to the later squares of the chessboard. Just like the rice grains doubled with every square, the exponential bound that we derived (for the number of orthogonal vectors that can be accommodated) proved that the number of vectors K that we can fit without them touching scales grows exponentially with N^2. So, at N=100, we aren’t just adding room for a few more vectors. We are suddenly in a universe where we can fit millions of mutually perpendicular directions. At N=1000, we have passed the “Mount Everest” point. The space is now so vastly, mind-bogglingly huge that you could pick billions of random vectors, and the probability of any two of them pointing in the same direction is essentially zero. This is why what is normally a “curse” of exponential growth (when it comes to computing time or space) becomes a “boon” here for accommodating orthogonal vectors in a space.

If you are building a garage or a storehouse or a library (or a database), in 3D space, you only have directionally 3 distinct axes of shelves (X, Y, Z). But, in a 1,000-dimensional space, you have trillions of approximately orthogonal shelves. You can give every single narrow genre of book (or data point) its own private shelf (orthogonal direction).

> Just as the king underestimated the rice because he couldn’t visualise
> the explosion of numbers on the 64th square, we underestimate
> high-dimensional space. We think adding a dimension just adds ‘one
> more axis’ like adding a line on a graph. In reality, adding a
> dimension doubles the ‘volume’ of the universe. In 10,000 dimensions,
> space is so incredibly vast that everything is far away from
> everything else, and ‘collisions’—where two different ideas get
> confused—become mathematically impossible.”

# Application to Natural Language Processing : Low-Dimensional Embedding

What use is this ability to store lots of orthogonal directions you might ask? For computers to understand and process natural language, there are two fundamental problems about language that makes it unamenable to computation directly.

Most computers in other ML areas are designed to learn functions that are essentially numbers. Eg. Learn Y=F(X). X might be a 1000 dimensional vector and Y be a hundred dimensional vector - that is okay but both X and Y are both a set of a fixed quantity of real numbers. That is what computers are designed to handle.

Compared to other AI fields such as robotics and computer vision, language has its own quirks. Unlike images, first of all, utterances and sentences in natural languages have variable length. You can say a very short sentence (“Hello.”) or a very long one (“The mouse that the cat hit that the dog bit that the fly landed on ran away.”). Most machine learning algorithms are not good at dealing with something of variable length, and you need to come up with ways to represent languages with something more fixed.

Another characteristic of language is that it is discrete. What this means is that things in languages are separate as concepts. For example, if you take a word “rat” and change its first letter to the next one, you’ll have “sat.” In computer memory, the difference is just a single bit. However, there is no relationship between those two words except they both end with “at,” and maybe a rat can sit. There is no such thing as something that is in between “rat” and “sat.” The fact that “rat” and “sat” are close when analysed as strings, does not signify any real world closeness between the concepts of rat and sat respectively. These two are totally discrete, separate concepts that happen to have similar spelling. On the other hand, if you take an image of a car and change the value of just one pixel by a single bit, you still have a car that is almost identical to the one before this change. Maybe it has a slightly different color. In other words, images and sounds are continuous, meaning that you can make small modifications without greatly affecting what they are. Many mathematical toolkits, such as vectors, matrices, and functions, are good at dealing with something continuous.

The history of NLP is actually a history of challenging these two aspects - **variable length** and **discreteness** of language, and only recently have we begun to see some successes on this front, for example, with word embeddings.

A language text is basically a string of words. Let N be the total number of words in a language labelled and ordered as per a dictionary. A linguistic corpus which is just a bunch of words in succession. just a bunch of numbers in succession. If each word is assigned a numerical label from 1 to N, then it is just a bunch of numbers in succession.

Now, we saw that “rat” and “sat” despite being close as strings, are different things in language. Is there a way to assign a point for each word in a N dimensional space such that

- Similar words for similar concepts map to a set of points with similar
  direction

- Antonym words expressing opposite or complementary concepts map to a
  set of points with opposite directions

- Words whose concepts are unrelated and are independent map to a set of
  points that are orthogonal to each other

- More frequent words occur closer to the origin

So, what we are asking for is a visualisation of words of a language as vectors in a N dimensional space where cosine similarity captures semantic relations between words, the length captures inverse frequency, and orthogonality captures semantic independence.

But in a language, there are millions of unrelated categories of words and hence if we demanded exact orthogonality of all sets of semantically unrelated words, we would have to go for an exorbitantly high dimensional spaces. But if we settle for approximate orthogonality, then we can accommodate an exponentially high curse worthy number of unrelated independent concepts in very small dimensional spaces that run in just a few hundreds. This is what **embedding** means in natural language processing. It is the mapping of words to points in a low dimensional spaces where semantic relations are easily captured geometrically.

[](https://substackcdn.com/image/fetch/$s_!pioV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa1108865-400f-4c89-b3ed-97631f6af5a8_1146x1100.heic)

![](https://substackcdn.com/image/fetch/$s_!pioV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa1108865-400f-4c89-b3ed-97631f6af5a8_1146x1100.heic)

Now, using this technique, every word of a natural language becomes a point in a reasonably low dimensional space (embedding). So, since the dimension of the embedding is low and fixed, this solves the variable length problem. Since semantic dependence and independence translate as geometric orthogonal dependence and independence (and frequency with length), the problem of continuity is solved. The words “rat” and “sat” will be mapped to nearly orthogonal vectors even though as strings, they are similar. Whereas the words “cat” and “dog” would be mapped to similar vectors with very high degree of cosine similarity despite not being similar or close when analysed as strings.

Now how to learn the embedding - who sits and does this assignment of each word to a point? This relation is learnt by a neural network using appropriate training. Once this embedding is learnt, words in a language can be treated and manipulated like vectors by computers.

There are two popular methods of training neural networks to learn word embeddings from large corpuses of textual data. I will continue this in a future article where I continue to discuss aspects of NLP and other topics in machine learning.

15

4

5

Share
