# UpdateWalletRequest

## Example Usage

```typescript
import { UpdateWalletRequest } from "openapi/models/operations";

let value: UpdateWalletRequest = {
  id: "<id>",
  body: {},
};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `id`                                                                       | *string*                                                                   | :heavy_check_mark:                                                         | Wallet ID                                                                  |
| `body`                                                                     | [models.DtoUpdateWalletRequest](../../models/dto-update-wallet-request.md) | :heavy_check_mark:                                                         | Update wallet request                                                      |