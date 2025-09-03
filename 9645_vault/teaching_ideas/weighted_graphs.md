prereqs: 
- [[unweighted_graphs]]

rationale:
- some edges in graphs have more information
- like maps between nodes have distances
- problem: unweighted graphs can't store this information
- solution: make edges have a number called the "weight"

implementation: 
- adj list w/ weights

tasks:
- modify the adj list implementation in [[unweighted_graphs]] to add weights
	- solution in [[source#Weighted Graph by Adjacency List]]
- why would an adj matrix not be sutiable for weighted graphs?