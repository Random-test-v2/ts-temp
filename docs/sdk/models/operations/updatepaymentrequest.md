# UpdatePaymentRequest

## Example Usage

```typescript
import { UpdatePaymentRequest } from "flexprice-ts/sdk/models/operations";

let value: UpdatePaymentRequest = {
  id: "<id>",
  dtoUpdatePaymentRequest: {},
};
```

## Fields

| Field                                                                                   | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `id`                                                                                    | *string*                                                                                | :heavy_check_mark:                                                                      | Payment ID                                                                              |
| `dtoUpdatePaymentRequest`                                                               | [shared.DtoUpdatePaymentRequest](../../../sdk/models/shared/dtoupdatepaymentrequest.md) | :heavy_check_mark:                                                                      | Payment configuration                                                                   |