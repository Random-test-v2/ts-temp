# TopUpWalletRequest

## Example Usage

```typescript
import { TopUpWalletRequest } from "flexprice-ts/sdk/models/operations";

let value: TopUpWalletRequest = {
  id: "<id>",
  dtoTopUpWalletRequest: {
    transactionReason: "INVOICE_PAYMENT",
  },
};
```

## Fields

| Field                                                                               | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `id`                                                                                | *string*                                                                            | :heavy_check_mark:                                                                  | Wallet ID                                                                           |
| `dtoTopUpWalletRequest`                                                             | [shared.DtoTopUpWalletRequest](../../../sdk/models/shared/dtotopupwalletrequest.md) | :heavy_check_mark:                                                                  | Top up request                                                                      |