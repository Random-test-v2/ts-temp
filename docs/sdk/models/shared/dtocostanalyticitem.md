# DtoCostAnalyticItem

## Example Usage

```typescript
import { DtoCostAnalyticItem } from "flexprice-ts/sdk/models/shared";

let value: DtoCostAnalyticItem = {};
```

## Fields

| Field                                                               | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `costByPeriod`                                                      | [shared.DtoCostPoint](../../../sdk/models/shared/dtocostpoint.md)[] | :heavy_minus_sign:                                                  | Breakdown                                                           |
| `costsheetId`                                                       | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `currency`                                                          | *string*                                                            | :heavy_minus_sign:                                                  | Metadata                                                            |
| `customerId`                                                        | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `externalCustomerId`                                                | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `meter`                                                             | [shared.MeterMeter](../../../sdk/models/shared/metermeter.md)       | :heavy_minus_sign:                                                  | N/A                                                                 |
| `meterId`                                                           | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `meterName`                                                         | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `price`                                                             | [shared.PricePrice](../../../sdk/models/shared/priceprice.md)       | :heavy_minus_sign:                                                  | N/A                                                                 |
| `priceId`                                                           | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `properties`                                                        | Record<string, *string*>                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `source`                                                            | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `totalCost`                                                         | *string*                                                            | :heavy_minus_sign:                                                  | Aggregated metrics                                                  |
| `totalEvents`                                                       | *number*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `totalQuantity`                                                     | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |