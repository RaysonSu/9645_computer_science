r- talk about why graphs are useful
	- give examples
		- friendship graphs
		- relationships
		- maps
		- show some images of graphs
			- (note include some unconnected graphs)
	
- say what the formal definition is?
	- some nodes (a set V of nodes)
	- some edges connecting the nodes (a set E (or multiset) of pairs of nodes)

- talk about the usual implementations
	- adj list
		- assumes nodes are indexed by integers from 0 to |V| - 1
		- usual implementation when |E| ~ |V|
		- uses O(|E| + |V|) space
		- but adding/removing edges may take up to O(|V|) time, because lists
		- ```
		    # implementation
		    
		    class Graph:
			    def __init__(self, node_count: n) -> None:
			        self.edges: list[list[int]] = [[] for _ in range(n)]
			        # self.edges[u] represents the 
				
				def add_edge(self, u: int, v: int) -> None:
					# u, v are the ids of the nodes that the edge connects
				    self.edges[u].append(v)
				    self.edges[v].append(u)
		  ```
	- adj matrix
		- usual implementation when |E| ~ |V|<sup>2</sup>
		- always uses O(|V|<sup>2</sup>) space
		- but allows for O(1) adding/removing edges
		- ```
		    # implementation
		    
		    class Graph:
			    def __init__(self, node_count: n) -> None:
			        self.edges: list[list[int]] = [[] for _ in range(n)]
				
				def add_edge(self, u: int, v: int) -> None:
					# u, v are the ids of the nodes that the edge connects
				    self.edges[u].append(v)
				    self.edges[v].append(u)
		  ```