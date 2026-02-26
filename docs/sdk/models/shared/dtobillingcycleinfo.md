# DtoBillingCycleInfo

## Example Usage

```typescript
import { DtoBillingCycleInfo } from "flexprice-ts/sdk/models/shared";

let value: DtoBillingCycleInfo = {};
```

## Fields

| Field                                                                           | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `billingAnchor`                                                                 | *string*                                                                        | :heavy_minus_sign:                                                              | billing_anchor is the new billing anchor                                        |
| `billingCadence`                                                                | [shared.TypesBillingCadence](../../../sdk/models/shared/typesbillingcadence.md) | :heavy_minus_sign:                                                              | N/A                                                                             |
| `billingPeriod`                                                                 | [shared.TypesBillingPeriod](../../../sdk/models/shared/typesbillingperiod.md)   | :heavy_minus_sign:                                                              | N/A                                                                             |
| `billingPeriodCount`                                                            | *number*                                                                        | :heavy_minus_sign:                                                              | billing_period_count is the billing period count                                |
| `periodEnd`                                                                     | *string*                                                                        | :heavy_minus_sign:                                                              | period_end is the end of the new billing period                                 |
| `periodStart`                                                                   | *string*                                                                        | :heavy_minus_sign:                                                              | period_start is the start of the new billing period                             |