# DeleteSubscriptionLineItemRequest

## Example Usage

```typescript
import { DeleteSubscriptionLineItemRequest } from "flexprice-ts/sdk/models/operations";

let value: DeleteSubscriptionLineItemRequest = {
  id: "<id>",
  dtoDeleteSubscriptionLineItemRequest: {},
};
```

## Fields

| Field                                                                                                             | Type                                                                                                              | Required                                                                                                          | Description                                                                                                       |
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                              | *string*                                                                                                          | :heavy_check_mark:                                                                                                | Line Item ID                                                                                                      |
| `dtoDeleteSubscriptionLineItemRequest`                                                                            | [shared.DtoDeleteSubscriptionLineItemRequest](../../../sdk/models/shared/dtodeletesubscriptionlineitemrequest.md) | :heavy_check_mark:                                                                                                | Delete Line Item Request                                                                                          |