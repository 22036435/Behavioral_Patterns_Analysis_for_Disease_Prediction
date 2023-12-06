#Longest Path in a Directed Acyclic Graph

    #Overview

        This Python script finds the longest path from a given starting node to all other nodes in a weighted Directed Acyclic Graph (DAG). This problem is a variant of the classic shortest path problem, and it is solved using dynamic programming and topological sorting.

    #Problem Statement

        Given a weighted Directed Acyclic Graph (DAG) and a starting node, the objective is to find the longest path from the starting node to every other node in the graph. The graph consists of nodes connected by directed edges, each with an associated weight. The weight of a path is the sum of the weights of its constituent edges.

    #Algorithm Description

        The script implements the following algorithm:

            Topological Sorting: The DAG is first topologically sorted. A topological sort of a DAG is a linear ordering of its nodes where for every directed edge UV from node U to node V, U comes before V in the ordering.
            
            Distance Initialization: A distance dictionary is initialized where the distance to the starting node is set to 0 and the distances to all other nodes are set to negative infinity. This is because we are interested in finding the maximum distance (longest path).
            
            Relaxation of Edges: The script then iterates through each node in the topologically sorted order. For each node, it relaxes the edges by checking if the longest path to an adjacent node can be improved by going through the current node.

#Minimum Coins for Change Problem

    #Overview

        This script solves the Minimum Coins for Change problem, a classic problem in dynamic programming. The goal is to find the minimum number of coins that you need to make up a certain amount of money, given an unlimited supply of coins of different denominations.

    #Problem Statement

        Given a set of coin denominations and an input value, determine the minimum number of coins needed to make up that amount. If that amount of money cannot be made up by any combination of the coins, return -1.

    #Algorithm Description

        The script uses a dynamic programming approach to solve this problem:

            Dynamic Array Initialization: Create an array dp where dp[i] will store the minimum number of coins required for amount i. Initialize dp[0] to 0 (since no coins are needed for amount 0) and the rest of the elements to infinity (as a placeholder for yet-to-be-calculated values).

            Bottom-Up Calculation: For each amount from 1 to the input value, compute the minimum number of coins required. This is done by iterating through each coin denomination and updating dp[i] if a better (smaller) number of coins is found.

            Result: The last element in the dp array gives the minimum number of coins required for the input value.