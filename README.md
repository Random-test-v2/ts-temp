# openapi

Developer-friendly & type-safe Typescript SDK specifically catered to leverage *openapi* API.

[![Built by Speakeasy](https://img.shields.io/badge/Built_by-SPEAKEASY-374151?style=for-the-badge&labelColor=f3f4f6)](https://www.speakeasy.com/?utm_source=openapi&utm_campaign=typescript)
[![License: MIT](https://img.shields.io/badge/LICENSE_//_MIT-3b5bdb?style=for-the-badge&labelColor=eff6ff)](https://opensource.org/licenses/MIT)


<br /><br />
> [!IMPORTANT]
> This SDK is not yet ready for production use. To complete setup please follow the steps outlined in your [workspace](https://app.speakeasy.com/org/flexprice/prod). Delete this section before > publishing to a package manager.

<!-- Start Summary [summary] -->
## Summary

Flexprice API: Flexprice API provides billing, metering, and subscription management for SaaS and usage-based products. Use it to manage customers, plans, invoices, payments, usage events, and entitlements. Authenticate with an API key in the x-api-key header.
<!-- End Summary [summary] -->

<!-- Start Table of Contents [toc] -->
## Table of Contents
<!-- $toc-max-depth=2 -->
* [openapi](#openapi)
  * [SDK Installation](#sdk-installation)
  * [Requirements](#requirements)
  * [SDK Example Usage](#sdk-example-usage)
  * [Authentication](#authentication)
  * [Available Resources and Operations](#available-resources-and-operations)
  * [Standalone functions](#standalone-functions)
  * [Retries](#retries)
  * [Error Handling](#error-handling)
  * [Custom HTTP Client](#custom-http-client)
  * [Debugging](#debugging)
* [Development](#development)
  * [Maturity](#maturity)
  * [Contributions](#contributions)

<!-- End Table of Contents [toc] -->

<!-- Start SDK Installation [installation] -->
## SDK Installation

The SDK can be installed with either [npm](https://www.npmjs.com/), [pnpm](https://pnpm.io/), [bun](https://bun.sh/) or [yarn](https://classic.yarnpkg.com/en/) package managers.

### NPM

```bash
npm add openapi
```

### PNPM

```bash
pnpm add openapi
```

### Bun

```bash
bun add openapi
```

### Yarn

```bash
yarn add openapi
```

> [!NOTE]
> This package is published with CommonJS and ES Modules (ESM) support.
<!-- End SDK Installation [installation] -->

<!-- Start Requirements [requirements] -->
## Requirements

For supported JavaScript runtimes, please consult [RUNTIMES.md](RUNTIMES.md).
<!-- End Requirements [requirements] -->

<!-- Start SDK Example Usage [usage] -->
## SDK Example Usage

### Example

```typescript
import { SDK } from "openapi";

const sdk = new SDK({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await sdk.addons.createAddon({
    lookupKey: "<value>",
    name: "<value>",
    type: "multiple_instance",
  });

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->

<!-- Start Authentication [security] -->
## Authentication

### Per-Client Security Schemes

This SDK supports the following security scheme globally:

| Name         | Type   | Scheme  |
| ------------ | ------ | ------- |
| `apiKeyAuth` | apiKey | API key |

To authenticate with the API the `apiKeyAuth` parameter must be set when initializing the SDK client instance. For example:
```typescript
import { SDK } from "openapi";

const sdk = new SDK({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await sdk.addons.createAddon({
    lookupKey: "<value>",
    name: "<value>",
    type: "multiple_instance",
  });

  console.log(result);
}

run();

```
<!-- End Authentication [security] -->

<!-- Start Available Resources and Operations [operations] -->
## Available Resources and Operations

<details open>
<summary>Available methods</summary>

### [Addons](docs/sdks/addons/README.md)

* [createAddon](docs/sdks/addons/README.md#createaddon) - Create addon
* [getAddonByLookupKey](docs/sdks/addons/README.md#getaddonbylookupkey) - Get addon by lookup key
* [queryAddon](docs/sdks/addons/README.md#queryaddon) - Query addons
* [getAddon](docs/sdks/addons/README.md#getaddon) - Get addon
* [updateAddon](docs/sdks/addons/README.md#updateaddon) - Update addon
* [deleteAddon](docs/sdks/addons/README.md#deleteaddon) - Delete addon

### [Alerts](docs/sdks/alerts/README.md)

* [queryAlertLog](docs/sdks/alerts/README.md#queryalertlog) - Query alert logs

### [Costs](docs/sdks/costs/README.md)

* [createCostsheet](docs/sdks/costs/README.md#createcostsheet) - Create costsheet
* [getActiveCostsheet](docs/sdks/costs/README.md#getactivecostsheet) - Get active costsheet
* [getDetailedCostAnalytics](docs/sdks/costs/README.md#getdetailedcostanalytics) - Get combined revenue and cost analytics
* [getDetailedCostAnalyticsV2](docs/sdks/costs/README.md#getdetailedcostanalyticsv2) - Get combined revenue and cost analytics (V2)
* [queryCostsheet](docs/sdks/costs/README.md#querycostsheet) - Query costsheets
* [getCostsheet](docs/sdks/costs/README.md#getcostsheet) - Get costsheet
* [updateCostsheet](docs/sdks/costs/README.md#updatecostsheet) - Update costsheet
* [deleteCostsheet](docs/sdks/costs/README.md#deletecostsheet) - Delete costsheet

### [Coupons](docs/sdks/coupons/README.md)

* [createCoupon](docs/sdks/coupons/README.md#createcoupon) - Create coupon
* [queryCoupon](docs/sdks/coupons/README.md#querycoupon) - Query coupons
* [getCoupon](docs/sdks/coupons/README.md#getcoupon) - Get coupon
* [updateCoupon](docs/sdks/coupons/README.md#updatecoupon) - Update coupon
* [deleteCoupon](docs/sdks/coupons/README.md#deletecoupon) - Delete coupon

### [CreditGrants](docs/sdks/creditgrants/README.md)

* [createCreditGrant](docs/sdks/creditgrants/README.md#createcreditgrant) - Create credit grant
* [getCreditGrant](docs/sdks/creditgrants/README.md#getcreditgrant) - Get credit grant
* [updateCreditGrant](docs/sdks/creditgrants/README.md#updatecreditgrant) - Update credit grant
* [deleteCreditGrant](docs/sdks/creditgrants/README.md#deletecreditgrant) - Delete credit grant
* [getPlanCreditGrants](docs/sdks/creditgrants/README.md#getplancreditgrants) - Get plan credit grants

### [CreditNotes](docs/sdks/creditnotes/README.md)

* [createCreditNote](docs/sdks/creditnotes/README.md#createcreditnote) - Create credit note
* [getCreditNote](docs/sdks/creditnotes/README.md#getcreditnote) - Get credit note
* [processCreditNote](docs/sdks/creditnotes/README.md#processcreditnote) - Finalize credit note
* [voidCreditNote](docs/sdks/creditnotes/README.md#voidcreditnote) - Void credit note

### [Customers](docs/sdks/customers/README.md)

* [updateCustomer](docs/sdks/customers/README.md#updatecustomer) - Update customer
* [createCustomer](docs/sdks/customers/README.md#createcustomer) - Create customer
* [getCustomerByExternalId](docs/sdks/customers/README.md#getcustomerbyexternalid) - Get customer by external ID
* [queryCustomer](docs/sdks/customers/README.md#querycustomer) - Query customers
* [getCustomerUsageSummary](docs/sdks/customers/README.md#getcustomerusagesummary) - Get customer usage summary
* [getCustomer](docs/sdks/customers/README.md#getcustomer) - Get customer
* [deleteCustomer](docs/sdks/customers/README.md#deletecustomer) - Delete customer
* [getCustomerEntitlements](docs/sdks/customers/README.md#getcustomerentitlements) - Get customer entitlements
* [getCustomerUpcomingGrants](docs/sdks/customers/README.md#getcustomerupcominggrants) - Get upcoming credit grant applications

### [Entitlements](docs/sdks/entitlements/README.md)

* [getAddonEntitlements](docs/sdks/entitlements/README.md#getaddonentitlements) - Get addon entitlements
* [createEntitlement](docs/sdks/entitlements/README.md#createentitlement) - Create entitlement
* [createEntitlementsBulk](docs/sdks/entitlements/README.md#createentitlementsbulk) - Create entitlements in bulk
* [queryEntitlement](docs/sdks/entitlements/README.md#queryentitlement) - Query entitlements
* [getEntitlement](docs/sdks/entitlements/README.md#getentitlement) - Get entitlement
* [updateEntitlement](docs/sdks/entitlements/README.md#updateentitlement) - Update entitlement
* [deleteEntitlement](docs/sdks/entitlements/README.md#deleteentitlement) - Delete entitlement
* [getPlanEntitlements](docs/sdks/entitlements/README.md#getplanentitlements) - Get plan entitlements

### [EntityIntegrationMappings](docs/sdks/entityintegrationmappings/README.md)

* [createEntityIntegrationMapping](docs/sdks/entityintegrationmappings/README.md#createentityintegrationmapping) - Create entity integration mapping
* [deleteEntityIntegrationMapping](docs/sdks/entityintegrationmappings/README.md#deleteentityintegrationmapping) - Delete entity integration mapping

### [Environments](docs/sdks/environments/README.md)

* [createEnvironment](docs/sdks/environments/README.md#createenvironment) - Create environment
* [updateEnvironment](docs/sdks/environments/README.md#updateenvironment) - Update environment

### [Events](docs/sdks/events/README.md)

* [ingestEvent](docs/sdks/events/README.md#ingestevent) - Ingest event
* [getUsageAnalytics](docs/sdks/events/README.md#getusageanalytics) - Get usage analytics
* [ingestEventsBulk](docs/sdks/events/README.md#ingesteventsbulk) - Bulk ingest events
* [getHuggingfaceInferenceData](docs/sdks/events/README.md#gethuggingfaceinferencedata) - Get Hugging Face inference data
* [listRawEvents](docs/sdks/events/README.md#listrawevents) - List raw events
* [getUsageStatistics](docs/sdks/events/README.md#getusagestatistics) - Get usage statistics
* [getUsageByMeter](docs/sdks/events/README.md#getusagebymeter) - Get usage by meter
* [getEvent](docs/sdks/events/README.md#getevent) - Get event

### [Features](docs/sdks/features/README.md)

* [createFeature](docs/sdks/features/README.md#createfeature) - Create feature
* [queryFeature](docs/sdks/features/README.md#queryfeature) - Query features
* [updateFeature](docs/sdks/features/README.md#updatefeature) - Update feature
* [deleteFeature](docs/sdks/features/README.md#deletefeature) - Delete feature

### [Groups](docs/sdks/groups/README.md)

* [createGroup](docs/sdks/groups/README.md#creategroup) - Create group
* [queryGroup](docs/sdks/groups/README.md#querygroup) - Query groups
* [getGroup](docs/sdks/groups/README.md#getgroup) - Get group
* [deleteGroup](docs/sdks/groups/README.md#deletegroup) - Delete group

### [Integrations](docs/sdks/integrations/README.md)

* [getIntegration](docs/sdks/integrations/README.md#getintegration) - Get integration details
* [createOrUpdateIntegration](docs/sdks/integrations/README.md#createorupdateintegration) - Create or update an integration
* [listLinkedIntegrations](docs/sdks/integrations/README.md#listlinkedintegrations) - List linked integrations
* [deleteIntegration](docs/sdks/integrations/README.md#deleteintegration) - Delete an integration

### [Invoices](docs/sdks/invoices/README.md)

* [getCustomerInvoiceSummary](docs/sdks/invoices/README.md#getcustomerinvoicesummary) - Get customer invoice summary
* [createInvoice](docs/sdks/invoices/README.md#createinvoice) - Create one-off invoice
* [getInvoicePreview](docs/sdks/invoices/README.md#getinvoicepreview) - Get invoice preview
* [queryInvoice](docs/sdks/invoices/README.md#queryinvoice) - Query invoices
* [getInvoice](docs/sdks/invoices/README.md#getinvoice) - Get invoice
* [updateInvoice](docs/sdks/invoices/README.md#updateinvoice) - Update invoice
* [triggerInvoiceCommsWebhook](docs/sdks/invoices/README.md#triggerinvoicecommswebhook) - Trigger invoice communication webhook
* [finalizeInvoice](docs/sdks/invoices/README.md#finalizeinvoice) - Finalize invoice
* [updateInvoicePaymentStatus](docs/sdks/invoices/README.md#updateinvoicepaymentstatus) - Update invoice payment status
* [attemptInvoicePayment](docs/sdks/invoices/README.md#attemptinvoicepayment) - Attempt invoice payment
* [getInvoicePdf](docs/sdks/invoices/README.md#getinvoicepdf) - Get invoice PDF
* [recalculateInvoice](docs/sdks/invoices/README.md#recalculateinvoice) - Recalculate invoice
* [voidInvoice](docs/sdks/invoices/README.md#voidinvoice) - Void invoice

### [Payments](docs/sdks/payments/README.md)

* [listPayments](docs/sdks/payments/README.md#listpayments) - List payments
* [createPayment](docs/sdks/payments/README.md#createpayment) - Create payment
* [getPayment](docs/sdks/payments/README.md#getpayment) - Get payment
* [updatePayment](docs/sdks/payments/README.md#updatepayment) - Update payment
* [deletePayment](docs/sdks/payments/README.md#deletepayment) - Delete payment
* [processPayment](docs/sdks/payments/README.md#processpayment) - Process payment

### [Plans](docs/sdks/plans/README.md)

* [createPlan](docs/sdks/plans/README.md#createplan) - Create plan
* [queryPlan](docs/sdks/plans/README.md#queryplan) - Query plans
* [getPlan](docs/sdks/plans/README.md#getplan) - Get plan
* [updatePlan](docs/sdks/plans/README.md#updateplan) - Update plan
* [deletePlan](docs/sdks/plans/README.md#deleteplan) - Delete plan
* [syncPlanPrices](docs/sdks/plans/README.md#syncplanprices) - Synchronize plan prices

### [PriceUnits](docs/sdks/priceunits/README.md)

* [listPriceUnits](docs/sdks/priceunits/README.md#listpriceunits) - List price units
* [createPriceUnit](docs/sdks/priceunits/README.md#createpriceunit) - Create price unit
* [getPriceUnitByCode](docs/sdks/priceunits/README.md#getpriceunitbycode) - Get price unit by code
* [queryPriceUnit](docs/sdks/priceunits/README.md#querypriceunit) - Query price units
* [getPriceUnit](docs/sdks/priceunits/README.md#getpriceunit) - Get price unit
* [updatePriceUnit](docs/sdks/priceunits/README.md#updatepriceunit) - Update price unit
* [deletePriceUnit](docs/sdks/priceunits/README.md#deletepriceunit) - Delete price unit

### [Prices](docs/sdks/prices/README.md)

* [createPrice](docs/sdks/prices/README.md#createprice) - Create price
* [createPricesBulk](docs/sdks/prices/README.md#createpricesbulk) - Create prices in bulk
* [getPriceByLookupKey](docs/sdks/prices/README.md#getpricebylookupkey) - Get price by lookup key
* [queryPrice](docs/sdks/prices/README.md#queryprice) - Query prices
* [getPrice](docs/sdks/prices/README.md#getprice) - Get price
* [updatePrice](docs/sdks/prices/README.md#updateprice) - Update price
* [deletePrice](docs/sdks/prices/README.md#deleteprice) - Delete price

### [Rbac](docs/sdks/rbac/README.md)

* [listRbacRoles](docs/sdks/rbac/README.md#listrbacroles) - List all RBAC roles
* [getRbacRole](docs/sdks/rbac/README.md#getrbacrole) - Get a specific RBAC role

### [ScheduledTasks](docs/sdks/scheduledtasks/README.md)

* [listScheduledTasks](docs/sdks/scheduledtasks/README.md#listscheduledtasks) - List scheduled tasks
* [createScheduledTask](docs/sdks/scheduledtasks/README.md#createscheduledtask) - Create scheduled task
* [scheduleUpdateBillingPeriod](docs/sdks/scheduledtasks/README.md#scheduleupdatebillingperiod) - Schedule update billing period
* [getScheduledTask](docs/sdks/scheduledtasks/README.md#getscheduledtask) - Get scheduled task
* [updateScheduledTask](docs/sdks/scheduledtasks/README.md#updatescheduledtask) - Update a scheduled task
* [deleteScheduledTask](docs/sdks/scheduledtasks/README.md#deletescheduledtask) - Delete a scheduled task
* [triggerScheduledTaskRun](docs/sdks/scheduledtasks/README.md#triggerscheduledtaskrun) - Trigger force run

### [Secrets](docs/sdks/secrets/README.md)

* [listApiKeys](docs/sdks/secrets/README.md#listapikeys) - List API keys
* [createApiKey](docs/sdks/secrets/README.md#createapikey) - Create a new API key
* [deleteApiKey](docs/sdks/secrets/README.md#deleteapikey) - Delete an API key

### [Subscriptions](docs/sdks/subscriptions/README.md)

* [createSubscription](docs/sdks/subscriptions/README.md#createsubscription) - Create subscription
* [addSubscriptionAddon](docs/sdks/subscriptions/README.md#addsubscriptionaddon) - Add addon to subscription
* [removeSubscriptionAddon](docs/sdks/subscriptions/README.md#removesubscriptionaddon) - Remove addon from subscription
* [updateSubscriptionLineItem](docs/sdks/subscriptions/README.md#updatesubscriptionlineitem) - Update subscription line item
* [deleteSubscriptionLineItem](docs/sdks/subscriptions/README.md#deletesubscriptionlineitem) - Delete subscription line item
* [querySubscription](docs/sdks/subscriptions/README.md#querysubscription) - Query subscriptions
* [getSubscriptionUsage](docs/sdks/subscriptions/README.md#getsubscriptionusage) - Get usage by subscription
* [getSubscription](docs/sdks/subscriptions/README.md#getsubscription) - Get subscription
* [updateSubscription](docs/sdks/subscriptions/README.md#updatesubscription) - Update subscription
* [activateSubscription](docs/sdks/subscriptions/README.md#activatesubscription) - Activate draft subscription
* [getSubscriptionAddonAssociations](docs/sdks/subscriptions/README.md#getsubscriptionaddonassociations) - Get active addon associations
* [cancelSubscription](docs/sdks/subscriptions/README.md#cancelsubscription) - Cancel subscription
* [executeSubscriptionChange](docs/sdks/subscriptions/README.md#executesubscriptionchange) - Execute subscription plan change
* [previewSubscriptionChange](docs/sdks/subscriptions/README.md#previewsubscriptionchange) - Preview subscription plan change
* [getSubscriptionEntitlements](docs/sdks/subscriptions/README.md#getsubscriptionentitlements) - Get subscription entitlements
* [getSubscriptionUpcomingGrants](docs/sdks/subscriptions/README.md#getsubscriptionupcominggrants) - Get upcoming credit grant applications
* [createSubscriptionLineItem](docs/sdks/subscriptions/README.md#createsubscriptionlineitem) - Create subscription line item
* [pauseSubscription](docs/sdks/subscriptions/README.md#pausesubscription) - Pause a subscription
* [listSubscriptionPauses](docs/sdks/subscriptions/README.md#listsubscriptionpauses) - List all pauses for a subscription
* [resumeSubscription](docs/sdks/subscriptions/README.md#resumesubscription) - Resume a paused subscription
* [getSubscriptionV2](docs/sdks/subscriptions/README.md#getsubscriptionv2) - Get subscription (V2)
* [listAllSubscriptionSchedules](docs/sdks/subscriptions/README.md#listallsubscriptionschedules) - List all subscription schedules
* [getSubscriptionSchedule](docs/sdks/subscriptions/README.md#getsubscriptionschedule) - Get subscription schedule
* [cancelSubscriptionSchedule](docs/sdks/subscriptions/README.md#cancelsubscriptionschedule) - Cancel subscription schedule
* [listSubscriptionSchedules](docs/sdks/subscriptions/README.md#listsubscriptionschedules) - List subscription schedules

### [Tasks](docs/sdks/tasks/README.md)

* [listTasks](docs/sdks/tasks/README.md#listtasks) - List tasks
* [createTask](docs/sdks/tasks/README.md#createtask) - Create a new task
* [getTaskResult](docs/sdks/tasks/README.md#gettaskresult) - Get task processing result
* [getTask](docs/sdks/tasks/README.md#gettask) - Get a task
* [downloadTaskExport](docs/sdks/tasks/README.md#downloadtaskexport) - Download task export file
* [updateTaskStatus](docs/sdks/tasks/README.md#updatetaskstatus) - Update task status

### [TaxAssociations](docs/sdks/taxassociations/README.md)

* [listTaxAssociations](docs/sdks/taxassociations/README.md#listtaxassociations) - List tax associations
* [createTaxAssociation](docs/sdks/taxassociations/README.md#createtaxassociation) - Create Tax Association
* [getTaxAssociation](docs/sdks/taxassociations/README.md#gettaxassociation) - Get Tax Association
* [updateTaxAssociation](docs/sdks/taxassociations/README.md#updatetaxassociation) - Update tax association
* [deleteTaxAssociation](docs/sdks/taxassociations/README.md#deletetaxassociation) - Delete tax association

### [TaxRates](docs/sdks/taxrates/README.md)

* [getTaxRates](docs/sdks/taxrates/README.md#gettaxrates) - Get tax rates
* [createTaxRate](docs/sdks/taxrates/README.md#createtaxrate) - Create a tax rate
* [getTaxRate](docs/sdks/taxrates/README.md#gettaxrate) - Get a tax rate
* [updateTaxRate](docs/sdks/taxrates/README.md#updatetaxrate) - Update a tax rate
* [deleteTaxRate](docs/sdks/taxrates/README.md#deletetaxrate) - Delete a tax rate

### [Tenants](docs/sdks/tenants/README.md)

* [getTenantBillingUsage](docs/sdks/tenants/README.md#gettenantbillingusage) - Get billing usage for the current tenant
* [createTenant](docs/sdks/tenants/README.md#createtenant) - Create a new tenant
* [updateTenant](docs/sdks/tenants/README.md#updatetenant) - Update a tenant
* [getTenant](docs/sdks/tenants/README.md#gettenant) - Get tenant

### [Users](docs/sdks/users/README.md)

* [createUser](docs/sdks/users/README.md#createuser) - Create service account
* [getUserInfo](docs/sdks/users/README.md#getuserinfo) - Get current user
* [queryUser](docs/sdks/users/README.md#queryuser) - Query users

### [Wallets](docs/sdks/wallets/README.md)

* [getCustomerWallets](docs/sdks/wallets/README.md#getcustomerwallets) - Get Customer Wallets
* [getWalletsByCustomerId](docs/sdks/wallets/README.md#getwalletsbycustomerid) - Get wallets by customer ID
* [createWallet](docs/sdks/wallets/README.md#createwallet) - Create a new wallet
* [queryWallet](docs/sdks/wallets/README.md#querywallet) - Query wallets
* [queryWalletTransaction](docs/sdks/wallets/README.md#querywallettransaction) - Query wallet transactions
* [getWallet](docs/sdks/wallets/README.md#getwallet) - Get wallet
* [updateWallet](docs/sdks/wallets/README.md#updatewallet) - Update a wallet
* [getWalletBalance](docs/sdks/wallets/README.md#getwalletbalance) - Get wallet balance
* [terminateWallet](docs/sdks/wallets/README.md#terminatewallet) - Terminate a wallet
* [topUpWallet](docs/sdks/wallets/README.md#topupwallet) - Top up wallet
* [getWalletTransactions](docs/sdks/wallets/README.md#getwallettransactions) - Get wallet transactions

### [Webhooks](docs/sdks/webhooks/README.md)

* [handleChargebeeWebhook](docs/sdks/webhooks/README.md#handlechargebeewebhook) - Handle Chargebee webhook events
* [handleHubspotWebhook](docs/sdks/webhooks/README.md#handlehubspotwebhook) - Handle HubSpot webhook events
* [handleMoyasarWebhook](docs/sdks/webhooks/README.md#handlemoyasarwebhook) - Handle Moyasar webhook events
* [handleNomodWebhook](docs/sdks/webhooks/README.md#handlenomodwebhook) - Handle Nomod webhook events
* [handleQuickbooksWebhook](docs/sdks/webhooks/README.md#handlequickbookswebhook) - Handle QuickBooks webhook events
* [handleRazorpayWebhook](docs/sdks/webhooks/README.md#handlerazorpaywebhook) - Handle Razorpay webhook events
* [handleStripeWebhook](docs/sdks/webhooks/README.md#handlestripewebhook) - Handle Stripe webhook events

### [Workflows](docs/sdks/workflows/README.md)

* [queryWorkflow](docs/sdks/workflows/README.md#queryworkflow) - Query workflows

</details>
<!-- End Available Resources and Operations [operations] -->

<!-- Start Standalone functions [standalone-funcs] -->
## Standalone functions

All the methods listed above are available as standalone functions. These
functions are ideal for use in applications running in the browser, serverless
runtimes or other environments where application bundle size is a primary
concern. When using a bundler to build your application, all unused
functionality will be either excluded from the final bundle or tree-shaken away.

To read more about standalone functions, check [FUNCTIONS.md](./FUNCTIONS.md).

<details>

<summary>Available standalone functions</summary>

- [`addonsCreateAddon`](docs/sdks/addons/README.md#createaddon) - Create addon
- [`addonsDeleteAddon`](docs/sdks/addons/README.md#deleteaddon) - Delete addon
- [`addonsGetAddon`](docs/sdks/addons/README.md#getaddon) - Get addon
- [`addonsGetAddonByLookupKey`](docs/sdks/addons/README.md#getaddonbylookupkey) - Get addon by lookup key
- [`addonsQueryAddon`](docs/sdks/addons/README.md#queryaddon) - Query addons
- [`addonsUpdateAddon`](docs/sdks/addons/README.md#updateaddon) - Update addon
- [`alertsQueryAlertLog`](docs/sdks/alerts/README.md#queryalertlog) - Query alert logs
- [`costsCreateCostsheet`](docs/sdks/costs/README.md#createcostsheet) - Create costsheet
- [`costsDeleteCostsheet`](docs/sdks/costs/README.md#deletecostsheet) - Delete costsheet
- [`costsGetActiveCostsheet`](docs/sdks/costs/README.md#getactivecostsheet) - Get active costsheet
- [`costsGetCostsheet`](docs/sdks/costs/README.md#getcostsheet) - Get costsheet
- [`costsGetDetailedCostAnalytics`](docs/sdks/costs/README.md#getdetailedcostanalytics) - Get combined revenue and cost analytics
- [`costsGetDetailedCostAnalyticsV2`](docs/sdks/costs/README.md#getdetailedcostanalyticsv2) - Get combined revenue and cost analytics (V2)
- [`costsQueryCostsheet`](docs/sdks/costs/README.md#querycostsheet) - Query costsheets
- [`costsUpdateCostsheet`](docs/sdks/costs/README.md#updatecostsheet) - Update costsheet
- [`couponsCreateCoupon`](docs/sdks/coupons/README.md#createcoupon) - Create coupon
- [`couponsDeleteCoupon`](docs/sdks/coupons/README.md#deletecoupon) - Delete coupon
- [`couponsGetCoupon`](docs/sdks/coupons/README.md#getcoupon) - Get coupon
- [`couponsQueryCoupon`](docs/sdks/coupons/README.md#querycoupon) - Query coupons
- [`couponsUpdateCoupon`](docs/sdks/coupons/README.md#updatecoupon) - Update coupon
- [`creditGrantsCreateCreditGrant`](docs/sdks/creditgrants/README.md#createcreditgrant) - Create credit grant
- [`creditGrantsDeleteCreditGrant`](docs/sdks/creditgrants/README.md#deletecreditgrant) - Delete credit grant
- [`creditGrantsGetCreditGrant`](docs/sdks/creditgrants/README.md#getcreditgrant) - Get credit grant
- [`creditGrantsGetPlanCreditGrants`](docs/sdks/creditgrants/README.md#getplancreditgrants) - Get plan credit grants
- [`creditGrantsUpdateCreditGrant`](docs/sdks/creditgrants/README.md#updatecreditgrant) - Update credit grant
- [`creditNotesCreateCreditNote`](docs/sdks/creditnotes/README.md#createcreditnote) - Create credit note
- [`creditNotesGetCreditNote`](docs/sdks/creditnotes/README.md#getcreditnote) - Get credit note
- [`creditNotesProcessCreditNote`](docs/sdks/creditnotes/README.md#processcreditnote) - Finalize credit note
- [`creditNotesVoidCreditNote`](docs/sdks/creditnotes/README.md#voidcreditnote) - Void credit note
- [`customersCreateCustomer`](docs/sdks/customers/README.md#createcustomer) - Create customer
- [`customersDeleteCustomer`](docs/sdks/customers/README.md#deletecustomer) - Delete customer
- [`customersGetCustomer`](docs/sdks/customers/README.md#getcustomer) - Get customer
- [`customersGetCustomerByExternalId`](docs/sdks/customers/README.md#getcustomerbyexternalid) - Get customer by external ID
- [`customersGetCustomerEntitlements`](docs/sdks/customers/README.md#getcustomerentitlements) - Get customer entitlements
- [`customersGetCustomerUpcomingGrants`](docs/sdks/customers/README.md#getcustomerupcominggrants) - Get upcoming credit grant applications
- [`customersGetCustomerUsageSummary`](docs/sdks/customers/README.md#getcustomerusagesummary) - Get customer usage summary
- [`customersQueryCustomer`](docs/sdks/customers/README.md#querycustomer) - Query customers
- [`customersUpdateCustomer`](docs/sdks/customers/README.md#updatecustomer) - Update customer
- [`entitlementsCreateEntitlement`](docs/sdks/entitlements/README.md#createentitlement) - Create entitlement
- [`entitlementsCreateEntitlementsBulk`](docs/sdks/entitlements/README.md#createentitlementsbulk) - Create entitlements in bulk
- [`entitlementsDeleteEntitlement`](docs/sdks/entitlements/README.md#deleteentitlement) - Delete entitlement
- [`entitlementsGetAddonEntitlements`](docs/sdks/entitlements/README.md#getaddonentitlements) - Get addon entitlements
- [`entitlementsGetEntitlement`](docs/sdks/entitlements/README.md#getentitlement) - Get entitlement
- [`entitlementsGetPlanEntitlements`](docs/sdks/entitlements/README.md#getplanentitlements) - Get plan entitlements
- [`entitlementsQueryEntitlement`](docs/sdks/entitlements/README.md#queryentitlement) - Query entitlements
- [`entitlementsUpdateEntitlement`](docs/sdks/entitlements/README.md#updateentitlement) - Update entitlement
- [`entityIntegrationMappingsCreateEntityIntegrationMapping`](docs/sdks/entityintegrationmappings/README.md#createentityintegrationmapping) - Create entity integration mapping
- [`entityIntegrationMappingsDeleteEntityIntegrationMapping`](docs/sdks/entityintegrationmappings/README.md#deleteentityintegrationmapping) - Delete entity integration mapping
- [`environmentsCreateEnvironment`](docs/sdks/environments/README.md#createenvironment) - Create environment
- [`environmentsUpdateEnvironment`](docs/sdks/environments/README.md#updateenvironment) - Update environment
- [`eventsGetEvent`](docs/sdks/events/README.md#getevent) - Get event
- [`eventsGetHuggingfaceInferenceData`](docs/sdks/events/README.md#gethuggingfaceinferencedata) - Get Hugging Face inference data
- [`eventsGetUsageAnalytics`](docs/sdks/events/README.md#getusageanalytics) - Get usage analytics
- [`eventsGetUsageByMeter`](docs/sdks/events/README.md#getusagebymeter) - Get usage by meter
- [`eventsGetUsageStatistics`](docs/sdks/events/README.md#getusagestatistics) - Get usage statistics
- [`eventsIngestEvent`](docs/sdks/events/README.md#ingestevent) - Ingest event
- [`eventsIngestEventsBulk`](docs/sdks/events/README.md#ingesteventsbulk) - Bulk ingest events
- [`eventsListRawEvents`](docs/sdks/events/README.md#listrawevents) - List raw events
- [`featuresCreateFeature`](docs/sdks/features/README.md#createfeature) - Create feature
- [`featuresDeleteFeature`](docs/sdks/features/README.md#deletefeature) - Delete feature
- [`featuresQueryFeature`](docs/sdks/features/README.md#queryfeature) - Query features
- [`featuresUpdateFeature`](docs/sdks/features/README.md#updatefeature) - Update feature
- [`groupsCreateGroup`](docs/sdks/groups/README.md#creategroup) - Create group
- [`groupsDeleteGroup`](docs/sdks/groups/README.md#deletegroup) - Delete group
- [`groupsGetGroup`](docs/sdks/groups/README.md#getgroup) - Get group
- [`groupsQueryGroup`](docs/sdks/groups/README.md#querygroup) - Query groups
- [`integrationsCreateOrUpdateIntegration`](docs/sdks/integrations/README.md#createorupdateintegration) - Create or update an integration
- [`integrationsDeleteIntegration`](docs/sdks/integrations/README.md#deleteintegration) - Delete an integration
- [`integrationsGetIntegration`](docs/sdks/integrations/README.md#getintegration) - Get integration details
- [`integrationsListLinkedIntegrations`](docs/sdks/integrations/README.md#listlinkedintegrations) - List linked integrations
- [`invoicesAttemptInvoicePayment`](docs/sdks/invoices/README.md#attemptinvoicepayment) - Attempt invoice payment
- [`invoicesCreateInvoice`](docs/sdks/invoices/README.md#createinvoice) - Create one-off invoice
- [`invoicesFinalizeInvoice`](docs/sdks/invoices/README.md#finalizeinvoice) - Finalize invoice
- [`invoicesGetCustomerInvoiceSummary`](docs/sdks/invoices/README.md#getcustomerinvoicesummary) - Get customer invoice summary
- [`invoicesGetInvoice`](docs/sdks/invoices/README.md#getinvoice) - Get invoice
- [`invoicesGetInvoicePdf`](docs/sdks/invoices/README.md#getinvoicepdf) - Get invoice PDF
- [`invoicesGetInvoicePreview`](docs/sdks/invoices/README.md#getinvoicepreview) - Get invoice preview
- [`invoicesQueryInvoice`](docs/sdks/invoices/README.md#queryinvoice) - Query invoices
- [`invoicesRecalculateInvoice`](docs/sdks/invoices/README.md#recalculateinvoice) - Recalculate invoice
- [`invoicesTriggerInvoiceCommsWebhook`](docs/sdks/invoices/README.md#triggerinvoicecommswebhook) - Trigger invoice communication webhook
- [`invoicesUpdateInvoice`](docs/sdks/invoices/README.md#updateinvoice) - Update invoice
- [`invoicesUpdateInvoicePaymentStatus`](docs/sdks/invoices/README.md#updateinvoicepaymentstatus) - Update invoice payment status
- [`invoicesVoidInvoice`](docs/sdks/invoices/README.md#voidinvoice) - Void invoice
- [`paymentsCreatePayment`](docs/sdks/payments/README.md#createpayment) - Create payment
- [`paymentsDeletePayment`](docs/sdks/payments/README.md#deletepayment) - Delete payment
- [`paymentsGetPayment`](docs/sdks/payments/README.md#getpayment) - Get payment
- [`paymentsListPayments`](docs/sdks/payments/README.md#listpayments) - List payments
- [`paymentsProcessPayment`](docs/sdks/payments/README.md#processpayment) - Process payment
- [`paymentsUpdatePayment`](docs/sdks/payments/README.md#updatepayment) - Update payment
- [`plansCreatePlan`](docs/sdks/plans/README.md#createplan) - Create plan
- [`plansDeletePlan`](docs/sdks/plans/README.md#deleteplan) - Delete plan
- [`plansGetPlan`](docs/sdks/plans/README.md#getplan) - Get plan
- [`plansQueryPlan`](docs/sdks/plans/README.md#queryplan) - Query plans
- [`plansSyncPlanPrices`](docs/sdks/plans/README.md#syncplanprices) - Synchronize plan prices
- [`plansUpdatePlan`](docs/sdks/plans/README.md#updateplan) - Update plan
- [`pricesCreatePrice`](docs/sdks/prices/README.md#createprice) - Create price
- [`pricesCreatePricesBulk`](docs/sdks/prices/README.md#createpricesbulk) - Create prices in bulk
- [`pricesDeletePrice`](docs/sdks/prices/README.md#deleteprice) - Delete price
- [`pricesGetPrice`](docs/sdks/prices/README.md#getprice) - Get price
- [`pricesGetPriceByLookupKey`](docs/sdks/prices/README.md#getpricebylookupkey) - Get price by lookup key
- [`pricesQueryPrice`](docs/sdks/prices/README.md#queryprice) - Query prices
- [`pricesUpdatePrice`](docs/sdks/prices/README.md#updateprice) - Update price
- [`priceUnitsCreatePriceUnit`](docs/sdks/priceunits/README.md#createpriceunit) - Create price unit
- [`priceUnitsDeletePriceUnit`](docs/sdks/priceunits/README.md#deletepriceunit) - Delete price unit
- [`priceUnitsGetPriceUnit`](docs/sdks/priceunits/README.md#getpriceunit) - Get price unit
- [`priceUnitsGetPriceUnitByCode`](docs/sdks/priceunits/README.md#getpriceunitbycode) - Get price unit by code
- [`priceUnitsListPriceUnits`](docs/sdks/priceunits/README.md#listpriceunits) - List price units
- [`priceUnitsQueryPriceUnit`](docs/sdks/priceunits/README.md#querypriceunit) - Query price units
- [`priceUnitsUpdatePriceUnit`](docs/sdks/priceunits/README.md#updatepriceunit) - Update price unit
- [`rbacGetRBACRole`](docs/sdks/rbac/README.md#getrbacrole) - Get a specific RBAC role
- [`rbacListRBACRoles`](docs/sdks/rbac/README.md#listrbacroles) - List all RBAC roles
- [`scheduledTasksCreateScheduledTask`](docs/sdks/scheduledtasks/README.md#createscheduledtask) - Create scheduled task
- [`scheduledTasksDeleteScheduledTask`](docs/sdks/scheduledtasks/README.md#deletescheduledtask) - Delete a scheduled task
- [`scheduledTasksGetScheduledTask`](docs/sdks/scheduledtasks/README.md#getscheduledtask) - Get scheduled task
- [`scheduledTasksListScheduledTasks`](docs/sdks/scheduledtasks/README.md#listscheduledtasks) - List scheduled tasks
- [`scheduledTasksScheduleUpdateBillingPeriod`](docs/sdks/scheduledtasks/README.md#scheduleupdatebillingperiod) - Schedule update billing period
- [`scheduledTasksTriggerScheduledTaskRun`](docs/sdks/scheduledtasks/README.md#triggerscheduledtaskrun) - Trigger force run
- [`scheduledTasksUpdateScheduledTask`](docs/sdks/scheduledtasks/README.md#updatescheduledtask) - Update a scheduled task
- [`secretsCreateApiKey`](docs/sdks/secrets/README.md#createapikey) - Create a new API key
- [`secretsDeleteApiKey`](docs/sdks/secrets/README.md#deleteapikey) - Delete an API key
- [`secretsListApiKeys`](docs/sdks/secrets/README.md#listapikeys) - List API keys
- [`subscriptionsActivateSubscription`](docs/sdks/subscriptions/README.md#activatesubscription) - Activate draft subscription
- [`subscriptionsAddSubscriptionAddon`](docs/sdks/subscriptions/README.md#addsubscriptionaddon) - Add addon to subscription
- [`subscriptionsCancelSubscription`](docs/sdks/subscriptions/README.md#cancelsubscription) - Cancel subscription
- [`subscriptionsCancelSubscriptionSchedule`](docs/sdks/subscriptions/README.md#cancelsubscriptionschedule) - Cancel subscription schedule
- [`subscriptionsCreateSubscription`](docs/sdks/subscriptions/README.md#createsubscription) - Create subscription
- [`subscriptionsCreateSubscriptionLineItem`](docs/sdks/subscriptions/README.md#createsubscriptionlineitem) - Create subscription line item
- [`subscriptionsDeleteSubscriptionLineItem`](docs/sdks/subscriptions/README.md#deletesubscriptionlineitem) - Delete subscription line item
- [`subscriptionsExecuteSubscriptionChange`](docs/sdks/subscriptions/README.md#executesubscriptionchange) - Execute subscription plan change
- [`subscriptionsGetSubscription`](docs/sdks/subscriptions/README.md#getsubscription) - Get subscription
- [`subscriptionsGetSubscriptionAddonAssociations`](docs/sdks/subscriptions/README.md#getsubscriptionaddonassociations) - Get active addon associations
- [`subscriptionsGetSubscriptionEntitlements`](docs/sdks/subscriptions/README.md#getsubscriptionentitlements) - Get subscription entitlements
- [`subscriptionsGetSubscriptionSchedule`](docs/sdks/subscriptions/README.md#getsubscriptionschedule) - Get subscription schedule
- [`subscriptionsGetSubscriptionUpcomingGrants`](docs/sdks/subscriptions/README.md#getsubscriptionupcominggrants) - Get upcoming credit grant applications
- [`subscriptionsGetSubscriptionUsage`](docs/sdks/subscriptions/README.md#getsubscriptionusage) - Get usage by subscription
- [`subscriptionsGetSubscriptionV2`](docs/sdks/subscriptions/README.md#getsubscriptionv2) - Get subscription (V2)
- [`subscriptionsListAllSubscriptionSchedules`](docs/sdks/subscriptions/README.md#listallsubscriptionschedules) - List all subscription schedules
- [`subscriptionsListSubscriptionPauses`](docs/sdks/subscriptions/README.md#listsubscriptionpauses) - List all pauses for a subscription
- [`subscriptionsListSubscriptionSchedules`](docs/sdks/subscriptions/README.md#listsubscriptionschedules) - List subscription schedules
- [`subscriptionsPauseSubscription`](docs/sdks/subscriptions/README.md#pausesubscription) - Pause a subscription
- [`subscriptionsPreviewSubscriptionChange`](docs/sdks/subscriptions/README.md#previewsubscriptionchange) - Preview subscription plan change
- [`subscriptionsQuerySubscription`](docs/sdks/subscriptions/README.md#querysubscription) - Query subscriptions
- [`subscriptionsRemoveSubscriptionAddon`](docs/sdks/subscriptions/README.md#removesubscriptionaddon) - Remove addon from subscription
- [`subscriptionsResumeSubscription`](docs/sdks/subscriptions/README.md#resumesubscription) - Resume a paused subscription
- [`subscriptionsUpdateSubscription`](docs/sdks/subscriptions/README.md#updatesubscription) - Update subscription
- [`subscriptionsUpdateSubscriptionLineItem`](docs/sdks/subscriptions/README.md#updatesubscriptionlineitem) - Update subscription line item
- [`tasksCreateTask`](docs/sdks/tasks/README.md#createtask) - Create a new task
- [`tasksDownloadTaskExport`](docs/sdks/tasks/README.md#downloadtaskexport) - Download task export file
- [`tasksGetTask`](docs/sdks/tasks/README.md#gettask) - Get a task
- [`tasksGetTaskResult`](docs/sdks/tasks/README.md#gettaskresult) - Get task processing result
- [`tasksListTasks`](docs/sdks/tasks/README.md#listtasks) - List tasks
- [`tasksUpdateTaskStatus`](docs/sdks/tasks/README.md#updatetaskstatus) - Update task status
- [`taxAssociationsCreateTaxAssociation`](docs/sdks/taxassociations/README.md#createtaxassociation) - Create Tax Association
- [`taxAssociationsDeleteTaxAssociation`](docs/sdks/taxassociations/README.md#deletetaxassociation) - Delete tax association
- [`taxAssociationsGetTaxAssociation`](docs/sdks/taxassociations/README.md#gettaxassociation) - Get Tax Association
- [`taxAssociationsListTaxAssociations`](docs/sdks/taxassociations/README.md#listtaxassociations) - List tax associations
- [`taxAssociationsUpdateTaxAssociation`](docs/sdks/taxassociations/README.md#updatetaxassociation) - Update tax association
- [`taxRatesCreateTaxRate`](docs/sdks/taxrates/README.md#createtaxrate) - Create a tax rate
- [`taxRatesDeleteTaxRate`](docs/sdks/taxrates/README.md#deletetaxrate) - Delete a tax rate
- [`taxRatesGetTaxRate`](docs/sdks/taxrates/README.md#gettaxrate) - Get a tax rate
- [`taxRatesGetTaxRates`](docs/sdks/taxrates/README.md#gettaxrates) - Get tax rates
- [`taxRatesUpdateTaxRate`](docs/sdks/taxrates/README.md#updatetaxrate) - Update a tax rate
- [`tenantsCreateTenant`](docs/sdks/tenants/README.md#createtenant) - Create a new tenant
- [`tenantsGetTenant`](docs/sdks/tenants/README.md#gettenant) - Get tenant
- [`tenantsGetTenantBillingUsage`](docs/sdks/tenants/README.md#gettenantbillingusage) - Get billing usage for the current tenant
- [`tenantsUpdateTenant`](docs/sdks/tenants/README.md#updatetenant) - Update a tenant
- [`usersCreateUser`](docs/sdks/users/README.md#createuser) - Create service account
- [`usersGetUserInfo`](docs/sdks/users/README.md#getuserinfo) - Get current user
- [`usersQueryUser`](docs/sdks/users/README.md#queryuser) - Query users
- [`walletsCreateWallet`](docs/sdks/wallets/README.md#createwallet) - Create a new wallet
- [`walletsGetCustomerWallets`](docs/sdks/wallets/README.md#getcustomerwallets) - Get Customer Wallets
- [`walletsGetWallet`](docs/sdks/wallets/README.md#getwallet) - Get wallet
- [`walletsGetWalletBalance`](docs/sdks/wallets/README.md#getwalletbalance) - Get wallet balance
- [`walletsGetWalletsByCustomerId`](docs/sdks/wallets/README.md#getwalletsbycustomerid) - Get wallets by customer ID
- [`walletsGetWalletTransactions`](docs/sdks/wallets/README.md#getwallettransactions) - Get wallet transactions
- [`walletsQueryWallet`](docs/sdks/wallets/README.md#querywallet) - Query wallets
- [`walletsQueryWalletTransaction`](docs/sdks/wallets/README.md#querywallettransaction) - Query wallet transactions
- [`walletsTerminateWallet`](docs/sdks/wallets/README.md#terminatewallet) - Terminate a wallet
- [`walletsTopUpWallet`](docs/sdks/wallets/README.md#topupwallet) - Top up wallet
- [`walletsUpdateWallet`](docs/sdks/wallets/README.md#updatewallet) - Update a wallet
- [`webhooksHandleChargebeeWebhook`](docs/sdks/webhooks/README.md#handlechargebeewebhook) - Handle Chargebee webhook events
- [`webhooksHandleHubspotWebhook`](docs/sdks/webhooks/README.md#handlehubspotwebhook) - Handle HubSpot webhook events
- [`webhooksHandleMoyasarWebhook`](docs/sdks/webhooks/README.md#handlemoyasarwebhook) - Handle Moyasar webhook events
- [`webhooksHandleNomodWebhook`](docs/sdks/webhooks/README.md#handlenomodwebhook) - Handle Nomod webhook events
- [`webhooksHandleQuickbooksWebhook`](docs/sdks/webhooks/README.md#handlequickbookswebhook) - Handle QuickBooks webhook events
- [`webhooksHandleRazorpayWebhook`](docs/sdks/webhooks/README.md#handlerazorpaywebhook) - Handle Razorpay webhook events
- [`webhooksHandleStripeWebhook`](docs/sdks/webhooks/README.md#handlestripewebhook) - Handle Stripe webhook events
- [`workflowsQueryWorkflow`](docs/sdks/workflows/README.md#queryworkflow) - Query workflows

</details>
<!-- End Standalone functions [standalone-funcs] -->

<!-- Start Retries [retries] -->
## Retries

Some of the endpoints in this SDK support retries.  If you use the SDK without any configuration, it will fall back to the default retry strategy provided by the API.  However, the default retry strategy can be overridden on a per-operation basis, or across the entire SDK.

To change the default retry strategy for a single API call, simply provide a retryConfig object to the call:
```typescript
import { SDK } from "openapi";

const sdk = new SDK({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await sdk.addons.createAddon({
    lookupKey: "<value>",
    name: "<value>",
    type: "multiple_instance",
  }, {
    retries: {
      strategy: "backoff",
      backoff: {
        initialInterval: 1,
        maxInterval: 50,
        exponent: 1.1,
        maxElapsedTime: 100,
      },
      retryConnectionErrors: false,
    },
  });

  console.log(result);
}

run();

```

If you'd like to override the default retry strategy for all operations that support retries, you can provide a retryConfig at SDK initialization:
```typescript
import { SDK } from "openapi";

const sdk = new SDK({
  serverURL: "https://api.example.com",
  retryConfig: {
    strategy: "backoff",
    backoff: {
      initialInterval: 1,
      maxInterval: 50,
      exponent: 1.1,
      maxElapsedTime: 100,
    },
    retryConnectionErrors: false,
  },
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await sdk.addons.createAddon({
    lookupKey: "<value>",
    name: "<value>",
    type: "multiple_instance",
  });

  console.log(result);
}

run();

```
<!-- End Retries [retries] -->

<!-- Start Error Handling [errors] -->
## Error Handling

[`SDKError`](./src/models/errors/sdk-error.ts) is the base class for all HTTP error responses. It has the following properties:

| Property            | Type       | Description                                                                             |
| ------------------- | ---------- | --------------------------------------------------------------------------------------- |
| `error.message`     | `string`   | Error message                                                                           |
| `error.statusCode`  | `number`   | HTTP response status code eg `404`                                                      |
| `error.headers`     | `Headers`  | HTTP response headers                                                                   |
| `error.body`        | `string`   | HTTP body. Can be empty string if no body is returned.                                  |
| `error.rawResponse` | `Response` | Raw HTTP response                                                                       |
| `error.data$`       |            | Optional. Some errors may contain structured data. [See Error Classes](#error-classes). |

### Example
```typescript
import { SDK } from "openapi";
import * as errors from "openapi/models/errors";

const sdk = new SDK({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  try {
    const result = await sdk.addons.createAddon({
      lookupKey: "<value>",
      name: "<value>",
      type: "multiple_instance",
    });

    console.log(result);
  } catch (error) {
    // The base class for HTTP error responses
    if (error instanceof errors.SDKError) {
      console.log(error.message);
      console.log(error.statusCode);
      console.log(error.body);
      console.log(error.headers);

      // Depending on the method different errors may be thrown
      if (error instanceof errors.ErrorsErrorResponse) {
        console.log(error.data$.error); // models.ErrorsErrorDetail
        console.log(error.data$.success); // boolean
      }
    }
  }
}

run();

```

### Error Classes
**Primary errors:**
* [`SDKError`](./src/models/errors/sdk-error.ts): The base class for HTTP error responses.
  * [`ErrorsErrorResponse`](./src/models/errors/errors-error-response.ts): *

<details><summary>Less common errors (6)</summary>

<br />

**Network errors:**
* [`ConnectionError`](./src/models/errors/http-client-errors.ts): HTTP client was unable to make a request to a server.
* [`RequestTimeoutError`](./src/models/errors/http-client-errors.ts): HTTP request timed out due to an AbortSignal signal.
* [`RequestAbortedError`](./src/models/errors/http-client-errors.ts): HTTP request was aborted by the client.
* [`InvalidRequestError`](./src/models/errors/http-client-errors.ts): Any input used to create a request is invalid.
* [`UnexpectedClientError`](./src/models/errors/http-client-errors.ts): Unrecognised or unexpected error.


**Inherit from [`SDKError`](./src/models/errors/sdk-error.ts)**:
* [`ResponseValidationError`](./src/models/errors/response-validation-error.ts): Type mismatch between the data returned from the server and the structure expected by the SDK. See `error.rawValue` for the raw value and `error.pretty()` for a nicely formatted multi-line string.

</details>

\* Check [the method documentation](#available-resources-and-operations) to see if the error is applicable.
<!-- End Error Handling [errors] -->

<!-- Start Custom HTTP Client [http-client] -->
## Custom HTTP Client

The TypeScript SDK makes API calls using an `HTTPClient` that wraps the native
[Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API). This
client is a thin wrapper around `fetch` and provides the ability to attach hooks
around the request lifecycle that can be used to modify the request or handle
errors and response.

The `HTTPClient` constructor takes an optional `fetcher` argument that can be
used to integrate a third-party HTTP client or when writing tests to mock out
the HTTP client and feed in fixtures.

The following example shows how to:
- route requests through a proxy server using [undici](https://www.npmjs.com/package/undici)'s ProxyAgent
- use the `"beforeRequest"` hook to add a custom header and a timeout to requests
- use the `"requestError"` hook to log errors

```typescript
import { SDK } from "openapi";
import { ProxyAgent } from "undici";
import { HTTPClient } from "openapi/lib/http";

const dispatcher = new ProxyAgent("http://proxy.example.com:8080");

const httpClient = new HTTPClient({
  // 'fetcher' takes a function that has the same signature as native 'fetch'.
  fetcher: (input, init) =>
    // 'dispatcher' is specific to undici and not part of the standard Fetch API.
    fetch(input, { ...init, dispatcher } as RequestInit),
});

httpClient.addHook("beforeRequest", (request) => {
  const nextRequest = new Request(request, {
    signal: request.signal || AbortSignal.timeout(5000)
  });

  nextRequest.headers.set("x-custom-header", "custom value");

  return nextRequest;
});

httpClient.addHook("requestError", (error, request) => {
  console.group("Request Error");
  console.log("Reason:", `${error}`);
  console.log("Endpoint:", `${request.method} ${request.url}`);
  console.groupEnd();
});

const sdk = new SDK({ httpClient: httpClient });
```
<!-- End Custom HTTP Client [http-client] -->

<!-- Start Debugging [debug] -->
## Debugging

You can setup your SDK to emit debug logs for SDK requests and responses.

You can pass a logger that matches `console`'s interface as an SDK option.

> [!WARNING]
> Beware that debug logging will reveal secrets, like API tokens in headers, in log messages printed to a console or files. It's recommended to use this feature only during local development and not in production.

```typescript
import { SDK } from "openapi";

const sdk = new SDK({ debugLogger: console });
```
<!-- End Debugging [debug] -->

<!-- Placeholder for Future Speakeasy SDK Sections -->

# Development

## Maturity

This SDK is in beta, and there may be breaking changes between versions without a major version update. Therefore, we recommend pinning usage
to a specific package version. This way, you can install the same version each time without breaking changes unless you are intentionally
looking for the latest version.

## Contributions

While we value open-source contributions to this SDK, this library is generated programmatically. Any manual changes added to internal files will be overwritten on the next generation. 
We look forward to hearing your feedback. Feel free to open a PR or an issue with a proof of concept and we'll do our best to include it in a future release. 

### SDK Created by [Speakeasy](https://www.speakeasy.com/?utm_source=openapi&utm_campaign=typescript)
