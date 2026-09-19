ProcessId: graph_hygiene

Steps:
1. scanGraphForOrphanNodes()
2. scanGraphForInvalidEdges()
3. scanGraphForStaleRecords()
4. removeInvalidNodes()
5. removeInvalidEdges()
6. updateGraph()

Tools:
- GraphValidator
- GraphCleaner
