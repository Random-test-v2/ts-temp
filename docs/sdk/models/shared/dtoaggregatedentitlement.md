# DtoAggregatedEntitlement

## Example Usage

```typescript
import { DtoAggregatedEntitlement } from "flexprice-ts/sdk/models/shared";

let value: DtoAggregatedEntitlement = {};
```

## Fields

| Field                                                                                                     | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `isEnabled`                                                                                               | *boolean*                                                                                                 | :heavy_minus_sign:                                                                                        | N/A                                                                                                       |
| `isSoftLimit`                                                                                             | *boolean*                                                                                                 | :heavy_minus_sign:                                                                                        | N/A                                                                                                       |
| `staticValues`                                                                                            | *string*[]                                                                                                | :heavy_minus_sign:                                                                                        | For static/SLA features                                                                                   |
| `usageLimit`                                                                                              | *number*                                                                                                  | :heavy_minus_sign:                                                                                        | N/A                                                                                                       |
| `usageResetPeriod`                                                                                        | [shared.TypesEntitlementUsageResetPeriod](../../../sdk/models/shared/typesentitlementusageresetperiod.md) | :heavy_minus_sign:                                                                                        | N/A                                                                                                       |