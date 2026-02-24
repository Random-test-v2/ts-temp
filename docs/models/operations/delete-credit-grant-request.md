# DeleteCreditGrantRequest

## Example Usage

```typescript
import { DeleteCreditGrantRequest } from "openapi/models/operations";

let value: DeleteCreditGrantRequest = {
  id: "<id>",
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `id`                                                                                  | *string*                                                                              | :heavy_check_mark:                                                                    | Credit Grant ID                                                                       |
| `body`                                                                                | [models.DtoDeleteCreditGrantRequest](../../models/dto-delete-credit-grant-request.md) | :heavy_minus_sign:                                                                    | Optional: effective_date for subscription-scoped grants                               |