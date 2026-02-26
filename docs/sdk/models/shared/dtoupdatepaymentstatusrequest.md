# DtoUpdatePaymentStatusRequest

## Example Usage

```typescript
import { DtoUpdatePaymentStatusRequest } from "flexprice-ts/sdk/models/shared";

let value: DtoUpdatePaymentStatusRequest = {
  paymentStatus: "INITIATED",
};
```

## Fields

| Field                                                                         | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `amount`                                                                      | *string*                                                                      | :heavy_minus_sign:                                                            | amount is the optional payment amount to record                               |
| `paymentStatus`                                                               | [shared.TypesPaymentStatus](../../../sdk/models/shared/typespaymentstatus.md) | :heavy_check_mark:                                                            | N/A                                                                           |