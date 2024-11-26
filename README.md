# CSC-333--Linear-Programming-Problems
This contains Graphical solutions to Linear programming problems
1. Purpose
The goal of the code is to:

Solve optimization problems (e.g., maximize profit or minimize cost).
Visualize constraints, feasible regions, and optimal solutions.
Use Python libraries for plotting and calculations.
2. Libraries
The code imports:

numpy: For mathematical operations, such as defining arrays and calculating constraint boundaries.
matplotlib: For plotting graphs to visualize constraints, feasible regions, and optimal points.
3. Problem Setup
Each question focuses on:

Decision Variables: Represented by 
x
x and 
y
y, these are the quantities to optimize.
Objective Function: A linear equation, 
Z
=
c
1
x
+
c
2
y
Z=c 
1
​
 x+c 
2
​
 y, to maximize or minimize.
Constraints: Inequalities, such as 
a
1
x
+
b
1
y
≤
d
1
a 
1
​
 x+b 
1
​
 y≤d 
1
​
 , defining the limits of the problem.
4. Constraints Implementation
Each constraint is represented as a function in Python.
These functions compute the corresponding 
y
y-values for a given range of 
x
x-values.
For example, a constraint like 
2
x
+
3
y
≤
12
2x+3y≤12 is rewritten as:
y
≤
12
−
2
x
3
y≤ 
3
12−2x
​
 
The function computes 
y
y for a series of 
x
x-values, and the resulting line is plotted.
5. Feasible Region
The feasible region is where all constraints are satisfied.
The code uses numpy.minimum to find the intersection of constraints and shades the valid region using plt.fill_between.
Non-Negativity Constraint: The code ensures that 
x
,
y
≥
0
x,y≥0 by restricting the plotted region to positive values.

6. Corner Points
The intersection points of constraints (corner points of the feasible region) are critical because the optimal solution lies at one of these points.
The code uses analytical methods (e.g., solving simultaneous equations with numpy.linalg.solve) to calculate these points.
7. Optimal Solution
For maximization/minimization, the objective function is evaluated at each corner point.
The corner point yielding the highest (or lowest) value of the objective function is the optimal solution.
8. Visualization
The code plots:
Constraint lines.
The shaded feasible region.
Corner points (marked with dots).
The optimal solution (highlighted and annotated).
Annotations: Each corner point and the optimal solution are labeled on the graph for clarity.

9. Example Problem
Each question in the code tackles a unique optimization scenario:

Maximizing Profit: Example: 
Z
=
3
x
+
2
y
Z=3x+2y subject to constraints like 
2
x
+
3
y
≤
12
2x+3y≤12.
Minimizing Cost: Similar setup but focuses on finding the lowest value of 
Z
Z.
Resource Allocation: Constraints represent available resources, and the objective function quantifies their utilization.
10. Key Features
Reusable Structure: Each question is defined in a modular way, allowing constraints and objectives to change easily.
Dynamic Graphs: The code dynamically adapts to constraints and highlights the feasible region and solutions.
Accurate Results: By calculating corner points explicitly, the optimal solution is guaranteed.
