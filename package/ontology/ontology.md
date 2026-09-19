Ontology Version: 1.0

Top-Level Classes:
- Identity
- Record
- Domain
- Anomaly
- Task
- Procedure
- Tool
- Goal

Relationships:
- Identity → Record (hasRecord)
- Identity → Anomaly (hasAnomaly)
- Record → Provenance (hasProvenance)
- Domain → Record (producesRecord)
- Goal → Task (requiresTask)
- Task → Procedure (implementedBy)
- Procedure → Tool (requiresTool)
