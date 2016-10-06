Some explanantions of my soluitions:
#1 ~ #4: The main structrue are exactly the same, except for the usage of data structure.
Differences are listerd below:

	#1: DFS - the firnge is a Stack  
	#2: BFS - the firnge is a Queue
	#3: UCS - the firnge is a PriorityQueue, 
	  	and the priority is defined by the total cost up to the current point: g(n)
	#4: A* - the firnge is a PriorityQueue, 
	  	and the priority is defined by the total cost up to the current point 
		plus the heuristic function to the goal: g(n)+h(n)



#5: The main idea of implementing this agent is to design a data type that include 
    the state representing which corners have been traversed.
    example: A designed state coulde be ((x,y),cornersTraversed)
             -- x is the x-coordinate of the current point being checked
             -- y is the y-coordinate of the current point being checked	
             -- cornersTraversed is a list to store which corners have been traversed

            when cornersTravesed includes all the corners,the goal state is reached.

#6: The idea of the heuristic fucntion is to separate the whole searching process into several stages.
    At each stages, I calculated the manhattan distance from the current point to the nearest corners in 
    the set of rest corners. If a corner has been visited, then it is poped from the list of rest corners.
    Repeat this until the set becomes empty.
    At the end, the heuristic function returns the sum of those distances calculated in each stage. 

#7:

#8: The main idea is to find the nearst dot by making use of manhattan distacne to estimate the nearset dot. 
    And when the goal state is found, I just use the information of the nearst dot to apply BFS to find the path  
    from the start point to the nearest dot.
     