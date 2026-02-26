# DeleteCreditGrantRequest

## Example Usage

```typescript
import { DeleteCreditGrantRequest } from "flexprice-ts/sdk/models/operations";

let value: DeleteCreditGrantRequest = {
  id: "<id>",
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `id`                                                                                            | *string*                                                                                        | :heavy_check_mark:                                                                              | Credit Grant ID                                                                                 |
| `dtoDeleteCreditGrantRequest`                                                                   | [shared.DtoDeleteCreditGrantRequest](../../../sdk/models/shared/dtodeletecreditgrantrequest.md) | :heavy_minus_sign:                                                                              | Optional: effective_date for subscription-scoped grants                                         |