# DtoCreateTaskRequest

## Example Usage

```typescript
import { DtoCreateTaskRequest } from "openapi/models";

let value: DtoCreateTaskRequest = {
  entityType: "FEATURES",
  fileType: "JSON",
  fileUrl: "https://necessary-wombat.net/",
  taskType: "IMPORT",
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `entityType`                                             | [models.TypesEntityType](../models/types-entity-type.md) | :heavy_check_mark:                                       | N/A                                                      |
| `fileName`                                               | *string*                                                 | :heavy_minus_sign:                                       | N/A                                                      |
| `fileType`                                               | [models.TypesFileType](../models/types-file-type.md)     | :heavy_check_mark:                                       | N/A                                                      |
| `fileUrl`                                                | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `metadata`                                               | Record<string, *any*>                                    | :heavy_minus_sign:                                       | N/A                                                      |
| `taskType`                                               | [models.TypesTaskType](../models/types-task-type.md)     | :heavy_check_mark:                                       | N/A                                                      |