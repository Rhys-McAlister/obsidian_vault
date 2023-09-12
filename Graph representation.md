 
## Components of a graph

Objects ($N$): nodes, vertices
Interactions ($E$): links, edges
System($G(N,E)$): network, graph

Determining the manner in which you represent your problem or domain in terms of its graph structure is key to using networks successfully. 

**Node degree** $k_i$. the number of edges adjacent to a given node $i$. The average degree is the average over all the nodes within the network and is given by: $\bar{k} = \frac{2E}{N}$ . When considering directed graphs there is more granularity in how edges are defined. Degrees in directed networks are defined in terms of in-degrees and out-degrees and the total degree of a node is the sum of the in and out degrees.

**Bipartite graph**. A graph in which nodes can be divided into two disjoint sets $U$ and $V$ such that every link connects a node in $U$ to one in $V$. Note that $U$ and $V$ are independent sets.

## Representation 

**Adjacency matrix**. A square matrix of boolean values indicating connections between nodes. $A_{ij} = 1$ if there is a connection from node $i$ to $j$ otherwise $0$. Adjacency matrices based on real data tend to be sparse.  

**Edge list**. A more dense representation of graph connectivity comes in the form of edge lists. An edge list simply provides a vector of tuples of node indexes indicating an edge being present between the two nodes. This approach tends to be computationally efficient but harder to reason about for analysis.

**Adjacency list**. A list of a given nodes neighbours. Tends to be easier to reason about when the network is large and/or sparse. Allows for the easy retrieval of all neighbours of a given node.

**Node and Edge attributes**. 