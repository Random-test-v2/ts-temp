# DtoListInvoicesResponse

## Example Usage

```typescript
import { DtoListInvoicesResponse } from "openapi/models";

let value: DtoListInvoicesResponse = {
  items: [
    {
      subscription: {
        latestInvoice: {
          subscription: {
            plan: {},
          },
        },
        plan: {},
      },
    },
  ],
};
```

## Fields

| Field                                                                    | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `items`                                                                  | [models.DtoInvoiceResponse](../models/dto-invoice-response.md)[]         | :heavy_minus_sign:                                                       | N/A                                                                      |
| `pagination`                                                             | [models.TypesPaginationResponse](../models/types-pagination-response.md) | :heavy_minus_sign:                                                       | N/A                                                                      |