# TypesUserFilter

## Example Usage

```typescript
import { TypesUserFilter } from "openapi/models";

let value: TypesUserFilter = {};
```

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `endTime`                                                            | *string*                                                             | :heavy_minus_sign:                                                   | N/A                                                                  |
| `expand`                                                             | *string*                                                             | :heavy_minus_sign:                                                   | N/A                                                                  |
| `filters`                                                            | [models.TypesFilterCondition](../models/types-filter-condition.md)[] | :heavy_minus_sign:                                                   | filters allows complex filtering based on multiple fields            |
| `limit`                                                              | *number*                                                             | :heavy_minus_sign:                                                   | N/A                                                                  |
| `offset`                                                             | *number*                                                             | :heavy_minus_sign:                                                   | N/A                                                                  |
| `order`                                                              | [models.TypesUserFilterOrder](../models/types-user-filter-order.md)  | :heavy_minus_sign:                                                   | N/A                                                                  |
| `roles`                                                              | *string*[]                                                           | :heavy_minus_sign:                                                   | N/A                                                                  |
| `sort`                                                               | [models.TypesSortCondition](../models/types-sort-condition.md)[]     | :heavy_minus_sign:                                                   | N/A                                                                  |
| `startTime`                                                          | *string*                                                             | :heavy_minus_sign:                                                   | N/A                                                                  |
| `status`                                                             | [models.TypesStatus](../models/types-status.md)                      | :heavy_minus_sign:                                                   | N/A                                                                  |
| `type`                                                               | [models.TypesUserType](../models/types-user-type.md)                 | :heavy_minus_sign:                                                   | N/A                                                                  |
| `userIds`                                                            | *string*[]                                                           | :heavy_minus_sign:                                                   | Specific filters for users                                           |