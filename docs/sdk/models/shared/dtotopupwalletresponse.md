# DtoTopUpWalletResponse

## Example Usage

```typescript
import { DtoTopUpWalletResponse } from "flexprice-ts/sdk/models/shared";

let value: DtoTopUpWalletResponse = {};
```

## Fields

| Field                                                                                             | Type                                                                                              | Required                                                                                          | Description                                                                                       |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `invoiceId`                                                                                       | *string*                                                                                          | :heavy_minus_sign:                                                                                | Invoice ID if an invoice was created (only for PURCHASED_CREDIT_INVOICED)                         |
| `wallet`                                                                                          | [shared.DtoWalletResponse](../../../sdk/models/shared/dtowalletresponse.md)                       | :heavy_minus_sign:                                                                                | N/A                                                                                               |
| `walletTransaction`                                                                               | [shared.DtoWalletTransactionResponse](../../../sdk/models/shared/dtowallettransactionresponse.md) | :heavy_minus_sign:                                                                                | N/A                                                                                               |