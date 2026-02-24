# TypesGroupFilter

## Example Usage

```typescript
import { TypesGroupFilter } from "openapi/models";

let value: TypesGroupFilter = {};
```

## Fields

| Field                                                                 | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `endTime`                                                             | *string*                                                              | :heavy_minus_sign:                                                    | N/A                                                                   |
| `entityType`                                                          | *string*                                                              | :heavy_minus_sign:                                                    | N/A                                                                   |
| `expand`                                                              | *string*                                                              | :heavy_minus_sign:                                                    | N/A                                                                   |
| `filters`                                                             | [models.TypesFilterCondition](../models/types-filter-condition.md)[]  | :heavy_minus_sign:                                                    | filters allows complex filtering based on multiple fields             |
| `groupIds`                                                            | *string*[]                                                            | :heavy_minus_sign:                                                    | Group specific filters                                                |
| `limit`                                                               | *number*                                                              | :heavy_minus_sign:                                                    | N/A                                                                   |
| `lookupKey`                                                           | *string*                                                              | :heavy_minus_sign:                                                    | N/A                                                                   |
| `name`                                                                | *string*                                                              | :heavy_minus_sign:                                                    | N/A                                                                   |
| `offset`                                                              | *number*                                                              | :heavy_minus_sign:                                                    | N/A                                                                   |
| `order`                                                               | [models.TypesGroupFilterOrder](../models/types-group-filter-order.md) | :heavy_minus_sign:                                                    | N/A                                                                   |
| `sort`                                                                | [models.TypesSortCondition](../models/types-sort-condition.md)[]      | :heavy_minus_sign:                                                    | N/A                                                                   |
| `startTime`                                                           | *string*                                                              | :heavy_minus_sign:                                                    | N/A                                                                   |
| `status`                                                              | [models.TypesStatus](../models/types-status.md)                       | :heavy_minus_sign:                                                    | N/A                                                                   |