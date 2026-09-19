ProcessId: employment_verification

Domains:
- Education
- Licensing
- Corporate
- Tax

Steps:
1. retrieveEmploymentClaims()
2. retrieveEducationRecords()
3. retrieveLicensingRecords()
4. retrieveCorporateFilings()
5. retrieveTaxFilings()
6. normalizeAllRecords()
7. alignEmploymentDates()
8. validateRequiredCertifications()
9. validateTaxFilings()
10. updateGraph()
11. updateProvenance()

Tools:
- EducationNormalizer
- LicensingValidator
- CorporateValidator
- TaxValidator
- ProvenanceUpdater
