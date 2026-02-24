# ResumeSubscriptionRequest

## Example Usage

```typescript
import { ResumeSubscriptionRequest } from "flexprice-ts/sdk/models/operations";

let value: ResumeSubscriptionRequest = {
  id: "<id>",
  dtoResumeSubscriptionRequest: {
    resumeMode: "immediate",
  },
};
```

## Fields

| Field                                                                                             | Type                                                                                              | Required                                                                                          | Description                                                                                       |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `id`                                                                                              | *string*                                                                                          | :heavy_check_mark:                                                                                | Subscription ID                                                                                   |
| `dtoResumeSubscriptionRequest`                                                                    | [shared.DtoResumeSubscriptionRequest](../../../sdk/models/shared/dtoresumesubscriptionrequest.md) | :heavy_check_mark:                                                                                | Resume subscription request                                                                       |