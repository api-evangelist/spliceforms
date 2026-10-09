---
name: spliceforms-otp-authentication
description: Authenticate a bank customer with OTP and obtain an access token from Spliceforms Stitch Auth Services.
api: openapi/spliceforms-auth-services-openapi.yml
operations:
  - initiateAuthentication
  - resendOTP
  - verifyOTPAndIssueToken
generated: 2026-10-09
---

# spliceforms-otp-authentication

Authenticate a bank customer with OTP and obtain an access token from Spliceforms Stitch Auth Services.

## Steps

1. Call `initiateAuthentication` (POST /v1/otp/initiate) to start the OTP flow for the customer.
2. If the OTP does not arrive, call `resendOTP` (POST /v1/otp/resend).
3. Call `verifyOTPAndIssueToken` (POST /v1/otp/token) with the OTP to receive the token used by the other Stitch services.

## Rules

- The OpenAPI declares no securitySchemes; obtain a token via the OTP flow (Auth Services) where required.
- No idempotency keys are documented: do not blindly retry POSTs that create or submit records; check status first.
- Grounded only in operationIds from `openapi/spliceforms-auth-services-openapi.yml`.
