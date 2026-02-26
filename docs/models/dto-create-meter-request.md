# DtoCreateMeterRequest

## Example Usage

```typescript
import { DtoCreateMeterRequest } from "openapi/models";

let value: DtoCreateMeterRequest = {
  aggregation: {},
  eventName: "api_request",
  name: "API Usage Meter",
  resetUsage: "BILLING_PERIOD",
};
```

## Fields

| Field                                                     | Type                                                      | Required                                                  | Description                                               | Example                                                   |
| --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- |
| `aggregation`                                             | [models.MeterAggregation](../models/meter-aggregation.md) | :heavy_check_mark:                                        | N/A                                                       |                                                           |
| `eventName`                                               | *string*                                                  | :heavy_check_mark:                                        | N/A                                                       | api_request                                               |
| `filters`                                                 | [models.MeterFilter](../models/meter-filter.md)[]         | :heavy_minus_sign:                                        | N/A                                                       |                                                           |
| `name`                                                    | *string*                                                  | :heavy_check_mark:                                        | N/A                                                       | API Usage Meter                                           |
| `resetUsage`                                              | [models.TypesResetUsage](../models/types-reset-usage.md)  | :heavy_check_mark:                                        | N/A                                                       |                                                           |