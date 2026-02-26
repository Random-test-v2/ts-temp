# PreviewSubscriptionChangeRequest

## Example Usage

```typescript
import { PreviewSubscriptionChangeRequest } from "flexprice-ts/sdk/models/operations";

let value: PreviewSubscriptionChangeRequest = {
  id: "<id>",
  dtoSubscriptionChangeRequest: {
    billingCadence: "RECURRING",
    billingCycle: "anniversary",
    billingPeriod: "QUARTERLY",
    prorationBehavior: "create_prorations",
    targetPlanId: "<id>",
  },
};
```

## Fields

| Field                                                                                             | Type                                                                                              | Required                                                                                          | Description                                                                                       |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `id`                                                                                              | *string*                                                                                          | :heavy_check_mark:                                                                                | Subscription ID                                                                                   |
| `dtoSubscriptionChangeRequest`                                                                    | [shared.DtoSubscriptionChangeRequest](../../../sdk/models/shared/dtosubscriptionchangerequest.md) | :heavy_check_mark:                                                                                | Subscription change preview request                                                               |