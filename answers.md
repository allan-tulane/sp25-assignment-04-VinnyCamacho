# CMPS 2200 Assignment 5
## Answers

**Name:** Vincent Camacho






- **1a.** log<sub>d</sub>n # where n is the number of nodes and d is the amount of branches at each node. I found the <sub> subscript </sub> syntax to turn subscript on and off from reddit


- **1b.** For delete-min it is O(dlog<sub>d</sub>n). For insert it is O(log<sub>d</sub>n).


- **1c.** If m is the number of edges or |E| and n is the number of vertices or |V| then we have n deletes and m inserts. The work is O(ndlog<sub>d</sub>n + mlog<sub>d</sub>n).

- **1d.** Pick d that satisfies running time of O(|E|). If d = m/n, then the costs will be equal. so O(2mlog<sub>m/n</sub>n) = O(m(logn/(log(m/n)))). if |E| = |V|<sup>1+ε</sup> or m = n<sup>1+ε</sup>, then we can plug this in for m. This yields: logn/log(n<sup>1+ε</sup>/n) = logn/logn<sup>ε</sup> = logn/εlogn = 1/ε. So O(m(1/ε)) which is just O(m)
 

- **2a.** Starting V | Ending V | k = 0 | k = 1 | k = 2 | total cost
- 0|0|0|0|0
- 0|1|-2|-2|-2
- 0|2|2|-1|-1
- 1|0|-2|-2|-2
- 1|1|0|0|0
- 1|2|1|1|1
- 2|0|2|-1|-1
- 2|1|1|1|1
- 2|2|0|0|0
 
- **2b.** APSP(i,j,1) is the shortest path from i to j only allowing nodes 0 and 1. APSP(i,j,2) is the shortest path from i to j allowing 0,1, and 2. So APSP(i,j,1) will be the same as APSP(i,j,2) if the paths connected to vertex 2 don't help lessen the total weight. However, APSP(i,j,2) will be shorter if there is a lighter path that will lessen the total weight and therefore allowing 2 may decrease the weight. The relationship is recursive as APSP(i,j,1) is a simplified version of APSP(i,j,2) and each level depends on the previous one. 

- **2c.** APSP(i,j,k) = min(APSP(i,j,k-1), APSP(i,k,k-1) + APSP(k,j,k-1))

- **2d.** O(|V|<sup>3</sup>), that is the amount of possible inputs for APSP(i,j,k).

- **2e.** Johnson is O(|V| * |E|log|E|). We prefer the new algorithm when |E|log|E| << |V|<sup>2</sup>


- **3a.** 


- **3b.**


- **3c.**
