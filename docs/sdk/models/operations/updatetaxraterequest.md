# UpdateTaxRateRequest

## Example Usage

```typescript
import { UpdateTaxRateRequest } from "flexprice-ts/sdk/models/operations";

let value: UpdateTaxRateRequest = {
  id: "<id>",
  dtoUpdateTaxRateRequest: {},
};
```

## Fields

| Field                                                                                   | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `id`                                                                                    | *string*                                                                                | :heavy_check_mark:                                                                      | Tax rate ID                                                                             |
| `dtoUpdateTaxRateRequest`                                                               | [shared.DtoUpdateTaxRateRequest](../../../sdk/models/shared/dtoupdatetaxraterequest.md) | :heavy_check_mark:                                                                      | Tax rate to update                                                                      |