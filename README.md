[<img src="https://assets.signaloid.io/add-to-signaloid-cloud-logo-dark-v6.svg#gh-dark-mode-only" alt="[Add to signaloid.io]" height="30">](https://signaloid.io/repositories?connect=<https://github.com/gcizman/Signaloid-Signaloid-Demo-Robotics-AStarSearch>#gh-dark-mode-only)
[<img src="https://assets.signaloid.io/add-to-signaloid-cloud-logo-light-v6.svg#gh-light-mode-only" alt="[Add to signaloid.io]" height="30">](https://signaloid.io/repositories?connect=<https://github.com/gcizman/Signaloid-Signaloid-Demo-Robotcs-AStarSearch>#gh-light-mode-only)


#A * Search Algorithm

This is an example implementation of the A* search algorithm1, which searches a graph for the shortest path between two nodes. To improve performance, heuristics are used to prioritise paths that are most likely to be optimal.

The heuristic function estimates the cost of the cheapest path from each node to the destination node — if the heuristic function is guaranteed to never overestimate the actual path cost, then the A* algorithm is guaranteed to find the optimal shortest path from start node to end node. An example of a heuristic function could be the Euclidean distance between a node and the destination node.

Since the heuristic function can only provide an estimate for path lengths, there may be an element of uncertainty in the heuristic values for each node. Another potential source of uncertainty is in the graph's edge weights, for example if they have been empirically determined by a robot operating in the real-world. Signaloid's uncertainty tracking technology allows the A* algorithm to be implemented using uncertain variables, tracking uncertainty through to the final output.

In this example, we model uncertainty in heuristic values using a Gaussian distribution with standard deviation of 10% of the mean value. Uncertainty in graph edge weights is modelled using a Gaussian distribution with standard deviation of 5% of the mean value. These distributions have been picked arbitrarily for illustrative purposes — Signaloid's uncertainty tracking technology allows you to use any uncertainty distributions here.
