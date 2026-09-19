Engine: ConsistencyEngine

Layers:
- identityGraph
- records
- expectedRecords
- anomalies
- llmOutputs
- tasks/procedures/tools
- executionResults

Modules:
- SnapshotCollector
- LayerValidators
- ReportAggregator
- CorrectionGenerator

Outputs:
- consistencyReport
- correctionTasks[]
