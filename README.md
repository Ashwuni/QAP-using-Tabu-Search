# QAP-using-Tabu-Search

This is one of the QAP (quadratic assignment problem) test problems of Nugent et al.
20 departments are to be placed in 20 locations with five in each row (see below). The objective is to
minimize costs between the placed departments. The cost is (flow * rectilinear distance), where both flow
and distance are symmetric between any given pair of departments. The flow and distance matrices are
attached to this assignment. The optimal solution is 1285 (or 2570 if you double the flows).

1. Code a simple TS to solve the problem. To do this you need to encode the problem as a permutation,
define a neighborhood and a move operator, set a tabu list size and select a stopping criterion. Use only a
recency based tabu list and no aspiration criteria at this point. Set the default neighborhood function to
check the whole neighborhood.
2. Run your TS.
3. Perform the following changes on your TS code (one by one) and compare the
results.
• Change the initial starting point (initial solution) 10 times
• Change the tabu list size twice – once smaller and once larger than your original choice
• Change the tabu list size to a dynamic one – an easy way to do this is to choose a range and
generate a random uniform integer between this range every so often (i.e., only change the tabu
list size infrequently)
• Add 2 aspiration criteria in 2 separate experiments: best solution so far, best solution in the
neighborhood
• Use less than the whole neighborhood to select the next solution
