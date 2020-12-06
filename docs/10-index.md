# Introduction

## Open Banking

The Tide Open Banking API is based on the Open Banking Standard which allows regulated Third Party Providers (TPPs) to access Account Information Services (AIS), Payment Initiation Services (PIS) and funds confirmation requests for member accounts. Access to these services on behalf of members is controlled by strong customer authentication within Tide apps as part of OpenID Connect authorisation flows. 

We currently support app->app, mobile-web->app, web->web authentication flows.

Tide is an FCA registered Account Servicing Payment Service Provider (ASPSP) who provides access to these services via the Open Banking standard. 

You can find out more about Open Banking here: [What is Open Banking](https://www.openbanking.org.uk/customers/what-is-open-banking/)

## API Documentation

Please see the following specifications we have aligned with:

- [Dynamic Client Registration (DCR) Specification](https://openbankinguk.github.io/dcr-docs-pub/v3.2/dynamic-client-registration.html): Use this specification to register your TPP client to use our APIs
- [Open ID Foundation's Financial Grade API (FAPI) Profile](https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_001.md): This specification enables user authentication of consents for open banking
- Open Banking API Specification: Based on Open Banking Read/Write API Specification v3.1.2, this specification describes the resources that are available on our service:
  - [Accounts & Transaction Infomration API](../swagger/tide-ais-schema.yaml)
  - [Confirmation Of Funds API](../swagger/tide-cbpii-schema.yaml)
  - [Payment Initiation API](../swagger//tide-pis-schema.yaml)

## Getting started

We recommend that you start off by accessing our [Sandbox](./40-sandbox.md). 

Our Sandbox fully reflects our production environment and provides an easy route to testing out your proposition.

To access the production environment, you must be a TPP authorised by the FCA or passported into the UK. Instructions for accessing our Production APIs are [here](./30-production.md).

### Screen scraping
<!-- theme: success -->

> For those third party providers wishing to screen scrape, or continue screen scraping against Tide's web channels please connect to `mci.openbanking.tide.co`
>
> Tide's international currency account information and international payments APIs are available via this modified customer interface.
>
> If you require test accounts please contact help@tide.co

## Getting Started

See our [Getting Started]() page for instructions on accessing our sandbox and production APIs
