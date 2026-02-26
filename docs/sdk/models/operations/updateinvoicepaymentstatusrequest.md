# UpdateInvoicePaymentStatusRequest

## Example Usage

```typescript
import { UpdateInvoicePaymentStatusRequest } from "flexprice-ts/sdk/models/operations";

let value: UpdateInvoicePaymentStatusRequest = {
  id: "<id>",
  dtoUpdatePaymentStatusRequest: {
    paymentStatus: "PARTIALLY_REFUNDED",
  },
};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `id`                                                                                                | *string*                                                                                            | :heavy_check_mark:                                                                                  | Invoice ID                                                                                          |
| `dtoUpdatePaymentStatusRequest`                                                                     | [shared.DtoUpdatePaymentStatusRequest](../../../sdk/models/shared/dtoupdatepaymentstatusrequest.md) | :heavy_check_mark:                                                                                  | Payment Status Update Request                                                                       |