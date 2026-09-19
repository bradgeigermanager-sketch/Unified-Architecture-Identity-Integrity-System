DAG: RecordCollectionDAG
Purpose: Collect, normalize, validate, and assemble records.

Nodes:
- DomainCollectors
- RecordNormalizer
- RecordValidator
- ProvenanceAttacher
- RecordAssembler

Edges:
- DomainCollectors → RecordNormalizer
- RecordNormalizer → RecordValidator
- RecordValidator → ProvenanceAttacher
- ProvenanceAttacher → RecordAssembler

Execution Semantics:
- DomainCollectors gather raw records from all domains.
- RecordNormalizer aligns records to ontology schemas.
- RecordValidator enforces domain rules.
- ProvenanceAttacher adds lineage metadata.
- RecordAssembler produces unified record sets.

Integration Points:
- List Determination Engine
- ExpectedRecord Engine
- Anomaly Engine
- Consistency Engine
