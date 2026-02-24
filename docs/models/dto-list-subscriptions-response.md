# DtoListSubscriptionsResponse

## Example Usage

```typescript
import { DtoListSubscriptionsResponse } from "openapi/models";

let value: DtoListSubscriptionsResponse = {
  items: [
    {
      latestInvoice: {
        subscription: {
          plan: {},
        },
      },
      plan: {},
    },
  ],
};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `items`                                                                    | [models.DtoSubscriptionResponse](../models/dto-subscription-response.md)[] | :heavy_minus_sign:                                                         | N/A                                                                        |
| `pagination`                                                               | [models.TypesPaginationResponse](../models/types-pagination-response.md)   | :heavy_minus_sign:                                                         | N/A                                                                        |