# DeletePriceRequest

## Example Usage

```typescript
import { DeletePriceRequest } from "openapi/models/operations";

let value: DeletePriceRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                    | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `id`                                                                     | *string*                                                                 | :heavy_check_mark:                                                       | Price ID                                                                 |
| `body`                                                                   | [models.DtoDeletePriceRequest](../../models/dto-delete-price-request.md) | :heavy_check_mark:                                                       | Delete Price Request                                                     |