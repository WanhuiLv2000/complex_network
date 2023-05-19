# complex network
This paper introduces the methods of community division and node importance ranking in social networks.
## requirements
pip install networkx

pip install community

pip install matplotlib

pip install pandas

pip install openpyxl
## experiments
Data is available from the Stanford Data Sets website
http://snap.stanford.edu/data/ego-Facebook.html
### cummunity detection
1.The Louvain algorithm was used to divide the Facebook social network, and the sub-community was visually analyzed by finding the inducer graph.And import the results into a table.https://github.com/WanhuiLv2000/complex_network/blob/main/detection.xlsx

partition=community_louvain.best_partition(G)

subgraph=G.subgraph()

2.Sub-community characteristics such as average degree, clustering coefficient, network transitivity, network diameter, and average shortest path are calculated.

nx.average_clustering()

nx.transitivity()

nx.diameter()

......

### Importance ordering
We use betweenness centrality,closeness centrality and degree centrality to calculate the importance of each node.And import the results into a table.

nx.betweenness_centrality()

nx.closeness_centrality()

nx.degree_centrality()

## results
It is divided into 16 communities, with nodes 107 and 348 ranked first.
