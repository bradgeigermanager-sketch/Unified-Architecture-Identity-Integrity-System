Engine: AnomalyEngine

Inputs:
- identity.records
- expectedRecords
- domain.schemas
- identityGraph

Outputs:
- anomalies[]
- anomalySeverityScores[]
- anomalyExplanations[]

Modules:
- FeatureExtractor
- AnomalyClassifier
- SeverityScorer
- ExplanationGenerator

Anomaly Types:
- Inconsistency
- Completeness
- ExpectedRecord
- SyntheticIdentity
- EmergentIdentity
- SpatiotemporalCluster
