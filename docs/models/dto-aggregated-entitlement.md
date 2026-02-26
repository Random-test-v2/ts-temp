# DtoAggregatedEntitlement

## Example Usage

```typescript
import { DtoAggregatedEntitlement } from "openapi/models";

let value: DtoAggregatedEntitlement = {};
```

## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `isEnabled`                                                                                  | *boolean*                                                                                    | :heavy_minus_sign:                                                                           | N/A                                                                                          |
| `isSoftLimit`                                                                                | *boolean*                                                                                    | :heavy_minus_sign:                                                                           | N/A                                                                                          |
| `staticValues`                                                                               | *string*[]                                                                                   | :heavy_minus_sign:                                                                           | For static/SLA features                                                                      |
| `usageLimit`                                                                                 | *number*                                                                                     | :heavy_minus_sign:                                                                           | N/A                                                                                          |
| `usageResetPeriod`                                                                           | [models.TypesEntitlementUsageResetPeriod](../models/types-entitlement-usage-reset-period.md) | :heavy_minus_sign:                                                                           | N/A                                                                                          |