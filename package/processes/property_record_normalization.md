ProcessId: property_record_normalization

Preconditions:
- Property domain schema loaded
- Raw property records available
- Normalization tools available

Inputs:
- rawPropertyRecords[]
- propertySchema

Steps:
1. load(rawPropertyRecords)
2. validateSchemaCompliance(rawPropertyRecords, propertySchema)
3. standardizeFieldNames(rawPropertyRecords)
4. normalizeAddressFormats(rawPropertyRecords)
5. normalizeDateFormats(rawPropertyRecords)
6. normalizeOwnershipFields(rawPropertyRecords)
7. attachProvenance(rawPropertyRecords)
8. writeToGraph(normalizedRecords)

Postconditions:
- Property records normalized
- Provenance updated

Errors:
- Missing fields
- Invalid formats
- Conflicting ownership

Tools:
- PropertyNormalizer
- ProvenanceUpdater

Integration:
- RecordCollectionEngine
- ConsistencyEngine
