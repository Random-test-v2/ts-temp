# DtoCreateScheduledTaskRequest

## Example Usage

```typescript
import { DtoCreateScheduledTaskRequest } from "flexprice-ts/sdk/models/shared";

let value: DtoCreateScheduledTaskRequest = {
  connectionId: "<id>",
  entityType: "credit_topups",
  interval: "custom",
  jobConfig: {},
};
```

## Fields

| Field                                                                                             | Type                                                                                              | Required                                                                                          | Description                                                                                       |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `connectionId`                                                                                    | *string*                                                                                          | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `enabled`                                                                                         | *boolean*                                                                                         | :heavy_minus_sign:                                                                                | N/A                                                                                               |
| `entityType`                                                                                      | [shared.TypesScheduledTaskEntityType](../../../sdk/models/shared/typesscheduledtaskentitytype.md) | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `interval`                                                                                        | [shared.TypesScheduledTaskInterval](../../../sdk/models/shared/typesscheduledtaskinterval.md)     | :heavy_check_mark:                                                                                | N/A                                                                                               |
| `jobConfig`                                                                                       | [shared.TypesS3JobConfig](../../../sdk/models/shared/typess3jobconfig.md)                         | :heavy_check_mark:                                                                                | N/A                                                                                               |