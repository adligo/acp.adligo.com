---
layout: cd1
title: Identify Node Networks
---
# IdentifyNodeNetworks

1.3.6.1.4.1.33097.7.0.3.60002


          
Given a [Digraph#1.3.6.1.4.1.33097.1.0.14](https://adligo.github.io/papers.adligo.com/data_structures/abstract/Graphs.html) \G=(V, E)\ with \V\ Vertices(aka [Nodes#1.3.6.1.4.1.33097.1.0.12.0](https://adligo.github.io/papers.adligo.com/data_structures/abstract/NodeNetworks.html#nodes)) and \E\ [Edges#1.3.6.1.4.1.33097.1.0.12.1](https://adligo.github.io/papers.adligo.com/data_structures/abstract/NodeNetworks.html#edges).  Identify the number of [NodeNetworks#1.3.6.1.4.1.33097.1.0.12](https://adligo.github.io/papers.adligo.com/data_structures/abstract/NodeNetworks).


## Pre-Requisite Problems

We suggest you solve this problem first;
[IdentifyUpstreamOriginNodes#1.3.6.1.4.1.33097.7.0.3.60001](IdentifyUpstreamOriginNodes.md)

## Code Listing

<code>
class AdjacencyMapMutant:
    def __init__(self, directional: bool):
        self.directional = directional
        # map of character to set of character
        self.nodeIdsToEdgeNodeIds = {}

    def isDirected(self):
        return self.directional

    def addNode(self, nodeId: str):
        self.nodeIdsToEdgeNodeIds.setdefault(nodeId, set())

    def addEdge(self, fromNodeId: str, toNodeId: str):
        self.nodeIdsToEdgeNodeIds.setdefault(fromNodeId, set()).add(toNodeId)
        self.addNode(toNodeId)

    def getAllNodes(self):
        return self.nodeIdsToEdgeNodeIds.keys()

    def getEdges(self, fromNodeId: str):
        return self.nodeIdsToEdgeNodeIds[fromNodeId]
        
def identifyNodeNetworks(map: AdjacencyMapMutant) -> int:
    #Your code goes here
    return 0
</code>

# Performance

### Time Cost O(v log log v)

### Space Cost O(v)

# Examples

### Example A / #001
##### Input

<code>
a → d
e → f
d → f
</code>

##### Output

<code>
1
</code>

### Example B / #002
##### Input

<code>
a → d
c → f
d → z
</code>

##### Output

<code>
3
</code>

