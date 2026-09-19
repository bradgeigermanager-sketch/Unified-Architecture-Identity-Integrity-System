DAG: ConsistencyDAG
Purpose: Validate coherence across identity graph, records, expected records, anomalies, LLM outputs, tasks, procedures, tools, and execution results.

Nodes:
- SnapshotCollector
- LayerValidators
- ReportAggregator
- CorrectionGenerator

Edges:
- SnapshotCollector → LayerValidators
- LayerValidators → ReportAggregator
- ReportAggregator → CorrectionGenerator

Execution Semantics:
- SnapshotCollector captures system state.
- LayerValidators run domain-specific checks.
- ReportAggregator merges validation results.
- CorrectionGenerator produces repair tasks and updates.

Integration Points:
- Feedback Loop
- Task Orchestration DAG
- Engines: ExpectedRecord, Anomaly, Provenance
