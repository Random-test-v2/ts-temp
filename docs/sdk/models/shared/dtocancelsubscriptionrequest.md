# DtoCancelSubscriptionRequest

## Example Usage

```typescript
import { DtoCancelSubscriptionRequest } from "flexprice-ts/sdk/models/shared";

let value: DtoCancelSubscriptionRequest = {
  cancellationType: "immediate",
};
```

## Fields

| Field                                                                                                           | Type                                                                                                            | Required                                                                                                        | Description                                                                                                     |
| --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| `cancelImmediatelyInovicePolicy`                                                                                | [shared.TypesCancelImmediatelyInvoicePolicy](../../../sdk/models/shared/typescancelimmediatelyinvoicepolicy.md) | :heavy_minus_sign:                                                                                              | N/A                                                                                                             |
| `cancellationType`                                                                                              | [shared.TypesCancellationType](../../../sdk/models/shared/typescancellationtype.md)                             | :heavy_check_mark:                                                                                              | N/A                                                                                                             |
| `prorationBehavior`                                                                                             | [shared.TypesProrationBehavior](../../../sdk/models/shared/typesprorationbehavior.md)                           | :heavy_minus_sign:                                                                                              | N/A                                                                                                             |
| `reason`                                                                                                        | *string*                                                                                                        | :heavy_minus_sign:                                                                                              | Reason for cancellation (for audit and business intelligence)                                                   |