# DtoSubscriptionChangeRequest

Request object for changing a subscription plan (upgrade/downgrade)

## Example Usage

```typescript
import { DtoSubscriptionChangeRequest } from "flexprice-ts/sdk/models/shared";

let value: DtoSubscriptionChangeRequest = {
  billingCadence: "ONETIME",
  billingCycle: "calendar",
  billingPeriod: "WEEKLY",
  prorationBehavior: "none",
  targetPlanId: "<id>",
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `billingCadence`                                                                      | [shared.TypesBillingCadence](../../../sdk/models/shared/typesbillingcadence.md)       | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `billingCycle`                                                                        | [shared.TypesBillingCycle](../../../sdk/models/shared/typesbillingcycle.md)           | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `billingPeriod`                                                                       | [shared.TypesBillingPeriod](../../../sdk/models/shared/typesbillingperiod.md)         | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `billingPeriodCount`                                                                  | *number*                                                                              | :heavy_minus_sign:                                                                    | billing_period_count is the billing period count for the new subscription             |
| `changeAt`                                                                            | [shared.TypesScheduleType](../../../sdk/models/shared/typesscheduletype.md)           | :heavy_minus_sign:                                                                    | N/A                                                                                   |
| `metadata`                                                                            | Record<string, *string*>                                                              | :heavy_minus_sign:                                                                    | metadata contains additional key-value pairs for storing extra information            |
| `prorationBehavior`                                                                   | [shared.TypesProrationBehavior](../../../sdk/models/shared/typesprorationbehavior.md) | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `targetPlanId`                                                                        | *string*                                                                              | :heavy_check_mark:                                                                    | target_plan_id is the ID of the new plan to change to (required)                      |