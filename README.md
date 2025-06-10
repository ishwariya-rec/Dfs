# Dfs



---

# Depth First Search (DFS) Implementation in Python

# Using adjacency list representation for the graph

def dfs(graph, start, visited=None):
    if visited is None:
        visited = set()

  # Mark the current node as visited
  visited.add(start)
    print(start, end=' ')  # You can also store this in a list if needed

  # Recur for all the adjacent nodes
  for neighbor in graph[start]:
        if neighbor not in visited:
            dfs(graph, neighbor, visited)

  return visited

# Sample graph represented as an adjacency list
graph = {
    'A': ['B', 'C'],
    'B': ['D', 'E'],
    'C': ['F'],
    'D': [],
    'E': ['F'],
    'F': []
}

# Driver code
if __name__ == "__main__":
    print("Depth First Search starting from node A:")
    dfs(graph, 'A')

