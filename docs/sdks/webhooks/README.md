# Webhooks

## Overview

### Available Operations

* [handleChargebeeWebhook](#handlechargebeewebhook) - Handle Chargebee webhook events
* [handleHubspotWebhook](#handlehubspotwebhook) - Handle HubSpot webhook events
* [handleMoyasarWebhook](#handlemoyasarwebhook) - Handle Moyasar webhook events
* [handleNomodWebhook](#handlenomodwebhook) - Handle Nomod webhook events
* [handleQuickbooksWebhook](#handlequickbookswebhook) - Handle QuickBooks webhook events
* [handleRazorpayWebhook](#handlerazorpaywebhook) - Handle Razorpay webhook events
* [handleStripeWebhook](#handlestripewebhook) - Handle Stripe webhook events

## handleChargebeeWebhook

Use as the Chargebee webhook endpoint URL. Receives payment and subscription events from Chargebee to sync status into FlexPrice.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="handleChargebeeWebhook" method="post" path="/webhooks/chargebee/{tenant_id}/{environment_id}" -->
```typescript
import { SDK } from "openapi";

const sdk = new SDK({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await sdk.webhooks.handleChargebeeWebhook({
    tenantId: "<id>",
    environmentId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SDKCore } from "openapi/core.js";
import { webhooksHandleChargebeeWebhook } from "openapi/funcs/webhooks-handle-chargebee-webhook.js";

// Use `SDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const sdk = new SDKCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await webhooksHandleChargebeeWebhook(sdk, {
    tenantId: "<id>",
    environmentId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webhooksHandleChargebeeWebhook failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.HandleChargebeeWebhookRequest](../../models/operations/handle-chargebee-webhook-request.md)                                                                        | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[{ [k: string]: any }](../../models/.md)\>**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| errors.SDKDefaultError | 4XX, 5XX               | \*/\*                  |

## handleHubspotWebhook

Use as the HubSpot webhook endpoint URL. Receives deal and customer events (e.g. deal closed won) to create or update customers in FlexPrice.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="handleHubspotWebhook" method="post" path="/webhooks/hubspot/{tenant_id}/{environment_id}" -->
```typescript
import { SDK } from "openapi";

const sdk = new SDK({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await sdk.webhooks.handleHubspotWebhook({
    tenantId: "<id>",
    environmentId: "<id>",
    xHubSpotSignatureV3: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SDKCore } from "openapi/core.js";
import { webhooksHandleHubspotWebhook } from "openapi/funcs/webhooks-handle-hubspot-webhook.js";

// Use `SDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const sdk = new SDKCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await webhooksHandleHubspotWebhook(sdk, {
    tenantId: "<id>",
    environmentId: "<id>",
    xHubSpotSignatureV3: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webhooksHandleHubspotWebhook failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.HandleHubspotWebhookRequest](../../models/operations/handle-hubspot-webhook-request.md)                                                                            | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[{ [k: string]: any }](../../models/.md)\>**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| errors.SDKDefaultError | 4XX, 5XX               | \*/\*                  |

## handleMoyasarWebhook

Use as the Moyasar webhook endpoint URL. Receives payment events from Moyasar to update payment status in FlexPrice.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="handleMoyasarWebhook" method="post" path="/webhooks/moyasar/{tenant_id}/{environment_id}" -->
```typescript
import { SDK } from "openapi";

const sdk = new SDK({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await sdk.webhooks.handleMoyasarWebhook({
    tenantId: "<id>",
    environmentId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SDKCore } from "openapi/core.js";
import { webhooksHandleMoyasarWebhook } from "openapi/funcs/webhooks-handle-moyasar-webhook.js";

// Use `SDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const sdk = new SDKCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await webhooksHandleMoyasarWebhook(sdk, {
    tenantId: "<id>",
    environmentId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webhooksHandleMoyasarWebhook failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.HandleMoyasarWebhookRequest](../../models/operations/handle-moyasar-webhook-request.md)                                                                            | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[{ [k: string]: any }](../../models/.md)\>**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| errors.SDKDefaultError | 4XX, 5XX               | \*/\*                  |

## handleNomodWebhook

Use as the Nomod webhook endpoint URL. Receives payment and invoice events from Nomod to keep FlexPrice in sync.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="handleNomodWebhook" method="post" path="/webhooks/nomod/{tenant_id}/{environment_id}" -->
```typescript
import { SDK } from "openapi";

const sdk = new SDK({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await sdk.webhooks.handleNomodWebhook({
    tenantId: "<id>",
    environmentId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SDKCore } from "openapi/core.js";
import { webhooksHandleNomodWebhook } from "openapi/funcs/webhooks-handle-nomod-webhook.js";

// Use `SDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const sdk = new SDKCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await webhooksHandleNomodWebhook(sdk, {
    tenantId: "<id>",
    environmentId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webhooksHandleNomodWebhook failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.HandleNomodWebhookRequest](../../models/operations/handle-nomod-webhook-request.md)                                                                                | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[{ [k: string]: any }](../../models/.md)\>**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| errors.SDKDefaultError | 4XX, 5XX               | \*/\*                  |

## handleQuickbooksWebhook

Use as the QuickBooks webhook endpoint URL. Receives payment events from QuickBooks to sync payment status into FlexPrice.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="handleQuickbooksWebhook" method="post" path="/webhooks/quickbooks/{tenant_id}/{environment_id}" -->
```typescript
import { SDK } from "openapi";

const sdk = new SDK({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await sdk.webhooks.handleQuickbooksWebhook({
    tenantId: "<id>",
    environmentId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SDKCore } from "openapi/core.js";
import { webhooksHandleQuickbooksWebhook } from "openapi/funcs/webhooks-handle-quickbooks-webhook.js";

// Use `SDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const sdk = new SDKCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await webhooksHandleQuickbooksWebhook(sdk, {
    tenantId: "<id>",
    environmentId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webhooksHandleQuickbooksWebhook failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.HandleQuickbooksWebhookRequest](../../models/operations/handle-quickbooks-webhook-request.md)                                                                      | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[{ [k: string]: any }](../../models/.md)\>**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| errors.SDKDefaultError | 4XX, 5XX               | \*/\*                  |

## handleRazorpayWebhook

Use as the Razorpay webhook endpoint URL. Receives payment capture and failure events to update invoice or payment status in FlexPrice.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="handleRazorpayWebhook" method="post" path="/webhooks/razorpay/{tenant_id}/{environment_id}" -->
```typescript
import { SDK } from "openapi";

const sdk = new SDK({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await sdk.webhooks.handleRazorpayWebhook({
    tenantId: "<id>",
    environmentId: "<id>",
    xRazorpaySignature: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SDKCore } from "openapi/core.js";
import { webhooksHandleRazorpayWebhook } from "openapi/funcs/webhooks-handle-razorpay-webhook.js";

// Use `SDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const sdk = new SDKCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await webhooksHandleRazorpayWebhook(sdk, {
    tenantId: "<id>",
    environmentId: "<id>",
    xRazorpaySignature: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webhooksHandleRazorpayWebhook failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.HandleRazorpayWebhookRequest](../../models/operations/handle-razorpay-webhook-request.md)                                                                          | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[{ [k: string]: any }](../../models/.md)\>**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| errors.SDKDefaultError | 4XX, 5XX               | \*/\*                  |

## handleStripeWebhook

Use as the Stripe webhook endpoint URL. Receives payment and customer events from Stripe to keep FlexPrice in sync (e.g. payment succeeded, customer created).

### Example Usage

<!-- UsageSnippet language="typescript" operationID="handleStripeWebhook" method="post" path="/webhooks/stripe/{tenant_id}/{environment_id}" -->
```typescript
import { SDK } from "openapi";

const sdk = new SDK({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await sdk.webhooks.handleStripeWebhook({
    tenantId: "<id>",
    environmentId: "<id>",
    stripeSignature: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { SDKCore } from "openapi/core.js";
import { webhooksHandleStripeWebhook } from "openapi/funcs/webhooks-handle-stripe-webhook.js";

// Use `SDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const sdk = new SDKCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await webhooksHandleStripeWebhook(sdk, {
    tenantId: "<id>",
    environmentId: "<id>",
    stripeSignature: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webhooksHandleStripeWebhook failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.HandleStripeWebhookRequest](../../models/operations/handle-stripe-webhook-request.md)                                                                              | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[{ [k: string]: any }](../../models/.md)\>**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| errors.SDKDefaultError | 4XX, 5XX               | \*/\*                  |