# ListTasksRequest

## Example Usage

```typescript
import { ListTasksRequest } from "openapi/models/operations";

let value: ListTasksRequest = {};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `createdBy`                                                                | *string*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |
| `endTime`                                                                  | *string*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |
| `entityType`                                                               | [operations.EntityType](../../models/operations/entity-type.md)            | :heavy_minus_sign:                                                         | N/A                                                                        |
| `expand`                                                                   | *string*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |
| `limit`                                                                    | *number*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |
| `offset`                                                                   | *number*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |
| `order`                                                                    | [operations.ListTasksOrder](../../models/operations/list-tasks-order.md)   | :heavy_minus_sign:                                                         | N/A                                                                        |
| `scheduledTaskId`                                                          | *string*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |
| `sort`                                                                     | *string*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |
| `startTime`                                                                | *string*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |
| `status`                                                                   | [operations.ListTasksStatus](../../models/operations/list-tasks-status.md) | :heavy_minus_sign:                                                         | N/A                                                                        |
| `taskStatus`                                                               | [operations.TaskStatus](../../models/operations/task-status.md)            | :heavy_minus_sign:                                                         | N/A                                                                        |
| `taskType`                                                                 | [operations.TaskType](../../models/operations/task-type.md)                | :heavy_minus_sign:                                                         | N/A                                                                        |