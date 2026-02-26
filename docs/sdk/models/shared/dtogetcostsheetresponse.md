# DtoGetCostsheetResponse

## Example Usage

```typescript
import { DtoGetCostsheetResponse } from "flexprice-ts/sdk/models/shared";

let value: DtoGetCostsheetResponse = {
  costsheet: {
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
};
```

## Fields

| Field                                                                             | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `costsheet`                                                                       | [shared.DtoCostsheetResponse](../../../sdk/models/shared/dtocostsheetresponse.md) | :heavy_minus_sign:                                                                | N/A                                                                               |