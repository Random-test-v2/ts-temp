# DtoFeatureResponse

## Example Usage

```typescript
import { DtoFeatureResponse } from "flexprice-ts/sdk/models/shared";

let value: DtoFeatureResponse = {
  meter: {
    createdAt: "2024-03-20T15:04:05Z",
    eventName: "api_request",
    id: "550e8400-e29b-41d4-a716-446655440000",
    name: "API Usage Meter",
    status: "published",
    tenantId: "tenant123",
    updatedAt: "2024-03-20T15:04:05Z",
  },
};
```

## Fields

| Field                                                                         | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `alertSettings`                                                               | [shared.TypesAlertSettings](../../../sdk/models/shared/typesalertsettings.md) | :heavy_minus_sign:                                                            | N/A                                                                           |
| `createdAt`                                                                   | *string*                                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |
| `createdBy`                                                                   | *string*                                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |
| `description`                                                                 | *string*                                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |
| `environmentId`                                                               | *string*                                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |
| `id`                                                                          | *string*                                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |
| `lookupKey`                                                                   | *string*                                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |
| `metadata`                                                                    | Record<string, *string*>                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |
| `meter`                                                                       | [shared.DtoMeterResponse](../../../sdk/models/shared/dtometerresponse.md)     | :heavy_minus_sign:                                                            | N/A                                                                           |
| `meterId`                                                                     | *string*                                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |
| `name`                                                                        | *string*                                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |
| `status`                                                                      | [shared.TypesStatus](../../../sdk/models/shared/typesstatus.md)               | :heavy_minus_sign:                                                            | N/A                                                                           |
| `tenantId`                                                                    | *string*                                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |
| `type`                                                                        | [shared.TypesFeatureType](../../../sdk/models/shared/typesfeaturetype.md)     | :heavy_minus_sign:                                                            | N/A                                                                           |
| `unitPlural`                                                                  | *string*                                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |
| `unitSingular`                                                                | *string*                                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |
| `updatedAt`                                                                   | *string*                                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |
| `updatedBy`                                                                   | *string*                                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |