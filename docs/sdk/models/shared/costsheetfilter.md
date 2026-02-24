# CostsheetFilter

## Example Usage

```typescript
import { CostsheetFilter } from "flexprice-ts/sdk/models/shared";

let value: CostsheetFilter = {};
```

## Fields

| Field                                                                               | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `costsheetIDs`                                                                      | *string*[]                                                                          | :heavy_minus_sign:                                                                  | CostsheetIDs allows filtering by specific costsheet IDs                             |
| `environmentID`                                                                     | *string*                                                                            | :heavy_minus_sign:                                                                  | EnvironmentID filters by specific environment ID                                    |
| `filters`                                                                           | [shared.TypesFilterCondition](../../../sdk/models/shared/typesfiltercondition.md)[] | :heavy_minus_sign:                                                                  | Filters contains custom filtering conditions                                        |
| `lookupKey`                                                                         | *string*                                                                            | :heavy_minus_sign:                                                                  | LookupKey filters by lookup key                                                     |
| `name`                                                                              | *string*                                                                            | :heavy_minus_sign:                                                                  | Name filters by costsheet name                                                      |
| `queryFilter`                                                                       | [shared.TypesQueryFilter](../../../sdk/models/shared/typesqueryfilter.md)           | :heavy_minus_sign:                                                                  | N/A                                                                                 |
| `sort`                                                                              | [shared.TypesSortCondition](../../../sdk/models/shared/typessortcondition.md)[]     | :heavy_minus_sign:                                                                  | Sort specifies result ordering preferences                                          |
| `status`                                                                            | [shared.TypesStatus](../../../sdk/models/shared/typesstatus.md)                     | :heavy_minus_sign:                                                                  | N/A                                                                                 |
| `tenantID`                                                                          | *string*                                                                            | :heavy_minus_sign:                                                                  | TenantID filters by specific tenant ID                                              |
| `timeRangeFilter`                                                                   | [shared.TypesTimeRangeFilter](../../../sdk/models/shared/typestimerangefilter.md)   | :heavy_minus_sign:                                                                  | N/A                                                                                 |