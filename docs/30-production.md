# Production

Below are the paths of our well-known endpoints for the production environment.

Our production authorisation server uses the strict profile defined above and testable in the Sandbox.

## Authorisation Server URLs
- OIDC Well Known endpoint: https://issuer1.openbanking.api.tide.co/.well-known/openid-configuration
- baseUrl: https://rs1.openbanking.api.tide.co:4501/v1.0

## Resource Server URLs
- Account Information Services API: https://rs1.openbanking.api.tide.co:4501/v1.0/open-banking/v3.1/aisp/**
- Confirmation of Funds API: https://rs1.openbanking.api.tide.co:4501/v1.0/open-banking/v3.1/cbpii/**
- Payment initiation services API: https://rs1.openbanking.api.tide.co:4501/v1.0/open-banking/v3.1/pisp/**