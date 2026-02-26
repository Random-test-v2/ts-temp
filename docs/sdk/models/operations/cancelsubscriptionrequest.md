# CancelSubscriptionRequest

## Example Usage

```typescript
import { CancelSubscriptionRequest } from "flexprice-ts/sdk/models/operations";

let value: CancelSubscriptionRequest = {
  id: "<id>",
  dtoCancelSubscriptionRequest: {
    cancellationType: "immediate",
  },
};
```

## Fields

| Field                                                                                             | Type                                                                                              | Required                                                                                          | Description                                                                                       |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `id`                                                                                              | *string*                                                                                          | :heavy_check_mark:                                                                                | Subscription ID                                                                                   |
| `dtoCancelSubscriptionRequest`                                                                    | [shared.DtoCancelSubscriptionRequest](../../../sdk/models/shared/dtocancelsubscriptionrequest.md) | :heavy_check_mark:                                                                                | Cancel Subscription Request                                                                       |