# Graph by Adjacency List
```python
class AdjListGraph:
	def __init__(self, node_count: n) -> None:
		self.edges: list[list[int]] = [[] for _ in range(n)]
		# self.edges[u] represents the nodes v that are connected to u
				
	def add_edge(self, u: int, v: int) -> None:
		# u, v are the ids of the nodes that the edge connects
		self.edges[u].append(v)
		self.edges[v].append(u)
```

# Graph by Adjacency Matrix
```python
class AdjMatrixGraph:
	def __init__(self, node_count: n) -> None:
		self.edges: list[list[int]] = [[] for _ in range(n)]
		# self.edges[u][v] is 1 if an edge exists between nodes u <-> v, 0 otherwise
	
	def add_edge(self, u: int, v: int) -> None:
		# u, v are the ids of the nodes that the edge connects
		self.edges[u][v] = 1
		self.edges[v][u] = 1
```

# Weighted Graph by Adjacency List
```python
class AdjListWeightedGraph:
	def __init__(self, node_count: n) -> None:
		self.edges: list[list[tuple[int, int]]] = [[] for _ in range(n)]
		# self.edges[u] list of a tuples v, w
		# which represents that there is an edge between nodes u, v with weight w
				
	def add_edge(self, u: int, v: int, w: int) -> None:
		# u, v are the ids of the nodes that the edge connects
		# w is the edge weight
		self.edges[u].append((v, w))
		self.edges[v].append((u, w))
```

# BFS
```python
from queue import Queue

def bfs(graph: Graph, initial_node: int, target_node: int) -> None:
	queue
```