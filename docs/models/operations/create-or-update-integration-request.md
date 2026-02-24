# CreateOrUpdateIntegrationRequest

## Example Usage

```typescript
import { CreateOrUpdateIntegrationRequest } from "openapi/models/operations";

let value: CreateOrUpdateIntegrationRequest = {
  provider: "<value>",
  body: {
    credentials: {
      "key": "<value>",
      "key1": "<value>",
    },
    name: "<value>",
    provider: "chargebee",
  },
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `provider`                                                                           | *string*                                                                             | :heavy_check_mark:                                                                   | Integration provider                                                                 |
| `body`                                                                               | [models.DtoCreateIntegrationRequest](../../models/dto-create-integration-request.md) | :heavy_check_mark:                                                                   | Integration creation request                                                         |