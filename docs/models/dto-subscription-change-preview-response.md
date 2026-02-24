# DtoSubscriptionChangePreviewResponse

Response showing the financial impact of a subscription plan change

## Example Usage

```typescript
import { DtoSubscriptionChangePreviewResponse } from "openapi/models";

let value: DtoSubscriptionChangePreviewResponse = {};
```

## Fields

| Field                                                                             | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `changeType`                                                                      | [models.TypesSubscriptionChangeType](../models/types-subscription-change-type.md) | :heavy_minus_sign:                                                                | N/A                                                                               |
| `currentPlan`                                                                     | [models.DtoPlanSummary](../models/dto-plan-summary.md)                            | :heavy_minus_sign:                                                                | N/A                                                                               |
| `effectiveDate`                                                                   | *string*                                                                          | :heavy_minus_sign:                                                                | effective_date is when the change would take effect                               |
| `metadata`                                                                        | Record<string, *string*>                                                          | :heavy_minus_sign:                                                                | metadata from the request                                                         |
| `newBillingCycle`                                                                 | [models.DtoBillingCycleInfo](../models/dto-billing-cycle-info.md)                 | :heavy_minus_sign:                                                                | N/A                                                                               |
| `nextInvoicePreview`                                                              | [models.DtoInvoicePreview](../models/dto-invoice-preview.md)                      | :heavy_minus_sign:                                                                | N/A                                                                               |
| `prorationDetails`                                                                | [models.DtoProrationDetails](../models/dto-proration-details.md)                  | :heavy_minus_sign:                                                                | N/A                                                                               |
| `subscriptionId`                                                                  | *string*                                                                          | :heavy_minus_sign:                                                                | subscription_id is the ID of the subscription being changed                       |
| `targetPlan`                                                                      | [models.DtoPlanSummary](../models/dto-plan-summary.md)                            | :heavy_minus_sign:                                                                | N/A                                                                               |
| `warnings`                                                                        | *string*[]                                                                        | :heavy_minus_sign:                                                                | warnings contains any warnings about the change                                   |