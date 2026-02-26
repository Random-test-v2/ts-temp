# ResumeSubscriptionRequest

## Example Usage

```typescript
import { ResumeSubscriptionRequest } from "openapi/models/operations";

let value: ResumeSubscriptionRequest = {
  id: "<id>",
  body: {
    resumeMode: "immediate",
  },
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `id`                                                                                   | *string*                                                                               | :heavy_check_mark:                                                                     | Subscription ID                                                                        |
| `body`                                                                                 | [models.DtoResumeSubscriptionRequest](../../models/dto-resume-subscription-request.md) | :heavy_check_mark:                                                                     | Resume subscription request                                                            |