# DtoCreateTaxAssociationRequest

## Example Usage

```typescript
import { DtoCreateTaxAssociationRequest } from "flexprice-ts/sdk/models/shared";

let value: DtoCreateTaxAssociationRequest = {
  entityId: "<id>",
  entityType: "tenant",
  taxRateCode: "<value>",
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `autoApply`                                                                           | *boolean*                                                                             | :heavy_minus_sign:                                                                    | N/A                                                                                   |
| `currency`                                                                            | *string*                                                                              | :heavy_minus_sign:                                                                    | N/A                                                                                   |
| `entityId`                                                                            | *string*                                                                              | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `entityType`                                                                          | [shared.TypesTaxRateEntityType](../../../sdk/models/shared/typestaxrateentitytype.md) | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `metadata`                                                                            | Record<string, *string*>                                                              | :heavy_minus_sign:                                                                    | N/A                                                                                   |
| `priority`                                                                            | *number*                                                                              | :heavy_minus_sign:                                                                    | N/A                                                                                   |
| `taxRateCode`                                                                         | *string*                                                                              | :heavy_check_mark:                                                                    | N/A                                                                                   |