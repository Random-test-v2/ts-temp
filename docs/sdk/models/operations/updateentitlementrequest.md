# UpdateEntitlementRequest

## Example Usage

```typescript
import { UpdateEntitlementRequest } from "flexprice-ts/sdk/models/operations";

let value: UpdateEntitlementRequest = {
  id: "<id>",
  dtoUpdateEntitlementRequest: {},
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `id`                                                                                            | *string*                                                                                        | :heavy_check_mark:                                                                              | Entitlement ID                                                                                  |
| `dtoUpdateEntitlementRequest`                                                                   | [shared.DtoUpdateEntitlementRequest](../../../sdk/models/shared/dtoupdateentitlementrequest.md) | :heavy_check_mark:                                                                              | Entitlement configuration                                                                       |