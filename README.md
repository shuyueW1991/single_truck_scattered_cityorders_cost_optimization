# single_truck_scattered_cityorders_cost_optimization
I have a truck, and I have several assigned orders that involves many cities. What is the route for the truck that leads to a minimized cost about taking shipment at the starting point of an order, releasing shipment at the ending point of an order, and distancial coverage consumption.

## permutation
I can randomly loop the permutations of the involved cities.
Since I confine the problem into ** 1 truck ** ( as subject) with ** multiple orders involving several cities **, the permutation range of cities can be viewed as not necessarily involving other new ones: because as far as I see it, any extra coverage to other cities not listed in the involving city list is simply redundance.
In the company code, I tested to see that the permutation is really time-costly. Since the enumeration amount mounts up really quickly with the number of city candidates.

## Genetic Algorithm
In order to cut down this cost, a GA is expected due to the fact that  a good-local-solution-inspired enumeration helps the preserving a good solution in cases where people are not that forced to have **THE** best solution. 
However, the GA is essentially the same method as compared to permutation.

## a vague modeled output via RL
If a model that is **quasi-approariate** for a lot of cases (their shared common characteristics can be discussed beforehand), its output can be used to be the initial solution.
Its improvement can be also iterated via RL.
Then, a time cost can be saved in the realtime agile cases.

# RL: several notes
With this perspective, I do this shit.

## Framework
I am still wondering, do I establish my own, relatively simple framework of RL, or utilizing other exisitng big stuff while introducing redundant stuffs?

## Problem formulation
I decide to commence the voyage from a small number of city candidates, since the convergence can be quick. 




