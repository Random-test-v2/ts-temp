# DtoCreateScheduledTaskRequest

## Example Usage

```typescript
import { DtoCreateScheduledTaskRequest } from "openapi/models";

let value: DtoCreateScheduledTaskRequest = {
  connectionId: "<id>",
  entityType: "credit_topups",
  interval: "custom",
  jobConfig: {},
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `connectionId`                                                                       | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `enabled`                                                                            | *boolean*                                                                            | :heavy_minus_sign:                                                                   | N/A                                                                                  |
| `entityType`                                                                         | [models.TypesScheduledTaskEntityType](../models/types-scheduled-task-entity-type.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `interval`                                                                           | [models.TypesScheduledTaskInterval](../models/types-scheduled-task-interval.md)      | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `jobConfig`                                                                          | [models.TypesS3JobConfig](../models/types-s3-job-config.md)                          | :heavy_check_mark:                                                                   | N/A                                                                                  |