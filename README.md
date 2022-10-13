# Matrix Visualization for Graphical Terminology Definition Generation Data

Even though graph neural networks show promising results in definition generation, understanding node relationships and visualizing patterns is challenging in graph structure due to its high complexity.

In our repository, we will focus on the below problems:
1. How to visualize terminology graph structure effectively?
2. How this visualization relates to the similarity of each pair of terminology definitions?

Dataset:
Graphine dataset - Graphine datase contains 2,010,648 terminology definition pairs organized in 227 graphs curated by different domain experts. Each vertex in each graph is associated with terminology and its definition. Each graph is structured from coarse to fine-grained terminologies. We receive the graphs in JSON files in the original dataset as terminologies with their immediate parents. The data will be transformed into matrix form with each cell having a node proximity score between row and column vertices.

Algorithms
1. Automatic vertex ordering
We will use the leaf order method for ordering vertices. The method first defines the distance between two vertices and then computes the ordering by constructing hierarchical clustering on the vertices. We define the distance between two vertices as the minimum number of edges between the vertices. Hierarchical clustering considers each vertex as a cluster and then iteratively combines two clusters that are close to each other. This returns an optimal order in which the vertices are to be ordered. Since this method requires no manual effort, it is highly efficient and scalable.

2. Computing definition similarity
There are many ways to define similarity between terminology definitions. For our study, we define two terminology definitions as similar when the definitions contain at least one non-stop word common between them.

Conclusion:
In this study, we show how we can effectively visualize large graph networks and how incorporating graph structures can help in different downstream tasks. We see that the clusters formed using the vertices node proximity relationship have high definition similarity. We conclude that terminology definition generation can benefit by using graph structures.

References:
1. Z. Liu, S. Wang, Y. Gu, R. Zhang, M. Zhang, and S. Wang. Graphine: A Dataset for
Graph-aware Terminology Definition Generation. EMNLP, 2021.
2. Z. Bar-Joseph, D. K. Gifford, and T. S. Jaakkola. Fast optimal leaf ordering for hierarchical
clustering. Bioinformatics, 2001. 

