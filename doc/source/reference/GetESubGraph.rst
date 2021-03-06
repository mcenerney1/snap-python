GetESubGraph
''''''''''''

.. function:: GetESubGraph(Graph, EIdV)

Returns a subgraph of graph *Graph*, where *Graph* is an instance of :class:`TNEANet`. The resulting subgraph contains all the edges from *Graph* with edge IDs in *EIdV* and all the nodes that are connected by at least one edge in *EIdV*. Nodes and edges in the resulting subgraph have the same IDs as in *Graph*.

Parameters:

- *Graph*: :class:`TNEANet` network (input)
    A Snap.py network.

- *EIdV*: TIntV, a vector of ints (input)
    A vector of edge IDs in graph.

Return value:

- network
    A subgraph of *Graph* with *EIdV* edges.

The following example shows how to use :func:`GetESubGraph` with
:class:`TNEANet`::

    import snap

    Graph = snap.GenRndGnm(snap.PNEANet, 100, 1000)
    EIdV = snap.TIntV()
    for edge in Graph.Edges():
        EIdV.Add(edge.GetId())
    ESubGraph = snap.GetESubGraph(Graph, EIdV)
