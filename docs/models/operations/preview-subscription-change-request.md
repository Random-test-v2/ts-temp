# PreviewSubscriptionChangeRequest

## Example Usage

```typescript
import { PreviewSubscriptionChangeRequest } from "openapi/models/operations";

let value: PreviewSubscriptionChangeRequest = {
  id: "<id>",
  body: {
    billingCadence: "RECURRING",
    billingCycle: "anniversary",
    billingPeriod: "QUARTERLY",
    prorationBehavior: "create_prorations",
    targetPlanId: "<id>",
  },
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `id`                                                                                   | *string*                                                                               | :heavy_check_mark:                                                                     | Subscription ID                                                                        |
| `body`                                                                                 | [models.DtoSubscriptionChangeRequest](../../models/dto-subscription-change-request.md) | :heavy_check_mark:                                                                     | Subscription change preview request                                                    |