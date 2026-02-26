# UpdatePriceRequest

## Example Usage

```typescript
import { UpdatePriceRequest } from "flexprice-ts/sdk/models/operations";

let value: UpdatePriceRequest = {
  id: "<id>",
  dtoUpdatePriceRequest: {},
};
```

## Fields

| Field                                                                               | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `id`                                                                                | *string*                                                                            | :heavy_check_mark:                                                                  | Price ID                                                                            |
| `dtoUpdatePriceRequest`                                                             | [shared.DtoUpdatePriceRequest](../../../sdk/models/shared/dtoupdatepricerequest.md) | :heavy_check_mark:                                                                  | Price configuration                                                                 |