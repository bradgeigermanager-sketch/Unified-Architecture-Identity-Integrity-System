{
  "type": "object",
  "properties": {
    "identityId": { "type": "string" },
    "identityType": { "type": "string" },
    "attributes": { "type": "object" },
    "records": {
      "type": "array",
      "items": { "$ref": "#/definitions/Record" }
    },
    "anomalies": {
      "type": "array",
      "items": { "$ref": "#/definitions/Anomaly" }
    },
    "continuityMarkers": {
      "type": "array",
      "items": { "type": "string" }
    }
  }
}

{
  "type": "object",
  "properties": {
    "recordId": { "type": "string" },
    "domain": { "type": "string" },
    "recordType": { "type": "string" },
    "attributes": { "type": "object" },
    "provenance": { "$ref": "#/definitions/Provenance" },
    "timestamp": { "type": "string" },
    "confidenceScore": { "type": "number" }
  }
}

{
  "type": "object",
  "properties": {
    "source": { "type": "string" },
    "timestamp": { "type": "string" },
    "method": { "type": "string" },
    "confidence": { "type": "number" }
  }
}

{
  "type": "object",
  "properties": {
    "anomalyId": { "type": "string" },
    "anomalyType": { "type": "string" },
    "severity": { "type": "number" },
    "attributes": { "type": "object" },
    "relatedRecords": { "type": "array", "items": { "type": "string" } },
    "relatedDomains": { "type": "array", "items": { "type": "string" } }
  }
}

{
  "type": "object",
  "properties": {
    "taskId": { "type": "string" },
    "description": { "type": "string" },
    "domain": { "type": "string" },
    "inputs": { "type": "array", "items": { "type": "string" } },
    "outputs": { "type": "array", "items": { "type": "string" } },
    "validation": { "type": "string" },
    "dependencies": { "type": "array", "items": { "type": "string" } }
  }
}

{
  "type": "object",
  "properties": {
    "procedureId": { "type": "string" },
    "steps": { "type": "array", "items": { "type": "string" } },
    "preconditions": { "type": "array", "items": { "type": "string" } },
    "postconditions": { "type": "array", "items": { "type": "string" } },
    "errorHandling": { "type": "array", "items": { "type": "string" } },
    "requiredTools": { "type": "array", "items": { "type": "string" } }
  }
}

{
  "type": "object",
  "properties": {
    "toolId": { "type": "string" },
    "purpose": { "type": "string" },
    "inputs": { "type": "array", "items": { "type": "string" } },
    "outputs": { "type": "array", "items": { "type": "string" } },
    "integrationPoints": { "type": "array", "items": { "type": "string" } },
    "domain": { "type": "string" }
  }
}

{
  "type": "object",
  "properties": {
    "goalId": { "type": "string" },
    "description": { "type": "string" },
    "goalType": { "type": "string" },
    "tasks": { "type": "array", "items": { "type": "string" } },
    "subGoals": { "type": "array", "items": { "type": "string" } },
    "priority": { "type": "number" }
  }
}

