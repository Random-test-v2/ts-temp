# CancelSubscriptionScheduleRequest

## Example Usage

```typescript
import { CancelSubscriptionScheduleRequest } from "flexprice-ts/sdk/models/operations";

let value: CancelSubscriptionScheduleRequest = {
  scheduleId: "<id>",
};
```

## Fields

| Field                                                                                     | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `scheduleId`                                                                              | *string*                                                                                  | :heavy_check_mark:                                                                        | Schedule ID (optional if using request body)                                              |
| `dtoCancelScheduleRequest`                                                                | [shared.DtoCancelScheduleRequest](../../../sdk/models/shared/dtocancelschedulerequest.md) | :heavy_minus_sign:                                                                        | Cancel request (optional if using path parameter)                                         |