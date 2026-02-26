# DtoSubscriptionPriceCreateRequest

## Example Usage

```typescript
import { DtoSubscriptionPriceCreateRequest } from "openapi/models";

let value: DtoSubscriptionPriceCreateRequest = {
  billingCadence: "ONETIME",
  billingModel: "TIERED",
  billingPeriod: "HALF_YEARLY",
  invoiceCadence: "ADVANCE",
  priceUnitType: "CUSTOM",
  type: "FIXED",
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `amount`                                                               | *string*                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `billingCadence`                                                       | [models.TypesBillingCadence](../models/types-billing-cadence.md)       | :heavy_check_mark:                                                     | N/A                                                                    |
| `billingModel`                                                         | [models.TypesBillingModel](../models/types-billing-model.md)           | :heavy_check_mark:                                                     | N/A                                                                    |
| `billingPeriod`                                                        | [models.TypesBillingPeriod](../models/types-billing-period.md)         | :heavy_check_mark:                                                     | N/A                                                                    |
| `billingPeriodCount`                                                   | *number*                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `description`                                                          | *string*                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `displayName`                                                          | *string*                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `endDate`                                                              | *string*                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `filterValues`                                                         | Record<string, *string*[]>                                             | :heavy_minus_sign:                                                     | N/A                                                                    |
| `invoiceCadence`                                                       | [models.TypesInvoiceCadence](../models/types-invoice-cadence.md)       | :heavy_check_mark:                                                     | N/A                                                                    |
| `lookupKey`                                                            | *string*                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `metadata`                                                             | Record<string, *string*>                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `meterId`                                                              | *string*                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `minQuantity`                                                          | *number*                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `priceUnitConfig`                                                      | [models.DtoPriceUnitConfig](../models/dto-price-unit-config.md)        | :heavy_minus_sign:                                                     | N/A                                                                    |
| `priceUnitType`                                                        | [models.TypesPriceUnitType](../models/types-price-unit-type.md)        | :heavy_check_mark:                                                     | N/A                                                                    |
| `startDate`                                                            | *string*                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `tierMode`                                                             | [models.TypesBillingTier](../models/types-billing-tier.md)             | :heavy_minus_sign:                                                     | N/A                                                                    |
| `tiers`                                                                | [models.DtoCreatePriceTier](../models/dto-create-price-tier.md)[]      | :heavy_minus_sign:                                                     | N/A                                                                    |
| `transformQuantity`                                                    | [models.PriceTransformQuantity](../models/price-transform-quantity.md) | :heavy_minus_sign:                                                     | N/A                                                                    |
| `trialPeriod`                                                          | *number*                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `type`                                                                 | [models.TypesPriceType](../models/types-price-type.md)                 | :heavy_check_mark:                                                     | N/A                                                                    |