# DtoCreateBulkPriceResponse

## Example Usage

```typescript
import { DtoCreateBulkPriceResponse } from "flexprice-ts/sdk/models/shared";

let value: DtoCreateBulkPriceResponse = {
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

| Field                                                                       | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `items`                                                                     | [shared.DtoPriceResponse](../../../sdk/models/shared/dtopriceresponse.md)[] | :heavy_minus_sign:                                                          | N/A                                                                         |