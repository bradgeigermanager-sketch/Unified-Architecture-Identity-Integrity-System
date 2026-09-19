type Identity {
  identityId: ID!
  identityType: String
  attributes: JSON
  records: [Record]
  anomalies: [Anomaly]
  continuityMarkers: [String]
}

type Record {
  recordId: ID!
  domain: String
  recordType: String
  attributes: JSON
  provenance: Provenance
  timestamp: String
  confidenceScore: Float
}

type Provenance {
  source: String
  timestamp: String
  method: String
  confidence: Float
}

type Anomaly {
  anomalyId: ID!
  anomalyType: String
  severity: Int
  attributes: JSON
  relatedRecords: [String]
  relatedDomains: [String]
}

type Task {
  taskId: ID!
  description: String
  domain: String
  inputs: [String]
  outputs: [String]
  validation: String
  dependencies: [String]
}

type Procedure {
  procedureId: ID!
  steps: [String]
  preconditions: [String]
  postconditions: [String]
  errorHandling: [String]
  requiredTools: [String]
}

type Tool {
  toolId: ID!
  purpose: String
  inputs: [String]
  outputs: [String]
  integrationPoints: [String]
  domain: String
}

type Goal {
  goalId: ID!
  description: String
  goalType: String
  tasks: [String]
  subGoals: [String]
  priority: Int
}

