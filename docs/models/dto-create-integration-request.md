# DtoCreateIntegrationRequest

## Example Usage

```typescript
import { DtoCreateIntegrationRequest } from "openapi/models";

let value: DtoCreateIntegrationRequest = {
  credentials: {},
  name: "<value>",
  provider: "s3",
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `credentials`                                                    | Record<string, *string*>                                         | :heavy_check_mark:                                               | N/A                                                              |
| `name`                                                           | *string*                                                         | :heavy_check_mark:                                               | N/A                                                              |
| `provider`                                                       | [models.TypesSecretProvider](../models/types-secret-provider.md) | :heavy_check_mark:                                               | N/A                                                              |