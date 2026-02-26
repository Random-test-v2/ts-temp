# UpdateCostsheetRequest

## Example Usage

```typescript
import { UpdateCostsheetRequest } from "openapi/models/operations";

let value: UpdateCostsheetRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `id`                                                                             | *string*                                                                         | :heavy_check_mark:                                                               | Costsheet ID                                                                     |
| `body`                                                                           | [models.DtoUpdateCostsheetRequest](../../models/dto-update-costsheet-request.md) | :heavy_check_mark:                                                               | Costsheet configuration                                                          |