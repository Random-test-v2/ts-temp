# DtoCreateBulkPriceRequest

## Example Usage

```typescript
import { DtoCreateBulkPriceRequest } from "flexprice-ts/sdk/models/shared";

let value: DtoCreateBulkPriceRequest = {
  items: [
    {
      billingCadence: "RECURRING",
      billingModel: "TIERED",
      billingPeriod: "DAILY",
      currency: "Gourde",
      entityId: "<id>",
      entityType: "ADDON",
      invoiceCadence: "ARREAR",
      priceUnitType: "FIAT",
      type: "FIXED",
    },
  ],
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `items`                                                                               | [shared.DtoCreatePriceRequest](../../../sdk/models/shared/dtocreatepricerequest.md)[] | :heavy_check_mark:                                                                    | N/A                                                                                   |