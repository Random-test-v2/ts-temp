# UpdateTaxAssociationRequest

## Example Usage

```typescript
import { UpdateTaxAssociationRequest } from "flexprice-ts/sdk/models/operations";

let value: UpdateTaxAssociationRequest = {
  id: "<id>",
  dtoTaxAssociationUpdateRequest: {},
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `id`                                                                                                  | *string*                                                                                              | :heavy_check_mark:                                                                                    | Tax Config ID                                                                                         |
| `dtoTaxAssociationUpdateRequest`                                                                      | [shared.DtoTaxAssociationUpdateRequest](../../../sdk/models/shared/dtotaxassociationupdaterequest.md) | :heavy_check_mark:                                                                                    | Tax Config Request                                                                                    |