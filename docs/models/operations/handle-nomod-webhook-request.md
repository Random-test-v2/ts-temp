# HandleNomodWebhookRequest

## Example Usage

```typescript
import { HandleNomodWebhookRequest } from "openapi/models/operations";

let value: HandleNomodWebhookRequest = {
  tenantId: "<id>",
  environmentId: "<id>",
};
```

## Fields

| Field                                | Type                                 | Required                             | Description                          |
| ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| `tenantId`                           | *string*                             | :heavy_check_mark:                   | Tenant ID                            |
| `environmentId`                      | *string*                             | :heavy_check_mark:                   | Environment ID                       |
| `xApiKey`                            | *string*                             | :heavy_minus_sign:                   | Nomod webhook secret (if configured) |