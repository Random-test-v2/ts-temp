# DtoCustomerMultiCurrencyInvoiceSummary

## Example Usage

```typescript
import { DtoCustomerMultiCurrencyInvoiceSummary } from "flexprice-ts/sdk/models/shared";

let value: DtoCustomerMultiCurrencyInvoiceSummary = {};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `customerId`                                                                                  | *string*                                                                                      | :heavy_minus_sign:                                                                            | customer_id is the unique identifier of the customer                                          |
| `defaultCurrency`                                                                             | *string*                                                                                      | :heavy_minus_sign:                                                                            | default_currency is the primary currency for this customer                                    |
| `summaries`                                                                                   | [shared.DtoCustomerInvoiceSummary](../../../sdk/models/shared/dtocustomerinvoicesummary.md)[] | :heavy_minus_sign:                                                                            | summaries contains the invoice summaries for each currency                                    |