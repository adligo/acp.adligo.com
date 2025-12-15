---
layout: cd1
title: Identify Upstream Origin Nodes
---

# IdentifyUpstreamOriginNodes

Id 1.3.6.1.4.1.33097.7.0.3.60001

Given a [Digraph#1.3.6.1.4.1.33097.1.0.14](https://adligo.github.io/papers.adligo.com/data_structures/abstract/Graphs.html) `G=(V, E)` with `V` Vertices(aka [Nodes#1.3.6.1.4.1.33097.1.0.12.0](https://adligo.github.io/papers.adligo.com/data_structures/abstract/NodeNetworks.html#nodes)) and `E` [Edges#1.3.6.1.4.1.33097.1.0.12.1](https://adligo.github.io/papers.adligo.com/data_structures/abstract/NodeNetworks.html#edges).  Identify the number of [UpstreamOriginNodes#1.3.6.1.4.1.33097.1.0.13.1](https://adligo.github.io/papers.adligo.com/data_structures/abstract/DirectedNodeNetworks.html#upstreamoriginnodes).

The data will be provided in pairs of letters, each letter representing a [NodeId#1.3.6.1.4.1.33097.1.0.12.0.0](https://adligo.github.io/papers.adligo.com/data_structures/abstract/NodeNetworks.html#nodeids).  In addition, an AdjacencyMap class will be provided as follows.


## [Code Listing](IdentifyUpstreamOriginNodesCodeListing.md)

# Performance

### Time Cost O(v log log v)

### Space Cost O(v)

# Examples

### Example A / #001
##### Input

<div class="language-plaintext highlighter-rouge">
<pre class="highlight"><code>
a → d
e → f
d → f
</code></pre></div>

##### Output

<div class="language-plaintext highlighter-rouge">
<pre class="highlight"><code>
2
</code></pre></div>

### Example B / #002
##### Input

<div class="language-plaintext highlighter-rouge">
<pre class="highlight"><code>
a → d
d → f
d → h
</code></pre></div>

##### Output

<div class="language-plaintext highlighter-rouge">
<pre class="highlight"><code>
1
</code></pre></div>

