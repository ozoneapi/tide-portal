# Introduction

## Open Banking

The Tide Open Banking API is based on the Open Banking Standard which allows regulated Third Party Providers (TPPs) to access Account Information Services (AIS), Payment Initiation Services (PIS) and funds confirmation requests for member accounts. Access to these services on behalf of members is controlled by strong customer authentication within Tide apps as part of OpenID Connect authorisation flows. 

We currently support app->app, mobile-web->app, web->web authentication flows.

Tide is an FCA registered Account Servicing Payment Service Provider (ASPSP) who provides access to these services via the Open Banking standard. 

You can find out more about Open Banking here: [What is Open Banking](https://www.openbanking.org.uk/customers/what-is-open-banking/)

![get-started-icon](https://img.icons8.com/cotton/128/000000/launch-rocket.png)

## API Documentation

Please see the following specifications we have aligned with:

- [Dynamic Client Registration (DCR) Specification](): Use this specification to register your TPP client to use our APIs
- [Open ID Foundation's Financial Grade API (FAPI) Profile](): This specification enables user authentication of consents for open banking
- [Tide Open Banking API Specification](): Based on Open Banking Read/Write API Specification v3.1.2, this specification describes the resources that are available on our service


Account Information Services API
https://rs1.openbanking.api.tide.co:4501/v1.0/open-banking/v3.1/aisp/**
Confirmation of Funds API
https://rs1.openbanking.api.tide.co:4501/v1.0/open-banking/v3.1/cbpii/**
Payment initiation services API
https://rs1.openbanking.api.tide.co:4501/v1.0/open-banking/v3.1/pisp/**

### Screen scraping
<!-- theme: success -->

> For those third party providers wishing to screen scrape, or continue screen scraping against Tide's web channels please connect to `mci.openbanking.tide.co`
>
> Tide's international currency account information and international payments APIs are available via this modified customer interface.
>
> If you require test accounts please contact help@tide.co

## Getting Started

See our [Getting Started]() page for instructions on accessing our sandbox and production APIs

![support-icon](https://img.icons8.com/cotton/64/000000/technical-support.png)

