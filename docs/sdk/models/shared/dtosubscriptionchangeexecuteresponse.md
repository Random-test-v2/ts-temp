# DtoSubscriptionChangeExecuteResponse

Response after successfully executing a subscription plan change

## Example Usage

```typescript
import { DtoSubscriptionChangeExecuteResponse } from "flexprice-ts/sdk/models/shared";

let value: DtoSubscriptionChangeExecuteResponse = {
  invoice: {
    subscription: {
      latestInvoice: {
        subscription: {
          plan: {},
        },
      },
      plan: {},
    },
  },
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `changeType`                                                                                    | [shared.TypesSubscriptionChangeType](../../../sdk/models/shared/typessubscriptionchangetype.md) | :heavy_minus_sign:                                                                              | N/A                                                                                             |
| `creditGrants`                                                                                  | [shared.DtoCreditGrantResponse](../../../sdk/models/shared/dtocreditgrantresponse.md)[]         | :heavy_minus_sign:                                                                              | credit_grants contains any credit grants created for proration credits                          |
| `effectiveDate`                                                                                 | *string*                                                                                        | :heavy_minus_sign:                                                                              | effective_date is when the change took effect                                                   |
| `invoice`                                                                                       | [shared.DtoInvoiceResponse](../../../sdk/models/shared/dtoinvoiceresponse.md)                   | :heavy_minus_sign:                                                                              | N/A                                                                                             |
| `isScheduled`                                                                                   | *boolean*                                                                                       | :heavy_minus_sign:                                                                              | is_scheduled indicates if the change was scheduled or executed immediately                      |
| `metadata`                                                                                      | Record<string, *string*>                                                                        | :heavy_minus_sign:                                                                              | metadata from the request                                                                       |
| `newSubscription`                                                                               | [shared.DtoSubscriptionSummary](../../../sdk/models/shared/dtosubscriptionsummary.md)           | :heavy_minus_sign:                                                                              | N/A                                                                                             |
| `oldSubscription`                                                                               | [shared.DtoSubscriptionSummary](../../../sdk/models/shared/dtosubscriptionsummary.md)           | :heavy_minus_sign:                                                                              | N/A                                                                                             |
| `prorationApplied`                                                                              | [shared.DtoProrationDetails](../../../sdk/models/shared/dtoprorationdetails.md)                 | :heavy_minus_sign:                                                                              | N/A                                                                                             |
| `scheduleId`                                                                                    | *string*                                                                                        | :heavy_minus_sign:                                                                              | schedule_id is the ID of the created schedule (only if is_scheduled=true)                       |
| `scheduledAt`                                                                                   | *string*                                                                                        | :heavy_minus_sign:                                                                              | scheduled_at is when the change will execute (only if is_scheduled=true)                        |