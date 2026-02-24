# DtoCreatePaymentRequest

## Example Usage

```typescript
import { DtoCreatePaymentRequest } from "flexprice-ts/sdk/models/shared";

let value: DtoCreatePaymentRequest = {
  amount: "31.14",
  currency: "Moroccan Dirham",
  destinationId: "<id>",
  destinationType: "INVOICE",
  paymentMethodType: "PAYMENT_LINK",
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `amount`                                                                                        | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `cancelUrl`                                                                                     | *string*                                                                                        | :heavy_minus_sign:                                                                              | N/A                                                                                             |
| `currency`                                                                                      | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `destinationId`                                                                                 | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `destinationType`                                                                               | [shared.TypesPaymentDestinationType](../../../sdk/models/shared/typespaymentdestinationtype.md) | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `idempotencyKey`                                                                                | *string*                                                                                        | :heavy_minus_sign:                                                                              | N/A                                                                                             |
| `metadata`                                                                                      | Record<string, *string*>                                                                        | :heavy_minus_sign:                                                                              | N/A                                                                                             |
| `paymentGateway`                                                                                | [shared.TypesPaymentGatewayType](../../../sdk/models/shared/typespaymentgatewaytype.md)         | :heavy_minus_sign:                                                                              | N/A                                                                                             |
| `paymentMethodId`                                                                               | *string*                                                                                        | :heavy_minus_sign:                                                                              | N/A                                                                                             |
| `paymentMethodType`                                                                             | [shared.TypesPaymentMethodType](../../../sdk/models/shared/typespaymentmethodtype.md)           | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `processPayment`                                                                                | *boolean*                                                                                       | :heavy_minus_sign:                                                                              | N/A                                                                                             |
| `saveCardAndMakeDefault`                                                                        | *boolean*                                                                                       | :heavy_minus_sign:                                                                              | N/A                                                                                             |
| `successUrl`                                                                                    | *string*                                                                                        | :heavy_minus_sign:                                                                              | N/A                                                                                             |