# UpdateScheduledTaskRequest

## Example Usage

```typescript
import { UpdateScheduledTaskRequest } from "flexprice-ts/sdk/models/operations";

let value: UpdateScheduledTaskRequest = {
  id: "<id>",
  dtoUpdateScheduledTaskRequest: {
    enabled: false,
  },
};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `id`                                                                                                | *string*                                                                                            | :heavy_check_mark:                                                                                  | Scheduled Task ID                                                                                   |
| `dtoUpdateScheduledTaskRequest`                                                                     | [shared.DtoUpdateScheduledTaskRequest](../../../sdk/models/shared/dtoupdatescheduledtaskrequest.md) | :heavy_check_mark:                                                                                  | Update request (enabled: true/false to pause/resume)                                                |