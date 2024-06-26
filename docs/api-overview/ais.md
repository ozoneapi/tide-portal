# AISP API Overview

The Account and Transaction API Profile describes the flows and common functionality for the Accounts and Transaction API, which allows an Account Information Service Provider ('AISP') to:

- Register an intent to retrieve account information by creating an "account access consent". This registers the data "permissions", expiration and historical period allowed for transactions / statements - that the customer (PSU) has consented to provide to the AISP; and
- Subsequently, retrieve account and transaction data.

This profile should be read in conjunction with a compatible Read/Write Data API Profile which provides a description of the elements that are common across all the Read/Write Data APIs, and compatible individual resources.

## Base URL
The base URL for all AIS APIs is: `https://rs1.openbanking.api.tide.co:4501/v1.0/open-banking/v3.1/aisp/**`

## Account Access Consents
[Account Access Consents API](/swagger/tide-ais-schema.yaml/paths/~1account-access-consents/post)

## Accounts
[Accounts API](/swagger/tide-ais-schema.yaml/paths/~1accounts/get)

Tide members will have one of the following accounts:
- E-money Business Wallet
- Business Current Account

## Balances
[Balances API](/swagger/tide-ais-schema.yaml/paths/~1accounts~1%7BAccountId%7D~1balances/get)

Balances shown in this endpoint include `Expected`, `InterimAvailable` and `InterimCleared`.

`Expected` balance is the value displayed most widely to our members within the Tide apps.

## Transactions
[Transactions API](swagger/tide-ais-schema.yaml/paths/~1accounts~1%7BAccountId%7D~1balances/get)

Pagination is supported on GET /accounts/{AccountId}/transactions end point with a page size of 2000 transactions.

Please note GET /transactions end point does not support pagination.

<!-- theme: danger -->
> ### Deprecation Warning
>
> GET /transactions end point will be deprecated as of 12:00am 01/02/2021

## Beneficiaries
[Beneficiaries API](/swagger/tide-ais-schema.yaml/paths/~1accounts~1%7BAccountId%7D~1beneficiaries/get)

Payment recipients are accessible via the Beneficiaries API. Payments are currently only permitted to pre-registered beneficiaries or one of the Member's other accounts (for account transfers). This API is useful when setting up payments.

<!-- theme: warning -->
>
> Tide does not support the "bulk" beneficiaries endpoint `GET /beneficiaries`

## Products
[Products API](/swagger/tide-ais-schema.yaml/paths/~1accounts~1%7BAccountId%7D~1product/get)

Tide currently offers Business Current Accounts and Business E-Money Accounts.

## Direct Debits
[Direct Debits API](/swagger/tide-ais-schema.yaml/paths/~1accounts~1%7BAccountId%7D~1direct-debits/get)

<!-- theme: warning -->
>
> Tide does not support the "bulk" direct debit endpoint `GET /direct-debits`

## Standing Orders
[Standing Orders API](/swagger/tide-ais-schema.yaml/paths/~1accounts~1%7BAccountId%7D~1standing-orders/get)

DateTime elements have been used so that there is consistency across all API endpoints using dates. However, for Standing Orders we only process based on the day element, therefore, the time portion of the DateTime element will be defaulted to 00:00:00+00:00.

Standing orders will only return `FirstPaymentAmount` which will be the same amount for the duration of the standing order.

## Scheduled Payments
[Scheduled Payments API](/swagger/tide-ais-schema.yaml/paths/~1accounts~1%7BAccountId%7D~1scheduled-payments/get)

DateTime elements have been used so that there is consistency across all API endpoints using dates. However, for Standing Orders we only process based on the day element, therefore, the time portion of the DateTime element will be defaulted to 00:00:00+00:00.

## Parties
[Parties API](/swagger/tide-ais-schema.yaml/paths/~1accounts~1%7BAccountId%7D~1parties/get)

In addition to Open Banking API specification, Tide have additional `SupplementaryData` in the following two end points responses.

| Name |	XPath | EnhancedDefinition |
|------|--------|--------------------|
| SupplementaryData <br/> 0..1 | `OBParty2. SupplementaryData` | Supplementary information		
| VatNumber         <br/>	0..1 | `OBParty2. SupplementaryData. VatNumber` | Account holders VAT number
| CompanyId         <br/> 0..1 | `OBParty2. SupplementaryData. CompanyId` |	Account holders company number as registered with companies house in the UK

## Statements
Statements API

<!-- theme: warning -->
>
> Tide does not support the following statement end points:
>
> - GET /accounts/{AccountId}/statements/{StatementId}
> - GET /accounts/{AccountId}/statements/{StatementId}/transactions
> - GET /statements