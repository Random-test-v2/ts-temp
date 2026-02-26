# DtoCreateAPIKeyRequest

## Example Usage

```typescript
import { DtoCreateAPIKeyRequest } from "flexprice-ts/sdk/models/shared";

let value: DtoCreateAPIKeyRequest = {
  name: "<value>",
  type: "private_key",
};
```

## Fields

| Field                                                                   | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `expiresAt`                                                             | *string*                                                                | :heavy_minus_sign:                                                      | N/A                                                                     |
| `name`                                                                  | *string*                                                                | :heavy_check_mark:                                                      | N/A                                                                     |
| `serviceAccountId`                                                      | *string*                                                                | :heavy_minus_sign:                                                      | N/A                                                                     |
| `type`                                                                  | [shared.TypesSecretType](../../../sdk/models/shared/typessecrettype.md) | :heavy_check_mark:                                                      | N/A                                                                     |