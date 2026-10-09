---
name: spliceforms-application-form-capture
description: Capture, validate and submit a bank application form (e.g. fixed deposit) with Spliceforms Stitch Capture Services.
api: openapi/spliceforms-capture-services-openapi.yml
operations:
  - initiateApplication
  - saveAccount
  - saveAccountNomination
  - savePayinPreferences
  - saveConsents
  - initiatePayin
  - fetchPayinStatus
  - validateApplicationForm
  - submitApplicationForm
  - fetchApplicationStatus
generated: 2026-10-09
---

# spliceforms-application-form-capture

Capture, validate and submit a bank application form (e.g. fixed deposit) with Spliceforms Stitch Capture Services.

## Steps

1. Call `initiateApplication` (POST /v1/application-forms) to get an applicationId.
2. Save account preferences with `saveAccount`, then nomination with `saveAccountNomination`.
3. Save pay-in preferences with `savePayinPreferences` and consents with `saveConsents`.
4. Start payment with `initiatePayin` and poll `fetchPayinStatus`.
5. Call `validateApplicationForm`, fix reported issues, then `submitApplicationForm`.
6. Track progress with `fetchApplicationStatus`.

## Rules

- The OpenAPI declares no securitySchemes; obtain a token via the OTP flow (Auth Services) where required.
- No idempotency keys are documented: do not blindly retry POSTs that create or submit records; check status first.
- Grounded only in operationIds from `openapi/spliceforms-capture-services-openapi.yml`.
