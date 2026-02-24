# CostsheetFilter

## Example Usage

```typescript
import { CostsheetFilter } from "openapi/models";

let value: CostsheetFilter = {};
```

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `costsheetIDs`                                                       | *string*[]                                                           | :heavy_minus_sign:                                                   | CostsheetIDs allows filtering by specific costsheet IDs              |
| `environmentID`                                                      | *string*                                                             | :heavy_minus_sign:                                                   | EnvironmentID filters by specific environment ID                     |
| `filters`                                                            | [models.TypesFilterCondition](../models/types-filter-condition.md)[] | :heavy_minus_sign:                                                   | Filters contains custom filtering conditions                         |
| `lookupKey`                                                          | *string*                                                             | :heavy_minus_sign:                                                   | LookupKey filters by lookup key                                      |
| `name`                                                               | *string*                                                             | :heavy_minus_sign:                                                   | Name filters by costsheet name                                       |
| `queryFilter`                                                        | [models.TypesQueryFilter](../models/types-query-filter.md)           | :heavy_minus_sign:                                                   | N/A                                                                  |
| `sort`                                                               | [models.TypesSortCondition](../models/types-sort-condition.md)[]     | :heavy_minus_sign:                                                   | Sort specifies result ordering preferences                           |
| `status`                                                             | [models.TypesStatus](../models/types-status.md)                      | :heavy_minus_sign:                                                   | N/A                                                                  |
| `tenantID`                                                           | *string*                                                             | :heavy_minus_sign:                                                   | TenantID filters by specific tenant ID                               |
| `timeRangeFilter`                                                    | [models.TypesTimeRangeFilter](../models/types-time-range-filter.md)  | :heavy_minus_sign:                                                   | N/A                                                                  |