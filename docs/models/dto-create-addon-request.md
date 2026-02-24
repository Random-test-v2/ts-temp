# DtoCreateAddonRequest

## Example Usage

```typescript
import { DtoCreateAddonRequest } from "openapi/models";

let value: DtoCreateAddonRequest = {
  lookupKey: "<value>",
  name: "<value>",
  type: "onetime",
};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `description`                                          | *string*                                               | :heavy_minus_sign:                                     | N/A                                                    |
| `lookupKey`                                            | *string*                                               | :heavy_check_mark:                                     | N/A                                                    |
| `metadata`                                             | Record<string, *any*>                                  | :heavy_minus_sign:                                     | N/A                                                    |
| `name`                                                 | *string*                                               | :heavy_check_mark:                                     | N/A                                                    |
| `type`                                                 | [models.TypesAddonType](../models/types-addon-type.md) | :heavy_check_mark:                                     | N/A                                                    |