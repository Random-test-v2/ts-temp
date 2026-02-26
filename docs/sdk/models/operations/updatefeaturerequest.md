# UpdateFeatureRequest

## Example Usage

```typescript
import { UpdateFeatureRequest } from "flexprice-ts/sdk/models/operations";

let value: UpdateFeatureRequest = {
  id: "<id>",
  dtoUpdateFeatureRequest: {},
};
```

## Fields

| Field                                                                                   | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `id`                                                                                    | *string*                                                                                | :heavy_check_mark:                                                                      | Feature ID                                                                              |
| `dtoUpdateFeatureRequest`                                                               | [shared.DtoUpdateFeatureRequest](../../../sdk/models/shared/dtoupdatefeaturerequest.md) | :heavy_check_mark:                                                                      | Feature update data                                                                     |