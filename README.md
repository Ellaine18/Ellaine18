- import matplotlib.pyplot as plt
import networkx as nx

# Create a directed graph
G = nx.DiGraph()

# Add nodes
nodes = [
    "Financial Literacy", "Effective Budgeting and Saving", "Self-Efficacy",
    "Perceived Behavioral Control", "Attitudes Towards Financial Management",
    "Social Influences", "Family Expectations"
]

G.add_nodes_from(nodes)

# Add edges
edges = [
    ("Financial Literacy", "Effective Budgeting and Saving"),
    ("Effective Budgeting and Saving", "Self-Efficacy"),
    ("Effective Budgeting and Saving", "Perceived Behavioral Control"),
    ("Effective Budgeting and Saving", "Attitudes Towards Financial Management"),
    ("Attitudes Towards Financial Management", "Social Influences"),
    ("Attitudes Towards Financial Management", "Family Expectations")
]

G.add_edges_from(edges)

# Define positions for nodes
pos = {
    "Financial Literacy": (0, 3),
    "Effective Budgeting and Saving": (0, 2),
    "Self-Efficacy": (-1, 1),
    "Perceived Behavioral Control": (0, 1),
    "Attitudes Towards Financial Management": (1, 1),
    "Social Influences": (0.5, 0),
    "Family Expectations": (1.5, 0)
}

# Draw the graph
plt.figure(figsize=(10, 6))
nx.draw(G, pos, with_labels=True, node_size=3000, node_color="skyblue", font_size=10, font_weight="bold", arrows=True)
plt.title("Financial Literacy Hierarchy Diagram")
plt.show()

-
