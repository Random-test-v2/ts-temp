# DtoCreateTaskRequest

## Example Usage

```typescript
import { DtoCreateTaskRequest } from "flexprice-ts/sdk/models/shared";

let value: DtoCreateTaskRequest = {
  entityType: "FEATURES",
  fileType: "JSON",
  fileUrl: "https://necessary-wombat.net/",
  taskType: "IMPORT",
};
```

## Fields

| Field                                                                   | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `entityType`                                                            | [shared.TypesEntityType](../../../sdk/models/shared/typesentitytype.md) | :heavy_check_mark:                                                      | N/A                                                                     |
| `fileName`                                                              | *string*                                                                | :heavy_minus_sign:                                                      | N/A                                                                     |
| `fileType`                                                              | [shared.TypesFileType](../../../sdk/models/shared/typesfiletype.md)     | :heavy_check_mark:                                                      | N/A                                                                     |
| `fileUrl`                                                               | *string*                                                                | :heavy_check_mark:                                                      | N/A                                                                     |
| `metadata`                                                              | Record<string, *any*>                                                   | :heavy_minus_sign:                                                      | N/A                                                                     |
| `taskType`                                                              | [shared.TypesTaskType](../../../sdk/models/shared/typestasktype.md)     | :heavy_check_mark:                                                      | N/A                                                                     |