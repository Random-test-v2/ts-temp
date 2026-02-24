# DeletePriceRequest

## Example Usage

```typescript
import { DeletePriceRequest } from "flexprice-ts/sdk/models/operations";

let value: DeletePriceRequest = {
  id: "<id>",
  dtoDeletePriceRequest: {},
};
```

## Fields

| Field                                                                               | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `id`                                                                                | *string*                                                                            | :heavy_check_mark:                                                                  | Price ID                                                                            |
| `dtoDeletePriceRequest`                                                             | [shared.DtoDeletePriceRequest](../../../sdk/models/shared/dtodeletepricerequest.md) | :heavy_check_mark:                                                                  | Delete Price Request                                                                |