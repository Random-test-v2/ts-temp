# DtoTenantBillingUsage

## Example Usage

```typescript
import { DtoTenantBillingUsage } from "flexprice-ts/sdk/models/shared";

let value: DtoTenantBillingUsage = {
  subscriptions: [
    {
      latestInvoice: {
        subscription: {
          plan: {},
        },
      },
      plan: {},
    },
  ],
  usage: {
    features: [
      {
        feature: {
          meter: {
            createdAt: "2024-03-20T15:04:05Z",
            eventName: "api_request",
            id: "550e8400-e29b-41d4-a716-446655440000",
            name: "API Usage Meter",
            status: "published",
            tenantId: "tenant123",
            updatedAt: "2024-03-20T15:04:05Z",
          },
        },
      },
    ],
  },
};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `subscriptions`                                                                                         | [shared.DtoSubscriptionResponse](../../../sdk/models/shared/dtosubscriptionresponse.md)[]               | :heavy_minus_sign:                                                                                      | N/A                                                                                                     |
| `usage`                                                                                                 | [shared.DtoCustomerUsageSummaryResponse](../../../sdk/models/shared/dtocustomerusagesummaryresponse.md) | :heavy_minus_sign:                                                                                      | N/A                                                                                                     |