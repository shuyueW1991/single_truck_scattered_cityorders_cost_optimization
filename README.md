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
With this perspective, I begins to do this shit.

## Framework
I am still wondering, do I establish my own, relatively simple framework of RL, or utilizing other exisitng big stuff while introducing redundant stuffs?

## Problem formulation
I decide to commence the voyage from a small number of city candidates, since the convergence can be quick. 


## Learnability
However, there remains one problem:
The formulation is also about the learnability of rl.
I need to know whether the formulated problem as welll as its solution is appliable to other similar cases, or how to define 'similar'?
In the worst case, similar cases have similar topologies, with only differences in values.
For example, 
1 truck;
same number of cities;
same number of orders(?);
same topological location of orders compared with interrelation betweens cities without orders.

I think that, the convenience of deploying RL-trained model cannot be seen until it is applied directly rather than random initialization.
Therefore, the transplatability matters, which is still invisible to me.
This frustrates me. 
I look up the ** transfer in (deep) reiniforcement learning**. 
I think **policy transfer** in this area may help. also is the case of ** adaptive policy transfer**。
They refer the tranfer to the osurce policy.
I think the similarity is case-oriented, which can be delayed after the mission in the next section is majorly done.



# GAN with transfer
The idea comes from two sources:
GAN is inspired by their application in pictures, while transfer is deemed to be a direct applying of existing solution or human experience.
For one given truck with assigned city list (since city composites the final path of the truck), the best solutuion to the each order urban distribution variation can be seen as a 1-dimensional image. Like there are many images that depicts **dog**.
Therefore, I think the similarity in this GAN transfer case is more controllable.

## diagram
1. hard-corely accumulate correct answers
2.maybe the benefit can be seen by increasing the scale of city numbers
3. is there local improvemnet for the output of given model?
4. is there way of extrapolate the result, in terms of city numbers, for example? maybe, transfer? but I think further analogy is way too complicated.




