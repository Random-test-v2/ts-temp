# UpdateCreditGrantRequest

## Example Usage

```typescript
import { UpdateCreditGrantRequest } from "openapi/models/operations";

let value: UpdateCreditGrantRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `id`                                                                                  | *string*                                                                              | :heavy_check_mark:                                                                    | Credit Grant ID                                                                       |
| `body`                                                                                | [models.DtoUpdateCreditGrantRequest](../../models/dto-update-credit-grant-request.md) | :heavy_check_mark:                                                                    | Credit Grant configuration                                                            |