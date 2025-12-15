---
layout: cd1
title: Identify Node Networks Code Listing
---
# IdentifyNodeNetworks

## Code Listing

<div markdown="1">
```

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
```
</div>
