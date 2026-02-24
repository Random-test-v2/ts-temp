# DtoCreatePriceRequest

## Example Usage

```typescript
import { DtoCreatePriceRequest } from "openapi/models";

let value: DtoCreatePriceRequest = {
  billingCadence: "RECURRING",
  billingModel: "TIERED",
  billingPeriod: "ANNUAL",
  currency: "Vatu",
  entityId: "<id>",
  entityType: "ADDON",
  invoiceCadence: "ARREAR",
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
| `currency`                                                             | *string*                                                               | :heavy_check_mark:                                                     | N/A                                                                    |
| `description`                                                          | *string*                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `displayName`                                                          | *string*                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `endDate`                                                              | *string*                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `entityId`                                                             | *string*                                                               | :heavy_check_mark:                                                     | N/A                                                                    |
| `entityType`                                                           | [models.TypesPriceEntityType](../models/types-price-entity-type.md)    | :heavy_check_mark:                                                     | N/A                                                                    |
| `filterValues`                                                         | Record<string, *string*[]>                                             | :heavy_minus_sign:                                                     | N/A                                                                    |
| `groupId`                                                              | *string*                                                               | :heavy_minus_sign:                                                     | GroupID is the id of the group to add the price to                     |
| `invoiceCadence`                                                       | [models.TypesInvoiceCadence](../models/types-invoice-cadence.md)       | :heavy_check_mark:                                                     | N/A                                                                    |
| `lookupKey`                                                            | *string*                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `metadata`                                                             | Record<string, *string*>                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `meterId`                                                              | *string*                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `minQuantity`                                                          | *number*                                                               | :heavy_minus_sign:                                                     | MinQuantity is the minimum quantity of the price                       |
| `priceUnitConfig`                                                      | [models.DtoPriceUnitConfig](../models/dto-price-unit-config.md)        | :heavy_minus_sign:                                                     | N/A                                                                    |
| `priceUnitType`                                                        | [models.TypesPriceUnitType](../models/types-price-unit-type.md)        | :heavy_check_mark:                                                     | N/A                                                                    |
| `startDate`                                                            | *string*                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `tierMode`                                                             | [models.TypesBillingTier](../models/types-billing-tier.md)             | :heavy_minus_sign:                                                     | N/A                                                                    |
| `tiers`                                                                | [models.DtoCreatePriceTier](../models/dto-create-price-tier.md)[]      | :heavy_minus_sign:                                                     | N/A                                                                    |
| `transformQuantity`                                                    | [models.PriceTransformQuantity](../models/price-transform-quantity.md) | :heavy_minus_sign:                                                     | N/A                                                                    |
| `trialPeriod`                                                          | *number*                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `type`                                                                 | [models.TypesPriceType](../models/types-price-type.md)                 | :heavy_check_mark:                                                     | N/A                                                                    |