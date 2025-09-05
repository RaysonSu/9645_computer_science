- talk about why graphs are useful
	- give examples
		- friendship graphs
		- relationships
		- maps
		- show some images of graphs
			- (note include some unconnected graphs)
	
- say what the formal definition is?
	- some nodes (a set V of nodes)
	- some edges connecting the nodes (a set E (or multiset) of pairs of nodes)

- terms:
	- node = some objects
	- edge = a relationship between two nodes
	- distance = length of the shortest path between 2 nodes

- talk about the usual implementations
	- assumes nodes are indexed by integers from 0 to |V| - 1
	- adj list
		- usual implementation when |E| ~ |V|
		- uses O(|E| + |V|) space
		- but removing edges may take up to O(|V|) time, because arrays are expensive
		- checking if two nodes are connected also requires O(|V|) time
		- see [[source#Graph by Adjacency List]] for example implementation
	- adj matrix
		- usual implementation when |E| ~ |V|<sup>2</sup>
		- sometimes convenient for doing maths on the graph
		- always uses O(|V|<sup>2</sup>) space
		- but allows for O(1) adding/removing edges
		- see [[source#Graph by Adjacency Matrix]] for example implementation

possible activities?
- How would you implement checking if an edge between two nodes existed?
- 