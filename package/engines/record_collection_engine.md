Engine: RecordCollectionEngine

Modules:
- DomainCollectors
- RecordNormalizer
- RecordValidator
- ProvenanceAttacher
- RecordAssembler

Pipeline:
1. collectFromDomains()
2. normalizeRecords()
3. validateRecords()
4. attachProvenance()
5. assembleUnifiedRecordSet()

Outputs:
- unifiedRecords[]
- collectionReport
