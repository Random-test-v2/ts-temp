# DtoUpdateSubscriptionLineItemRequest

## Example Usage

```typescript
import { DtoUpdateSubscriptionLineItemRequest } from "openapi/models";

let value: DtoUpdateSubscriptionLineItemRequest = {};
```

## Fields

| Field                                                                       | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `amount`                                                                    | *string*                                                                    | :heavy_minus_sign:                                                          | Amount is the new price amount that overrides the original price            |
| `billingModel`                                                              | [models.TypesBillingModel](../models/types-billing-model.md)                | :heavy_minus_sign:                                                          | N/A                                                                         |
| `commitmentAmount`                                                          | *number*                                                                    | :heavy_minus_sign:                                                          | Commitment fields                                                           |
| `commitmentDuration`                                                        | [models.TypesBillingPeriod](../models/types-billing-period.md)              | :heavy_minus_sign:                                                          | N/A                                                                         |
| `commitmentOverageFactor`                                                   | *number*                                                                    | :heavy_minus_sign:                                                          | N/A                                                                         |
| `commitmentQuantity`                                                        | *number*                                                                    | :heavy_minus_sign:                                                          | N/A                                                                         |
| `commitmentTrueUpEnabled`                                                   | *boolean*                                                                   | :heavy_minus_sign:                                                          | N/A                                                                         |
| `commitmentType`                                                            | [models.TypesCommitmentType](../models/types-commitment-type.md)            | :heavy_minus_sign:                                                          | N/A                                                                         |
| `commitmentWindowed`                                                        | *boolean*                                                                   | :heavy_minus_sign:                                                          | N/A                                                                         |
| `effectiveFrom`                                                             | *string*                                                                    | :heavy_minus_sign:                                                          | EffectiveFrom for the existing line item (if not provided, defaults to now) |
| `metadata`                                                                  | Record<string, *string*>                                                    | :heavy_minus_sign:                                                          | Metadata for the new line item                                              |
| `tierMode`                                                                  | [models.TypesBillingTier](../models/types-billing-tier.md)                  | :heavy_minus_sign:                                                          | N/A                                                                         |
| `tiers`                                                                     | [models.DtoCreatePriceTier](../models/dto-create-price-tier.md)[]           | :heavy_minus_sign:                                                          | Tiers determines the pricing tiers for this line item                       |
| `transformQuantity`                                                         | [models.PriceTransformQuantity](../models/price-transform-quantity.md)      | :heavy_minus_sign:                                                          | N/A                                                                         |