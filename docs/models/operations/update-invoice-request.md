# UpdateInvoiceRequest

## Example Usage

```typescript
import { UpdateInvoiceRequest } from "openapi/models/operations";

let value: UpdateInvoiceRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `id`                                                                         | *string*                                                                     | :heavy_check_mark:                                                           | Invoice ID                                                                   |
| `body`                                                                       | [models.DtoUpdateInvoiceRequest](../../models/dto-update-invoice-request.md) | :heavy_check_mark:                                                           | Invoice Update Request                                                       |