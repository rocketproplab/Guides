# Evolutionary Algorithms

Evolutionary algorithms can be applied to design problems to converge on an optimal solution for multidimensional problems.

## Genetic Algorithms
Genetic algorithms use a selection, mutation sequence of steps to converge on a solution that lies on the _Pareto Front_.

### Step 1: Generate Initial Population
Generate at least _R_ linearly independent individuals for a problem in _R_ space.

### Step 2: Selection
Evaluate the population against a fitness function of _R_ variables and select a subset >1 of the individuals to remain.

### Step 3: Mutation
Apply semi-stochastic operations to the selected population to create a new population of _R_ individuals.

### Step 4: Recursion
Repeat steps 1-3 until the fitness of an individual passes the termination test.

### Step 5: Completion
Termination yields a single individual that is _an_ optimal solution. This method is nondeterministic, so multiple optimal solutions are possible. Perhaps add option to throw "nonstochastic" flag to the program to ensure the program converges on the same solution. 
