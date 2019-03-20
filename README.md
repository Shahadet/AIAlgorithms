# AIAlgorithms
Different Algorithm Implementation for Artificial Intelligence

Algorithms:

1. BFS
2. Bounded DFS
3. Iterative deepening DFS

4. A* with Heuristic functions h:
    o number of tiles out of place
    o minimum number of moves to reach the goal state (Manhattan distance)
    o heuristic H defined below
    o 2*C where C is the Chebyshev distance (see below)
   
    H is a combination of two measures:
    1. totdist: the "total distance" of the eight tiles in Pos (Pos is a board position) from their
    "home squares". We use the Manhattan distance (see below for the definition of the
    Manhattan distance) to calculate the distance of each tile from its home square. For
    example, in the starting position of the puzzle (a) in the figure below, totdist = 4.
    2. seq: the "sequence score" that measures the degree to which the tiles are already ordered
      in the current position with respect to the order required in the goal configuration. seq is
      computed as the sum of scores for each tile according to the following rules:
      o a tile in the centre scores 1;
      o a tile on a non-central square scores 0 if the tile is, in the clockwise direction,
      followed by its proper successor.
      o such a tile scores 2 if it is not followed by its proper successor.
      For example, for the starting position (a) of the puzzle in the figure below, seq = 6.
      The heuristic estimate, H, is computed as:
      H = totdist + 3*seq
    The "Manhattan distance" between 2 squares S1 and S2 is the distance between S1 and S2 in
    the horizontal direction (dx) plus the distance between S1 and S2 in the vertical direction (dy).
    We want to minimize the length of solutions. Therefore, we define the cost of all the arcs in the
    state space to equal 1.
    The Chebyshev distance, C, is defined as follows (using dx and dy defined above):
    C = max(dx,dy)

 Instruction to Execute:
 The program is developed with Java 8. However this code should work with older java version as well.
 Can be run with command(>javac assign2mha263.java		>java assign2mha263) or with any IDE
 The program will ask for two states, one is starting state another one is goal state and will provide all instruction at runtime
 You can test the whole application in a single run just by following instructions changing input,goal,algorithms.
 you can even turn on the log to see sequence of execution(optional)

 
  Example of execution(without log):
  For giving input simply provide values sequentially. For example if your input is:
	1 2 3
	8   4
	7 6 5
	---------
	Provide values as: 123804765
	Please enter starting(initial) state :
	283164705
	Please enter goal(final) state :
	123804765
	Please Specify the algorithm type:
	b : for BFS
	d : for Bounded DFS
	i : for Iterative DFS
	a*t : for a* with Tiles Mismatch function
	a*m : for a* with Manhatten distance function
	a*h : for a* with The Hurestic H function
	a*c : for a* with The Chebyshev function
	a* : for a* with all four function
	Please type: e for EXIT
	b
	Input:
	2 8 3
	1 6 4
	7   5
	---------
	Goal:
	1 2 3
	8   4
	7 6 5
	---------
	Solution States(Using BFS):
	2 8 3
	1 6 4
	7   5
	---------
	2 8 3
	1   4
	7 6 5
	---------
	2   3
	1 8 4
	7 6 5
	---------
	  2 3
	1 8 4
	7 6 5
	---------
	1 2 3
	  8 4
	7 6 5
	---------
	1 2 3
	8   4
	7 6 5
	---------
	Toatl Number of states Generated:61
	Program Run Time: [902884]Nano Second or [9.02884E-4] Second 
  
 
