## Knapsack Problem (KP) and Travelling Salesman Problem (TSP)

### Question 1: Linear Knapsack Problem

The Knapsack Problem (KP) is a combinatorial optimization problem. A Knapsack model serves as an abstract model with a wide range of applications, such as:
- Resource allocation problems
- Portfolio optimization
- Cargo-loading problems
- Cutting stock problems

In the linear KP, the objective function and constraints are linear. The following problem can be formulated as a linear KP problem.

#### Problem 1: Linear Knapsack Problem
Consider the following pairs:

\[
(v_i, w_i) = \{(2, 7), (6, 3), (8, 3), (7, 5), (3, 4), (4, 7), (6, 5), (5, 4), (10, 15), (9, 10), (8, 17), (11, 3), (12, 6), (15, 11), (6, 6), (8, 14), (13, 4), (14, 8), (15, 9), (16, 10), (13, 14), (14, 17), (15, 9), (26, 24), (13, 11), (9, 17), (25, 12), (26, 14)\}
\]

with total capacity \( W = 30 \).

#### Greedy Algorithm for Solving the Knapsack Problem

1. Identify the available items with their weights and values, noting the maximum capacity of the knapsack.
2. Use an efficiency function (profit-to-weight ratio): \( \frac{v_i}{w_i} \).
3. Sort the items in non-increasing order according to the efficiency function.
4. Add items with the highest score into the knapsack, tracking their cumulative weights until no more items can be added without exceeding the capacity.
5. Return the set of items that satisfies the weight limit and yields the maximum profit.

**[7 Marks]**

---

### Question 2: Travelling Salesman Problem (TSP)

Consider the following distance matrix for a 7-city symmetric Travelling Salesman Problem (STSP):

\[
M = 
\begin{bmatrix}
0 & 1.5 & 3 & 13 & 3.5 & 4.5 & 1.5 \\
1.5 & 0 & 1.3 & 13 & 13 & 2.3 & 1.5 \\
3 & 1.3 & 0 & 1.5 & 13 & 3 & 20 \\
13 & 13 & 1.5 & 0 & 1.5 & 13 & 3.3 \\
3.5 & 13 & 13 & 1.5 & 0 & 1.5 & 3.3 \\
4.5 & 2.3 & 3 & 13 & 1.5 & 0 & 1.5 \\
1.5 & 1.5 & 20 & 3.3 & 3.3 & 1.5 & 0
\end{bmatrix}
\]

where \( m_{ij} = m_{ji} \).

#### 2-Opt Heuristic Solution

Minimize the above problem using the 2-Opt heuristic. Use the initial route:

\[
x = (1, 3, 5, 7, 4, 6, 2)
\]

Count the number of improving solutions found during the 2-Opt procedure, and list each improving solution \( (x_i, f(x_i)) \). Finally, report the optimal solution \( x^* \) and the corresponding optimal distance \( f(x^*) \).
