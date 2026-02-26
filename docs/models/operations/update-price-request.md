# UpdatePriceRequest

## Example Usage

```typescript
import { UpdatePriceRequest } from "openapi/models/operations";

let value: UpdatePriceRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                    | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `id`                                                                     | *string*                                                                 | :heavy_check_mark:                                                       | Price ID                                                                 |
| `body`                                                                   | [models.DtoUpdatePriceRequest](../../models/dto-update-price-request.md) | :heavy_check_mark:                                                       | Price configuration                                                      |