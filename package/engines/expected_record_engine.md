Engine: ExpectedRecordInferenceEngine

Inputs:
- identity.attributes
- domain.rules
- population.norms
- lifecycle.stage
- crossDomain.correlations

Outputs:
- expectedRecords[]
- missingExpectedRecords[]
- expectedRecordExplanations[]

Modules:
- ExpectedRecordClassifier
- ExpectedRecordGenerator
- ExpectedRecordComparator

Rules:
- Expected records must align with domain schemas.
- Expected records must reflect lifecycle stage.
- Expected records must reflect population norms.
