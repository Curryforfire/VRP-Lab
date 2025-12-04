# VRP-Lab: A Unified Experimental Framework for Vehicle Routing Problems
VRP-Lab is a research-oriented framework for studying Vehicle Routing Problems (VRPs) from both a classical optimization and a learning-based perspective. The initial focus is on the Capacitated Vehicle Routing Problem (CVRP) and the Vehicle Routing Problem with Time Windows (VRPTW, Solomon instances).

The long-term goal is to build a coherent “playground” where different algorithmic paradigms — exact methods, heuristics, metaheuristics, and learning-based approaches — can be implemented, compared, and combined in a systematic way.

⸻

Objectives

The project is designed with the following objectives:

+ Provide clean and reusable abstractions for VRP instances and solutions (CVRP and VRPTW as core benchmarks).
+ Implement baseline exact models (MIP) that serve as references and lower bounds.
+ Implement classical constructive heuristics and local search operators to understand core algorithmic ideas.
+ Develop metaheuristics (e.g., Simulated Annealing, Adaptive Large Neighborhood Search) on top of these operators.
+ Integrate learning-based components (e.g., Pointer Networks, RL-guided neighborhood selection) into the existing heuristic and metaheuristic frameworks.
+ Enable systematic benchmarking on standard datasets (CVRPLIB and Solomon) with reproducible experiments.

⸻

Planned Workflow

The development follows a staged and incremental workflow:

1. **Problem abstraction.**  
   Define common data structures and interfaces for VRP instances and solutions, starting with CVRP and VRPTW (Solomon) as primary testbeds.

2. **Exact baselines.**  
   Formulate and implement MIP models for CVRP and VRPTW using a commercial or open-source solver, to obtain exact solutions or strong lower bounds on small and medium-sized instances.

3. **Classical heuristics.**  
   Implement constructive heuristics (e.g., Clarke–Wright, insertion) and local search operators (e.g., 2-opt, relocate, swap), and use them to generate feasible solutions of reasonable quality.

4. **Metaheuristics layer.**  
   Build metaheuristic frameworks (e.g., multi-start local search, Simulated Annealing, Adaptive Large Neighborhood Search) that orchestrate these operators and improve solution quality under time limits.

5. **Learning-based components.**  
   Introduce learning-based modules that interact with the existing frameworks, such as neural policies for next-customer selection, destroy/repair operator selection, or route construction, while keeping the underlying VRP structure explicit.

6. **Benchmarking and analysis.**  
   Run controlled experiments on standard benchmarks (CVRPLIB for CVRP, Solomon for VRPTW), compare algorithms under unified interfaces, and analyze trade-offs between solution quality, runtime, and implementation complexity.
