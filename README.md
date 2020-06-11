# Computational-Complexity

Final project:
    Identify an NP-hard problem from an area of CS research (preferably your own research area), and build a tool that solves instances of this problem using off-the-shelf SAT/SMT solvers.
    
Topic: Graph Coloring

##

install minisat: cd minisat and run make

compile: run 
             g++ -o ggen ggen.cpp -std=c++11
             g++ -o g2cnf g2cnf.cpp -std=c++11
             g++ -o sln sln.cpp -std=c++11

generate a Graph G(V, E):
            ./ggen <#nodes> <#probability> [#out-file]

convert to CNF: 
            ./g2cnf <#gfile> <#color> [#our-file]

throw it to the SAT solver:  
            ./minisat  [#cnf-file] [#sat-file]

output the solution: 
            ./sln <#cnf-file> [#sat-file]
