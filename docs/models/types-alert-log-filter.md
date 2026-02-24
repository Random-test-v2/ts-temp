# TypesAlertLogFilter

## Example Usage

```typescript
import { TypesAlertLogFilter } from "openapi/models";

let value: TypesAlertLogFilter = {};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `alertStatus`                                                                | [models.TypesAlertState](../models/types-alert-state.md)                     | :heavy_minus_sign:                                                           | N/A                                                                          |
| `alertType`                                                                  | [models.TypesAlertType](../models/types-alert-type.md)                       | :heavy_minus_sign:                                                           | N/A                                                                          |
| `customerId`                                                                 | *string*                                                                     | :heavy_minus_sign:                                                           | N/A                                                                          |
| `endTime`                                                                    | *string*                                                                     | :heavy_minus_sign:                                                           | N/A                                                                          |
| `entityId`                                                                   | *string*                                                                     | :heavy_minus_sign:                                                           | N/A                                                                          |
| `entityType`                                                                 | [models.TypesAlertEntityType](../models/types-alert-entity-type.md)          | :heavy_minus_sign:                                                           | N/A                                                                          |
| `expand`                                                                     | *string*                                                                     | :heavy_minus_sign:                                                           | N/A                                                                          |
| `filters`                                                                    | [models.TypesFilterCondition](../models/types-filter-condition.md)[]         | :heavy_minus_sign:                                                           | filters allows complex filtering based on multiple fields                    |
| `limit`                                                                      | *number*                                                                     | :heavy_minus_sign:                                                           | N/A                                                                          |
| `offset`                                                                     | *number*                                                                     | :heavy_minus_sign:                                                           | N/A                                                                          |
| `order`                                                                      | [models.TypesAlertLogFilterOrder](../models/types-alert-log-filter-order.md) | :heavy_minus_sign:                                                           | N/A                                                                          |
| `sort`                                                                       | [models.TypesSortCondition](../models/types-sort-condition.md)[]             | :heavy_minus_sign:                                                           | N/A                                                                          |
| `startTime`                                                                  | *string*                                                                     | :heavy_minus_sign:                                                           | N/A                                                                          |
| `status`                                                                     | [models.TypesStatus](../models/types-status.md)                              | :heavy_minus_sign:                                                           | N/A                                                                          |