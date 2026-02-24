# UpdatePriceUnitRequest

## Example Usage

```typescript
import { UpdatePriceUnitRequest } from "flexprice-ts/sdk/models/operations";

let value: UpdatePriceUnitRequest = {
  id: "<id>",
  dtoUpdatePriceUnitRequest: {},
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `id`                                                                                        | *string*                                                                                    | :heavy_check_mark:                                                                          | Price unit ID                                                                               |
| `dtoUpdatePriceUnitRequest`                                                                 | [shared.DtoUpdatePriceUnitRequest](../../../sdk/models/shared/dtoupdatepriceunitrequest.md) | :heavy_check_mark:                                                                          | Price unit details to update                                                                |