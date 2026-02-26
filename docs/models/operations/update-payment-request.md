# UpdatePaymentRequest

## Example Usage

```typescript
import { UpdatePaymentRequest } from "openapi/models/operations";

let value: UpdatePaymentRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `id`                                                                         | *string*                                                                     | :heavy_check_mark:                                                           | Payment ID                                                                   |
| `body`                                                                       | [models.DtoUpdatePaymentRequest](../../models/dto-update-payment-request.md) | :heavy_check_mark:                                                           | Payment configuration                                                        |