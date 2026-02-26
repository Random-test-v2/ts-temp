# Invoices

## Overview

### Available Operations

* [attemptInvoicePayment](#attemptinvoicepayment) - Attempt invoice payment
* [createInvoice](#createinvoice) - Create one-off invoice
* [finalizeInvoice](#finalizeinvoice) - Finalize invoice
* [getCustomerInvoiceSummary](#getcustomerinvoicesummary) - Get customer invoice summary
* [getInvoice](#getinvoice) - Get invoice
* [getInvoicePdf](#getinvoicepdf) - Get invoice PDF
* [getInvoicePreview](#getinvoicepreview) - Get invoice preview
* [queryInvoice](#queryinvoice) - Query invoices
* [recalculateInvoice](#recalculateinvoice) - Recalculate invoice
* [triggerInvoiceCommsWebhook](#triggerinvoicecommswebhook) - Trigger invoice communication webhook
* [updateInvoice](#updateinvoice) - Update invoice
* [updateInvoicePaymentStatus](#updateinvoicepaymentstatus) - Update invoice payment status
* [voidInvoice](#voidinvoice) - Void invoice

## attemptInvoicePayment

Use when paying an invoice with the customer's wallet balance (e.g. prepaid credits or balance applied at checkout).

### Example Usage

<!-- UsageSnippet language="typescript" operationID="attemptInvoicePayment" method="post" path="/invoices/{id}/payment/attempt" -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.invoices.attemptInvoicePayment({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { FlexPriceCore } from "flexprice-ts/core.js";
import { invoicesAttemptInvoicePayment } from "flexprice-ts/funcs/invoicesAttemptInvoicePayment.js";

// Use `FlexPriceCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const flexPrice = new FlexPriceCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await invoicesAttemptInvoicePayment(flexPrice, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("invoicesAttemptInvoicePayment failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.AttemptInvoicePaymentRequest](../../sdk/models/operations/attemptinvoicepaymentrequest.md)                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.AttemptInvoicePaymentResponse](../../sdk/models/operations/attemptinvoicepaymentresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4XX, 5XX        | \*/\*           |

## createInvoice

Use when creating a manual or one-off invoice (e.g. custom charge or non-recurring billing). Invoice is created in draft; finalize when ready.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="createInvoice" method="post" path="/invoices" -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.invoices.createInvoice({
    amountDue: "<value>",
    currency: "Surinam Dollar",
    customerId: "<id>",
    subtotal: "<value>",
    total: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { FlexPriceCore } from "flexprice-ts/core.js";
import { invoicesCreateInvoice } from "flexprice-ts/funcs/invoicesCreateInvoice.js";

// Use `FlexPriceCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const flexPrice = new FlexPriceCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await invoicesCreateInvoice(flexPrice, {
    amountDue: "<value>",
    currency: "Surinam Dollar",
    customerId: "<id>",
    subtotal: "<value>",
    total: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("invoicesCreateInvoice failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [shared.DtoCreateInvoiceRequest](../../sdk/models/shared/dtocreateinvoicerequest.md)                                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.CreateInvoiceResponse](../../sdk/models/operations/createinvoiceresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4XX, 5XX        | \*/\*           |

## finalizeInvoice

Use when locking an invoice for payment (e.g. after review). Once finalized, line items are locked; invoice can be paid or voided.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="finalizeInvoice" method="post" path="/invoices/{id}/finalize" -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.invoices.finalizeInvoice({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { FlexPriceCore } from "flexprice-ts/core.js";
import { invoicesFinalizeInvoice } from "flexprice-ts/funcs/invoicesFinalizeInvoice.js";

// Use `FlexPriceCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const flexPrice = new FlexPriceCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await invoicesFinalizeInvoice(flexPrice, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("invoicesFinalizeInvoice failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.FinalizeInvoiceRequest](../../sdk/models/operations/finalizeinvoicerequest.md)                                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.FinalizeInvoiceResponse](../../sdk/models/operations/finalizeinvoiceresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4XX, 5XX        | \*/\*           |

## getCustomerInvoiceSummary

Use when showing a customer's invoice overview (e.g. billing portal or balance summary). Includes totals and multi-currency breakdown.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getCustomerInvoiceSummary" method="get" path="/customers/{id}/invoices/summary" -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.invoices.getCustomerInvoiceSummary({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { FlexPriceCore } from "flexprice-ts/core.js";
import { invoicesGetCustomerInvoiceSummary } from "flexprice-ts/funcs/invoicesGetCustomerInvoiceSummary.js";

// Use `FlexPriceCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const flexPrice = new FlexPriceCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await invoicesGetCustomerInvoiceSummary(flexPrice, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("invoicesGetCustomerInvoiceSummary failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetCustomerInvoiceSummaryRequest](../../sdk/models/operations/getcustomerinvoicesummaryrequest.md)                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetCustomerInvoiceSummaryResponse](../../sdk/models/operations/getcustomerinvoicesummaryresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4XX, 5XX        | \*/\*           |

## getInvoice

Use when loading an invoice for display or editing (e.g. portal or reconciliation). Supports group_by for usage breakdown and force_runtime_recalculation.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getInvoice" method="get" path="/invoices/{id}" -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.invoices.getInvoice({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { FlexPriceCore } from "flexprice-ts/core.js";
import { invoicesGetInvoice } from "flexprice-ts/funcs/invoicesGetInvoice.js";

// Use `FlexPriceCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const flexPrice = new FlexPriceCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await invoicesGetInvoice(flexPrice, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("invoicesGetInvoice failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetInvoiceRequest](../../sdk/models/operations/getinvoicerequest.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetInvoiceResponse](../../sdk/models/operations/getinvoiceresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4XX, 5XX        | \*/\*           |

## getInvoicePdf

Use when delivering an invoice PDF to the customer (e.g. email attachment or download). Use url=true for a presigned URL instead of binary.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getInvoicePdf" method="get" path="/invoices/{id}/pdf" -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.invoices.getInvoicePdf({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { FlexPriceCore } from "flexprice-ts/core.js";
import { invoicesGetInvoicePdf } from "flexprice-ts/funcs/invoicesGetInvoicePdf.js";

// Use `FlexPriceCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const flexPrice = new FlexPriceCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await invoicesGetInvoicePdf(flexPrice, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("invoicesGetInvoicePdf failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetInvoicePdfRequest](../../sdk/models/operations/getinvoicepdfrequest.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetInvoicePdfResponse](../../sdk/models/operations/getinvoicepdfresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4XX, 5XX        | \*/\*           |

## getInvoicePreview

Use when showing a customer what they will be charged (e.g. preview before checkout or plan change). No invoice is created.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getInvoicePreview" method="post" path="/invoices/preview" -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.invoices.getInvoicePreview({
    subscriptionId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { FlexPriceCore } from "flexprice-ts/core.js";
import { invoicesGetInvoicePreview } from "flexprice-ts/funcs/invoicesGetInvoicePreview.js";

// Use `FlexPriceCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const flexPrice = new FlexPriceCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await invoicesGetInvoicePreview(flexPrice, {
    subscriptionId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("invoicesGetInvoicePreview failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [shared.DtoGetPreviewInvoiceRequest](../../sdk/models/shared/dtogetpreviewinvoicerequest.md)                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetInvoicePreviewResponse](../../sdk/models/operations/getinvoicepreviewresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4XX, 5XX        | \*/\*           |

## queryInvoice

Use when listing or searching invoices (e.g. admin view or customer history). Returns a paginated list; supports filtering by customer, status, date range.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="queryInvoice" method="post" path="/invoices/search" -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.invoices.queryInvoice({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { FlexPriceCore } from "flexprice-ts/core.js";
import { invoicesQueryInvoice } from "flexprice-ts/funcs/invoicesQueryInvoice.js";

// Use `FlexPriceCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const flexPrice = new FlexPriceCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await invoicesQueryInvoice(flexPrice, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("invoicesQueryInvoice failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [shared.TypesInvoiceFilter](../../sdk/models/shared/typesinvoicefilter.md)                                                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.QueryInvoiceResponse](../../sdk/models/operations/queryinvoiceresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4XX, 5XX        | \*/\*           |

## recalculateInvoice

Use when subscription or usage data changed and you need to refresh a draft invoice before finalizing. Optional finalize=true to lock after recalc.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="recalculateInvoice" method="post" path="/invoices/{id}/recalculate" -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.invoices.recalculateInvoice({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { FlexPriceCore } from "flexprice-ts/core.js";
import { invoicesRecalculateInvoice } from "flexprice-ts/funcs/invoicesRecalculateInvoice.js";

// Use `FlexPriceCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const flexPrice = new FlexPriceCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await invoicesRecalculateInvoice(flexPrice, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("invoicesRecalculateInvoice failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.RecalculateInvoiceRequest](../../sdk/models/operations/recalculateinvoicerequest.md)                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.RecalculateInvoiceResponse](../../sdk/models/operations/recalculateinvoiceresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4XX, 5XX        | \*/\*           |

## triggerInvoiceCommsWebhook

Use when sending an invoice to the customer (e.g. trigger email or Slack). Payload includes full invoice details for your integration.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="triggerInvoiceCommsWebhook" method="post" path="/invoices/{id}/comms/trigger" -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.invoices.triggerInvoiceCommsWebhook({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { FlexPriceCore } from "flexprice-ts/core.js";
import { invoicesTriggerInvoiceCommsWebhook } from "flexprice-ts/funcs/invoicesTriggerInvoiceCommsWebhook.js";

// Use `FlexPriceCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const flexPrice = new FlexPriceCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await invoicesTriggerInvoiceCommsWebhook(flexPrice, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("invoicesTriggerInvoiceCommsWebhook failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.TriggerInvoiceCommsWebhookRequest](../../sdk/models/operations/triggerinvoicecommswebhookrequest.md)                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.TriggerInvoiceCommsWebhookResponse](../../sdk/models/operations/triggerinvoicecommswebhookresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4XX, 5XX        | \*/\*           |

## updateInvoice

Use when updating invoice metadata or due date (e.g. PDF URL, net terms). For paid invoices only safe fields can be updated.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="updateInvoice" method="put" path="/invoices/{id}" -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.invoices.updateInvoice({
    id: "<id>",
    dtoUpdateInvoiceRequest: {},
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { FlexPriceCore } from "flexprice-ts/core.js";
import { invoicesUpdateInvoice } from "flexprice-ts/funcs/invoicesUpdateInvoice.js";

// Use `FlexPriceCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const flexPrice = new FlexPriceCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await invoicesUpdateInvoice(flexPrice, {
    id: "<id>",
    dtoUpdateInvoiceRequest: {},
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("invoicesUpdateInvoice failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.UpdateInvoiceRequest](../../sdk/models/operations/updateinvoicerequest.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.UpdateInvoiceResponse](../../sdk/models/operations/updateinvoiceresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4XX, 5XX        | \*/\*           |

## updateInvoicePaymentStatus

Use when reconciling payment status from an external gateway or manual entry (e.g. mark paid after bank confirmation).

### Example Usage

<!-- UsageSnippet language="typescript" operationID="updateInvoicePaymentStatus" method="put" path="/invoices/{id}/payment" -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.invoices.updateInvoicePaymentStatus({
    id: "<id>",
    dtoUpdatePaymentStatusRequest: {
      paymentStatus: "INITIATED",
    },
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { FlexPriceCore } from "flexprice-ts/core.js";
import { invoicesUpdateInvoicePaymentStatus } from "flexprice-ts/funcs/invoicesUpdateInvoicePaymentStatus.js";

// Use `FlexPriceCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const flexPrice = new FlexPriceCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await invoicesUpdateInvoicePaymentStatus(flexPrice, {
    id: "<id>",
    dtoUpdatePaymentStatusRequest: {
      paymentStatus: "INITIATED",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("invoicesUpdateInvoicePaymentStatus failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.UpdateInvoicePaymentStatusRequest](../../sdk/models/operations/updateinvoicepaymentstatusrequest.md)                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.UpdateInvoicePaymentStatusResponse](../../sdk/models/operations/updateinvoicepaymentstatusresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4XX, 5XX        | \*/\*           |

## voidInvoice

Use when cancelling an invoice (e.g. order cancelled or duplicate). Only unpaid invoices can be voided.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="voidInvoice" method="post" path="/invoices/{id}/void" -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.invoices.voidInvoice({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { FlexPriceCore } from "flexprice-ts/core.js";
import { invoicesVoidInvoice } from "flexprice-ts/funcs/invoicesVoidInvoice.js";

// Use `FlexPriceCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const flexPrice = new FlexPriceCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await invoicesVoidInvoice(flexPrice, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("invoicesVoidInvoice failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.VoidInvoiceRequest](../../sdk/models/operations/voidinvoicerequest.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.VoidInvoiceResponse](../../sdk/models/operations/voidinvoiceresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4XX, 5XX        | \*/\*           |