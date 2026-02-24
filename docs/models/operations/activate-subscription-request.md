# ActivateSubscriptionRequest

## Example Usage

```typescript
import { ActivateSubscriptionRequest } from "openapi/models/operations";

let value: ActivateSubscriptionRequest = {
  id: "<id>",
  body: {
    startDate: "<value>",
  },
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `id`                                                                                                  | *string*                                                                                              | :heavy_check_mark:                                                                                    | Subscription ID                                                                                       |
| `body`                                                                                                | [models.DtoActivateDraftSubscriptionRequest](../../models/dto-activate-draft-subscription-request.md) | :heavy_check_mark:                                                                                    | Activate Draft Subscription Request                                                                   |