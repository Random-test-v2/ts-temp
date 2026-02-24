# DtoCreateIntegrationRequest

## Example Usage

```typescript
import { DtoCreateIntegrationRequest } from "flexprice-ts/sdk/models/shared";

let value: DtoCreateIntegrationRequest = {
  credentials: {},
  name: "<value>",
  provider: "s3",
};
```

## Fields

| Field                                                                           | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `credentials`                                                                   | Record<string, *string*>                                                        | :heavy_check_mark:                                                              | N/A                                                                             |
| `name`                                                                          | *string*                                                                        | :heavy_check_mark:                                                              | N/A                                                                             |
| `provider`                                                                      | [shared.TypesSecretProvider](../../../sdk/models/shared/typessecretprovider.md) | :heavy_check_mark:                                                              | N/A                                                                             |