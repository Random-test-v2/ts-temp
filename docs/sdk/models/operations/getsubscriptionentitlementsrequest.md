# GetSubscriptionEntitlementsRequest

## Example Usage

```typescript
import { GetSubscriptionEntitlementsRequest } from "flexprice-ts/sdk/models/operations";

let value: GetSubscriptionEntitlementsRequest = {
  id: "<id>",
};
```

## Fields

| Field                    | Type                     | Required                 | Description              |
| ------------------------ | ------------------------ | ------------------------ | ------------------------ |
| `id`                     | *string*                 | :heavy_check_mark:       | Subscription ID          |
| `featureIds`             | *string*[]               | :heavy_minus_sign:       | Feature IDs to filter by |