# PauseSubscriptionRequest

## Example Usage

```typescript
import { PauseSubscriptionRequest } from "openapi/models/operations";

let value: PauseSubscriptionRequest = {
  id: "<id>",
  body: {
    pauseMode: "immediate",
  },
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `id`                                                                                 | *string*                                                                             | :heavy_check_mark:                                                                   | Subscription ID                                                                      |
| `body`                                                                               | [models.DtoPauseSubscriptionRequest](../../models/dto-pause-subscription-request.md) | :heavy_check_mark:                                                                   | Pause subscription request                                                           |