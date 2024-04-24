# project
import networkx as nx
import matplotlib.pyplot as plt

# Create a new graph
G = nx.Graph()

# Adding nodes
G.add_node("Alice")
G.add_node("Bob")
G.add_node("Charlie")
G.add_node("Diana")
G.add_node("Eve")

# Adding edges
G.add_edge("Alice", "Bob")
G.add_edge("Alice", "Charlie")
G.add_edge("Bob", "Diana")
G.add_edge("Charlie", "Diana")
G.add_edge("Diana", "Eve")

# Add more nodes and edges to enrich the graph
G.add_edges_from([("Alice", "Eve"), ("Bob", "Eve"), ("Charlie", "Eve"), ("Alice", "Diana")])

# Draw the graph
nx.draw(G, with_labels=True, node_color='skyblue', node_size=2000, edge_color='k', font_size=10, font_color="darkblue")

# Display the plot
plt.show()
