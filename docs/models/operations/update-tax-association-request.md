# UpdateTaxAssociationRequest

## Example Usage

```typescript
import { UpdateTaxAssociationRequest } from "openapi/models/operations";

let value: UpdateTaxAssociationRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `id`                                                                                        | *string*                                                                                    | :heavy_check_mark:                                                                          | Tax Config ID                                                                               |
| `body`                                                                                      | [models.DtoTaxAssociationUpdateRequest](../../models/dto-tax-association-update-request.md) | :heavy_check_mark:                                                                          | Tax Config Request                                                                          |