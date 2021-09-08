# Introduction
## Enrol with FCA

To access the production environment, you must be a TPP authorised by the FCA or passported into the UK. Instructions for accessing our [Production APIs](./30-production.md).

## Enrol with Open Banking

You must also enrol onto the Open Banking Directory, the key component that enables TPPs to enrol with Open Banking and participate in account information and payment initiation transactions through APIs.

- [Enrol to Open Banking](https://www.openbanking.org.uk/wp-content/uploads/Enrolling-Onto-Open-Banking-Guide.pdf)


## Enrol with Tide using Dynamic Client Registration

This specification defines the APIs for a TPP to submit a Software Statement Assertion to an ASPSP for the purpose of creating OAuth clients that are registered with ASPSP.

Please see the following specifications we have aligned with:

- [Dynamic Client Registration (DCR) Specification](https://openbankinguk.github.io/dcr-docs-pub/v3.2/dynamic-client-registration.html): Use this specification to register your TPP client to use our APIs


## Sandbox

We recommend that you start off by accessing our [Sandbox](./sandbox.md).  

Our Sandbox fully reflects our production environment and provides an easy route to testing out your proposition.

## Production

To access the production environment, you must be a TPP authorised by the FCA or passported into the UK. Instructions for accessing our [Production APIs](./production.md). 


## API Documentation

Please see the following specifications we have aligned with:

- [Dynamic Client Registration (DCR) Specification](https://openbankinguk.github.io/dcr-docs-pub/v3.2/dynamic-client-registration.html): Use this specification to register your TPP client to use our APIs
- [Open ID Foundation's Financial Grade API (FAPI) Profile](https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_001.md): This specification enables user authentication of consents for open banking
- Open Banking API Specification: Based on Open Banking Read/Write API Specification v3.1.2, this specification describes the resources that are available on our service:
  - [Accounts & Transaction Information API](../../swagger/tide-ais-schema.yaml)
  - [Confirmation Of Funds API](../../swagger/tide-cbpii-schema.yaml)
  - [Payment Initiation API](../../swagger/tide-pis-schema.yaml)

### Screen scraping
<!-- theme: success -->

> For those third party providers wishing to screen scrape, or continue screen scraping against Tide's web channels please connect to `mci.openbanking.tide.co`
>
> Tide's international currency account information and international payments APIs are available via this modified customer interface.
>
> If you require test accounts please contact help@tide.co

