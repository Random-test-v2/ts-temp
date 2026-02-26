# CreateSubscriptionLineItemRequest

## Example Usage

```typescript
import { CreateSubscriptionLineItemRequest } from "flexprice-ts/sdk/models/operations";

let value: CreateSubscriptionLineItemRequest = {
  id: "<id>",
  dtoCreateSubscriptionLineItemRequest: {},
};
```

## Fields

| Field                                                                                                             | Type                                                                                                              | Required                                                                                                          | Description                                                                                                       |
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                              | *string*                                                                                                          | :heavy_check_mark:                                                                                                | Subscription ID                                                                                                   |
| `dtoCreateSubscriptionLineItemRequest`                                                                            | [shared.DtoCreateSubscriptionLineItemRequest](../../../sdk/models/shared/dtocreatesubscriptionlineitemrequest.md) | :heavy_check_mark:                                                                                                | Create Line Item Request                                                                                          |