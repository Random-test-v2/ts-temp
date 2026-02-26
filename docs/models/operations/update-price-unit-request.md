# UpdatePriceUnitRequest

## Example Usage

```typescript
import { UpdatePriceUnitRequest } from "openapi/models/operations";

let value: UpdatePriceUnitRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                             | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `id`                                                                              | *string*                                                                          | :heavy_check_mark:                                                                | Price unit ID                                                                     |
| `body`                                                                            | [models.DtoUpdatePriceUnitRequest](../../models/dto-update-price-unit-request.md) | :heavy_check_mark:                                                                | Price unit details to update                                                      |