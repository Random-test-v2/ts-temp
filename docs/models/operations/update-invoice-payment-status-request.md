# UpdateInvoicePaymentStatusRequest

## Example Usage

```typescript
import { UpdateInvoicePaymentStatusRequest } from "openapi/models/operations";

let value: UpdateInvoicePaymentStatusRequest = {
  id: "<id>",
  body: {
    paymentStatus: "PARTIALLY_REFUNDED",
  },
};
```

## Fields

| Field                                                                                     | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `id`                                                                                      | *string*                                                                                  | :heavy_check_mark:                                                                        | Invoice ID                                                                                |
| `body`                                                                                    | [models.DtoUpdatePaymentStatusRequest](../../models/dto-update-payment-status-request.md) | :heavy_check_mark:                                                                        | Payment Status Update Request                                                             |