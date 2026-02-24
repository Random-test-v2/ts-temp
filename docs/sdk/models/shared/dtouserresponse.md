# DtoUserResponse

## Example Usage

```typescript
import { DtoUserResponse } from "flexprice-ts/sdk/models/shared";

let value: DtoUserResponse = {};
```

## Fields

| Field                                                                       | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `email`                                                                     | *string*                                                                    | :heavy_minus_sign:                                                          | Empty for service accounts                                                  |
| `id`                                                                        | *string*                                                                    | :heavy_minus_sign:                                                          | N/A                                                                         |
| `roles`                                                                     | *string*[]                                                                  | :heavy_minus_sign:                                                          | N/A                                                                         |
| `tenant`                                                                    | [shared.DtoTenantResponse](../../../sdk/models/shared/dtotenantresponse.md) | :heavy_minus_sign:                                                          | N/A                                                                         |
| `type`                                                                      | [shared.TypesUserType](../../../sdk/models/shared/typesusertype.md)         | :heavy_minus_sign:                                                          | N/A                                                                         |