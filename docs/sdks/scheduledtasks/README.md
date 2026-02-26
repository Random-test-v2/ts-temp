# ScheduledTasks

## Overview

### Available Operations

* [createScheduledTask](#createscheduledtask) - Create scheduled task
* [deleteScheduledTask](#deletescheduledtask) - Delete a scheduled task
* [getScheduledTask](#getscheduledtask) - Get scheduled task
* [listScheduledTasks](#listscheduledtasks) - List scheduled tasks
* [scheduleUpdateBillingPeriod](#scheduleupdatebillingperiod) - Schedule update billing period
* [triggerScheduledTaskRun](#triggerscheduledtaskrun) - Trigger force run
* [updateScheduledTask](#updatescheduledtask) - Update a scheduled task

## createScheduledTask

Use when setting up recurring data exports or other scheduled jobs. Ideal for report generation or syncing data on a schedule.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="createScheduledTask" method="post" path="/tasks/scheduled" -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.scheduledTasks.createScheduledTask({
    connectionId: "<id>",
    entityType: "credit_topups",
    interval: "hourly",
    jobConfig: {},
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { FlexPriceCore } from "flexprice-ts/core.js";
import { scheduledTasksCreateScheduledTask } from "flexprice-ts/funcs/scheduledTasksCreateScheduledTask.js";

// Use `FlexPriceCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const flexPrice = new FlexPriceCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await scheduledTasksCreateScheduledTask(flexPrice, {
    connectionId: "<id>",
    entityType: "credit_topups",
    interval: "hourly",
    jobConfig: {},
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("scheduledTasksCreateScheduledTask failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [shared.DtoCreateScheduledTaskRequest](../../sdk/models/shared/dtocreatescheduledtaskrequest.md)                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.CreateScheduledTaskResponse](../../sdk/models/operations/createscheduledtaskresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4XX, 5XX        | \*/\*           |

## deleteScheduledTask

Use when removing a scheduled task from the active roster. Archives the task and removes it from the scheduler (soft delete).

### Example Usage

<!-- UsageSnippet language="typescript" operationID="deleteScheduledTask" method="delete" path="/tasks/scheduled/{id}" -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.scheduledTasks.deleteScheduledTask({
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
import { scheduledTasksDeleteScheduledTask } from "flexprice-ts/funcs/scheduledTasksDeleteScheduledTask.js";

// Use `FlexPriceCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const flexPrice = new FlexPriceCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await scheduledTasksDeleteScheduledTask(flexPrice, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("scheduledTasksDeleteScheduledTask failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.DeleteScheduledTaskRequest](../../sdk/models/operations/deletescheduledtaskrequest.md)                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[shared.ErrorsErrorResponse](../../sdk/models/shared/errorserrorresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4XX, 5XX        | \*/\*           |

## getScheduledTask

Use when you need to load a single scheduled task (e.g. to show details in a UI or check its configuration).

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getScheduledTask" method="get" path="/tasks/scheduled/{id}" -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.scheduledTasks.getScheduledTask({
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
import { scheduledTasksGetScheduledTask } from "flexprice-ts/funcs/scheduledTasksGetScheduledTask.js";

// Use `FlexPriceCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const flexPrice = new FlexPriceCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await scheduledTasksGetScheduledTask(flexPrice, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("scheduledTasksGetScheduledTask failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetScheduledTaskRequest](../../sdk/models/operations/getscheduledtaskrequest.md)                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetScheduledTaskResponse](../../sdk/models/operations/getscheduledtaskresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4XX, 5XX        | \*/\*           |

## listScheduledTasks

Use when listing or managing scheduled tasks in an admin UI. Returns a list; supports filtering by status, type, and pagination.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="listScheduledTasks" method="get" path="/tasks/scheduled" -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.scheduledTasks.listScheduledTasks();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { FlexPriceCore } from "flexprice-ts/core.js";
import { scheduledTasksListScheduledTasks } from "flexprice-ts/funcs/scheduledTasksListScheduledTasks.js";

// Use `FlexPriceCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const flexPrice = new FlexPriceCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await scheduledTasksListScheduledTasks(flexPrice);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("scheduledTasksListScheduledTasks failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListScheduledTasksRequest](../../sdk/models/operations/listscheduledtasksrequest.md)                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListScheduledTasksResponse](../../sdk/models/operations/listscheduledtasksresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4XX, 5XX        | \*/\*           |

## scheduleUpdateBillingPeriod

Use when you need to trigger a billing-period update workflow (e.g. to recalculate or sync billing windows).

### Example Usage

<!-- UsageSnippet language="typescript" operationID="scheduleUpdateBillingPeriod" method="post" path="/tasks/scheduled/schedule-update-billing-period" -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.scheduledTasks.scheduleUpdateBillingPeriod({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { FlexPriceCore } from "flexprice-ts/core.js";
import { scheduledTasksScheduleUpdateBillingPeriod } from "flexprice-ts/funcs/scheduledTasksScheduleUpdateBillingPeriod.js";

// Use `FlexPriceCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const flexPrice = new FlexPriceCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await scheduledTasksScheduleUpdateBillingPeriod(flexPrice, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("scheduledTasksScheduleUpdateBillingPeriod failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ScheduleUpdateBillingPeriodRequest](../../sdk/models/operations/scheduleupdatebillingperiodrequest.md)                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ScheduleUpdateBillingPeriodResponse](../../sdk/models/operations/scheduleupdatebillingperiodresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4XX, 5XX        | \*/\*           |

## triggerScheduledTaskRun

Use when you need to run a scheduled export immediately (e.g. on-demand report or catch-up). Supports optional custom time range.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="triggerScheduledTaskRun" method="post" path="/tasks/scheduled/{id}/run" -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.scheduledTasks.triggerScheduledTaskRun({
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
import { scheduledTasksTriggerScheduledTaskRun } from "flexprice-ts/funcs/scheduledTasksTriggerScheduledTaskRun.js";

// Use `FlexPriceCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const flexPrice = new FlexPriceCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await scheduledTasksTriggerScheduledTaskRun(flexPrice, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("scheduledTasksTriggerScheduledTaskRun failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.TriggerScheduledTaskRunRequest](../../sdk/models/operations/triggerscheduledtaskrunrequest.md)                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.TriggerScheduledTaskRunResponse](../../sdk/models/operations/triggerscheduledtaskrunresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4XX, 5XX        | \*/\*           |

## updateScheduledTask

Use when pausing or resuming a scheduled task. Only the enabled field can be changed.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="updateScheduledTask" method="put" path="/tasks/scheduled/{id}" -->
```typescript
import { FlexPrice } from "flexprice-ts";

const flexPrice = new FlexPrice({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await flexPrice.scheduledTasks.updateScheduledTask({
    id: "<id>",
    dtoUpdateScheduledTaskRequest: {
      enabled: false,
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
import { scheduledTasksUpdateScheduledTask } from "flexprice-ts/funcs/scheduledTasksUpdateScheduledTask.js";

// Use `FlexPriceCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const flexPrice = new FlexPriceCore({
  serverURL: "https://api.example.com",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await scheduledTasksUpdateScheduledTask(flexPrice, {
    id: "<id>",
    dtoUpdateScheduledTaskRequest: {
      enabled: false,
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("scheduledTasksUpdateScheduledTask failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.UpdateScheduledTaskRequest](../../sdk/models/operations/updatescheduledtaskrequest.md)                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.UpdateScheduledTaskResponse](../../sdk/models/operations/updatescheduledtaskresponse.md)\>**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4XX, 5XX        | \*/\*           |