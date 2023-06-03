+++
title = "100 MPG on Gasoline"
full_title = "100 MPG on Gasoline Could We Really?"
upstream_url = "https://dothemath.ucsd.edu/2011/07/100-mpg-on-gasoline/"
date = "2011-07-17"

+++
Source: [here](https://dothemath.ucsd.edu/2011/07/100-mpg-on-gasoline/).

100 MPG on Gasoline: Could We Really?

Since I was a teenager, I frequently heard stories that some guy had invented a car that could get 100 miles per gallon (MPG), but that powerful interests (often GM, Chevron, etc.) had bought rights to the idea and sat on it. We suckers were left to shell out major bucks for gasoline, when a solution was in hand and under wraps.

Leaving aside the notion that such a design would bring unbelievable prosperity to its holder (i.e., no real incentive to *sit* on it), let’s look at what physics says is possible.

We like cars because we can travel quickly from point A to point B. So let’s evaluate the energy requirements to make that journey at freeway speeds. We will use the somewhat awkward (although appropriate) speed of 67m.p.h. because it conveniently maps to 30 meters per second. At these speeds, aerodynamic resistance is the dominant energy drain, so we will start by evaluating *only* this to get a lower bound on fuel efficiency, and find that we do a pretty good job\!

## What a Drag!

As long as your car is bigger than a dust grain, air resistance increases as the square of velocity. This is because in the car’s frame of reference, with an oncoming “wind,” the kinetic energy in the “wind” that the car disrupts depends on the square of the air velocity. If the car had no aerodynamic attributes (like a sheet of plywood face-on to the flow), it would basically rob the oncoming column of air of *all* its kinetic energy.

If the distance traveled is *D*, the car sweeps out a volume of air during its travel equal to the cross-sectional area of the car, *A*, times the travel distance, *D*. To make this more explicit, a car with a frontal area of 3 square meters (2 meters wide and 1.5 meters tall) traveling 25 miles (40km) will impact a tube of air with base area 3m² and 40,000 meters long. The kinetic energy in this tube is ½*mv*², where *m* is the mass of the air involved. We already know that the volume of the air impacted is *A·D*, so its mass is just the volume times the density of air, which we will call *ρ*. At sea level, *ρ*=1.3 kg/m³ for air (for reference, water has a density of 1000 in these units).

Putting these together, a tragically un-aerodynamic car would see a drain of energy of *E*_(drag)=½(*ρAD*)*v*², where the term in parentheses is the mass of the air involved. A real car has better aerodynamic performance than a piece of plywood, so we include a term called the drag coefficient, *c*_(D), and the energy expended on fighting air for the journey becomes *E*_(drag)=½*c*_(D)*ρADv*². The drag coefficient for cars ranges from 0.25 for a Prius to numbers like 0.5–0.6 for SUVs and pickup trucks. Loads of sedans come in around *c*_(D)=0.3, so we’ll use that number for the present analysis.

## Heat Engines and Gasoline

We, of course, get the energy to fight air resistance by burning gasoline in our engines. Automobile engines constitute heat engines, whose thermodynamic efficiency is bounded by limitations on entropy to be no more than 100×(*T_(h)* − *T_(c)*)/*T_(h)* percent, where *T_(h)* and *T_(c)* are the hot and “cold” temperatures (in Kelvin) that the engine operates between. This, plus practical limitations, puts most automobile engines in the range of 15–25%. If we could achieve an ideal heat engine operating between the volume-averaged explosion temperature of around 1200°K (my guess) and the ambient 300°K, we’d have an efficiency of 75%. But the exhaust manifold—acting as the “cold” temperature for the cylinder—is much warmer than ambient temperature, and the cylinder walls moderate the effective hot temperature to reduce the theoretically achievable efficiency. A turbo-pump can use the hot exhaust to recover some of the lost energy flow and achieve better performance.

Gasoline delivers 36.6kWh (132MJ) per gallon. Used at 20% efficiency, this translates to *E*_(deliv)=26MJ (megajoules) of energy actually delivered to the drive train per gallon burned.

## Our Calculated Mileage

We are now in a position to calculate how many miles we can expect to travel per gallon of gasoline. Setting the energy delivered by a gallon of gas equal to the energy required to overcome air resistance: *E*_(deliv)=½*c*_(D)*ρADv*² and solving for *D* using the values sprinkled above, we find that *D*=50,000m, or 50km, or 31 miles. So our hypothetical air-resistance-only car gets 31MPG at freeway speeds. Seems completely reasonable. We’ll adjust this and all other air-resistance-only calculations later for rolling resistance.

## Pushing Limits

What could we do to improve mileage? The simplest option is to slow down. The quadratic dependence on velocity is striking, and this is where the biggest, easiest gains may be had. But we like to engineer our way to a solution, not change behaviors. So the knobs are: engine efficiency; coefficient of drag; and frontal area. The best, weird-looking concept cars achieve drag coefficients around 0.15. If we were willing to live with trout-shaped cars, we might get *c*_(D) down to a bit less than 0.1. Diesel engines operate at a higher temperature and get better thermodynamic efficiency. The best of the best (in train locomotives and large ships) get 50%. For a gasoline engine made from steel, 30% would be a stretch. Decreasing frontal area is not usually compatible with our need to transport multiple people. If we were willing to sit single-file, we could do the trout shape with low frontal area. We might even stop hearing “stop touching me!” from the back seat. I will point out that trout cars would be a real pain to parallel park, necessarily being pretty long—with much of the length in a tail section that is too narrow to be of much use.

[![](https://dothemath.ucsd.edu/wp-content/uploads/2011/07/trout-car-300x119.png "trout-car")](https://dothemath.ucsd.edu/wp-content/uploads/2011/07/trout-car.png)As a fantastical example, using *A*=1.5m², *c*_(D)=0.1, and engine efficiency at 50%, we get the astounding fuel economy number of 466MPG. But you’re not going to get a locomotive-performance engine in a 1.5 square meter trout-car. A more practical set of limits given our behavioral and aesthetic preferences might be *A*=2.5m², *c*_(D)=0.2, and 30% engine efficiency. This puts us at 84MPG. Not a bad place to be, but shy of the magic 100MPG. And even this is not a snap: note that we are nowhere close to this mark at present.

How does the Prius today get a fuel economy in the low 50’s? The drag coefficient is on the low side, at 0.25. The area is small-ish—I estimate 2.5m², and the big trick is that the engine can be optimized for freeway speeds since the battery can assist acceleration at lower speeds. Traditional cars sacrifice freeway efficiency for the get-up-and-go performance that is so important in test drives. If I use 25% engine efficiency with the aforementioned values, I get 56 MPG.

## What About Rolling Resistance?

We have so far neglected rolling resistance (mainly from tires) in this analysis, primarily to keep things simple while capturing the dominant contributor to fuel economy at freeway speeds. At a rolling friction coefficient of 0.01, a 1 ton car (1000kg; 10,000 Newtons) requires 100 Newtons of force to push along—independent of velocity. This effect alone (e.g., driving in a vacuum) would result in a limit of 160MPG at a 20% engine efficiency. At 30m/s (67m.p.h.) in air, factoring in rolling resistance: our 31MPG sedan becomes 26MPG; our 56MPG Prius becomes 45MPG; our absurd locomotive trout car at 466MPG becomes 220MPG; and our “realistic” 84MPG car now gets 63MPG.

But keep in mind that these numbers are not to be taken *too* literally. We made plenty of round-number estimates for frontal area, engine efficiency, etc. The numbers are *reasonable* and give us a framework for understanding approximate limits. So I don’t want to hear anyone speaking of 63MPG as a meaningful hard limit. It’s ballpark. It’s useful. Lots of details could be added to the analysis, but we’ve already captured the essence of the problem.

## The Point of it All

The purpose of this post is to illustrate that fuel efficiency on the freeway is *not mysterious*. It’s the air, stupid. We have few knobs to turn, and are limited in how much more we can turn them. The biggest disappointment, perhaps, is the typical 20% performance of our engines. Naïvely, this suggests a factor of five potential gain. But as long as we’re making fireballs in our cylinders, we’re limited by harsh thermodynamic realities. A [future post](https://dothemath.ucsd.edu/2011/08/mpg-for-electric-cars/ "MPG for Electric Cars?") will deal with the potential of electric cars. We’ll have to abandon gallons as a measure (and when we do, we should also flip the measure to be energy per distance, opposite our familiar MPG).

Hits: 5497

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2011%2F07%2F100-mpg-on-gasoline%2F&linkname=100%20MPG%20on%20Gasoline%3A%20Could%20We%20Really%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2011%2F07%2F100-mpg-on-gasoline%2F&linkname=100%20MPG%20on%20Gasoline%3A%20Could%20We%20Really%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fdothemath.ucsd.edu%2F2011%2F07%2F100-mpg-on-gasoline%2F&linkname=100%20MPG%20on%20Gasoline%3A%20Could%20We%20Really%3F "Email")[](https://www.addtoany.com/share)
