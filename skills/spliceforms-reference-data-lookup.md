---
name: spliceforms-reference-data-lookup
description: Look up branches, geographies, codesets, consent definitions and banks needed to fill a Spliceforms application form.
api: openapi/spliceforms-data-services-openapi.yml
operations:
  - fetchBranchStates
  - fetchBranchCities
  - fetchBranches
  - fetchCodesets
  - get-v1-data-codesets-codes
  - fetchConsentDefinitions
  - get-v1-banks
  - get-v1-banks-branches
generated: 2026-10-09
---

# spliceforms-reference-data-lookup

Look up branches, geographies, codesets, consent definitions and banks needed to fill a Spliceforms application form.

## Steps

1. Narrow branches with `fetchBranchStates` → `fetchBranchCities` → `fetchBranches`.
2. List codesets with `fetchCodesets` and read values with `get-v1-data-codesets-codes`.
3. Get consent text to display with `fetchConsentDefinitions`.
4. For external pay-in accounts, use `get-v1-banks` and `get-v1-banks-branches`.

## Rules

- The OpenAPI declares no securitySchemes; obtain a token via the OTP flow (Auth Services) where required.
- No idempotency keys are documented: do not blindly retry POSTs that create or submit records; check status first.
- Grounded only in operationIds from `openapi/spliceforms-data-services-openapi.yml`.
