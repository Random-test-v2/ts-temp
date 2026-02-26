# ListPriceUnitsRequest

## Example Usage

```typescript
import { ListPriceUnitsRequest } from "flexprice-ts/sdk/models/operations";

let value: ListPriceUnitsRequest = {};
```

## Fields

| Field                                                                                   | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `status`                                                                                | *string*                                                                                | :heavy_minus_sign:                                                                      | Filter by status                                                                        |
| `limit`                                                                                 | *number*                                                                                | :heavy_minus_sign:                                                                      | Limit number of results                                                                 |
| `offset`                                                                                | *number*                                                                                | :heavy_minus_sign:                                                                      | Offset for pagination                                                                   |
| `sort`                                                                                  | *string*                                                                                | :heavy_minus_sign:                                                                      | Sort field                                                                              |
| `order`                                                                                 | [operations.ListPriceUnitsOrder](../../../sdk/models/operations/listpriceunitsorder.md) | :heavy_minus_sign:                                                                      | Sort order                                                                              |