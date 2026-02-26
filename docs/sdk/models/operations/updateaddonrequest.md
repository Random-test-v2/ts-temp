# UpdateAddonRequest

## Example Usage

```typescript
import { UpdateAddonRequest } from "flexprice-ts/sdk/models/operations";

let value: UpdateAddonRequest = {
  id: "<id>",
  dtoUpdateAddonRequest: {},
};
```

## Fields

| Field                                                                               | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `id`                                                                                | *string*                                                                            | :heavy_check_mark:                                                                  | Addon ID                                                                            |
| `dtoUpdateAddonRequest`                                                             | [shared.DtoUpdateAddonRequest](../../../sdk/models/shared/dtoupdateaddonrequest.md) | :heavy_check_mark:                                                                  | Update Addon Request                                                                |