# ActivateSubscriptionRequest

## Example Usage

```typescript
import { ActivateSubscriptionRequest } from "flexprice-ts/sdk/models/operations";

let value: ActivateSubscriptionRequest = {
  id: "<id>",
  dtoActivateDraftSubscriptionRequest: {
    startDate: "<value>",
  },
};
```

## Fields

| Field                                                                                                           | Type                                                                                                            | Required                                                                                                        | Description                                                                                                     |
| --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                            | *string*                                                                                                        | :heavy_check_mark:                                                                                              | Subscription ID                                                                                                 |
| `dtoActivateDraftSubscriptionRequest`                                                                           | [shared.DtoActivateDraftSubscriptionRequest](../../../sdk/models/shared/dtoactivatedraftsubscriptionrequest.md) | :heavy_check_mark:                                                                                              | Activate Draft Subscription Request                                                                             |