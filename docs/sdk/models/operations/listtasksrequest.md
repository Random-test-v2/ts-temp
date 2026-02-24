# ListTasksRequest

## Example Usage

```typescript
import { ListTasksRequest } from "flexprice-ts/sdk/models/operations";

let value: ListTasksRequest = {};
```

## Fields

| Field                                                                           | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `createdBy`                                                                     | *string*                                                                        | :heavy_minus_sign:                                                              | N/A                                                                             |
| `endTime`                                                                       | *string*                                                                        | :heavy_minus_sign:                                                              | N/A                                                                             |
| `entityType`                                                                    | [operations.EntityType](../../../sdk/models/operations/entitytype.md)           | :heavy_minus_sign:                                                              | N/A                                                                             |
| `expand`                                                                        | *string*                                                                        | :heavy_minus_sign:                                                              | N/A                                                                             |
| `limit`                                                                         | *number*                                                                        | :heavy_minus_sign:                                                              | N/A                                                                             |
| `offset`                                                                        | *number*                                                                        | :heavy_minus_sign:                                                              | N/A                                                                             |
| `order`                                                                         | [operations.ListTasksOrder](../../../sdk/models/operations/listtasksorder.md)   | :heavy_minus_sign:                                                              | N/A                                                                             |
| `scheduledTaskId`                                                               | *string*                                                                        | :heavy_minus_sign:                                                              | N/A                                                                             |
| `sort`                                                                          | *string*                                                                        | :heavy_minus_sign:                                                              | N/A                                                                             |
| `startTime`                                                                     | *string*                                                                        | :heavy_minus_sign:                                                              | N/A                                                                             |
| `status`                                                                        | [operations.ListTasksStatus](../../../sdk/models/operations/listtasksstatus.md) | :heavy_minus_sign:                                                              | N/A                                                                             |
| `taskStatus`                                                                    | [operations.TaskStatus](../../../sdk/models/operations/taskstatus.md)           | :heavy_minus_sign:                                                              | N/A                                                                             |
| `taskType`                                                                      | [operations.TaskType](../../../sdk/models/operations/tasktype.md)               | :heavy_minus_sign:                                                              | N/A                                                                             |