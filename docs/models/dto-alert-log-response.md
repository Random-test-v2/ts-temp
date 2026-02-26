# DtoAlertLogResponse

## Example Usage

```typescript
import { DtoAlertLogResponse } from "openapi/models";

let value: DtoAlertLogResponse = {
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
};
```

## Fields

| Field                                                               | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `alertInfo`                                                         | [models.TypesAlertInfo](../models/types-alert-info.md)              | :heavy_minus_sign:                                                  | N/A                                                                 |
| `alertStatus`                                                       | [models.TypesAlertState](../models/types-alert-state.md)            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `alertType`                                                         | [models.TypesAlertType](../models/types-alert-type.md)              | :heavy_minus_sign:                                                  | N/A                                                                 |
| `createdAt`                                                         | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `createdBy`                                                         | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `customer`                                                          | [models.DtoCustomerResponse](../models/dto-customer-response.md)    | :heavy_minus_sign:                                                  | Customer response object containing all customer information        |
| `customerId`                                                        | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `entityId`                                                          | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `entityType`                                                        | [models.TypesAlertEntityType](../models/types-alert-entity-type.md) | :heavy_minus_sign:                                                  | N/A                                                                 |
| `environmentId`                                                     | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `feature`                                                           | [models.DtoFeatureResponse](../models/dto-feature-response.md)      | :heavy_minus_sign:                                                  | N/A                                                                 |
| `id`                                                                | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `parentEntityId`                                                    | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `parentEntityType`                                                  | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `status`                                                            | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `tenantId`                                                          | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `updatedAt`                                                         | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `updatedBy`                                                         | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `wallet`                                                            | [models.DtoWalletResponse](../models/dto-wallet-response.md)        | :heavy_minus_sign:                                                  | N/A                                                                 |