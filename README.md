# DP - Dynamic Programming
## Defs
Dynamic Programming: a time-saving storage-based technique, in place of brute force recursion for runtime efficiency. The are two ideas behind it:
* to split a problem into identified and solved subproblems 
* to merge subproblems results together to solve the problem. 

Sub-problems are smaller versions of the original problem and to *find subproblems* for the original one - the most challenging part. Common subproblems:
* if a sequence is as Input, subproblem can be the part of this sequence (from the beggining or in the middle)
* if unordered sequence is as Input, it can be firstly sorted and subproblem can be the part of the sorted sequence
* if two sequences in input, the appropriate subset of both can be a subproblem
* if a matrix is as input, subproblem could be a matrix with the less dimension as the original one

Dynamic programming based on principle of optimality: if all steps of a process are optimized, then the result is also optimized. The optimal step: takes the least amount of time or takes the fewest new computations.

Dynamic programming optimizes recursive programming and saves the time of re-computing inputs later. It's special case of recursive programming, however not all recursive cases can use dynamic programming. Main advantage of dynamic programming: instead of recomputing shared steps, to store the results of each step the first time and reuse it each subsequent time. But recursive programs often repeat work when faced with overlapping steps, spending unneeded time and resources in the process.

Dynamic programming ensure each identical step is only completed once: storing that step’s results in a hash table or an array to call whenever it’s needed again. Hence, allows less repeated work and therefore better runtime efficiency.

Dynamic solutions are built bottom-up or top-down, depending on how each begins a problem and how sub-problem results are stored.

## Bottom-up
Bottom-up start by looking at the smallest possible sub-problem, called the *base case*, and then works step-by-step up to each sub-problem. As each sub-problem is solved, its solution is saved and used to solve the next lowest sub-problem. In the end, these building solutions will lead to an answer to the *main problem*.

### Tabulation
Tabulation is the process of storing results of sub-problems from a bottom-up approach sequentially. It's iterative, not recursive process, as in tabulation we complete each sub-problem before beginning the next.

In tabulation, there are no choice for sub-problems, but every sub-problem between the *base case* and the *main problem*, hence such a sequential order lends to use lists or array to collect sub-problem results in a specific order.

## Top-down
Top-down is the opposite to bottom-up: first looks at the main problem and breaks it into smaller and smaller sub-problems until the *base case* is reached. This is the common method to build recursive solutions. Hier only solves sub-problems as they are needed, rather than solving all in order.

### Memoization
Memoization is the process of storing sub-problem results in a top-down approach.
Because of nature top-down approaches to solve problems as needed, memoization stores data in a non-sequential way. Hence, hashtables are often used for collections, as they store data in an unordered way.

