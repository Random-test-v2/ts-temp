# DtoAddAddonRequest

## Example Usage

```typescript
import { DtoAddAddonRequest } from "flexprice-ts/sdk/models/shared";

let value: DtoAddAddonRequest = {
  addonId: "<id>",
  subscriptionId: "<id>",
};
```

## Fields

| Field                                                                                                           | Type                                                                                                            | Required                                                                                                        | Description                                                                                                     |
| --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| `addonId`                                                                                                       | *string*                                                                                                        | :heavy_check_mark:                                                                                              | N/A                                                                                                             |
| `lineItemCommitments`                                                                                           | Record<string, [shared.DtoLineItemCommitmentConfig](../../../sdk/models/shared/dtolineitemcommitmentconfig.md)> | :heavy_minus_sign:                                                                                              | LineItemCommitments allows setting commitment configuration per addon line item (keyed by price_id)             |
| `metadata`                                                                                                      | Record<string, *any*>                                                                                           | :heavy_minus_sign:                                                                                              | N/A                                                                                                             |
| `startDate`                                                                                                     | *string*                                                                                                        | :heavy_minus_sign:                                                                                              | N/A                                                                                                             |
| `subscriptionId`                                                                                                | *string*                                                                                                        | :heavy_check_mark:                                                                                              | N/A                                                                                                             |