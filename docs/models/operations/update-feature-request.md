# UpdateFeatureRequest

## Example Usage

```typescript
import { UpdateFeatureRequest } from "openapi/models/operations";

let value: UpdateFeatureRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `id`                                                                         | *string*                                                                     | :heavy_check_mark:                                                           | Feature ID                                                                   |
| `body`                                                                       | [models.DtoUpdateFeatureRequest](../../models/dto-update-feature-request.md) | :heavy_check_mark:                                                           | Feature update data                                                          |