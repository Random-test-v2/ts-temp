# UpdateSubscriptionLineItemRequest

## Example Usage

```typescript
import { UpdateSubscriptionLineItemRequest } from "flexprice-ts/sdk/models/operations";

let value: UpdateSubscriptionLineItemRequest = {
  id: "<id>",
  dtoUpdateSubscriptionLineItemRequest: {},
};
```

## Fields

| Field                                                                                                             | Type                                                                                                              | Required                                                                                                          | Description                                                                                                       |
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                              | *string*                                                                                                          | :heavy_check_mark:                                                                                                | Line Item ID                                                                                                      |
| `dtoUpdateSubscriptionLineItemRequest`                                                                            | [shared.DtoUpdateSubscriptionLineItemRequest](../../../sdk/models/shared/dtoupdatesubscriptionlineitemrequest.md) | :heavy_check_mark:                                                                                                | Update Line Item Request                                                                                          |