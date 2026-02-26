# CreateOrUpdateIntegrationRequest

## Example Usage

```typescript
import { CreateOrUpdateIntegrationRequest } from "flexprice-ts/sdk/models/operations";

let value: CreateOrUpdateIntegrationRequest = {
  provider: "<value>",
  dtoCreateIntegrationRequest: {
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

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `provider`                                                                                      | *string*                                                                                        | :heavy_check_mark:                                                                              | Integration provider                                                                            |
| `dtoCreateIntegrationRequest`                                                                   | [shared.DtoCreateIntegrationRequest](../../../sdk/models/shared/dtocreateintegrationrequest.md) | :heavy_check_mark:                                                                              | Integration creation request                                                                    |