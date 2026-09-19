Domain Procedures
Domain procedures operate inside a single domain and ensure correctness, completeness, and consistency.

Procedure: Property Record Normalization
Purpose: Normalize property records into unified schema.

Preconditions:

Property domain schema loaded

Raw property records available

Steps:

Retrieve raw property records

Validate schema compliance

Standardize field names

Normalize address formats

Normalize date formats

Normalize ownership fields

Attach provenance

Write normalized record to graph

Postconditions:

Property records normalized

Provenance updated

Errors:

Missing fields

Invalid formats

Conflicting ownership

Procedure: Vehicle Registration Verification
Purpose: Verify vehicle registration and insurance.

Steps:

Retrieve vehicle registration

Retrieve insurance records

Validate VIN consistency

Validate registration dates

Validate insurance coverage

Update identity graph

Update provenance

Procedure: Utility Account Validation
Purpose: Validate utilities for a residence.

Steps:

Retrieve utility accounts

Validate address match

Validate service dates

Validate provider consistency

Update graph

Update provenance
