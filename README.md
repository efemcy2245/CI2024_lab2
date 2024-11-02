# CI2024_lab2
Travelling salesman problem

Inside there is the implementation of genetic algorithm using different components to see different behaviour:
From the first to the fourth row we have the application of classic genetic algorithm in which we combine different parent selection ( roulette wheel and tourment selection (tao = 5 number of selected parents) ). We see that the greedy algorithm is yet really optimize for this particular problem, we start from a good solution, in this way is difficult to optimize. (only the  roulette_wheel - swap_mutation has received a little improvement on the solution).

In the hyper-modern Genetic Algorithms if we start from a good solution using a greedy algorithm or something similar we can't see any improvement, but if we start from a worst solution we can get improvement in time ( to demostrate that the algorthm works but the problem is NP-hard )

If you see the code in the hyper-modern Genetic Algorithms, the operator algorithm is chosen from a bernoulli distribution, P(mutation)=0.8 and P(combination)=0.2, if we pick the mutation then we have another bernoulli distribution to pick the right mutation algorithm P(swap mutation) = 0.5 P(insert mutation)=0.5.
For hyper-modern Genetic Algorithms we use 5_000_000 instead of 1_000_000.


| Typology_method  | Initial_cost |  Cost_after_mutation | Typology algorithm  | Steps |
|----------|----------|----------|----------|----------|
| roulette_wheel - swap_mutation | 4436.031770 | 4431.363768 | Greedy algorithm | 1_000_000 |
| roulette_wheel - insert_mutation | 4436.031770 | 4436.031770 | Greedy algorithm | 1_000_000 |
| tourment_selection - swap_mutation | 4436.031770 | 4436.031770 | Greedy algorithm | 1_000_000 |
| tourment selection - insert_mutation | 4436.031770 |4436.031770 | Greedy algorithm | 1_000_000 |
| Tourment Selection - swap_mutation - insert_mutation - inner_over (hyper-modern Genetic Algorithm) | 4436.031770 | 4436.031770 | Greedy algorithm | 5_000_000 |
| Tourment Selection - swap_mutation - insert_mutation - inner_over (hyper-modern Genetic Algorithm)| 4898.633717 | 4898.633717 | Similar Greedy algorithm | 5_000_000 |
| Tourment Selection - swap_mutation - insert_mutation - inner_over (hyper-modern Genetic Algorithm)| 17985.344514 | 15277.778943 | Mean Distance algorithm | 5_000_000 |

