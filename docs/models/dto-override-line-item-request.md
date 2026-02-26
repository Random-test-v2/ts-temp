# DtoOverrideLineItemRequest

## Example Usage

```typescript
import { DtoOverrideLineItemRequest } from "openapi/models";

let value: DtoOverrideLineItemRequest = {
  priceId: "<id>",
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `amount`                                                                                           | *string*                                                                                           | :heavy_minus_sign:                                                                                 | Amount is the new price amount that overrides the original price (optional)                        |
| `billingModel`                                                                                     | [models.TypesBillingModel](../models/types-billing-model.md)                                       | :heavy_minus_sign:                                                                                 | N/A                                                                                                |
| `priceId`                                                                                          | *string*                                                                                           | :heavy_check_mark:                                                                                 | PriceID references the plan price to override                                                      |
| `priceUnitAmount`                                                                                  | *string*                                                                                           | :heavy_minus_sign:                                                                                 | PriceUnitAmount is the amount of the price unit (for CUSTOM type, FLAT_FEE/PACKAGE billing models) |
| `priceUnitTiers`                                                                                   | [models.DtoCreatePriceTier](../models/dto-create-price-tier.md)[]                                  | :heavy_minus_sign:                                                                                 | PriceUnitTiers are the tiers for the price unit (for CUSTOM type, TIERED billing model)            |
| `quantity`                                                                                         | *string*                                                                                           | :heavy_minus_sign:                                                                                 | Quantity for this line item (optional)                                                             |
| `tierMode`                                                                                         | [models.TypesBillingTier](../models/types-billing-tier.md)                                         | :heavy_minus_sign:                                                                                 | N/A                                                                                                |
| `tiers`                                                                                            | [models.DtoCreatePriceTier](../models/dto-create-price-tier.md)[]                                  | :heavy_minus_sign:                                                                                 | Tiers determines the pricing tiers for this line item                                              |
| `transformQuantity`                                                                                | [models.PriceTransformQuantity](../models/price-transform-quantity.md)                             | :heavy_minus_sign:                                                                                 | N/A                                                                                                |