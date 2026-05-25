+++
title = "Introduction to"
full_title = "Introduction to Differential Equations & Control with the Aerothrust Pendulum Part 1 Stability"
upstream_url = "https://ramaseshanchandrasekaran.substack.com/p/introduction-to-differential-equations"
date = "2026-05-01"
+++
Source: [here](https://ramaseshanchandrasekaran.substack.com/p/introduction-to-differential-equations).

Introduction to Differential Equations & Control with the Aerothrust Pendulum : Part 1 - Stability

# Introduction to Differential Equations & Control with the Aerothrust Pendulum : Part 1 - Stability

### In this series of four articles, I explain the basics of differential equation and control theory (especially the mathematics behind it) by taking the simple example of an aerothrust pendulum

[](https://substack.com/@ramaseshanc)

![Rama Seshan Chandrasekaran's avatar](https://substackcdn.com/image/fetch/$s_!ZHOm!,w_36,h_36,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11e50d60-b811-4831-8bbc-4d320762e60b_96x96.png)

[Rama Seshan Chandrasekaran](https://substack.com/@ramaseshanc)

Mar 30, 2026

13

3

Share

Have you always been scared of differential equations? Did you feel so lost in your signals and systems or control systems class in your engineering and want to know what it actually meant? The following are the notes that I prepared as an undergraduate for conducing a workshop to teach control theory through a simple setup called the aerothrust pendulum. This is the first of a four part series of articles on differential equations, dynamical systems, and control theory.

------------------------------------------------------------------------

# Systems Theoretic View of the World

Hi everyone. Dynamics is one of the most or personally my most interesting branch of physics and engineering. Here we are going to learn how to control the aerothrust pendulum system. It looks like this :

[](https://substackcdn.com/image/fetch/$s_!17wE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffd010e99-265f-47cc-be29-c18e67dad757_618x452.heic)

![](https://substackcdn.com/image/fetch/$s_!17wE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffd010e99-265f-47cc-be29-c18e67dad757_618x452.heic)

This is the schematic of the aero thrust pendulum system. This can be called as a “*one-joint arm*” except that instead of being actuated by motors at the shoulder, somebody thought of a more fancier idea. They attached the motor to the tip, allowed it to rotate a propeller through air. The resulting thrust produced by the aerodynamic design of the propeller lifts the pendulum by creating a torque about its point of support. This is the bird’s eye view of the system.

So this may be viewed as the first step in creating an “**Air-Man!**”, a man whose entire body is actuated by propulsion through air! This is the shoulder of such a man. For now our ambitions are limited though. This may not be the world’s most enthralling robot but even this humble set up can teach us so many physics and mathematics whose applications scale all the way up to those complicated robots we have in the world today. Mastering as many fundamental principles and transferable skills through as simple as an example possible would be our aim now.

Robotics is a very exciting branch of engineering because it involves in creation of beings that behave like us. In this process, we learn more about ourselves and appreciate the complexity of our very own structure. Some unique characteristics of humans are as follows:

[](https://substackcdn.com/image/fetch/$s_!Ak7s!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1687e503-ea71-4ada-b6a2-88522e1b05c0_1068x552.heic)

![](https://substackcdn.com/image/fetch/$s_!Ak7s!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1687e503-ea71-4ada-b6a2-88522e1b05c0_1068x552.heic)

Each is a milestone and involves diverse area of study and research. The first function of learning comes under the broad subject of “Artificial Intelligence” and “Machine Learning”. In this course, we will be bothered about two functions of mobility and autonomous performance of a task.

The part that deals with movement is called dynamics that embraces physics. It guides us on choosing the variables of motion, identifying the forces acting on the system and forming the equations that describe how the forces affect the motion variables. The part that deals with autonomy comes under the umbrella of control theory. It deals with representation, analysis and solving equations governing any system. The last two are still frontiers. All robots these days are powered by an external source and cannot extract energy through substances from the environment. No robots also can reproduce till present.

Let us begin. We have an arm now. What would you want the arm to do autonomously? Its movement is simple though. All it can do is rotate through the support axis and change the angle 𝜃. It changes with time. In the language of mathematics, it is a function of time. It is denoted by θ(t).

What would you want a shoulder to do? The first thing it should do is, it should go to an arbitrary reference command angle as quickly as possible wherever it is initially. Mathematically, the task is

[](https://substackcdn.com/image/fetch/$s_!_p4B!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb2b84cc0-a2c7-4d0e-a4ea-0792d427fa9a_572x104.heic)

![](https://substackcdn.com/image/fetch/$s_!_p4B!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb2b84cc0-a2c7-4d0e-a4ea-0792d427fa9a_572x104.heic)

r: command angle (arbitrary, fixed, desired by user)

How would you do that? Of course trial and error works here. But that kills the physics. A brief flow of variables of the system which is decipherable by anyone is given below.

[](https://substackcdn.com/image/fetch/$s_!AbOS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F07806fdd-036d-4546-948c-958bf9a3c61e_630x242.heic)

![](https://substackcdn.com/image/fetch/$s_!AbOS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F07806fdd-036d-4546-948c-958bf9a3c61e_630x242.heic)

We now see that the voltage given to the BLDC motor is converted to the rotational speed of the propeller which generates a thrust whose moment or torque about the pendulum axis accelerates and affects the arm angle 𝜃 .So the modeling of this system involves three stages:

1\. Voltage to speed

2\. Speed to Thrust

3\. Thrust to Arm position

The first is in the realm of electro-mechanics. The second involves aerodynamics. Although they are complicated and demand immense expertise, experimentally, they are very trivial. We shall start with the last stage. This as you see now is a complicated system. In its extremely simple manner it is represented as

[](https://substackcdn.com/image/fetch/$s_!blip!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe0f8bd67-4404-4484-b3ae-8ccc231192ad_690x244.heic)

![](https://substackcdn.com/image/fetch/$s_!blip!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe0f8bd67-4404-4484-b3ae-8ccc231192ad_690x244.heic)

What we can control here is voltage. What we want to control or interested in is the arm position. So we would want a relation between the variables 𝑉(𝑡) and 𝜃(𝑡). Any system, however complicated it may be can fit into this framework.

[](https://substackcdn.com/image/fetch/$s_!LWMj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F826abff7-44c0-49cb-9af3-fb53a0615233_656x248.heic)

![](https://substackcdn.com/image/fetch/$s_!LWMj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F826abff7-44c0-49cb-9af3-fb53a0615233_656x248.heic)

“Systems theoretic view of the world” : In any system, we have three elements:

**INPUT VARIABLES**: These are the variables that can be controlled by us. Their values at any given instant of time can be chosen to arbitrary value at free will. Eg. Voltages, Forces, Inflows, Fuel injection, etc..

**OUTPUT VARIABLES**: These are the variables that are of interest to us. They want to be controlled at every instant of time. Eg. Currents, displacements, Level or concentration, rpm of wheel etc...

It would be nice if the input itself is the output. The variable we can control itself is the variable we also want to control. But this seldom happens in practice. Often this is not the case. Take the simple case of AC. The variable you want to control is temperature. But the variable which you can control is the voltage to the compressor motor. But all is not lost since you already expect that effects in compressor power also affects the temperature (which is why you have bought the air-conditioner). So, next comes

**SYSTEM MODEL**: It is a mathematical (quantitative) description that relates the functions U(t) \[the input\] and Y(t) \[the output\].

A qualitative model of the air conditioner would be “increase in compressor power would decrease the temperature of the room”. But for precise control of temperature, we need much more information than that. This is the **systems theoretic view of the world**.

The process of arriving at the quantitative relationship between the input and the output of the system is called **mathematical modeling.** This involves the physics of the system. Once we have, we know the relation between U(t) and Y(t). Hence, we can choose U(t) so as to obtain a desired profile of Y(t). Which is the control problem.

We want to illustrate how it feels like to model a system and bring out the essential features. But the aero thrust pendulum itself is a little complicated to start with. So, we shall start with a simpler system and then see how it fits for the aero thrust pendulum system. This is popular in physics and is called the mass-spring-damper system.

------------------------------------------------------------------------

# Mass - Spring -Damper System

This system is very simple but highly representative of many systems in this world. It is like this. Straight line is one of the most fundamental shapes of geometry. And any other complicated curve, can be approximated by a straight line in a small stretch. Similarly the structure of the equation that results from this system is like that. We will be able to appreciate this better when we finish.

The name of the system is descriptive of it. It contains a mass, a spring and a damper. Do not let the damper dampen your spirit!

[](https://substackcdn.com/image/fetch/$s_!KlDF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9456bb3a-d2f8-4d51-9f3e-cb9d77bf43e5_512x512.heic)

![](https://substackcdn.com/image/fetch/$s_!KlDF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9456bb3a-d2f8-4d51-9f3e-cb9d77bf43e5_512x512.heic)

The systems theoretic view of the spring block is as usual, the cute box given below.

[](https://substackcdn.com/image/fetch/$s_!c7oo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb500bce-9148-4fb7-8095-fd051b6fb97b_664x218.heic)

![](https://substackcdn.com/image/fetch/$s_!c7oo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb500bce-9148-4fb7-8095-fd051b6fb97b_664x218.heic)

According to Newton, for any mechanical system, forces are agents that effect motion. We can apply an arbitrary force to the mass at any time and that is given by f(t). The variable we are interested to control is the position of the mass x(t). We want to know the relationship between the force and the motion. Those are called the ***dynamic equations of motion***. They determine the relationship between the force (cause) and the motion (effect).

Modeling is the process of arriving at this dynamic equation using physical principles or experimentation or a combination of both.

[](https://substackcdn.com/image/fetch/$s_!JrpS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa7cab8b4-b021-4add-a925-8879116a295d_524x306.heic)

![](https://substackcdn.com/image/fetch/$s_!JrpS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa7cab8b4-b021-4add-a925-8879116a295d_524x306.heic)

What do you think should be the features of a good model?

- Should be **simple** mathematically. Obviously you would not want the
  dynamic equations of your robot to fill up this entire page. Of
  course, you would have the correct relationship but you will not get
  anywhere with it.

- Should also be **accurate** in capturing all the features of the
  actual system. The relationship in paper should hold perfectly in
  practice. Otherwise, design in paper based on the mathematical model
  would fail in practice.

[](https://substackcdn.com/image/fetch/$s_!uU2z!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7c199247-d81c-49d2-81f1-8a7ecfa5b0cd_724x510.heic)

![](https://substackcdn.com/image/fetch/$s_!uU2z!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7c199247-d81c-49d2-81f1-8a7ecfa5b0cd_724x510.heic)

Now, we need to proceed in modeling the system keeping in mind the above guideline. Ignore unnecessary complications that do not improve the accuracy to a great extent. The dynamic equations we obtain should reflect the spirit.

In mechanics, there are several routes to obtain the dynamic equation of a system. Of course all the formalisms lead to the same equation for the same system. But personal choices and ease of application for the given system biases the decision of which formalism we choose to obtain the equation. There are four formalisms of which I know about which I will briefly elucidate upon.

[](https://substackcdn.com/image/fetch/$s_!UHlY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2a52c07d-436e-4faf-af18-36494518efd5_916x866.heic)

![](https://substackcdn.com/image/fetch/$s_!UHlY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2a52c07d-436e-4faf-af18-36494518efd5_916x866.heic)

[](https://substackcdn.com/image/fetch/$s_!xzVh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd91c25bc-f7d3-4ae6-8831-2908be9e829b_952x760.heic)

![](https://substackcdn.com/image/fetch/$s_!xzVh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd91c25bc-f7d3-4ae6-8831-2908be9e829b_952x760.heic)

However, in this text since all systems are simple we use only the Newtonian formalism. It is simple.

1\. Identify all the forces acting on the body

2\. Write “Total force = mass of the body x acceleration of the body”

3\. Solve the resulting equation of motion and get position

Now what are the forces acting on the mass that is attached to the spring and the damper? Surely, the spring and the damper exert force on the block. There are several other incidental forces like aerodynamic drag, stiction, etc.. which make the treatment only little more accurate but are too complicated to account for. Hence, in the above spirit, we neglect them. We also have our input force f(t) which we can apply arbitrarily apart from all other forces that we can control and which we hope it to use in controlling the position of the block x(t). Thus, the free body diagram of the system is

[](https://substackcdn.com/image/fetch/$s_!EkL6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc32c8cd1-93e1-4cdb-96d1-e8ff5bec5ad8_856x280.heic)

![](https://substackcdn.com/image/fetch/$s_!EkL6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc32c8cd1-93e1-4cdb-96d1-e8ff5bec5ad8_856x280.heic)

The forces are sketched above. Now we need field equations for expressing spring and damping force. But we again give a reasonably approximate expression for spring and damper forces avoiding the complicated mayhem of formulating and solving the field equations. This trick is technically called “*first order Taylor series approximation*”.

First with the **spring force Fs.** Spring does not apply force to the block when it is at equilibrium. In other force

Fs = 0 when x=0 (equilibrium position)

Whenever the block is away from equilibrium the spring applies a force to bring it back to equilibrium. When block is displaced rightward from equilibrium (x\>0), the spring force points left (FS\<0). When block is leftward displaced from equilibrium (x\<0), the spring applies force right (FS\>0). In other words, Fs always points towards equilibrium. Such a spring is called restoring spring.

[](https://substackcdn.com/image/fetch/$s_!ed_P!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd3135608-2c18-4399-ba4b-eaed56dc84e6_212x156.heic)

![](https://substackcdn.com/image/fetch/$s_!ed_P!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd3135608-2c18-4399-ba4b-eaed56dc84e6_212x156.heic)

A typical sketch of the force would look like this. We also know that the spring force does not depend on factors other than ‘x’.

[](https://substackcdn.com/image/fetch/$s_!-o-y!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1f06b4fb-b2cb-428b-a0a0-701e7af9f25b_880x628.heic)

![](https://substackcdn.com/image/fetch/$s_!-o-y!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1f06b4fb-b2cb-428b-a0a0-701e7af9f25b_880x628.heic)

For small range of displacements, Fs can be approximated to a straight line and be postulated to linearly depend on ‘x’. Such a spring is called a **linear spring**. And this approximation is credited to Hooke and is called **Hooke’s Law**.

‘k’: spring constant

Next the **damper force Fb.** No matter wherever you are, the damper or friction in general, opposes you only depending on how fast you are moving. In other words, Fb depends on ‘v’ or ‘dx/dt’ at that instant. When you are moving in the right direction, damper applies a leftward force and vice versa.

[](https://substackcdn.com/image/fetch/$s_!EaSC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb31b9f05-cdd7-4499-8d73-a78348dc1734_224x420.heic)

![](https://substackcdn.com/image/fetch/$s_!EaSC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb31b9f05-cdd7-4499-8d73-a78348dc1734_224x420.heic)

The same story repeats with velocity now.

[](https://substackcdn.com/image/fetch/$s_!lh9-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F65dbbede-7c77-4dbe-aa56-53e1e1b37263_830x674.heic)

![](https://substackcdn.com/image/fetch/$s_!lh9-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F65dbbede-7c77-4dbe-aa56-53e1e1b37263_830x674.heic)

[](https://substackcdn.com/image/fetch/$s_!6GwC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a63b72e-8168-4982-9025-88a8f35f0841_578x168.heic)

![](https://substackcdn.com/image/fetch/$s_!6GwC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a63b72e-8168-4982-9025-88a8f35f0841_578x168.heic)

Thus, we now have :

[](https://substackcdn.com/image/fetch/$s_!Hu88!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c230c0c-c737-4ca8-8b28-4ad2fae337a3_670x338.heic)

![](https://substackcdn.com/image/fetch/$s_!Hu88!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c230c0c-c737-4ca8-8b28-4ad2fae337a3_670x338.heic)

Now, comes Newton and says

> Sum of all forces equals mass times acceleration

Acceleration is the derivative of velocity which itself is the derivative of displacement.

[](https://substackcdn.com/image/fetch/$s_!NeVT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F14fedb50-547a-4fa6-ab59-66e67c91f860_222x102.heic)

![](https://substackcdn.com/image/fetch/$s_!NeVT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F14fedb50-547a-4fa6-ab59-66e67c91f860_222x102.heic)

Newton’s law says

[](https://substackcdn.com/image/fetch/$s_!W75v!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faf361bf4-bfcc-4200-84d1-2639f0505e2f_420x52.heic)

![](https://substackcdn.com/image/fetch/$s_!W75v!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faf361bf4-bfcc-4200-84d1-2639f0505e2f_420x52.heic)

Thus, we have finally, the dynamic equation

[](https://substackcdn.com/image/fetch/$s_!_gvY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F02aea840-9474-4aab-b7e9-0339479c3460_1000x1078.heic)

![](https://substackcdn.com/image/fetch/$s_!_gvY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F02aea840-9474-4aab-b7e9-0339479c3460_1000x1078.heic)

------------------------------------------------------------------------

# Solving a Differential Equation

We wanted to know how the input f(t) affects the output x(t). Here, it is!! We have stumbled upon a relation! An equation relating x(t) and f(t). We have stumbled upon what is called a “**differential equation**”. Since the equation involves differentials or derivatives of a function. The physical problem of finding x(t) given f(t) now reduces to the mathematical problem of solving this beast, one hell of a differential equation. The problem now entirely boils down now to whether we can solve this differential equation or not. The differential equation also arises in many other branches of physics and science. Let us better learn to deal with it rather than running away from it. Some people say this is where the physics ends and mathematics begins. There are three generic ways to solve this (or any) differential equation.

[](https://substackcdn.com/image/fetch/$s_!A0d9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fba7c96f5-5e82-4318-a1e9-60a554501fb3_1012x1014.heic)

![](https://substackcdn.com/image/fetch/$s_!A0d9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fba7c96f5-5e82-4318-a1e9-60a554501fb3_1012x1014.heic)

Of course we will apply the extreme cleverness technique for this system. You have textbooks for the other two! Let us once again stare at the beast. And try to admire its structure.

[](https://substackcdn.com/image/fetch/$s_!oJ2i!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4f6066af-3a7b-4b78-9cec-99f094ce36f8_272x50.heic)

![](https://substackcdn.com/image/fetch/$s_!oJ2i!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4f6066af-3a7b-4b78-9cec-99f094ce36f8_272x50.heic)

Why did nature give this differential equation for the spring block system? It could have given us some nasty equation like

[](https://substackcdn.com/image/fetch/$s_!9D-b!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F61a808f6-5699-4029-a7ce-9ba06466896f_446x116.heic)

![](https://substackcdn.com/image/fetch/$s_!9D-b!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F61a808f6-5699-4029-a7ce-9ba06466896f_446x116.heic)

Sure, this equation also involves derivative of the function x(t) and the input f(t).What makes the above equation nastier than the original equation we got?

First, the equation that we have does involve derivatives of x(t). But it does not involve all derivatives. It contains only up to second derivatives of x(t) unlike the random equation that involves 76th order derivatives. In other words it is a **second order differential equation**.

What is the consequence of this? Why did nature gives us a second order differential equation for the spring block system? Remember that to solve and get x(t), we need to kind of integrate (undo the derivatives) and to nullify two derivatives, we get two arbitrary constants of integration. What do those two arbitrary constants correspond to?

Yes, you guesses right! They represent the freedom we possess in choosing the initial position and initial velocity of the block arbitrarily. Values of initial position and velocity uniquely determine these arbitrary constants of integration. So, presence of two arbitrary constants lead to a second order differential equation.

We need two and only two arbitrary constants to specify the solution x(t) for time t\>0 given f(t) for t\>0 and they are determined by x(0) and 𝑑𝑥/𝑑𝑡 (0). It is not only a freedom or luxury but it is a necessity. For a Nth order differential equation, we need exactly N arbitrary constants. If we have less than or more than N, it is a serious problem.

So freedom in choosing the initial position and velocity and nothing more (acceleration is determined by the forces) led us to a second order differential equation. That is the first structure. Having said it is a second order equation, it still does not look like a randomly written second order equation. It still has more structure. Consider this

[](https://substackcdn.com/image/fetch/$s_!iklu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F153fde77-e237-4249-9527-dec580f1cfaa_548x108.heic)

![](https://substackcdn.com/image/fetch/$s_!iklu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F153fde77-e237-4249-9527-dec580f1cfaa_548x108.heic)

This is also a second order equation. But this is definitely more nastier right? What makes our equation better? That is the structure. So again look at the above equation and our equation. What is nicer about our equation?

The functions

[](https://substackcdn.com/image/fetch/$s_!T8B0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F97b0ee43-b1c5-4901-8349-0ee258f54d9b_222x42.heic)

![](https://substackcdn.com/image/fetch/$s_!T8B0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F97b0ee43-b1c5-4901-8349-0ee258f54d9b_222x42.heic)

appear only as linear combinations in our equation! Only to the first power! No squares or cubes or cross terms or transcendental terms like log or sin or any other function. The equation says that a particular linear combination of the funcitons above, weighed by 𝑘, 𝑏, 𝑚 equals the function 𝑓(𝑡) for all ′𝑡′. That will be enormous good news. Go back to algebra. Your teacher first introduced you to solve linear equations in one variable first. Then quadratic. Then cubic. Then transcendental equations. Only in college you learnt how to solve system of linear equations. Then the general case. Solving a system of non linear equations. But the simplest case was linear equations in one variable. We are back to the same square one here. We are starting differential equations with linear differential equations of one function.

So it is good news as this leads to enormous simplification. But the fact that our differential equation is linear is not an accident. We approximated the graphs of FS and Fb with straight lines. It was some curve. It is in fact we who had “**linearized”** the equation. Let us now embrace the linearity structure with full enthusiasm. Once again looking at

[](https://substackcdn.com/image/fetch/$s_!An3Z!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6d5c9226-5b6f-4f80-a051-53624b9cfccf_246x64.heic)

![](https://substackcdn.com/image/fetch/$s_!An3Z!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6d5c9226-5b6f-4f80-a051-53624b9cfccf_246x64.heic)

We need to find some function x(t) that satisfies the above equation and the initial conditions. Let us keep looking into this equation.

### Superposition

[](https://substackcdn.com/image/fetch/$s_!2PIw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9bf30d24-b969-4f7d-b021-1009e7945013_892x866.heic)

![](https://substackcdn.com/image/fetch/$s_!2PIw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9bf30d24-b969-4f7d-b021-1009e7945013_892x866.heic)

When input adds, so the solutions! That is the beauty of a linear equation. This would not be the case if there were non-linear terms! Let the spring be a cubic spring and the equation if it had been

[](https://substackcdn.com/image/fetch/$s_!a6vb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F71eaaf3d-36e4-4bf0-b937-e05ce7c7a499_890x1062.heic)

![](https://substackcdn.com/image/fetch/$s_!a6vb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F71eaaf3d-36e4-4bf0-b937-e05ce7c7a499_890x1062.heic)

This is the beauty of linear systems and is referred to as the **superposition principle.** Next comes another property.

### Homogeneity

[](https://substackcdn.com/image/fetch/$s_!I7cm!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F53471186-0c0c-4401-aa75-549f976e256d_900x436.heic)

![](https://substackcdn.com/image/fetch/$s_!I7cm!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F53471186-0c0c-4401-aa75-549f976e256d_900x436.heic)

This beautiful structural property of linear system is called **homogeneity.**

> **Linearity = Homogeneity + Superposition**

Linearity implies that scaling and addition of inputs does not change the nature of the solution. In other words, generically,

[](https://substackcdn.com/image/fetch/$s_!EELO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff6670af0-4fde-46b0-9cef-ddbd682f62a7_900x330.heic)

![](https://substackcdn.com/image/fetch/$s_!EELO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff6670af0-4fde-46b0-9cef-ddbd682f62a7_900x330.heic)

[](https://substackcdn.com/image/fetch/$s_!EDPc!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9f11e153-c43c-426e-83b2-26534472eb3c_912x488.heic)

![](https://substackcdn.com/image/fetch/$s_!EDPc!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9f11e153-c43c-426e-83b2-26534472eb3c_912x488.heic)

Linear combination of inputs results in a linear combination of the corresponding solutions. It is straightforward to see that this is valid for not just two but an arbitrary number of inputs. The block diagram for this property is given below.

[](https://substackcdn.com/image/fetch/$s_!0UJX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9b45e463-3104-43be-85fe-564620a0b4a3_554x434.heic)

![](https://substackcdn.com/image/fetch/$s_!0UJX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9b45e463-3104-43be-85fe-564620a0b4a3_554x434.heic)

[](https://substackcdn.com/image/fetch/$s_!B4Uf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F06ff810a-54bf-4473-85fb-94107790be30_816x1280.heic)

![](https://substackcdn.com/image/fetch/$s_!B4Uf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F06ff810a-54bf-4473-85fb-94107790be30_816x1280.heic)

Thus linear systems obey superposition and homogeneity. What are its consequences? They are the basis of the entire body of linear systems theory. They enable us to get the solution without solving the equation.

### Complementary Function & Particular Integral

Now, let 𝑂(𝑡) represent a function whose value is zero always for all time ‘t’. What does this tell you? Let us now look back.

[](https://substackcdn.com/image/fetch/$s_!ZT6z!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7ed51c42-c247-43d0-b5f8-d355cac51e8f_738x210.heic)

![](https://substackcdn.com/image/fetch/$s_!ZT6z!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7ed51c42-c247-43d0-b5f8-d355cac51e8f_738x210.heic)

What happens if we add this function O(t) to any arbitrary input f(t)?We see that this does not change the problem at all. But by superposition principle, x(t) is made up of two solutions.

[](https://substackcdn.com/image/fetch/$s_!B8dn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F975c6461-bbad-4b73-8563-c2360d6a7adf_560x172.heic)

![](https://substackcdn.com/image/fetch/$s_!B8dn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F975c6461-bbad-4b73-8563-c2360d6a7adf_560x172.heic)

We see that the solution to 𝑶(𝒕) is always present, irrespective of what f(t), we apply this is always present. This cannot be cancelled. This also does not depend on the input we apply. This part always is present. This comes to us as a free gift from the system even when we do nothing. So this part of the solution is called “**Complementary function**“ ! It is always a part of the system response and is representative of the initial conditions only. This is called by different names in different branches.

[](https://substackcdn.com/image/fetch/$s_!dbdV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5f451c98-6f4d-47df-b0e5-f5071926c380_896x214.heic)

![](https://substackcdn.com/image/fetch/$s_!dbdV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5f451c98-6f4d-47df-b0e5-f5071926c380_896x214.heic)

The solution particular to the input **f(t)** we apply ; we can control this part through changing the input f(t). This is in our hands. Again it is called **particular integral** and also has so many other names.

[](https://substackcdn.com/image/fetch/$s_!jnTv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa914f902-6647-4687-a854-3ef9eb8afd92_904x218.heic)

![](https://substackcdn.com/image/fetch/$s_!jnTv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa914f902-6647-4687-a854-3ef9eb8afd92_904x218.heic)

We shall call them in short as CF and PI. So the first result in the theory of linear differential equations is

𝑥(𝑡) = 𝐶𝐹 + 𝑃𝐼

CF: Solution when there is no input (cannot be controlled by us)

PI: Can be controlled by us by changing input f(t)

CF is always present and unavoidable but cannot be controlled by us. Means, it better decay to zero as fast as possible so that the controllable PI can take over. When we cannot control something, it had better surrender and die by itself! That is the philosophy. This is also what defines the **stability** of a linear system.

[](https://substackcdn.com/image/fetch/$s_!6R1w!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F148e83d0-cae2-4075-9318-5f546675e64a_724x554.heic)

![](https://substackcdn.com/image/fetch/$s_!6R1w!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F148e83d0-cae2-4075-9318-5f546675e64a_724x554.heic)

------------------------------------------------------------------------

# Solving for the Complementary Function

So we have to find the CF and examine its stability. We expect intuitively that for the spring block system, CF is stable, because when we do not apply any force to the block and just leave it with a initial position and/or velocity, it can no way exhibit unbounded motions. We shall then establish that firmly now. Let us find CF. For that we should not bother about the input. We need to solve the equation

[](https://substackcdn.com/image/fetch/$s_!S-YO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1c749448-28d8-4730-87d1-bbed8f47a779.heic)

![](https://substackcdn.com/image/fetch/$s_!S-YO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1c749448-28d8-4730-87d1-bbed8f47a779.heic)

How do we solve this equation? Again we are just going to stare and gently play around with the equation. No brute force. There is some unknown function x(t) which is not directly revealed to us by nature. She gives us the above puzzle. Let us try to understand what nature is trying to whisper to our ears. She says that **a linear combination of derivatives of the function x(t) adds to zero at all time**. Let us take a random function and see if this is possible.

[](https://substackcdn.com/image/fetch/$s_!xoju!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6958d91d-3f75-4cc7-867c-a1f8bb71260c_970x734.heic)

![](https://substackcdn.com/image/fetch/$s_!xoju!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6958d91d-3f75-4cc7-867c-a1f8bb71260c_970x734.heic)

[](https://substackcdn.com/image/fetch/$s_!Rl33!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fda7ed6c3-5749-4a60-998a-34a0471fca70_988x302.heic)

![](https://substackcdn.com/image/fetch/$s_!Rl33!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fda7ed6c3-5749-4a60-998a-34a0471fca70_988x302.heic)

Is the above situation possible with the random function and its derivatives that is shown above? No, most certainly not right? For some particular time t0,if it happens that the combination weighed by m,b,k did add up to zero, using the same weights, the combinations at some other time ‘t1’ won’t add up to zero if the function is some random function. Unless it were very special. How special would it have to be for this miracle to happen? How should it behave under differentiation? Think a little more and proceed to the next paragraph. I hope you get the idea now. For this to happen, the first and second derivative of x(t) should look like the function x(t) itself. Again, pictures.

[](https://substackcdn.com/image/fetch/$s_!Af5O!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe24cdf84-818a-4a1b-b5b4-d96352e1c9b7_610x646.heic)

![](https://substackcdn.com/image/fetch/$s_!Af5O!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe24cdf84-818a-4a1b-b5b4-d96352e1c9b7_610x646.heic)

Now see the picture. The derivatives of x(t) look like x(t) themselves. In other words, they are proportional to the function itself. So at time let us say t=0,

[](https://substackcdn.com/image/fetch/$s_!CPWR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0a7d1c04-85c1-4d60-a2b3-91b8f64aef8d_696x142.heic)

![](https://substackcdn.com/image/fetch/$s_!CPWR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0a7d1c04-85c1-4d60-a2b3-91b8f64aef8d_696x142.heic)

In other words, **the derivatives of x(t) should be proportional to x(t) for the CF.** What function you know satisfies this property that its derivatives are proportional to itself? Of course, the exponential. So let us postulate that the function x(t) that satisfies the CF equation is

[](https://substackcdn.com/image/fetch/$s_!3VsH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3d78d73b-5775-49ea-97f4-537b28acd223_652x272.heic)

![](https://substackcdn.com/image/fetch/$s_!3VsH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3d78d73b-5775-49ea-97f4-537b28acd223_652x272.heic)

We see that the derivatives are proportional to x(t) itself. Plugging this into the CF equation, we get

[](https://substackcdn.com/image/fetch/$s_!iunr!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0a84e0e2-f898-4317-ba86-5fcb531cdb90_746x218.heic)

![](https://substackcdn.com/image/fetch/$s_!iunr!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0a84e0e2-f898-4317-ba86-5fcb531cdb90_746x218.heic)

Our guess is right provided that the constant ‘s’ satisfies the above quadratic equation. So differential equation is converted to an algebraic equation. Any quadratic equation has two roots. The above equation is called the **characteristic equation** of a linear system. It has two roots , say 𝑠1and 𝑠2.

[](https://substackcdn.com/image/fetch/$s_!wUEQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faf66dfe1-a3f6-4a00-a14a-14178de3a9d3_890x932.heic)

![](https://substackcdn.com/image/fetch/$s_!wUEQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faf66dfe1-a3f6-4a00-a14a-14178de3a9d3_890x932.heic)

Means that for the spring-block system,

[](https://substackcdn.com/image/fetch/$s_!LLOb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffd28e8bc-3768-45c1-b144-e93ff93870e2_874x155.jpeg)

![](https://substackcdn.com/image/fetch/$s_!LLOb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffd28e8bc-3768-45c1-b144-e93ff93870e2_874x155.jpeg)

Depending on the nature of m,b,k the roots may be real or complex. So we have three cases:

### Underdamped Solution

[](https://substackcdn.com/image/fetch/$s_!kmZH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb8e4a248-e7d0-47d1-ad40-cd8515765330_986x1236.heic)

![](https://substackcdn.com/image/fetch/$s_!kmZH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb8e4a248-e7d0-47d1-ad40-cd8515765330_986x1236.heic)

[](https://substackcdn.com/image/fetch/$s_!Yoix!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1adf1af5-9cc7-47d5-8b13-a7f9d61cf41a_924x1180.heic)

![](https://substackcdn.com/image/fetch/$s_!Yoix!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1adf1af5-9cc7-47d5-8b13-a7f9d61cf41a_924x1180.heic)

### Undamped Solution

[](https://substackcdn.com/image/fetch/$s_!mV5z!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F27183b46-ea36-4e11-9083-fed05a3a0857_846x1134.heic)

![](https://substackcdn.com/image/fetch/$s_!mV5z!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F27183b46-ea36-4e11-9083-fed05a3a0857_846x1134.heic)

### Critically Damped Solution

[](https://substackcdn.com/image/fetch/$s_!Qeiq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4524dc5e-05be-469c-84ac-db964650fa08_924x518.heic)

![](https://substackcdn.com/image/fetch/$s_!Qeiq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4524dc5e-05be-469c-84ac-db964650fa08_924x518.heic)

### Overdamped Solution

[](https://substackcdn.com/image/fetch/$s_!83WI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1182f461-a72e-4aa5-9b1c-09172e30028f_816x604.heic)

![](https://substackcdn.com/image/fetch/$s_!83WI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1182f461-a72e-4aa5-9b1c-09172e30028f_816x604.heic)

[](https://substackcdn.com/image/fetch/$s_!o4ti!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffe602827-39d7-4dc0-a3c5-a2f466ec5544_666x536.heic)

![](https://substackcdn.com/image/fetch/$s_!o4ti!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffe602827-39d7-4dc0-a3c5-a2f466ec5544_666x536.heic)

### Types of Damping Summarised

[](https://substackcdn.com/image/fetch/$s_!e0oP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fefe08129-a790-4704-b320-1dfbf52b3bdc_900x632.heic)

![](https://substackcdn.com/image/fetch/$s_!e0oP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fefe08129-a790-4704-b320-1dfbf52b3bdc_900x632.heic)

[](https://substackcdn.com/image/fetch/$s_!O4LL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F693f9f45-1af9-4620-842c-553b4c965b7b_1042x1152.heic)

![](https://substackcdn.com/image/fetch/$s_!O4LL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F693f9f45-1af9-4620-842c-553b4c965b7b_1042x1152.heic)

Let us now examine closely the effect of pole location on system response. Anyway the CF decays to zero in most cases (unless b is exactly zero). But we want it to decay to zero as quickly as possible so that the PI or forced response can dominate the scene. How fast it decays depends on system parameters (which here is m,b,k).

[](https://substackcdn.com/image/fetch/$s_!jQeB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7a091d3-6929-4fcc-b8c8-11b062cf5d2d_934x932.heic)

![](https://substackcdn.com/image/fetch/$s_!jQeB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7a091d3-6929-4fcc-b8c8-11b062cf5d2d_934x932.heic)

[](https://substackcdn.com/image/fetch/$s_!mCEq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa6ff02f1-ab98-4ee1-853a-b33a87577f6f_924x1168.heic)

![](https://substackcdn.com/image/fetch/$s_!mCEq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa6ff02f1-ab98-4ee1-853a-b33a87577f6f_924x1168.heic)

[](https://substackcdn.com/image/fetch/$s_!19pc!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b25bc99-65de-479f-9ce4-b6f55f2367ac_944x962.heic)

![](https://substackcdn.com/image/fetch/$s_!19pc!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b25bc99-65de-479f-9ce4-b6f55f2367ac_944x962.heic)

[](https://substackcdn.com/image/fetch/$s_!HhHl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5d620bfe-3516-4616-945b-2e30bc69f581_934x722.heic)

![](https://substackcdn.com/image/fetch/$s_!HhHl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5d620bfe-3516-4616-945b-2e30bc69f581_934x722.heic)

So now you can see and have a feel of various types of second order system responses. We see that as long as b,m,k (coefficients of the characteristic equation) are positive, the CF of a second order linear differential equation can never go unstable. This is an accident only for second order equations and not for any other higher order.

In our example, due to the particular nature of the spring block system, the coefficients of the characteristic equation (m,b,k) were all positive. But in general, there do pop up systems where one or more of these can be negative too and now the roots of the associated characteristic equation can be anywhere in the complex plane. Let us now consider the most generic case:

Consider an arbitrary second order characteristic polynomial equation

[](https://substackcdn.com/image/fetch/$s_!BE8z!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcf764493-3e8f-4b6f-8e31-1d302948c042_560x110.heic)

![](https://substackcdn.com/image/fetch/$s_!BE8z!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcf764493-3e8f-4b6f-8e31-1d302948c042_560x110.heic)

Let us discuss all the possibilities of the location of the roots:

[](https://substackcdn.com/image/fetch/$s_!SO2x!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7e82c453-c15b-4a53-a377-eb3085740006_840x964.heic)

![](https://substackcdn.com/image/fetch/$s_!SO2x!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7e82c453-c15b-4a53-a377-eb3085740006_840x964.heic)

[](https://substackcdn.com/image/fetch/$s_!P5nr!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F981ddfa7-fb79-49e2-acb0-fbb73b698116_670x764.heic)

![](https://substackcdn.com/image/fetch/$s_!P5nr!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F981ddfa7-fb79-49e2-acb0-fbb73b698116_670x764.heic)

[](https://substackcdn.com/image/fetch/$s_!lP0D!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd348bc29-192a-44f7-88bc-7cc135d222f3_908x472.heic)

![](https://substackcdn.com/image/fetch/$s_!lP0D!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd348bc29-192a-44f7-88bc-7cc135d222f3_908x472.heic)

[](https://substackcdn.com/image/fetch/$s_!YkyO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1369e88c-5d83-4429-b03a-41668b29b903_772x664.heic)

![](https://substackcdn.com/image/fetch/$s_!YkyO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1369e88c-5d83-4429-b03a-41668b29b903_772x664.heic)

[](https://substackcdn.com/image/fetch/$s_!mcEo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4eb7a303-63ab-4855-9f34-911690149b75_688x474.heic)

![](https://substackcdn.com/image/fetch/$s_!mcEo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4eb7a303-63ab-4855-9f34-911690149b75_688x474.heic)

[](https://substackcdn.com/image/fetch/$s_!ga7q!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F103877a2-6f5f-4db5-9091-99f83dfe5a6f_510x312.heic)

![](https://substackcdn.com/image/fetch/$s_!ga7q!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F103877a2-6f5f-4db5-9091-99f83dfe5a6f_510x312.heic)

[](https://substackcdn.com/image/fetch/$s_!X91t!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F992fde20-eff0-4701-b989-08c4e186f9fe_914x724.heic)

![](https://substackcdn.com/image/fetch/$s_!X91t!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F992fde20-eff0-4701-b989-08c4e186f9fe_914x724.heic)

[](https://substackcdn.com/image/fetch/$s_!TQP4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa4c736e8-deac-48c0-822d-5436b905e82b.heic)

![](https://substackcdn.com/image/fetch/$s_!TQP4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa4c736e8-deac-48c0-822d-5436b905e82b.heic)

[](https://substackcdn.com/image/fetch/$s_!YgRq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6d9ec4f5-413b-42c6-8f10-c77168cdfd5d_960x744.heic)

![](https://substackcdn.com/image/fetch/$s_!YgRq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6d9ec4f5-413b-42c6-8f10-c77168cdfd5d_960x744.heic)

[](https://substackcdn.com/image/fetch/$s_!jpJU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7f8a75e-e4ad-4d54-a7e8-f9810f280d21_932x744.heic)

![](https://substackcdn.com/image/fetch/$s_!jpJU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7f8a75e-e4ad-4d54-a7e8-f9810f280d21_932x744.heic)

[](https://substackcdn.com/image/fetch/$s_!AByu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb5f24ac-6d04-4ded-8ab1-7f7f493d9417_884x504.heic)

![](https://substackcdn.com/image/fetch/$s_!AByu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb5f24ac-6d04-4ded-8ab1-7f7f493d9417_884x504.heic)

[](https://substackcdn.com/image/fetch/$s_!Owfa!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4191c797-6d2f-4ab2-a080-e468b519d58c_788x410.heic)

![](https://substackcdn.com/image/fetch/$s_!Owfa!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4191c797-6d2f-4ab2-a080-e468b519d58c_788x410.heic)

[](https://substackcdn.com/image/fetch/$s_!8n3Z!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fda7dcf81-799d-4307-8bb0-73b5d41a2df4_942x810.heic)

![](https://substackcdn.com/image/fetch/$s_!8n3Z!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fda7dcf81-799d-4307-8bb0-73b5d41a2df4_942x810.heic)

[](https://substackcdn.com/image/fetch/$s_!TLZj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F620df62a-9e20-40ba-b2df-0fc1c9c6a7d4_756x860.heic)

![](https://substackcdn.com/image/fetch/$s_!TLZj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F620df62a-9e20-40ba-b2df-0fc1c9c6a7d4_756x860.heic)

Now, hence it should have become clear to you by now in what all cases, is the linear system of second order stable. We now give a new name to the roots of the characteristic equation.

------------------------------------------------------------------------

# Poles of a Linear System

[](https://substackcdn.com/image/fetch/$s_!7qSk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa4612239-38e4-4dfa-9599-6e9220afc85e_766x672.heic)

![](https://substackcdn.com/image/fetch/$s_!7qSk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa4612239-38e4-4dfa-9599-6e9220afc85e_766x672.heic)

But for now, assume that I am always tired of typing and saying “roots of the characteristic equation” and picked a single random word “pole” to refer to them. This should be obvious to you that

[](https://substackcdn.com/image/fetch/$s_!RHkz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2f609462-f06e-4b53-b5a3-edf6110c2541_812x748.heic)

![](https://substackcdn.com/image/fetch/$s_!RHkz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2f609462-f06e-4b53-b5a3-edf6110c2541_812x748.heic)

This is stated as a direct consequence of the analysis described above.

------------------------------------------------------------------------

# Force-Torque Equivalence

Now, you would have had enough intuition for the spring block system. Let us now proceed with the vision we started, the aero-thrust pendulum. Coming back, we have this set-up which we saw long ago!

[](https://substackcdn.com/image/fetch/$s_!tlpJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcf4ea668-87ba-4cc2-be53-9e425cc45074_422x358.heic)

![](https://substackcdn.com/image/fetch/$s_!tlpJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcf4ea668-87ba-4cc2-be53-9e425cc45074_422x358.heic)

The thrust always is produced along the direction of rotation. This is a rotational system now. We know that for rotational motion, Newtonian formalism deals with the dual quantities for rotation.

[](https://substackcdn.com/image/fetch/$s_!CxVO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5fe54de2-3966-4577-ba89-e9578b28b678_900x286.heic)

![](https://substackcdn.com/image/fetch/$s_!CxVO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5fe54de2-3966-4577-ba89-e9578b28b678_900x286.heic)

The modified Newtonian dynamic equation for rotations is

[](https://substackcdn.com/image/fetch/$s_!FU4M!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F75f40174-7828-4d3b-91e2-83b7057c2d82_810x64.heic)

![](https://substackcdn.com/image/fetch/$s_!FU4M!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F75f40174-7828-4d3b-91e2-83b7057c2d82_810x64.heic)

So, they are analogous given that I have told you to find torques and moments of inertia about an axis. Torques are due to:

1\. Thrust

2\. Damping

3\. Gravity

[](https://substackcdn.com/image/fetch/$s_!xspA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7e68ea39-cd48-4beb-a14f-f12b332624d5_746x490.heic)

![](https://substackcdn.com/image/fetch/$s_!xspA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7e68ea39-cd48-4beb-a14f-f12b332624d5_746x490.heic)

Note that the net force of gravity acts in the centre of mass (COM) of the system which is at a perpendicular distance of LCM from the axis whereas the thrust force acts along the propeller which is at a perpendicular distance of L from the axis that is also the length of the rod.

[](https://substackcdn.com/image/fetch/$s_!SlB0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F80c88851-1c1f-4026-83f2-f7d0903031db_910x412.heic)

![](https://substackcdn.com/image/fetch/$s_!SlB0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F80c88851-1c1f-4026-83f2-f7d0903031db_910x412.heic)

[](https://substackcdn.com/image/fetch/$s_!4yTM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0f55ce84-7b70-4a19-bcb3-48a867fee758_796x478.heic)

![](https://substackcdn.com/image/fetch/$s_!4yTM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0f55ce84-7b70-4a19-bcb3-48a867fee758_796x478.heic)

Whoa! It looks like almost our heart equation in spring block system!!! Let us see the strikingly similar analogies!

[](https://substackcdn.com/image/fetch/$s_!458R!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fedbcc6eb-9d31-40e2-a307-0a3eb74acaea_930x220.heic)

![](https://substackcdn.com/image/fetch/$s_!458R!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fedbcc6eb-9d31-40e2-a307-0a3eb74acaea_930x220.heic)

But wait!! There is a bad person here! Yeah the gravity! We have a sin 𝜃 term instead of our good old linear version 𝜃. The function sin 𝜃 is too far from being a linear function! In fact it is a horribly non linear function of 𝜃. It contains all powers of 𝜃 and is called a “transcendental” function.

[](https://substackcdn.com/image/fetch/$s_!ykcq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb62dc991-2b92-4ffe-9da7-7c3acd1b3235_704x156.heic)

![](https://substackcdn.com/image/fetch/$s_!ykcq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb62dc991-2b92-4ffe-9da7-7c3acd1b3235_704x156.heic)

The only linear term is 𝜃. Its graph is shown below and will be familiar to you.

[](https://substackcdn.com/image/fetch/$s_!IUwr!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8a86f3a4-c646-487c-ba5a-ace8b88b12e2_568x508.heic)

![](https://substackcdn.com/image/fetch/$s_!IUwr!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8a86f3a4-c646-487c-ba5a-ace8b88b12e2_568x508.heic)

Hence we cannot proceed further in solving the differential equation using the “extreme cleverness” technique that exploited the superposition and homogenity structure of the equation of the linear system.

It turns out that the famous pendulum equation also occurs in many other places which you would not believe:

- Equation governing evolution of phase of wave function in a
  superconducting Josephson junction.

- An integated ciruit called the Phase Locked Loop (PLL)

- Synchronization of fire fly’s flashing rhythm

- Rotor angle of a synchronous generator connected to an infinite bus
  (swing equation in power system analysis)

It turns out that the pendulum equation can be solved by a brute force technique when b=0 by invoking a ghostly creature called the”elliptic integral”. But again no brute force solutions as we are keeping everything nice and soft. And no numerical methods at any cost. What would be another solution?

Do you remember? Even our original springs and dampers were arbitrary curves. We invoked small displacements and used the straight line fit. Similarly, let us take a pledge to keep 𝜃 small. Hence, we throw away the non linear terms or we perform the standard straight line approximation.

[](https://substackcdn.com/image/fetch/$s_!cfxz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5a1af8a7-24e6-403d-99bb-d4e645e0b44c_866x842.heic)

![](https://substackcdn.com/image/fetch/$s_!cfxz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5a1af8a7-24e6-403d-99bb-d4e645e0b44c_866x842.heic)

The other analogies follow. And we can apply the same old mantra. Now do you realize the power of linear system!!

[](https://substackcdn.com/image/fetch/$s_!CTKb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F170dd826-5faf-452b-b707-09f265fbd0ee_976x510.heic)

![](https://substackcdn.com/image/fetch/$s_!CTKb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F170dd826-5faf-452b-b707-09f265fbd0ee_976x510.heic)

This is the significance of the linear differential equation. It is the most fundamental equation among differential equation like the straight line is, among geometry. Any other curve around small region of a point can be approximated by a straight line using the tangent line approximation. Similarly the corresponding process of straightening the curves in differential equations (by chucking off the non linear terms in an infinite polynomial expansion) is called **JACOBIAN LINEARIZATION.** Jacobian linearization is the process of linearizing a differential equation around a fixed operating point.

[](https://substackcdn.com/image/fetch/$s_!uTud!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa18e435e-a799-40db-bff1-d05e6735723a_898x430.heic)

![](https://substackcdn.com/image/fetch/$s_!uTud!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa18e435e-a799-40db-bff1-d05e6735723a_898x430.heic)

[](https://substackcdn.com/image/fetch/$s_!O67S!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9067e02-6f23-4b78-aa19-1e406964db5e_708x442.heic)

![](https://substackcdn.com/image/fetch/$s_!O67S!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9067e02-6f23-4b78-aa19-1e406964db5e_708x442.heic)

Now, perturb the pendulum by giving it an initial angle not too far (in the safely linear range) and just observe the free oscillations in the computer or DSO. Check whether the observed time period matches with the above calculate time period.

As far as ‘b’ is concerned, it is difficult to identify it theoretically since friction is a mystery always. We can identify it experimentally. The free oscillations show an exponentially decaying envelope. Fit an exponential curve for those envelope using any curve fitting algorithm or Ms Excel.

[](https://substackcdn.com/image/fetch/$s_!_vqg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F83561fe2-4034-4edc-b4d1-45bce4de15b8_606x268.heic)

![](https://substackcdn.com/image/fetch/$s_!_vqg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F83561fe2-4034-4edc-b4d1-45bce4de15b8_606x268.heic)

Thus, we come to the end of today’s theory. No doubt it is immense information. Take your time to swallow. Attempt the exercises. That will greatly help you kindle and drill the concepts deep into your head. This is the beginning of systems theoretic view of the world. All the concepts used here will be freely referred to later. So it is important that the foundations in the spring-block-damper system is strong. If you have mastered this system, then you have mastered systems and control theory. Many control problems and algorithms can be easily visualized by appealing to the spring block system.

In the next article in this series, we will continue with Jacobian linearization and control techniques. Also pending is the question of how to find the particular integral (PI). We have found only CF so far. Adieu for now.

Find the link for the next article below.

[](https://ramaseshanchandrasekaran.substack.com/p/introduction-to-differential-equations-95a)

![Introduction to Differential Equations & Control with the Aerothrust Pendulum : Part 2 - PID Control](https://substackcdn.com/image/fetch/$s_!Iepw!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F66c7e8c3-8626-4b31-b88e-8cddea988a0e_742x442.heic)

#### Introduction to Differential Equations & Control with the Aerothrust Pendulum : Part 2 - PID Control

[Rama Seshan Chandrasekaran](https://substack.com/profile/195425058-rama-seshan-chandrasekaran)

·

Mar 31

[](https://ramaseshanchandrasekaran.substack.com/p/introduction-to-differential-equations-95a)

Read full story

------------------------------------------------------------------------

13

3

Share
