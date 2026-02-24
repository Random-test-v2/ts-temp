# TypesAddonFilter

## Example Usage

```typescript
import { TypesAddonFilter } from "openapi/models";

let value: TypesAddonFilter = {};
```

## Fields

| Field                                                                 | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `addonIds`                                                            | *string*[]                                                            | :heavy_minus_sign:                                                    | N/A                                                                   |
| `addonType`                                                           | [models.TypesAddonType](../models/types-addon-type.md)                | :heavy_minus_sign:                                                    | N/A                                                                   |
| `endTime`                                                             | *string*                                                              | :heavy_minus_sign:                                                    | N/A                                                                   |
| `expand`                                                              | *string*                                                              | :heavy_minus_sign:                                                    | N/A                                                                   |
| `filters`                                                             | [models.TypesFilterCondition](../models/types-filter-condition.md)[]  | :heavy_minus_sign:                                                    | filters allows complex filtering based on multiple fields             |
| `limit`                                                               | *number*                                                              | :heavy_minus_sign:                                                    | N/A                                                                   |
| `lookupKeys`                                                          | *string*[]                                                            | :heavy_minus_sign:                                                    | N/A                                                                   |
| `offset`                                                              | *number*                                                              | :heavy_minus_sign:                                                    | N/A                                                                   |
| `order`                                                               | [models.TypesAddonFilterOrder](../models/types-addon-filter-order.md) | :heavy_minus_sign:                                                    | N/A                                                                   |
| `sort`                                                                | [models.TypesSortCondition](../models/types-sort-condition.md)[]      | :heavy_minus_sign:                                                    | N/A                                                                   |
| `startTime`                                                           | *string*                                                              | :heavy_minus_sign:                                                    | N/A                                                                   |
| `status`                                                              | [models.TypesStatus](../models/types-status.md)                       | :heavy_minus_sign:                                                    | N/A                                                                   |