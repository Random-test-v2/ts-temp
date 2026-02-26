# DtoCancelSubscriptionRequest

## Example Usage

```typescript
import { DtoCancelSubscriptionRequest } from "openapi/models";

let value: DtoCancelSubscriptionRequest = {
  cancellationType: "immediate",
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `cancelImmediatelyInovicePolicy`                                                                   | [models.TypesCancelImmediatelyInvoicePolicy](../models/types-cancel-immediately-invoice-policy.md) | :heavy_minus_sign:                                                                                 | N/A                                                                                                |
| `cancellationType`                                                                                 | [models.TypesCancellationType](../models/types-cancellation-type.md)                               | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `prorationBehavior`                                                                                | [models.TypesProrationBehavior](../models/types-proration-behavior.md)                             | :heavy_minus_sign:                                                                                 | N/A                                                                                                |
| `reason`                                                                                           | *string*                                                                                           | :heavy_minus_sign:                                                                                 | Reason for cancellation (for audit and business intelligence)                                      |