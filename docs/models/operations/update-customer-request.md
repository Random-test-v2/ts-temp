# UpdateCustomerRequest

## Example Usage

```typescript
import { UpdateCustomerRequest } from "openapi/models/operations";

let value: UpdateCustomerRequest = {
  body: {},
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `id`                                                                           | *string*                                                                       | :heavy_minus_sign:                                                             | Customer ID                                                                    |
| `externalCustomerId`                                                           | *string*                                                                       | :heavy_minus_sign:                                                             | Customer External ID                                                           |
| `body`                                                                         | [models.DtoUpdateCustomerRequest](../../models/dto-update-customer-request.md) | :heavy_check_mark:                                                             | Customer                                                                       |