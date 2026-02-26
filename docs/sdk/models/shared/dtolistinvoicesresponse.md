# DtoListInvoicesResponse

## Example Usage

```typescript
import { DtoListInvoicesResponse } from "flexprice-ts/sdk/models/shared";

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

| Field                                                                                   | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `items`                                                                                 | [shared.DtoInvoiceResponse](../../../sdk/models/shared/dtoinvoiceresponse.md)[]         | :heavy_minus_sign:                                                                      | N/A                                                                                     |
| `pagination`                                                                            | [shared.TypesPaginationResponse](../../../sdk/models/shared/typespaginationresponse.md) | :heavy_minus_sign:                                                                      | N/A                                                                                     |