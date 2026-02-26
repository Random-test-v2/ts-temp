# CancelSubscriptionRequest

## Example Usage

```typescript
import { CancelSubscriptionRequest } from "openapi/models/operations";

let value: CancelSubscriptionRequest = {
  id: "<id>",
  body: {
    cancellationType: "immediate",
  },
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `id`                                                                                   | *string*                                                                               | :heavy_check_mark:                                                                     | Subscription ID                                                                        |
| `body`                                                                                 | [models.DtoCancelSubscriptionRequest](../../models/dto-cancel-subscription-request.md) | :heavy_check_mark:                                                                     | Cancel Subscription Request                                                            |