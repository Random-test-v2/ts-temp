# PostPlansIdCloneRequest

## Example Usage

```typescript
import { PostPlansIdCloneRequest } from "openapi/models/operations";

let value: PostPlansIdCloneRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `id`                                                                 | *string*                                                             | :heavy_check_mark:                                                   | Source Plan ID                                                       |
| `body`                                                               | [models.DtoClonePlanRequest](../../models/dto-clone-plan-request.md) | :heavy_check_mark:                                                   | Clone configuration                                                  |