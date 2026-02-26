# UpdatePlanRequest

## Example Usage

```typescript
import { UpdatePlanRequest } from "flexprice-ts/sdk/models/operations";

let value: UpdatePlanRequest = {
  id: "<id>",
  dtoUpdatePlanRequest: {},
};
```

## Fields

| Field                                                                             | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `id`                                                                              | *string*                                                                          | :heavy_check_mark:                                                                | Plan ID                                                                           |
| `dtoUpdatePlanRequest`                                                            | [shared.DtoUpdatePlanRequest](../../../sdk/models/shared/dtoupdateplanrequest.md) | :heavy_check_mark:                                                                | Plan update                                                                       |