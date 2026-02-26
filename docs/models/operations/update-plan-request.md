# UpdatePlanRequest

## Example Usage

```typescript
import { UpdatePlanRequest } from "openapi/models/operations";

let value: UpdatePlanRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `id`                                                                   | *string*                                                               | :heavy_check_mark:                                                     | Plan ID                                                                |
| `body`                                                                 | [models.DtoUpdatePlanRequest](../../models/dto-update-plan-request.md) | :heavy_check_mark:                                                     | Plan update                                                            |