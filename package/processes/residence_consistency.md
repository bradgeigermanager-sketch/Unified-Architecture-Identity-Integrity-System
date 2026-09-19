ProcessId: residence_consistency

Domains:
- Property
- Utilities
- Communications

Steps:
1. retrievePropertyRecords()
2. retrieveUtilityRecords()
3. retrieveCommunicationsBilling()
4. normalizeAllRecords()
5. alignAddressFields()
6. alignDateFields()
7. detectMismatches()
8. reconcileMismatches()
9. updateGraph()
10. updateProvenance()

Tools:
- PropertyNormalizer
- UtilityNormalizer
- CommunicationsNormalizer
- ReconciliationTool
- ProvenanceUpdater
