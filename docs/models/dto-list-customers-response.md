# DtoListCustomersResponse

Response object for listing customers with pagination

## Example Usage

```typescript
import { DtoListCustomersResponse } from "openapi/models";

let value: DtoListCustomersResponse = {};
```

## Fields

| Field                                                                    | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `items`                                                                  | [models.DtoCustomerResponse](../models/dto-customer-response.md)[]       | :heavy_minus_sign:                                                       | N/A                                                                      |
| `pagination`                                                             | [models.TypesPaginationResponse](../models/types-pagination-response.md) | :heavy_minus_sign:                                                       | N/A                                                                      |