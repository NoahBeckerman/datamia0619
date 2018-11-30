![IronHack Logo](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_d5c5793015fec3be28a63c4fa3dd4d55.png)

# Advanced Topic: Network Analysis

## Objectives

- Understand the basics of network/graph analysis
- Build graphs from scratch using the Python Networkx library
- Compute graph statistics and conduct basic network analysis
- Create graphs from existing data in pandas data frames
- Create data visualizations from network data
- Perform deeper analysis of network graphs
- Understand how to incorporate network analysis in your final project

## Graph Theory and Network Composition

Network analysis (also called graph analysis) is a very important, very useful, but often underrated part of data analytics. Its primary purpose is to examine relationships between entities. One of the most obvious targets for network analysis are social networks, where the entities are people and the relationships between them are based on whether someone is friends with (or has followed) someone else.

However, only applying network analysis to social networks is limiting and merely scratches the surface of what you can do with it. Networks are actually ubiquitous: they are everywhere. Look around you. Every object you see is an entity, and they can be connected to each other as part of a network based on anything they have in common - whether or not they belong to you, they are electronic, they are writing instruments, they are furniture, they are located in the same room, etc. When you practice thinking about connections in this way, then you start to see networks everywhere. This is the type of thinking you should utilize when analyzing networks.

[Graph theory](https://en.wikipedia.org/wiki/Graph_theory) is the study of mathematical structures called graphs which model the pairwise relationships between entities. Graph theory provides us with a mathematical foundation and tools with which we can analyze networks, since networks are essentially constructed from relationships between pairs of entities.

Whenever we define a graph, we define it in terms of its *nodes* and *edges*, and visually, they look like the image below. The nodes in the graph represent the entities in our network and the edges are visualized as lines that connect nodes where a relationship exists between the entities they represent.

![Graph Nodes and Edges](./images/graph-nodes-and-edges.png)

There are also two main types of graphs:

- **Directed** - there is a direction to the relationship (e.g. Person A follows Person B).
- **Undirected** - the relationship is nondirectional (e.g. Person A and Person B are friends).

[Networkx](https://networkx.github.io/documentation/stable/) is a Python library for performing network analysis. It has a variety of methods for building graph objects, computing graph statistics, running algorithms on them, and even visualizing them.

If you don't already have Networkx installed, you can pip install it as follows.

```bash
$ pip install networkx
```

Once it is installed, you can import it as follows. It is typically aliased to `nx`.

```python
import networkx as nx
```

From there, you can create a graph by using the `Graph` method.

```python
G = nx.Graph()
```

Once the graph is created, you can add nodes and edges to the graph using the respective `add_node` and `add_edge` methods.

```python
G.add_node(1)
G.add_nodes_from([2, 3])

G.add_edge(1, 2)
G.add_edges_from([(1, 2), (1, 3)])
```

These topics are covered in greater detail in the following tutorial and in the Networkx documentation:

- [PyCon 2018: Network Analysis Made Simple, Part 1 Tutorial](https://www.youtube.com/watch?v=HkbMUrgzwMs)
- [Networkx Documentation Tutorial](https://networkx.github.io/documentation/stable/tutorial.html)

You are highly encouraged to watch the *Network Analysis Made Simple* tutorial and work through the examples in the *Networkx Documentation Tutorial* so that you gain a solid understanding of network analysis and some practice using the Networkx library.

You should also try to complete the exercises in the *Networkx Basics Notebook* (up until the Tests section) that accompanies the *Network Analysis Made Simple* tutorial:

- [Network Analysis Made Simple: Networkx Basics Notebook](https://github.com/ericmjl/Network-Analysis-Made-Simple/blob/master/2-networkx-basics-student.ipynb)

## Analyzing Networks

Graph statistics

- Number of nodes
- Number of edges
- Average degree
- Density
- Diameter
- Average distance

Centrality metrics

- Betweenness
- Closeness
- Eigenvector
- Degree
- PageRank

## Building and Analyzing Graphs from Tabular Data

When analyzing networks from tabular data, there are typically three main things you can analyze:

- Entities (and their attributes)
- Relationships (and their attributes)
- Interactions (and their attributes)

Recall from previous lessons in the program that when data is structured in a tabular format, entities are typically represented by rows and attributes (or features) of the entities are typically represented by the columns in the table.

- Identifying entities
- Identifying & defining relationships
- Transforming data to graph structure
- Converting data frames to graphs
- Analyzing networks extracted from data

## Visualization of Network Data

- Network visualizations
    - Different layouts - spring, circular, etc.
- Other ways to visualize network data
    - Bar charts
    - Scatter plots
    - Line charts

## Deeper Analysis of Networks

- Subgraphs
- Hierarchical graphs
- Querying graphs
- Community detection
- Clustering

## Resources

- [Wikipedia: Graph Theory](https://en.wikipedia.org/wiki/Graph_theory)
- [PyCon 2018: Network Analysis Made Simple, Part 1 Tutorial](https://www.youtube.com/watch?v=HkbMUrgzwMs)
- [PyCon 2018: Network Analysis Made Simple, Part 2 Tutorial](https://www.youtube.com/watch?v=MRCLwmYTVpc)
- [Network Analysis Made Simple Github Repo](https://github.com/ericmjl/Network-Analysis-Made-Simple)
- [Networkx Documentation](https://networkx.github.io/documentation/stable/)
- [DataCamp Social Network Analysis Article](https://www.datacamp.com/community/tutorials/social-network-analysis-python)