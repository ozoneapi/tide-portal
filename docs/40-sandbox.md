# API Sandbox

Our API Sandbox contains a full simulation of our APIs but without connecting to any real customer accounts. Any developer can access this Sandbox using their own self signed certificates.

## Try our API in the Sandbox

We provide two sandboxes - a regulatory sandbox that fully reflects our production APIs and a _permissible_ sandbox that allows developers to access the APIs without strict FAPI compliance.

### Regulatory Sandbox

- Authorisation Server 1: Provides both strict and permissive client profiles in headless and non headless options.
- OIDC Well Known endpoint: https://ob-issuer1.sandbox.tide.co/.well-known/openid-configuration
- baseUrl: https://ob-api1.sandbox.tide.co:4501/v1.0

### Permissible Sandbox
- Authorisation Server 2: Provides a more permissive security profile is used to help TPP onboarding and learning
- OIDC Well Known endpoint: https://ob-issuer2.sandbox.tide.co/.well-known/openid-configuration
- baseUrl: https://ob-api2.sandbox.tide.co:4502/v1.0

## Sandbox User Accounts
| user | password |
|---|---|
| rora |	rora
| mits |	mits
| ivsa |	ivsa

