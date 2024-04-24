# project
import networkx as nx
import matplotlib.pyplot as plt

G = nx.Graph()
nodes = ['Alice', 'Bob', 'Charlie', 'Diana', 'Eve']
edges = [('Alice', 'Bob'), ('Alice', 'Charlie'), ('Bob', 'Diana'), ('Charlie', 'Diana'), ('Diana', 'Eve'), ('Alice', 'Eve'), ('Bob', 'Eve'), ('Charlie', 'Eve'), ('Alice', 'Diana')]
G.add_nodes_from(nodes)
G.add_edges_from(edges)
options = {
    'node_color': 'skyblue',
    'node_size': 2000,
    'width': 2,
    'edge_color': 'gray',
    'font_size': 10,
    'font_color': 'darkred',
    'with_labels': True
}
plt.figure(figsize=(8, 8))
nx.draw(G, **options)
plt.title("Simple Social Network Graph")
plt.show()
