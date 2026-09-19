Engine: FeedbackLoop

Modules:
- FeedbackCollector
- FeedbackAnalyzer
- UpdateGenerator
- UpdateApplier

Inputs:
- taskResults
- procedureOutcomes
- consistencyReport
- anomalyDeltas
- expectedRecordDeltas
- provenanceDeltas

Outputs:
- goalUpdates[]
- newGoals[]
- procedureUpdates[]
- toolUpdates[]
- modelUpdates[]
- followUpTasks[]
