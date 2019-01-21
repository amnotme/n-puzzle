# N-Puzzle

###  The project  
  
  The goal of this project is to solve the N-puzzle game using the A (star)   
search algorithm or one of its variants  

  You start with board of N x N cells.  One of these cells is empty, the others  
will contain numbers from 1 to ((N x N) - 1) and that are of unique distance  
in the puzzle.  

  The search algorithm will find valid sequence of moves in order to reach  
the final state in a "snail solution" fashion.

  The solving algorithm time constraint will be that of a reasonable  
performance:  Taking a few seconds to solve a 3-puzzle is pusshing it,  
ten seconds is unacceptable.  

  The only move you can do in an N-puzzle is to swap the empty cell with one  
of its neighbors excluding cells diagonally placed.  Imagine you're sliding  
a block with a number on it.  

###  15-puzzle spiral solution  

![15-puzzle spiral solution](/images/15_puzzle.svg.png)  

### Things to do  

  The end goal is to implement the A\* search algorithm (or one of its variants)  
to solve an N-puzzle, with the following constraints:  

- [ ] You have to manage different puzzle sizes (3,4,5,17,etc...).  The higher  
your program can manage, the better.  :+1  
- [ ] You have to manage both randomly determined states (of your own generation)
, or input files that specify a starting board.  
- [ ] The cost associated with each transition is always 1.  
- [ ] The user must be able to choose at __LEAST__ 3 (relevant) heuristic functions. 
The __Manhattan-distance__ heuristic is mandatory, the other two are up to you. 
- [ ] At the end of the search, the program has to provide the following values:  
	- [ ] Total number of states ever selected in the 'opened' set (complexity in time).  
	- [ ] Max number of states ever represented in memory at the same time during the search (complexity in size).  
	- [ ] Number of moves required to transition from the initial state to the final state, according to the search.  
	- [ ] The ordered sequence of states that make up the solution, according to the search.  
	- [ ] The puzzle may be unsolvable, in which case you have to inform the user and exit.  

### Language constraints  

	You are free to use whatever language you want, but keep in mind that some  
	languages are more time and space-efficient than others, so your choice in languagaes  
	may influence the performances of your program.  

###  Further explanation on A\*
	
  A\* is an informed search algorithm or a BFS.  It is formulated in terms of  
weighted graphs: starting from a specific node of a graph, it aims to find  
to the give goal node having the smallest cost (least distance travelled, 
shortest time, etc.).  Maintained by a tree of paths originating at the start  
node and extending those paths one edge at a time until its termination criterion  
is satisfied.  

  A\* selects the path that minimizes  ```f(n) = g(n) + h(n)```  
```g(n)``` is the cost of the path from the start node to ```n```  
```h(n)``` is a heuristic function that estimates the cost of the cheapest path  
from ```n``` to the goal. A* terminates when the path it chooses to extend is a   
path from start to goal or if there are no paths eligible to be extended.  The  
heuristic function is problem-specific.  if the heuristic function is ```admissible```  
, meaning that it never overestimates the actual cost to get to the goal.  A*  
is __guaranteed__ to return a least-cost path from start to goal.   
	


### Author  

```lhernand```  


