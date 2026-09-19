Class: Identity
Attributes:
- identityId: string
- identityType: string
- attributes: object
- records: Record[]
- anomalies: Anomaly[]
- continuityMarkers: string[]

Relationships:
- hasRecord
- hasAnomaly
- participatesInDomain
- hasGoal
