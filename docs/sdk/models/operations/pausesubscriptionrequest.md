# PauseSubscriptionRequest

## Example Usage

```typescript
import { PauseSubscriptionRequest } from "flexprice-ts/sdk/models/operations";

let value: PauseSubscriptionRequest = {
  id: "<id>",
  dtoPauseSubscriptionRequest: {
    pauseMode: "immediate",
  },
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `id`                                                                                            | *string*                                                                                        | :heavy_check_mark:                                                                              | Subscription ID                                                                                 |
| `dtoPauseSubscriptionRequest`                                                                   | [shared.DtoPauseSubscriptionRequest](../../../sdk/models/shared/dtopausesubscriptionrequest.md) | :heavy_check_mark:                                                                              | Pause subscription request                                                                      |