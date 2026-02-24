# CancelSubscriptionScheduleRequest

## Example Usage

```typescript
import { CancelSubscriptionScheduleRequest } from "openapi/models/operations";

let value: CancelSubscriptionScheduleRequest = {
  scheduleId: "<id>",
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `scheduleId`                                                                   | *string*                                                                       | :heavy_check_mark:                                                             | Schedule ID (optional if using request body)                                   |
| `body`                                                                         | [models.DtoCancelScheduleRequest](../../models/dto-cancel-schedule-request.md) | :heavy_minus_sign:                                                             | Cancel request (optional if using path parameter)                              |