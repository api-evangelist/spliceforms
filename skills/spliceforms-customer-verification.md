---
name: spliceforms-customer-verification
description: Verify a customer UPI VPA or bank account, fetch existing nominees and calculate FD maturity via Spliceforms Stitch Inquiry Services.
api: openapi/spliceforms-inquiry-services-openapi.yml
operations:
  - verifyCustomerVpa
  - verifyCustomerBankAccount
  - getCustomerAccountNominees
  - calculateFDMaturity
generated: 2026-10-09
---

# spliceforms-customer-verification

Verify a customer UPI VPA or bank account, fetch existing nominees and calculate FD maturity via Spliceforms Stitch Inquiry Services.

## Steps

1. Verify a pay-in/pay-out VPA with `verifyCustomerVpa` or a bank account with `verifyCustomerBankAccount`.
2. Pre-fill nomination using `getCustomerAccountNominees`.
3. Show expected returns with `calculateFDMaturity`.

## Rules

- The OpenAPI declares no securitySchemes; obtain a token via the OTP flow (Auth Services) where required.
- No idempotency keys are documented: do not blindly retry POSTs that create or submit records; check status first.
- Grounded only in operationIds from `openapi/spliceforms-inquiry-services-openapi.yml`.
