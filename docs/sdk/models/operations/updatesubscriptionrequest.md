# UpdateSubscriptionRequest

## Example Usage

```typescript
import { UpdateSubscriptionRequest } from "flexprice-ts/sdk/models/operations";

let value: UpdateSubscriptionRequest = {
  id: "<id>",
  dtoUpdateSubscriptionRequest: {},
};
```

## Fields

| Field                                                                                             | Type                                                                                              | Required                                                                                          | Description                                                                                       |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `id`                                                                                              | *string*                                                                                          | :heavy_check_mark:                                                                                | Subscription ID                                                                                   |
| `dtoUpdateSubscriptionRequest`                                                                    | [shared.DtoUpdateSubscriptionRequest](../../../sdk/models/shared/dtoupdatesubscriptionrequest.md) | :heavy_check_mark:                                                                                | Update Subscription Request                                                                       |