# UpdateTaxRateRequest

## Example Usage

```typescript
import { UpdateTaxRateRequest } from "openapi/models/operations";

let value: UpdateTaxRateRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                         | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `id`                                                                          | *string*                                                                      | :heavy_check_mark:                                                            | Tax rate ID                                                                   |
| `body`                                                                        | [models.DtoUpdateTaxRateRequest](../../models/dto-update-tax-rate-request.md) | :heavy_check_mark:                                                            | Tax rate to update                                                            |