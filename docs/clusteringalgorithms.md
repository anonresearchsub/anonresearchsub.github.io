---
layout: default
title: Clustering Algorithms
nav_order: 4
has_children: false
permalink: /docs/clusteringimplementation
---

# Clustering Implementation
---

#### Bunch

Bunch implementation and extension for the consensus-based decomposition approach: [zip](/assets/data/Bunch-source.zip).  
Alternatively, the Bunch clustering approach can be executed using a jar file: [jar](/assets/data/Bunch-jar.zip).

**To run the jar file:**\
`java -cp Bunch.jar bunch.RunBunch <relationship graph: file in .csv format> <consensus groups: file in .txt format> <population size: integer> <output dir: directory path>`

Inputs:
- The `relationship graph` must be a CSV file. Specifically, each line represents a relationship and must be formatted as follows: `[caller class],[callee class],[relationship weight]`.
- The `consensus groups` in TXT format contains all the elements in the relationship graph that you wish to lock together during the clustering process. Each line represents a consensus group and must be formatted as follows: `SS('GROUP_NAME'.ss) = entity0, entity1, entity2...`. 
  - Note: if you wish to define NO consensus groups, then input an empty txt file. 
- The `population size` is parameter used to optimize the clustering. The higher the population size, the better the clustering result. 
- The `output dir` is the directory path where the results will be saved. 

\
*Examples:*
* To produce the by-static decomposition, execute with the static relationships graph and no consensus groups.
* To produce the consensus-based decomposition, execute with the combined weighted relationship graph with consensus groups.


#### Spectral Clustering

Spectral clustering implementation: [zip](/assets/data/Spectral-source.zip).  

Execute the `run_cosnensus_spectral_clustering.py` script with the following arguments:
* `--relationship-graph`\*: relationship graph in CSV format
* `--output`\*: output destination
* `--num-of-cluster`\*: number of clusters *k*
* `--consensus-groups`: file containing the consensus groups (i.e. groups of entities that should be locked together during clustering) in TXT format. If this is not provided, then no entities are locked together.
  * *Note*: this argument is required to produce the consensus-based decomposition
* `--normalize`: boolean to indicate whether the graph should be normalized before clustering. If the graph is already normalized, set to false.
* `--directed`: boolean to indicate whether the graph is directed. This should be set to true for static and combined weighted relationship graphs, and false for name relationship graphs.