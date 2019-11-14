# Domain-specific knowledge graph for recommendation.

The main goal of the project is to provide a technology intelligence platform for technology competitive analysis. We created technology space maps, in which nodes represent technology domains and edges denote the relationships between the technology domains, by applying different statistical methods, e.g., similarity measures, information theory, economic base metrics. It is a network-analytic based decision making tool.

## The main work have been published in the papers shown below:
1. [Measuring technological distance for patent mapping](https://doi.org/10.1002/asi.23664), Journal of the association for information science and technology 68(2):423-437.

2. [Filtering patent maps for visualization of diversification paths of inventors and organizations](https://doi.org/10.1002/asi.23780), Journal of the association for information science and technology 68(6):1551-1563.

3. [InnoGPS for data-driven exploration of design opportunities and directions: the case of Google driverless car project](https://doi.org/10.1115/1.4037680), Journal of mechanical design 139(11), 111416.

4. [The superior knowledge proximity measure for patent mapping](https://arxiv.org/pdf/1901.03925.pdf), arXiv, 2019.

## Main features:
1. Build technology road mapping for agents, like companies, individual inventors, etc., using the technology space map.

2. Provide economic metrics to evaluate the technology performance (e.g., coherence, diversification) based on agents’ technology portfolios and relationships between technology domains in technology space.

3. Recommend related whitespace technology domains for agents to explore, based on their technology portfolios.

4. Recommend possible technology development pathways using the network properties of technology space.

5. Automatically recommend a suitable graph for agents.

6. Recommend similar agents using their technology portfolios.

## Following work:

**This repository only shares some following work (shown below) after the published work. If you are interested in the methodology part or have questions/comments, please feel free to contact. Please also note that the networks shared in the repository can only be used for academic research purpose. **

1. Technology space map visualization. 

In previous studies, we used maximum spanning tree and technology expansion power to filter the relationships between technology domains, so that we can have a clear map visualization. Since the original networks are fully connected, it is difficult to visualize them directly using the existing network visualization tools. In the current work, we use t-SNE to visualize the networks in 2D dimension. t-SNE is very useful for visualizing high-dimensional data. In the experiment, we treat the weights as dimensional data. The result looks reasonable. 

2. Similar competitors recommendation. 

Previously, we used cosine similarity and soft cosine similarity to measure how similar between agents, and choose top-N competitors to the specific agent. According to the result obtained in the technology space map visualization, we decided to use dimension reduction methods to compare similarity between agents, e.g., using t-SNE. In the comparison, the correlation between t-SNE and soft cosine similarity (involving similarity between technology domains) is not high, which means that one of them might be useful for comparing the similarity of agents. The cosine similarity does not consider magnitude of vectors, which might not be able to extract the technology strength for different agents. The cosine similarity is more like a “direction” measure rather than a magnitude measure. We have only chosen some cases for testing, and the resulting plots obtained by t-SNE look more reasonable. 
