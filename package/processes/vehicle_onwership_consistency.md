ProcessId: vehicle_ownership_consistency

Domains:
- Vehicle
- Insurance
- Residence

Steps:
1. retrieveVehicleRecords()
2. retrieveInsuranceRecords()
3. retrieveResidenceRecords()
4. normalizeAllRecords()
5. validateVIN()
6. validateInsuranceCoverage()
7. validateResidenceMatch()
8. updateGraph()
9. updateProvenance()

Tools:
- VehicleNormalizer
- InsuranceValidator
- ResidenceValidator
- ProvenanceUpdater
