# PostPlansIdCloneRequest

## Example Usage

```typescript
import { PostPlansIdCloneRequest } from "flexprice-ts/sdk/models/operations";

let value: PostPlansIdCloneRequest = {
  id: "<id>",
  dtoClonePlanRequest: {},
};
```

## Fields

| Field                                                                           | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `id`                                                                            | *string*                                                                        | :heavy_check_mark:                                                              | Source Plan ID                                                                  |
| `dtoClonePlanRequest`                                                           | [shared.DtoClonePlanRequest](../../../sdk/models/shared/dtocloneplanrequest.md) | :heavy_check_mark:                                                              | Clone configuration                                                             |