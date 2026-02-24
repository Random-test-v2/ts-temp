# UpdateCustomerRequest

## Example Usage

```typescript
import { UpdateCustomerRequest } from "flexprice-ts/sdk/models/operations";

let value: UpdateCustomerRequest = {
  dtoUpdateCustomerRequest: {},
};
```

## Fields

| Field                                                                                     | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `id`                                                                                      | *string*                                                                                  | :heavy_minus_sign:                                                                        | Customer ID                                                                               |
| `externalCustomerId`                                                                      | *string*                                                                                  | :heavy_minus_sign:                                                                        | Customer External ID                                                                      |
| `dtoUpdateCustomerRequest`                                                                | [shared.DtoUpdateCustomerRequest](../../../sdk/models/shared/dtoupdatecustomerrequest.md) | :heavy_check_mark:                                                                        | Customer                                                                                  |