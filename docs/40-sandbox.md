

## API Sandbox

Our API Sandbox contains a full simulation of our APIs but without connecting to any real customer accounts. Any developer can access this Sandbox using their own self signed certificates.

Try our API in the Sandbox
Below are the paths of our well-known endpoints for the Sandbox environments.

Authorisation Server 1: Provides both strict and permissive client profiles in headless and non headless options.
OIDC Well Known endpoint: https://ob-issuer1.sandbox.tide.co/.well-known/openid-configuration
baseUrl: https://ob-api1.sandbox.tide.co:4501/v1.0
Security Profiles
Authorisation Server 2: Provides a more permissive security profile is used to help TPP onboarding and learning
OIDC Well Known endpoint: https://ob-issuer2.sandbox.tide.co/.well-known/openid-configuration
baseUrl: https://ob-api2.sandbox.tide.co:4502/v1.0
Security Profiles
Sandbox Testing Info
Sandbox User Accounts
user	password
rora	rora
mits	mits
ivsa	ivsa
Production API
Our Production API can be accessed by any authorised TPP who has enrolled on the OBIE Directory and has production Open Banking certificates.

Below are the paths of our well-known endpoints for the production environment.

Authorisation Server: Our production authorisation server uses the strict profile defined above and testable in the Sandbox.
OIDC Well Known endpoint: https://issuer1.openbanking.api.tide.co/.well-known/openid-configuration
baseUrl: https://rs1.openbanking.api.tide.co:4501/v1.0
Security profile is as defined above