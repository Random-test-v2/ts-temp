# DtoGetUsageAnalyticsResponse

## Example Usage

```typescript
import { DtoGetUsageAnalyticsResponse } from "flexprice-ts/sdk/models/shared";

let value: DtoGetUsageAnalyticsResponse = {
  items: [
    {
      price: {
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
    },
  ],
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `currency`                                                                            | *string*                                                                              | :heavy_minus_sign:                                                                    | N/A                                                                                   |
| `customAnalytics`                                                                     | [shared.DtoCustomAnalyticItem](../../../sdk/models/shared/dtocustomanalyticitem.md)[] | :heavy_minus_sign:                                                                    | N/A                                                                                   |
| `items`                                                                               | [shared.DtoUsageAnalyticItem](../../../sdk/models/shared/dtousageanalyticitem.md)[]   | :heavy_minus_sign:                                                                    | N/A                                                                                   |
| `totalCost`                                                                           | *string*                                                                              | :heavy_minus_sign:                                                                    | N/A                                                                                   |