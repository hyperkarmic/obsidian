# Introduction To Alogrithms - Thomas Cormen
## Parker Klein Notes
-   An algorithm is a sequence of computational steps that transforms the input into the output. A tool for solving a well-specified computational problem
    
-   Which algorithm is best depends on the number of items, the extent to which the items are already somewhat sorted, possible restrictions on the item values, the architecture of the system, the kind of storage devices to be used
    
-   Data structure: a way to store and organize data in order to facilitate access and modifications
    
-   Insertion sort is faster than merge sort for small values of n
    
-   Insertion sort: an efficient algorithm for sorting a small number of elements. Sorts numbers in place: rearranges the numbers within the array
    
-   Boolean operators 'and' and 'or' are short-circuiting
    
-   Runtime is the number of primitive operations or 'steps' executed. Sum of the running times for each statement executed. We focus on worst-case running time, the longest running time for any input of size n. Guarantees the algorithm will never take any longer
    
-   Incremental: insertion sort, one element at a time
    
-   Recursive: call themselves recursively to deal with closely related sub-problems
    
-   Divide-and-conquer: break the problem into several subproblems that are similar to the original but smaller in size, solve the subproblems recursively, and then combine these solutions to create a solution to the original problem
    
-   Merge sort: divide the n-element array into two subsequences of n/2 elements each, sort the two subsequences recursively using merge sort, merge the two sorted subsequences to produce the sorted array
    
-   Sentinel values are used to know when to stop
    
-   Divide-and-conquer: solve the problem recursively, applying 3 steps at each level of recursion. 1. Divide the problem into a number of subproblems that are smaller instances of the same problem. 2. Conquer the subproblems by solving them recursively. If the subproblems sizes are small enough, just solve them. 3. Combine the solutions to the subproblems into the solution for the original problem
    
-   Directed graph: G is a pair (V, E), V is vertex set, E is edge set. Self loops: edge from a vertex to itself is possible
    
-   Undirected graph: G = (V, E) is unordered
    
-   Edge notation: (U, V) incident from U and incident to V
    
-   Degree is incidences on the vertex
    
-   Acyclic is no cycles
    
-   Adjacent vertices have an edge between
    
-   Isolated is a vertex with degree 0
    
-   An undirected graph is connected if every vertex is reachable from all other verticies
    
-   Directed graph is strongly connected if every two vertices are reachable from each other
    
-   A complete graph is an undirected graph in which every pair of vertices is adjacent
    
-   A bipartite graph is an undirect graph in which V can be partitioned into two sets V1 and V2 such that all edges go between V1 and V2
    
-   Forest: undirected acyclic graph
    
-   The number of children of node x in a tree is the degree of x
    
-   Full binary tree: each node is either a leaf or has degree exactly 2
    
-   Permutation: finite set S is an ordered sequence of all the elements of S, with each element appearing exactly once
    
-   Probability comes from a sample space S, whose elements are elementary events which are possible outcomes of an experiment. An event is a subset of a sample space. A sample space is all the possible combinations of outcomes
    
-   Bernoulli trial: an experiment with only two possible outcomes: success with probability p, and failure with probability q = 1 - p
    
-   Probabilistic analysis is the use of probability in the analysis of problems
    
-   An algorithm is randomized if its behavior is determined by its input and by values produced by a random-number generator
    
-   Heapsort uses the heap data structure which is also good for priority queues
    
-   Heapsort uses max-heaps, priority queues use min-heaps
    
-   Height of a node is the number of edges on the longest simple downward path from the node to a leaf
    
-   Radix sort: sorts by least significant digit first, it continues to sort by putting the elements into the appropriate bin based on the digit or column and eventually they are sorted in the correct order
    
-   Stacks: the element deleted from the set is the one most recently inserted, LIFO policy
    
-   Queue: element deleted is the one that has been in the set for the longest time, FIFO
    
-   Sentinel: dummy objects to allow us to simplify boundary conditions
    
-   Collision: when two keys hash to the same slot
    
-   Chaining: the simplest collision resolution technique
    
-   Chaining: we place all the elements that hash to the same slot into the same linked list
    
-   Dynamic programming solves problems by combining solutions to subproblems. Solves each subproblem once and then saves its answer in a table
    
-   Dynamic programming uses additional memory to save computation time. This is a time-memory trade-off
    
-   Top-down with memoization: write a recursive procedure, and save the result of each subproblem, first checks if the subproblem has been previously solved. Memoized: it remembers what results were previously computed
    
-   Bottom-up method: solving any particular subproblem depends only on solving 'smaller' subproblems, we sort the subproblems by size and solve them in order, smallest first
    
-   Common pattern in discovering optimal structure: 1. solution to the problem involves a choice. The choice leaves one or more subproblems to be solved 2. you suppose a choice leads to an optimal solution, you don't concern yourself yet with how to determine the choice, you assume it is given 3. given the choice, you determine which subproblems ensue 4. you use a cut-and-paste technique to show solutions to subproblems within an optimal solution are optimal themselves
    
-   Greedy algorithms always make the choice that looks best at the moment
    
-   Greedy algorithm process: 1. determine the optimal substructure of the problem 2. develop a recursive solution 3. show if we make the greedy choice, only one subproblem remains 4. prove it is always safe to make a greedy choice 5. develop a recursive algorithm that implements the greedy strategy 6. convert the recursive algorithm to an iterative algorithm
    
-   Minimum spanning tree: given a connected undirect graph G = (V, E), find a subset of edges that connects all the vertices together and has a minimum total length
    
-   Two most common representations of graphs are adjacency lists and adjacency matrices
    
-   Adjacency-list: compact way to represent sparse graphs
    
-   Adjacency-matrix: useful for dense graphs, or when we need to tell quickly if there is an edge connecting two given vertices
    
-   Breadth-first search: given a graph G = (V, E) and a source vertex S, explore the edges of G to 'discover' every vertex that is reachable from S
    
-   Depth-first search: search deeper in the graph whenever possible. Explores edges out of the most recently discovered vertex V that still has unexplored edges, once all V's edges have been explored, it backtracks to explore edges leaving the vertex from which V was discovered

#algorithms
#cormen
