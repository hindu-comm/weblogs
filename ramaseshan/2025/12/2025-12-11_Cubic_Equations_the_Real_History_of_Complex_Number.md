+++
title = "Cubic Equations & the"
full_title = "Cubic Equations & the Real History of Complex Numbers"
upstream_url = "https://ramaseshanchandrasekaran.substack.com/p/cubic-equations-and-the-real-history"
date = "2025-12-11"
+++
Source: [here](https://ramaseshanchandrasekaran.substack.com/p/cubic-equations-and-the-real-history).

Cubic Equations & the Real History of Complex Numbers 

# Cubic Equations & the Real History of Complex Numbers

### We have all been told that imaginary numbers were invented to solve quadratic equations with negative squares but the real history is far from the truth and has to do with cubic equations !!!

[](https://substack.com/@ramaseshanc)

![Rama Seshan Chandrasekaran's avatar](https://substackcdn.com/image/fetch/$s_!ZHOm!,w_36,h_36,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11e50d60-b811-4831-8bbc-4d320762e60b_96x96.png)

[Rama Seshan Chandrasekaran](https://substack.com/@ramaseshanc)

Nov 01, 2025

7

1

Share

[](https://substackcdn.com/image/fetch/$s_!_7aC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd0ffe351-b12c-4250-bffb-999dae443115_250x250.jpeg)

![Picture](https://substackcdn.com/image/fetch/$s_!_7aC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd0ffe351-b12c-4250-bffb-999dae443115_250x250.jpeg "Picture")

# Quadratic Equations with No Roots

I was in grade 11 when my mathematics teacher told me the following story. The following quadratic equation

\\x^2+1=0\\

did not have any root.

This also makes sense. If you graph this function

\\y=x^2+1\\

on a graph sheet (as shown below in red), it never touches the x-axis (as shown below in green) where y=0.

[](https://substackcdn.com/image/fetch/$s_!mlfp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F65fecfd2-6567-4cc7-9db4-384738befa6e_812x992.heic)

![](https://substackcdn.com/image/fetch/$s_!mlfp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F65fecfd2-6567-4cc7-9db4-384738befa6e_812x992.heic)

> Physically also, the square of any number cannot be negative and any
> solution to it is meaningless. Then, it absolutely makes no sense to
> invent artificial solutions to this above equation without any
> motivation. **Mathematicians are often accused for being other-worldly
> and thinking about useless stuff but they are not at fault definitely
> in this case. It turns out that complex numbers were not invented to
> solve quadratic equations with negative discriminant. Turns out these
> imaginary and complex numbers were invented for a pretty real purpose
> !!** Imaginary numbers were invented for actually solving cubic
> equations!

# Quadratic Equations

Before heading to the case of the cubic equations, let us first recap the technique of solving the quadratic equation of the generic form

\\f(x) = x^2+bx+c=0\\

Now, in school we learnt a trick called completing the square. Here, we see that since

\\x^2 + bx = \bigg(x+\frac{b}{2}\bigg)^2 - \frac{b^2}{4}\\

substituting

\\x+\frac{b}{2} = y\\

reduces the original quadratic equation to

\\y^2 + \bigg(c-\frac{b^2}{4}\bigg) = 0\\

In terms of y, the coefficient of the linear term vanishes and this enables solving for y to be easy in terms of a direct square root as

\\y=\pm \sqrt{ \frac{b^2}{4}-c }\\

which gives the famous quadratic formula

\\x=-\frac{b}{2}\pm \sqrt{ \frac{b^2}{4}-c }\\

If u, v are the two roots of the quadratic equation, by adding and multiplying them, we get

\\u + v = -b\\

\\uv = c\\

Together, these u and v solve the quadratic equation

\\x^2+bx+c=0\\

# Cubic Equations : Cardano’s formula

[](https://substackcdn.com/image/fetch/$s_!MUAV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F36ce464f-bbb7-4b20-a695-ea5d1851fe98_1280x1649.jpeg)

![undefined](https://substackcdn.com/image/fetch/$s_!MUAV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F36ce464f-bbb7-4b20-a695-ea5d1851fe98_1280x1649.jpeg "undefined")

Consider a generic cubic equation with the coefficient of the cubic term normalised to unity and hence with the following form

\\f(x) = x^3+ax^2+bx+c=0\\

Now, this cubic equation (unlike the quadratic case) always has to have at least one real solution for any choice of the coefficients a,b,c. This is because as x becomes very large, the cubic term in f(x) dominates and hence the value of f(x) tends to +∞ . As x becomes very small in the negative direction, due to the same reason, the value of f(x) tends to -∞ . Or in more precise terms, we have

\\\lim\_{x\rightarrow \infty} f(x) = \infty, (and) \lim\_{x\rightarrow
-\infty} f(x) = -\infty\\

And hence, f(x) has to cross zero in between at least once as any continuous function that changes sign must pass through zero at least once.

**Note** : *In the remainder of this entire section, we are going to derive the formulae for the solution to the cubic equation above. If you are not interested in little mental workouts, you may safely skip the section and proceed to the formula for x at the very end of this section and accept it as a matter of faith, without losing any flow in reading.*

Now, how do we solve the generic cubic equation in the beginning of this section? We complete the square to solve quadratic equations. Let us complete the cube and see what happens.

Making the following substitution

\\x+\frac{a}{3}=y\\

we see that the equation becomes (after little bit of playing around patiently)

\\y^3 + py + q=0\\

where

\\p=\frac{-a^2+3b}{3}\\

\\q = \frac{2a^3-9ab+27c}{27}\\

So, we see that we have reduced a cubic equation in x to a cubic equation in y except that this time, the coefficient of the square term is zero. If your brain is lazy to do this arithmetic, then assume for a moment that someone gave a cubic equation in the variable y with no square term. Now, completing the cube is not enough, unlike in the case of quadratic equations where completing the square gave a direct solution. How do we solve the following equation?

\\y^3 + py + q=0\\

Now, trying out this out-of-the-hat magic substitution (don’t ask me why, it simply works!)

\\y=\sqrt\[3\]{u}+\sqrt\[3\]{v}\\

Cubing both sides, we get

\\y^3=u+v+3\sqrt\[3\]{u}\sqrt\[3\]{v}(\sqrt\[3\]{u}+\sqrt\[3\]{v})\\

Putting this in the cubic equation for y, we get

\\u+v+3\sqrt\[3\]{u}\sqrt\[3\]{v}(\sqrt\[3\]{u}+\sqrt\[3\]{v}) + p(\sqrt\[3\]{u}+\sqrt\[3\]{v})+q=0\\

Rearranging it, we get

\\(u+v+q) + (3\sqrt\[3\]{u}\sqrt\[3\]{v}+p)(\sqrt\[3\]{u}+\sqrt\[3\]{v}) = 0\\

Now, note that y was just one independent variable that we need to solve for and u and v are two intermediate variables we assumed to split y. So, we can always consider v to be arbitrary and then determine u to be determined from the choice of v. So, if we select u and v such that

\\ 3\sqrt\[3\]{u}\sqrt\[3\]{v}+p = 0\\

Then, the cubic equation reduces to

\\u+v+q=0\\

So, the solution to the cubic equation reduces to solving two simultaneous equations in u and v which are

\\u + v = -q\\

\\uv = -\frac{p^3}{27}\\

This must remind you of the formulae of the sums and products of the roots u and v of a quadratic equation. So, these u and v must satisfy the quadratic equation

\\z^2+qz -\frac{p^3}{27}=0\\

So, this tells us that u and v are solved as

\\u,v = -\frac{q}{2}\pm \sqrt{\frac{q^2}{4}+\frac{p^3}{27}}\\

Solving for u,v using these quadratic formulae gives us y through the substitution

\\y=\sqrt\[3\]{u}+\sqrt\[3\]{v}\\

which gives x through the substitution

\\x+\frac{a}{3}=y\\

Thus, the final formula for x after putting all these substitutions is

\\x=-\frac{a}{3}+\sqrt\[3\]{ -\frac{q}{2}+ \sqrt{\frac{q^2}{4}+\frac{p^3}{27}}} + \sqrt\[3\]{
-\frac{q}{2}-\sqrt{\frac{q^2}{4}+\frac{p^3}{27}}}\\

This messy solution is called **Cardano’s formula** for the cubic equation named after an Italian Renaissance mathematician !!!!

# Something is wrong with Cardano’s formula

An old Chinese proverb says

Be careful what you wish for; you might get it !

We wished for a formula to solve for the roots of the cubic equation and we got it!! What next?

Consider a simple equation like

\\y^3-15y-4=0\\

Here, by substation, we know for sure that **y = 4** is definitely a solution!!

But Cardano found something creepy when he used his formula for the roots of the cubic equation to derive this obvious answer.

Comparing it to the standard

\\y^3+py+q=0\\

We have p=-15, q=-4, and hence putting it in the formula

\\y=+\sqrt\[3\]{ -\frac{q}{2}+ \sqrt{\frac{q^2}{4}+\frac{p^3}{27}}} + \sqrt\[3\]{ -\frac{q}{2}-\sqrt{\frac{q^2}{4}+\frac{p^3}{27}}}\\

that he discovered gives

\\x=\sqrt\[3\]{ 2+ \sqrt{4-125}} + \sqrt\[3\]{ 2-\sqrt{4-125}}\\

which upon simplification gives

\\x=\sqrt\[3\]{ 2+ \sqrt{-121}} + \sqrt\[3\]{ 2-\sqrt{-121}}\\

Did you see something above !!! Did you see a square root of a **negative** 121 in the above formula!!!! Cardano was baffled by this expression!!

# Bombelli fixes Cardano’s formula

But another Italian mathematician **Bombelli** found out that if you pretended for a moment that negative numbers had square roots, he found out that just arithmetic manipulation gives the required root y=4.

[](https://substackcdn.com/image/fetch/$s_!ZxNS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F285da5e6-5816-4aeb-af60-369a689ccb0a_405x600.gif)

![undefined](https://substackcdn.com/image/fetch/$s_!ZxNS!,w_1456,c_limit,f_auto,q_auto:good,fl_lossy/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F285da5e6-5816-4aeb-af60-369a689ccb0a_405x600.gif "undefined")

Assuming the two square roots of -1 as **+i** and **-i** and manipulating them like any other numbers with the same arithmetic rules, we get

\\\pm \sqrt{-121} = \pm \sqrt{-1\times 121} = \pm 11i\\

Substituting it in Cardano’s expression, we have

\\x=\sqrt\[3\]{ 2+ 11i} + \sqrt\[3\]{ 2-11i}\\

Now, by doing the following arithmetic, we have

\\(2\pm i)^3 = 8 \mp i \pm 12i -6 = 2 \pm 11i !!!\\

Hence, we have!!!

\\\sqrt\[3\]{2\pm 11i}= 2\pm i\\

Substituting this in Cardano’s formula, Bombelli got

\\x=\sqrt\[3\]{ 2+ 11i} + \sqrt\[3\]{ 2-11i} = (2+i)+(2-i) = 4 \\

finally x=4, the expected answer!!

This was a revolution!! The problem was real and the final answer was real and the arithmetic carried out worked the same as real arithmetic but for Cardano’s formula to be valid, one had to take a detour to imaginary square roots of negative numbers !! Thus, these square roots of negative numbers while imaginary could be useful for real problems !! Bombelli expressed scepticism as to whether such expressions like square roots of negative numbers had any meaning (although it seemed to be working in giving real answers) but later mathematicians like **Albert Girard** argued that such expressions should be considered valid as formal expressions and should be included for the certitude of the general rules (making the formula work). At this time, even negative numbers were not that much widely accepted in Europe, let alone their imaginary square roots and hence Girard was way ahead of his time!

Now these complex numbers involving “i” are used in all sorts of real applications ranging from studying oscillators in engineering to being present in the very heart of the fundamental law of quantum mechanics which is the Schrodinger equation (see below the first number on the left - the imaginary square root of negative one at one of the most fundamental frameworks in describing nature !

[](https://substackcdn.com/image/fetch/$s_!GjWU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5ef96023-f9a6-4787-beb4-bc03de73f6a8_1354x258.heic)

![](https://substackcdn.com/image/fetch/$s_!GjWU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5ef96023-f9a6-4787-beb4-bc03de73f6a8_1354x258.heic)

7

1

Share
