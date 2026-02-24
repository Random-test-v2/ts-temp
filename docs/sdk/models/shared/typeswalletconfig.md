# TypesWalletConfig

## Example Usage

```typescript
import { TypesWalletConfig } from "flexprice-ts/sdk/models/shared";

let value: TypesWalletConfig = {};
```

## Fields

| Field                                                                                                            | Type                                                                                                             | Required                                                                                                         | Description                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| `allowedPriceTypes`                                                                                              | [shared.TypesWalletConfigPriceType](../../../sdk/models/shared/typeswalletconfigpricetype.md)[]                  | :heavy_minus_sign:                                                                                               | AllowedPriceTypes is a list of price types that are allowed for the wallet<br/>nil means all price types are allowed |