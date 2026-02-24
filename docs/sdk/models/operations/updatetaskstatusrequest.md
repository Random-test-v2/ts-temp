# UpdateTaskStatusRequest

## Example Usage

```typescript
import { UpdateTaskStatusRequest } from "flexprice-ts/sdk/models/operations";

let value: UpdateTaskStatusRequest = {
  id: "<id>",
  dtoUpdateTaskStatusRequest: {
    taskStatus: "PROCESSING",
  },
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Task ID                                                                                       |
| `dtoUpdateTaskStatusRequest`                                                                  | [shared.DtoUpdateTaskStatusRequest](../../../sdk/models/shared/dtoupdatetaskstatusrequest.md) | :heavy_check_mark:                                                                            | Status update                                                                                 |