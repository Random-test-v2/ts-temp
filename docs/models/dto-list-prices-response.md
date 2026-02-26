# DtoListPricesResponse

## Example Usage

```typescript
import { DtoListPricesResponse } from "openapi/models";

let value: DtoListPricesResponse = {
  items: [
    {
      addon: {
        prices: [
          {
            addon: {},
            meter: {
              createdAt: "2024-03-20T15:04:05Z",
              eventName: "api_request",
              id: "550e8400-e29b-41d4-a716-446655440000",
              name: "API Usage Meter",
              status: "published",
              tenantId: "tenant123",
              updatedAt: "2024-03-20T15:04:05Z",
            },
            plan: {},
          },
        ],
      },
      meter: {
        createdAt: "2024-03-20T15:04:05Z",
        eventName: "api_request",
        id: "550e8400-e29b-41d4-a716-446655440000",
        name: "API Usage Meter",
        status: "published",
        tenantId: "tenant123",
        updatedAt: "2024-03-20T15:04:05Z",
      },
      plan: {},
    },
  ],
};
```

## Fields

| Field                                                                    | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `items`                                                                  | [models.DtoPriceResponse](../models/dto-price-response.md)[]             | :heavy_minus_sign:                                                       | N/A                                                                      |
| `pagination`                                                             | [models.TypesPaginationResponse](../models/types-pagination-response.md) | :heavy_minus_sign:                                                       | N/A                                                                      |