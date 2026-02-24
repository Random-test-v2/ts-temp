# UpdateCostsheetRequest

## Example Usage

```typescript
import { UpdateCostsheetRequest } from "flexprice-ts/sdk/models/operations";

let value: UpdateCostsheetRequest = {
  id: "<id>",
  dtoUpdateCostsheetRequest: {},
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `id`                                                                                        | *string*                                                                                    | :heavy_check_mark:                                                                          | Costsheet ID                                                                                |
| `dtoUpdateCostsheetRequest`                                                                 | [shared.DtoUpdateCostsheetRequest](../../../sdk/models/shared/dtoupdatecostsheetrequest.md) | :heavy_check_mark:                                                                          | Costsheet configuration                                                                     |