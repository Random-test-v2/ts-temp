# UpdateCreditGrantRequest

## Example Usage

```typescript
import { UpdateCreditGrantRequest } from "flexprice-ts/sdk/models/operations";

let value: UpdateCreditGrantRequest = {
  id: "<id>",
  dtoUpdateCreditGrantRequest: {},
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `id`                                                                                            | *string*                                                                                        | :heavy_check_mark:                                                                              | Credit Grant ID                                                                                 |
| `dtoUpdateCreditGrantRequest`                                                                   | [shared.DtoUpdateCreditGrantRequest](../../../sdk/models/shared/dtoupdatecreditgrantrequest.md) | :heavy_check_mark:                                                                              | Credit Grant configuration                                                                      |