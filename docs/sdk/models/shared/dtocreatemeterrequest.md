# DtoCreateMeterRequest

## Example Usage

```typescript
import { DtoCreateMeterRequest } from "flexprice-ts/sdk/models/shared";

let value: DtoCreateMeterRequest = {
  aggregation: {},
  eventName: "api_request",
  name: "API Usage Meter",
  resetUsage: "BILLING_PERIOD",
};
```

## Fields

| Field                                                                     | Type                                                                      | Required                                                                  | Description                                                               | Example                                                                   |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `aggregation`                                                             | [shared.MeterAggregation](../../../sdk/models/shared/meteraggregation.md) | :heavy_check_mark:                                                        | N/A                                                                       |                                                                           |
| `eventName`                                                               | *string*                                                                  | :heavy_check_mark:                                                        | N/A                                                                       | api_request                                                               |
| `filters`                                                                 | [shared.MeterFilter](../../../sdk/models/shared/meterfilter.md)[]         | :heavy_minus_sign:                                                        | N/A                                                                       |                                                                           |
| `name`                                                                    | *string*                                                                  | :heavy_check_mark:                                                        | N/A                                                                       | API Usage Meter                                                           |
| `resetUsage`                                                              | [shared.TypesResetUsage](../../../sdk/models/shared/typesresetusage.md)   | :heavy_check_mark:                                                        | N/A                                                                       |                                                                           |