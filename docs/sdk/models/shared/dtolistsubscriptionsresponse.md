# DtoListSubscriptionsResponse

## Example Usage

```typescript
import { DtoListSubscriptionsResponse } from "flexprice-ts/sdk/models/shared";

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

| Field                                                                                     | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `items`                                                                                   | [shared.DtoSubscriptionResponse](../../../sdk/models/shared/dtosubscriptionresponse.md)[] | :heavy_minus_sign:                                                                        | N/A                                                                                       |
| `pagination`                                                                              | [shared.TypesPaginationResponse](../../../sdk/models/shared/typespaginationresponse.md)   | :heavy_minus_sign:                                                                        | N/A                                                                                       |