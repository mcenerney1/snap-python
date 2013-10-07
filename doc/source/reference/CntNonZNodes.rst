CntNonZNodes 
''''''''''''

.. function:: CntNonZNodes (Graph) 

Returns the number of nodes with degree greater than 0.

Parameters:

- *Graph*: graph (input)
    A Snap.py graph or a network

Return value: 

- int

The following example shows how to calculate the number of non-zero nodes for graphs
:class:`TNGraph`, :class:`TUNGraph`, and :class:`TNEANet`::

    import snap

    Graph = snap.GenRndGnm(snap.PNGraph, 100, 1000)
    CntNonZNodes = snap.CntNonZNodes (Graph)

    Graph = snap.GenRndGnm(snap.PUNGraph, 100, 1000)
    CntNonZNodes = snap.CntNonZNodes (Graph)

    Graph = snap.GenRndGnm(snap.PNEANet, 100, 1000)
    CntNonZNodes = snap.CntNonZNodes (Graph)

