# TriggerScheduledTaskRunRequest

## Example Usage

```typescript
import { TriggerScheduledTaskRunRequest } from "flexprice-ts/sdk/models/operations";

let value: TriggerScheduledTaskRunRequest = {
  id: "<id>",
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `id`                                                                                        | *string*                                                                                    | :heavy_check_mark:                                                                          | Scheduled Task ID                                                                           |
| `dtoTriggerForceRunRequest`                                                                 | [shared.DtoTriggerForceRunRequest](../../../sdk/models/shared/dtotriggerforcerunrequest.md) | :heavy_minus_sign:                                                                          | Optional start and end time for custom range                                                |