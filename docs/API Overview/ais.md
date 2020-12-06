# AISP API Overview

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

<!-- theme: warning -->
> ### Deprecation Warning
>
> GET /transactions end point will be deprecated as of 12:00am 01/02/2021

## Beneficiaries
[Beneficiaries API](/swagger/tide-ais-schema.yaml/paths/~1accounts~1%7BAccountId%7D~1beneficiaries/get)

Payment recipients are accessible via the Beneficiaries API. Payments are currently only permitted to pre-registered beneficiaries or one of the Member's other accounts (for account transfers). This API is useful when setting up payments.

Tide does not support the "bulk" beneficiaries endpoint `GET /beneficiaries`

## Products
[Products API](/swagger/tide-ais-schema.yaml/paths/~1accounts~1%7BAccountId%7D~1product/get)

Tide currently offers Business Current Accounts and Business E-Money Accounts.

Direct Debits
Direct Debits API

Tide does not support the following direct debits end points:

GET /directdebits (bulk end point)
Standing Orders
Standing Orders API

DateTime elements have been used so that there is consistency across all API endpoints using dates. However, for Standing Orders we only process based on the day element, therefore, the time portion of the DateTime element will be defaulted to 00:00:00+00:00.

Standing orders will only return FirstPaymentAmount which will be the same amount for the duration of the standing order.

Scheduled Payments
Scheduled Payments API

DateTime elements have been used so that there is consistency across all API endpoints using dates. However, for Standing Orders we only process based on the day element, therefore, the time portion of the DateTime element will be defaulted to 00:00:00+00:00.

Parties
Parties API

Please note that in addition to Open Banking API spec in the above link Tide have an additional section on the following two end points:

GET /accounts/{AccountId}/parties
GET /accounts/{AccountId}/party
Name	Occurrence	XPath	EnhancedDefinition	Class
SupplementaryData	0..n	OBParty2/ SupplementaryData		
vatNumber	0..1	OBParty2/SupplementaryData/vatNumber	Account holders VAT number	String
companyId	0..1	OBParty2/ SupplementaryData/ companyId	Account holders company number as registered with companies house in the UK	String
Statements
Statements API

Tide does not support the following statement end points:

GET /accounts/{AccountId}/statements/{StatementId}
GET /accounts/{AccountId}/statements/{StatementId}/transactions
GET /statements
Endpoints
The API endpoints for these resources are given below.

They can be accessed from the following baseUrl: https://rs1.openbanking.api.tide.co:4501/v1.0/open-banking/v3.1/aisp/**