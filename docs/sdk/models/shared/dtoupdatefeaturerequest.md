# DtoUpdateFeatureRequest

## Example Usage

```typescript
import { DtoUpdateFeatureRequest } from "flexprice-ts/sdk/models/shared";

let value: DtoUpdateFeatureRequest = {};
```

## Fields

| Field                                                                         | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `alertSettings`                                                               | [shared.TypesAlertSettings](../../../sdk/models/shared/typesalertsettings.md) | :heavy_minus_sign:                                                            | N/A                                                                           |
| `description`                                                                 | *string*                                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |
| `filters`                                                                     | [shared.MeterFilter](../../../sdk/models/shared/meterfilter.md)[]             | :heavy_minus_sign:                                                            | N/A                                                                           |
| `metadata`                                                                    | Record<string, *string*>                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |
| `name`                                                                        | *string*                                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |
| `unitPlural`                                                                  | *string*                                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |
| `unitSingular`                                                                | *string*                                                                      | :heavy_minus_sign:                                                            | N/A                                                                           |