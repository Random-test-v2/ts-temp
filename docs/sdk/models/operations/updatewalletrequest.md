# UpdateWalletRequest

## Example Usage

```typescript
import { UpdateWalletRequest } from "flexprice-ts/sdk/models/operations";

let value: UpdateWalletRequest = {
  id: "<id>",
  dtoUpdateWalletRequest: {},
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `id`                                                                                  | *string*                                                                              | :heavy_check_mark:                                                                    | Wallet ID                                                                             |
| `dtoUpdateWalletRequest`                                                              | [shared.DtoUpdateWalletRequest](../../../sdk/models/shared/dtoupdatewalletrequest.md) | :heavy_check_mark:                                                                    | Update wallet request                                                                 |